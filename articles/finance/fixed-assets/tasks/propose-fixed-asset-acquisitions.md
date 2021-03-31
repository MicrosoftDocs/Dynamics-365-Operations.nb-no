---
title: Foreslå anleggsmiddelanskaffelser
description: Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 426a5e42c1fc26958ab37eddd915334f8b0e19cc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205034"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="61fc8-103">Foreslå anleggsmiddelanskaffelser</span><span class="sxs-lookup"><span data-stu-id="61fc8-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61fc8-104">Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.</span><span class="sxs-lookup"><span data-stu-id="61fc8-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="61fc8-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="61fc8-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="61fc8-106">Hvis du vil anskaffe et anleggsmiddel via en journal for forslag til anleggsmidler, må du først opprette anleggsmiddelposten og deretter definere anskaffelsesprisen i anleggsmiddelboken.</span><span class="sxs-lookup"><span data-stu-id="61fc8-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="61fc8-107">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="61fc8-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-108">Select **New**.</span></span>
3. <span data-ttu-id="61fc8-109">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="61fc8-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="61fc8-110">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="61fc8-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="61fc8-111">Velg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="61fc8-112">Velg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="61fc8-113">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-113">Select **Filter**.</span></span> <span data-ttu-id="61fc8-114">Velg **Tilbakestill** for å fjerne de tidligere verdiene.</span><span class="sxs-lookup"><span data-stu-id="61fc8-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="61fc8-115">Velg raden **Anleggsmidlets** nummer.</span><span class="sxs-lookup"><span data-stu-id="61fc8-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="61fc8-116">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="61fc8-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="61fc8-117">Angi de gjenværende vilkårene for anleggsmidlene du vil anskaffe med dette forslaget.</span><span class="sxs-lookup"><span data-stu-id="61fc8-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="61fc8-118">Velg **OK** to ganger for å gå ut av ruten.</span><span class="sxs-lookup"><span data-stu-id="61fc8-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="61fc8-119">Kontroller transaksjonslinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="61fc8-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="61fc8-120">Bare anleggsmidler med anskaffelsesdato og anskaffelsespris som er angitt i tablået, inkluderes i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="61fc8-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="61fc8-121">Velg kategorien **Tablåer** på siden.</span><span class="sxs-lookup"><span data-stu-id="61fc8-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="61fc8-122">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="61fc8-122">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]