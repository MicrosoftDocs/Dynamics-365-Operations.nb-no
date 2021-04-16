---
title: Regnskapsdistribusjoner
description: Dette emnet inneholder informasjon om regnskapsdistribusjoner og beskriver alternativene som er tilgjengelige for behandling av dem.
author: ShylaThompson
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution
audience: Application User
ms.reviewer: roschlom
ms.custom: 17231
ms.assetid: 9030355d-8e6e-408b-9e7d-7b346eaa652c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c17c2e00c8c3b32062f70baf1da76a04dcd5d924
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820961"
---
# <a name="accounting-distributions"></a>Regnskapsdistribusjoner

[!include [banner](../includes/banner.md)]

Dette emnet inneholder informasjon om regnskapsdistribusjoner og beskriver alternativene som er tilgjengelige for behandling av dem. Regnskapsdistribusjoner brukes til å tildele pengebeløp for et kildedokument til bestemte finanskontoer. 

Regnskapsdistribusjoner er en funksjonalitet for hele programmet som brukes og utvides av hvert kildedokument, for eksempel en bestilling, leverandørfaktura, utgiftsrapport og fritekstfaktura. En standard regnskapsdistribusjon genereres som standard for hver kildedokumentlinje og hvert pengebeløp, og kan endres basert på betingelser. 

> [!NOTE] 
> Enkelte dokumenter støtter også pengebeløp i topptekstdokument, for eksempel gebyr for bestillinger og fakturaer. 

Generiske funksjoner for regnskapsdistribusjon gir følgende alternativer for behandling av regnskapsdistribusjoner:

-   **Fordel beløp** – Vis og endre regnskapsdistribusjonene for et enkelt dokumenthode eller en enkelt linje og eventuelle underordnede linjer, for eksempel avgifter eller gebyrer.
    -   Når det gjelder de øverste pengebeløpsdistribusjonene (overordnede distribusjoner), kan hovedkontoen og finansdimensjonene redigeres direkte i den segmenterte oppføringskontrollen i rutenettet. Den utvidede prisen er et typisk eksempel på en slik overordnet distribusjon.
    -   Distribusjonsbeløpene er basert på noteringsvalutaen for dokumentet. Denne valutaen er vanligvis transaksjonsvalutaen. Regnskaps- og rapporteringsvalutabeløp genereres som en del av underfinansregnskap.
    -   Distribusjonene viser regnskapsdatoen og regnskapshendelsen. Vanligvis settes regnskapshendelsen til **Ingen** til dokumentet er postert/journalført. På dette tidspunktet blir regnskapshendelsen **Opprinnelig**. Etter at distribusjonene er postert, kan du ikke endre dem.
    -   **Del**-knappen kan være aktivert for overordnede distribusjoner. **Del** genererer nye regnskapsdistribusjoner, og delingen kan være basert på prosent, beløp eller antall.
    -   **Fordel likt**-knappen kan brukes sammen med **Del** til å fordele beløpet likt på tvers av alle distribusjoner automatisk.
    -   **Tilbakestill**-knappen kan aktiveres for overordnede distribusjoner når det finnes flere distribusjoner. **Tilbakestill** reverserer manuelle endringer i distribusjonen ved å slette alle eksisterende distribusjoner og generere de standard distribusjonene på nytt.
    -   Alle underordnede distribusjoner, for eksempel rabatt, tillegg og merverdiavgift, følger alltid den overordnede distribusjonen. Du kan vise relasjonen overordnet/underordnet på **Referanse** &gt; **Overordnet informasjon**.
    -   Hovedkontoen og finansdimensjonen kan redigeres for underordnede også.
    -   Finansdimensjonene på regnskapsdistribusjonene følger et tilbakestillingsmønster som et dokument kan utvide.
    -   Avviksdistribusjoner kan genereres i samsvarsscenarier, for eksempel samsvar mellom en leverandørfaktura og en bestilling. Du kan vise samsvarsrelasjonene mellom regnskapsdistribusjon på **Referanse** &gt; **Dokumentinformasjon**.
    -   **Rett**-knappen vises og er aktivert for dokumenter som støtter rettelser. **Rett** oppretter nye distribusjoner. Først opprettes distribusjoner som de opprinnelige distribusjonene. Disse distribusjonene kan ikke endres. Deretter opprettes nye, riktige regnskapsdistribusjoner. Disse distribusjonene kan endres hvis de opprinnelige distribusjonene kan endres.
    -   **Prosjektdetaljer**-knappen aktiveres som en utvidelse når en linje knyttes til et prosjekt. Prosjektregnskapsdistribusjoner gjøre at du kan endre detaljer, for eksempel finansieringskilden og linjeegenskapen.
    -   Du kan vise gjeldende regnskapsstatus for dokument i **Referanse**. Statusen er for hele dokumentet og angir om dokumentet er under behandling eller fullført.
-   **Vis distribusjoner** – Vis regnskapsdistribusjonene for alle linjene og pengebeløpene i dokumentet. Du kan ikke endre regnskapsdistribusjonene fra denne visningen.

I versjon 10.0.13 er det lagt til en funksjon som validerer tabellen for regnskapsdistribusjon for å sikre at nye felt er riktig satt opp. Denne funksjonen kalles **Aktiver ytterligere validering av data for dokumenter som bruker regnskapsrammeverket for kildedokumenter**. Hvis du vil bruke funksjonen, må du aktivere den ved hjelp av arbeidsområdet for **Funksjonsbehandling**. Hvis du vil aktivere funksjonen, kan du søke etter funksjonsnavnet i **Søk**-feltet på siden **Funksjonsbehandling** og deretter velge **Aktiver nå**.

Se [Regnskapsdistribusjoner og underfinansjournaloppføringer for leverandørfakturaer](accounting-distributions-subledger-journal-entries-vendor-invoices.md) for mer informasjon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]