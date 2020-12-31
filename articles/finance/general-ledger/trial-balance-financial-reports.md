---
title: Finansrapporter for råbalanse
description: Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b48510febf5a5f9f4a01728b242d9750b3c62c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446245"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="ff783-104">Finansrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="ff783-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff783-105">Denne artikkelen beskriver standardrapportene for råbalanser.</span><span class="sxs-lookup"><span data-stu-id="ff783-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="ff783-106">Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="ff783-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="ff783-107">Standardrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="ff783-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="ff783-108">Tre råbalanserapporter er tilgjengelige i Finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="ff783-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="ff783-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="ff783-109">Default report</span></span>                                 | <span data-ttu-id="ff783-110">Resultat</span><span class="sxs-lookup"><span data-stu-id="ff783-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff783-111">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="ff783-112">Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ff783-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="ff783-113">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="ff783-114">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.</span><span class="sxs-lookup"><span data-stu-id="ff783-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="ff783-115">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="ff783-116">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.</span><span class="sxs-lookup"><span data-stu-id="ff783-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="ff783-117">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="ff783-117">Building blocks</span></span>
<span data-ttu-id="ff783-118">Finansrapportene for råbalanse bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ff783-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="ff783-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="ff783-119">Default report</span></span>                                 | <span data-ttu-id="ff783-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="ff783-120">Row definition</span></span>          | <span data-ttu-id="ff783-121">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="ff783-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="ff783-122">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="ff783-123">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="ff783-123">Trial Balance - Default</span></span> | <span data-ttu-id="ff783-124">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="ff783-125">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="ff783-126">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="ff783-126">Trial Balance - Default</span></span> | <span data-ttu-id="ff783-127">Råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="ff783-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="ff783-128">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="ff783-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="ff783-129">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="ff783-129">Trial Balance - Default</span></span> | <span data-ttu-id="ff783-130">Årlig råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="ff783-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="ff783-131">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="ff783-131">Row definition</span></span>

<span data-ttu-id="ff783-132">Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="ff783-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="ff783-133">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="ff783-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="ff783-134">Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="ff783-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="ff783-135">Du kan endre raddefinisjonen slik at den inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="ff783-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="ff783-136">Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ff783-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="ff783-137">Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="ff783-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="ff783-138">Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ff783-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="ff783-139">Du skal bruke **Hovedkonto** for denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ff783-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="ff783-140">Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff783-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="ff783-141">Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="ff783-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="ff783-142">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="ff783-142">Column definition</span></span>

<span data-ttu-id="ff783-143">Hver rapport for råbalanse bruker en annen kolonnedefinisjon.</span><span class="sxs-lookup"><span data-stu-id="ff783-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="ff783-144">Disse kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="ff783-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="ff783-145">**Detaljert råbalanse – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="ff783-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="ff783-146">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ff783-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ff783-147">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="ff783-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ff783-148">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="ff783-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="ff783-149">Transaksjonsdato</span><span class="sxs-lookup"><span data-stu-id="ff783-149">Transaction Date</span></span>
        -   <span data-ttu-id="ff783-150">Bilag</span><span class="sxs-lookup"><span data-stu-id="ff783-150">Voucher</span></span>
        -   <span data-ttu-id="ff783-151">Journalbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="ff783-151">Journal Description</span></span>
    -   <span data-ttu-id="ff783-152">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="ff783-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="ff783-153">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="ff783-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="ff783-154">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="ff783-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="ff783-155">**Råbalansesammendrag – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="ff783-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="ff783-156">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="ff783-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ff783-157">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ff783-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ff783-158">**ATTR** – Et attributt:</span><span class="sxs-lookup"><span data-stu-id="ff783-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="ff783-159">Bilag</span><span class="sxs-lookup"><span data-stu-id="ff783-159">Voucher</span></span>
    -   <span data-ttu-id="ff783-160">**FD** – Økonomiske data for starsaldo</span><span class="sxs-lookup"><span data-stu-id="ff783-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="ff783-161">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="ff783-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="ff783-162">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="ff783-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="ff783-163">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="ff783-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="ff783-164">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="ff783-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="ff783-165">**Årlig råbalansesammendrag – standard:**</span><span class="sxs-lookup"><span data-stu-id="ff783-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="ff783-166">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="ff783-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="ff783-167">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="ff783-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="ff783-168">**ATTR** – Et attributt</span><span class="sxs-lookup"><span data-stu-id="ff783-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="ff783-169">Bilag</span><span class="sxs-lookup"><span data-stu-id="ff783-169">Voucher</span></span>
    -   <span data-ttu-id="ff783-170">**FD** – Økonomiske data for startsaldo for inneværende år</span><span class="sxs-lookup"><span data-stu-id="ff783-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="ff783-171">**FD** Økonomiske data som inneholder bare debet for inneværende år</span><span class="sxs-lookup"><span data-stu-id="ff783-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="ff783-172">**FD** – Økonomiske data som inneholder bare kredit for inneværende år</span><span class="sxs-lookup"><span data-stu-id="ff783-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="ff783-173">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="ff783-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="ff783-174">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="ff783-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="ff783-175">**FD** – Økonomiske data som inneholder bare debet for forrige år</span><span class="sxs-lookup"><span data-stu-id="ff783-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="ff783-176">**FD** – Økonomiske data som inneholder bare kredit for forrige år</span><span class="sxs-lookup"><span data-stu-id="ff783-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="ff783-177">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ff783-177">Additional resources</span></span>
--------

[<span data-ttu-id="ff783-178">Oversikt over finansrapportering</span><span class="sxs-lookup"><span data-stu-id="ff783-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="ff783-179">Vise finansrapporter</span><span class="sxs-lookup"><span data-stu-id="ff783-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="ff783-180">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="ff783-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



