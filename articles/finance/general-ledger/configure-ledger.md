---
title: Konfigurere finans
description: Dette emnet gir informasjon om hvordan du konfigurerer finans for hver juridiske enhet. Det inneholder informasjon om hvordan du velger valutaer, regnskapskalendere, kontoplanen og kontostrukturene som skal brukes med hver juridiske enhet.
author: kweekley
manager: ''
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 929ab7ae66a217de836ce49373faed76325c4d3a
ms.sourcegitcommit: ac0a676c91e3053ad7f9432d576c9af3ff98a99a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4446613"
---
# <a name="configure-ledgers"></a>Konfigurere finans

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om hvordan du konfigurerer finans for hver juridiske enhet. Det inneholder informasjon om hvordan du velger valutaer, regnskapskalendere, kontoplanen og kontostrukturene som skal brukes med hver juridiske enhet.

## <a name="selecting-the-chart-of-accounts"></a>Velge kontoplanen

Detaljer om finans må konfigureres for hver juridiske enhet i Microsoft Dynamics 365 Finance. På **Finans**-siden kan du velge kontoplanen og kontostrukturene som skal brukes for den valgte juridiske enheten. Du kan dele kontoplanen og kontostrukturene ved å konfigurere **Finans**-siden i hver juridiske enhet slik at de bruker samme kontoplan og kontostrukturer. Du kan også dele en del av konfigurasjonen i hver juridiske enhet og ha spesifikke konfigurasjoner i hver juridiske enhet.

Hvis de juridiske enhetene må ha ulike kontoplaner eller kontostrukturer, kan overstyringsfunksjonen for den juridiske enheten være nyttig. Når du bruker den samme kontoplanen og de samme kontostrukturene for flere juridiske enheter og deretter administrerer eventuelle unntak via overstyringer for juridisk enhet, kan du forenkle vedlikeholdet over tid.

Du kan konfigurere kontoplanen for en juridisk enhet ved å gå til **Økonomimodul \> Finansoppsett \> Finans**. På **Finans**-siden velger du **Kontoplan**, og deretter velger du kontoplanen du vil bruke, i listen. Vær oppmerksom på at kontoplanen ikke kan endres etter at du har valgt en verdi og postert transaksjoner i den juridiske enheten.

Hvis du vil ha mer informasjon om hvordan du planlegger og konfigurerer kontoplanen og hovedkontoene, kan du se [Planlegge kontoplanen](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Velge kontostrukturer

Hver juridiske enhet i Dynamics 365 Finance kan konfigureres slik at den bruker én eller flere kontostrukturer. Hver kontostruktur definerer finansdimensjonene og kombinasjonene av hovedkontoer og finansdimensjoner, som skal være tillatt når transaksjoner posteres. Du kan bruke de samme kontostrukturene i flere enn én juridisk enhet.

Vær oppmerksom på at hvis du har flere kontostrukturer, kan du bare velge kontostrukturer som ikke har overlappende kombinasjoner av hovedkontoer og finansdimensjoner. En av kontostrukturene er for eksempel konfigurert slik at den legger til en forretningsenhet for hovedkontoer mellom 1000 og 1999. I en annen kontostruktur har du lagt til en Avdeling-finansdimensjon for hovedkontoer som begynner med 1. I dette tilfellet kan bare én av kontostrukturene legges til i samme juridiske enhet.

Hvis du vil konfigurere kontostrukturer for finans, velger du **Legg til** i hurtigfanen **Kontostrukturer** på **Finans**-siden. Deretter velger du en kontostruktur i listen, og til slutt velger du **Velg**. Det kan ta noen minutter før kontostrukturene legges til og lagres. Vær oppmerksom på at kontostrukturene du velger, må være aktive. Ellers blir ikke detaljene i kontostrukturene virksomme i de juridiske enhetene der de er koblet.

Du kan fjerne en kontostruktur ved å velge **Fjern** i hurtigfanen **Kontostrukturer** på **Finans**-siden. Vær oppmerksom på at hvis du fjerner en kontostruktur fra finans, fjerner du ikke eventuelle transaksjoner som ble postert ved hjelp av konfigurasjonen for denne kontostrukturen.

Hvis du vil ha mer informasjon om hvordan du konfigurerer kontostrukturer, kan du se [Konfigurere kontostrukturer](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Konfigurere kalendere for finans

En annen komponent i finans er regnskapskalenderen. Du må velge en regnskapskalender for hver juridisk enhet. Du kan bruke samme regnskapskalender i flere enn én juridisk enhet. Når du velger en regnskapskalender for finans, opprettes det en kopi. Denne kopien kalles finanskalenderen. I finanskalenderen kan du velge statusen for periodene og modulene i hver periode.

Hvis du vil ha tilgang til og oppdatere kalenderen for den valgte juridiske enheten, velger du **Finanskalender** i handlingsruten på **Finans**-siden.

Du velger kalenderen ved å velge **Regnskapskalendere** og deretter velge kalenderen i listen. Hvis du endrer regnskapskalenderen etter at transaksjoner er postert i den juridiske enheten, må du velge **Beregn finansperioder på nytt**. I dialogboksen som vises, kan du deretter oppdatere finanssaldoene for periodene i kalenderen. Vi anbefaler at du kjører prosessen **Beregn finansperioder på nytt** i **Satsvis** modus, og at du kjører den når ikke-kritiske prosesser forekommer i systemet. Denne prosessen kan ta litt tid, avhengig av antall transaksjoner og kombinasjoner av finansdimensjoner.

Hvis ingen regnskapskalender er valgt for en juridisk enhet, får du en feilmelding når du prøver å postere en transaksjon i den juridiske enheten.

Hvis du vil ha mer informasjon, se [Regnskapskalendere, regnskapsår og perioder](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Bruke en saldofinansdimensjon

Etter at du har valgt kontoplanen og lagt til én eller flere kontostrukturer, kan du eventuelt velge én finansdimensjon som skal brukes som saldofinansdimensjon. Dimensjonen du velger, må finnes i alle kontostrukturene. Den må også være balansert i alle regnskapsoppføringer. Debet og kredit må med andre ord være like for hovedkontoen og saldofinansdimensjonen. Systemet oppretter automatisk transaksjoner for å balansere oppføringene, basert på hovedkontoene som er angitt i feltene **Enhetsintern - kredit** og **Enhetsintern - debet** på siden **Kontoer for automatiske transaksjoner**.

Hvis du vil ha mer informasjon om balanserende oppføringer, kan du se [Balanserte journaler for interenhetsregnskap](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Konfigurere valutaer for finans

**Finans**-siden brukes også til å styre og definere valutaene som skal brukes når transaksjoner posteres i økonomimodulen. Du må angi regnskapsvalutaen, som er valutaen som brukes i kolonnen **Regnskapsvaluta** i økonomimodulen for alle bilag. Du kan i tillegg eventuelt velge en andre valuta i kolonnen **Rapporteringsvaluta**. Hvis du velger en rapporteringsvaluta, blir alle transaksjonene registrert i denne valutaen i kolonnen **Rapporteringsvaluta** i økonomimodulen for alle bilag.

Hvis transaksjoner posteres i en annen valuta, konverterer systemet automatisk transaksjonsbeløpet fra transaksjonsvalutaen til regnskapsvalutaen og rapporteringsvalutaen for bilaget. På **Finans**-siden i feltet **Type valutakurs for regnskapsvaluta** velger du typen valutakurs som skal konfigureres for valutakursene som skal brukes til å konvertere verdier fra transaksjonsvalutaen til regnskapsvalutaen for et bilag. Hvis du valgte en rapporteringsvaluta, må du også angi valuta **Type valutakurs for rapporteringsvaluta** for å angi valutakursen som skal brukes til å konvertere verdier fra transaksjonsvalutaen til rapporteringsvalutaen for et bilag.

Hvis du bruker budsjetteringsfunksjonalitet, kan du også angi feltet **Type valutakurs for budsjett** for å angi valutakursen som skal brukes til å konvertere budsjettransaksjoner fra én valuta til en annen.

Hvis du bruker to valutaer, eller hvis du bruker én valuta, men transaksjoner posteres i en annen valuta, må du konfigurere hurtigfanen **Kontoer for revaluering av valuta** på **Finans**-siden. I denne hurtigfanen definerer du standardkontoer for realisert og urealisert fortjeneste og tap som skal brukes som standard når transaksjoner posteres, hvis ingen konto er angitt på siden **Kontoer for revaluering av valuta**. (Siden **Kontoer for revaluering av valuta** brukes til å konfigurere ulike kontoer for realisert og urealisert fortjeneste og tap for hver valuta.)

Realisert fortjeneste og tap er fortjeneste og tap som kommer fra fullførte transaksjoner. De registreres i resultatregnskapet. Urealisert fortjeneste og tap er fortjeneste og tap som er materialisert, men transaksjonen er ikke fullført. Du har med andre ord for eksempel postert en faktura, men fakturaen er ikke utlignet og betalt ennå. Urealisert fortjeneste og tap registreres i balansen.

Hvis du vil ha mer informasjon om hvordan du bruker to valutaer, kan du se [Dobbel valuta](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]