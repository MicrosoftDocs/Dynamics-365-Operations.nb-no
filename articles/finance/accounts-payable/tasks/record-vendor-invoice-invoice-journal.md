---
title: Registrere en leverandørfaktura i fakturajournalen
description: Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140381"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en leverandørfaktura i fakturajournalen

[!include [banner](../../includes/banner.md)]

Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger. Eksempler på denne typen faktura er utgifter for forsyninger eller tjenester.  Denne registreringen bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Leverandører > Arbeidsområder > Leverandørfakturaregistrering**.
2. Klikk **Ny fakturajournal** i **handlingsruten**.
3. Klikk på **Ny**.
4. I **Navn**-feltet angir du journalnavnet eller klikker rullegardinknappen for å åpne oppslaget.
5. Skriv inn en verdi i **Beskrivelse**-feltet.
6. Klikk på **Linjer** i **handlingsruten**. Angi posteringsdatoen som oppdaterer Økonomimodul, i **Dato**-feltet.  
7. Angi **leverandørkontoen** i **Konto**-feltet.
8. I **Faktura**-feltet angir du fakturanummeret.
9. Skriv inn en verdi i **Beskrivelse**-feltet.
10. Angi et tall i **Kredit**-feltet.
11. I **Motkonto**-feltet angir du kontonummeret eller klikker rullegardinknappen for å åpne oppslaget.
    * **Mva-gruppen** hentes fra leverandørkontoen.  
    * **Mva-gruppen for vare** hentes fra hovedkontoen angitt i **Motkonto**-feltet.  
    * **Forfallsdatoen** beregnes basert på betalingsbetingelsene.  
    * **Kontantrabatten** hentes fra leverandørkontoen.  
12. Klikk **Poster**.
13. Lukk siden.

