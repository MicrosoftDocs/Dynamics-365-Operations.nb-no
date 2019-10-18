---
title: Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgavene direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 977037f0e2b313ebf05a3e1616d34567f82e82d7
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250398"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c3a20-103">Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c3a20-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3a20-104">Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgavene direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c3a20-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c3a20-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="c3a20-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="c3a20-106">Hvis du bruker Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du kan konfigurere funksjonslåsing.</span><span class="sxs-lookup"><span data-stu-id="c3a20-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c3a20-107">Hvis du må tilbakestille regnskapsdistribusjonene, anbefalte vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="c3a20-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="c3a20-108">Integrasjon av faktiske data er tilgjengelig i versjon 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="c3a20-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c3a20-109">Dataflyt for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="c3a20-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c3a20-110">Project Service Automation til Finance-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="c3a20-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c3a20-111">Integreringsmalen som er tilgjengelig med dataintegreringsfunksjonen muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="c3a20-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3a20-112">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="c3a20-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c3a20-113">[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c3a20-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="c3a20-114">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="c3a20-114">Template and task</span></span>

<span data-ttu-id="c3a20-115">For å få tilgang til malen velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="c3a20-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c3a20-116">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="c3a20-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c3a20-117">**Navnet på malen i Dataintegrering:** Prosjektoppgaver (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c3a20-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c3a20-118">**Navnet på oppgaven i prosjektet:** Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="c3a20-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="c3a20-119">Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c3a20-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c3a20-120">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="c3a20-120">Entity set</span></span>

| <span data-ttu-id="c3a20-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c3a20-121">Project Service Automation</span></span> | <span data-ttu-id="c3a20-122">Finans</span><span class="sxs-lookup"><span data-stu-id="c3a20-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="c3a20-123">Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="c3a20-123">Project Tasks</span></span>              | <span data-ttu-id="c3a20-124">Integreringsenhet for prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="c3a20-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c3a20-125">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="c3a20-125">Entity flow</span></span>

<span data-ttu-id="c3a20-126">Prosjektaktiviteter administreres i Project Service Automation, og de synkroniseres til Finance som prosjektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="c3a20-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c3a20-127">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="c3a20-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="c3a20-128">Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="c3a20-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="c3a20-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="c3a20-129">Power Query</span></span>

<span data-ttu-id="c3a20-130">Du må bruke Microsoft Power Query for Excel til å filtrere data hvis denne betingelsen er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="c3a20-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="c3a20-131">Du har ressursspesifikke poster i en prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="c3a20-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="c3a20-132">Hvis du må bruke Power Query, følger du disse retningslinjene:</span><span class="sxs-lookup"><span data-stu-id="c3a20-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="c3a20-133">Prosjektoppgaver-malen (PSA til Fin and Ops) har et standardfilter som utelater ressursspesifikke poster fra en prosjektoppgave ved å angi filteret i **IsLineTask** til **Usann**.</span><span class="sxs-lookup"><span data-stu-id="c3a20-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="c3a20-134">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="c3a20-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c3a20-135">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="c3a20-135">Template mapping in Data integration</span></span>

<span data-ttu-id="c3a20-136">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="c3a20-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="c3a20-137">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="c3a20-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c3a20-138">[![Tilordning av mal](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="c3a20-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
