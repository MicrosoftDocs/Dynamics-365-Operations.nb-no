--- 
title: "Registrere en leverandørfaktura i fakturajournalen"
description: "Denne oppgaveveiledningen viser hvordan du kan registrere leverandørfakturaer som ikke er knyttet til bestillinger."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Registrere en leverandørfaktura i fakturajournalen

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


