---
title: Definere lagre for overføringsordrer
description: Dette emnet beskriver hvordan du kan definere lagre for overføringsordrer.
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: aa5786df72f87da992f1020bbaaa1c2185adf043
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216719"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="2e511-103">Definere lagre for overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="2e511-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e511-104">Du kan bruke lagernivåer for å opprette et hierarki som støtter overføringsordrer mellom lagre.</span><span class="sxs-lookup"><span data-stu-id="2e511-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="2e511-105">På grunnlag av dette oppsettet blir hovedplanlegging brukt til å beregne varebehov på det enkelte lagernivå og generere planlagte overføringsordrer fra et tilordnet kildelager for å dekke behovet.</span><span class="sxs-lookup"><span data-stu-id="2e511-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="2e511-106">Klikk **Lagerstyring > Oppsett > Lageroppdeling > Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2e511-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="2e511-107">Velg lageret du vil fylle på.</span><span class="sxs-lookup"><span data-stu-id="2e511-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="2e511-108">På **Hovedplanlegging**-hurtigkategorien merker du av for **Påfylling**.</span><span class="sxs-lookup"><span data-stu-id="2e511-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="2e511-109">I **Hovedlager**-feltet velger du lageret du vil tilordne som påfyllingslager.</span><span class="sxs-lookup"><span data-stu-id="2e511-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="2e511-110">Hovedplanleggingen beregner et overføringsbehov for det valgte lager og genererer en planlagt overføringsordre fra tilordnet **Hovedlager**.</span><span class="sxs-lookup"><span data-stu-id="2e511-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="2e511-111">Hvis du fjerner merket for <STRONG>Påfylling</STRONG>, blir det valgte lageret tilordnet et lagernivå i forhold til <STRONG>Hovedlager</STRONG>, men <STRONG>Hovedlager</STRONG> blir ikke definert som et påfyllingslager.</span><span class="sxs-lookup"><span data-stu-id="2e511-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="2e511-112">Velg siden for å bruke det nye oppsettet.</span><span class="sxs-lookup"><span data-stu-id="2e511-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="2e511-113">Hvis du vil tilordne et lager for påfylling, må du først definere lagret som en lagringsdimensjon på siden <STRONG>Lagringsdimensjonsgrupper</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="2e511-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="2e511-114">På denne siden velger du feltet <STRONG>Aktiv</STRONG> og feltet <STRONG>Dekningsplanlegg etter dimensjon</STRONG> for lageret.</span><span class="sxs-lookup"><span data-stu-id="2e511-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="2e511-115">Angi leveringstid for transporten</span><span class="sxs-lookup"><span data-stu-id="2e511-115">Set up transport lead time</span></span>

<span data-ttu-id="2e511-116">Du må også definere leveringstiden for transport mellom lagrene på siden **Transportdager**.</span><span class="sxs-lookup"><span data-stu-id="2e511-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="2e511-117">Gå til **Lagerstyring > Oppsett > Distribusjon > Transportdager**.</span><span class="sxs-lookup"><span data-stu-id="2e511-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="2e511-118">I **Mottakspunkt**-feltet velger du **lager**.</span><span class="sxs-lookup"><span data-stu-id="2e511-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="2e511-119">Velg **Leverende lager**, **Mottakende lager** og **Transportdager**.</span><span class="sxs-lookup"><span data-stu-id="2e511-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="2e511-120">(Valgfritt) Du kan også angi transporttiden, avhengig av leveringsmåten, under **Transportdager per leveringsmåte**-fanen.</span><span class="sxs-lookup"><span data-stu-id="2e511-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
