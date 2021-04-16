---
title: Statuser for transportstyring
description: Dette emnet forklarer hvordan du oppretter en transportstatus og tilordner statusen til en transportørstatus.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807614"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="489ff-103">Statuser for transportstyring</span><span class="sxs-lookup"><span data-stu-id="489ff-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="489ff-104">Definer primærkoder for transportstatuser for å tolke koder som leveres av transportørene.</span><span class="sxs-lookup"><span data-stu-id="489ff-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="489ff-105">Dermed kan du integrere med transportører for å angi en status.</span><span class="sxs-lookup"><span data-stu-id="489ff-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="489ff-106">Transportstatusen du angir for en primær kode for transportstatus, kan hjelpe deg med å spore status for en last, forsendelse eller container.</span><span class="sxs-lookup"><span data-stu-id="489ff-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="489ff-107">Den bestemte transportstatusen for last, forsendelse eller container kan bare oppdateres gjennom dataintegrering, og ikke manuelt via brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="489ff-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="489ff-108">Opprette en transportstatus</span><span class="sxs-lookup"><span data-stu-id="489ff-108">Create a transportation status</span></span>

<span data-ttu-id="489ff-109">Hvis du vil opprette en transportstatus, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="489ff-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="489ff-110">Gå til **Transportstyring \> Oppsett \> Transportstatusmal**.</span><span class="sxs-lookup"><span data-stu-id="489ff-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="489ff-111">Velg **Ny** for å opprette en transportstatusmal.</span><span class="sxs-lookup"><span data-stu-id="489ff-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="489ff-112">I **Transportstatusmal**-feltet angir du inn en unik kode for transportstatusen.</span><span class="sxs-lookup"><span data-stu-id="489ff-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="489ff-113">I **Transporttype**-feltet velger du enten *Transportør* eller *Hub* som transporttype.</span><span class="sxs-lookup"><span data-stu-id="489ff-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="489ff-114">Angi et navn og en transportstatus.</span><span class="sxs-lookup"><span data-stu-id="489ff-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="489ff-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="489ff-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="489ff-116">Tilordne en transportstatus til en transportørstatus</span><span class="sxs-lookup"><span data-stu-id="489ff-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="489ff-117">Følg denne fremgangsmåten for å tilordne en transportstatus til en transportørstatus:</span><span class="sxs-lookup"><span data-stu-id="489ff-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="489ff-118">Gå til **Transportstyring \> Oppsett \> Transportører \> Transportstatus for transportør**.</span><span class="sxs-lookup"><span data-stu-id="489ff-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="489ff-119">Velg **Ny** for å tilordne en kode fra en transportør til en primær kode for transportstatus.</span><span class="sxs-lookup"><span data-stu-id="489ff-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="489ff-120">Velg den unike ID-en for transportøren og transportørtjenesten.</span><span class="sxs-lookup"><span data-stu-id="489ff-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="489ff-121">Velg transportstatuskoden som du vil tilordne til den valgte transportørkoden.</span><span class="sxs-lookup"><span data-stu-id="489ff-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="489ff-122">Angi den eksterne koden transportøren bruker.</span><span class="sxs-lookup"><span data-stu-id="489ff-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="489ff-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="489ff-123">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]