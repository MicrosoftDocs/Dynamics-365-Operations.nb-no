---
title: Vise og eksportere feltbeskrivelser
description: "Denne artikkelen beskriver hvordan du viser beskrivelser og hvordan du bruker siden Feltbeskrivelser til å eksportere beskrivelser."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6426f208a51ffbf72c6faa8cb281aba2984052d7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="189a3-103">Vise og eksportere feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="189a3-103">View and export field descriptions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="189a3-104">Denne artikkelen beskriver hvordan du viser beskrivelser og hvordan du bruker siden Feltbeskrivelser til å eksportere beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="189a3-105">Microsoft Dynamics 365 for Finance and Operations har beskrivelsene for noen av de mer kompliserte feltene.</span><span class="sxs-lookup"><span data-stu-id="189a3-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="189a3-106">Disse beskrivelsene vises når du holder pekeren over et felt.</span><span class="sxs-lookup"><span data-stu-id="189a3-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="189a3-107">Du kan også vise og eksportere beskrivelser på siden **Feltbeskrivelser**.</span><span class="sxs-lookup"><span data-stu-id="189a3-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="189a3-108">Ikke alle sider har feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="189a3-109">Vi vil bare gi beskrivelser for de mer komplekse feltene, og ikke der bruken av feltet er åpenbart.</span><span class="sxs-lookup"><span data-stu-id="189a3-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="189a3-110">Derfor ha noen sider ikke noen feltbeskrivelser, noen sider har noen få beskrivelser og noen av de mer komplekse sidene, for eksempel mange av parametersidene, har mange beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="189a3-111">Hvis du har tilgang til utviklingsmiljøet i Finance and Operations, kan du legge til nye feltbeskrivelser og tilpasse eksisterende beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="189a3-112">Du kan for eksempel legge til firmaspesifikk informasjon i en feltbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="189a3-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="189a3-113">Hvis du vil ha mer informasjon, kan du se [hjelpen for å tilpasse felt](../../dev-itpro/user-interface/customize-field-help.md).</span><span class="sxs-lookup"><span data-stu-id="189a3-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="189a3-114">Se feltbeskrivelsene i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="189a3-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="189a3-115">Du kan vise feltbeskrivelser ved å holde pekeren over et felt.</span><span class="sxs-lookup"><span data-stu-id="189a3-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="189a3-116">Hvis ingen beskrivelse er tilgjengelig, kan du se navnet på feltet når du holder pekeren over feltet.</span><span class="sxs-lookup"><span data-stu-id="189a3-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="189a3-117">(Obs! I Dynamics AX 7.0 (februar 2016) kan feltbeskrivelser bare vises på siden **Feltbeskrivelser**.) Illustrasjon nedenfor viser feltbeskrivelsen som vises når du holder pekeren over feltet **Lås varer under opptelling**.</span><span class="sxs-lookup"><span data-stu-id="189a3-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="189a3-118">[![Eksempel på en feltbeskrivelse](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="189a3-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="189a3-119">Bruk siden Feltbeskrivelser til å vise og eksportere felthjelp</span><span class="sxs-lookup"><span data-stu-id="189a3-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="189a3-120">Siden **Feltbeskrivelser** lar deg vise og eksportere feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="189a3-121">Du kan se feltbeskrivelsene som er tilgjengelige for én side om gangen.</span><span class="sxs-lookup"><span data-stu-id="189a3-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="189a3-122">Vise beskrivelsene for en side</span><span class="sxs-lookup"><span data-stu-id="189a3-122">View the descriptions for a page</span></span>

<span data-ttu-id="189a3-123">Følg fremgangsmåten nedenfor for å vise beskrivelsene for en side.</span><span class="sxs-lookup"><span data-stu-id="189a3-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="189a3-124">Skriv inn navn på siden i feltet **Velg en side**.</span><span class="sxs-lookup"><span data-stu-id="189a3-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="189a3-125">Klikk eventuelt pilen for å åpne en liste over alle sidene, og bla deretter gjennom eller filtrer listen.</span><span class="sxs-lookup"><span data-stu-id="189a3-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="189a3-126">Du kan bruke navnet på siden som vises i brukergrensesnittet (for eksempel **Kunder**), eller kodenavnet (navn på applikasjonsobjekttre) som er tilgjengelig når du høyreklikker på en side (for eksempel **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="189a3-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="189a3-127">Hvis du vil ha informasjon om de forskjellige måtene å filtrere listen over sider, kan du se delen Søke etter en side senere i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="189a3-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="189a3-128">Hvis du setter alternativet **Inkluder felt uten beskrivelse** til **Ja**, vises alle feltene på siden selv om de ikke har en feltbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="189a3-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="189a3-129">Eksportere beskrivelsene for en side</span><span class="sxs-lookup"><span data-stu-id="189a3-129">Export the descriptions for a page</span></span>

<span data-ttu-id="189a3-130">Følg fremgangsmåten nedenfor for å eksportere beskrivelsene for en side.</span><span class="sxs-lookup"><span data-stu-id="189a3-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="189a3-131">Velg en siden i feltet **Velg en side**.</span><span class="sxs-lookup"><span data-stu-id="189a3-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="189a3-132">Klikk **Åpne i Microsoft Office** i øvre høyre hjørne, og klikk deretter **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="189a3-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="189a3-133">Søke etter en side</span><span class="sxs-lookup"><span data-stu-id="189a3-133">Searching for a page</span></span>

<span data-ttu-id="189a3-134">Det finnes flere måter å søke etter en side på i feltet **Velg en side**.</span><span class="sxs-lookup"><span data-stu-id="189a3-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="189a3-135">I mange tilfeller må du klikke pilen i feltet **Velg en side** for å åpne rullegardinlisten og deretter velge fra en filtrert liste over sider.</span><span class="sxs-lookup"><span data-stu-id="189a3-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="189a3-136">Skriv inn deler av navnet, og åpne deretter rullegardinlisten for å velge fra en filtrert liste over sider.</span><span class="sxs-lookup"><span data-stu-id="189a3-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="189a3-137">Åpne rullegardinlisten, og klikk deretter **Sidenavn**-toppteksten øverst i listen, eller toppteksten **Navn på applikasjonsobjekttre for side**.</span><span class="sxs-lookup"><span data-stu-id="189a3-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="189a3-138">Det vises en dialogboks der du kan bruke alternativer for avansert filtrering, for eksempel **Sidenavn begynner med**.</span><span class="sxs-lookup"><span data-stu-id="189a3-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="189a3-139">Skriv inn det fullstendige navnet på siden.</span><span class="sxs-lookup"><span data-stu-id="189a3-139">Type the full name of the page.</span></span> <span data-ttu-id="189a3-140">Når du bruker dette alternativet, er det best å åpne rullegardinlisten og se hva som ellers er i den, selv om feltbeskrivelser vises.</span><span class="sxs-lookup"><span data-stu-id="189a3-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="189a3-141">Hvis det er ett nøyaktig treff på navnet, vises feltbeskrivelsene for denne siden.</span><span class="sxs-lookup"><span data-stu-id="189a3-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="189a3-142">Hvis det finnes mer enn ett treff, vises ingen beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="189a3-143">Du må åpne rullegardinlisten, og velg siden du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="189a3-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="189a3-144">Hvis navnet du skrev inn er en del av navnet på en annen side, vises beskrivelsene for siden.</span><span class="sxs-lookup"><span data-stu-id="189a3-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="189a3-145">Hvis du imidlertid åpner rullegardinlisten, vises flere sider som inneholder dette navnet.</span><span class="sxs-lookup"><span data-stu-id="189a3-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="189a3-146">Ingen beskrivelser vises for eksempel når du skriver inn **Opptelling** i feltet ****Velg en side****.</span><span class="sxs-lookup"><span data-stu-id="189a3-146">For example, no descriptions are shown when you type **Counting** in the ****Select a page**** field.</span></span> <span data-ttu-id="189a3-147">Du åpner rullegardinlisten og ser at det er to sider med navnet **Opptelling**, i tillegg til flere sider som inneholder ordet Opptelling i navnet.</span><span class="sxs-lookup"><span data-stu-id="189a3-147">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="189a3-148">Hvis du velger siden som har **InventJournalCount** som navn på applikasjonsobjekttre, vises feltbeskrivelsene for denne siden.</span><span class="sxs-lookup"><span data-stu-id="189a3-148">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="189a3-149">Hvis du imidlertid åpner rullegardinlisten på nytt, ser du at listen nå inneholder alle sider som har "InventJournalCount"» som en del av navnet på applikasjonsobjekttreet.</span><span class="sxs-lookup"><span data-stu-id="189a3-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="189a3-150">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="189a3-150">Troubleshooting</span></span>
<span data-ttu-id="189a3-151">Dette avsnittet inneholder informasjon om hvordan du feilsøker problemer som kan oppstå når du bruker feltbeskrivelser.</span><span class="sxs-lookup"><span data-stu-id="189a3-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="189a3-152">Det er en feltbeskrivelse jeg ikke finner</span><span class="sxs-lookup"><span data-stu-id="189a3-152">I can't find a field description</span></span>

<span data-ttu-id="189a3-153">Vi holder på med å legge til beskrivelser for de mer komplekse feltene.</span><span class="sxs-lookup"><span data-stu-id="189a3-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="189a3-154">Hvis du trenger hjelp med et bestemt felt, må du gjerne gi oss tilbakemelding ved å legge til en kommentar for dette emnet.</span><span class="sxs-lookup"><span data-stu-id="189a3-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="189a3-155">Feltbeskrivelsen er ikke nyttig</span><span class="sxs-lookup"><span data-stu-id="189a3-155">The field description isn't helpful</span></span>

<span data-ttu-id="189a3-156">Gi oss tilbakemelding ved å legge til en kommentar for dette emnet.</span><span class="sxs-lookup"><span data-stu-id="189a3-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="189a3-157">Hvis du kan, beskriver du den ekstra informasjonen du trenger.</span><span class="sxs-lookup"><span data-stu-id="189a3-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="189a3-158">Jeg finner ikke et felt på siden Feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="189a3-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="189a3-159">Hvis du vil vise alle feltene på en side, kan du angi **Ja** for alternativet **Inkluder felt uten beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="189a3-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="189a3-160">Klikk feltet **Velg en side** for å kontrollere at du har valgt den riktige siden.</span><span class="sxs-lookup"><span data-stu-id="189a3-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="189a3-161">Hvis navnet du skrev inn er en del av et annet feltnavn, har du kanskje valgt siden som har det lengste navnet.</span><span class="sxs-lookup"><span data-stu-id="189a3-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="189a3-162">Jeg finner ikke en side på siden Feltbeskrivelser</span><span class="sxs-lookup"><span data-stu-id="189a3-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="189a3-163">Hvis du vil ha informasjon om de forskjellige måtene å finne sider, kan du se avsnittet Søke etter sider tidligere i denne artikkelen.</span><span class="sxs-lookup"><span data-stu-id="189a3-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="189a3-164">Hvis du har skrevet inn det nøyaktige navnet på siden, kan det hende at feltbeskrivelsene ikke vises hvis det finnes flere sider med samme navn.</span><span class="sxs-lookup"><span data-stu-id="189a3-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="189a3-165">Klikk pilen i feltet **Velg en side** for å åpne en filtrert liste over sidene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="189a3-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="see-also"></a><span data-ttu-id="189a3-166">Se også</span><span class="sxs-lookup"><span data-stu-id="189a3-166">See also</span></span>
--------

[<span data-ttu-id="189a3-167">Hjelp for å tilpasse felt</span><span class="sxs-lookup"><span data-stu-id="189a3-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





