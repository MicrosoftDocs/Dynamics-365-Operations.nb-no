---
title: Synkroniser prosjektaktiviteter fra Project Service Automation
description: "Dette emnet beskriver malen og underliggende oppgave som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: nb-no
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="d1024-103">Synkroniser prosjektaktiviteter fra Project Service Automation direkte til prosjektaktiviteter i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1024-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="d1024-104">Dette emnet beskriver malen og underliggende oppgave som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1024-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="d1024-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="d1024-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="d1024-106">Dataflyt for Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1024-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="d1024-107">Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1024-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="d1024-108">Integreringsmalen som er tilgjengelig med dataintegreringsfunksjonen muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1024-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d1024-109">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1024-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="d1024-110">[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="d1024-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="d1024-111">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="d1024-111">Template and task</span></span>

<span data-ttu-id="d1024-112">Hvis du vil åpne malen, velg **Prosjekter** i Microsoft PowerApps Admin Center, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="d1024-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d1024-113">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="d1024-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="d1024-114">-**Navnet på malen i Dataintegrasjon:** Prosjektoppgaver (PSA til Fin and Ops) -**Navnet på oppgaven i prosjektet:** Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="d1024-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="d1024-115">Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="d1024-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d1024-116">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="d1024-116">Entity set</span></span>

|<span data-ttu-id="d1024-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d1024-117">Project Service Automation</span></span>               | <span data-ttu-id="d1024-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d1024-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="d1024-119">Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="d1024-119">Project Tasks</span></span>                           | <span data-ttu-id="d1024-120">Integreringsenhet for prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="d1024-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="d1024-121">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="d1024-121">Entity flow</span></span>

<span data-ttu-id="d1024-122">Prosjektaktiviteter administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="d1024-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d1024-123">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="d1024-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="d1024-124">Før synkronisering av prosjektaktiviteter kan skje, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="d1024-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="d1024-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="d1024-125">Power Query</span></span>

<span data-ttu-id="d1024-126">Du må bruke Microsoft Power Query til å filtrere data hvis disse betingelsene er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="d1024-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="d1024-127">Du har ressursspesifikke poster i en prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="d1024-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="d1024-128">Hvis du må bruke Power Query, følger du disse retningslinjene:</span><span class="sxs-lookup"><span data-stu-id="d1024-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="d1024-129">Prosjektoppgaver-malen (PSA til Fin and Ops) har et standardfilter for å utelate ressursspesifikke poster fra en prosjektoppgave ved å angi filteret i **IsLineTask** til **Usann**.</span><span class="sxs-lookup"><span data-stu-id="d1024-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="d1024-130">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="d1024-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d1024-131">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="d1024-131">Template mapping in Data integration</span></span>

<span data-ttu-id="d1024-132">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="d1024-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="d1024-133">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d1024-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d1024-134">[![Tilordning av mal](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="d1024-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


