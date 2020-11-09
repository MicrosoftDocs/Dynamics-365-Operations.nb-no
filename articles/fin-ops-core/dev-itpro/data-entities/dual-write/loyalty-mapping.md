---
title: Kundefordelskort og belønningspoeng
description: Dette emnet beskriver integreringen av data om kundefordelskort og belønningspoeng mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998020"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="73766-103">Kundefordelskort og belønningspoeng</span><span class="sxs-lookup"><span data-stu-id="73766-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="73766-104">Firmaer klassifiserer kunder og tilbyr avanserte tjenester basert på kunders handle- og forbruksmønstre.</span><span class="sxs-lookup"><span data-stu-id="73766-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="73766-105">I Microsoft Dynamics 365-serien med programmer har Dynamics 365 Commerce infrastrukturen og funksjonene for å lette og håndtere kundelojalitetskort, belønningspoeng, lojalitetsbasert prissetting og belønningsbaserte handleopplevelser.</span><span class="sxs-lookup"><span data-stu-id="73766-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="73766-106">Når data om kundefordelskort og belønningspoeng i Commerce er synkronisert med Common Data Service, kan modelldrevne apper i Dynamics 365 bruke disse dataene.</span><span class="sxs-lookup"><span data-stu-id="73766-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="73766-107">Dynamics 365 Customer Service-brukere kan for eksempel bruke dataene til å gi de samme avanserte tjenestene gjennom brukerstøtten.</span><span class="sxs-lookup"><span data-stu-id="73766-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="73766-108">Maler</span><span class="sxs-lookup"><span data-stu-id="73766-108">Templates</span></span>

| <span data-ttu-id="73766-109">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="73766-109">Finance and Operations apps</span></span> | <span data-ttu-id="73766-110">Modelldrevne apper i Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="73766-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="73766-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="73766-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="73766-112">Fordelskort</span><span class="sxs-lookup"><span data-stu-id="73766-112">Loyalty card</span></span>                | <span data-ttu-id="73766-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="73766-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="73766-114">Denne malen synkroniserer informasjon om kundefordelskort.</span><span class="sxs-lookup"><span data-stu-id="73766-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="73766-115">Fordelspoeng</span><span class="sxs-lookup"><span data-stu-id="73766-115">Loyalty reward points</span></span>       | <span data-ttu-id="73766-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="73766-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="73766-117">Denne malen synkroniserer informasjon om fordelspoeng.</span><span class="sxs-lookup"><span data-stu-id="73766-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
