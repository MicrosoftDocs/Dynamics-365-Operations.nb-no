---
title: Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal
description: Dette emnet forklarer hvordan du bruker ankomstregistreringen til å opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f19c31a3ca20ad4b11e2529bdcb9db351c37f6c2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971884"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du bruker ankomstregistreringen til å opprette fakturaer, og deretter bruke godkjenningsjournalen for å oppdatere utgiftskontoene.

## <a name="create-and-post-and-invoice"></a>Opprette og postere en faktura
1. Gå til **Moduler > Leverandører > Fakturaer > Ankomstregistrering** i navigasjonsruten.
2. Velg **Ny**.
3. Velg navnet på ankomstregistreringen du vil bruke.
4. Velg **Linjer** for å åpne registeret og angi utgiftslinjer.
5. Velg en leverandør. Du kan for eksempel angi eller velge `US-104`.
6. Skriv inn en verdi i **Faktura**-feltet.
7. Skriv inn en verdi i **Beskrivelse**-feltet.
8. Angi et tall i **Kredit**-feltet.
9. I **Godkjent av**-feltet velger du en godkjenner fra rullegardinmenyen.
10. Velg **Poster**.

## <a name="approve-an-invoice"></a>Godkjenne en faktura
1. Gå til **Moduler > Leverandører > Fakturaer > Fakturagodkjenning** i navigasjonsruten.
2. Velg **Ny**.
3. Velg navnet på fakturagodkjenningsjournalen du vil bruke.
4. Velg **Linjer** for å vise en side der du kan velge fakturaene som du vil godkjenne.
5. Velg **Finn bilag** for å vise alle fakturaer som er klare til godkjenning.
6. Merk fakturaen som du opprettet, og klikk deretter på **Velg** . Bilagene som du valgte ovenfor, flyttes til denne listen når du merker dem.  
7. Velg **OK**.
8. Velg **kontonummer**-feltet for å legge til en utgiftskonto i fakturaen.
9. Skriv inn et kontonummer og gå ut av feltet. Skriv for eksempel inn `600120`.
10. Velg **Poster**.
11. Velg **Bilag** for å vise oppføringene som ble postert. Kontoen for fakturaen som venter på godkjenning, tilbakeføres og erstattes med den faktiske utgiftskontoen.  

