---
title: Project Service Automation
description: Dette emnet gir informasjon om integrasjonsløsningen Project Service Automation til Finance and Operations. Denne integreringsløsningen bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1d6d0b219666bb31cf08da580c701f93d08389a
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741228"
---
# <a name="project-service-automation"></a><span data-ttu-id="390fa-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="390fa-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="390fa-105">Løsningen Project Service Automation til Finance and Operations bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="390fa-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="390fa-106">Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="390fa-107">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing.</span><span class="sxs-lookup"><span data-stu-id="390fa-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="390fa-108">Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="390fa-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="390fa-109">Hvis du bruker Finance and Operations 7.3.0, må du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="390fa-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="390fa-110">Du vil da kunne integrere fastprisprosjekter.</span><span class="sxs-lookup"><span data-stu-id="390fa-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="390fa-111">Hvis du bruker Finance and Operations 7.3.0, og du henter gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å inkludere disse gebyrene i prosjektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="390fa-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="390fa-112">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="390fa-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="390fa-113">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere, vil du ikke kunne synkronisere faktiske data.</span><span class="sxs-lookup"><span data-stu-id="390fa-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="390fa-114">Før du kan integrere Project Service Automation med Finance and Operations, må du konfigurere Project Service Automation-integrasjonsparameterne.</span><span class="sxs-lookup"><span data-stu-id="390fa-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="390fa-115">Hvis du vil ha mer informasjon, kan du se [Project Service Automation-integreringsparameterne](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="390fa-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="390fa-116">Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:</span><span class="sxs-lookup"><span data-stu-id="390fa-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="390fa-117">Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-118">Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-119">Oppretthold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-120">Oppretthold milepæler på prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-121">Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-122">Oppretthold utgiftstransaksjonskategorier i Finance and Operations, og synkroniser dem direkte fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="390fa-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="390fa-123">Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-124">Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="390fa-125">Opprett faktiske data for prosjekttid, utgifter og avgifter i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="390fa-126">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="390fa-126">Data synchronization</span></span>

<span data-ttu-id="390fa-127">Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="390fa-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="390fa-128">Ikke alle maler er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="390fa-128">Not all templates are currently available.</span></span> <span data-ttu-id="390fa-129">Maler gis ut når de er fullført.</span><span class="sxs-lookup"><span data-stu-id="390fa-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="390fa-130">[![Project Service Automation-integrasjon med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="390fa-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="390fa-131">Systemkrav for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="390fa-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="390fa-132">Hvis du vil bruke Project Service Automation to Finance and Operations-integrasjonsløsningen, må du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 med plattformoppdatering 12 eller senere.</span><span class="sxs-lookup"><span data-stu-id="390fa-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="390fa-133">Systemkrav for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="390fa-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="390fa-134">Hvis du vil bruke Project Service Automation til Finance and Operations-integrasjonsløsningen, må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="390fa-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="390fa-135">Microsoft Dynamics 365 for Project Service Automation versjon 9.0.0.0 eller senere</span><span class="sxs-lookup"><span data-stu-id="390fa-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="390fa-136">Kundeemne til kontanter-løsningen for Microsoft Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere</span><span class="sxs-lookup"><span data-stu-id="390fa-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="390fa-137">Project Service Automation til Finance and Operations-løsning for Microsoft Dynamics 365 for Project Service Automation versjon 1.0.0.0 eller senere</span><span class="sxs-lookup"><span data-stu-id="390fa-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="390fa-138">Installer Project Service Automation til Finance and Operations-integrasjonsløsningen i Project Service Automation-forekomsten</span><span class="sxs-lookup"><span data-stu-id="390fa-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="390fa-139">Last ned Project Service Automation til Finance and Operations-integrasjonsløsningen fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.</span><span class="sxs-lookup"><span data-stu-id="390fa-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
