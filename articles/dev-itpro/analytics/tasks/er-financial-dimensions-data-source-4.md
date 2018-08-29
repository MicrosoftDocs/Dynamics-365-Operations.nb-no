--- 
title: "Kjøre rapporter som bruker finansdimensjoner som datakilder"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6569f9b97d5d15bf74b8b3882bf4bab50970dd0f
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="run-reports-that-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="25f66-103">Kjøre rapporter som bruker finansdimensjoner som datakilder</span><span class="sxs-lookup"><span data-stu-id="25f66-103">Run reports that use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25f66-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="25f66-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="25f66-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="25f66-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="25f66-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten).</span><span class="sxs-lookup"><span data-stu-id="25f66-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="25f66-107">Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="25f66-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="25f66-108">Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="25f66-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="25f66-109">Kjøre rapport</span><span class="sxs-lookup"><span data-stu-id="25f66-109">Run report</span></span>
1. <span data-ttu-id="25f66-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="25f66-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="25f66-111">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="25f66-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="25f66-112">Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="25f66-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="25f66-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="25f66-113">Click Run.</span></span>
5. <span data-ttu-id="25f66-114">I Dimensjonsnavn-feltet skriver du inn eller velger en verdi.</span><span class="sxs-lookup"><span data-stu-id="25f66-114">In the Dimension name field, In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="25f66-115">Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="25f66-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="25f66-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="25f66-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="25f66-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="25f66-117">Click Filter.</span></span>
8. <span data-ttu-id="25f66-118">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="25f66-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="25f66-119">Skriv inn 00057 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="25f66-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="25f66-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="25f66-120">Click OK.</span></span>
11. <span data-ttu-id="25f66-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="25f66-121">Click OK.</span></span>
    * <span data-ttu-id="25f66-122">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="25f66-122">Review the generated output.</span></span> <span data-ttu-id="25f66-123">Legg merke til at for hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="25f66-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="25f66-124">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten av Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25f66-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations instance.</span></span>  


