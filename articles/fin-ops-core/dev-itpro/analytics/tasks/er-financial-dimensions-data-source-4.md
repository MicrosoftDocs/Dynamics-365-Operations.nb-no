---
title: ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)
description: Dette emnet beskriver hvordan du konfigurerer en ER-modell (Elektronisk rapportering) for å bruke finansdimensjoner som en datakilde for ER-rapporter. (Del 4)
author: NickSelin
ms.date: 05/27/2020
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
ms.openlocfilehash: 4a06936da71d7b05f312a99c8c11d148403d29c3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752394"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="4342d-104">ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)</span><span class="sxs-lookup"><span data-stu-id="4342d-104">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4342d-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="4342d-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="4342d-106">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="4342d-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="4342d-107">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten).</span><span class="sxs-lookup"><span data-stu-id="4342d-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="4342d-108">Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4342d-108">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="4342d-109">Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="4342d-109">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="4342d-110">Kjøre rapport</span><span class="sxs-lookup"><span data-stu-id="4342d-110">Run report</span></span>
1. <span data-ttu-id="4342d-111">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="4342d-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4342d-112">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="4342d-112">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4342d-113">Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="4342d-113">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="4342d-114">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="4342d-114">Click Run.</span></span>
<span data-ttu-id="4342d-115">![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="4342d-115">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="4342d-116">Angi eller velg en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="4342d-116">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="4342d-117">Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende informasjon: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="4342d-117">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="4342d-119">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="4342d-119">Expand the Records to include section.</span></span>
7. <span data-ttu-id="4342d-120">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="4342d-120">Click Filter.</span></span>
8. <span data-ttu-id="4342d-121">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="4342d-121">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="4342d-122">Skriv inn 00057 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="4342d-122">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="4342d-123">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="4342d-123">Click OK.</span></span>
11. <span data-ttu-id="4342d-124">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="4342d-124">Click OK.</span></span>
<span data-ttu-id="4342d-125">![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="4342d-125">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="4342d-126">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="4342d-126">Review the generated output.</span></span> <span data-ttu-id="4342d-127">For hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="4342d-127">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="4342d-128">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.</span><span class="sxs-lookup"><span data-stu-id="4342d-128">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]