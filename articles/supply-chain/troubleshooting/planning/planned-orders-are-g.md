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
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742010"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Hovedplanlegging genererer planlagte bestillinger for fantomprodukter

KB-nummer: 4614729

## <a name="symptoms"></a>Symptomer

Planlagte ordrer genereres for fantomprodukter etter hovedplanlegging kjøres.

## <a name="resolution"></a>Oppløsning

Innstillingen for **Fantom**-alternativet for frigitte produkter bestemmer standard linjetype i stykklisten. Hvis **Fantom**-alternativet er satt til *Ja*, vil systemet fremdeles opprette planlagte bestillinger for varen, men alternativet for **Direkte avledet behov** for hver planlagte bestilling blir satt til *Ja*. Derfor kan ikke den planlagte produksjonsordren autoriseres på egen hånd. I stedet inkluderes den alltid automatisk når den overordnede produksjonsordren autoriseres. I tillegg blir stykklistelinjene til den planlagte fantomordren tatt med i stykklisten til den overordnede produksjonsordren.
