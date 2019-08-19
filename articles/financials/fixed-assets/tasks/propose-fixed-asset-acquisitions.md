---
title: Foreslå anleggsmiddelanskaffelser
description: Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839911"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="b0fef-103">Foreslå anleggsmiddelanskaffelser</span><span class="sxs-lookup"><span data-stu-id="b0fef-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0fef-104">Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.</span><span class="sxs-lookup"><span data-stu-id="b0fef-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="b0fef-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="b0fef-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="b0fef-106">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="b0fef-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-107">Select **New**.</span></span>
3. <span data-ttu-id="b0fef-108">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fef-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="b0fef-109">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b0fef-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="b0fef-110">Velg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="b0fef-111">Velg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="b0fef-112">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-112">Select **Filter**.</span></span> <span data-ttu-id="b0fef-113">Velg **Tilbakestill** for å fjerne de tidligere verdiene.</span><span class="sxs-lookup"><span data-stu-id="b0fef-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="b0fef-114">Velg raden **Anleggsmidlets** nummer.</span><span class="sxs-lookup"><span data-stu-id="b0fef-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="b0fef-115">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b0fef-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="b0fef-116">Angi de gjenværende vilkårene for anleggsmidlene du vil anskaffe med dette forslaget.</span><span class="sxs-lookup"><span data-stu-id="b0fef-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="b0fef-117">Velg **OK** to ganger for å gå ut av ruten.</span><span class="sxs-lookup"><span data-stu-id="b0fef-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="b0fef-118">Kontroller transaksjonslinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="b0fef-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="b0fef-119">Bare anleggsmidler med anskaffelsesdato og anskaffelsespris som er angitt i tablået, inkluderes i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="b0fef-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="b0fef-120">Velg kategorien **Tablåer** på siden.</span><span class="sxs-lookup"><span data-stu-id="b0fef-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="b0fef-121">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="b0fef-121">Select **Post**.</span></span>

