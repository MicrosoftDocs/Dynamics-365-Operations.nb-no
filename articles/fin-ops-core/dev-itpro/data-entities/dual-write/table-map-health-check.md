---
title: Feilkoder for tilstandskontroll for tabelltilordning
description: Denne artikkelen beskriver feilkoder for tilstandskontroll for tabelltilordning.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 3ae78077fc716311c38620b14665af3983a44c2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884090"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Feilkoder for tilstandskontroll for tabelltilordning

[!include [banner](../../includes/banner.md)]



Denne artikkelen beskriver feilkoder for tilstandskontroll for tabelltilordning.

## <a name="error-100"></a>Feil 100

Feilmeldingen er "Minimum nødvendig Finance og Operations-plattformversjon er PU 43 for å kjøre Finance og operations-anbefalinger."

Funksjonen krever plattformoppdateringer for versjon 10.0.19 eller senere av økonomi- og driftsapper.

## <a name="error-400"></a>Feil 400

Feilmeldingen er: "Ingen registreringsdata for forretningshendelser funnet for enheten \{Finance og Operations UniqueEntityName\}, som betyr at tilordningen ikke kjører, eller at alle felttilordningen er enveis."

## <a name="error-500"></a>Feil 500

Feilmeldingen er at "ingen prosjektkonfigurasjoner blir funnet for \{-prosjektprosjektnavnet\}. Dette kan enten være at prosjektet ikke er aktivert, eller alle felttilordningene er enveis fra Customer Engagement til Finance og Operations."

Kontroller tilordningene for tabelltilordningen. Hvis de er enveis fra Customer Engagement-apper til økonomi- og driftsapper, genereres ingen trafikk for direkte synkronisering fra økonomi- og driftsapper til Dataverse.

## <a name="error-900"></a>Feil 900

Feilmeldingen er: "Ugyldig kildefilter \{sourceFilter\}-format for enheten \{Finance og Operations UniqueEntityName\}."

Kildefilteret som er angitt på tabelltilordningen for økonomi- og driftsapper, er ikke syntaktisk korrekt. Hvis du vil validere filterkriteriene, kan du se [Feilsøke direkte synkroniseringsproblemer](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Feil 1000

Feilmeldingen er: "Enhet \{Finance og Operations UniqueEntityName\}-spørring som brukes for direkte synkronisering med dobbel skriving, er \{Finance og Operations EntityFilterQueryString\}. Poster som oppfyller spørringskriteriene, blir plukket opp for direkte synkronisering."

Enhetsspørringen som ble returnert, er den støttende SQL-spørringen for enheten. Se etter interne koblinger eller filtre på spørringen som bestemmer forretningsdataene som blir plukket opp for direktesynkronisering. Interne koblinger og filtre er obligatoriske betingelser som må oppfylles for hver post som plukkes opp for direktesynkronisering med skrivetilgang.

## <a name="error-1300"></a>Feil 1300

Feilmeldingen er: "Virtuelle felter \{s.EntityFieldName\} for enheten \{Finance og Operations EntityMetadata.EntityProperties.LogicalEntityName\} kan ikke spores for dobbel skriving."

Virtuelle felter fra tabeller i Finance og Operations er ikke aktivert for sporing. Direkte synkronisering kan synkronisere dataene, men den vil ikke være i stand til å plukke opp endringene som gjøres i kolonnene.

## <a name="error-1500"></a>Feil 1500

Feilmeldingen er at "Det skal være minst ett felt som er tilordnet til et ikke-oppslagsfelt på Customer Engagement for å aktivere sporing på datakilden \{datasource.DataSourceName\}."

Datakilden fra enheten har ikke noen felt som er tilordnet for dobbel skriving. Endringer i den underliggende tabellen spores ikke for dobbel skriving.

## <a name="error-1600"></a>Feil 1600

Feilmeldingen er: "Datakilde: \{datasource.DataSourceName\} for enheten \{Finance og Operations EntityMetadata.EntityProperties.LogicalEntityName\} har et område. Bare poster som oppfyller områdebetingelsen, hentes for utgående."

Enheter i økonomi- og driftsapper kan ha datakilder der filterområder er aktivert. Disse områdene definerer postene som plukkes opp som del av direktesynkronisering. Hvis noen poster hoppes over fra økonomi- og driftsapper til Dataverse, må du kontrollere om postene oppfyller områdekriteriene for enheten. En enkel måte å utføre denne kontrollen på, er å kjøre en SQL-spørring som ligner på følgende eksempel.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Feil 1700

Feilmeldingen er "Tabell: \{datasourceTable.Key.subscribedTableName\} for enhet \{datasourceTable.Key.entityName\} spores for enhet \{origTableToEntityMaps.EntityName\}. Samme tabeller som spores for flere enheter, kan påvirke systemytelsen for synkroniseringstransaksjoner."

Hvis den samme tabellen spores av flere enheter, vil alle endringer i tabellen utløse evaluering av dobbel skriving for de koblede enhetene. Selv om filtersetningene bare sender de gyldige postene, kan evalueringen forårsake et ytelsesproblem hvis det finnes langsiktige spørringer eller ikkeoptimaliserte spørringsplaner. Dette problemet kan kanskje ikke unngås fra forretningsperspektivet. Hvis det imidlertid er mange kryssende tabeller på tvers av flere enheter, bør du vurdere å forenkle enheten eller kontrollere optimaliseringer for enhetsspørringer.

## <a name="error-1800"></a>Feil 1800
Feilmeldingen er "Datakilde: {} for enheten CustCustomerV3Entity inkluderer en områdeverdi. Inngående postupserter fra Dataverse til Økonomi- og drift kan påvirkes av områdeverdier på enhet. Test registreringsoppdateringer fra Dataverse til Økonomi og drift med poster som ikke samsvarer med filterkriteriene for å validere innstillingene dine.

Hvis det er angitt et område for enheten i økonomi- og driftsapper, bør innkommende synkronisering fra Dataverse til økonomi- og driftsapper testes for oppdateringsvirkemåte for poster som ikke samsvarer med dette områdekriteriet. Alle poster som ikke samsvarer med området, blir behandlet som en innsettingsoperasjon av enheten. Hvis det finnes en eksisterende post i den underliggende tabellen, vil innsettingen mislykkes. Vi anbefaler at du tester dette brukstilfellet for alle scenarier før du distribuerer til produksjon.

## <a name="error-1900"></a>Feil 1900
Feilmeldingen er: Enheten har {} datakilder som ikke spores for utgående dobbelt skriving. Dette kan påvirke ytelsen for direktesynkroniseringsspørring. Ommodeller enheten i økonomi- og drift for å fjerne ubrukte datakilder og tabeller, eller implementere getEntityRecordIdsImpactedByTableChange for å optimalisere kjøretidsspørringene.

Hvis det er mange datakilder som ikke brukes til sporing i faktisk livesynkronisering fra økonomi- og driftsapper, kan enhetsytelsen påvirke direktesynkronisering. Når du skal optimalisere de sporede tabellene, bruker du metoden getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Feil 5000
Feilmeldingen er at synkrone plugin-moduler registreres for datastyringshendelser for enhetskontoer. Disse kan påvirke opprinnelig synkronisering og ytelsen for live sync-import til Dataverse. Hvis du vil ha best mulig ytelse, kan du endre pluginmodulene til asynkron behandling. Liste over registrerte plugin-moduler {}.

Synkrone plugin-moduler på en Dataverse-enhet kan påvirke direkte synkronisering og innledende synkroniseringsytelse fordi den legges på transaksjonsbelastningen. Den anbefalte tilnærmingen er å enten slå av plugin-modulene eller gjøre disse asynkrone hvis du har treg belastning i innledende synkronisering eller synkroniserer for en bestemt enhet.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
