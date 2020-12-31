---
title: ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4596f7d7789ea44d49d7e7f273e4a52ee38dd90f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684529"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a><span data-ttu-id="82358-103">ER Bruke vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk (del 2 - Kjøre format)</span><span class="sxs-lookup"><span data-stu-id="82358-103">ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 2 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82358-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="82358-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="82358-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="82358-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="82358-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke vannrett utvidbare områder for legge til kolonner i Excel-rapporter dynamisk (del 1: Utforme format)".</span><span class="sxs-lookup"><span data-stu-id="82358-106">To complete these steps, you must first complete the steps in the "ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)" procedure.</span></span>

<span data-ttu-id="82358-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="82358-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="82358-108">Søke etter opprettet format</span><span class="sxs-lookup"><span data-stu-id="82358-108">Find created format</span></span>
1. <span data-ttu-id="82358-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="82358-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="82358-110">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="82358-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="82358-111">Velg Eksempelmodell for finansdimensjoner\Eksempelrapport med vannrett utvidbare områder i treet.</span><span class="sxs-lookup"><span data-stu-id="82358-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="82358-112">Kjøre format for å opprette Excel-utdata</span><span class="sxs-lookup"><span data-stu-id="82358-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="82358-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="82358-113">Click Run.</span></span>
2. <span data-ttu-id="82358-114">I Dimensjonsnavn-feltet skriver du inn BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="82358-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="82358-115">Angi eller velg en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="82358-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="82358-116">Hvis du vil velge alle dimensjoner for gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="82358-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="82358-117">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="82358-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="82358-118">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="82358-118">Click Filter.</span></span>
5. <span data-ttu-id="82358-119">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="82358-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="82358-120">Skriv inn 00057..00058 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="82358-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="82358-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="82358-121">00057..00058</span></span>  
7. <span data-ttu-id="82358-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="82358-122">Click OK.</span></span>
8. <span data-ttu-id="82358-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="82358-123">Click OK.</span></span>
    * <span data-ttu-id="82358-124">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="82358-124">Review the generated output.</span></span> <span data-ttu-id="82358-125">Legg merke til at den nylig opprettede Excel-filen inneholder samme antall kolonner som ble valgt for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="82358-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="82358-126">Rapporthodet i disse kolonnene representerer finansdimensjonenes navn.</span><span class="sxs-lookup"><span data-stu-id="82358-126">The report header in those columns represents financial dimensions' names.</span></span> <span data-ttu-id="82358-127">Linjene til transaksjonene i disse kolonnene representerer finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="82358-127">The transactions' lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="82358-128">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.</span><span class="sxs-lookup"><span data-stu-id="82358-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

