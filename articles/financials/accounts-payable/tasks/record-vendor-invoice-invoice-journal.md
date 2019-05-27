---
title: Registrere en leverandørfaktura i fakturajournalen
description: Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556362"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en leverandørfaktura i fakturajournalen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger. Eksempler på denne typen faktura er utgifter for forsyninger eller tjenester.  Denne registreringen bruker demonstrasjonsfirmaet USMF.

1. Gå til Leverandører > Arbeidsområder > Leverandørfakturaregistrering.
2. Klikk Ny fakturajournal.
3. Klikk Ny.
4. I Navn-feltet angir du journalnavnet eller klikker rullegardinknappen for å åpne oppslaget.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Linjer.
    * Angi posteringsdatoen som oppdaterer Økonomimodul, i Dato-feltet.  
7. Angi leverandørkontoen i Konto-feltet.
8. I Faktura-feltet angir du fakturanummeret.
9. Skriv inn en verdi i Beskrivelse-feltet.
10. Angi et tall i Kredit-feltet.
11. I Motkonto-feltet angir du kontonummeret eller klikker rullegardinknappen for å åpne oppslaget.
    * Mva-gruppen hentes fra leverandørkontoen.  
    * Mva-gruppen for vare hentes fra hovedkontoen angitt i Motkonto-feltet.  
    * Forfallsdatoen beregnes basert på betalingsbetingelsene.  
    * Kontantrabatten hentes fra leverandørkontoen.  
12. Klikk Poster.
13. Lukk siden.

