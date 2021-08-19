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
ms.openlocfilehash: bb753878a3ce8c29e2a7e7e90e1d6cf6d56c0358d16e3173253ae729cb123502
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731823"
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