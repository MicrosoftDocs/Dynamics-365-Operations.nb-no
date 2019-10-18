---
title: Oversikt over Project Service Automation
description: Dette emnet inneholder informasjon om integreringsløsningen Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250559"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="ab029-103">Oversikt over Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab029-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab029-104">Løsningen Project Service Automation til Finance bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ab029-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="ab029-105">Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ab029-106">Hvis du bruker versjon 7.3.0, må du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="ab029-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="ab029-107">Du vil da kunne integrere fastprisprosjekter.</span><span class="sxs-lookup"><span data-stu-id="ab029-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="ab029-108">Hvis du bruker versjon 7.3.0, og du henter gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å inkludere disse gebyrene i prosjektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="ab029-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="ab029-109">Hvis du bruker versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="ab029-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="ab029-110">Hvis du bruker versjon 8.0.1 eller nyere, vil du ikke kunne synkronisere faktiske data.</span><span class="sxs-lookup"><span data-stu-id="ab029-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="ab029-111">Før du kan integrere Project Service Automation med Finance, må du konfigurere Project Service Automation-integrasjonsparameterne.</span><span class="sxs-lookup"><span data-stu-id="ab029-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="ab029-112">Hvis du vil ha mer informasjon, kan du se [Project Service Automation-integreringsparameterne](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ab029-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="ab029-113">Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:</span><span class="sxs-lookup"><span data-stu-id="ab029-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="ab029-114">Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-115">Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-116">Oppretthold prosjektkontraktslinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-117">Oppretthold milepæler på prosjektkontraktlinje i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-118">Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-119">Oppretthold utgiftstransaksjonskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ab029-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="ab029-120">Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-121">Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ab029-122">Opprett faktiske data for prosjekttid, utgifter og avgifter i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="ab029-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="ab029-123">Data synchronization</span></span>

<span data-ttu-id="ab029-124">Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="ab029-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="ab029-125">Ikke alle maler er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="ab029-125">Not all templates are currently available.</span></span> <span data-ttu-id="ab029-126">Maler gis ut når de er fullført.</span><span class="sxs-lookup"><span data-stu-id="ab029-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="ab029-127">[![Integrering av Project Service Automation med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="ab029-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="ab029-128">Systemkrav for Finance</span><span class="sxs-lookup"><span data-stu-id="ab029-128">System requirements for Finance</span></span>

<span data-ttu-id="ab029-129">Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere Enterprise Edition 7.3 med Platform update 12 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="ab029-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="ab029-130">Systemkrav for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ab029-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="ab029-131">Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="ab029-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="ab029-132">Dynamics 365 Project Service Automation versjon 9.0.0.0 eller senere</span><span class="sxs-lookup"><span data-stu-id="ab029-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="ab029-133">Kundeemne til kontanter-løsningen for Dynamics 365 Sales, versjon 1.14.0.0 (v14) eller nyere.</span><span class="sxs-lookup"><span data-stu-id="ab029-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="ab029-134">Project Service Automation til Finance-løsning for Dynamics 365 Project Service Automation versjon 1.0.0.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="ab029-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="ab029-135">Installer Project Service Automation til Finance-integrasjonsløsningen i Project Service Automation-forekomsten</span><span class="sxs-lookup"><span data-stu-id="ab029-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="ab029-136">Last ned Project Service Automation til Finance-integrasjonsløsningen fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.</span><span class="sxs-lookup"><span data-stu-id="ab029-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
