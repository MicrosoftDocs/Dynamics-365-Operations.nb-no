---
title: Opprette en avskrivningsjournal for en kunde
description: Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21aaeda413e767fed1815423b0262127c6692bb6
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775306"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Opprette en avskrivningsjournal for en kunde

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen viser hvordan du definerer parameterne for avskrivninger og deretter skriver av transaksjoner fra Innkrevinger-siden, siden Åpne kundefakturaer og Kunde-siden. Denne oppgaven bruker demonstrasjonsfirmaet USMF.


## <a name="set-up-the-write-off-parameters"></a>Konfigurere avskrivningsparameterne
1. Gå til **Navigasjonsrute > Moduler > Kreditt og innkreving > Oppsett > Kundeparametere**.
2. Klikk fanen **Innkrevinger**.
3. Vis eller skjul **Avskrive**-delen.
    - **Avskrivningsjournalen** er økonomijournalen som skal inneholde avskrivningstransaksjonene som du oppretter.  
    - Du kan knytte en årsakskode til hver avskrivning. Du kan overskrive denne standardverdien under avskrivningen.  
    - Angi **Separat merverdiavgift** til Ja hvis du vil skille merverdiavgiften fra den opprinnelige transaksjonen i avskrivningen.  
4. Lukk siden.
5. Gå til **Kreditt og innkreving > Oppsett > Kundeposteringsprofiler**. Avskrivningskontoen skal brukes som utgiftskontoen eller reserverejustering i økonomijournalen.
6. Lukk siden.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Avskrive en kundesaldo fra siden Aldersfordelte saldoer
1. Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**.
2. Merk raden for kunden som du vil skrive av. Merk for eksempel linjen med Birch firma på den.
3. Klikk **Innkreving** i **handlingsruten**.
4. Klikk **Avskrive**.
5. Klikk **OK**.
6. Lukk siden.
7. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.
8. Velg journalpartinummeret for journalen som inneholder avskrivningen. Det opprettes én linje for å tilbakeføre kundesaldoen. Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.  
9. Lukk siden.


## <a name="write-off-transactions-from-the-collections-page"></a>Skriv av transaksjoner fra purresiden
1. Gå til **Kreditt og innkreving > Innkrevinger > Aldersfordelte saldoer**.
2. Velg navnet på kunden som har transaksjonene du vil skrive av. Velg for eksempel Cave Wholesales (US-004).
3. Merk raden for den første transaksjonen.
4. Merk raden for den andre transaksjonen.
5. Klikk **Avskrive**.
6. Skriv inn "Misligholdt gjeld" i **Årsakskommentar**-feltet.
7. Klikk **OK**.
8. Lukk siden.
9. Lukk siden.
10. Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**.
11. Velg journalpartinummeret for journalen som inneholder avskrivningen. Det opprettes én linje for å tilbakeføre kundesaldoen. Én eller flere linjer opprettes for å postere avskrivningen til avskrivningskontoen.  
12. Lukk siden.


## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Skrive av en faktura fra siden Åpne kundefakturaer
1. Gå til **Navigasjonsrute > Moduler > Kunder > Fakturaer > Åpne fritekstfakturaer**.
2. Merk linjen for en faktura. Merk for eksempel linjen for CIV-000667..
3. Klikk **Faktura** i **handlingsruten**.
4. Klikk **Avskrive**.
5. Klikk **OK**.
6. Lukk siden.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Skrive av en kundesaldo fra kundesiden
1. Gå til **Kunder > Kunder > Alle kunder**.
2. Velg en kundekonto. Velg for eksempel US-001 (Contoso Retail San Diego).
3. Klikk **Innkreving** i **handlingsruten**.
4. Klikk **Avskrive**.
5. Klikk **OK**.
6. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
