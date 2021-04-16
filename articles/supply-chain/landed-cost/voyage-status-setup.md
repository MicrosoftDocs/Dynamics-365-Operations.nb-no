---
title: Oppsett av sjøreisestatus
description: Dette emnet beskriver hvordan du fastsetter statusverdiene som brukere kan tilordne til sjøreiser.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829794"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="90ae9-103">Oppsett av sjøreisestatus</span><span class="sxs-lookup"><span data-stu-id="90ae9-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90ae9-104">På siden **Sjøreisestatuser** fastsetter du settet med statusverdier som brukere kan tilordne til sjøreiser.</span><span class="sxs-lookup"><span data-stu-id="90ae9-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="90ae9-105">Brukere kan tilordne statusverdier for sjøreiser til alle nivåer for en sjøreise: sjøreise, forsendelsescontainer, folio, bestillinger og vare (innkjøpslinjer og overføringsordrelinjer).</span><span class="sxs-lookup"><span data-stu-id="90ae9-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="90ae9-106">De brukes til to formål:</span><span class="sxs-lookup"><span data-stu-id="90ae9-106">They are used for two purposes:</span></span>

- <span data-ttu-id="90ae9-107">Informer brukeren om statusen til sjøreisen, forsendelsescontaineren, folioen, bestillingen eller varen (innkjøpslinjer og overføringsordrelinjer).</span><span class="sxs-lookup"><span data-stu-id="90ae9-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="90ae9-108">Begrens bruken av kostnadsområdet ved å hindre endring eller sletting.</span><span class="sxs-lookup"><span data-stu-id="90ae9-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="90ae9-109">Hvis du vil konfigurere sjøreisestatusene, går du til **Netto innkjøpspris \> Oppsett \> Sjøreisestatuser**.</span><span class="sxs-lookup"><span data-stu-id="90ae9-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="90ae9-110">Der kan du legge til, fjerne og redigere statuser ved hjelp av knappene i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="90ae9-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="90ae9-111">Hvert kostnadsområde har sitt eget sett og hierarki av sjøreisestatuser.</span><span class="sxs-lookup"><span data-stu-id="90ae9-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="90ae9-112">Derfor må du først velge kostnadsområdet du vil vise eller opprette sjøreisestatuser for, i feltet **Kostnadsområde** på siden **Sjøreisestatuser**.</span><span class="sxs-lookup"><span data-stu-id="90ae9-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="90ae9-113">Angi deretter verdier i feltene som er beskrevet i tabellen nedenfor, for hver sjøreisestatus, etter behov.</span><span class="sxs-lookup"><span data-stu-id="90ae9-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="90ae9-114">Vær oppmerksom på at statusen for en sjøreise også kan endres automatisk av systemhendelser, for eksempel regler som er fastsatt ved hjelp av sporingskontrollsenteret.</span><span class="sxs-lookup"><span data-stu-id="90ae9-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="90ae9-115">Felt</span><span class="sxs-lookup"><span data-stu-id="90ae9-115">Field</span></span> | <span data-ttu-id="90ae9-116">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="90ae9-116">Description</span></span> |
|---|---|
| <span data-ttu-id="90ae9-117">Sjøreisestatus</span><span class="sxs-lookup"><span data-stu-id="90ae9-117">Voyage status</span></span> | <span data-ttu-id="90ae9-118">Angi navnet på sjøreisestatusen.</span><span class="sxs-lookup"><span data-stu-id="90ae9-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="90ae9-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="90ae9-119">Description</span></span> | <span data-ttu-id="90ae9-120">Angi en beskrivelse av sjøreisestatusen.</span><span class="sxs-lookup"><span data-stu-id="90ae9-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="90ae9-121">Endre</span><span class="sxs-lookup"><span data-stu-id="90ae9-121">Modify</span></span> | <span data-ttu-id="90ae9-122">Merk av i denne avmerkingsboksen hvis brukere har tillatelse til å endre sjøreiser som har denne statusen.</span><span class="sxs-lookup"><span data-stu-id="90ae9-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="90ae9-123">Delete</span><span class="sxs-lookup"><span data-stu-id="90ae9-123">Delete</span></span> | <span data-ttu-id="90ae9-124">Merk av i denne avmerkingsboksen hvis brukere har tillatelse til å slette sjøreiser som har denne statusen.</span><span class="sxs-lookup"><span data-stu-id="90ae9-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="90ae9-125">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="90ae9-125">Mandatory</span></span> | <span data-ttu-id="90ae9-126">Merk av i denne avmerkingsboksen for å gjøre sjøreisestatusen obligatorisk, slik at den ikke kan hoppes over.</span><span class="sxs-lookup"><span data-stu-id="90ae9-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="90ae9-127">Overordnet</span><span class="sxs-lookup"><span data-stu-id="90ae9-127">Parent</span></span> | <span data-ttu-id="90ae9-128">Bruk dette feltet til å opprette et hierarki blant statusverdiene.</span><span class="sxs-lookup"><span data-stu-id="90ae9-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="90ae9-129">Sjøreisestatuser kan endres (manuelt eller automatisk) bare nedover i hierarkiet, fra overordnet status til en av dens underordnede statuser.</span><span class="sxs-lookup"><span data-stu-id="90ae9-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="90ae9-130">Du trenger bare konfigurere de spesifikke sjøreisestatusene som organisasjonen bruker.</span><span class="sxs-lookup"><span data-stu-id="90ae9-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="90ae9-131">Typiske sjøreisestatuser inkluderer *Bekreftet*, *Varer i transitt*, *Mottatt*, *Klar til etterkalkulering* og *Kostnadsført*.</span><span class="sxs-lookup"><span data-stu-id="90ae9-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="90ae9-132">Andre statuser kan imidlertid være til stede.</span><span class="sxs-lookup"><span data-stu-id="90ae9-132">However, other statuses might be present.</span></span>
