---
title: Opprette en bestilling som styres av budsjett
description: Bruk denne fremgangsmåten til å opprette en bestilling som sjekkes for tilgjengelig budsjett.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e2bfec4d7d38ef95d1f0ce3bd89938337ecf731
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572055"
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