---
title: Opprette varebehov for serviceordrer
description: Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b342b20cc11addc53fc6ea4e1a23d3b449eb9ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257950"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="8637d-103">Opprette varebehov for serviceordrer</span><span class="sxs-lookup"><span data-stu-id="8637d-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8637d-104">Du kan opprette en serviceordre for å spore og behandle tjenestene du tilbyr kundene dine.</span><span class="sxs-lookup"><span data-stu-id="8637d-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="8637d-105">Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den.</span><span class="sxs-lookup"><span data-stu-id="8637d-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="8637d-106">Et varebehov kan brukes umiddelbart fra lageret, eller det kan starte en produksjonsordre for varen.</span><span class="sxs-lookup"><span data-stu-id="8637d-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="8637d-107">Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="8637d-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="8637d-108">Varebehov for serviceordrer behandles via et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="8637d-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="8637d-109">Hvis du vil opprette et varebehov opprettes på en serviceordre, må serviceordren tilordnes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="8637d-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="8637d-110">Når du har opprettet et varebehov for en serviceordre, kan du vise varebehovet i **Prosjekter**-skjemaet for det valgte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="8637d-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="8637d-111">Opprette et varebehov for en serviceordre</span><span class="sxs-lookup"><span data-stu-id="8637d-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="8637d-112">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="8637d-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="8637d-113">Velg serviceordren du vil opprette et varebehov for.</span><span class="sxs-lookup"><span data-stu-id="8637d-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="8637d-114">I **handlingsruten** på fanen **Fordeling** klikker du på **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="8637d-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="8637d-115">Skriv inn informasjon for den nødvendige varen i **Varebehov**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8637d-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="8637d-116">Hvis du vil ha mer informasjon om de spesifikke feltene, kan du se [Varebehov (skjema)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="8637d-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="8637d-117">Opprette et varebehov for en serviceavtale</span><span class="sxs-lookup"><span data-stu-id="8637d-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="8637d-118">Klikk på **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="8637d-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="8637d-119">Åpne serviceavtalen som du vil opprette et varebehov for.</span><span class="sxs-lookup"><span data-stu-id="8637d-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="8637d-120">På hurtigfanen **Linjer** klikker du på **Legg til** for å opprette en ny linje.</span><span class="sxs-lookup"><span data-stu-id="8637d-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="8637d-121">I **Transaksjonstype**-feltet velger du **Vare**.</span><span class="sxs-lookup"><span data-stu-id="8637d-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="8637d-122">I **Vareoppsett**-feltet velger du **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="8637d-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="8637d-123">I **Varenummer**-feltet velger du varen som er nødvendig for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="8637d-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="8637d-124">På hurtigfanen **Linjedetaljer** på fanen **Produktdimensjoner** i feltet **Område** velger du lagerområdet for varen.</span><span class="sxs-lookup"><span data-stu-id="8637d-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="8637d-125">Hvis du vil opprette en serviceordre fra avtalelinjen, går du til hurtigfanen **Linjer**, klikker på **Opprett serviceordrer** og skriver deretter inn den relevante informasjonen i skjemaet **Opprett serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="8637d-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="8637d-126">Se også</span><span class="sxs-lookup"><span data-stu-id="8637d-126">See also</span></span>

<span data-ttu-id="8637d-127">[Opprette serviceordrer automatisk](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="8637d-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]