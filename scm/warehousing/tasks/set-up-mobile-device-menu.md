--- 
title: "Definere et menyelement for mobilenhet for å fullføre arbeid i en bestilling"
description: "Denne fremgangsmåten viser hvordan du definerer et Mobilenhet-menyelement."
author: BibiSp
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b80c258d6a779a8fc5bb6c846abd3af7e69d5e06
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="5acf7-103">Definere et menyelement for mobilenhet for å fullføre arbeid i en bestilling</span><span class="sxs-lookup"><span data-stu-id="5acf7-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5acf7-104">Denne fremgangsmåten viser hvordan du definerer et Mobilenhet-menyelement.</span><span class="sxs-lookup"><span data-stu-id="5acf7-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="5acf7-105">I dette eksemplet brukes menyelementet til å utføre arbeid av typen Bestilling.</span><span class="sxs-lookup"><span data-stu-id="5acf7-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="5acf7-106">Arbeidsklassen som er tilknyttet menyelementet, bestemmer hvilket arbeid som er gyldig.</span><span class="sxs-lookup"><span data-stu-id="5acf7-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="5acf7-107">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="5acf7-108">Denne fremgangsmåten utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="5acf7-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="5acf7-109">Opprette et menyelement for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="5acf7-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="5acf7-110">Gå til Menyelementer på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5acf7-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="5acf7-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5acf7-111">Click New.</span></span>
3. <span data-ttu-id="5acf7-112">Skriv inn en verdi i feltet Menyelementnavn.</span><span class="sxs-lookup"><span data-stu-id="5acf7-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="5acf7-113">Angi en unikt verdi.</span><span class="sxs-lookup"><span data-stu-id="5acf7-113">Enter a unique value.</span></span> <span data-ttu-id="5acf7-114">Du kan for eksempel skrive inn Bestillingsflytting.</span><span class="sxs-lookup"><span data-stu-id="5acf7-114">For example, you could type POMove.</span></span> <span data-ttu-id="5acf7-115">Husk verdien. Du trenger den senere.</span><span class="sxs-lookup"><span data-stu-id="5acf7-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="5acf7-116">Skriv inn en verdi i Tittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="5acf7-117">Dette er tittelen som skal vises på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5acf7-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="5acf7-118">Du kan for eksempel skrive inn Bestillingsflytting.</span><span class="sxs-lookup"><span data-stu-id="5acf7-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="5acf7-119">Velg Arbeid i feltet Modus.</span><span class="sxs-lookup"><span data-stu-id="5acf7-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="5acf7-120">Velg Ja i feltet Bruk eksisterende arbeid.</span><span class="sxs-lookup"><span data-stu-id="5acf7-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="5acf7-121">Dette menyelementet for mobilenheten brukes til å utføre eksisterende arbeid.</span><span class="sxs-lookup"><span data-stu-id="5acf7-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="5acf7-122">Derfor må du sette denne verdien til Ja.</span><span class="sxs-lookup"><span data-stu-id="5acf7-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="5acf7-123">Feltet Vis beholdningsstatus angir om beholdningsstatusen for i lagerbeholdningen vises for lagermedarbeideren på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5acf7-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="5acf7-124">Velg Systemgruppering i feltet Styrt av.</span><span class="sxs-lookup"><span data-stu-id="5acf7-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="5acf7-125">Når du velger noe i Styrt av-feltet, vises flere felt i Generelt-delen på denne siden.</span><span class="sxs-lookup"><span data-stu-id="5acf7-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="5acf7-126">Feltene som vises, avhenger av hva du valgte.</span><span class="sxs-lookup"><span data-stu-id="5acf7-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="5acf7-127">Når du velger Systemgruppering, legges to nye felt til.</span><span class="sxs-lookup"><span data-stu-id="5acf7-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="5acf7-128">Disse er beskrevet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="5acf7-128">These are explained below.</span></span>  
8. <span data-ttu-id="5acf7-129">Velg WorkPoolID i Systemgruppering-feltet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="5acf7-130">Når lagermedarbeidere åpne dette menyelementet, blir de bedt om å skanne en ID for arbeidsutvalg.</span><span class="sxs-lookup"><span data-stu-id="5acf7-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="5acf7-131">Alle arbeidsordrer med denne ID-en for arbeidsutvalg og åpne arbeidsordrelinjer med én av arbeidsklassene som er lagt til på dette menyelementet, overføres til brukeren.</span><span class="sxs-lookup"><span data-stu-id="5acf7-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="5acf7-132">Skriv inn en verdi i feltet Systemgrupperingsetikett.</span><span class="sxs-lookup"><span data-stu-id="5acf7-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="5acf7-133">Denne teksten vises for brukerne på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="5acf7-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="5acf7-134">Du kan for eksempel skrive inn Arbeidsutvalg.</span><span class="sxs-lookup"><span data-stu-id="5acf7-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="5acf7-135">Velg Ja i feltet Overstyr nummerskilt under plassering.</span><span class="sxs-lookup"><span data-stu-id="5acf7-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="5acf7-136">Dette alternativet lar lagermedarbeidere overstyre målnummerskiltet når varer legges på en lokasjon som er styrt av nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="5acf7-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="5acf7-137">I feltet Gruppe plassert velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="5acf7-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="5acf7-138">Hvis alle plasseringslinjene på arbeidsordren deler samme lokasjon, mottar brukeren en kombinert plasseringsinstruksjon for alle linjer.</span><span class="sxs-lookup"><span data-stu-id="5acf7-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="5acf7-139">ID for revisjonsmal: En revisjonsmal lar det angi at arbeidsprosessen for et menyelement skal avbrytes, slik at en annen operasjon kan utføres.</span><span class="sxs-lookup"><span data-stu-id="5acf7-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="5acf7-140">Hvis dette menyelementet for eksempel er for innkommende arbeid, kan revisjonsmalen kreve at arbeideren kontrollerer temperaturen.</span><span class="sxs-lookup"><span data-stu-id="5acf7-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="5acf7-141">Punktet der prosessen avbrytes, er angitt i revisjonsmalen og kan for eksempel være når arbeid er startet eller fullført, eller når statusen endres.</span><span class="sxs-lookup"><span data-stu-id="5acf7-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="5acf7-142">Utvid Arbeidsklasser-delen.</span><span class="sxs-lookup"><span data-stu-id="5acf7-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="5acf7-143">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5acf7-143">Click New.</span></span>
14. <span data-ttu-id="5acf7-144">Skriv inn Innkjøp i feltet Arbeidsklasse-ID.</span><span class="sxs-lookup"><span data-stu-id="5acf7-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="5acf7-145">Arbeidsutvalget begrenser arbeidet som menyelementet kan brukes til.</span><span class="sxs-lookup"><span data-stu-id="5acf7-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="5acf7-146">I dette tilfellet vil det bli brukt for åpne arbeidsordrelinjene som har kjøp ID-en for innkjøpsarbeidsklasse.</span><span class="sxs-lookup"><span data-stu-id="5acf7-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="5acf7-147">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5acf7-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="5acf7-148">Definere arbeidsbekreftelse</span><span class="sxs-lookup"><span data-stu-id="5acf7-148">Set up work confirmation</span></span>
1. <span data-ttu-id="5acf7-149">Klikk Arbeidsbekreftelsesoppsett.</span><span class="sxs-lookup"><span data-stu-id="5acf7-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="5acf7-150">Velg Plukk i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="5acf7-151">Merk av for Automatisk bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="5acf7-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="5acf7-152">Arbeidsinstruksjonen med arbeidstypen Plukk bekreftes automatisk.</span><span class="sxs-lookup"><span data-stu-id="5acf7-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="5acf7-153">Denne instruksjonen presenteres ikke for brukeren.</span><span class="sxs-lookup"><span data-stu-id="5acf7-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="5acf7-154">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5acf7-154">Click New.</span></span>
5. <span data-ttu-id="5acf7-155">Velg Plasser i Arbeidstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="5acf7-156">Merk av for Lokasjonsbekreftelse.</span><span class="sxs-lookup"><span data-stu-id="5acf7-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="5acf7-157">Lagermedarbeideren vil bli bedt om å utføre en bekreftelsesskanning av lokasjonen når varen plasseres.</span><span class="sxs-lookup"><span data-stu-id="5acf7-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="5acf7-158">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5acf7-158">Click Save.</span></span>
8. <span data-ttu-id="5acf7-159">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5acf7-159">Close the page.</span></span>
9. <span data-ttu-id="5acf7-160">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5acf7-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="5acf7-161">Legge til menyelementet på en meny for mobilenhet</span><span class="sxs-lookup"><span data-stu-id="5acf7-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="5acf7-162">Gå til menyen Mobilenhet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="5acf7-163">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="5acf7-163">Click Edit.</span></span>
3. <span data-ttu-id="5acf7-164">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="5acf7-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5acf7-165">Du kan for eksempel filtrere på Navn-feltet med verdien innkommende.</span><span class="sxs-lookup"><span data-stu-id="5acf7-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="5acf7-166">Du vil finne menyen for inngående menyelementer.</span><span class="sxs-lookup"><span data-stu-id="5acf7-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="5acf7-167">I USMF kalles dette Inngående.</span><span class="sxs-lookup"><span data-stu-id="5acf7-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="5acf7-168">Velg en verdi i treet.</span><span class="sxs-lookup"><span data-stu-id="5acf7-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="5acf7-169">Klikk på pilen som peker mot høyre.</span><span class="sxs-lookup"><span data-stu-id="5acf7-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="5acf7-170">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="5acf7-170">Click Save.</span></span>
7. <span data-ttu-id="5acf7-171">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5acf7-171">Close the page.</span></span>


