---
title: Arbeidsordresamlinger
description: Dette emnet beskriver hvordan du arbeider med arbeidsordresamlinger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875820"
---
# <a name="work-order-pools"></a><span data-ttu-id="0a6c1-103">Arbeidsordresamlinger</span><span class="sxs-lookup"><span data-stu-id="0a6c1-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="0a6c1-104">Du kan bruke arbeidsordresamlinger til å gruppere arbeidsordrer som har noe til felles.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="0a6c1-105">Du kan for eksempel opprette arbeidsordresamlinger for</span><span class="sxs-lookup"><span data-stu-id="0a6c1-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="0a6c1-106">arbeidslag, for eksempel vedlikeholdslag A, vedlikeholdslag B</span><span class="sxs-lookup"><span data-stu-id="0a6c1-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="0a6c1-107">fagkompetanse, for eksempel elektrikere og rørleggere</span><span class="sxs-lookup"><span data-stu-id="0a6c1-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="0a6c1-108">fysiske lokasjoner</span><span class="sxs-lookup"><span data-stu-id="0a6c1-108">physical locations</span></span>  

- <span data-ttu-id="0a6c1-109">tidsplaner, for eksempel uker eller andre perioder</span><span class="sxs-lookup"><span data-stu-id="0a6c1-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="0a6c1-110">Hvis det er nødvendig, kan én arbeidsordre plasseres i mange arbeidsordresamlinger.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="0a6c1-111">Opprette arbeidsordresamling</span><span class="sxs-lookup"><span data-stu-id="0a6c1-111">Create work order pool</span></span>

<span data-ttu-id="0a6c1-112">I **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger** kan du få en oversikt over arbeidsordresamlingene og opprette nye samlinger.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="0a6c1-113">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordresamlinger** > **Alle arbeidsordresamlinger** eller **Aktive arbeidsordresamlinger**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="0a6c1-114">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-114">Click **New**.</span></span>

3. <span data-ttu-id="0a6c1-115">Sett inn en ID for arbeidsordresamling i **Samling**-feltet og et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="0a6c1-116">Velg Ja på **Aktiv**-veksleknappen for å angi at arbeidsordresamlingen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="0a6c1-117">Velg Ja på veksleknappen **Slett arbeidsordrerelasjoner** hvis du vil at arbeidsordrer skal fjernes automatisk fra arbeidsordresamlingen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="0a6c1-118">I feltet **Slett livssyklustilstand** velger du livssyklustilstanden for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="0a6c1-119">For eksempel kan livssyklustilstanden for arbeidsordre for å fullføre en arbeidsordre settes til å slette relasjoner til arbeidsordresamlinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="0a6c1-120">Du kan begynne å legge til arbeidsordrer i arbeideordresamlingen med én gang.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="0a6c1-121">Klikk på **Legg til linje** på hurtigfanen **Arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="0a6c1-122">Velg en arbeidsordre i feltet **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="0a6c1-123">De tilknyttede feltene oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="0a6c1-124">Gjenta trinn 7-8 hvis du vil legge til flere arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="0a6c1-125">I feltet **Sorteringsrekkefølge** kan du angi om arbeidsordrene skal utføres i en bestemt rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="0a6c1-126">Sett inn tallene 1, 2, 3 og så videre for å angi en bestemt rekkefølge for de valgte arbeidsordrene.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="0a6c1-127">Klikk på **Arbeidsordrer**-knappen for å vise en liste over alle arbeidsordrene som er inkludert i arbeidsordresamlingen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="0a6c1-128">Klikk på knappen **Kapasitetsbelastning** for å åpne **Kapasitetsbelastning** for å beregne og vise kapasitetsbelastning for vedlikeholdsplan, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="0a6c1-129">Klikk på knappen **Vareprognose** for å åpne **Vareprognose** for å beregne og vise prognoser for varer (reservedeler og andre nødvendige varer) knyttet til vedlikeholdsplan, ikke-planlagte arbeidsordrer og planlagte arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="0a6c1-130">Klikk på knappen **Innkjøpsrekvisisjon for arbeidsordre** for å åpne listen **Innkjøpsrekvisisjon for arbeidsordre** for å vise en liste over innkjøpsrekvisisjoner knyttet til arbeidsordrene i arbeidsordresamlingen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="0a6c1-131">Klikk på knappen **Arbeidsordrekjøp** for å åpne listen **Arbeidsordrekjøp** for å vise en liste over bestillinger knyttet til arbeidsordrene i arbeidsordresamlingen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="0a6c1-132">Når en arbeidsordresamling ikke lenger er relevant for arbeidsplanleggingen, setter du **Aktiv**-avmerkingsboksen for denne samlingen til Nei i listevisningen **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="0a6c1-133">Merk av for **Slett arbeidsordrerelasjoner** hvis du vil slette alle arbeidsordrelinjene, for eksempel for å opprette en tom samling som du kan bruke senere i andre arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="0a6c1-134">Husk å fjerne merket for **Slett arbeidsordrerelasjoner** hvis du vil bruke arbeidsordresamlingen til å opprette nye arbeidsordrerelasjoner senere.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Figur 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="0a6c1-136">Legge til arbeidsordre i en arbeidsordresamling</span><span class="sxs-lookup"><span data-stu-id="0a6c1-136">Add work order to a work order pool</span></span>

<span data-ttu-id="0a6c1-137">Som beskrevet i delen ovenfor, kan du legge til arbeidsordrer i en arbeidsordresamling når du oppretter samlingen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="0a6c1-138">Du kan også legge til en arbeidsordre i en arbeidsordresamling fra **Alle arbeidsordrer**-listen.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="0a6c1-139">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0a6c1-140">Velg arbeidsordren i listen, og klikk på **Arbeidsordresamling**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="0a6c1-141">Velg Legg til i **Legg til / fjern**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="0a6c1-142">Velg arbeidsordresamlingen i **Samling**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="0a6c1-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-143">Click **OK**.</span></span>

6. <span data-ttu-id="0a6c1-144">Når du har lagt til en arbeidsordre i en arbeidsordresamling, og du vil plassere arbeidsordren i en bestemt rekkefølge i puljen: Åpne en av listesidene for arbeidsordresamlinger, velg samlingen, klikk på **Rediger**, og juster sorteringsrekkefølgen for arbeidsordrene som er inkludert i samlingen, i **Arbeidsordresamling**-skjemaet > **Arbeidsordrer**-hurtigfanen > **Sorteringsrekkefølge**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="0a6c1-145">Hvis du vil fjerne den valgte arbeidsordren fra en arbeidsordresamling, velger du Fjern i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="0a6c1-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

