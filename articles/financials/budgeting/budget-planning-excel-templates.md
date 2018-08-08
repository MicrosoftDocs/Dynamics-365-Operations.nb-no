---
title: Maler for budsjettplanlegging for Excel
description: Dette emnet beskriver hvordan du oppretter Microsoft Excel-maler som kan brukes med budsjettplaner.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 079aa6bb4be020fc050b81c400050ed23d48f6ca
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="63387-103">Maler for budsjettplanlegging for Excel</span><span class="sxs-lookup"><span data-stu-id="63387-103">Budget planning templates for Excel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63387-104">Dette emnet beskriver hvordan du oppretter Microsoft Excel-maler som kan brukes med budsjettplaner.</span><span class="sxs-lookup"><span data-stu-id="63387-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="63387-105">Dette emnet viser hvordan du oppretter Excel-maler som skal brukes med budsjettplaner ved hjelp av standard demodatasettet og Admin-brukerpålogging.</span><span class="sxs-lookup"><span data-stu-id="63387-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="63387-106">Hvis du vil ha mer informasjon om budsjettplanlegging, kan du se [Oversikt over budsjettplanlegging.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="63387-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="63387-107">Du kan også følge opplæringen [Budsjettplanlegging 101](budget-plan.md) for å lære grunnleggende modulkonfigurasjon og -bruksprinsipper.</span><span class="sxs-lookup"><span data-stu-id="63387-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="63387-108">Generer et regneark ved hjelp av oppsett for budsjettplandokument</span><span class="sxs-lookup"><span data-stu-id="63387-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="63387-109">Budsjettplandokumenter kan vises og redigeres ved hjelp av ett eller flere oppsett.</span><span class="sxs-lookup"><span data-stu-id="63387-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="63387-110">Hvert oppsett kan ha en tilknyttet dokumentmal for budsjettplan for å vise og redigere budsjettplandataene i et Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="63387-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="63387-111">I dette emnet genereres en dokumentmal for budsjettplan ved hjelp av en eksisterende oppsettkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="63387-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="63387-112">Åpne **listen over budsjettplaner** (**Budsjettering** &gt; **Budsjettplaner**).</span><span class="sxs-lookup"><span data-stu-id="63387-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="63387-113">Klikk **Ny** for å opprette et nytt budsjettplandokument.</span><span class="sxs-lookup"><span data-stu-id="63387-113">Click **New** to create a new budget plan document.</span></span> 

   <span data-ttu-id="63387-114">[![Liste over budsjettplaner](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="63387-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="63387-115">Bruk alternativet **Legg til linje** for å legge til linjer.</span><span class="sxs-lookup"><span data-stu-id="63387-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="63387-116">Klikk **Oppsett** for å vise oppsettkonfigurasjonen for budsjettplandokument.</span><span class="sxs-lookup"><span data-stu-id="63387-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

   <span data-ttu-id="63387-117">[![Legg til budsjettplaner](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="63387-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="63387-118">Du kan gå gjennom oppsettkonfigurasjonen og justere den etter behov.</span><span class="sxs-lookup"><span data-stu-id="63387-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="63387-119">Gå til **Mal** &gt; **Generer** for å opprette en Excel-fil for dette oppsettet.</span><span class="sxs-lookup"><span data-stu-id="63387-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="63387-120">Etter at malen er generert, går du til **Mal** &gt; **Vis** for å åpne og se gjennom dokumentmalen for budsjettplan.</span><span class="sxs-lookup"><span data-stu-id="63387-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="63387-121">Du kan lagre Excel-filen på den lokale stasjonen.</span><span class="sxs-lookup"><span data-stu-id="63387-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="63387-122">[![Lagre som](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="63387-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="63387-123">Oppsettet av budsjettplandokumentet kan ikke redigeres etter at det er knyttet til en Excel-mal.</span><span class="sxs-lookup"><span data-stu-id="63387-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="63387-124">Hvis du vil endre oppsettet, sletter du den tilknyttede Excel-malfilen og genererer den på nytt.</span><span class="sxs-lookup"><span data-stu-id="63387-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="63387-125">Dette er nødvendig for å holde feltene i oppsettet og regnearket synkronisert.</span><span class="sxs-lookup"><span data-stu-id="63387-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="63387-126">Excel-malen inneholder alle elementene fra oppsettet for budsjettplandokument, der kolonnen **Tilgjengelig i regneark** er satt til sann.</span><span class="sxs-lookup"><span data-stu-id="63387-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="63387-127">Overlappende elementer er ikke tillatt i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="63387-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="63387-128">Hvis oppsettet for eksempel inneholder kolonnene Forespørsel Q1, Forespørsel Q2, Forespørsel Q3 og Forespørsel Q4, og en total forespørsel-kolonne som representerer en sum av alle 4 kvartalsvise kolonnene, er bare de kvartalsvise kolonnene eller totalkolonnen tilgjengelig for bruk i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="63387-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="63387-129">Excel-filen kan ikke oppdatere overlappende kolonner under oppdateringen, fordi dataene i tabellen kan bli foreldet og unøyaktige.</span><span class="sxs-lookup"><span data-stu-id="63387-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="63387-130">[![Eksempel](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="63387-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="63387-131">For å unngå potensielle problemer med å vise og redigere budsjettplandata ved hjelp av Excel, bør den samme brukeren være pålogget både Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics Office-tillegget Datakobling.</span><span class="sxs-lookup"><span data-stu-id="63387-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="63387-132">Legge til en topptekst i dokumentmalen for budsjettplan</span><span class="sxs-lookup"><span data-stu-id="63387-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="63387-133">Hvis du vil legge til topptekstinformasjon, velger du den øverste raden i Excel-filen og setter inn tomme rader.</span><span class="sxs-lookup"><span data-stu-id="63387-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="63387-134">Klikk **Utforming** i **Datakobling** for å legge til felt i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="63387-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="63387-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="63387-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="63387-136">I kategorien **Utforming** klikker du **Legg til felt** og velger **BudgetPlanHeader** som enhetsdatakilde.</span><span class="sxs-lookup"><span data-stu-id="63387-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="63387-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="63387-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="63387-138">Pek markøren mot ønsket plassering i Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="63387-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="63387-139">Klikk **Legg til etikett** for å legge til feltetiketten i den valgte plasseringen.</span><span class="sxs-lookup"><span data-stu-id="63387-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="63387-140">Velg **Legge til verdi** for å legge til verdifeltet i det valgte stedet.</span><span class="sxs-lookup"><span data-stu-id="63387-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="63387-141">Klikk på **Ferdig** for å lukke utformingen.</span><span class="sxs-lookup"><span data-stu-id="63387-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="63387-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="63387-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="63387-143">Legge til en beregnet kolonne i dokumentmaltabellen for budsjettplan</span><span class="sxs-lookup"><span data-stu-id="63387-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="63387-144">Deretter vil beregnede kolonner bli lagt til den genererte dokumentmalen for budsjettplan.</span><span class="sxs-lookup"><span data-stu-id="63387-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="63387-145">Kolonnen **Total forespørsel** som summerer kolonnene Forespørsel Q1: Forespørsel Q4, og kolonnen **Justering**, som beregner kolonnen **Total forespørsel** på nytt med en forhåndsdefinert faktor.</span><span class="sxs-lookup"><span data-stu-id="63387-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="63387-146">Klikk **Utforming** i **Datakobling** for å legge til kolonner i tabellen.</span><span class="sxs-lookup"><span data-stu-id="63387-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="63387-147">Klikk **Rediger** ved siden av **BudgetPlanWorksheet**-datakilden for å begynne å legge til kolonner.</span><span class="sxs-lookup"><span data-stu-id="63387-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="63387-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="63387-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="63387-149">Den valgte feltgruppen viser kolonnene som er tilgjengelige i malen.</span><span class="sxs-lookup"><span data-stu-id="63387-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="63387-150">Klikk **Formel** for å legge til en ny kolonne.</span><span class="sxs-lookup"><span data-stu-id="63387-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="63387-151">Gi den nye kolonnen et navn, og lim deretter inn formelen inn i **Formel**-feltet.</span><span class="sxs-lookup"><span data-stu-id="63387-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="63387-152">Klikk **Oppdater** for å sette inn kolonnen.</span><span class="sxs-lookup"><span data-stu-id="63387-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="63387-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="63387-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="63387-154">Hvis du vil definere formelen, oppretter du formelen i regnearket, og deretter kopierer du den til **Utforming**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="63387-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="63387-155">En tabell bundet til Finance and Operations, blir vanligvis kalt "AXTable1".</span><span class="sxs-lookup"><span data-stu-id="63387-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="63387-156">For å summere Forespørsel Q1: Forespørsel Q4 i regnearket, formelen = AxTable1\[Forespørsel Q1\]+ AxTable1\[Forespørsel Q2\]+ AxTable1\[Forespørsel Q3\]+ AxTable1\[Forespørsel Q4\].</span><span class="sxs-lookup"><span data-stu-id="63387-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="63387-157">Gjenta disse trinnene for å sette inn **Justering**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="63387-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="63387-158">Bruk formelen = AxTable1\[Total forespørsel\]\*$I$ 1 for denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="63387-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="63387-159">Dette henter verdien i celle I1 og multipliserer verdiene i kolonnen **Totale forespørsel** for å beregne justeringsbeløpene.</span><span class="sxs-lookup"><span data-stu-id="63387-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="63387-160">Lagre og lukk Excel-filen.</span><span class="sxs-lookup"><span data-stu-id="63387-160">Save and close the Excel file.</span></span> <span data-ttu-id="63387-161">Gå tilbake til Finance and Operations. Under **Oppsett** klikker du på **Mal &gt;Last opp** for å laste opp den lagrede Excel-malen som skal brukes for budsjettplanen.</span><span class="sxs-lookup"><span data-stu-id="63387-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="63387-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="63387-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="63387-163">Lukk **Oppsett**-glidebryteren.</span><span class="sxs-lookup"><span data-stu-id="63387-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="63387-164">I **Budsjettplan**-dokument klikker du **Regneark** for å vise og redigere dokumentet i Excel.</span><span class="sxs-lookup"><span data-stu-id="63387-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="63387-165">Merk at den justerte Excel-malen ble brukt til å opprette dette budsjettplanregnearket, og beregnede kolonner blir oppdatert ved hjelp av formler som ble definert i de forrige trinnene.</span><span class="sxs-lookup"><span data-stu-id="63387-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="63387-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="63387-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="63387-167">Tips og triks for å opprette budsjettplanmaler</span><span class="sxs-lookup"><span data-stu-id="63387-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="63387-168">Kan jeg legge til og bruke flere datakilder i en budsjettplanmal?</span><span class="sxs-lookup"><span data-stu-id="63387-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="63387-169">Ja, du kan bruke **Utforming**-menyen til å legge til flere enheter i samme eller andre ark i Excel-malen.</span><span class="sxs-lookup"><span data-stu-id="63387-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="63387-170">Du kan for eksempel legge til **BudgetPlanProposedProject**-datakilden for å opprette og vedlikeholde en liste over foreslåtte prosjekter samtidig når du arbeider med budsjettplandata i Excel.</span><span class="sxs-lookup"><span data-stu-id="63387-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="63387-171">Vær oppmerksom på at inkludering av datakilder med store volumer kan ha innvirkning på Excel-arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="63387-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="63387-172">Du kan bruke **Filter**-alternativet i **Datakobling** til å legge til ønskede filtre i flere datakilder.</span><span class="sxs-lookup"><span data-stu-id="63387-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="63387-173">Kan jeg skjule utformingsalternativet i Datakobling for andre brukere?</span><span class="sxs-lookup"><span data-stu-id="63387-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="63387-174">Ja, åpne alternativene for **Datakobling** for å skjule **Utforming**-alternativet fra andre brukere.</span><span class="sxs-lookup"><span data-stu-id="63387-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="63387-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="63387-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="63387-176">Utvid **Alternativer for datakobling** og fjern merket for **Aktiver utforming**.</span><span class="sxs-lookup"><span data-stu-id="63387-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="63387-177">Dette skjuler **Utforming**-alternativet fra **Datakobling**.</span><span class="sxs-lookup"><span data-stu-id="63387-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="63387-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="63387-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="63387-179">Kan jeg hindre at brukere ved et uhell lukker datakoblingen under arbeid med data?</span><span class="sxs-lookup"><span data-stu-id="63387-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="63387-180">Vi anbefaler å låse malen for å hindre brukere i å lukke den.</span><span class="sxs-lookup"><span data-stu-id="63387-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="63387-181">Du aktiverer låsen ved å klikke **Datakobling**. Det vises en pil i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="63387-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="63387-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="63387-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="63387-183">Klikk pilen for en åpne en tilleggsmeny.</span><span class="sxs-lookup"><span data-stu-id="63387-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="63387-184">Velg **Lås**.</span><span class="sxs-lookup"><span data-stu-id="63387-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="63387-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="63387-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="63387-186">Kan jeg bruke andre Excel-funksjoner, som celleformatering, farger, betinget formatering og diagrammer, med mine budsjettplanmaler?</span><span class="sxs-lookup"><span data-stu-id="63387-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="63387-187">Ja, de fleste standard Excel-funksjonene virker i budsjettplanmaler.</span><span class="sxs-lookup"><span data-stu-id="63387-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="63387-188">Vi anbefaler å bruke fargekoding slik at brukere kan skille mellom skrivebeskyttede og redigerbare kolonner.</span><span class="sxs-lookup"><span data-stu-id="63387-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="63387-189">Betinget formatering kan brukes til å fremheve problematiske områder i budsjettet.</span><span class="sxs-lookup"><span data-stu-id="63387-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="63387-190">Kolonnesummer kan enkelt presenteres ved hjelp av standard Excel-formler over tabellen.</span><span class="sxs-lookup"><span data-stu-id="63387-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="63387-191">Du kan også opprette og bruke pivottabeller og diagrammer for flere grupperinger og visualiseringer av budsjettdata.</span><span class="sxs-lookup"><span data-stu-id="63387-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="63387-192">I **Data**-kategorien i **Tilkoblinger**-gruppen klikker du **Oppdater alle**, og klikker deretter **Tilkoblingsegenskaper**.</span><span class="sxs-lookup"><span data-stu-id="63387-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="63387-193">Klikk kategorien **Bruk**. Under **Oppdater** velger du avmerkningsboksen **Oppdater data når filen åpnes**.</span><span class="sxs-lookup"><span data-stu-id="63387-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="63387-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="63387-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




