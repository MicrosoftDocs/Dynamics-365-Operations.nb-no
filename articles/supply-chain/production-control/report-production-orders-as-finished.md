---
title: Rapportere produksjonsordre som ferdigstilt
description: "Rapportere som ferdigstilt er et produksjonsstadium. På dette stadiet blir et ferdigstilt produkt rapportert og flyttet fra produksjonsordren til lageret."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 80a882e51332d87835bdfb41a1bb1fcda2471f02
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="report-production-orders-as-finished"></a><span data-ttu-id="40569-104">Rapportere produksjonsordre som ferdigstilt</span><span class="sxs-lookup"><span data-stu-id="40569-104">Report production orders as finished</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="40569-105">Rapportere som ferdigstilt er et produksjonsstadium.</span><span class="sxs-lookup"><span data-stu-id="40569-105">Report as finished is a production stage.</span></span> <span data-ttu-id="40569-106">På dette stadiet blir et ferdigstilt produkt rapportert og flyttet fra produksjonsordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="40569-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="40569-107">Når et antall av ferdigvarene rapporteres som ferdig i en produksjonsordre, oppdateres antallet som beholdning på lageret.</span><span class="sxs-lookup"><span data-stu-id="40569-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="40569-108">Delvise antall for det opprinnelig planlagte ordreantallet kan rapporteres som fullført.</span><span class="sxs-lookup"><span data-stu-id="40569-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="40569-109">Det er også mulig å rapportere antall feil med en tilknyttet feilårsak når antall rapporteres som ferdig.</span><span class="sxs-lookup"><span data-stu-id="40569-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="40569-110">Når produksjonsordren når stadiet Ferdigmeldt, angir det at ingen flere antall skal rapporteres for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="40569-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="40569-111">Følgende kjennetegn er også knyttet til **Rapporter som fullført**-prosessen:</span><span class="sxs-lookup"><span data-stu-id="40569-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="40569-112">Det er mulig å definere forbruk av råvarer og tiden som er proporsjonal med rapportert antall (rensing)</span><span class="sxs-lookup"><span data-stu-id="40569-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="40569-113">Plasseringsarbeid kan genereres for varer som er aktivert for lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="40569-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="40569-114">Planlagt eller standard kostverdi for de ferdige varene kan defineres for å bli rapportert til finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="40569-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="40569-115">En kvalitetsordre kan opprettes for det rapporterte antallet basert på oppsettet for en kvalitetstilknytning.</span><span class="sxs-lookup"><span data-stu-id="40569-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="40569-116">Antallet rapporteres til utleveringsstedet.</span><span class="sxs-lookup"><span data-stu-id="40569-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="40569-117">Lagerarbeid blir deretter generert for å flytte antallet fra utleveringsstedet til det endelige målet som er definert av lokasjonsdirektivet for plasseringsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="40569-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="40569-118">En kvalitetsordre kan opprettes når en produksjonsordre er rapportert som fullført, hvis en kvalitetstilknytning er definert.</span><span class="sxs-lookup"><span data-stu-id="40569-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="40569-119">Angi en produksjonsordre som Ferdigmelding</span><span class="sxs-lookup"><span data-stu-id="40569-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="40569-120">Du kan sette en produksjonsordre til **Ferdigmeld** ved hjelp av standard oppdateringsfunksjonen for produksjonsordre eller via rute- og jobbkortjournaler eller via journalen **Ferdigmeld**.</span><span class="sxs-lookup"><span data-stu-id="40569-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="40569-121">Du kan også oppdatere stadiet til **Ferdigmeld** via sidene for jobbkortterminalen og jobbkortenheten når du rapporterer om den siste jobben i produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="40569-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="40569-122">Til slutt kan du aktivere alternativet **Ferdigmeld** som en prosess for den håndholdte lagerenhetsløsningen.</span><span class="sxs-lookup"><span data-stu-id="40569-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  




