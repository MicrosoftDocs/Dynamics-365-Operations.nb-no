---
title: Ansvarlige vedlikeholdsarbeidere
description: Dette emnet forklarer hvordan du ansvarlige vedlikeholdspersoner i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208944"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="99747-103">Ansvarlige vedlikeholdsarbeidere</span><span class="sxs-lookup"><span data-stu-id="99747-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="99747-104">Ansvarlige vedlikeholdsarbeidere kan være relatert til aktivatyper, aktiva, arbeidssteder, kategorier for vedlikeholdsjobbtype, vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtype og fag.</span><span class="sxs-lookup"><span data-stu-id="99747-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="99747-105">De kan brukes på arbeidsordrer og vedlikeholdsanmodninger for å angi en preferanse om vedlikeholdsarbeiderne som skal være ansvarlig for en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="99747-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="99747-106">(Disse vedlikeholdsarbeiderne er imidlertid ikke nødvendigvis de samme arbeiderne som er planlagt å utføre arbeidsordren.) Bruk av denne funksjonen er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="99747-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="99747-107">Den kan for eksempel brukes til å velge ansvarlige arbeidere eller arbeidergrupper for bestemte arbeidstyper eller arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="99747-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="99747-108">Under et livsløp for en arbeidsordre eller et livsløp for en vedlikeholdsanmodning kan ansvarlige vedlikeholdsarbeidere endres eller oppdateres.</span><span class="sxs-lookup"><span data-stu-id="99747-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="99747-109">Denne endringen eller oppdateringen kan for eksempel være knyttet til en endring i livsløpstilstanden for vedlikeholdsanmodninger eller livsløpstilstanden for arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="99747-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="99747-110">Oppsettet på siden **Ansvarlige vedlikeholdsarbeidere** brukes *ikke* under planlegging av arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="99747-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="99747-111">I Aktivastyring kan du også definere *foretrukne* vedlikeholdsarbeidere som kan tildeles arbeidsordrer under planlegging av arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="99747-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="99747-112">Før du kan definere ansvarlige vedlikeholdsarbeidere, må du definere arbeidere og vedlikeholdsarbeidergrupper som skal være tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="99747-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="99747-113">(Hvis du vil ha informasjon om hvordan du definerer arbeidere og grupper med vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="99747-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="99747-114">Definer ansvarlige vedlikeholdspersoner</span><span class="sxs-lookup"><span data-stu-id="99747-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="99747-115">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidere** \> **Ansvarlige vedlikeholdsarbeidere**.</span><span class="sxs-lookup"><span data-stu-id="99747-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="99747-116">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="99747-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="99747-117">Opprett først en standard ansvarlig vedlikeholdsarbeider eller et gruppeoppsett for ansvarlig vedlikeholdsarbeider, der du angir bare feltet **Ansvarlig vedlikeholdspersongruppe** og/eller feltet **Ansvarlig arbeider**.</span><span class="sxs-lookup"><span data-stu-id="99747-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="99747-118">La de resterende feltene stå tomme.</span><span class="sxs-lookup"><span data-stu-id="99747-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="99747-119">Dette standardoppsettet vil bli brukt ved arbeidsordreplanlegging hvis ingen annen, mer spesifikk kombinasjon samsvarer med innholdet i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="99747-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="99747-120">Under opprettelsen av en vedlikeholdsanmodning, når en ansvarlig vedlikeholdsarbeider eller ansvarlig vedlikeholdsarbeidergruppe er gjort tilgjengelig for valg på siden **Alle vedlikeholdsanmodninger**, går Aktivastyring gjennom alle ansvarlige vedlikeholdsarbeiderposter for å se etter et mulig samsvar.</span><span class="sxs-lookup"><span data-stu-id="99747-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="99747-121">Den kontrollerer alltid den mest spesifikke kombinasjonen først.</span><span class="sxs-lookup"><span data-stu-id="99747-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="99747-122">Med andre ord ser Aktivastyring først etter et treff i **Fag**-feltet.</span><span class="sxs-lookup"><span data-stu-id="99747-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="99747-123">Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i feltet **Variant av vedlikeholdsjobbtype**.</span><span class="sxs-lookup"><span data-stu-id="99747-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="99747-124">Hvis det ikke blir funnet noe treff, kontrolleres det for et treff i **Vedlikeholdsjobbtype**-feltet, og så videre.</span><span class="sxs-lookup"><span data-stu-id="99747-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="99747-125">Som du kan se i oppsettet av siden, betyr dette at, for å finne den mest spesifikke kombinasjonen, kontrollerer Aktivastyring hver post fra høyre til venstre for et treff (først **Fag**, deretter **Variant av vedlikeholdsjobbtype**, deretter **Vedlikeholdsjobbtype**, deretter **Kategori av vedlikeholdsjobbtype**, deretter **Arbeidssted**, deretter **Aktiva** og til slutt **Aktivatype**).</span><span class="sxs-lookup"><span data-stu-id="99747-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="99747-126">Hvis det ikke blir funnet noen treff, brukes standardoppføringen, der det ikke er noen valg i disse sju feltene.</span><span class="sxs-lookup"><span data-stu-id="99747-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="99747-127">Illustrasjonen nedenfor viser et eksempel på siden **Ansarlige vedlikeholdsarbeidere**.</span><span class="sxs-lookup"><span data-stu-id="99747-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Siden Ansvarlige vedlikeholdsarbeidere](media/08-setup-for-requests.png)
