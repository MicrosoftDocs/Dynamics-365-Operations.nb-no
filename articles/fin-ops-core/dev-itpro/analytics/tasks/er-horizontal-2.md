---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)
description: Dette emnet beskriver hvordan du konfigurerer et ER-format (Elektronisk rapportering) slik at det genererer rapporter som OPENXML-regnearkfiler (Excel). (Del 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0b8c997549bca2cae5500c926ccba916a473b5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569539"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="752e9-104">ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)</span><span class="sxs-lookup"><span data-stu-id="752e9-104">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="752e9-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="752e9-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="752e9-106">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="752e9-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="752e9-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke vannrett utvidbare områder for legge til kolonner i Excel-rapporter dynamisk (del 1: Utforme format)".</span><span class="sxs-lookup"><span data-stu-id="752e9-107">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="752e9-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="752e9-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="752e9-109">Søke etter opprettet format</span><span class="sxs-lookup"><span data-stu-id="752e9-109">Find created format</span></span>
1. <span data-ttu-id="752e9-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="752e9-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="752e9-111">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="752e9-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="752e9-112">Velg Eksempelmodell for finansdimensjoner\Eksempelrapport med vannrett utvidbare områder i treet.</span><span class="sxs-lookup"><span data-stu-id="752e9-112">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="752e9-113">Kjøre format for å opprette Excel-utdata</span><span class="sxs-lookup"><span data-stu-id="752e9-113">Execute format to create Excel output</span></span>
1. <span data-ttu-id="752e9-114">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="752e9-114">Click Run.</span></span>
2. <span data-ttu-id="752e9-115">I Dimensjonsnavn-feltet skriver du inn BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="752e9-115">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="752e9-116">Angi eller velg en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="752e9-116">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="752e9-117">Hvis du vil velge alle dimensjoner for gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="752e9-117">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="752e9-118">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="752e9-118">Expand the Records to include section.</span></span>
4. <span data-ttu-id="752e9-119">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="752e9-119">Click Filter.</span></span>
5. <span data-ttu-id="752e9-120">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="752e9-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="752e9-121">Skriv inn 00057..00058 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="752e9-121">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="752e9-122">00057..00058</span><span class="sxs-lookup"><span data-stu-id="752e9-122">00057..00058</span></span>  
7. <span data-ttu-id="752e9-123">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="752e9-123">Click OK.</span></span>
8. <span data-ttu-id="752e9-124">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="752e9-124">Click OK.</span></span>
    * <span data-ttu-id="752e9-125">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="752e9-125">Review the generated output.</span></span> <span data-ttu-id="752e9-126">Legg merke til at den nylig opprettede Excel-filen inneholder samme antall kolonner som ble valgt for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="752e9-126">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="752e9-127">Rapporthodet i disse kolonnene representerer finansdimensjonenes navn.</span><span class="sxs-lookup"><span data-stu-id="752e9-127">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="752e9-128">Linjene til transaksjonene i disse kolonnene representerer finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="752e9-128">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="752e9-129">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.</span><span class="sxs-lookup"><span data-stu-id="752e9-129">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]