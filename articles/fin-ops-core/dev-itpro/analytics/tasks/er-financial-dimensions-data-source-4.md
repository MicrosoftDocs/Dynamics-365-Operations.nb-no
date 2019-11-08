---
title: ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27498fb8290fa18abd64d7f306e9c0bf4713a72f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550140"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="86d34-103">ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)</span><span class="sxs-lookup"><span data-stu-id="86d34-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86d34-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="86d34-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="86d34-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="86d34-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="86d34-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten).</span><span class="sxs-lookup"><span data-stu-id="86d34-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="86d34-107">Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="86d34-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="86d34-108">Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="86d34-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="86d34-109">Kjøre rapport</span><span class="sxs-lookup"><span data-stu-id="86d34-109">Run report</span></span>
1. <span data-ttu-id="86d34-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="86d34-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="86d34-111">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="86d34-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="86d34-112">Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="86d34-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="86d34-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="86d34-113">Click Run.</span></span>
5. <span data-ttu-id="86d34-114">I Dimensjonsnavn-feltet skriver du inn eller velger en verdi.</span><span class="sxs-lookup"><span data-stu-id="86d34-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="86d34-115">Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="86d34-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="86d34-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="86d34-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="86d34-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="86d34-117">Click Filter.</span></span>
8. <span data-ttu-id="86d34-118">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="86d34-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="86d34-119">Skriv inn 00057 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="86d34-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="86d34-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="86d34-120">Click OK.</span></span>
11. <span data-ttu-id="86d34-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="86d34-121">Click OK.</span></span>
    * <span data-ttu-id="86d34-122">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="86d34-122">Review the generated output.</span></span> <span data-ttu-id="86d34-123">Legg merke til at for hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="86d34-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="86d34-124">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.</span><span class="sxs-lookup"><span data-stu-id="86d34-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  

