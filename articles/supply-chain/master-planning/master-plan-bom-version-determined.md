---
title: "Fastslå stykklisteversjon"
description: "Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e6745a52138e545b557fa1aa286cd49481b2ecd
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="determine-the-bom-version"></a>Fastslå stykklisteversjon

[!include[banner](../includes/banner.md)]


Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned. 

Områdedimensjonen er alltid kjent og angis i behovstransaksjonen. Følgende prosess brukes til å fastsette hvilken stykklisteversjon som skal brukes:

-   Hvis en stykklisteversjon er definert for varen i området med behov, brukes den områdespesifikke stykklisten.
-   Hvis ingen områdespesifikk stykklisteversjon er definert for en vare i området med behov, brukes en generell stykkliste. En generell stykkliste viser ikke til noe område, og er gyldig for flere områder. Hvis en generell stykkliste finnes, brukes den.
-   Hvis det ikke finnes noen generell stykklisteversjon som kan brukes, vil nedbrytingen av behov stoppe her.

En gyldig stykklisteversjon må oppfylle de obligatoriske kriteriene for dato og antall, uansett om den er områdespesifikk eller generell.






