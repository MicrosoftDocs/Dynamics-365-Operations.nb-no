---
title: Synkronisere prosjektliste fra Supply Chain Management til Field Service
description: Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3d17b226cabd0668bcdb52e9a7fdfc5973fe49b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243063"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="1188b-103">Synkronisere prosjektliste fra Supply Chain Management til Field Service</span><span class="sxs-lookup"><span data-stu-id="1188b-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1188b-104">Dette emnet omhandler malene og de underliggende oppgavene som brukes til å synkronisere prosjekter fra Dynamics 365 Supply Chain Management til Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1188b-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="1188b-105">[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="1188b-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="1188b-106">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="1188b-106">Templates and tasks</span></span>
<span data-ttu-id="1188b-107">Følgende mal og underliggende oppgaver brukes til å utføre synkronisering av prosjekter fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="1188b-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="1188b-108">**Mal i Dataintegrasjon**</span><span class="sxs-lookup"><span data-stu-id="1188b-108">**Template in Data integration**</span></span>
- <span data-ttu-id="1188b-109">Prosjekter (Supply Chain Management til Field Service)</span><span class="sxs-lookup"><span data-stu-id="1188b-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="1188b-110">**Oppgave i Dataintegrasjonprosjektet**:</span><span class="sxs-lookup"><span data-stu-id="1188b-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="1188b-111">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1188b-111">Projects</span></span>

<span data-ttu-id="1188b-112">Følgende synkroniseringsoppgaver er påkrevd før synkronisering av prosjektliste kan inntreffe:</span><span class="sxs-lookup"><span data-stu-id="1188b-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="1188b-113">Kontoer (Sales til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="1188b-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="1188b-114">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="1188b-114">Entity set</span></span>
| <span data-ttu-id="1188b-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="1188b-115">Field Service</span></span>           | <span data-ttu-id="1188b-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1188b-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="1188b-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="1188b-117">msdynce_externalprojects</span></span> | <span data-ttu-id="1188b-118">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1188b-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="1188b-119">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="1188b-119">Entity flow</span></span>
<span data-ttu-id="1188b-120">Prosjekter opprettes i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1188b-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="1188b-121">Prosjekter med **Prosjekttype** satt til **Tid og materialer** og **Prosjektstadium** satt til **Pågår**, synkroniseres til **Eksternt prosjekt**-enheten i Field Service, inkludert prosjektnummer, prosjektnavn, prosjektstadium og informasjon om kundekonto.</span><span class="sxs-lookup"><span data-stu-id="1188b-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="1188b-122">Listen over **Eksternt prosjekt** brukes til å sammenkoble Field Service-arbeidsordrer med Supply Chain Management-prosjekter.</span><span class="sxs-lookup"><span data-stu-id="1188b-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="1188b-123">CRM-løsning for Field Service</span><span class="sxs-lookup"><span data-stu-id="1188b-123">Field Service CRM solution</span></span>
<span data-ttu-id="1188b-124">**Eksternt prosjekt**-enheten får alle prosjektene fra Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1188b-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="1188b-125">Feltet **Eksternt prosjekt** er lagt til **Arbeidsordre**-enheten.</span><span class="sxs-lookup"><span data-stu-id="1188b-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="1188b-126">Dette er et oppslagsfelt, så ved å kode arbeidsordren med et prosjekt, kobles salgsordren til et prosjekt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1188b-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="1188b-127">Når **Systemstatus** endrer **Åpen – pågår(690,970,000)** til en høyere status, låses feltet **Eksternt prosjekt**, og du kan ikke legge til, fjerne eller endre verdien.</span><span class="sxs-lookup"><span data-stu-id="1188b-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="1188b-128">Forutsetninger og tilordningsdefinisjon</span><span class="sxs-lookup"><span data-stu-id="1188b-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="1188b-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="1188b-129">Supply Chain Management</span></span>
<span data-ttu-id="1188b-130">Aktivere endringssporing for dataenhetsprosjekter.</span><span class="sxs-lookup"><span data-stu-id="1188b-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1188b-131">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="1188b-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="1188b-132">Prosjekter (Supply Chain Management til Field Service): Prosjekter</span><span class="sxs-lookup"><span data-stu-id="1188b-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="1188b-133">[![Maltilordning i Dataintegrering](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="1188b-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]