---
title: Opprette arbeidsordrer fra vedlikeholdsforespørsler
description: Dette emnet forklarer hvordan du oppretter en arbeidsordre fra en vedlikeholdsforespørsel i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c42f259a57675c3dbac829d6d671e91982ef9011
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571697"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="82cf7-103">Opprette arbeidsordrer fra vedlikeholdsforespørsler</span><span class="sxs-lookup"><span data-stu-id="82cf7-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="82cf7-104">Når du har opprettet vedlikeholdsforespørsler, kan du enkelt konvertere dem til arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="82cf7-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="82cf7-105">Dette emnet beskriver den raskeste måten å arbeide med vedlikeholdsforespørsler på, oppdatere flere vedlikeholdsforespørsler samtidig og deretter opprette en arbeidsordre for flere vedlikeholdsforespørsler samtidig.</span><span class="sxs-lookup"><span data-stu-id="82cf7-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="82cf7-106">På siden **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted** kan du også arbeide med én vedlikeholdsforespørsel om gangen og konvertere en vedlikeholdssforespørsel til en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="82cf7-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="82cf7-107">Hver vedlikeholdsforespørsel kan være relatert til bare én arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="82cf7-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="82cf7-108">Flere vedlikeholdsforespørsler kan imidlertid inkluderes i én arbeidsordre, selv om vedlikeholdsforespørslene har forskjellige aktiva.</span><span class="sxs-lookup"><span data-stu-id="82cf7-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="82cf7-109">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="82cf7-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="82cf7-110">Før du kan opprette en arbeidsordre fra vedlikeholdsforespørsler, må du minst velge en vedlikeholdsjobbtype for vedlikeholdsforespørslene, og også en type variant og fag for vedlikeholdsjobber, hvis denne informasjonen er relevant.</span><span class="sxs-lookup"><span data-stu-id="82cf7-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="82cf7-111">I rutenettvisningen kan du enkelt oppdatere informasjon for en vedlikeholdsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="82cf7-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="82cf7-112">Når du er klar til å opprette en arbeidsordre, velger du vedlikeholdsforespørslene du vil inkludere i den.</span><span class="sxs-lookup"><span data-stu-id="82cf7-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="82cf7-113">Hvis du velger flere vedlikeholdsforespørsler for å konvertere til en arbeidsordre, må både feltet **Aktiva** og **Vedlikeholdsjobbtype** være angitt før du oppretter arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="82cf7-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="82cf7-114">Hvis du velger én vedlikeholdsforespørsel for å konvertere til en arbeidsordre, må bare feltet **Aktiva** være angitt før du oppretter arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="82cf7-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="82cf7-115">Når du oppretter arbeidsordren, kan du imidlertid velge en vedlikeholdsjobbtype (og en tilknyttet variant og fag for vedlikeholdsjobbtypen hvis denne informasjonen er relevant), i dialogboksen **Opprett Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="82cf7-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="82cf7-116">Velg **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="82cf7-116">Select **Work order**.</span></span>
5. <span data-ttu-id="82cf7-117">Angi feltene i dialogboksen **Opprett arbeidsordre**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="82cf7-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="82cf7-118">En meldingslinje kan varsle deg om at det er opprettet en ny arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="82cf7-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="82cf7-119">I tillegg når du oppretter en arbeidsordre som er basert på en vedlikeholdsforespørsel, hvis aktivaet som er knyttet til vedlikeholdsforespørselen er inkludert i en garantiavtale, varsler en meldingslinje deg om garantiavtalen.</span><span class="sxs-lookup"><span data-stu-id="82cf7-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="82cf7-120">Velg **Aktivastyring** \> **Felles** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, og åpne den nye arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="82cf7-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Åpne ny arbeidsordre](media/05-manage-maintenance-requests.png)

