--- 
title: Opprette en salgsordre for et konfigurerbart produkt
description: "Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 4150c977824da2a4c6c4d2174351db885774fa9c
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="cf421-103">Opprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="cf421-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf421-104">Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="cf421-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="cf421-105">Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="cf421-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="cf421-106">En salgsordrebehandler bruker vanligvis denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="cf421-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="cf421-107">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="cf421-107">Create a sales order</span></span>
1. <span data-ttu-id="cf421-108">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="cf421-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="cf421-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cf421-109">Click New.</span></span>
3. <span data-ttu-id="cf421-110">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="cf421-110">Click Sales order.</span></span>
4. <span data-ttu-id="cf421-111">Velg US-001 i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="cf421-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="cf421-112">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cf421-112">Click OK.</span></span>
6. <span data-ttu-id="cf421-113">Velg D0006 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="cf421-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="cf421-114">Du må velge et konfigurerbart produkt for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="cf421-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="cf421-115">Klikk Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="cf421-115">Click Product and supply.</span></span>
8. <span data-ttu-id="cf421-116">Klikk Konfigurer linje.</span><span class="sxs-lookup"><span data-stu-id="cf421-116">Click Configure line.</span></span>
    * <span data-ttu-id="cf421-117">Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å ta med kabel er satt til sann.</span><span class="sxs-lookup"><span data-stu-id="cf421-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="cf421-118">Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.</span><span class="sxs-lookup"><span data-stu-id="cf421-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="cf421-119">Klikk Last inn mal.</span><span class="sxs-lookup"><span data-stu-id="cf421-119">Click Load template.</span></span>
    * <span data-ttu-id="cf421-120">Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="cf421-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="cf421-121">Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du klikke Lås opp-knappen.</span><span class="sxs-lookup"><span data-stu-id="cf421-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="cf421-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cf421-122">Click OK.</span></span>
11. <span data-ttu-id="cf421-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="cf421-123">Click OK.</span></span>
12. <span data-ttu-id="cf421-124">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="cf421-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="cf421-125">Klikk kategorien Produkt.</span><span class="sxs-lookup"><span data-stu-id="cf421-125">Click the Product tab.</span></span>
    * <span data-ttu-id="cf421-126">Konfigurasjonen for varen er nå oppført under produktdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="cf421-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="cf421-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="cf421-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="cf421-128">Velge produktkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="cf421-128">Select the product configuration</span></span>


