--- 
title: Legge til beregning i en produktkonfigurasjonsmodell
description: "Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2db8fb922b085a7f118822ef4fd974ac338f4d99
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>Legge til beregning i en produktkonfigurasjonsmodell

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell. Den viser hvordan du kan opprette et logisk uttrykk ved hjelp av operatoren "If" for å angi en høyttalerhøyde på 10 for hvite høyttalere og 15 for alle andre kabinettyper. Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.


## <a name="add-a-calculation"></a>Legge til en beregning

## <a name="create-calculation-expression"></a>Opprette beregningsuttrykk
1. Klikk Rediger uttrykk.
2. I ConstraintBody-feltet skriver du inn If[CabinetFinish=="White", 10, 15].
3. Klikk Valider.
4. Klikk Lukk.
5. Klikk OK.


