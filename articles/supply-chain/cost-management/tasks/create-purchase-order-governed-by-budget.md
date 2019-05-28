---
title: Opprette en bestilling som styres av budsjett
description: Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e82e40d67547f5932a4805f2580e8c9f58def284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569989"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Opprette en bestilling som styres av budsjett

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett. Denne registreringen bruker USMF-demodatafirmaet.


## <a name="review-the-budget-control-configuration"></a>Gå gjennom budsjettkontrollkonfigurasjonen
1. Gå til Budsjettering > Oppsett > Budsjettkontroll > Busjettkontrollkonfigurasjon.
2. Klikk fanen Tilgjengelige budsjettmidler.
3. Klikk fanen Dokumenter og kladder.
4. Klikk fanen Definer budsjettkontrollregler.
5. Klikk fanen Definer budsjettgrupper.
6. Lukk siden.

## <a name="create-the-purchase-order-header"></a>Opprette bestillingshode
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk Ny.
3. Angi eller velg en verdi i Leverandørkonto-feltet.
4. Utvid delen Generelt.
5. Angi datoen til 2016-01-01 i feltet Regnskapsdato.
6. Klikk OK.

## <a name="add-a-purchase-order-line"></a>Legge til en bestillingslinje
1. Angi eller velg en verdi i feltet Innkjøpskategori.
2. Sett Antall til 2.
3. Angi eller velg en verdi i Enhet-feltet.
4. Sett enhetspris til 10000.
5. Klikk Finans.
6. Klikk Fordel beløp.
7. Angi verdien 601300-001-023-- i feltet Finanskonto.
8. Lukk siden.

## <a name="perform-budget-checking"></a>Utfør budsjettkontroll
1. Klikk Finans.
2. Klikk Utfør budsjettkontroll.
3. Klikk Finans.
4. Klikk Feil eller advarsler for budsjettkontroll.
5. Klikk Lukk.

