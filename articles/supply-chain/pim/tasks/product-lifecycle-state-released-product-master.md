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
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c4e02a064fe84446fa54cc05b9a6a902c1860
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213153"
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
1. Klikk Rediger.
2. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.
3. Klikk Lagre.
4. Klikk Ja.

> [!NOTE]
> Hvis Ja er valgt, oppdateres også alle de tilknyttede frigitte produktvariantene som har samme opprinnelige status som den frigitte produktstandarden, til den nye produktlivssyklustilstanden. Hvis Nei er valgt, beholder alle varianter den faktiske tilstanden. Varianter som har en annen produktlivssyklustilstand fra den frigitte produktstandarden, blir ikke oppdatert.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Kontrollere livssyklustilstanden for variantene
1. Klikk Frigitte produktvarianter.

> [!NOTE]
> Vær oppmerksom på at alle varianter har arvet den valgte livssyklustilstanden fra den frigitte produktstandarden.  

2. Merk den valgte raden i listen.
3. Angi eller velg en verdi i feltet Livssyklustilstand for produkt.

