---
title: Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027986"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="5f2c6-103">Fjernede eller utgåtte funksjoner i Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="5f2c6-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f2c6-104">Dette emnet beskriver funksjoner som er fjernet eller avskrevet for Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5f2c6-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="5f2c6-105">En *fjernet* funksjon er ikke lenger tilgjengelig i tjenesten.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="5f2c6-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="5f2c6-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="5f2c6-108">Oktober 2019-kunngjøringer</span><span class="sxs-lookup"><span data-stu-id="5f2c6-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="5f2c6-109">Flytdiagrammer for forretningsprosessmodelerer</span><span class="sxs-lookup"><span data-stu-id="5f2c6-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="5f2c6-110"><strong>Årsak til avskrivning/fjerning</strong></span><span class="sxs-lookup"><span data-stu-id="5f2c6-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="5f2c6-111">Vi avskriver flytskjemakomponenten i BPM (Forretningsprosessmodelerer), fordi eldre utforming forårsaket lav bruk.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f2c6-112"><strong>Erstattet med en annen funksjon?</strong></span><span class="sxs-lookup"><span data-stu-id="5f2c6-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="5f2c6-113">Nei</span><span class="sxs-lookup"><span data-stu-id="5f2c6-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f2c6-114"><strong>Berørte områder</strong></span><span class="sxs-lookup"><span data-stu-id="5f2c6-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="5f2c6-115">Forretningsprosessmodelerer</span><span class="sxs-lookup"><span data-stu-id="5f2c6-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f2c6-116"><strong>Status</strong></span><span class="sxs-lookup"><span data-stu-id="5f2c6-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="5f2c6-117">Avskrevet: Komponenten flytdiagram i BPM forventes å bli fjernet i 2020.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="5f2c6-118">Følgende funksjonalitet blir fjernet:</span><span class="sxs-lookup"><span data-stu-id="5f2c6-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="5f2c6-119">Eksisterende flytskjemaer vil ikke være tilgjengelige for visning eller redigering.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="5f2c6-120">Figuregenskapene som er tilknyttet flytskjemaaktiviteter, vil heller ikke være tilgjengelige, fordi hele <strong>flytskjema</strong>-kategorien vil bli fjernet.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="5f2c6-121">Disse flytskjemaene inneholder både standard flytskjemaer som genereres automatisk og tilpassede flytskjemaer som endres basert på disse standard flytskjemaene.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="5f2c6-122">Den eldre funksjonen for tilpassings-/gapanalyse vil ikke være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="5f2c6-123">Derfor blir ingen gapliste automatisk opprettet eller tilgjengelig for eksport.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="5f2c6-124"><strong>Merk:</strong> Denne funksjonen ble tidligere avskrevet og erstattet av Microsoft Azure DevOps-integrasjoner.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="5f2c6-125">Versjonsloggen for flytskjemaet vil ikke være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="5f2c6-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
