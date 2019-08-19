---
title: Avstemme frakt manuelt
description: Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb9c850aa045b72137b8a1d3c8cdae51cf2fd7b6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843247"
---
# <a name="reconcile-freight-manually"></a>Avstemme frakt manuelt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du avstemmer frakt manuelt. Dette gjøres vanligvis av en transportkoordinator. Du kan bruke prosedyren i USMF-demodatafirmaet.


## <a name="select-a-load-to-reconcile"></a>Velge en last for avstemming
1. Gå til Transportstyring > Planlegging > Arbeidsområde for lastplanlegging.
2. Fjern merket for Skjul sendt og mottatt. 
3. I listen velger du lasten som har last-ID 00006.

## <a name="create-a-carrier-invoice"></a>Opprette en transportørfaktura
    * Hvis du avstemmer frakt manuelt og ikke mottar transportørfakturaer automatisk, kan du opprette en faktura basert på fraktbrevet.  
1. Klikk Relatert informasjon.
2. Klikk Detaljer for fraktbrev.
3. Klikk Generer fraktbrevfaktura.
4. Skriv inn en verdi i Faktura-feltet.
5. Klikk OK.

## <a name="reconcile-the-invoice"></a>Avstemme fakturaen
    * Når du avstemmer en transportørfaktura og et fraktbrev, gjøres dette linje for linje.  
1. Klikk Samsvar fraktbrev og fakturaer.
2. Vis delen Fakturadetaljer.
3. Utvid delen Detaljer for ikke-samsvart fraktbrev.
4. Merk den valgte raden i listen.
5. Klikk Samsvar.
6. Utvid delen Detaljer for samsvart fraktbrev.

## <a name="submit-the-invoice-for-approval"></a>Send fakturaen til godkjenning
1. Klikk Send til godkjenning.
2. Lukk siden.
3. Fjern merket for Skjul godkjent. 
4. Klikk Leverandørfakturajournaler.
5. Klikk for å følge koblingen i Referansejournalnummeret-feltet.
6. Klikk Linjer.

