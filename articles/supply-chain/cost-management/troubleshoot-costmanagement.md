---
title: Feilsøk kostnadsstyring
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med kostnadsstyring.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b8c527e578fee6abfeeade99fba8070365c020bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983856"
---
# <a name="troubleshoot-cost-management"></a>Feilsøk kostnadsstyring

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med kostnadsstyring.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funksjonshullene mellom rapporter om lagerverdi/aldersfordelinger og deres lagringsversjoner

Funksjonene [Lagring av rapport for aldersfordeling for lager](inventory-aging-report-storage.md) og [Rapport for oppbevaring av lagerverdi](inventory-value-report-storage.md) gjør det mulig for Supply Chain Management å vise store mengder lagertransaksjoner. I hvert tilfelle lagres rapportresultatene for lesing og eksport, i motsetning til ikke-lagerversjoner av disse rapportene. Det finnes imidlertid en del funksjonalitet som finnes i ikke-lagerversjoner av disse rapportene, som ikke finnes i lagerversjonene. Underdelene nedenfor gir en oversikt over forskjellene og løsninger.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Lagerrapporter inkluderer ikke delsummer, selv om de er aktivert i rapportoppsettet

Delsummer kan forårsake problemer når resultatet eksporteres, spesielt hvis brukerne endrer postrekkefølgen.

Hvis du vil kontrollere delsummene, kan du eksportere resultatet til Microsoft Excel. Hvis du vil kontrollere delsummer i Supply Chain Management, kan du også bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å aktivere funksjonene *Ny rutenettetkontroll* og *(Forhåndsversjon) Gruppering i rutenett*, som gir en mye mer fleksibel måte å se delsummen på for alle grupper etter kolonne. Hvis du vil ha mer informasjon, se [Rutenettfunksjoner](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Rapport for oppbevaring av lagerverdi støtter ikke finanskontoinformasjon

Du kan kjøre råbalansen for å hente saldoen for lagerkontoene og sammenligne dem med **rapporten for oppbevaring av lagerverdi**.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Advarsler eller feil vises når du endrer en status for en finansperiode uten å lukke lager

Microsoft innførte følgende valideringer for å forhindre problemer som skyldes feil periodeavslutningsprosess rundt etterkalkulering. Hvis du får en av følgende feilmeldinger, kan du se [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) for å få mer informasjon om hvordan du løser disse problemene.

- Du er i ferd med å utføre en omberegning med en dato %1 (10-02-2019). Den siste registrerte omberegningen ble utført i en foregående periode med en dato %2 (20-01-2019). Ingen kjøringer av en lagerlukking med en dato %3 (31-01-2019) som samsvarer med periodeslutt, er registrert. Husk å kjøre en lagerlukking per %3 (31-01-2019) som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

- Du er i ferd med å endre statusen for finansperioden %1 til %2. Ingen kjøringer av lagerlukking med en dato %3 som samsvarer med periodeslutt, er registrert. Utfør en lagerlukking per %3 som samsvarer med periodeslutt før, du endrer statusen. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført. Rapportert fra juridisk enhet %4. For øyeblikket er den bare til informasjon, men senere blir det nødvendig å utføre en slik handling.

- Kontostrukturen %1 er endret. En eller flere hovedkontoer %2 finnes ikke lenger. Disse hovedkontoene kreves av %3 med en dato %4. Legg til disse hovedkontoene i kontostrukturen %1 før du kan gjenoppta %3-jobben. For øyeblikket er den bare til informasjon, men senere blir det nødvendig å utføre en slik handling.

- Du er i ferd med å utføre en lagerlukking med en dato %1 (31-01-2019). Ingen kjøringer av beregning av backflush-etterkalkulering med en dato %2 (31-01-2019) som samsvarer med periodeslutt, er registrert. Husk å kjøre en beregning av backflush-etterkalkulering med en dato for %3 (31-01-2019) som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik blir kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

- Du er i ferd med å utføre en beregning av backflush-etterkalkulering med en dato %1 (28-02-2019). Den siste registrerte beregningen av backflush-etterkalkulering ble utført i en foregående periode med en dato %2 (31-01-2019). Ingen kjøringer av en lagerlukking med en dato %3 (31-01-2019) som samsvarer med en periodeslutt, er registrert.
Husk å kjøre en lagerlukking per %3 (31-01-2019) som samsvarer med en periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik er kanskje ikke riktige i underfinansjournaler eller økonomimodulen før lagerlukkingen er utført.

## <a name="inventory-aging-report-discrepancies"></a>Avvik i rapport for aldersfordeling for lager

**Rapport for aldersfordeling for lager** viser ulike verdier når de vises i forskjellige lagerdimensjoner (for eksempel område eller lager). Hvis du vil ha mer informasjon om rapporteringslogikken, kan du se [Eksempler og logikk for rapport for aldersfordeling for lager](inventory-aging-report.md).

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Det oppstår en oppdateringskonflikt når lagervurderingsmetoden er enten Standardkostnad eller Glidende gjennomsnitt

Når du posterer dokumenter, for eksempel lagerjournaler, bestillingsfakturaer eller salgsordrefakturaer parallelt for å forbedre skalerbarhet og ytelse, kan det hende at du får en feilmelding om en oppdateringskonflikt, og det kan hende at enkelte dokumenter ikke posteres. Dette problemet kan oppstå når lagervurderingsmetoden er enten *Standardkostnad* eller *Glidende gjennomsnitt*. Begge disse metodene er permanente etterkalkuleringsmetoder. Den endelige kostnaden fastsettes med andre ord ved postering.

Hvis du bruker metoden *Glidende gjennomsnitt*, ligner feilmeldingen på dette eksemplet:

> Lagerverdien xx,xx forventes ikke etter den proporsjonale utgiftsberegningen

Hvis du bruker metoden *Standardkostnad*, ligner feilmeldingen på dette eksemplet:

> Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen. Verdi = xx,xx, Ant. = yy,yy, Standardkostnad = zz,zz

Før Microsoft gir ut en løsning på problemet, må du vurdere å bruke følgende midlertidige løsninger for å unngå eller minimere disse feilene:

- Poster de mislykkede dokumentene på nytt.
- Opprett dokumenter med færre linjer.
- Unngå desimalverdier i standardkostnaden. Prøv å definere standardkostnaden slik at **Prisantall**-feltet settes til *1*. Hvis du må angi en verdi for **Prisantall** som er større enn *1*, kan du prøve å redusere antallet desimalplasser i enhetens standardkostnad. (Ideelt sett bør det være færre enn to desimalplasser.) Unngå å definere innstillinger for standardkostnad der for eksempel **Pris** = *10* og **Prisantall** = *3*, fordi disse vil gi en standardkostnad for en enhet på 3,333333 (der desimalverdien gjentas).
- I de fleste dokumenter bør du unngå å ha flere linjer som har samme kombinasjon av produkt og økonomiske lagerdimensjoner.
- Reduser graden av parallellisering. (I dette tilfellet kan systemet bli raskere fordi det oppstår færre oppdateringskonflikter og nye forsøk.)
