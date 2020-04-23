---
title: Produktbekreftelse for gruppeplukking
description: Dette emnet beskriver hvordan du definerer varebekreftelse sammen med gruppeplukking.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e6493afb64acb4d7644aac8dad71a0917c76549
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205788"
---
[!include [banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a>Produktbekreftelse for gruppeplukking
Gruppeplukking lar deg plukke varer for flere ordrer samtidig. Når gruppeplukking brukes, er varebekreftelse avgjørende for å bekrefte varene som legges til i grupper. Du kan bekrefte varer i gruppeplukking mens gruppeplukkingen utføres.

## <a name="where-it-applies"></a>Der det er aktuelt
Varebekreftelse for gruppeplukking fungerer på samme måte som når du bekrefter varer i plukkingsprosesser som ikke er gruppebasert. Oppsettet er basert på strekkodeoppsettet for produkt.

## <a name="set-up-item-verification-with-cluster-picking"></a>Definere varebekreftelse med gruppeplukking
1.  Åpne oppsettskjemaet for arbeidsbekreftelse for et menyelement på mobilenheten: **Lagerstyring** > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**.
2.  Åpne **Arbeidsbekreftelsesoppsett** fra menyelementet på mobilenheten.

|        Alternativ        |                                    beskrivelse                                    |
|----------------------|-----------------------------------------------------------------------------------|
| Produktbekreftelse | Lar deg bekrefte hver del av beholdningen fra den mobile enheten når den skannes. |

