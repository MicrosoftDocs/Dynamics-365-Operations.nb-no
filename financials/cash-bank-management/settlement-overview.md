---
title: Oversikt over utligning
description: "Denne artikkelen inneholder generell informasjon om utligningsprosessen. Den beskriver hvilke typer transaksjoner som kan utlignes, når og hvordan transaksjoner kan utlignes, og resultatene av utligningsprosessen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Oversikt over utligning

Denne artikkelen inneholder generell informasjon om utligningsprosessen. Den beskriver hvilke typer transaksjoner som kan utlignes, når og hvordan transaksjoner kan utlignes, og resultatene av utligningsprosessen.

Under utligning brukes transaksjonene fra ett dokument på transaksjonene på et annet dokument for å øke eller redusere saldoen for hvert dokument. For eksempel kan en betaling brukes til en faktura. Forskjellige transaksjonstyper kan utlignes, til forskjellige tider, og gjennom ulike metoder. Utligning kan også forårsake at nye transaksjoner genereres.

## <a name="what-transactions-can-be-settled"></a>Hvilke transaksjoner som kan utlignes
Utligning mellom leverandører og kunder kan forekomme mellom alle transaksjonstyper som påvirker leverandørsaldoen eller kundesaldoen, for eksempel fakturaer, betalinger, kreditnotaer og gebyrer. Alle transaksjonstyper kan utlignes mot alle andre transaksjonstyper. Du kan for eksempel utligne en betaling mot en faktura, en kreditnota mot en faktura, en faktura mot en faktura, og en betaling mot en betaling. Du kan utligne betalinger mot en transaksjon i den samme juridiske enheten eller i en annen juridisk enhet. I organisasjoner som bruker en modell for sentralisert betaling, [sentraliserte betalinger](set-up-centralized-payments.md) kan bidra til å strømlinjeforme betalingsprosessen.

## <a name="when-to-settle-transactions"></a>Når transaksjoner skal utlignes
Transaksjoner kan utlignes ved betalingsoppføring. Når du for eksempel foretar en betaling til en leverandør, velger du vanligvis fakturaer som skal betales. Ved å velge fakturaer, merker du dem for utligning mot betaling. Når kunder betaling clerks registrerer en kundebetaling, kan de merke de aktuelle fakturaene for utligning, basert på informasjonen som følger med kundens betaling. Siden **Utlign transaksjoner** brukes til å merke transaksjonene for utligning. Denne siden kan åpnes fra alle ikke-posterte fakturaer eller betalinger. Når transaksjonen posteres, posteres også utligningen. Transaksjoner kan også utlignes etter at de er bokført. Du kan angi og postere en kundebetaling uten at den utlignes mot fakturaer. Du må kanskje gjøre undersøkelser først for å kontrollere at betalingen utlignes mot den riktige fakturaen. Siden **Utlign transaksjoner** kan åpnes fra siden **Alle kunder** eller **Alle leverandører**, eller fra **Transaksjoner**-siden for en kunde eller leverandør. Du kan også reservere posterte forskudd for en faktura ved å merke betalingen for utligning mot en bestilling eller salgsordre. I dette tilfellet betaling vil fortsatt ha en åpen saldo, men den kan ikke utlignes mot en annen faktura. Betalingen utlignes automatisk mot fakturaen som er opprettet fra bestillingen eller salgsordren.

## <a name="how-to-settle-transactions"></a>Utligne transaksjoner
Transaksjoner kan utlignes manuelt, automatisk eller ved å bruke en kombinasjon av de to metodene. Valget av en utligningsmetode avhenger av forretningsprosesser, som kan implementeres gjennom oppsettet av utligning i leverandørparametere og kundeparametere. Du kan opprette leverandørbetalinger og avtalegirobetalinger for kunde ved hjelp av et betalingsforslag, som brukes til å velge fakturaer som skal betales. Betalingsforslaget startes manuelt, men Microsoft Dynamics 365 for operasjoner merker automatisk de valgte fakturaene for utligning når betalingene opprettes. Hvis betalingene opprettes manuelt, kan du bruke siden **Utlign transaksjoner** til å velge fakturaer for utligning. Du kan velge fakturaene manuelt, eller du kan bruke alternativet **Merk etter prioritet** for å merke fakturaer automatisk for utligning. Alternativet **Merk etter prioritet** er bare tilgjengelig for kunder. Hvis du vil aktivere dette alternativet, kan du bruke **Utligningsprioritet**-siden under kundeparametere. Hvis en betalingsassistent angir en betaling, men ikke utligner denne betalingen før han eller hun posteres den, kan betalingen utlignes automatisk. Du kan aktivere automatisk utligning i Kundeparametere- og leverandørparametere. Når du bruker automatisk utligning, kan du bruke forhåndsdefinerte utligning ordren, eller du kan definere dine egne prioritetsrekkefølge for utligning under kundeparametere. Denne funksjonen er bare tilgjengelig for kunder.

## <a name="results-of-settlement"></a>Resultat av utligning
Når transaksjonene er utlignet, økes eller reduseres den utestående saldoen for hver transaksjon etter behov. I de fleste tilfeller, der en faktura og betaling er utlignet, oppdateres statusen og saldoen for hver transaksjon i henhold til følgende regler:

-   Hvis betalingsbeløpet er større enn fakturabeløpet, reduseres fakturasaldoen til 0,00 og fakturaen lukkes. Betalingen beholdes åpen, og saldoen er det betalte beløpet som overskrider det fakturerte beløpet.
-   Hvis betalingsbeløpet er mindre enn fakturabeløpet, reduseres betalingssaldoen til 0,00 og betalingen lukkes. Fakturaen beholdes åpen, og saldoen er det underbetalte fakturabeløpet.
-   Hvis betalingsbeløpet er lik fakturabeløpet, lukkes både betalingen og fakturaen, og saldoen for begge er 0,00.

Hvis en [-betaling er mindre enn fakturabeløpet](../accounts-payable/vendor-payments-partial-amount.md) på grunn av en kontantrabatt, avskrivning eller underbetaling, kan fakturaen og betalingen fortsatt lukkes, avhengig av oppsettet for utligning i leverandørparametere og kundeparametere. Utligning kan også generere transaksjoner. Utligningen av en faktura og betaling kan for eksempel gi en kontantrabatt, realisert fortjeneste eller tap, mva-justeringer, avskrivninger eller øredifferanser.


