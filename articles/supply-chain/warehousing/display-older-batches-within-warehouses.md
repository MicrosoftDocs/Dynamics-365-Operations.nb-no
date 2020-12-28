---
title: Konfigurer Vis eldre partier i lageret på en mobilenhet
description: Dette emnet beskriver hvordan du konfigurerer en mobil enhet til å vise en liste over lokasjoner med partier som er eldre enn den gjeldende plasseringen til en linje i arbeid.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b1c9452a811d662976a25993264be0617ac67fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434391"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="5cab5-103">Konfigurer Vis eldre partier i lageret på en mobilenhet</span><span class="sxs-lookup"><span data-stu-id="5cab5-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cab5-104">Den **Vis eldre lagerpartier lageret** konfigurasjon kan du vise en liste over lokasjoner med partier som er eldre enn den gjeldende plasseringen til linjen arbeid.</span><span class="sxs-lookup"><span data-stu-id="5cab5-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="5cab5-105">Listen over lokasjoner som skal vises inneholder informasjon om eldre partiene på sted med utløpsdatoen og det fysiske lageret for hver bunke.</span><span class="sxs-lookup"><span data-stu-id="5cab5-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="5cab5-106">Du kan velge å velge fra et annet sted, eller for å fortsette plukking fra gjeldende plassering.</span><span class="sxs-lookup"><span data-stu-id="5cab5-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="5cab5-107">Velg fra et annet sted - hvis du velger en ny plassering for å velge fra, oppdateres den gjeldende linjen i arbeid hvis du vil bruke den nye plasseringen og fortsetter arbeidet på vanlig måte med den nye plasseringen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="5cab5-108">For den nye adressen skal være gyldig, må det ha nok tilgjengelig antall for hele fungerer linjen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="5cab5-109">Hvis behovsantallet ikke er tilgjengelig, oppdateres ikke arbeid linjen, og viser listen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="5cab5-110">Fortsette plukking fra gjeldende plassering – Hvis du fortsetter med befinner for arbeid, fortsetter antallet for linjen arbeid som skal plukkes fra den opprinnelige plasseringen.</span><span class="sxs-lookup"><span data-stu-id="5cab5-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="5cab5-111">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="5cab5-111">Where it applies</span></span>
<span data-ttu-id="5cab5-112">Vis eldre lageret er konfigurert på mobil enhet, menyelementer og påvirker plukkingen for partiet under elementene.</span><span class="sxs-lookup"><span data-stu-id="5cab5-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="5cab5-113">Definere visning eldre bunker i lager</span><span class="sxs-lookup"><span data-stu-id="5cab5-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="5cab5-114">Den **Vis eldre lagerpartier lageret** konfigurasjon er tilgjengelig på mobil enhet menyelementene når den **plukk eldste satsvis** er **varsel**.</span><span class="sxs-lookup"><span data-stu-id="5cab5-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="5cab5-115">Under **Lagerstyring** > **oppsett** > **mobil enhet** > **mobiltelefon menyelementer**, setter **bruker eksisterende arbeid** til **Ja** for menyelementet, og velg **varsel** i den **plukk eldste satsvis** feltet.</span><span class="sxs-lookup"><span data-stu-id="5cab5-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

