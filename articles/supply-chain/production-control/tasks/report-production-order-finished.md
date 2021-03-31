---
title: Rapportere en produksjonsordre som avsluttet
description: Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4848093bd4901d3aa801fc09d7ee3e79d65ebb0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204469"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="07863-103">Rapportere en produksjonsordre som avsluttet</span><span class="sxs-lookup"><span data-stu-id="07863-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07863-104">Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.</span><span class="sxs-lookup"><span data-stu-id="07863-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="07863-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="07863-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07863-106">Dette er den sjette fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="07863-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="07863-107">Rapportere en produksjonsordre som avsluttet</span><span class="sxs-lookup"><span data-stu-id="07863-107">Report a production order as finished</span></span>
1. <span data-ttu-id="07863-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="07863-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="07863-109">Velg en produksjonsordre med statusen Startet.</span><span class="sxs-lookup"><span data-stu-id="07863-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="07863-110">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="07863-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="07863-111">Klikk på Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="07863-111">Click Report as finished.</span></span>
    * <span data-ttu-id="07863-112">På denne siden kan du bekrefte antallet av det ferdige produktet som skal rapporteres som fullført.</span><span class="sxs-lookup"><span data-stu-id="07863-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="07863-113">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="07863-113">Click the General tab.</span></span>
5. <span data-ttu-id="07863-114">Angi Antall korrekte til "18".</span><span class="sxs-lookup"><span data-stu-id="07863-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="07863-115">Angi Antall feil til 2.</span><span class="sxs-lookup"><span data-stu-id="07863-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="07863-116">Velg "Materiale" i Feilårsak-feltet.</span><span class="sxs-lookup"><span data-stu-id="07863-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="07863-117">Merk av eller fjern merket i avmerkingsboksen Avslutt jobb.</span><span class="sxs-lookup"><span data-stu-id="07863-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="07863-118">Merk av eller fjern merket i boksen Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="07863-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="07863-119">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="07863-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="07863-120">Verifisere ferdigmeldingsjournalen</span><span class="sxs-lookup"><span data-stu-id="07863-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="07863-121">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="07863-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="07863-122">Klikk på Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="07863-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="07863-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="07863-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="07863-124">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="07863-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="07863-125">Ferdigmeldingsjournalen er postert.</span><span class="sxs-lookup"><span data-stu-id="07863-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="07863-126">Hvis du vil foreta justeringer i journalen, kan du manuelt opprette en ny journal der du kan gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="07863-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]