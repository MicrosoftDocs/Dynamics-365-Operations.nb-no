---
title: Opprette en bestilling som styres av budsjett
description: Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821375"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Opprette en bestilling som styres av budsjett

[!include [banner](../../includes/banner.md)]

Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett. Denne registreringen bruker USMF-demodatafirmaet.


## <a name="review-the-budget-control-configuration"></a>Gå gjennom budsjettkontrollkonfigurasjonen
1. Gå til Budsjettering > Oppsett > Budsjettkontroll > Busjettkontrollkonfigurasjon.
2. Klikk på fanen Tilgjengelige budsjettmidler.
3. Klikk på fanen Dokumenter og kladder.
4. Klikk på fanen Definer budsjettkontrollregler.
5. Klikk på fanen Definer budsjettgrupper.
6. Lukk siden.

## <a name="create-the-purchase-order-header"></a>Opprette bestillingshode
1. Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.
2. Klikk på Ny.
3. Angi eller velg en verdi i Leverandørkonto-feltet.
4. Utvid delen Generelt.
5. Angi datoen til 2016-01-01 i feltet Regnskapsdato.
6. Klikk på OK.

## <a name="add-a-purchase-order-line"></a>Legge til en bestillingslinje
1. Angi eller velg en verdi i feltet Innkjøpskategori.
2. Sett Antall til 2.
3. Angi eller velg en verdi i Enhet-feltet.
4. Sett enhetspris til 10000.
5. Klikk på Finans.
6. Klikk på Fordel beløp.
7. Angi verdien 601300-001-023-- i feltet Finanskonto.
8. Lukk siden.

## <a name="perform-budget-checking"></a>Utfør budsjettkontroll
1. Klikk på Finans.
2. Klikk på Utfør budsjettkontroll.
3. Klikk på Finans.
4. Klikk på Feil eller advarsler for budsjettkontroll.
5. Klikk på Lukk.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]