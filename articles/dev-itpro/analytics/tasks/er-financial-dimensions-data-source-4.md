--- 
title: "Kjøre en rapport som bruker finansdimensjoner som en datakilde for elektronisk rapportering (ER)"
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="e976a-103">Kjøre en rapport som bruker finansdimensjoner som en datakilde for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="e976a-103">Run a report that uses financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e976a-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere en elektronisk rapportering (ER)-modell til å bruke finansdimensjoner som datakilde for ER-rapporter.</span><span class="sxs-lookup"><span data-stu-id="e976a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e976a-105">Denne fremgangsmåten kan utføres i firmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="e976a-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="e976a-106">For å fullføre disse trinnene, må du først fullføre trinnene i prosedyren "ER Bruke finansdimensjoner som datakilde (del 3: Utforme rapporten).</span><span class="sxs-lookup"><span data-stu-id="e976a-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 3: Design the report)” procedure.</span></span> <span data-ttu-id="e976a-107">Du må også konfigurere standard dokumenttyper på siden Parametere for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="e976a-107">You must also configure default document types on the Electronic reporting parameters page.</span></span> <span data-ttu-id="e976a-108">Standard dokumenttyper angis også når du laster ned og importerer en ER-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="e976a-108">Default document types are also set when you download and import any ER configuration.</span></span> 


## <a name="run-report"></a><span data-ttu-id="e976a-109">Kjøre rapport</span><span class="sxs-lookup"><span data-stu-id="e976a-109">Run report</span></span>
1. <span data-ttu-id="e976a-110">Gå til Organisasjonsstyring > Elektronisk rapportering > Konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="e976a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e976a-111">Utvid Eksempelmodell for finansdimensjoner i treet.</span><span class="sxs-lookup"><span data-stu-id="e976a-111">In the tree, expand 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="e976a-112">Velg Eksempelmodell for finansdimensjoner\Finansjournalrapport i treet.</span><span class="sxs-lookup"><span data-stu-id="e976a-112">In the tree, select 'Financial dimensions sample model\Ledger journal report'.</span></span>
4. <span data-ttu-id="e976a-113">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="e976a-113">Click Run.</span></span>
5. <span data-ttu-id="e976a-114">I Dimensjonsnavn-feltet skriver du inn eller velger en verdi.</span><span class="sxs-lookup"><span data-stu-id="e976a-114">In the Dimension name field, In the Dimension name field, enter or select a value..</span></span>
    * <span data-ttu-id="e976a-115">Hvis du vil velge alle dimensjoner i gjeldende firma, kan du angi følgende: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span><span class="sxs-lookup"><span data-stu-id="e976a-115">To select all dimensions in the current company, enter the following:  BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project</span></span>  
6. <span data-ttu-id="e976a-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e976a-116">Expand the Records to include section.</span></span>
7. <span data-ttu-id="e976a-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="e976a-117">Click Filter.</span></span>
8. <span data-ttu-id="e976a-118">Merk raden for Finansjournal-tabellen og Journalpartinummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="e976a-118">Select the row for the Ledger journal table and the Journal batch number field.</span></span>
9. <span data-ttu-id="e976a-119">Skriv inn 00057 i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="e976a-119">In the Criteria field, type '00057'.</span></span>
10. <span data-ttu-id="e976a-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e976a-120">Click OK.</span></span>
11. <span data-ttu-id="e976a-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e976a-121">Click OK.</span></span>
    * <span data-ttu-id="e976a-122">Se gjennom de genererte utdataene.</span><span class="sxs-lookup"><span data-stu-id="e976a-122">Review the generated output.</span></span> <span data-ttu-id="e976a-123">Legg merke til at for hver transaksjon for det valgte partiet, presenteres finansdimensjonene fra det tilsvarende dimensjonssettet.</span><span class="sxs-lookup"><span data-stu-id="e976a-123">Note that for each transaction of the selected batch, the financial dimensions from the corresponding dimensions set are presented.</span></span> <span data-ttu-id="e976a-124">Kjør denne rapporten, og velg ulike dimensjoner for å se at rapporten ikke er avhengig av antall valgte dimensjoner eller antall dimensjoner som er konfigurert for denne forekomsten av Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="e976a-124">Run this report and select different dimensions to see that the report is not dependent on the number of selected dimensions or the number of dimensions configured for this Dynamics 365 for Finance and Operations, Enterprise edition instance.</span></span>  


