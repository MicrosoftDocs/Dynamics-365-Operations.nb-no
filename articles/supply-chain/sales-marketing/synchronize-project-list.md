---
title: Synkronisere prosjektliste fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "312514"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1873c-103">Synkronisere prosjektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="1873c-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1873c-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1873c-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1873c-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1873c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1873c-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="1873c-106">Templates and tasks</span></span>
<span data-ttu-id="1873c-107">Følgende mal og underliggende oppgavene brukes til å utføre synkronisering av prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1873c-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1873c-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="1873c-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1873c-109">Prosjekter (Finance and Operations til Field Service)</span><span class="sxs-lookup"><span data-stu-id="1873c-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="1873c-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="1873c-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1873c-111">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1873c-111">Projects</span></span>

<span data-ttu-id="1873c-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="1873c-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1873c-113">Kontoer (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="1873c-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1873c-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="1873c-114">Entity set</span></span>
| <span data-ttu-id="1873c-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1873c-115">Field Service</span></span>           | <span data-ttu-id="1873c-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1873c-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1873c-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1873c-117">msdynce_externalprojects</span></span> | <span data-ttu-id="1873c-118">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1873c-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1873c-119">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="1873c-119">Entity flow</span></span>
<span data-ttu-id="1873c-120">Prosjekter opprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1873c-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="1873c-121">Prosjekter med **Prosjekttype** satt til **Tid og materialer** og **Prosjektstadium** satt til **Pågår**, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto.</span><span class="sxs-lookup"><span data-stu-id="1873c-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="1873c-122">Listen over **Eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Finance and Operations-prosjekter.</span><span class="sxs-lookup"><span data-stu-id="1873c-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1873c-123">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="1873c-123">Field Service CRM solution</span></span>
<span data-ttu-id="1873c-124">**Eksternt prosjekt**-enheten får alle prosjektene fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1873c-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="1873c-125">Feltet **Eksternt prosjekt** er lagt til **Arbeidsordre**-enheten.</span><span class="sxs-lookup"><span data-stu-id="1873c-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="1873c-126">Dette er et oppslagsfelt, så ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1873c-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="1873c-127">Når **Systemstatus** endrer **Åpen – pågår(690,970,000)** til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="1873c-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1873c-128">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="1873c-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="1873c-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1873c-129">Finance and Operations</span></span>
<span data-ttu-id="1873c-130">Aktivere endringssporing for dataenhetsprosjekter.</span><span class="sxs-lookup"><span data-stu-id="1873c-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1873c-131">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="1873c-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="1873c-132">Prosjekter (Finance and Operations til Field Service): Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1873c-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="1873c-133">[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1873c-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
