---
title: Tilordne en produktlivssyklustilstand til en frigitt produktstandard
description: Denne fremgangsmåten viser hvordan du tilordner en produktlivssyklustilstand til en frigitt produktstandard og tilhørende varianter.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555914"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Tilordne en produktlivssyklustilstand til en frigitt produktstandard

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

