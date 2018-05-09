---
title: Frigi en produksjonsordre
description: "Denne fremgangsmåten viser hvordan du frigir en produksjonsordre."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77dc4f1908836498568251c75efde930b4f88fcf
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="release-a-production-order"></a><span data-ttu-id="9921c-103">Frigi en produksjonsordre</span><span class="sxs-lookup"><span data-stu-id="9921c-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9921c-104">Denne fremgangsmåten viser hvordan du frigir en produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="9921c-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="9921c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="9921c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9921c-106">Dette er den fjerde fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="9921c-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="9921c-107">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="9921c-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="9921c-108">Velg en produksjonsordre som har statusen Planlagt, i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9921c-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="9921c-109">Klikk Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9921c-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="9921c-110">Klikk Frigi.</span><span class="sxs-lookup"><span data-stu-id="9921c-110">Click Release.</span></span>
    * <span data-ttu-id="9921c-111">På denne siden kan du kontrollere frigivelsen av det merkede området for produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="9921c-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="9921c-112">Klikk Velg hvis du vil legge til ordrer.</span><span class="sxs-lookup"><span data-stu-id="9921c-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="9921c-113">Frigivelsestrinnet angir når produksjonsordren frigis til produksjon-Shop Floor, slik at Shop Floor-operatørene kan rapportere fremdrift om produksjonsjobbene.</span><span class="sxs-lookup"><span data-stu-id="9921c-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="9921c-114">Produksjonspapirer som inneholder relevant informasjon om behandling av jobbene, kan utstedes.</span><span class="sxs-lookup"><span data-stu-id="9921c-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="9921c-115">Lagerarbeidet for plukking av råvarer genereres for varer som er definert for lagerprosessen.</span><span class="sxs-lookup"><span data-stu-id="9921c-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="9921c-116">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="9921c-116">Click the General tab.</span></span>
    * <span data-ttu-id="9921c-117">Velg hvilke produksjonsrapporter som skal skrives ut.</span><span class="sxs-lookup"><span data-stu-id="9921c-117">Select which production reports should be printed.</span></span> <span data-ttu-id="9921c-118">Jobbkortrapporten skriver ut en side for hver planlagte jobb, og krever at produksjonsordren planlegges på jobbnivået.</span><span class="sxs-lookup"><span data-stu-id="9921c-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="9921c-119">Rapporten inneholder informasjon om planlagt start- og sluttidspunkt, antallet som skal produseres, og hvilken ressurs som behandler jobben.</span><span class="sxs-lookup"><span data-stu-id="9921c-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="9921c-120">Rutejobbrapporten samler inn samme informasjon på samme side, men skriver ikke ut en side for hver jobb.</span><span class="sxs-lookup"><span data-stu-id="9921c-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="9921c-121">Rutekortrapporten viser bare operasjoner, men ikke jobbene.</span><span class="sxs-lookup"><span data-stu-id="9921c-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="9921c-122">Denne rapporten krever derfor ikke finplanlegging, men kan brukes når produksjonsordrer er planlagt på operasjonsnivået.</span><span class="sxs-lookup"><span data-stu-id="9921c-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="9921c-123">Klikk i boksen Skriv ut rutekort.</span><span class="sxs-lookup"><span data-stu-id="9921c-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="9921c-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9921c-124">Click OK.</span></span>
7. <span data-ttu-id="9921c-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9921c-125">Close the page.</span></span>

