---
title: Vise journaloppføringer og transaksjoner
description: Denne artikkelen beskriver de forskjellige måtene du kan vise loggoppføringer og transaksjoner.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8ae038001e799666907fd1ba7bec09765785f45
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978467"
---
# <a name="view-journal-entries-and-transactions"></a>Vise journaloppføringer og transaksjoner

[!include [banner](../includes/banner.md)]

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


## <a name="additional-resources"></a>Tilleggsressurser
- [Kontosaldoer i økonomimodulen](general-ledger-account-balances.md) 
- [Regnskapskildeutforsker](../accounts-payable/accounting-source-explorer.md)
- [Oversikt over finansrapportering](financial-reporting-getting-started.md)
- [Vise journaloppføringer eller transaksjoner](tasks/view-journal-entries-or-transactions.md)



