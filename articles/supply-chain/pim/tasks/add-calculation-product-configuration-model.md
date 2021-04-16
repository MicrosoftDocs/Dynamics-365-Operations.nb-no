---
title: Legge til beregning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812686"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Legge til beregning i en produktkonfigurasjonsmodell

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell. Den viser hvordan du kan opprette et logisk uttrykk ved hjelp av operatoren "If" for å angi en høyttalerhøyde på 10 for hvite høyttalere og 15 for alle andre kabinettyper. Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.


## <a name="add-a-calculation"></a>Legge til en beregning

## <a name="create-calculation-expression"></a>Opprette beregningsuttrykk
1. Klikk på Rediger uttrykk.
2. I ConstraintBody-feltet skriver du inn If[CabinetFinish=="White", 10, 15].
3. Klikk på Valider.
4. Klikk på Lukk.
5. Klikk på OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]