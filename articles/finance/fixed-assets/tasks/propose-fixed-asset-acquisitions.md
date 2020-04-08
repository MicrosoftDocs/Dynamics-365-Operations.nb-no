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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142737"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="e1274-103">Foreslå anleggsmiddelanskaffelser</span><span class="sxs-lookup"><span data-stu-id="e1274-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1274-104">Dette emnet beskriver hvordan du anskaffer et anleggsmiddel ved hjelp av anskaffelsesforslaget i anleggsmiddeljournalen.</span><span class="sxs-lookup"><span data-stu-id="e1274-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="e1274-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="e1274-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="e1274-106">I navigasjonsruten går du til **Moduler > Anleggsmidler > Journaloppføringer > Anleggsmiddeljournal**.</span><span class="sxs-lookup"><span data-stu-id="e1274-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="e1274-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e1274-107">Select **New**.</span></span>
3. <span data-ttu-id="e1274-108">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e1274-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="e1274-109">Velg **Linjer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="e1274-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="e1274-110">Velg **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="e1274-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="e1274-111">Velg **Anskaffelsesforslag**.</span><span class="sxs-lookup"><span data-stu-id="e1274-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="e1274-112">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="e1274-112">Select **Filter**.</span></span> <span data-ttu-id="e1274-113">Velg **Tilbakestill** for å fjerne de tidligere verdiene.</span><span class="sxs-lookup"><span data-stu-id="e1274-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="e1274-114">Velg raden **Anleggsmidlets** nummer.</span><span class="sxs-lookup"><span data-stu-id="e1274-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="e1274-115">Angi eller velg en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e1274-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="e1274-116">Angi de gjenværende vilkårene for anleggsmidlene du vil anskaffe med dette forslaget.</span><span class="sxs-lookup"><span data-stu-id="e1274-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="e1274-117">Velg **OK** to ganger for å gå ut av ruten.</span><span class="sxs-lookup"><span data-stu-id="e1274-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="e1274-118">Kontroller transaksjonslinjene som er opprettet.</span><span class="sxs-lookup"><span data-stu-id="e1274-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="e1274-119">Bare anleggsmidler med anskaffelsesdato og anskaffelsespris som er angitt i tablået, inkluderes i anskaffelsesforslaget.</span><span class="sxs-lookup"><span data-stu-id="e1274-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="e1274-120">Velg kategorien **Tablåer** på siden.</span><span class="sxs-lookup"><span data-stu-id="e1274-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="e1274-121">Velg **Poster**.</span><span class="sxs-lookup"><span data-stu-id="e1274-121">Select **Post**.</span></span>

