---
title: Dokumenter for budsjettplanleggingsjusteringer
description: "Justeringsdokumenter gir en narrativ beskrivelse for dem som ber om et budsjett for å forklare hvorfor et bestemt budsjett er nødvendig."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: eb616d6802e32d9dcbbeaf9c9866491c8a8d59c8
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="budget-planning-justification-documents"></a><span data-ttu-id="f6bc4-103">Dokumenter for budsjettplanleggingsjusteringer</span><span class="sxs-lookup"><span data-stu-id="f6bc4-103">Budget planning justification documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f6bc4-104">Justeringsdokumenter gir en narrativ beskrivelse for dem som ber om et budsjett for å forklare hvorfor et bestemt budsjett er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="f6bc4-105">En budsjettplanmal opprettes av budsjettansvarlig i Microsoft Word og tilordnes den gjeldende budsjettplanleggingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="f6bc4-106">Budsjetteierne kan deretter åpne malen og la data fylles ut automatisk i Word basert på budsjettforespørselen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="f6bc4-107">De kan deretter legge til ekstra tekst eller data før de lagrer og knytter det personlige justeringsdokumentet til budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="f6bc4-108">Definer Microsoft Dynamics Office-tillegget for Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="f6bc4-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="f6bc4-109">Åpne et nytt Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="f6bc4-110">Klikk **Sett inn** på båndet, og klikk **Butikk**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="f6bc4-111">Søk etter Microsoft Dynamics Office-tillegg, og klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="f6bc4-112">Klikk **Legg til serverinformasjon** i den høyre ruten i Word.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="f6bc4-113">Skriv inn eller lim inn URL-adressen for serveren, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="f6bc4-114">Definere justeringsmalen i Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="f6bc4-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="f6bc4-115">Klikk **Utforming** i Microsoft Dynamics Office-tillegget etter at du har logget på.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="f6bc4-116">For hodeinformasjon bruker du **Legg til felt**-knappen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="f6bc4-117">Velg datakilden for enhet for BudgetPlanJustification, og klikk **Neste**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="f6bc4-118">**Merk:** Denne enheten er nødvendig for alle justeringsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="f6bc4-119">Andre enheter kan brukes, men opplastingen tilbake til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition mislykkes hvis denne enheten ikke er inkludert.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="f6bc4-120">Legg til etikettene og verdiene for BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber i Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="f6bc4-121">**Merk:** Du kan bruke egendefinerte etiketter i stedet for standardetikettene, hvis nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="f6bc4-122">Klikk **Utført** for å fullføre topptekstdelen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="f6bc4-123">For linjenivådetaljer for budsjettplanbeløp klikker du **Legg til tabell**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="f6bc4-124">Velg igjen datakilden for enhet for BudgetPlanJustification, og klikk **Neste**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="f6bc4-125">Legg til felt for EffectiveDate, ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="f6bc4-126">**Merk:** Hvis det finnes kommentarer som kan legges til i individuelle budsjettplanlinjer, kan de legges til i tabellen her.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="f6bc4-127">Legg til eventuelle instruksjoner til sluttbrukeren, og angi nødvendig formatering eller stiler i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="f6bc4-128">Lagre dokumentet på den lokale datamaskinen, og lukk filen før du fortsetter.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="f6bc4-129">Konfigurere budsjettplanprosessen for å bruke justeringsmalen</span><span class="sxs-lookup"><span data-stu-id="f6bc4-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="f6bc4-130">I Finance and Operations går du til **Budsjettering** &gt; **Oppsett** &gt; **Budsjettplanlegging** &gt; **Maler for justeringsdokument**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="f6bc4-131">Klikk **Ny**, og bla til det nylig opprettede Microsoft Word-dokumentet.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="f6bc4-132">Angi et malvisningsnavn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-132">Enter a template display name and description.</span></span> <span data-ttu-id="f6bc4-133">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-133">Click **OK**.</span></span>
4.  <span data-ttu-id="f6bc4-134">Gå til **Budsjettering** &gt; **Oppsett** &gt; **Budsjett** **planlegging** &gt; **Budsjettplanleggingsprosess**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="f6bc4-135">Velg prosessen der justeringsmalen skal brukes, og klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="f6bc4-136">I feltet **Mal for justeringsdokument** velger og lagrer du den relevante malen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="f6bc4-137">Redigere og lagre tilpassede justeringsdokumenter</span><span class="sxs-lookup"><span data-stu-id="f6bc4-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="f6bc4-138">Opprett en ny budsjettplan eller åpne en eksisterende budsjettplan i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="f6bc4-139">På **Justering**-rullegardinmenyen velger du **Opprett ny justering**.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="f6bc4-140">Når du har fylt ut detaljene, velger du å laste opp det egendefinerte dokumentet fra **Justering**-rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="f6bc4-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>





