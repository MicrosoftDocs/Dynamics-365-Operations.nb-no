---
title: Opprette en salgsordre for et konfigurerbart produkt
description: Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921295"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="371cf-103">Opprette en salgsordre for et konfigurerbart produkt</span><span class="sxs-lookup"><span data-stu-id="371cf-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="371cf-104">Denne prosedyren viser hvordan du bruker en konfigurasjonsmal for et produkt på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="371cf-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="371cf-105">Dette eksemplet bruker høyttalermodellen D0006 i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="371cf-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="371cf-106">En salgsordrebehandler bruker vanligvis denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="371cf-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="371cf-107">Opprette en salgsordre</span><span class="sxs-lookup"><span data-stu-id="371cf-107">Create a sales order</span></span>

1. <span data-ttu-id="371cf-108">Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.</span><span class="sxs-lookup"><span data-stu-id="371cf-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="371cf-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="371cf-109">Select **New**.</span></span>
1. <span data-ttu-id="371cf-110">Velg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="371cf-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="371cf-111">Velg *US-001* i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="371cf-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="371cf-112">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="371cf-112">Select **OK**.</span></span>
1. <span data-ttu-id="371cf-113">Velg *D0006* i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="371cf-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="371cf-114">Du må velge et konfigurerbart produkt for denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="371cf-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="371cf-115">Velg **Produkt og forsyning**.</span><span class="sxs-lookup"><span data-stu-id="371cf-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="371cf-116">Velg **Konfigurer linje**.</span><span class="sxs-lookup"><span data-stu-id="371cf-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="371cf-117">Vær oppmerksom på at prisen er endret, basert på konfigurasjonen som ble valgt, og at feltet for å **ta med kabel** er satt til *Sann*.</span><span class="sxs-lookup"><span data-stu-id="371cf-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="371cf-118">Vær oppmerksom på standardprisen og innstillingene som er valgt for kabelen.</span><span class="sxs-lookup"><span data-stu-id="371cf-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="371cf-119">Velg **Lastmal**.</span><span class="sxs-lookup"><span data-stu-id="371cf-119">Select **Load template**.</span></span>
    * <span data-ttu-id="371cf-120">Dette eksemplet viser hvordan du kan bruke en mal for å velge en forhåndsdefinert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="371cf-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="371cf-121">Hvis du bruker denne prosedyren som en oppgaveveiledning og ønsker å se andre attributtverdier som er tilgjengelige, må du velge **Lås opp**-knappen.</span><span class="sxs-lookup"><span data-stu-id="371cf-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="371cf-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="371cf-122">Select **OK**.</span></span>
1. <span data-ttu-id="371cf-123">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="371cf-123">Select **OK**.</span></span>
1. <span data-ttu-id="371cf-124">Vis delen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="371cf-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="371cf-125">Velg **Produkt**-fanen.</span><span class="sxs-lookup"><span data-stu-id="371cf-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="371cf-126">Konfigurasjonen for varen er nå oppført under produktdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="371cf-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="371cf-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="371cf-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]