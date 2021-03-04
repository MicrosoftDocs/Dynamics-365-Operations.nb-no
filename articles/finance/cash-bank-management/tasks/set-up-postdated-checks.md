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
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446461"
---
# <a name="set-up-postdated-checks"></a>Definere etterdaterte sjekker

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]