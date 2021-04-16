---
title: Rapportere en produksjonsordre som avsluttet
description: Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9b676ffefa9fd4b8d66a5c35012630295f8a263
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828616"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="33388-103">Rapportere en produksjonsordre som avsluttet</span><span class="sxs-lookup"><span data-stu-id="33388-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33388-104">Denne fremgangsmåten viser hvordan du rapporterer en produksjonsordre som ferdig.</span><span class="sxs-lookup"><span data-stu-id="33388-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="33388-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="33388-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="33388-106">Dette er den sjette fremgangsmåten av sju som forklarer livssyklusen for produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="33388-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="33388-107">Rapportere en produksjonsordre som avsluttet</span><span class="sxs-lookup"><span data-stu-id="33388-107">Report a production order as finished</span></span>
1. <span data-ttu-id="33388-108">Gå til Produksjonskontroll > Produksjonsordrer > Alle produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="33388-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="33388-109">Velg en produksjonsordre med statusen Startet.</span><span class="sxs-lookup"><span data-stu-id="33388-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="33388-110">Klikk på Produksjonsordre i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="33388-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="33388-111">Klikk på Rapporter som fullført.</span><span class="sxs-lookup"><span data-stu-id="33388-111">Click Report as finished.</span></span>
    * <span data-ttu-id="33388-112">På denne siden kan du bekrefte antallet av det ferdige produktet som skal rapporteres som fullført.</span><span class="sxs-lookup"><span data-stu-id="33388-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="33388-113">Klikk på fanen Generelt.</span><span class="sxs-lookup"><span data-stu-id="33388-113">Click the General tab.</span></span>
5. <span data-ttu-id="33388-114">Angi Antall korrekte til "18".</span><span class="sxs-lookup"><span data-stu-id="33388-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="33388-115">Angi Antall feil til 2.</span><span class="sxs-lookup"><span data-stu-id="33388-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="33388-116">Velg "Materiale" i Feilårsak-feltet.</span><span class="sxs-lookup"><span data-stu-id="33388-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="33388-117">Merk av eller fjern merket i avmerkingsboksen Avslutt jobb.</span><span class="sxs-lookup"><span data-stu-id="33388-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="33388-118">Merk av eller fjern merket i boksen Godtar feil.</span><span class="sxs-lookup"><span data-stu-id="33388-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="33388-119">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="33388-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="33388-120">Verifisere ferdigmeldingsjournalen</span><span class="sxs-lookup"><span data-stu-id="33388-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="33388-121">Klikk på Vis i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="33388-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="33388-122">Klikk på Ferdigmeldt.</span><span class="sxs-lookup"><span data-stu-id="33388-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="33388-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="33388-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="33388-124">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="33388-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="33388-125">Ferdigmeldingsjournalen er postert.</span><span class="sxs-lookup"><span data-stu-id="33388-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="33388-126">Hvis du vil foreta justeringer i journalen, kan du manuelt opprette en ny journal der du kan gjøre endringer.</span><span class="sxs-lookup"><span data-stu-id="33388-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]