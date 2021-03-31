---
title: Tilordne en produktlivssyklustilstand til en frigitt produktstandard
description: Denne fremgangsmåten viser hvordan du tilordner en produktlivssyklustilstand til en frigitt produktstandard og tilhørende varianter.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226743"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Tilordne en produktlivssyklustilstand til en frigitt produktstandard

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du tilordner en produktlivssyklustilstand til en frigitt produktstandard og tilhørende varianter. Forutsetning: Du må spille av oppgaveveiledningen Opprette en ny produktlivssyklustilstand først for å være sikker på at du har minst én produktlivssyklustilstand opprettet før du kan spille av denne oppgaveveiledningen.


## <a name="find-a-released-product-master"></a>Finne en frigitt produktstandard
1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Finn og velg ønsket post i listen.

> [!NOTE]
> En produktstandard har produktets undertype Produktstandard.  

## <a name="update-the-lifecycle-state"></a>Oppdatere livssyklustilstanden
1. Klikk på Rediger.
2. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.
3. Klikk på Lagre.
4. Klikk på Ja.

> [!NOTE]
> Hvis Ja er valgt, oppdateres også alle de tilknyttede frigitte produktvariantene som har samme opprinnelige status som den frigitte produktstandarden, til den nye produktlivssyklustilstanden. Hvis Nei er valgt, beholder alle varianter den faktiske tilstanden. Varianter som har en annen produktlivssyklustilstand fra den frigitte produktstandarden, blir ikke oppdatert.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Kontrollere livssyklustilstanden for variantene
1. Klikk på Frigitte produktvarianter.

> [!NOTE]
> Vær oppmerksom på at alle varianter har arvet den valgte livssyklustilstanden fra den frigitte produktstandarden.  

2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]