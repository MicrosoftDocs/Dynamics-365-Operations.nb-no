---
title: Konfigurere kontantstørrelser for salgsstedet
description: Kontantstørrelser for sedler og mynter kan defineres i Back Office som skal brukes av kasserere, selgere og ledere i butikken ved salgsstedet.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5dbef67728e86259ee48b51c48921f6e44a61015
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793063"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Konfigurere kontantstørrelser for salgsstedet

[!include [banner](includes/banner.md)]

Kontantstørrelser for sedler og mynter kan defineres i Back Office som skal brukes av kasserere, selgere og ledere i butikken ved salgsstedet. Disse størrelsene kan være til hjelp for å telle kontanter for dagsoppgjør eller raskt gjennomføring av et salg.

## <a name="define-denominations"></a>Definere størrelser

Størrelsene er definert per butikk i alternativet **Oppsett** \> **Kontantoppgjør** fra butikkoppgjørsiden.

![Kontantoppgjør-alternativet](./media/image1-denomination.png)

Slik definerer du en størrelse:

1. Klikk på **Ny**.
1. Angi typen (mynt eller seddel).
1. Angi beløpet (verdi).

![Kontantoppgjørsstørrelser-side](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Konfigurer funksjonalitetsprofilen

Ved kontantbetaling i salgsstedet POS kan brukeren bruke seddelstørrelsene til raskt å skrive inn beløpet som betales av kunden. I funksjonalitetsprofilen kan du konfigurere de to alternativene for å vise størrelsen i salgssted.

- **Større eller lik det forfalte beløpet** – Som standard viser salgssted bare seddelstørrelser som er større enn det forfalte beløpet, noe som muliggjør ett trykks betaling. Hvis det forfalte beløpet for eksempel er $ 7,50, kan salgssted vise følgende størrelser: $ 10, $ 20, $ 50 og $ 100. Berøres noen av disse beløpene, gjennomføres automatisk salget for dette beløpet. Sedlene $1 og $5 vises ikke siden disse beløpene er lavere enn beløpet som forfaller.
- **Alle størrelser** – Velg dette alternativet for alltid å vise alle seddelstørrelser i salgssted, uavhengig av forfalt beløp. Dette betyr at brukeren kan bruke en kombinasjon av sedler for å nå det forfalte beløpet. Hvis for eksempel det forfalte beløpet er $ 25,00, kan brukeren velge $ 20 og $ 5 for å fullføre salget.


[!INCLUDE[footer-include](../includes/footer-banner.md)]