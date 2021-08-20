---
title: Fastslå stykklisteversjon
description: Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91a55bfcd10ee0efbbf1170ad29194c17ea72d62cf5516e2661b43bad7446808
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766080"
---
# <a name="determine-the-bom-version"></a>Fastslå stykklisteversjon

[!include [banner](../includes/banner.md)]

Hvis en vare har produksjon som type standard bestilling, finner planleggingsmotoren en gyldig stykklisteversjon basert på området når behov brytes ned. 

Områdedimensjonen er alltid kjent og angis i behovstransaksjonen. Følgende prosess brukes til å fastsette hvilken stykklisteversjon som skal brukes:

-   Hvis en stykklisteversjon er definert for varen i området med behov, brukes den områdespesifikke stykklisten.
-   Hvis ingen områdespesifikk stykklisteversjon er definert for en vare i området med behov, brukes en generell stykkliste. En generell stykkliste viser ikke til noe område, og er gyldig for flere områder. Hvis en generell stykkliste finnes, brukes den.
-   Hvis det ikke finnes noen generell stykklisteversjon som kan brukes, vil nedbrytingen av behov stoppe her.

En gyldig stykklisteversjon må oppfylle de obligatoriske kriteriene for dato og antall, uansett om den er områdespesifikk eller generell.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]