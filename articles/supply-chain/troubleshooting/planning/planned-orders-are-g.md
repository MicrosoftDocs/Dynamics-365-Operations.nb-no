---
title: Hovedplanlegging genererer planlagte bestillinger for fantomprodukter
description: Planlagte ordrer genereres for fantomprodukter etter hovedplanlegging kjøres.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026786"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Hovedplanlegging genererer planlagte bestillinger for fantomprodukter

KB-nummer: 4614729

## <a name="symptoms"></a>Symptomer

Planlagte ordrer genereres for fantomprodukter etter hovedplanlegging kjøres.

## <a name="resolution"></a>Oppløsning

Innstillingen for **Fantom**-alternativet for frigitte produkter bestemmer standard linjetype i stykklisten. Hvis **Fantom**-alternativet er satt til *Ja*, vil systemet fremdeles opprette planlagte bestillinger for varen, men alternativet for **Direkte avledet behov** for hver planlagte bestilling blir satt til *Ja*. Derfor kan ikke den planlagte produksjonsordren autoriseres på egen hånd. I stedet inkluderes den alltid automatisk når den overordnede produksjonsordren autoriseres. I tillegg blir stykklistelinjene til den planlagte fantomordren tatt med i stykklisten til den overordnede produksjonsordren.
