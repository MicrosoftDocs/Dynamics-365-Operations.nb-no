---
title: "Vise journaloppføringer og transaksjoner"
description: "Denne artikkelen beskriver de forskjellige måtene du kan vise loggoppføringer og transaksjoner."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a6848ea9c05536ac18a038b1864c9ccb9408964c
ms.lasthandoff: 03/31/2017


---

# <a name="view-journal-entries-and-transactions"></a>Vise journaloppføringer og transaksjoner

Denne artikkelen beskriver de forskjellige måtene du kan vise loggoppføringer og transaksjoner. 

Brukere som vil vise journaler og transaksjoner, har flere måter å få tilgang til dataene på. De kan bruke forespørselssider med neddrillingsfunksjonalitet, eller de kan bruke forskjellige rapportalternativer i økonomimodulen.

## <a name="voucher-transactions"></a>Bilagstransaksjoner
**Bilagstransaksjoner** er en forespørselsside der du kan velge mellom ulike tabeller og felt for å angi kriterier for saldoen eller transaksjonen du søker etter. Du kan for eksempel vise alle transaksjoner for en bestemt dato eller en konto eller alle transaksjonene av typen **I drift** som er på et bestemt posteringslag. Siden viser journalnummeret, bilaget, datoen og hovedkontoen som standard, men du kan legge til flere tabeller, felt og kriterier for å begrense søket.

## <a name="audit-trail"></a>Revisjonsspor
**Revisjonsspor** er en forespørselsside som viser transaksjonstypene, beskrivelser, hvem transaksjonene ble opprettet av, og når de ble opprettet. Fra forespørselssiden **Revisjonsspor** kan du vise bilagstransaksjonene.

## <a name="financial-reports"></a>Finansrapporter
Du kan også utforske og analysere økonomimodultransaksjoner ved å kjøre finansrapporter. Siden utformingen av finansrapporter kan baseres på kontoer, dimensjoner, kontokategorier eller en kombinasjon av alle tre, kan du vise transaksjonene ved å drille ned på ulike måter. Hvis du trenger mer informasjon for økonomimodultransaksjoner, kan du også ta med flere transaksjonsegenskaper som en del av rapportutformingen. Hvis du i tillegg vil se transaksjonene som utgjør en saldo i økonomimodulen, kan du drille ned til kontotransaksjoner på samme måte som på listesiden **Råbalanse**.

## <a name="ledger-reports"></a>Finansrapporter
I tillegg til finansrapporter kan du bruke følgende rapporter til å vise økonomimodultransaksjoner:

-   **Dimensjonsoppgave** – Denne rapporten viser transaksjoner etter dag og konto, og det finnes også alternativer for å vise transaksjoner etter dimensjon og periode.
-   **Finanstransaksjonsliste** – Denne rapporten viser transaksjoner i transaksjons-, regnskaps- og rapporteringsvalutaer for en konto.
-   **Skriv ut journal** – Denne rapporten viser resultatet av en postert journal. Du kan kjøre rapporten med journalpartinummer eller journaltypen, eller du kan legge til flere felt.
-   **Posterte transaksjoner etter journal** – Denne rapporten viser transaksjonene som er postert til en journal, gruppert etter bilag.
-   **Transaksjonsliste etter dato** – Denne rapporten viser alle transaksjonene etter dato, sammen med journalnummeret, bilaget og finanskontoen. Den viser også transaksjonene i transaksjons-, regnskaps- og rapporteringsvalutaene.
-   **Transaksjonsopprinnelse** – Denne transaksjonsrapporten viser kontoen etter journal og etter transaksjons-, regnskaps- og rapporteringsvalutaen. Den viser også hver linjene i journalen som ble brukt som motkonto.


Hvis du vil ha mer informasjon, kan du se [Kontosaldoer i økonomimodulen](general-ledger-account-balances.md), [Regnskapskildeutforsker](\financials\accounts-payable\accounting-source-explorer) og [Finansrapportering](financial-reporting-getting-started.md)

