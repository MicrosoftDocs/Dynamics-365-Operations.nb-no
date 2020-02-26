---
title: Konfigurere kontantstørrelser for salgsstedet
description: Kontantstørrelser for sedler og mynter kan defineres i Back Office som skal brukes av kasserere, selgere og ledere i butikken ved salgsstedet.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a34ae8084c0ad55221f4ab93eb8c6481fa8c4771
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023513"
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
