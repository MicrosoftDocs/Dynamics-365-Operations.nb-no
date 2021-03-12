---
title: Opprette en salgsordre for et konfigurerbart produkt
description: Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 77404694b3426f9ef051721191b607f91c908cc4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992326"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="eb175-103">Opprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="eb175-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb175-104">Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="eb175-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="eb175-105">Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="eb175-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="eb175-106">En salgsordrebehandler bruker vanligvis denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="eb175-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="eb175-107">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="eb175-107">Create a sales order</span></span>
1. <span data-ttu-id="eb175-108">Klikk på Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="eb175-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="eb175-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="eb175-109">Click New.</span></span>
3. <span data-ttu-id="eb175-110">Klikk på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="eb175-110">Click Sales order.</span></span>
4. <span data-ttu-id="eb175-111">Velg US-001 i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="eb175-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="eb175-112">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="eb175-112">Click OK.</span></span>
6. <span data-ttu-id="eb175-113">Velg D0006 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="eb175-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="eb175-114">Du må velge et konfigurerbart produkt for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eb175-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="eb175-115">Klikk på Produkt og forsyning.</span><span class="sxs-lookup"><span data-stu-id="eb175-115">Click Product and supply.</span></span>
8. <span data-ttu-id="eb175-116">Klikk på Konfigurer linje.</span><span class="sxs-lookup"><span data-stu-id="eb175-116">Click Configure line.</span></span>
    * <span data-ttu-id="eb175-117">Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å ta med kabel er satt til sann.</span><span class="sxs-lookup"><span data-stu-id="eb175-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="eb175-118">Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.</span><span class="sxs-lookup"><span data-stu-id="eb175-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="eb175-119">Klikk på Last inn mal.</span><span class="sxs-lookup"><span data-stu-id="eb175-119">Click Load template.</span></span>
    * <span data-ttu-id="eb175-120">Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="eb175-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="eb175-121">Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du klikke Lås opp-knappen.</span><span class="sxs-lookup"><span data-stu-id="eb175-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="eb175-122">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="eb175-122">Click OK.</span></span>
11. <span data-ttu-id="eb175-123">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="eb175-123">Click OK.</span></span>
12. <span data-ttu-id="eb175-124">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="eb175-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="eb175-125">Klikk på fanen Produkt.</span><span class="sxs-lookup"><span data-stu-id="eb175-125">Click the Product tab.</span></span>
    * <span data-ttu-id="eb175-126">Konfigurasjonen for varen er nå oppført under produktdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="eb175-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="eb175-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eb175-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="eb175-128">Velge produktkonfigurasjonen</span><span class="sxs-lookup"><span data-stu-id="eb175-128">Select the product configuration</span></span>

