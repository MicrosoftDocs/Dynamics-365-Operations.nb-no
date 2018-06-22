---
title: Project Service Automation
description: "Denne løsningen bruker dataintegreringsfunksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="0f469-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0f469-103">Project Service Automation</span></span>

<span data-ttu-id="0f469-104">Project Service Automation til Finance and Operations-integreringsløsningen bruker dataintegreringsfunksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="0f469-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="0f469-105">Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="0f469-106">Hvis du bruker Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, må du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="0f469-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="0f469-107">Dermed kan du integrere fastprisprosjekter.</span><span class="sxs-lookup"><span data-stu-id="0f469-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="0f469-108">Hvis du bruker Dynamics 365 for Finance and Operations versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="0f469-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="0f469-109">Hvis du bruker Dynamics 365 for Finance and Operations versjon 8.0.1, vil du kunne synkronisere faktiske data.</span><span class="sxs-lookup"><span data-stu-id="0f469-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="0f469-110">Hvis du bruker Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing.</span><span class="sxs-lookup"><span data-stu-id="0f469-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="0f469-111">Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="0f469-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="0f469-112">Før du kan integrere Project Service Automation med Finance and Operations, må du konfigurere Project Service Automation-integrasjonsparameterne.</span><span class="sxs-lookup"><span data-stu-id="0f469-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="0f469-113">Hvis du vil ha mer informasjon, kan du se Project Service Automation-integreringsparameterne.</span><span class="sxs-lookup"><span data-stu-id="0f469-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="0f469-114">Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:</span><span class="sxs-lookup"><span data-stu-id="0f469-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="0f469-115">Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-116">Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-117">Oppretthold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-118">Oppretthold milepæler på prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-119">Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-120">Oppretthold utgiftstransaksjonskategorier i Finance and Operations, og synkroniser dem direkte fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="0f469-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="0f469-121">Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="0f469-122">Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="0f469-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="0f469-123">Data synchronization</span></span>
<span data-ttu-id="0f469-124">Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f469-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="0f469-125">Ikke alle maler er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="0f469-125">Not all templates are currently available.</span></span> <span data-ttu-id="0f469-126">Maler gis ut når de er fullført.</span><span class="sxs-lookup"><span data-stu-id="0f469-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="0f469-127">[![Project Service Automation-integrasjon med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="0f469-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="0f469-128">Systemkrav for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f469-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="0f469-129">Hvis du vil bruke Project Service Automation to Finance and Operations-integrasjonsløsningen, må du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med plattformoppdatering 12 eller senere.</span><span class="sxs-lookup"><span data-stu-id="0f469-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="0f469-130">Systemkrav for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0f469-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="0f469-131">Hvis du vil bruke Project Service Automation til Finance and Operations-integrasjonsløsningen, må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="0f469-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="0f469-132">Microsoft Dynamics 365 for Project Service Automation versjon 9.0.0.0 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="0f469-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="0f469-133">Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere.</span><span class="sxs-lookup"><span data-stu-id="0f469-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="0f469-134">Project Service Automation til Operations-løsningen for Dynamics 365 for Project Service Automation versjon 1.0.0.0 eller senere.</span><span class="sxs-lookup"><span data-stu-id="0f469-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="0f469-135">Installer Project Service Automation til Finance and Operations-integrasjonsløsningen i Project Service Automation-forekomsten</span><span class="sxs-lookup"><span data-stu-id="0f469-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



