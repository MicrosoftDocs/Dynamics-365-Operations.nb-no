---
title: Synkronisere prosjektliste fra Finance and Operations til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525883"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="1c3dc-103">Synkronisere prosjektliste fra Finance and Operations til Field Service</span><span class="sxs-lookup"><span data-stu-id="1c3dc-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1c3dc-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1c3dc-105">[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1c3dc-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1c3dc-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="1c3dc-106">Templates and tasks</span></span>
<span data-ttu-id="1c3dc-107">Følgende mal og underliggende oppgavene brukes til å utføre synkronisering av prosjekter fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="1c3dc-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="1c3dc-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1c3dc-109">Prosjekter (Fin and Ops til Field Service)</span><span class="sxs-lookup"><span data-stu-id="1c3dc-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="1c3dc-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="1c3dc-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1c3dc-111">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1c3dc-111">Projects</span></span>

<span data-ttu-id="1c3dc-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="1c3dc-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1c3dc-113">Kontoer (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="1c3dc-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1c3dc-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="1c3dc-114">Entity set</span></span>
| <span data-ttu-id="1c3dc-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1c3dc-115">Field Service</span></span>           | <span data-ttu-id="1c3dc-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1c3dc-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1c3dc-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1c3dc-117">msdynce_externalprojects</span></span> | <span data-ttu-id="1c3dc-118">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1c3dc-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1c3dc-119">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="1c3dc-119">Entity flow</span></span>
<span data-ttu-id="1c3dc-120">Prosjekter opprettes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="1c3dc-121">Prosjekter med **Prosjekttype** satt til **Tid og materialer** og **Prosjektstadium** satt til **Pågår**, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="1c3dc-122">Listen over **Eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Finance and Operations-prosjekter.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1c3dc-123">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="1c3dc-123">Field Service CRM solution</span></span>
<span data-ttu-id="1c3dc-124">**Eksternt prosjekt**-enheten får alle prosjektene fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="1c3dc-125">Feltet **Eksternt prosjekt** er lagt til **Arbeidsordre**-enheten.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="1c3dc-126">Dette er et oppslagsfelt, så ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="1c3dc-127">Når **Systemstatus** endrer **Åpen – pågår(690,970,000)** til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1c3dc-128">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="1c3dc-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="1c3dc-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1c3dc-129">Finance and Operations</span></span>
<span data-ttu-id="1c3dc-130">Aktivere endringssporing for dataenhetsprosjekter.</span><span class="sxs-lookup"><span data-stu-id="1c3dc-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1c3dc-131">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="1c3dc-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="1c3dc-132">Prosjekter (Fin and Ops til Field Service): Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1c3dc-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="1c3dc-133">[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1c3dc-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
