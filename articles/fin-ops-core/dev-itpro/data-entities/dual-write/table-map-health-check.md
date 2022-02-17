---
title: Feilkoder for tilstandskontroll for tabelltilordning
description: Dette emnet beskriver feilkoder for tilstandskontroll for tabelltilordning.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061284"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Feilkoder for tilstandskontroll for tabelltilordning

[!include [banner](../../includes/banner.md)]



Dette emnet beskriver feilkoder for tilstandskontroll for tabelltilordning.

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

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
