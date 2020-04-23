---
title: Varebehov for serviceordre
description: Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e31f58cf8782c715b97bdae0e89f684b15a76d2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215085"
---
# <a name="service-order-item-requirements"></a><span data-ttu-id="1310d-103">Varebehov for serviceordre</span><span class="sxs-lookup"><span data-stu-id="1310d-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1310d-104">Du kan opprette en serviceordre for å spore og behandle tjenestene du tilbyr kundene dine.</span><span class="sxs-lookup"><span data-stu-id="1310d-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="1310d-105">Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den.</span><span class="sxs-lookup"><span data-stu-id="1310d-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="1310d-106">Et varebehov kan brukes umiddelbart fra lageret, eller det kan starte en produksjonsordre for varen.</span><span class="sxs-lookup"><span data-stu-id="1310d-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="1310d-107">Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="1310d-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="1310d-108">Varebehov for serviceordrer behandles via et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="1310d-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="1310d-109">Hvis du vil opprette et varebehov opprettes på en serviceordre, må serviceordren tilknyttes et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="1310d-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="1310d-110">Så snart et varebehov er opprettet for en serviceordre, kan det vises fra **Prosjekt** i den enkelte serviceordren eller i **Salgsordre**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="1310d-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="1310d-111">Vise et varebehov fra en serviceordre</span><span class="sxs-lookup"><span data-stu-id="1310d-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="1310d-112">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="1310d-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="1310d-113">Klikk **Fordeling**, og klikk deretter **Varebehov** for å åpne **Varebehov**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="1310d-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="1310d-114">Klikk kategorien **Prosjekt**, og merk deretter av for **Serviceordre** for å vise serviceordrene for varebehovet.</span><span class="sxs-lookup"><span data-stu-id="1310d-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="1310d-115">Slette serviceordrer med varebehov</span><span class="sxs-lookup"><span data-stu-id="1310d-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="1310d-116">Hvis et varebehov opprettes på en serviceordre, kan du ikke slette serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1310d-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="1310d-117">Du må slette varebehovet før du kan slette serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1310d-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="1310d-118">Klikk på **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="1310d-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="1310d-119">Klikk **Fordeling**, og klikk deretter **Varebehov** for å åpne **Varebehov**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="1310d-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="1310d-120">Dette skjemaet viser varebehovene som er opprettet på serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1310d-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="1310d-121">Velg varebehovslinjen som skal slettes, og klikk deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="1310d-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="1310d-122">– eller –</span><span class="sxs-lookup"><span data-stu-id="1310d-122">–or–</span></span>

1.  <span data-ttu-id="1310d-123">Klikk på **Prosjektstyring og regnskap** \> **Felles** \> **Prosjekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="1310d-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="1310d-124">Åpne prosjektet som har serviceordren der det er opprettet et varebehov.</span><span class="sxs-lookup"><span data-stu-id="1310d-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="1310d-125">I **Prosjekter**-skjemaet, i den høyre ruten, klikk **Varebehov**.</span><span class="sxs-lookup"><span data-stu-id="1310d-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="1310d-126">**Varebehov**-skjemaet åpnes og viser varebehovene som er tilknyttet det valgte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="1310d-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="1310d-127">Velg varebehovslinjen som skal slettes, og klikk deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="1310d-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1310d-128">Se også</span><span class="sxs-lookup"><span data-stu-id="1310d-128">See also</span></span>

<span data-ttu-id="1310d-129">[Varebehov (skjema)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="1310d-129">[Item requirements (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))</span></span>

