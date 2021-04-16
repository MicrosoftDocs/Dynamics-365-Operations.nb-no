---
title: Foreslå anleggsmiddelanskaffelser
description: Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817177"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="8adfe-103">Foreslå anleggsmiddelanskaffelser</span><span class="sxs-lookup"><span data-stu-id="8adfe-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8adfe-104">Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.</span><span class="sxs-lookup"><span data-stu-id="8adfe-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="8adfe-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="8adfe-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="8adfe-106">Hvis du vil anskaffe et anleggsmiddel via en journal for forslag til anleggsmidler, må du først opprette anleggsmiddelposten og deretter definere anskaffelsesprisen i anleggsmiddelboken.</span><span class="sxs-lookup"><span data-stu-id="8adfe-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="8adfe-107">Opprette et forslag om anskaffelse av aktiva</span><span class="sxs-lookup"><span data-stu-id="8adfe-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="8adfe-108">Fullfør fremgangsmåten nedenfor for å opprette et forslag om anskaffelse av aktiva.</span><span class="sxs-lookup"><span data-stu-id="8adfe-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="8adfe-109">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="8adfe-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-110">Select **New**.</span></span>
3. <span data-ttu-id="8adfe-111">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8adfe-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="8adfe-112">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8adfe-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="8adfe-113">Velg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="8adfe-114">Velg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="8adfe-115">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-115">Select **Filter**.</span></span> <span data-ttu-id="8adfe-116">Velg **Tilbakestill** for å fjerne tidligere verdier.</span><span class="sxs-lookup"><span data-stu-id="8adfe-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="8adfe-117">Velg raden **Anleggsmidlets** nummer.</span><span class="sxs-lookup"><span data-stu-id="8adfe-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="8adfe-118">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8adfe-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="8adfe-119">Angi de gjenværende vilkårene for anleggsmidlene du vil anskaffe med dette forslaget.</span><span class="sxs-lookup"><span data-stu-id="8adfe-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="8adfe-120">Velg **OK** to ganger for å gå ut av ruten.</span><span class="sxs-lookup"><span data-stu-id="8adfe-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="8adfe-121">Kontroller at transaksjonslinjene er opprettet.</span><span class="sxs-lookup"><span data-stu-id="8adfe-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="8adfe-122">Bare anleggsmidler med anskaffelsesdato og anskaffelsespris som er angitt i tablået, inkluderes i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="8adfe-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="8adfe-123">Velg kategorien **Tablåer** på siden.</span><span class="sxs-lookup"><span data-stu-id="8adfe-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="8adfe-124">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="8adfe-125">Ta med standard finansdimensjoner i et anskaffelsesforslag.</span><span class="sxs-lookup"><span data-stu-id="8adfe-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="8adfe-126">Anskaffelsestransaksjonen kan opprettes ved hjelp av Excel-tillegg ved å gå til **Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="8adfe-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="8adfe-127">Opprett en ny journal, gå til **Linjer**-delen på siden, velg Excel-ikonet og velg deretter en anleggsmiddeljournallinje.</span><span class="sxs-lookup"><span data-stu-id="8adfe-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="8adfe-128">Systemet oppretter og åpner en Excel-mal som representerer journallinjer.</span><span class="sxs-lookup"><span data-stu-id="8adfe-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="8adfe-129">Du kan legge til data for journallinjene du legger til i malen, og deretter publisere informasjonen tilbake i systemet.</span><span class="sxs-lookup"><span data-stu-id="8adfe-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="8adfe-130">Hvis det er definert standarddimensjoner for det valgte anleggsmiddelboken og tilsvarende anleggsmidler som ble angitt i Excel-malen, blir de standard finansdimensjonene kalt fra hoveddataene for anleggsmiddelboken når journalen publiseres fra Excel til systemet.</span><span class="sxs-lookup"><span data-stu-id="8adfe-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="8adfe-131">Hvis du vil inkludere finansdimensjoner i et anleggsmiddelbok automatisk mens du publiserer anleggsmiddeljournalen fra Excel-tillegget, må standarddimensjonene defineres på forhånd.</span><span class="sxs-lookup"><span data-stu-id="8adfe-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
