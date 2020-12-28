---
title: Planlagt utførelse
description: Dette emnet beskriver planlagt utførelse i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434438"
---
# <a name="scheduled-execution"></a><span data-ttu-id="13726-103">Planlagt utførelse</span><span class="sxs-lookup"><span data-stu-id="13726-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="13726-104">Du kan bruke servicenivåer for arbeidsordrer til å definere planlagt utførelse.</span><span class="sxs-lookup"><span data-stu-id="13726-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="13726-105">(Hvis du vil ha mer informasjon om servicenivåer for arbeidsordrer, se [Servicenivå og -beskrivelse](service-level-and-description.md).) Planlagt utførelse gir fleksibilitet i arbeidsplanlegging for vedlikeholdsarbeidere fordi du kan definere mer detaljerte eller mindre detaljerte krav for intervallet som en arbeidsordre skal fullføres i.</span><span class="sxs-lookup"><span data-stu-id="13726-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="13726-106">For eksempel kan en vedlikeholdsarbeider som fullfører en jobb raskere enn forventet i et produksjonslokale, kunne gå videre til en annen jobb i nærheten som var planlagt for gjeldende uke, men ikke nødvendigvis for gjeldende dag.</span><span class="sxs-lookup"><span data-stu-id="13726-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="13726-107">Denne metoden gjør det mulig å optimalisere arbeiderplanlegging og jobbfullførelse.</span><span class="sxs-lookup"><span data-stu-id="13726-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="13726-108">Oppsett av planlagt utførelse, som er knyttet til arbeidsordrer, kan være generisk eller spesifikt.</span><span class="sxs-lookup"><span data-stu-id="13726-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="13726-109">Du kan definere generelle linjer som ikke er begrenset til bestemte arbeidsordretyper, anleggsmiddeltyper og så videre.</span><span class="sxs-lookup"><span data-stu-id="13726-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="13726-110">Du kan også opprette planlagte utførelseslinjer som gjelder for en bestemt arbeidsordretype, anleggsmiddeltype, vedlikeholdsjobbtype og så videre.</span><span class="sxs-lookup"><span data-stu-id="13726-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="13726-111">Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Planlagt utførelse**.</span><span class="sxs-lookup"><span data-stu-id="13726-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="13726-112">Velg **Ny** for å opprette en planlagt utførelseslinje.</span><span class="sxs-lookup"><span data-stu-id="13726-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="13726-113">Velg aktuelle verdier i feltene **Arbeidssted**, **Arbeidsordretype**, **Aktivatype**, **Produsent**, **Modell**, **Kategori for vedlikeholdsjobbtype**, **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.</span><span class="sxs-lookup"><span data-stu-id="13726-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="13726-114">Velg et servicenivå for arbeidsordren i **Servicenivå**-feltet.</span><span class="sxs-lookup"><span data-stu-id="13726-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="13726-115">Hvis du lar dette feltet stå tomt, får du den mest generelle typen av planlagt utførelseslinje.</span><span class="sxs-lookup"><span data-stu-id="13726-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="13726-116">Hvis du vil ha et eksempel på en generisk linje, kan du se den første posten i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="13726-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="13726-117">Denne linjen gjør at alle arbeidsordrer som ikke har noe arbeidsordreservicenivå, kan planlegges for en bestemt dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="13726-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="13726-118">Velg tidsintervall i **Planlagt utførelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="13726-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="13726-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="13726-119">Select **Save**.</span></span>

![Planlagt utførelse](media/20-setup-for-work-orders.png)
