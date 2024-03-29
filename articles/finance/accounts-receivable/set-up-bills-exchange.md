---
title: Definere veksler
description: Denne artikkelen beskriver fremgangsmåten for hvordan du konfigurerer veksler.
author: ShivamPandey-msft
ms.date: 09/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: kfend
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 91821b10afe7cdbabd0a58b61219ce29d686c5c9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874732"
---
# <a name="set-up-bills-of-exchange"></a>Definere veksler

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten for hvordan du konfigurerer veksler.

En veksel er en skriftlig eller elektronisk ordre fra en kunde som angir at en annen part, vanligvis en bank, skal betale et angitt beløp til selskapet. Når du bruker en veksel som betaling for en salgsordrefaktura eller fritekstfaktura, krediterer du kundekontoen. Denne kreditten sikres av vekselen, til kunden betaler vekselen til banken. Vanligvis vil du utligne fakturaen med vekselen på forfallsdatoen. Når du mottar varsel fra banken om at vekselen er innløst, kan du lukke den. Du kan trekke vekselen gjennom banken på et av følgende tidspunkt:

-   På forfallsdatoen. Denne fremgangsmåten kalles remitter for inkasso.
-   Før forfallsdatoen, vanligvis på diskontodatoen som er angitt i betalingsbetingelsene som er definert for kunden. Når du posterer transaksjonen, posteres rabattbeløpet til en utgiftskonto. Det resterende beløpet er gjeld til deg til banken mottar betaling fra kunden. Denne fremgangsmåten kalles remitter for diskonto.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Definere posteringsprofiler for veksler

Bruk siden **Kundeposteringsprofiler** til å definere posteringsprofiler som du kan bruke med veksler, protestere veksler, remisser for inkasso og remisser for diskonto. I **Samlekonto**-feltet velger du samlekontoen du vil postere vekselbeløp til. Denne kontoen debiteres eller krediteres avhengig av typen vekseltransaksjon:
-   For veksler debiteres denne kontoen når en veksel posteres, og den krediteres når en remisse for diskonto eller en remisse for inkasso posteres.
-   For protestert veksel debiteres denne kontoen når en protestert  veksel posteres.
-   For remisser for inkasso debiteres denne kontoen når en remisse for inkasso posteres.
-   For remisser for diskonto debiteres denne kontoen når en remisse for diskonto posteres.

I **Utligningskonto**-feltet velger du kontantkontoen du vil postere vekselbeløp til. Denne kontoen debiteres når en veksel utlignes. I **Mva-forskuddsbetalinger**-feltet velger du samlekontoen du vil postere mva-beløp til når veksler brukes for forskuddsbetalinger. Velg kontoen du vil postere rabattbeløpet til for remitteringer for rabatt, i feltet **Konto for rabattavsetning**. Denne kontoen krediteres når en remisse for diskonto posteres.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Definere kundeparametere for veksler

På siden **Kundeparametere for veksler**, er standardposteringssprofilene for vekslinger oppgitt i kategorien **Hovedbok og salgsavgift**. Antall sekvenser er definert på tabellen **Antall sekvenser**.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Definere journalnavn for veksler


På siden **Journalnavn** oppretter du minst fem journalnavn til bruk med veksler. Her er journaltypene:
-   **Kunde: trekk veksel** – Opprett et journalnavn for Journal for vekseltrekking.
-   **Kundeprotest veksel** – Opprett et journalnavn for Journal for vekselprotest.
-   **Kundens tilbaketrekking av veksel** – Opprett et journalnavn for Journal for ny vekseltilbaketrekking.
-   **Kunde: bankremisse** – Opprett et journalnavn for Remitteringsjournal.
-   **Kunde: avregn veksel** – Opprett et journalnavn for Vekselavregningsjournal.

På journalkupongsiden for hver vekslingsjournal angir du informasjon om bytte på kategorien **Veksling**. Etter at journallinjene for veksling er lagt ut, kan du se dem på siden **Journalforespørsler for veksling** og siden **Vekselavregningsjournal**.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Definere betalingsmåter for veksler

På siden **Betalingsmåter** definerer du minst én betalingsmåte for veksler. Hvis du opererer med flere banker, må du definere en betalingsmåte som stemmer overens med vekselremitteringsformatet som hver enkelt bank krever for veksler.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Definere betalingsgebyrer for veksler

Et betalingsgebyr et er gebyr som er tilknyttet prosessen med å samle inn betaling fra kunder. Flere konfigurasjonslinjer for betalingsgebyr kan tilknyttes hvert betalingsgebyr. Du kan bruke konfigurasjonslinjene til å styre hvordan standardbeløp for betalingsgebyr skal beregnes. Du kan for eksempel opprette konfigurasjonslinjer for betalingsmåter, betalingsspesifikasjoner, valutaer og tidsperioder. Du kan også opprette konfigurasjonslinjer for en prosent eller et beløp basert på dagsintervaller. Du kan for eksempel definere en renteprosent som er basert på hvor lenge betalingen har gått over forfall. Hvis banken tar forskjellige gebyrer for forskjellige remissetyper, for eksempel **Inkasso** eller **Rabatt**, kan du opprette en egen betalingsgebyrlinje for hver remissetype.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Definere remitteringsgebyrer for bankremissefiler

På **Bankkontoer**-siden kan du definere remitteringsgebyrer som banken belaster for hver remitteringsfil som genereres. Remitteringsgebyrene posteres når remitteringen er bekreftet og de realiserte gebyrbeløpene er kjent. Remitteringsgebyr er noe annet enn betalingsgebyrer, som hentes fra kunder og er tilknyttet journallinjer.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Definere dokumentoppsett for veksler

På **Bankkontoer**-siden klikker du på **Oppsett** og angir dokumentoppsettet som kreves for hver bankkonto som du vil generere vekseldokumenter for.

## <a name="set-up-customers-for-bills-of-exchange"></a>Definere kunder for veksler

For hver kunde som har avtalt å betale ved hjelp av en veksel, kan du definere en standard betalingsmåte for veksler i kategorien **Betalingsstandarder** på siden **Kunder**.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
