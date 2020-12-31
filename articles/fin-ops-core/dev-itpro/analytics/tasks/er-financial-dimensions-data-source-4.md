---
title: ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: fb7f49310aa25ff7c17ab4bcd50e1842be84fe2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684745"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a><span data-ttu-id="82c81-103">ER Bruke finansdimensjoner som en datakilde (del 4 - Kjøre rapporten)</span><span class="sxs-lookup"><span data-stu-id="82c81-103">ER Use financial dimensions as a data source (Part 4 - Run the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82c81-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="82c81-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="82c81-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="82c81-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="82c81-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten).</span><span class="sxs-lookup"><span data-stu-id="82c81-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 3: Design the report)" procedure.</span></span> <span data-ttu-id="82c81-107">Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="82c81-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="82c81-108">Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="82c81-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="82c81-109">Kjøre rapport</span><span class="sxs-lookup"><span data-stu-id="82c81-109">Run report</span></span>
1. <span data-ttu-id="82c81-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="82c81-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="82c81-111">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="82c81-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="82c81-112">Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="82c81-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="82c81-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="82c81-113">Click Run.</span></span>
<span data-ttu-id="82c81-114">![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run1.png)</span><span class="sxs-lookup"><span data-stu-id="82c81-114">![ER configurations page](../media/er-financial-dimensions-guides-run1.png)</span></span>
5. <span data-ttu-id="82c81-115">Angi eller velg en verdi i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="82c81-115">In the Dimension name field, enter or select a value.</span></span>
    * <span data-ttu-id="82c81-116">Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende informasjon: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="82c81-116">To select all dimensions in the current company, enter the following information:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run2.png)
6. <span data-ttu-id="82c81-118">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="82c81-118">Expand the Records to include section.</span></span>
7. <span data-ttu-id="82c81-119">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="82c81-119">Click Filter.</span></span>
8. <span data-ttu-id="82c81-120">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="82c81-120">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="82c81-121">Skriv inn 00057 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="82c81-121">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="82c81-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="82c81-122">Click OK.</span></span>
11. <span data-ttu-id="82c81-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="82c81-123">Click OK.</span></span>
<span data-ttu-id="82c81-124">![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run3.png)</span><span class="sxs-lookup"><span data-stu-id="82c81-124">![ER configurations page](../media/er-financial-dimensions-guides-run3.png)</span></span>
    * <span data-ttu-id="82c81-125">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="82c81-125">Review the generated output.</span></span> <span data-ttu-id="82c81-126">For hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="82c81-126">For each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="82c81-127">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten.</span><span class="sxs-lookup"><span data-stu-id="82c81-127">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this instance.</span></span>  
![Siden ER-konfigurasjoner](../media/er-financial-dimensions-guides-run4.png)
