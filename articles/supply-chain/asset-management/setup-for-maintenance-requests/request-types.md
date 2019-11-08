---
title: Typer vedlikeholdsanmodninger
description: Dette emnet forklarer hvordan du definerer typer vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 430e475b52638dd80512ffd79d42aac6f5f340e1
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571145"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="c5c1d-103">Typer vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="c5c1d-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c5c1d-104">Typer vedlikeholds anmodninger brukes til å kategorisere vedlikeholdsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="c5c1d-105">Du kan for eksempel ha typer vedlikeholdsanmodninger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="c5c1d-106">Eller du kan ha en spesiell type vedlikeholdsanmodning som brukes til å administrere reparasjon av aktiva (depotreparasjon).</span><span class="sxs-lookup"><span data-stu-id="c5c1d-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="c5c1d-107">En type vedlikeholdsanmodning definerer tilknytningen med en livsløpsgruppe for vedlikeholdsanmodninger (livsløpsmodell for vedlikehold).</span><span class="sxs-lookup"><span data-stu-id="c5c1d-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="c5c1d-108">Livsløpsmodeller for vedlikeholdsanmodninger definerer livsløpstilstandene som kan angis for en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="c5c1d-109">(Eksempler på livsløpstilstander for vedlikeholdsanmodninger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)</span><span class="sxs-lookup"><span data-stu-id="c5c1d-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="c5c1d-110">Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Typer vedlikeholdsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="c5c1d-111">Velg **Ny** for å opprette en type vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="c5c1d-112">Angi en ID for typen vedlikeholdsanmodning i feltet **Type vedlikeholdsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="c5c1d-113">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="c5c1d-114">På hurtigfanen **Generelt**, i feltet **Livsløpsmodell for vedlikeholdsanmodning**, velger du en livsløpsmodell for vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="c5c1d-115">Velg en arbeidsordretype i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="c5c1d-116">Når en vedlikeholdsanmodning konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="c5c1d-117">Illustrasjonen nedenfor viser et eksempel på siden **Typer vedlikeholdsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="c5c1d-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Siden Typer vedlikeholdsanmodninger](media/07-setup-for-requests.png)
