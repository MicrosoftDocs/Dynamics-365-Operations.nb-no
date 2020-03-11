---
title: Fjernede eller avskrevne Platform-funksjoner
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087889"
---
# <a name="removed-or-deprecated-platform-features"></a><span data-ttu-id="c4746-103">Fjernede eller avskrevne Platform-funksjoner</span><span class="sxs-lookup"><span data-stu-id="c4746-103">Removed or deprecated platform features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4746-104">Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="c4746-104">This topic describes features that have been removed, or that are planned for removal in platform updates of Finance and Operations apps.</span></span>

- <span data-ttu-id="c4746-105">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="c4746-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="c4746-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="c4746-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="c4746-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="c4746-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="c4746-108">Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="c4746-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="c4746-109">Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="c4746-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="c4746-110">Plattform update 32</span><span class="sxs-lookup"><span data-stu-id="c4746-110">Platform update 32</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="c4746-111">Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg</span><span class="sxs-lookup"><span data-stu-id="c4746-111">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="c4746-112">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="c4746-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="c4746-113">Dette var et sikkerhetsproblem fordi endringsforespørselen kunne sendes til en utilsiktet bruker.</span><span class="sxs-lookup"><span data-stu-id="c4746-113">This was a security issue because the request for change could be sent to an unintended user.</span></span> <span data-ttu-id="c4746-114">Dette var også et bruksproblem, fordi det tvang brukeren til å finne ut hvem arbeidsflytavsenderen var, og manuelt velge dem.</span><span class="sxs-lookup"><span data-stu-id="c4746-114">This was also a usability issue because it forced the user to determine who the workflow originator was and manually select them.</span></span>  |
| <span data-ttu-id="c4746-115">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="c4746-115">**Replaced by another feature?**</span></span>   | <span data-ttu-id="c4746-116">Nei</span><span class="sxs-lookup"><span data-stu-id="c4746-116">No</span></span> |
| <span data-ttu-id="c4746-117">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="c4746-117">**Product areas affected**</span></span>         | <span data-ttu-id="c4746-118">Arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="c4746-118">Workflow</span></span> |
| <span data-ttu-id="c4746-119">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="c4746-119">**Deployment option**</span></span>              | <span data-ttu-id="c4746-120">Alle</span><span class="sxs-lookup"><span data-stu-id="c4746-120">All</span></span> |
| <span data-ttu-id="c4746-121">**Status**</span><span class="sxs-lookup"><span data-stu-id="c4746-121">**Status**</span></span>                         | <span data-ttu-id="c4746-122">Rullegardinlisten for brukervalg ble fjernet fra dialogboksen for forespørselsendring i Platform Update 32.</span><span class="sxs-lookup"><span data-stu-id="c4746-122">The user selection drop-down list was removed from the request change dialog box in Platform update 32.</span></span> <span data-ttu-id="c4746-123">Forespørsler om forespørselsendring sendes automatisk til avsenderen som planlagt.</span><span class="sxs-lookup"><span data-stu-id="c4746-123">Request change requests will be automatically sent to the originator as intended.</span></span> <span data-ttu-id="c4746-124">Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Handlinger i godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span><span class="sxs-lookup"><span data-stu-id="c4746-124">For more information about this functionality, see [Actions in workflow approval processes](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="c4746-125">Tidligere kunngjøringer om fjernede eller avskrevne funksjoner</span><span class="sxs-lookup"><span data-stu-id="c4746-125">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="c4746-126">Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="c4746-126">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../migration-upgrade/deprecated-features.md).</span></span>

