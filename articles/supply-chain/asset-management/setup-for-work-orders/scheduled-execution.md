---
title: Planlagt utførelse
description: Dette emnet beskriver planlagt utførelse i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825644"
---
# <a name="scheduled-execution"></a><span data-ttu-id="42004-103">Planlagt utførelse</span><span class="sxs-lookup"><span data-stu-id="42004-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="42004-104">Du kan bruke servicenivåer for arbeidsordrer til å definere planlagt utførelse.</span><span class="sxs-lookup"><span data-stu-id="42004-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="42004-105">(Hvis du vil ha mer informasjon om servicenivåer for arbeidsordrer, se [Servicenivå og -beskrivelse](service-level-and-description.md).) Planlagt utførelse gir fleksibilitet i arbeidsplanlegging for vedlikeholdspersoner fordi du kan definere mer detaljerte eller mindre detaljerte krav for intervallet som en arbeidsordre skal fullføres i.</span><span class="sxs-lookup"><span data-stu-id="42004-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="42004-106">For eksempel kan en vedlikeholdsperson som fullfører en jobb raskere enn forventet i et produksjonslokale, kunne gå videre til en annen jobb i nærheten som var planlagt for gjeldende uke, men ikke nødvendigvis for gjeldende dag.</span><span class="sxs-lookup"><span data-stu-id="42004-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="42004-107">Denne metoden gjør det mulig å optimalisere arbeiderplanlegging og jobbfullførelse.</span><span class="sxs-lookup"><span data-stu-id="42004-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="42004-108">Oppsett av planlagt utførelse, som er knyttet til arbeidsordrer, kan være generisk eller spesifikt.</span><span class="sxs-lookup"><span data-stu-id="42004-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="42004-109">Du kan definere generelle linjer som ikke er begrenset til bestemte arbeidsordretyper, anleggsmiddeltyper og så videre.</span><span class="sxs-lookup"><span data-stu-id="42004-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="42004-110">Du kan også opprette planlagte utførelseslinjer som gjelder for en bestemt arbeidsordretype, anleggsmiddeltype, vedlikeholdsjobbtype og så videre.</span><span class="sxs-lookup"><span data-stu-id="42004-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="42004-111">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Planlagt utførelse**.</span><span class="sxs-lookup"><span data-stu-id="42004-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="42004-112">Velg **Ny** for å opprette en planlagt utførelseslinje.</span><span class="sxs-lookup"><span data-stu-id="42004-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="42004-113">Velg aktuelle verdier i feltene **Arbeidssted**, **Arbeidsordretype**, **Aktivatype**, **Produsent**, **Modell**, **Kategori for vedlikeholdsjobbtype**, **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="42004-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="42004-114">Velg et servicenivå for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="42004-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="42004-115">Hvis du lar dette feltet stå tomt, får du den mest generelle typen av planlagt utførelseslinje.</span><span class="sxs-lookup"><span data-stu-id="42004-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="42004-116">Hvis du vil ha et eksempel på en generisk linje, kan du se den første posten i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="42004-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="42004-117">Denne linjen gjør at alle arbeidsordrer som ikke har noe arbeidsordreservicenivå, kan planlegges for en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="42004-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="42004-118">Velg tidsintervall i **Planlagt utførelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="42004-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="42004-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="42004-119">Select **Save**.</span></span>

![Planlagt utførelse](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]