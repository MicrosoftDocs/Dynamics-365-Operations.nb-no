---
title: Generere og kjøre medfølgende rapporter
description: Bruk denne oppgaveveiledningen til å kjøre medfølgende rapporter i hovedkontorer fra forskjellige arbeidsområder og forespørsels- og salgsrapporter under Detaljhandel og handel.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550076"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="1c54f-103">Generere og kjøre medfølgende rapporter</span><span class="sxs-lookup"><span data-stu-id="1c54f-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1c54f-104">Bruk denne oppgaveveiledningen til å kjøre medfølgende rapporter i hovedkontorer fra forskjellige arbeidsområder og forespørsels- og salgsrapporter under Detaljhandel og handel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="1c54f-105">Demonstrasjonsdatafirmaet USRT brukes til å opprette dette opptaket.</span><span class="sxs-lookup"><span data-stu-id="1c54f-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="1c54f-106">Denne registreringen er ment for systemansvarligrollen.</span><span class="sxs-lookup"><span data-stu-id="1c54f-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="1c54f-107">Starte rapporter fra arbeidsområder</span><span class="sxs-lookup"><span data-stu-id="1c54f-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="1c54f-108">Gå til Detaljhandel og handel > Produkter og kategorier > Kategori- og produktstyring.</span><span class="sxs-lookup"><span data-stu-id="1c54f-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="1c54f-109">Klikk pilen for å vise eller skjule delen Rapporter.</span><span class="sxs-lookup"><span data-stu-id="1c54f-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="1c54f-110">Klikk Rapport om topprodukter.</span><span class="sxs-lookup"><span data-stu-id="1c54f-110">Click Top products report.</span></span>
4. <span data-ttu-id="1c54f-111">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="1c54f-112">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="1c54f-113">Klikk rullegardinknappen i Kanal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="1c54f-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1c54f-114">Velg Contoso Retail\Contoso Retail USA\Central\Houston i treet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="1c54f-115">Viser standard organisasjonshierarki for detaljhandel for rapporteringsformål for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="1c54f-116">Gå til Organisasjonsstyring >Organisasjoner > Formål for organisasjonshierarki og velg Detaljhandelsrapportering og under Tilordnede hierarkier kontrollerer du hierarkinavnet for hvilken standardkolonne som er avmerket.</span><span class="sxs-lookup"><span data-stu-id="1c54f-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="1c54f-117">Som en del av demonstrasjonsdataene (brukes i denne oppgaveregistreringen) vil du se at Detaljhandelbutikker etter område er standard organisasjonshierarki for rapporteringsformålet for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="1c54f-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1c54f-118">Click OK.</span></span>
9. <span data-ttu-id="1c54f-119">Velg et alternativ i Vis-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="1c54f-120">Velg et alternativ i Etter-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="1c54f-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1c54f-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="1c54f-122">Start rapporter fra forespørsels- og salgsrapportene under appkoblingen Detaljhandel og handel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="1c54f-123">Gå til Detaljhandel og handel > Forespørsler og rapporter > Salgsrapporter > Rapport for kategorisalg.</span><span class="sxs-lookup"><span data-stu-id="1c54f-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="1c54f-124">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="1c54f-125">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="1c54f-126">Klikk rullegardinknappen i Kanal-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="1c54f-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1c54f-127">Velg Contoso Retail\Contoso Retail USA\West\Seattle i treet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="1c54f-128">Viser standard organisasjonshierarki for detaljhandel for rapporteringsformål for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="1c54f-129">Gå til Organisasjonsstyring >Organisasjoner > Formål for organisasjonshierarki og velg Detaljhandelsrapportering og under Tilordnede hierarkier kontrollerer du hierarkinavnet for hvilken standardkolonne som er avmerket.</span><span class="sxs-lookup"><span data-stu-id="1c54f-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="1c54f-130">Som en del av demonstrasjonsdataene (brukes i denne oppgaveregistreringen) vil du se at Detaljhandelbutikker etter område er standard organisasjonshierarki for rapporteringsformålet for detaljhandel.</span><span class="sxs-lookup"><span data-stu-id="1c54f-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="1c54f-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1c54f-131">Click OK.</span></span>
7. <span data-ttu-id="1c54f-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1c54f-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="1c54f-133">Eksportere en Hovedkontor-rapport</span><span class="sxs-lookup"><span data-stu-id="1c54f-133">Export an HQ reports</span></span>
1. <span data-ttu-id="1c54f-134">Gå til Detaljhandel og handel > Forespørsler og rapporter > Salgsrapporter > Rapport for organisasjonssalg.</span><span class="sxs-lookup"><span data-stu-id="1c54f-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="1c54f-135">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="1c54f-136">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="1c54f-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="1c54f-137">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="1c54f-137">Click OK.</span></span>
5. <span data-ttu-id="1c54f-138">Klikk Eksporter.</span><span class="sxs-lookup"><span data-stu-id="1c54f-138">Click Export.</span></span>
6. <span data-ttu-id="1c54f-139">Klikk PDF.</span><span class="sxs-lookup"><span data-stu-id="1c54f-139">Click PDF.</span></span>

