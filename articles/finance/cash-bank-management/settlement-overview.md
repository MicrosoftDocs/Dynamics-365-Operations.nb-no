---
title: Oversikt over utligning
description: Dette emnet inneholder generell informasjon om utligningsprosessen. Den beskriver hvilke transaksjonstyper som kan utlignes, og tidsberegningen og prosessen for å utligne dem. Den beskriver også resultatene av utligningsprosessen.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 650b0ef0123cf9acf42c2e7460693b555897744f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446383"
---
# <a name="settlement-overview"></a>Oversikt over utligning

[!include [banner](../includes/banner.md)]

Dette emnet inneholder generell informasjon om utligningsprosessen. Den beskriver hvilke transaksjonstyper som kan utlignes, og tidsberegningen og prosessen for å utligne dem. Den beskriver også resultatene av utligningsprosessen.

Under utligning brukes transaksjonene fra ett dokument på transaksjonene på et annet dokument for å øke eller redusere saldoen for hvert dokument. En betaling kan for eksempel brukes på en faktura. Ulike transaksjonstyper kan utlignes, til forskjellige tider og via forskjellige metoder. Utligningsprosessen kan også generere nye transaksjoner.

## <a name="what-transactions-can-be-settled"></a>Hvilke transaksjoner som kan utlignes

I Leverandører og Kunder kan utligninger forekomme mellom alle transaksjonstyper som påvirker leverandørsaldoen eller kundesaldoen. Disse transaksjonstypene kan omfatte fakturaer, betalinger, kreditnotaer og gebyrer. Alle transaksjonstyper kan utlignes mot alle andre transaksjonstyper. Du kan for eksempel utligne en betaling mot en faktura, en kreditnota mot en faktura, en faktura mot en annen faktura, og en betaling mot en betaling.

Du kan utligne betalinger mot en transaksjon i den samme juridiske enheten eller i en annen juridisk enhet. I organisasjoner som bruker en modell for sentraliserts betaling, kan [sentraliserte betalinger](set-up-centralized-payments.md) bidra til å strømlinjeforme betalingsprosessen.

## <a name="when-to-settle-transactions"></a>Når transaksjoner skal utlignes

Transaksjoner kan utlignes når betalinger registreres. Når du for eksempel foretar en betaling til en leverandør, velger du vanligvis hvilke fakturaer som skal betales. Når du velger fakturaer, markerer du dem for utligning mot betalingen. Når betalingsmedarbeidere for Kunder registrerer kundebetalinger, kan de merke de aktuelle fakturaene for utligning basert på informasjonen som følger med hver kundens betaling. Du bruker siden **Utlign transaksjoner** til å merke transaksjonene for utligning. Du kan åpne denne siden fra alle ikke-posterte fakturaer eller betalinger. Når transaksjonen posteres, posteres også utligningen. 

Transaksjoner kan også utlignes etter at de er bokført. Du kan angi og postere en kundebetaling uten at den utlignes mot fakturaer. Du må kanskje sørge for at betalingen utlignes mot den riktige fakturaen før du posterer utligningen. Siden **Utlign transaksjoner** kan åpnes fra siden **Alle kunder** eller **Alle leverandører**, eller fra **Transaksjoner**-siden for en kunde eller leverandør.

Du kan også reservere posterte forskudd for en faktura ved å merke betalingen for utligning mot en bestilling eller salgsordre. I så fall vil betalingen fortsatt være en åpen saldo, men den kan ikke utlignes mot en annen faktura. Betalingen utlignes automatisk mot fakturaen som opprettes fra bestillingen eller salgsordren.

## <a name="how-to-settle-transactions"></a>Utligne transaksjoner

Transaksjoner kan utlignes manuelt, automatisk eller ved å bruke en kombinasjon av de to metodene. Valget av en utligningsmetode er avhengig av forretningsprosessene. På sidene **Leverandørparametere** og **Kundeparametere** kan du konfigurere utligningsprosessen slik at den er justert med de forretningsprosessene.

Du kan opprette leverandørbetalinger og avtalegirobetalinger for kunde ved hjelp av et betalingsforslag. Et betalingsforslag brukes til å velge fakturaer som skal betales. Betalingsforslaget startes manuelt, og så merker systemet automatisk de valgte fakturaene for utligning ved opprettelse av betalingene.

Hvis betalingene opprettes manuelt, kan du bruke siden **Utlign transaksjoner** til å velge fakturaer for utligning. Du kan velge fakturaene manuelt, eller du kan bruke alternativet **Merk etter prioritet** for å merke fakturaer automatisk for utligning. Alternativet **Merk etter prioritet** er bare tilgjengelig for kunder. Du kan aktivere dette alternativet i kategorien **Utligningsprioritet** på siden **Kundeparametere**.

Hvis en betalingsassistent angir en betaling, men ikke utligner denne betalingen før den posteres, kan betalingen utlignes automatisk. Du kan aktivere automatisk utligning på sidene **Kundeparametere** og **Leverandørparametere**. Automatisk utligning utligner transaksjoner bare i samme juridiske enhet. Den utligner ikke transaksjoner på tvers av flere juridiske enheter.

Når du bruker automatisk utligning, kan du bruke den forhåndsdefinerte utligningsprioriteten, eller du kan definere en egen prioritetsrekkefølge på siden **Kundeparametere**. Denne funksjonen er bare tilgjengelig for kunder.

## <a name="results-of-settlement"></a>Resultat av utligning

Når transaksjonene er utlignet, økes eller reduseres den utestående saldoen for hver transaksjon etter behov. Vanligvis når en faktura og en betaling utlignes, oppdateres statusen og saldoen for hver transaksjon i henhold til følgende regler:

- Hvis betalingsbeløpet er større enn fakturabeløpet, reduseres fakturasaldoen til 0,00 og fakturaen lukkes. Betalingen beholdes åpen, og saldoen er differansen mellom betalingsbeløpet og det fakturerte beløpet.
- Hvis betalingsbeløpet er mindre enn fakturabeløpet, reduseres betalingssaldoen til 0,00 og betalingen lukkes. Fakturaen beholdes åpen, og saldoen er differansen mellom fakturabeløpet og betalingsbeløpet.
- Hvis betalingsbeløpet er lik fakturabeløpet, lukkes både betalingen og fakturaen, og saldoen for begge reduseres til 0,00.

Hvis [betalingsbeløpet er mindre enn fakturabeløpet](../accounts-payable/vendor-payments-partial-amount.md) på grunn av en kontantrabatt, avskrivning eller underbetaling, kan fakturaen og betalingen fortsatt lukkes, avhengig av hvordan utligningene er konfigurert på sidene **Leverandørparametere** og **Kundeparametere**.

Utligninger kan også generere transaksjoner. Utligningen av en faktura og en betaling kan for eksempel gi en kontantrabatt, realisert fortjeneste eller tap, mva-justeringer, avskrivninger eller øredifferanser.

## <a name="identifying-marked-transactions-during-settlement"></a>Identifisere merkede transaksjoner under utligning

Når du prøver å utligne en transaksjon, kan det hende at du legger merke til et symbol som angir at transaksjonen er merket et annet sted. I dette tilfellet kan du velge transaksjonen på siden **Utligne transaksjoner** og deretter velge **Forespørsel \> Utligning fra utligningsvinduet**. Visningen for denne forespørselen viser journaler, salgsordrer, fakturaer, betalingsforslag og kundelokasjoner som kanskje blokkerer transaksjonen fra utligning. Hvis du vil løse problemet, kan du velge koblingen for å gå direkte fra forespørselen til den blokkerte plasseringen. Du kan deretter oppdatere dokumentet med justeringene som kreves for å utligne det. Du kan også bruke **Merket**-indikatoren til å identifisere andre dokumenter som er inkludert i samme blokkeringslokasjon.

## <a name="additional-resources"></a>Tilleggsressurser

- [Utlign rest](settle-remainder.md)
