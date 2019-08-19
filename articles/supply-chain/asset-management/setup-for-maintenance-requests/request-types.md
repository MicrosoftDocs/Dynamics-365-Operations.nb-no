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
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790525"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="841b0-103">Typer vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="841b0-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="841b0-104">Typer vedlikeholds anmodninger brukes til å kategorisere vedlikeholdsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="841b0-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="841b0-105">Du kan for eksempel ha typer vedlikeholdsanmodninger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="841b0-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="841b0-106">Eller du kan ha en spesiell type vedlikeholdsanmodning som brukes til å administrere reparasjon av aktiva (depotreparasjon).</span><span class="sxs-lookup"><span data-stu-id="841b0-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="841b0-107">En type vedlikeholdsanmodning definerer tilknytningen med en livsløpsgruppe for vedlikeholdsanmodninger (livsløpsmodell for vedlikehold).</span><span class="sxs-lookup"><span data-stu-id="841b0-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="841b0-108">Livsløpsmodeller for vedlikeholdsanmodninger definerer livsløpstilstandene som kan angis for en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="841b0-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="841b0-109">(Eksempler på livsløpstilstander for vedlikeholdsanmodninger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)</span><span class="sxs-lookup"><span data-stu-id="841b0-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="841b0-110">Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Typer vedlikeholdsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="841b0-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="841b0-111">Velg **Ny** for å opprette en type vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="841b0-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="841b0-112">Angi en ID for typen vedlikeholdsanmodning i feltet **Type vedlikeholdsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="841b0-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="841b0-113">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="841b0-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="841b0-114">På hurtigfanen **Generelt**, i feltet **Livsløpsmodell for vedlikeholdsanmodning**, velger du en livsløpsmodell for vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="841b0-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="841b0-115">Velg en arbeidsordretype i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="841b0-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="841b0-116">Når en vedlikeholdsanmodning konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="841b0-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="841b0-117">Illustrasjonen nedenfor viser et eksempel på siden **Typer vedlikeholdsanmodninger**.</span><span class="sxs-lookup"><span data-stu-id="841b0-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Figur 1](media/07-setup-for-requests.png)
