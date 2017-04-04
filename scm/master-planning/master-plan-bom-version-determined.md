---
title: "Fastslå hvilken versjon av Stykklisten"
description: "Under behovsnedbrytingen finne vil planleggingsmotoren en gyldig stykklisteversjon på grunnlag av området hvis en vare har en standard ordretype for produksjon."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e4f5f02dfa986669decbc8854148b5eff928c2a
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-bom-version"></a>Fastslå hvilken versjon av Stykklisten

Under behovsnedbrytingen finne vil planleggingsmotoren en gyldig stykklisteversjon på grunnlag av området hvis en vare har en standard ordretype for produksjon. 

Områdedimensjonen er alltid kjent og angis i behovstransaksjonen. Følgende prosess brukes til å fastsette hvilken stykklisteversjon som skal brukes:

-   Hvis en stykklisteversjon er definert for varen i området med behov, brukes den områdespesifikke stykklisten.
-   Hvis ingen områdespesifikk stykklisteversjon er definert for en vare i området med behov, brukes en generell stykkliste. En generell stykkliste viser ikke til noe område, og er gyldig for flere områder. Hvis en generell stykkliste finnes, brukes den.
-   Hvis det ikke finnes noen generell stykklisteversjon som kan brukes, vil nedbrytingen av behov stoppe her.

En gyldig stykklisteversjon må oppfylle de obligatoriske kriteriene for dato og antall, uansett om den er områdespesifikk eller generell.




