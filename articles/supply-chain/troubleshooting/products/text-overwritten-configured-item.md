---
title: Tekst overskrives når vare konfigureres på en salgsordrelinje
description: Når et produkt er konfigurert på en salgsordrelinje, overskrives endret tekst med standardtekst. Endre teksten etter at du har konfigurert linjen, ikke før.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477154"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Varetekst overskrives når et produkt konfigureres på en salgsordrelinje

## <a name="symptoms"></a>Symptomer

Dette problemet oppstår når du oppretter en salgsordrelinje for en konfigurerbar vare og deretter endrer vareteksten. Når du konfigurerer varen og velger **OK**, overskrives teksten med standardteksten.

## <a name="resolution"></a>Løsning

Denne virkemåten er forventet. Tekstfeltet inneholder variantnavnet, som bare fylles ut etter at du har konfigurert linjen. Du må derfor endre teksten etter at du har konfigurert linjen, ikke før.
