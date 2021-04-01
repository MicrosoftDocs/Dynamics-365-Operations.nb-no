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
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30022377cb02e7516cb98f48dc12e4f9e2ce172
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233037"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="88ab2-103">Produktbekreftelse for gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="88ab2-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88ab2-104">Gruppeplukking lar deg plukke varer for flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="88ab2-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="88ab2-105">Når gruppeplukking brukes, er varebekreftelse avgjørende for å bekrefte varene som legges til i grupper.</span><span class="sxs-lookup"><span data-stu-id="88ab2-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="88ab2-106">Du kan bekrefte varer i gruppeplukking mens gruppeplukkingen utføres.</span><span class="sxs-lookup"><span data-stu-id="88ab2-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="88ab2-107">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="88ab2-107">Where it applies</span></span>

<span data-ttu-id="88ab2-108">Varebekreftelse for gruppeplukking fungerer på samme måte som når du bekrefter varer i plukkingsprosesser som ikke er gruppebasert.</span><span class="sxs-lookup"><span data-stu-id="88ab2-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="88ab2-109">Oppsettet er basert på strekkodeoppsettet for produkt.</span><span class="sxs-lookup"><span data-stu-id="88ab2-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="88ab2-110">Definere varebekreftelse med gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="88ab2-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="88ab2-111">Åpne oppsettskjemaet for arbeidsbekreftelse for et menyelement på mobilenheten: **Lagerstyring** > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="88ab2-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="88ab2-112">Åpne **Arbeidsbekreftelsesoppsett** fra menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="88ab2-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="88ab2-113">Alternativ</span><span class="sxs-lookup"><span data-stu-id="88ab2-113">Option</span></span>        |                                    <span data-ttu-id="88ab2-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="88ab2-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88ab2-115">Produktbekreftelse</span><span class="sxs-lookup"><span data-stu-id="88ab2-115">Product confirmation</span></span> | <span data-ttu-id="88ab2-116">Lar deg bekrefte hver del av beholdningen fra den mobile enheten når den skannes.</span><span class="sxs-lookup"><span data-stu-id="88ab2-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]