--- 
title: "Kjøre et format som bruker vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c4538bd9f8c71108e7ec8fd9da2c2b914d76f13
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports"></a><span data-ttu-id="851f2-103">Kjøre et format som bruker vannrett utvidbare områder for å legge til kolonner i Excel-rapporter dynamisk</span><span class="sxs-lookup"><span data-stu-id="851f2-103">Run a format that uses horizontally-expandable ranges to dynamically add columns in Excel reports</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="851f2-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering, kan konfigurere et elektronisk rapportering (ER)-format for å generere rapporter som OPENXML-regnearkfiler (Excel) der de påkrevde kolonnene kan opprettes dynamisk som vannrett utvidbare områder.</span><span class="sxs-lookup"><span data-stu-id="851f2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to generate reports as OPENXML worksheets (Excel) files in which the required columns can be created dynamically as horizontally expandable ranges.</span></span> <span data-ttu-id="851f2-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="851f2-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="851f2-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke vannrett utvidbare områder for legge til kolonner i Excel-rapporter dynamisk (del 1: Utforme format)".</span><span class="sxs-lookup"><span data-stu-id="851f2-106">To complete these steps, you must first complete the steps in the “ER Use horizontally expandable ranges to dynamically add columns in Excel reports (Part 1: Design format)” procedure.</span></span>

<span data-ttu-id="851f2-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="851f2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="find-created-format"></a><span data-ttu-id="851f2-108">Søke etter opprettet format</span><span class="sxs-lookup"><span data-stu-id="851f2-108">Find created format</span></span>
1. <span data-ttu-id="851f2-109">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="851f2-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="851f2-110">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="851f2-110">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="851f2-111">Velg Eksempelmodell for finansdimensjoner\Eksempelrapport med vannrett utvidbare områder i treet.</span><span class="sxs-lookup"><span data-stu-id="851f2-111">In the tree, select 'Financial dimensions sample model\Sample report with horizontally expandable ranges'.</span></span>

## <a name="execute-format-to-create-excel-output"></a><span data-ttu-id="851f2-112">Kjøre format for å opprette Excel-utdata</span><span class="sxs-lookup"><span data-stu-id="851f2-112">Execute format to create Excel output</span></span>
1. <span data-ttu-id="851f2-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="851f2-113">Click Run.</span></span>
2. <span data-ttu-id="851f2-114">I Dimensjonsnavn-feltet skriver du inn BusinessUnit;CostCenter;Department.</span><span class="sxs-lookup"><span data-stu-id="851f2-114">In the Dimension name field, type 'BusinessUnit;CostCenter;Department'.</span></span>
    * <span data-ttu-id="851f2-115">Angi eller velg en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="851f2-115">In the Dimension name field, enter or select a value.</span></span>  <span data-ttu-id="851f2-116">Hvis du vil velge alle dimensjoner for gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="851f2-116">To select all dimensions for the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
3. <span data-ttu-id="851f2-117">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="851f2-117">Expand the Records to include section.</span></span>
4. <span data-ttu-id="851f2-118">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="851f2-118">Click Filter.</span></span>
5. <span data-ttu-id="851f2-119">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="851f2-119">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
6. <span data-ttu-id="851f2-120">Skriv inn 00057..00058 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="851f2-120">In the Criteria field, type '00057..00058'.</span></span>
    * <span data-ttu-id="851f2-121">00057..00058</span><span class="sxs-lookup"><span data-stu-id="851f2-121">00057..00058</span></span>  
7. <span data-ttu-id="851f2-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="851f2-122">Click OK.</span></span>
8. <span data-ttu-id="851f2-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="851f2-123">Click OK.</span></span>
    * <span data-ttu-id="851f2-124">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="851f2-124">Review the generated output.</span></span> <span data-ttu-id="851f2-125">Legg merke til at den nylig opprettede Excel-filen inneholder samme antall kolonner som ble valgt for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="851f2-125">Note that the newly created Excel file contains the same number of columns that were selected for financial dimensions.</span></span> <span data-ttu-id="851f2-126">Rapporthodet i disse kolonnene representerer finansdimensjonenes navn.</span><span class="sxs-lookup"><span data-stu-id="851f2-126">The report header in those columns represents financial dimensions’ names.</span></span> <span data-ttu-id="851f2-127">Linjene til transaksjonene i disse kolonnene representerer finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="851f2-127">The transactions’ lines in those columns represent financial dimensions.</span></span> <span data-ttu-id="851f2-128">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten av Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="851f2-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


