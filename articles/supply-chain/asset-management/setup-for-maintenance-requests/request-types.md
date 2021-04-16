---
title: Typer meldinger
description: Dette emnet forklarer hvordan du definerer typer meldinger i Aktivastyring.
author: johanhoffmann
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ff80b2f3e23f46467b8a2fe7a2abd805e5e3a20
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808502"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="2d9d7-103">Typer meldinger</span><span class="sxs-lookup"><span data-stu-id="2d9d7-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2d9d7-104">Typer vedlikeholds anmodninger brukes til å kategorisere meldinger.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="2d9d7-105">Du kan for eksempel ha typer meldinger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="2d9d7-106">Eller du kan ha en spesiell type melding som brukes til å administrere reparasjon av aktiva (depotreparasjon).</span><span class="sxs-lookup"><span data-stu-id="2d9d7-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="2d9d7-107">En type melding definerer tilknytningen med en livssyklusgruppe for meldinger (livssyklusmodell for vedlikehold).</span><span class="sxs-lookup"><span data-stu-id="2d9d7-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="2d9d7-108">Livssyklusmodeller for meldinger definerer livssyklustilstandene som kan angis for en melding.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="2d9d7-109">(Eksempler på livssyklustilstander for meldinger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)</span><span class="sxs-lookup"><span data-stu-id="2d9d7-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="2d9d7-110">Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Typer meldinger**.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="2d9d7-111">Velg **Ny** for å opprette en type melding.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="2d9d7-112">Angi en ID for typen melding i feltet **Type melding**.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="2d9d7-113">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="2d9d7-114">På hurtigfanen **Generelt**, i feltet **Livssyklusmodell for melding**, velger du en livssyklusmodell for melding.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="2d9d7-115">Velg en arbeidsordretype i feltet **Arbeidsordretype**.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="2d9d7-116">Når en melding konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen melding.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="2d9d7-117">Illustrasjonen nedenfor viser et eksempel på siden **Typer meldinger**.</span><span class="sxs-lookup"><span data-stu-id="2d9d7-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Siden Typer meldinger](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]