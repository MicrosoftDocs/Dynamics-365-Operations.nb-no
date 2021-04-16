---
title: Tillegg for transportstyring
description: Dette emnet beskriver hvordan transportgenererte tillegg må knyttes til en tilleggskode.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 53c25f204e98a911e9697f5bb950706555749a55
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828327"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="8b65d-103">Tillegg for transportstyring</span><span class="sxs-lookup"><span data-stu-id="8b65d-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b65d-104">Som med alle tillegg må transportgenererte tillegg knyttes til en tilleggskode.</span><span class="sxs-lookup"><span data-stu-id="8b65d-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="8b65d-105">Ellers blir de ikke lagt tilbake i ordren som et tillegg.</span><span class="sxs-lookup"><span data-stu-id="8b65d-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="8b65d-106">**Tilleggskoden** bestemmer hvordan tillegget er i forhold til ordren og ordrelinjen der den er lagt til.</span><span class="sxs-lookup"><span data-stu-id="8b65d-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="8b65d-107">Gå til **Transportstyring > Oppsett > Vurdering > Tillegg** for å definere kvalifiseringskriteriene som bestemmer når en bestemt **tilleggskode** skal brukes på et tillegg.</span><span class="sxs-lookup"><span data-stu-id="8b65d-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="8b65d-108">Du må ha minst ett oppsett for hver relevante **tilleggsmodulinnstilling** (*kunde* og *leverandør*) der **Tilleggstypen** er angitt til *Ingen*.</span><span class="sxs-lookup"><span data-stu-id="8b65d-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="8b65d-109">Hvis dette mangler, blir *ikke* tillegget lagt til i ordren.</span><span class="sxs-lookup"><span data-stu-id="8b65d-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]