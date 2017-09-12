--- 
title: "Opprette en bestilling for en engangsleverandør"
description: "Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="e7d41-103">Opprette en bestilling for en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="e7d41-103">Create a purchase order for a one-time supplier</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7d41-104">Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="e7d41-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="e7d41-105">Leverandøren opprettes automatisk med bestillingen, i stedet for å opprette leverandørkontoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="e7d41-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="e7d41-106">Bestillinger opprettes vanligvis av en innkjøpsagent.</span><span class="sxs-lookup"><span data-stu-id="e7d41-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="e7d41-107">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e7d41-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="e7d41-108">Det er en forutsetning at kontoen for engangsleverandør er definert på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="e7d41-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="e7d41-109">Opprette en bestilling for en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="e7d41-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="e7d41-110">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="e7d41-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e7d41-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e7d41-111">Click New.</span></span>
3. <span data-ttu-id="e7d41-112">Velg Ja i feltet Engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="e7d41-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="e7d41-113">En leverandørkonto blir automatisk opprettet og tilordnet bestillingen.</span><span class="sxs-lookup"><span data-stu-id="e7d41-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="e7d41-114">Leverandørkontoen blir opprettet basert på malen som er angitt i kategorien Generelt på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="e7d41-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="e7d41-115">I Navn-feltet skriver du inn et unikt navn for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="e7d41-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="e7d41-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e7d41-116">Click OK.</span></span>
    * <span data-ttu-id="e7d41-117">Bestillingen kan nå fullføres og behandles som hvilken som helst ordre.</span><span class="sxs-lookup"><span data-stu-id="e7d41-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="e7d41-118">Det finnes ingen spesielle egenskaper som er relatert til hvordan dette gjøres.</span><span class="sxs-lookup"><span data-stu-id="e7d41-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="e7d41-119">Fakturaen registrerer en forfallstransaksjon på leverandørkontoen som ble opprettet med ordren, og deretter behandles betalingen.</span><span class="sxs-lookup"><span data-stu-id="e7d41-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="e7d41-120">Når dette er fullført, kan leverandørkontoen slettes.</span><span class="sxs-lookup"><span data-stu-id="e7d41-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="e7d41-121">Dette gjøres vanligvis av leverandøravdelingen.</span><span class="sxs-lookup"><span data-stu-id="e7d41-121">This is typically done by the accounts payable department.</span></span>  


