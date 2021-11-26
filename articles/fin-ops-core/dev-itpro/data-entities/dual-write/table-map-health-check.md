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
ms.openlocfilehash: c2d1f1e39a5ddccddf6fbbf524ff7eb0945b3c32
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782242"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Feilkoder for tilstandskontroll for tabelltilordning

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet beskriver feilkoder for tilstandskontroll for tabelltilordning.

## <a name="error-100"></a>Feil 100

Feilmeldingen er "Minimum nødvendig Finance and Operations-plattformversjon er PU 43 for å kjøre Finance and Operations-anbefalinger."

Funksjonen krever plattformoppdateringer for versjon 10.0.19 eller senere Finance and Operations-apper.

## <a name="error-400"></a>Feil 400

Feilmeldingen er: "Ingen registreringsdata for forretningshendelser funnet for enheten \{Finance and Operations UniqueEntityName\}, som betyr at tilordningen ikke kjører, eller at alle felttilordningen er enveis."

## <a name="error-500"></a>Feil 500

Feilmeldingen er at "ingen prosjektkonfigurasjoner blir funnet for \{-prosjektprosjektnavnet\}. Dette kan enten være at prosjektet ikke er aktivert, eller alle felttilordningene er enveis fra Customer Engagement til Finance and Operations."

Kontroller tilordningene for tabelltilordningen. Hvis de er enveis fra Customer Engagement-apper til Finance and Operations-apper, genereres ingen trafikk for direkte synkronisering fra Finance and Operations-apper til Dataverse.

## <a name="error-900"></a>Feil 900

Feilmeldingen er om "ugyldig kildefilter \{sourceFilter\}-format for enheten \{Finance and Operations UniqueEntityName\}."

Kildefilteret som er angitt på tabelltilordningen for Finance and Operations-apper, er ikke syntaktisk korrekt. Hvis du vil validere filterkriteriene, kan du se [Feilsøke direkte synkroniseringsproblemer](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Feil 1000

Feilmeldingen er "Enhet \{Finance and Operations UniqueEntityName\}-spørring som brukes for direkte synkronisering med dobbel skriving, er \{Finance and Operations EntityFilterQueryString\}. Poster som oppfyller spørringskriteriene, blir plukket opp for direkte synkronisering."

Enhetsspørringen som ble returnert, er den støttende SQL-spørringen for enheten. Se etter interne koblinger eller filtre på spørringen som bestemmer forretningsdataene som blir plukket opp for direktesynkronisering. Interne koblinger og filtre er obligatoriske betingelser som må oppfylles for hver post som plukkes opp for direktesynkronisering med skrivetilgang.

## <a name="error-1300"></a>Feil 1300

Feilmeldingen er at "virtuelle felt \{s.EntityFieldName\} for enhet \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} ikke kan spores for dobbel skriving."

Virtuelle felt fra Finance and Operations-tabeller som ikke er aktivert for sporing. Direkte synkronisering kan synkronisere dataene, men den vil ikke være i stand til å plukke opp endringene som gjøres i kolonnene.

## <a name="error-1500"></a>Feil 1500

Feilmeldingen er at "Det skal være minst ett felt som er tilordnet til et ikke-oppslagsfelt på Customer Engagement for å aktivere sporing på datakilden \{datasource.DataSourceName\}."

Datakilden fra enheten har ikke noen felt som er tilordnet for dobbel skriving. Endringer i den underliggende tabellen spores ikke for dobbel skriving.

## <a name="error-1600"></a>Feil 1600

Feilmeldingen er "Datakilde: \{datasource.DataSourceName\} for enhet \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} har et område. Bare poster som oppfyller områdebetingelsen, hentes for utgående."

Enheter i Finance and Operations-apper kan ha datakilder der filterområder er aktivert. Disse områdene definerer postene som plukkes opp som del av direktesynkronisering. Hvis noen poster hoppes over fra Finance and Operations-apper til Dataverse, må du kontrollere om postene oppfyller områdekriteriene for enheten. En enkel måte å utføre denne kontrollen på, er å kjøre en SQL-spørring som ligner på følgende eksempel.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Feil 1700

Feilmeldingen er "Tabell: \{datasourceTable.Key.subscribedTableName\} for enhet \{datasourceTable.Key.entityName\} spores for enhet \{origTableToEntityMaps.EntityName\}. Samme tabeller som spores for flere enheter, kan påvirke systemytelsen for synkroniseringstransaksjoner."

Hvis den samme tabellen spores av flere enheter, vil alle endringer i tabellen utløse evaluering av dobbel skriving for de koblede enhetene. Selv om filtersetningene bare sender de gyldige postene, kan evalueringen forårsake et ytelsesproblem hvis det finnes langsiktige spørringer eller ikkeoptimaliserte spørringsplaner. Dette problemet kan kanskje ikke unngås fra forretningsperspektivet. Hvis det imidlertid er mange kryssende tabeller på tvers av flere enheter, bør du vurdere å forenkle enheten eller kontrollere optimaliseringer for enhetsspørringer.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
