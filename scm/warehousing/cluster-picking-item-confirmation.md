---
title: Produktbekreftelse for gruppeplukking
description: Dette emnet beskriver hvordan du definerer varebekreftelse sammen med gruppeplukking.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 17f5761df4294abfea28e7cb8d50c86f1e3e136f
ms.contentlocale: nb-no
ms.lasthandoff: 07/18/2017

---

[!include[banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="046d9-103">Produktbekreftelse for gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="046d9-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="046d9-104">Gruppeplukking lar deg plukke varer for flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="046d9-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="046d9-105">Når gruppeplukking brukes, er varebekreftelse avgjørende for å bekrefte varene som legges til i grupper.</span><span class="sxs-lookup"><span data-stu-id="046d9-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="046d9-106">Du kan bekrefte varer i gruppeplukking mens gruppeplukkingen utføres.</span><span class="sxs-lookup"><span data-stu-id="046d9-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="046d9-107">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="046d9-107">Where it applies</span></span>
<span data-ttu-id="046d9-108">Varebekreftelse for gruppeplukking fungerer på samme måte som når du bekrefter varer i plukkingsprosesser som ikke er gruppebasert.</span><span class="sxs-lookup"><span data-stu-id="046d9-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="046d9-109">Oppsettet er basert på strekkodeoppsettet for produkt.</span><span class="sxs-lookup"><span data-stu-id="046d9-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="046d9-110">Definere varebekreftelse med gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="046d9-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="046d9-111">Åpne oppsettskjemaet for arbeidsbekreftelse for et menyelement på mobilenheten: **Lagerstyring** > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="046d9-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="046d9-112">Åpne **Arbeidsbekreftelsesoppsett** fra menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="046d9-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

| <span data-ttu-id="046d9-113">Alternativ</span><span class="sxs-lookup"><span data-stu-id="046d9-113">Option</span></span>        | <span data-ttu-id="046d9-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="046d9-114">Description</span></span>   | 
| ------------- | ------------- |
|<span data-ttu-id="046d9-115">Produktbekreftelse</span><span class="sxs-lookup"><span data-stu-id="046d9-115">Product confirmation</span></span> | <span data-ttu-id="046d9-116">Lar deg bekrefte hver del av beholdningen fra den mobile enheten når den skannes.</span><span class="sxs-lookup"><span data-stu-id="046d9-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span>|

