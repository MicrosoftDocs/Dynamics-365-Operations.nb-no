--- 
title: Definere etterdaterte sjekker
description: "Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d83713f9d54b396a10894995024ac1c8dd47a6f1
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-postdated-checks"></a>Definere etterdaterte sjekker

[!include [task guide banner](../../includes/task-guide-banner.md)]

Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger. Du kan også angi avregningskontoer for utstedte sjekker, mottatte sjekker og kildeskatt. Etterdaterte sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato. Du kan angi om sjekken skal gjenspeiles i regnskapet før forfallsdatoen.



Rollen til denne prosedyren er kasserer. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.


## <a name="set-up-postdated-checks"></a>Definere etterdaterte sjekker
1. Gå til Kontant- og bankbehandling > Oppsett > Parametere for bankstyring.
2. Velg kategorien Etterdaterte sjekker.
3. Merk av eller fjern merket i avmerkingsboksen Aktiver etterdaterte sjekker.
4. Merk av eller fjern merket i avmerkingsboksen Poster journaloppføringer for etterdaterte sjekker.
5. Angi ønskede verdier i feltet Avregningskonto for utstedte sjekker.
6. Angi ønskede verdier i feltet Avregningskonto for mottatte sjekker.
7. Skriv inn en verdi i feltet Økonomijournal for klarering av oppføringer.
8. Skriv inn en verdi i feltet Overfør etterdaterte sjekker til denne leverandørbetalingsjournalen.
9. Angir ønskede verdier feltet Clearingkonto for kildeskatt.
10. Klikk Lagre.
11. Lukk siden.
12. Gå til Leverandører > Betalingsoppsett > Betalingsmåter.
13. Klikk Ny.
14. Skriv inn en verdi i Betalingsmåte-feltet.
15. Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.
16. Velg Bank i feltet Kontotype.
    * Motkontoen for betalingsmetoden vil være en bank.  
17. Angi ønskede verdier i feltet Betalingskonto.
    * Velg bankkontoen som brukes til å trekke fakturabeløpet.  
18. Lukk siden.
19. Gå til Kunder > Betalingsoppsett > Betalingsmåter.
20. Klikk Ny.
21. Skriv inn en verdi i Betalingsmåte-feltet.
22. Velg alternativet Etterdatert sjekklareringspostering for å indikere at sjekkbeløpet posteres til en avregningskonto.
23. Velg Bank i feltet Kontotype.
    * Motkontoen for betalingsmetoden vil være en bank.  
24. Angi ønskede verdier i feltet Betalingskonto.
    * Velg bankkontoen som brukes til å trekke fakturabeløpet.  
25. Lukk siden.


