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
ms.openlocfilehash: f9f2cbe0c9d1609aa3713776f81bafa396fff301
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645287"
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
12. Hvis du har aktivert arbeidsflyten for leverandørfakturajournal, klikker du **Arbeidsflyt > Send**.
    * Når sendingen er godkjent, vil datoen flyttes til den første dagen i neste åpne periode hvis posteringsdatoen for transaksjonen er innenfor en periode som er på vent eller lukket for finanspostering.
12. Klikk **Poster**.
13. Lukk siden.

