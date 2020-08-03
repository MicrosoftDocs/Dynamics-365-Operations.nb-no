---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597122"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="2f24a-103">Funksjoner som er fjernet eller avskrevet i Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="2f24a-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f24a-104">Dette emnet vil bli oppdatert når fjernede eller avskrevne funksjoner er dokumentert for Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2f24a-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="2f24a-105">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="2f24a-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2f24a-106">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="2f24a-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2f24a-107">Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging.</span><span class="sxs-lookup"><span data-stu-id="2f24a-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="2f24a-108">Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="2f24a-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="2f24a-109">Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="2f24a-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="2f24a-110">Fjernede eller avskrevne funksjoner i Supply Chain Management 10.0.11</span><span class="sxs-lookup"><span data-stu-id="2f24a-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="2f24a-111">Bruk av innebygd hovedplanleggingsmotor Supply Chain Management for distribusjonscenarioer</span><span class="sxs-lookup"><span data-stu-id="2f24a-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="2f24a-112">**Årsak til avskrivning/fjerning**</span><span class="sxs-lookup"><span data-stu-id="2f24a-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="2f24a-113">For å forbedre ytelsen og redusere SQL-databasebelastningen under kjøring av hovedplanlegging, blir den innebygde Supply Chain Management-hovedplanleggingsmotoren erstattet av Planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="2f24a-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="2f24a-114">Planleggingsoptimalisering gjør det mulig å utføre raske planleggingskjøringer som kan utføres selv i kontortiden.</span><span class="sxs-lookup"><span data-stu-id="2f24a-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="2f24a-115">Dette gjør at planleggerne kan reagere umiddelbart på endringer i behovs- eller planleggingsparametere.</span><span class="sxs-lookup"><span data-stu-id="2f24a-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="2f24a-116">**Erstattet med en annen funksjon?**</span><span class="sxs-lookup"><span data-stu-id="2f24a-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="2f24a-117">Ja, planleggingsoptimalisering erstatter den eksisterende innebygde planleggingsmotoren Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="2f24a-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="2f24a-118">**Berørte produktområder**</span><span class="sxs-lookup"><span data-stu-id="2f24a-118">**Product areas affected**</span></span>         | <span data-ttu-id="2f24a-119">Supply Chain Management – Hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="2f24a-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="2f24a-120">**Distribusjonsalternativ**</span><span class="sxs-lookup"><span data-stu-id="2f24a-120">**Deployment option**</span></span>              | <span data-ttu-id="2f24a-121">Bare sky.</span><span class="sxs-lookup"><span data-stu-id="2f24a-121">Cloud only.</span></span> <span data-ttu-id="2f24a-122">Planleggingsoptimalisering ikke med lokale distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="2f24a-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="2f24a-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="2f24a-123">**Status**</span></span>                         | <span data-ttu-id="2f24a-124">Avskrevet.</span><span class="sxs-lookup"><span data-stu-id="2f24a-124">Deprecated.</span></span> <span data-ttu-id="2f24a-125">Fra april 2021 vil distribusjonsscenarioer ikke lenger støttes med den innebygde Dynamics 365 Supply Chain Management-hovedplanleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="2f24a-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="2f24a-126">For distribusjonsscenarioer må kunder bruke planleggingsoptimalisering for hovedplanleggingsberegninger.</span><span class="sxs-lookup"><span data-stu-id="2f24a-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="2f24a-127">Hvis du vil ha mer informasjon, se [dokumentasjon for planleggingsoptimalisering](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="2f24a-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="2f24a-128">Kunder som har lokale distribusjoner av Dynamics 365 Supply Chain Management, kan fortsette å bruke Supply Chain Management-hovedplanleggingsmotoren for distribusjonscenarioer etter april 2021.</span><span class="sxs-lookup"><span data-stu-id="2f24a-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="2f24a-129">Det vil imidlertid ikke bli gitt flere funksjonsforbedringer.</span><span class="sxs-lookup"><span data-stu-id="2f24a-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="2f24a-130">Tidligere kunngjøringer om fjernede eller avskrevne funksjoner</span><span class="sxs-lookup"><span data-stu-id="2f24a-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="2f24a-131">Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="2f24a-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
