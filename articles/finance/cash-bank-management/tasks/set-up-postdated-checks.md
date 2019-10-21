---
title: Definere etterdaterte sjekker
description: Dette emnet forklarer hvordan du angir om du vil postere journaloppføringer for etterdaterte sjekker og hvilke posteringsjournaler som skal brukes til å slette oppføringer og leverandørbetalinger.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 035f6e3b0268f8ee4c9006ca5f0527133cf2771c
ms.sourcegitcommit: 69f8233e86b32347474a25d83b4ac5920f60407d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2019
ms.locfileid: "2538484"
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
18. Klikk Lagre.
19. Lukk siden.

