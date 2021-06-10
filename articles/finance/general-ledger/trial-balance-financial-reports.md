---
title: Finansrapporter for råbalanse
description: Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103664"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="4d671-104">Finansrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="4d671-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d671-105">Denne artikkelen beskriver standardrapportene for råbalanser.</span><span class="sxs-lookup"><span data-stu-id="4d671-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="4d671-106">Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="4d671-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="4d671-107">Standardrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="4d671-107">Default trial balance reports</span></span>

<span data-ttu-id="4d671-108">Tre råbalanserapporter er tilgjengelige i Finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="4d671-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="4d671-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="4d671-109">Default report</span></span>                                 | <span data-ttu-id="4d671-110">Resultat</span><span class="sxs-lookup"><span data-stu-id="4d671-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d671-111">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="4d671-112">Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4d671-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="4d671-113">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="4d671-114">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.</span><span class="sxs-lookup"><span data-stu-id="4d671-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="4d671-115">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="4d671-116">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.</span><span class="sxs-lookup"><span data-stu-id="4d671-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="4d671-117">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="4d671-117">Building blocks</span></span>
<span data-ttu-id="4d671-118">Finansrapportene for råbalanse bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4d671-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="4d671-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="4d671-119">Default report</span></span>                                 | <span data-ttu-id="4d671-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="4d671-120">Row definition</span></span>          | <span data-ttu-id="4d671-121">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="4d671-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="4d671-122">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="4d671-123">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="4d671-123">Trial Balance - Default</span></span> | <span data-ttu-id="4d671-124">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="4d671-125">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="4d671-126">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="4d671-126">Trial Balance - Default</span></span> | <span data-ttu-id="4d671-127">Råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="4d671-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="4d671-128">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="4d671-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="4d671-129">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="4d671-129">Trial Balance - Default</span></span> | <span data-ttu-id="4d671-130">Årlig råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="4d671-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="4d671-131">Når du kjører rapporten **Råbalanse** i Financial Reporting, må du huske å merke av for **Vis rader uten beløp** og **Vise rapporter uten aktive rader** i kategorien **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="4d671-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="4d671-132">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="4d671-132">Row definition</span></span>

<span data-ttu-id="4d671-133">Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="4d671-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="4d671-134">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="4d671-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="4d671-135">Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="4d671-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="4d671-136">Du kan endre raddefinisjonen slik at den inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="4d671-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="4d671-137">Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="4d671-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="4d671-138">Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="4d671-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="4d671-139">Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4d671-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="4d671-140">Du skal bruke **Hovedkonto** for denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4d671-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="4d671-141">Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4d671-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="4d671-142">Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="4d671-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="4d671-143">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="4d671-143">Column definition</span></span>

<span data-ttu-id="4d671-144">Hver rapport for råbalanse bruker en annen kolonnedefinisjon.</span><span class="sxs-lookup"><span data-stu-id="4d671-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="4d671-145">Disse kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="4d671-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="4d671-146">**Detaljert råbalanse – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="4d671-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="4d671-147">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4d671-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4d671-148">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="4d671-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="4d671-149">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="4d671-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="4d671-150">Transaksjonsdato</span><span class="sxs-lookup"><span data-stu-id="4d671-150">Transaction Date</span></span>
        -   <span data-ttu-id="4d671-151">Bilag</span><span class="sxs-lookup"><span data-stu-id="4d671-151">Voucher</span></span>
        -   <span data-ttu-id="4d671-152">Journalbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="4d671-152">Journal Description</span></span>
    -   <span data-ttu-id="4d671-153">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="4d671-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="4d671-154">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="4d671-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="4d671-155">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="4d671-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="4d671-156">**Råbalansesammendrag – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="4d671-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="4d671-157">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="4d671-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="4d671-158">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4d671-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4d671-159">**ATTR** – Et attributt:</span><span class="sxs-lookup"><span data-stu-id="4d671-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="4d671-160">Bilag</span><span class="sxs-lookup"><span data-stu-id="4d671-160">Voucher</span></span>
    -   <span data-ttu-id="4d671-161">**FD** – Økonomiske data for starsaldo</span><span class="sxs-lookup"><span data-stu-id="4d671-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="4d671-162">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="4d671-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="4d671-163">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="4d671-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="4d671-164">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="4d671-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="4d671-165">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="4d671-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="4d671-166">**Årlig råbalansesammendrag – standard:**</span><span class="sxs-lookup"><span data-stu-id="4d671-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="4d671-167">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="4d671-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="4d671-168">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="4d671-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4d671-169">**ATTR** – Et attributt</span><span class="sxs-lookup"><span data-stu-id="4d671-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="4d671-170">Bilag</span><span class="sxs-lookup"><span data-stu-id="4d671-170">Voucher</span></span>
    -   <span data-ttu-id="4d671-171">**FD** – Økonomiske data for startsaldo for inneværende år</span><span class="sxs-lookup"><span data-stu-id="4d671-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="4d671-172">**FD** Økonomiske data som inneholder bare debet for inneværende år</span><span class="sxs-lookup"><span data-stu-id="4d671-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="4d671-173">**FD** – Økonomiske data som inneholder bare kredit for inneværende år</span><span class="sxs-lookup"><span data-stu-id="4d671-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="4d671-174">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="4d671-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="4d671-175">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="4d671-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="4d671-176">**FD** – Økonomiske data som inneholder bare debet for forrige år</span><span class="sxs-lookup"><span data-stu-id="4d671-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="4d671-177">**FD** – Økonomiske data som inneholder bare kredit for forrige år</span><span class="sxs-lookup"><span data-stu-id="4d671-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d671-178">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4d671-178">Additional resources</span></span>

[<span data-ttu-id="4d671-179">Oversikt over finansrapportering</span><span class="sxs-lookup"><span data-stu-id="4d671-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="4d671-180">Vise finansrapporter</span><span class="sxs-lookup"><span data-stu-id="4d671-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="4d671-181">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="4d671-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
