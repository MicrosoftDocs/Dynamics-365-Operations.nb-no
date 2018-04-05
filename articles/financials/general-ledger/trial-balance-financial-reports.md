---
title: "Finansrapporter for råbalanse"
description: "Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 77e46e8693c65410ac7c44754edcb3c181f2aa18
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="trial-balance-financial-reports"></a><span data-ttu-id="8b0ec-104">Finansrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="8b0ec-104">Trial balance financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8b0ec-105">Denne artikkelen beskriver standardrapportene for råbalanser.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="8b0ec-106">Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="8b0ec-107">Standardrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="8b0ec-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="8b0ec-108">Tre råbalanserapporter er tilgjengelige i økonomisk rapportering i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="8b0ec-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="8b0ec-109">Default report</span></span>                                 | <span data-ttu-id="8b0ec-110">Resultat</span><span class="sxs-lookup"><span data-stu-id="8b0ec-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ec-111">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="8b0ec-112">Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="8b0ec-113">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="8b0ec-114">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="8b0ec-115">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="8b0ec-116">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="8b0ec-117">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="8b0ec-117">Building blocks</span></span>
<span data-ttu-id="8b0ec-118">Finansrapportene for råbalanse bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="8b0ec-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="8b0ec-119">Default report</span></span>                                 | <span data-ttu-id="8b0ec-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="8b0ec-120">Row definition</span></span>          | <span data-ttu-id="8b0ec-121">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="8b0ec-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="8b0ec-122">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="8b0ec-123">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-123">Trial Balance - Default</span></span> | <span data-ttu-id="8b0ec-124">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="8b0ec-125">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="8b0ec-126">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-126">Trial Balance - Default</span></span> | <span data-ttu-id="8b0ec-127">Råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="8b0ec-128">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="8b0ec-129">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-129">Trial Balance - Default</span></span> | <span data-ttu-id="8b0ec-130">Årlig råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="8b0ec-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="8b0ec-131">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="8b0ec-131">Row definition</span></span>

<span data-ttu-id="8b0ec-132">Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="8b0ec-133">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="8b0ec-134">Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="8b0ec-135">Du kan endre raddefinisjonen slik at den inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="8b0ec-136">Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="8b0ec-137">Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="8b0ec-138">Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="8b0ec-139">Du skal bruke **Hovedkonto** for denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="8b0ec-140">Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="8b0ec-141">Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="8b0ec-142">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="8b0ec-142">Column definition</span></span>

<span data-ttu-id="8b0ec-143">Hver rapport for råbalanse bruker en annen kolonnedefinisjon.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="8b0ec-144">Disse kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="8b0ec-145">**Detaljert råbalanse – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="8b0ec-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="8b0ec-146">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8b0ec-147">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="8b0ec-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8b0ec-148">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="8b0ec-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="8b0ec-149">Transaksjonsdato</span><span class="sxs-lookup"><span data-stu-id="8b0ec-149">Transaction Date</span></span>
        -   <span data-ttu-id="8b0ec-150">Bilag</span><span class="sxs-lookup"><span data-stu-id="8b0ec-150">Voucher</span></span>
        -   <span data-ttu-id="8b0ec-151">Journalbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8b0ec-151">Journal Description</span></span>
    -   <span data-ttu-id="8b0ec-152">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="8b0ec-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="8b0ec-153">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="8b0ec-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="8b0ec-154">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="8b0ec-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="8b0ec-155">**Råbalansesammendrag – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="8b0ec-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="8b0ec-156">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="8b0ec-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8b0ec-157">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8b0ec-158">**ATTR** – Et attributt:</span><span class="sxs-lookup"><span data-stu-id="8b0ec-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="8b0ec-159">Bilag</span><span class="sxs-lookup"><span data-stu-id="8b0ec-159">Voucher</span></span>
    -   <span data-ttu-id="8b0ec-160">**FD** – Økonomiske data for starsaldo</span><span class="sxs-lookup"><span data-stu-id="8b0ec-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="8b0ec-161">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="8b0ec-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="8b0ec-162">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="8b0ec-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="8b0ec-163">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="8b0ec-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="8b0ec-164">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="8b0ec-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="8b0ec-165">**Årlig råbalansesammendrag – standard:**</span><span class="sxs-lookup"><span data-stu-id="8b0ec-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="8b0ec-166">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="8b0ec-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="8b0ec-167">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="8b0ec-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="8b0ec-168">**ATTR** – Et attributt</span><span class="sxs-lookup"><span data-stu-id="8b0ec-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="8b0ec-169">Bilag</span><span class="sxs-lookup"><span data-stu-id="8b0ec-169">Voucher</span></span>
    -   <span data-ttu-id="8b0ec-170">**FD** – Økonomiske data for startsaldo for inneværende år</span><span class="sxs-lookup"><span data-stu-id="8b0ec-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="8b0ec-171">**FD** Økonomiske data som inneholder bare debet for inneværende år</span><span class="sxs-lookup"><span data-stu-id="8b0ec-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="8b0ec-172">**FD** – Økonomiske data som inneholder bare kredit for inneværende år</span><span class="sxs-lookup"><span data-stu-id="8b0ec-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="8b0ec-173">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="8b0ec-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="8b0ec-174">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="8b0ec-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="8b0ec-175">**FD** – Økonomiske data som inneholder bare debet for forrige år</span><span class="sxs-lookup"><span data-stu-id="8b0ec-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="8b0ec-176">**FD** – Økonomiske data som inneholder bare kredit for forrige år</span><span class="sxs-lookup"><span data-stu-id="8b0ec-176">**FD** – Financial data that contains only credits for the last year</span></span>

 

<a name="see-also"></a><span data-ttu-id="8b0ec-177">Se også</span><span class="sxs-lookup"><span data-stu-id="8b0ec-177">See also</span></span>
--------

[<span data-ttu-id="8b0ec-178">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="8b0ec-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="8b0ec-179">Vis finansrapporter</span><span class="sxs-lookup"><span data-stu-id="8b0ec-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="8b0ec-180">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="8b0ec-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




