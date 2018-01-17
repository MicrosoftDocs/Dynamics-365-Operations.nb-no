---
title: "Spore en vare eller råvare"
description: "Denne fremgangsmåten beskriver hvordan du bruker varesporing til å identifisere hvor varer eller råmaterialer er brukt, eller er i bruk."
author: pjacobse
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 9054455a2a48e851d085a1b1ff8040261ce17672
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="1cd24-103">Spore en vare eller råvare</span><span class="sxs-lookup"><span data-stu-id="1cd24-103">Trace an item or raw material</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cd24-104">Denne fremgangsmåten beskriver hvordan du bruker varesporing til å identifisere hvor varer eller råmaterialer er brukt, eller er i bruk.</span><span class="sxs-lookup"><span data-stu-id="1cd24-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="1cd24-105">Du kan identifisere en vare, spore den tilbake til kilden, og deretter spore fremover gjennom produksjon og salg av det ferdige produktet med denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="1cd24-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="1cd24-106">Prosessen kan brukes til å undersøke kundene berørt, salgsordrene påvirket og mer.</span><span class="sxs-lookup"><span data-stu-id="1cd24-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="1cd24-107">Denne prosedyren bruker demonstrasjonsdatafirmaet USP2.</span><span class="sxs-lookup"><span data-stu-id="1cd24-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="1cd24-108">Spore en vare bakover ved hjelp av et kjent partinummer</span><span class="sxs-lookup"><span data-stu-id="1cd24-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="1cd24-109">Gå til Lagerstyring > Forespørsler og rapporter > Sporingsdimensjoner > Varesporing.</span><span class="sxs-lookup"><span data-stu-id="1cd24-109">Go to Inventory management > Inquiries and reports > Tracking dimensions > Item tracing.</span></span>
2. <span data-ttu-id="1cd24-110">Velg P9100 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="1cd24-110">In the Item number field, select P9100.</span></span>
3. <span data-ttu-id="1cd24-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1cd24-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1cd24-112">Velg "Bakover" i feltet Forover eller bakover.</span><span class="sxs-lookup"><span data-stu-id="1cd24-112">In the Forward or backward field, select 'Backward'.</span></span>
5. <span data-ttu-id="1cd24-113">Velg som-12-344-01 i Partinummer-feltet</span><span class="sxs-lookup"><span data-stu-id="1cd24-113">In the Batch number field, select as-12-344-01.</span></span>
6. <span data-ttu-id="1cd24-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="1cd24-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="1cd24-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1cd24-115">Click OK.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="1cd24-116">Identifisere en vare, spore den fremover og gjøre en analyse</span><span class="sxs-lookup"><span data-stu-id="1cd24-116">Identify an item, trace it forward, and make an analysis</span></span>
    * <span data-ttu-id="1cd24-117">Toppnoden i treet representerer beholdningen for den valgte varen og partiet.</span><span class="sxs-lookup"><span data-stu-id="1cd24-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="1cd24-118">Du må vise nodene i treet for å finne varen som fremoversporingen skal utføres på.</span><span class="sxs-lookup"><span data-stu-id="1cd24-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="1cd24-119">I treet viser du nodene som er beskrevet nedenfor, og velger deretter den siste noden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    * <span data-ttu-id="1cd24-120">Vis: P9100 / 1 / 10 / som-12-344-01 ● 2 keg ● 7,00 gal \P9100 ● Plukket ● Salgsordre 000072 ● 12/22/2015 ● -1 keg ● -4,00 gal ● Område = 1, Lager=10, Partinummer=som-12-344-01 \P9100 ● Produksjon B-000050 ● 12/9/2015● 7 keg ● 27,00 gal ● Område=1, Lager=10, Partinummer=som-12-344-01 ● Koprodukter: P9101, og velg deretter noden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="1cd24-121">I treet viser du noden som er beskrevet nedenfor, og velger deretter denne noden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    * <span data-ttu-id="1cd24-122">Fra og med noden som du akkurat har valgtviser du M9103 ● Produksjonslinje B-000050 ● 12/9/2015 ● -160,00 lb ● Størrelse=70, Farge=OK, Område=1, Lager=10, Partinummer=App01, og velg deretter denne noden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="1cd24-123">Klikk Spor fra node.</span><span class="sxs-lookup"><span data-stu-id="1cd24-123">Click Trace from node.</span></span>
4. <span data-ttu-id="1cd24-124">Klikk Forover.</span><span class="sxs-lookup"><span data-stu-id="1cd24-124">Click Forward.</span></span>
5. <span data-ttu-id="1cd24-125">Klikk Sporing i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1cd24-125">On the Action Pane, click Tracing.</span></span>
    * <span data-ttu-id="1cd24-126">Det finnes flere sporingsalternativer som gir informasjon om hvilke kunder som berøres av varen som du sporer og salgsordrene som er knyttet til varen som har blitt og ikke er levert.</span><span class="sxs-lookup"><span data-stu-id="1cd24-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="1cd24-127">Klikk Kunder.</span><span class="sxs-lookup"><span data-stu-id="1cd24-127">Click Customers.</span></span>
7. <span data-ttu-id="1cd24-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-128">Close the page.</span></span>
8. <span data-ttu-id="1cd24-129">Klikk Sporing i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1cd24-129">On the Action Pane, click Tracing.</span></span>
9. <span data-ttu-id="1cd24-130">Klikk Leverte salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="1cd24-130">Click Shipped sales orders.</span></span>
10. <span data-ttu-id="1cd24-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="1cd24-131">Close the page.</span></span>

