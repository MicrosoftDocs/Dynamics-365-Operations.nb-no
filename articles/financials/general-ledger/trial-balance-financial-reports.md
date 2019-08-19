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
ms.openlocfilehash: 842eecf68f5a658be6cdc7a05c365a18fe7d91dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846105"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="d3c99-104">Finansrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="d3c99-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3c99-105">Denne artikkelen beskriver standardrapportene for råbalanser.</span><span class="sxs-lookup"><span data-stu-id="d3c99-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="d3c99-106">Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.</span><span class="sxs-lookup"><span data-stu-id="d3c99-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="d3c99-107">Standardrapporter for råbalanse</span><span class="sxs-lookup"><span data-stu-id="d3c99-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="d3c99-108">Tre råbalanserapporter er tilgjengelige i Finansrapportering i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d3c99-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="d3c99-109">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="d3c99-109">Default report</span></span>                                 | <span data-ttu-id="d3c99-110">Resultat</span><span class="sxs-lookup"><span data-stu-id="d3c99-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c99-111">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d3c99-112">Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3c99-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="d3c99-113">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d3c99-114">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.</span><span class="sxs-lookup"><span data-stu-id="d3c99-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="d3c99-115">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d3c99-116">Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år.</span><span class="sxs-lookup"><span data-stu-id="d3c99-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d3c99-117">Byggeblokker</span><span class="sxs-lookup"><span data-stu-id="d3c99-117">Building blocks</span></span>
<span data-ttu-id="d3c99-118">Finansrapportene for råbalanse bruker byggeblokkene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d3c99-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="d3c99-119">Standardrapport</span><span class="sxs-lookup"><span data-stu-id="d3c99-119">Default report</span></span>                                 | <span data-ttu-id="d3c99-120">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="d3c99-120">Row definition</span></span>          | <span data-ttu-id="d3c99-121">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="d3c99-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="d3c99-122">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d3c99-123">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-123">Trial Balance - Default</span></span> | <span data-ttu-id="d3c99-124">Detaljert råbalanse – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="d3c99-125">Råbalansesammendrag – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d3c99-126">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-126">Trial Balance - Default</span></span> | <span data-ttu-id="d3c99-127">Råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="d3c99-128">Sammendrag Råbalanse Årlig – Standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d3c99-129">Råbalanse – standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-129">Trial Balance - Default</span></span> | <span data-ttu-id="d3c99-130">Årlig råbalansesammendrag – standard</span><span class="sxs-lookup"><span data-stu-id="d3c99-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="d3c99-131">Raddefinisjon</span><span class="sxs-lookup"><span data-stu-id="d3c99-131">Row definition</span></span>

<span data-ttu-id="d3c99-132">Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="d3c99-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="d3c99-133">Derfor kan alle generere rapporten uten å gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="d3c99-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="d3c99-134">Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto.</span><span class="sxs-lookup"><span data-stu-id="d3c99-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="d3c99-135">Du kan endre raddefinisjonen slik at den inneholder flere detaljer.</span><span class="sxs-lookup"><span data-stu-id="d3c99-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="d3c99-136">Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d3c99-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="d3c99-137">Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="d3c99-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="d3c99-138">Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="d3c99-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="d3c99-139">Du skal bruke **Hovedkonto** for denne raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="d3c99-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="d3c99-140">Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3c99-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="d3c99-141">Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="d3c99-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d3c99-142">Kolonnedefinisjon</span><span class="sxs-lookup"><span data-stu-id="d3c99-142">Column definition</span></span>

<span data-ttu-id="d3c99-143">Hver rapport for råbalanse bruker en annen kolonnedefinisjon.</span><span class="sxs-lookup"><span data-stu-id="d3c99-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="d3c99-144">Disse kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.</span><span class="sxs-lookup"><span data-stu-id="d3c99-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d3c99-145">**Detaljert råbalanse – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="d3c99-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="d3c99-146">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="d3c99-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3c99-147">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="d3c99-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3c99-148">**ATTR (3)** – Attributter:</span><span class="sxs-lookup"><span data-stu-id="d3c99-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="d3c99-149">Transaksjonsdato</span><span class="sxs-lookup"><span data-stu-id="d3c99-149">Transaction Date</span></span>
        -   <span data-ttu-id="d3c99-150">Bilag</span><span class="sxs-lookup"><span data-stu-id="d3c99-150">Voucher</span></span>
        -   <span data-ttu-id="d3c99-151">Journalbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="d3c99-151">Journal Description</span></span>
    -   <span data-ttu-id="d3c99-152">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="d3c99-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d3c99-153">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="d3c99-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d3c99-154">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="d3c99-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="d3c99-155">**Råbalansesammendrag – standard kolonnetyper:**</span><span class="sxs-lookup"><span data-stu-id="d3c99-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="d3c99-156">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="d3c99-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3c99-157">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="d3c99-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3c99-158">**ATTR** – Et attributt:</span><span class="sxs-lookup"><span data-stu-id="d3c99-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="d3c99-159">Bilag</span><span class="sxs-lookup"><span data-stu-id="d3c99-159">Voucher</span></span>
    -   <span data-ttu-id="d3c99-160">**FD** – Økonomiske data for starsaldo</span><span class="sxs-lookup"><span data-stu-id="d3c99-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="d3c99-161">**FD** – Økonomiske data som inneholder bare debet</span><span class="sxs-lookup"><span data-stu-id="d3c99-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d3c99-162">**FD** – Økonomiske data som inneholder bare kredit</span><span class="sxs-lookup"><span data-stu-id="d3c99-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d3c99-163">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="d3c99-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d3c99-164">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="d3c99-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="d3c99-165">**Årlig råbalansesammendrag – standard:**</span><span class="sxs-lookup"><span data-stu-id="d3c99-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="d3c99-166">**ACCT** – Kontokoder</span><span class="sxs-lookup"><span data-stu-id="d3c99-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3c99-167">**DESC** – Beskrivelsen fra raddefinisjonen.</span><span class="sxs-lookup"><span data-stu-id="d3c99-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3c99-168">**ATTR** – Et attributt</span><span class="sxs-lookup"><span data-stu-id="d3c99-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="d3c99-169">Bilag</span><span class="sxs-lookup"><span data-stu-id="d3c99-169">Voucher</span></span>
    -   <span data-ttu-id="d3c99-170">**FD** – Økonomiske data for startsaldo for inneværende år</span><span class="sxs-lookup"><span data-stu-id="d3c99-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="d3c99-171">**FD** Økonomiske data som inneholder bare debet for inneværende år</span><span class="sxs-lookup"><span data-stu-id="d3c99-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="d3c99-172">**FD** – Økonomiske data som inneholder bare kredit for inneværende år</span><span class="sxs-lookup"><span data-stu-id="d3c99-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="d3c99-173">**CALC** – Nettodifferansen</span><span class="sxs-lookup"><span data-stu-id="d3c99-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d3c99-174">**CALC** – Avslutningssaldo</span><span class="sxs-lookup"><span data-stu-id="d3c99-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="d3c99-175">**FD** – Økonomiske data som inneholder bare debet for forrige år</span><span class="sxs-lookup"><span data-stu-id="d3c99-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="d3c99-176">**FD** – Økonomiske data som inneholder bare kredit for forrige år</span><span class="sxs-lookup"><span data-stu-id="d3c99-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="d3c99-177">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d3c99-177">Additional resources</span></span>
--------

[<span data-ttu-id="d3c99-178">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="d3c99-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d3c99-179">Vise finansrapporter</span><span class="sxs-lookup"><span data-stu-id="d3c99-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d3c99-180">Blogg for Dynamics-finansrapportering</span><span class="sxs-lookup"><span data-stu-id="d3c99-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



