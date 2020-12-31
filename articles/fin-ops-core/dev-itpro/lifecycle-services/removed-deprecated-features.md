---
title: Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abf7a1a0a75ac3098efeeab3df65481999b69acc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687884"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="b78b3-103">Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b78b3-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b78b3-104">Dette emnet beskriver funksjoner som er fjernet eller avskrevet for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b78b3-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="b78b3-105">En *fjernet* funksjon er ikke lenger tilgjengelig i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b78b3-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="b78b3-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="b78b3-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="b78b3-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="b78b3-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="b78b3-108">Oktober 2019-kunngjøringer</span><span class="sxs-lookup"><span data-stu-id="b78b3-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="b78b3-109">Flytdiagrammer for forretningsprosessmodelerer</span><span class="sxs-lookup"><span data-stu-id="b78b3-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="b78b3-110"><strong>Årsak til avskrivning/fjerning</strong></span><span class="sxs-lookup"><span data-stu-id="b78b3-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="b78b3-111">Vi avskriver flytskjemakomponenten i BPM (Forretningsprosessmodelerer), fordi eldre utforming forårsaket lav bruk.</span><span class="sxs-lookup"><span data-stu-id="b78b3-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b78b3-112"><strong>Erstattet med en annen funksjon?</strong></span><span class="sxs-lookup"><span data-stu-id="b78b3-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="b78b3-113">Nei</span><span class="sxs-lookup"><span data-stu-id="b78b3-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b78b3-114"><strong>Berørte områder</strong></span><span class="sxs-lookup"><span data-stu-id="b78b3-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="b78b3-115">Forretningsprosessmodelerer</span><span class="sxs-lookup"><span data-stu-id="b78b3-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b78b3-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="b78b3-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="b78b3-117">Avskrevet: Komponenten flytdiagram i BPM forventes å bli fjernet i 2020.</span><span class="sxs-lookup"><span data-stu-id="b78b3-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="b78b3-118">Følgende funksjonalitet vil være utilgjengelig:</span><span class="sxs-lookup"><span data-stu-id="b78b3-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="b78b3-119">Alle flytskjemaer vil være skrivebeskyttede og ikke tilgjengelige for redigering.</span><span class="sxs-lookup"><span data-stu-id="b78b3-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="b78b3-120">Figuregenskapene som er knyttet til flytskjemaaktiviteter, vil heller ikke være tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="b78b3-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="b78b3-121">Disse flytskjemaene inneholder både standard flytskjemaer som genereres automatisk og tilpassede flytskjemaer som endres basert på disse standard flytskjemaene.</span><span class="sxs-lookup"><span data-stu-id="b78b3-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="b78b3-122">Prosesstrinnene vil være skrivebeskyttede og ikke tilgjengelige for redigering.</span><span class="sxs-lookup"><span data-stu-id="b78b3-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="b78b3-123">Den eldre funksjonen for tilpassings-/gapanalyse vil ikke være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b78b3-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="b78b3-124">Derfor blir ingen gapliste automatisk opprettet eller tilgjengelig for eksport.</span><span class="sxs-lookup"><span data-stu-id="b78b3-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="b78b3-125"><strong>Merk:</strong> Denne funksjonen ble tidligere avskrevet og erstattet av Microsoft Azure DevOps-integrasjoner.</span><span class="sxs-lookup"><span data-stu-id="b78b3-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="b78b3-126">Versjonsloggen for flytskjemaet vil ikke være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="b78b3-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
