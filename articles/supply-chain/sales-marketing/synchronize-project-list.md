---
title: Synkronisere prosjektliste fra Finance and Operations til Field Service
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: nb-no
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="10a61-103">Synkronisere prosjektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="10a61-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10a61-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="10a61-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="10a61-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="10a61-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="10a61-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="10a61-106">Templates and tasks</span></span>
<span data-ttu-id="10a61-107">Følgende mal og underliggende oppgaver brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="10a61-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="10a61-108">**Navnet på malen i Dataintegrasjon:**</span><span class="sxs-lookup"><span data-stu-id="10a61-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="10a61-109">Prosjekter (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="10a61-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="10a61-110">**Navnet på oppgaven i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="10a61-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="10a61-111">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="10a61-111">Projects</span></span>

<span data-ttu-id="10a61-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="10a61-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="10a61-113">Kontoer (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="10a61-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="10a61-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="10a61-114">Entity set</span></span>
<span data-ttu-id="10a61-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10a61-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="10a61-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="10a61-116">Field Service</span></span>           | <span data-ttu-id="10a61-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="10a61-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="10a61-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="10a61-118">msdynce_externalprojects</span></span> | <span data-ttu-id="10a61-119">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="10a61-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="10a61-120">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="10a61-120">Entity flow</span></span>
<span data-ttu-id="10a61-121">Prosjekter opprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="10a61-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="10a61-122">Prosjekter med **prosjekttype** Etter regning og **Prosjektstadium** som pågår, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto.</span><span class="sxs-lookup"><span data-stu-id="10a61-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="10a61-123">Listen over **eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Finance and Operations-prosjekter.</span><span class="sxs-lookup"><span data-stu-id="10a61-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="10a61-124">Field Service CRM-løsningen Det eksterne prosjektet er en ny enhet som henter alle prosjektene fra Operations.</span><span class="sxs-lookup"><span data-stu-id="10a61-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="10a61-125">Feltet Eksternt prosjekt er lagt til arbeidsordreenheten.</span><span class="sxs-lookup"><span data-stu-id="10a61-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="10a61-126">Dette feltet er et oppslag og ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Operations.</span><span class="sxs-lookup"><span data-stu-id="10a61-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="10a61-127">Når systemstatusen endres fra Åpen – pågår(690,970,000) til en høyere status, låses feltet Eksternt prosjekt, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="10a61-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="10a61-128">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="10a61-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="10a61-129">I Finance og Operations</span><span class="sxs-lookup"><span data-stu-id="10a61-129">In Finance and Operations</span></span>
<span data-ttu-id="10a61-130">Aktivere endringssporing for dataenhetsprosjekter</span><span class="sxs-lookup"><span data-stu-id="10a61-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="10a61-131">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="10a61-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="10a61-132">Prosjekter (Finance and Operations til Field Service): Prosjekter</span><span class="sxs-lookup"><span data-stu-id="10a61-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="10a61-133">[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="10a61-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

