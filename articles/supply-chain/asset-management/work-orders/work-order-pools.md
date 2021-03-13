---
title: Arbeidsordresamlinger
description: Dette emnet beskriver hvordan du arbeider med arbeidsordresamlinger i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afea5b8d0f958c3ab53d6cef8c9a0e9030d7c67b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017523"
---
# <a name="work-order-pools"></a><span data-ttu-id="23061-103">Arbeidsordresamlinger</span><span class="sxs-lookup"><span data-stu-id="23061-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="23061-104">Du kan bruke arbeidsordresamlinger til å gruppere arbeidsordrer som har noe til felles.</span><span class="sxs-lookup"><span data-stu-id="23061-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="23061-105">Her er noen eksempler på ting du kan opprette arbeidsordresamlinger for:</span><span class="sxs-lookup"><span data-stu-id="23061-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="23061-106">Arbeidslag, for eksempel vedlikeholdslag A eller vedlikeholdslag B</span><span class="sxs-lookup"><span data-stu-id="23061-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="23061-107">Fagkompetanse, for eksempel elektrikere og rørleggere</span><span class="sxs-lookup"><span data-stu-id="23061-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="23061-108">Fysiske lokasjoner</span><span class="sxs-lookup"><span data-stu-id="23061-108">Physical locations</span></span>  

- <span data-ttu-id="23061-109">Tidsplaner, for eksempel uker eller andre perioder</span><span class="sxs-lookup"><span data-stu-id="23061-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="23061-110">Du kan du plassere én arbeidsordre i flere arbeidsordresamlinger, etter behov.</span><span class="sxs-lookup"><span data-stu-id="23061-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="23061-111">Opprette en arbeidsordresamling</span><span class="sxs-lookup"><span data-stu-id="23061-111">Create a work order pool</span></span>

<span data-ttu-id="23061-112">På listesiden **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger** kan du få en oversikt over arbeidsordresamlingene og opprette nye samlinger.</span><span class="sxs-lookup"><span data-stu-id="23061-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="23061-113">Velg **Aktivastyring** > **Felles** > **Arbeidsordresamlinger** > **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**.</span><span class="sxs-lookup"><span data-stu-id="23061-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="23061-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="23061-114">Select **New**.</span></span>

3. <span data-ttu-id="23061-115">Angi en ID for arbeidsordresamlingen i feltet **Pulje**.</span><span class="sxs-lookup"><span data-stu-id="23061-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="23061-116">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="23061-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="23061-117">Sett alternativet **Aktiv** til **Ja** for å angi at arbeidsordresamlingen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="23061-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="23061-118">Sett alternativet **Slett arbeidsordrerelasjoner** til **Ja** hvis arbeidsordrer automatisk skal fjernes fra arbeidsordresamlingen.</span><span class="sxs-lookup"><span data-stu-id="23061-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="23061-119">I feltet **Slett livssyklustilstand** velger du livssyklustilstanden for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="23061-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="23061-120">For eksempel kan livssyklustilstanden for arbeidsordre for å fullføre en arbeidsordre settes til å slette relasjoner til arbeidsordresamlinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="23061-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="23061-121">Du kan begynne å legge til arbeidsordrer i arbeideordresamlingen med én gang.</span><span class="sxs-lookup"><span data-stu-id="23061-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="23061-122">Velg **Legg til linje** på hurtigfanen **Arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="23061-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="23061-123">Velg en arbeidsordre i feltet **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="23061-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="23061-124">De tilknyttede feltene oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="23061-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="23061-125">Gjenta trinn 8 til og med 9 hvis du vil legge til flere arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="23061-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="23061-126">Hvis arbeidsordrene du la til, skal utføres i en bestemt rekkefølge, kan du angi tallene **1**, **2**, **3** og så videre i feltet **Sorteringsrekkefølge** for å angi rekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="23061-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="23061-127">Hvis du vil vise en liste over alle arbeidsordrene som er inkludert i arbeidsordren, går du til handlingsruten, fanen **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Arbeidsordrer** for å åpne listesiden **Alle arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="23061-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="23061-128">Hvis du vil beregne og vise kapasitetsbelastningen for vedlikeholdsplanen, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer, går du til handlingsruten, fanen **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Kapasitetsbelastning** for å åpne dialogboksen **Beregn kapasitetsbelastning**.</span><span class="sxs-lookup"><span data-stu-id="23061-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="23061-129">Hvis du vil beregne og vise prognoser for elementene (reservedeler og andre nødvendige varer) som er relatert til vedlikeholdsplanen, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer, går du til handlingsruten, fanen **Arbeidsordresamling**, gruppen **Vis arbeidsordresamlingsrelatert** og velger **Vareprognose** for å åpne dialogboksen **Beregn vareprognose**.</span><span class="sxs-lookup"><span data-stu-id="23061-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="23061-130">Hvis du vil vise en liste over innkjøpsrekvisisjoner som er relatert til arbeidsordrene i arbeidsordresamlingen, går du til handlingsruten, fanen **Arbeidsordresamling**, gruppen **Innkjøp** og velger **Innkjøpsrekvisisjon for arbeidsordre** for å åpne listesiden **Innkjøpsrekvisisjon for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="23061-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="23061-131">Hvis du vil vise en liste over bestillinger som er relatert til arbeidsordrene i arbeidsordresamlingen, går du til handlingsruten, fanen **Arbeidsordresamling**, gruppen **Innkjøp** og velger **Innkjøp for arbeidsordre** for å åpne listesiden **Innkjøp for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="23061-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="23061-132">Når en arbeidsordresamling ikke lenger er relevant for arbeidsplanleggingen, setter du alternativet **Aktiv** for denne samlingen til **Nei** i listevisningen på siden **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="23061-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="23061-133">Hvis du vil slette alle arbeidsordrelinjer, setter du alternativet **Slett arbeidsordrerelasjoner** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="23061-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="23061-134">Dette alternativet er nyttig hvis du for eksempel vil opprette et tomt utvalg som du kan bruke senere for andre arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="23061-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="23061-135">Når du er klar til å bruke arbeidsordresamlingen til å opprette nye arbeidsordrerelasjoner senere, må du huske å sette **Slett arbeidsordrerelasjoner** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="23061-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="23061-136">Illustrasjonen nedenfor viser et eksempel på listesiden **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="23061-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Figur 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="23061-138">Legge til en arbeidsordre i en arbeidsordresamling</span><span class="sxs-lookup"><span data-stu-id="23061-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="23061-139">Som beskrevet i forrige del, kan du legge til arbeidsordrer i en arbeidsordresamling når du oppretter samlingen.</span><span class="sxs-lookup"><span data-stu-id="23061-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="23061-140">Du kan også legge til arbeidsordrer i en arbeidsordresamling på listesiden **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="23061-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="23061-141">Velg arbeidsordren, og deretter går du til handlingsruten, fanen **Arbeidsordre**, gruppen **Vedlikehold** og velger **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="23061-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="23061-142">Velg arbeidsordren i listen, og klikk på **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="23061-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="23061-143">I dialogboksen **Vedlikehold arbeidsordresamling** i feltet **Legg til/fjern** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="23061-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="23061-144">Velg arbeidsordresamlingen i **Pulje**-feltet.</span><span class="sxs-lookup"><span data-stu-id="23061-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="23061-145">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="23061-145">Select **OK**.</span></span>

6. <span data-ttu-id="23061-146">Hvis du vil plassere arbeidsordren du la til, i en bestemt rekkefølge i arbeidsordreutvalget, går du til listesiden **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**, velger samlingen og deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="23061-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="23061-147">Deretter, på siden **Arbeidsordresamling** i hurtigfanen **Arbeidsordrer**, bruker du feltet **Sorteringsrekkefølge** til å justere sorteringsrekkefølgen for arbeidsordrene som er inkludert i samlingen.</span><span class="sxs-lookup"><span data-stu-id="23061-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="23061-148">Hvis du vil fjerne en arbeidsordre fra en arbeidsordresamling, gjentar du disse trinnene, men velger **Fjern** i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="23061-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

