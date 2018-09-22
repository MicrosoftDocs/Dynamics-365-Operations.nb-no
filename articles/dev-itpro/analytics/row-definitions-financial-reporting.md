---
title: Raddefinisjoner i Utforming av finansrapport
description: "En raddefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i hver rad i finansrapport. En raddefinisjon kan kombineres med kolonnedefinisjoner, definisjoner av rapporttre og rapportdefinisjoner for å opprette en blokkgruppe som kan brukes av flere firmaer."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.contentlocale: nb-no
ms.lasthandoff: 08/13/2018

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="3fb5b-104">Raddefinisjoner i Utforming av finansrapport</span><span class="sxs-lookup"><span data-stu-id="3fb5b-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fb5b-105">En raddefinisjon er en rapportkomponent eller byggeblokk som angir innholdet i hver rad i finansrapport.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="3fb5b-106">En raddefinisjon kan kombineres med kolonnedefinisjoner, definisjoner av rapporttre og rapportdefinisjoner for å opprette en blokkgruppe som kan brukes av flere firmaer.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="3fb5b-107">Opprette en raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-107">Create a row definition</span></span>

1. <span data-ttu-id="3fb5b-108">I navigasjonsruten i Rapportutforming klikker du **Raddefinisjoner**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="3fb5b-109">Klikk **Ny** på **Fil**-menyen, og klikk deretter **Raddefinisjon**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="3fb5b-110">Hvis du vil ha mer informasjon om innholdet i hver celle, kan du se [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="3fb5b-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="3fb5b-111">Åpne en raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-111">Open a row definition</span></span>
1. <span data-ttu-id="3fb5b-112">I navigasjonsruten i Rapportutforming klikker du **Raddefinisjoner**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="3fb5b-113">Dobbeltklikk navnet på raddefinisjonen du vil åpne.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="3fb5b-114">Hvis du vil vise alle byggeblokker som er knyttet til raddefinisjonen, høyreklikker du raddefinisjonen og velger deretter **Tilknytninger**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="3fb5b-115"> Innholdet i en raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-115">Contents of a row definition</span></span>
<span data-ttu-id="3fb5b-116">En raddefinisjon kan inneholde opptil 20 000 finansdimensjonsrader og kan inneholder følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="3fb5b-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="3fb5b-117">Beskrivende tekst som gir mening i rapporten ved å opprette inndelingsoverskrifter, linjer og mellomrom, for eksempel **Kontanter** eller **Totalomsetning**</span><span class="sxs-lookup"><span data-stu-id="3fb5b-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="3fb5b-118">Koblinger til økonomiske data, som kan inkludere dimensjonsverdier i Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3fb5b-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fb5b-119">Du kan sette opp en raddefinisjon til å hente data fra finansdimensjonssystemet hver gang rapporten genereres.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="3fb5b-120">Totaler og formler for rader som er basert på de økonomiske dataen som er koblet</span><span class="sxs-lookup"><span data-stu-id="3fb5b-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="3fb5b-121">Hver rad i en raddefinisjon inneholder vanligvis én av følgende typer informasjon:</span><span class="sxs-lookup"><span data-stu-id="3fb5b-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="3fb5b-122">Referanser til finansdimensjonssystemet</span><span class="sxs-lookup"><span data-stu-id="3fb5b-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="3fb5b-123">Totaler eller beregninger som er basert på dataene</span><span class="sxs-lookup"><span data-stu-id="3fb5b-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="3fb5b-124">Formatering</span><span class="sxs-lookup"><span data-stu-id="3fb5b-124">Formatting</span></span>

<span data-ttu-id="3fb5b-125">Det finnes to metoder for å skrive inn informasjon i en raddefinisjon:</span><span class="sxs-lookup"><span data-stu-id="3fb5b-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="3fb5b-126">Angi radinformasjon manuelt i en ny raddefinisjon.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="3fb5b-127">Hvis du vil ha mer informasjon, kan du se [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="3fb5b-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="3fb5b-128">Bruk rapportutforming til å hente radinformasjon direkte fra finansdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="3fb5b-129">Hvis du vil ha mer informasjon, kan du se delen Relaterte formler/rader/enheter i [Endre celler for raddefinisjon](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="3fb5b-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="3fb5b-130"> Legge til dimensjoner i en raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="3fb5b-131">En dimensjon er en overlapping av data og verdier.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="3fb5b-132">Du kan gruppere data og verdier i rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-132">You can group data and values in report designer.</span></span> <span data-ttu-id="3fb5b-133">Du kan deretter klassifisere og analysere transaksjoner mer detaljert.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="3fb5b-134">Du kan bruke dialogboksen **Sett inn rader fra dimensjoner** for å legge til flere rader i en raddefinisjon samtidig.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="3fb5b-135">Dialogboksen viser én kolonne for hver dimensjon.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="3fb5b-136">Tabellen nedenfor beskriver informasjonen du kan angi i hver dimensjon.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="3fb5b-137">Alternativ</span><span class="sxs-lookup"><span data-stu-id="3fb5b-137">Option</span></span>                | <span data-ttu-id="3fb5b-138">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="3fb5b-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="3fb5b-139">Dimensjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-139">Dimension</span></span>             | <span data-ttu-id="3fb5b-140">Mønsteret som identifiserer dimensjonen som skal legges til raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="3fb5b-141">Dette mønsteret inneholder ett &-tegn eller nummertegn (\#) for hver posisjon i dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="3fb5b-142">Bruk vanligvis bare &-tegn for hovedkontodimensjonen og bare nummertegn (#) for andre dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="3fb5b-143">Dimensjonsområdestart</span><span class="sxs-lookup"><span data-stu-id="3fb5b-143">Dimension Range Start</span></span> | <span data-ttu-id="3fb5b-144">Den første verdien for denne dimensjonen som skal legges til i raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="3fb5b-145">Dimensjonsområdeslutt</span><span class="sxs-lookup"><span data-stu-id="3fb5b-145">Dimension Range End</span></span>   | <span data-ttu-id="3fb5b-146">Den siste verdien for denne dimensjonen som skal legges til raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="3fb5b-147">Følg fremgangsmåten nedenfor for å legge til dimensjoner i en raddefinisjon.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="3fb5b-148">I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-149">På **Rediger**-menyen klikker du **Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="3fb5b-150">I dialogboksen **Sett inn rader fra dimensjoner**, i **Dimensjoner**-raden, velger du cellen for dimensjonen som skal overføres til raddefinisjonen, og deretter klikker du **Bare &&&**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="3fb5b-151">Hvis du vil begrense raddefinisjonen for et bestemt områder dimensjonsverdier, angir du startverdien for dimensjonen i cellen **Start på dimensjonsområde**, og deretter angir du sluttverdien for dimensjonen i cellen **Slutt på dimensjonsområde**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="3fb5b-152">Hvis du vil inkludere alle verdier for den valgte dimensjonen, lar du disse cellene stå tomme.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fb5b-153">Jokertegn (\* eller ?) i dimensjonsområder returnerer kanskje ikke alle resultatene du ønsker, alt etter hvordan ERP-databasen sorterer data.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="3fb5b-154">I feltet **Kode for startrad** angir du radkoden for den første dimensjonsverdien som skal legges til raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="3fb5b-155">I feltet **Øk hver rad med** angir du avstanden mellom etterfølgende radkoder.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="3fb5b-156">Hvis den første radkoden for eksempel er 100 og økningsverdien er 30, har de første nye radene kodene 100, 130, 160, 190 og 220.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="3fb5b-157">Bruk en inkrementell verdi som gir nok plass til å sette inn nye format- og formelrader.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="3fb5b-158">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-158">Click **OK**.</span></span> <span data-ttu-id="3fb5b-159">Én linje for hver valgte dimensjonsverdi legges til raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="3fb5b-160"> Justere avrunding i en raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="3fb5b-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="3fb5b-161">Hvis du har en balanse der beløpene er avrundet, kan det hende totalene ikke er i balanse.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="3fb5b-162">Dette problemet kan oppstå hvis du for eksempel bruker alternativet for avrunding på en balanserapport og rapportdefinisjonen også angir avrunding.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="3fb5b-163">Du kan bruke alternativet **Avrundingsjustering** i raddefinisjonen for å balansere beløpene i balansen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="3fb5b-164">Du kan deaktivere eller endre avrunding i kategorien **Innstillinger** i rapportdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="3fb5b-165">Tabellen nedenfor viser hvordan beløp avrundes.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="3fb5b-166">I denne tabellen er totalene forskjellige for rad 100 og 200 når avrunding er aktivert.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="3fb5b-167">Radkode</span><span class="sxs-lookup"><span data-stu-id="3fb5b-167">Row code</span></span> | <span data-ttu-id="3fb5b-168">Beløp uten avrunding</span><span class="sxs-lookup"><span data-stu-id="3fb5b-168">Amounts without rounding</span></span> | <span data-ttu-id="3fb5b-169">Beløp med avrunde til hele tusener</span><span class="sxs-lookup"><span data-stu-id="3fb5b-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="3fb5b-170">100</span><span class="sxs-lookup"><span data-stu-id="3fb5b-170">100</span></span>      | <span data-ttu-id="3fb5b-171">3,600</span><span class="sxs-lookup"><span data-stu-id="3fb5b-171">3,600</span></span>                    | <span data-ttu-id="3fb5b-172">4</span><span class="sxs-lookup"><span data-stu-id="3fb5b-172">4</span></span>                                       |
| <span data-ttu-id="3fb5b-173">200</span><span class="sxs-lookup"><span data-stu-id="3fb5b-173">200</span></span>      | <span data-ttu-id="3fb5b-174">3,700</span><span class="sxs-lookup"><span data-stu-id="3fb5b-174">3,700</span></span>                    | <span data-ttu-id="3fb5b-175">4</span><span class="sxs-lookup"><span data-stu-id="3fb5b-175">4</span></span>                                       |
| <span data-ttu-id="3fb5b-176">Sum</span><span class="sxs-lookup"><span data-stu-id="3fb5b-176">Total</span></span>    | <span data-ttu-id="3fb5b-177">7,300</span><span class="sxs-lookup"><span data-stu-id="3fb5b-177">7,300</span></span>                    | <span data-ttu-id="3fb5b-178">8</span><span class="sxs-lookup"><span data-stu-id="3fb5b-178">8</span></span>                                       |

<span data-ttu-id="3fb5b-179">Følg fremgangsmåten nedenfor hvis du vil justere avrunding i en balanse.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="3fb5b-180">I Rapportutforming klikker du **Raddefinisjoner**, og deretter åpner du raddefinisjonen som skal endres.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-181">Klikk **Avrundingsjustering** på **Rediger**-menyen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="3fb5b-182">Skriv inn følgende verdier i dialogboksen **Avrundingsjusteringer**:</span><span class="sxs-lookup"><span data-stu-id="3fb5b-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="3fb5b-183">**Raden Avrundingsjustering** – Radkoden for raden som skal justeres for å balansere balansen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="3fb5b-184">**Raden Sum aktiva** – Radkoden for raden i balansen som inneholder de samlede aktivaene.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="3fb5b-185">**Raden Samlet gjeld og egenkapital** – Radkoden for raden i balansen som inneholder samlet gjeld og egenkapital.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="3fb5b-186">**Grense for justeringsbeløp** – Et positivt heltall som angir grensen for automatiske justeringer.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="3fb5b-187">Dette beløpet sammenlignes med den absolutte verdien for den faktiske avrundingsdifferansen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fb5b-188">Disse radkodene må være koblet til finansdataene.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="3fb5b-189">Raden må med andre ord ha en dimensjonsverdi i cellen **Kobling til finansdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="3fb5b-190">**Ikke** refererer til raden for beskrivelse (**DESC**), beregnet (**CALC**) eller summert (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="3fb5b-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="3fb5b-191">Beløpene i balansen vil nå være i balanse når avrunding er aktivert.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="3fb5b-192">Justeringsgrensen brukes basert på hva som er angitt under alternativet **Avrundingspresisjon** for rapportdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="3fb5b-193">Hvis du for eksempel velger å runde av rapporten til tusener og angi **2** i feltet **Grense for justeringsbeløp**, vises en advarsel når verdien som identifiseres i feltet **Raden Avrundingsjustering**, økes eller reduseres med mer enn 2 000.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="3fb5b-194">Formatere rad- og kolonnetekst</span><span class="sxs-lookup"><span data-stu-id="3fb5b-194">Format row and column text</span></span>
<span data-ttu-id="3fb5b-195">Du kan tilpasse utseendet på rapportene ved å endre skrifter og formatere tekst.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="3fb5b-196">Avsnittene nedenfor beskriver hvordan du kan formatere utseendet på rader og kolonner i rapporter.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="3fb5b-197">Behandle skriftstiler</span><span class="sxs-lookup"><span data-stu-id="3fb5b-197">Manage font styles</span></span>

<span data-ttu-id="3fb5b-198">Du kan opprette og endre skriftstiler for rapporten.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="3fb5b-199">Du kan deretter bruke disse stilene i dokumentet, eller på en bestemt rad eller kolonne i en rapport.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="3fb5b-200"><strong>Opprette en skriftstil</strong></span><span class="sxs-lookup"><span data-stu-id="3fb5b-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="3fb5b-201">På <strong>Format</strong>-menyen i Rapportutforming klikker du <strong>Stiler og formatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="3fb5b-202">Klikk <strong>Ny</strong> i dialogboksen <strong>Stiler og formatering</strong>, og skriv deretter inn et unikt navn for den nye stilen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="3fb5b-203">Velg skrifter, og klikk deretter <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3fb5b-204"><strong>Endre en skriftstil</strong></span><span class="sxs-lookup"><span data-stu-id="3fb5b-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="3fb5b-205">På <strong>Format</strong>-menyen i Rapportutforming klikker du <strong>Stiler og formatering</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="3fb5b-206">Velg en stil du vil endre i dialogboksen <strong>Stiler og formatering</strong>, og klikk deretter <strong>Endre</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="3fb5b-207">Velg skrifter, og klikk deretter <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3fb5b-208"><strong>Bruke en skriftstil</strong></span><span class="sxs-lookup"><span data-stu-id="3fb5b-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="3fb5b-209">I en definisjon eller kolonnedefinisjon, eller i topptekst og bunntekst, velger du én eller flere celler i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="3fb5b-210">Velg en skriftstil i <strong>Stil</strong>-listen på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="3fb5b-211">Formatere radtekst</span><span class="sxs-lookup"><span data-stu-id="3fb5b-211">Format row text</span></span>

<span data-ttu-id="3fb5b-212">Formateringen som er angitt i raddefinisjonen, overstyrer all formatering som er angitt i kolonnedefinisjonen og rapportdefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="3fb5b-213">Du kan endre tekstformatet ved hjelp av kontrollene på formateringsverktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="3fb5b-214">Disse kontrollene er standardkontroller for Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="3fb5b-215">Åpne raddefinisjonen som skal endres i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-216">Velg cellene som skal formateres.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-216">Select the cells to format.</span></span> <span data-ttu-id="3fb5b-217">Hvis du vil velge flere celler, holder du nede CTRL-tasten når du velger cellen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="3fb5b-218">Klikk verktøylinjeknappen for formatet som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="3fb5b-219">Hvis du for eksempel vil rykke inn en rad, velger du raden og klikk deretter på **Øk innrykk** ![Øk innrykk](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Øk innrykk") på verktøylinjen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="3fb5b-220">Justere kolonner mens du utformer rapporter</span><span class="sxs-lookup"><span data-stu-id="3fb5b-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="3fb5b-221">Hvis du vil gjøre det enklere å vise kolonnene som du arbeider med i raddefinisjonen, kan du justere bredden på en kolonne og skjul (minimere) eller vise kolonner i visningsruten.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="3fb5b-222">Endringene du gjør, påvirker bare utseendet til kolonnene på skjermen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="3fb5b-223">De påvirker ikke kolonneformatering i rapporter.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="3fb5b-224">Endre bredden på en kolonne i visningruten</span><span class="sxs-lookup"><span data-stu-id="3fb5b-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="3fb5b-225">Åpne raddefinisjonen som skal endres i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-226">Velg **Kolonnebredde** på **Format**-menyen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="3fb5b-227">Angi en verdi, og klikk deretter **OK** i dialogboksen **Kolonnebredde**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="3fb5b-228">Du kan også dra den høyre kanten av en kolonneoverskriftscelle for å endre bredden på kolonnen.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="3fb5b-229">Skjule kolonner i visningsruten</span><span class="sxs-lookup"><span data-stu-id="3fb5b-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="3fb5b-230">Åpne raddefinisjonen som skal endres i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-231">Merk kolonnen eller kolonnene som skal minimeres.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="3fb5b-232">Høyreklikk og klikk deretter **Skjul**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="3fb5b-233">Vise alle skjulte kolonner i visningsruten</span><span class="sxs-lookup"><span data-stu-id="3fb5b-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="3fb5b-234">Åpne raddefinisjonen som skal endres i Rapportutforming.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="3fb5b-235">Høyreklikk den minimerte kolonnen som skal vises, og klikk deretter **Vis**.</span><span class="sxs-lookup"><span data-stu-id="3fb5b-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="3fb5b-236">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3fb5b-236">Additional resources</span></span>

[<span data-ttu-id="3fb5b-237">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="3fb5b-237">Financial reporting</span></span>](financial-reporting-intro.md)

