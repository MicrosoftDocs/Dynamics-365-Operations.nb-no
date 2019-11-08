---
title: Arbeidsordretyper
description: Dette emnet forklarer arbeidsordretypene i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3e813bd4f2d47b928b6184bb063d9afa45695727
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569737"
---
# <a name="work-order-types"></a><span data-ttu-id="ff6c8-103">Arbeidsordretyper</span><span class="sxs-lookup"><span data-stu-id="ff6c8-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ff6c8-104">Arbeidsordretyper brukes til å kategorisere arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="ff6c8-105">Du kan for eksempel ha arbeidsordrer som er knyttet til forebyggende vedlikehold eller korrigerende vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="ff6c8-106">En arbeidsordretype definerer en tilknytning til en livssyklusmodell for arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="ff6c8-107">En livssyklusmodell for arbeidsordre definerer livssyklustilstandene for arbeidsordre som kan angis i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="ff6c8-108">(Eksempler på livssyklustilstander for arbeidsordre inkluderer **Opprettet**, **Pågår** og **Avsluttet**.)</span><span class="sxs-lookup"><span data-stu-id="ff6c8-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="ff6c8-109">Hvis du vil ha mer informasjon om livssyklustilstander for arbeidsordrer og prosjektstadier, kan du se [i Livssyklustilstand for arbeidsordre](work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="ff6c8-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="ff6c8-110">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Arbeidsordretyper**.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="ff6c8-111">Velg **Ny** for å opprette en ny arbeidsordretype.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="ff6c8-112">Angi en ID for arbeidsordretypen i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="ff6c8-113">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="ff6c8-114">Velg en livsløpsmodell i feltet **Livsløpsmodell for arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="ff6c8-115">Sett alternativet **Én vedlikeholdsperson** til **Ja** hvis alle arbeidsordrejobber som er relatert til en arbeidsordre av denne typen, skal planlegges til samme vedlikeholdsarbeider.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="ff6c8-116">I **Kostnadstype**-feltet velger du **Korrektiv**, **Forebyggende**eller **Investering** etter behov.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="ff6c8-117">Alle arbeidsordrejobber i en arbeidsordre må ha samme kostnadstype.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="ff6c8-118">I **Obligatorisk**-delen setter du de relevante alternativene til **Ja** for å angi hvilken feilrelatert eller vedlikeholdsnedetidrelatert informasjon som legges til en arbeidsordre av denne typen.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff6c8-119">Alternativene i **Obligatorisk**-delen er knyttet til alternativene i hurtigfanen **Valider** på siden **Livssyklustilstand for arbeidsordre** (**Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Livssyklustilstander**).</span><span class="sxs-lookup"><span data-stu-id="ff6c8-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="ff6c8-120">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ff6c8-120">Select **Save**.</span></span>

![Arbeidsordretyper](media/16-setup-for-work-orders.png)
