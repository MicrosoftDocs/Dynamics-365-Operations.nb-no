---
title: Prognoser, arbeidsordrer og prosjekter
description: Dette emnet beskriver prognoser og arbeidsordreintegrering med modulen Prosjektstyring og regnskap i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886822"
---
# <a name="forecasts-work-orders-and-projects"></a><span data-ttu-id="3dcee-103">Prognoser, arbeidsordrer og prosjekter</span><span class="sxs-lookup"><span data-stu-id="3dcee-103">Forecasts, work orders, and projects</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3dcee-104">I Aktivastyring gjøres integreringen til modulen **Prosjektstyring og regnskap** for å optimalisere kostnadskontroll, slik at brukere kan spore kostnader for prognoser ved vedlikeholdsjobbtype og arbeidsordrejobber.</span><span class="sxs-lookup"><span data-stu-id="3dcee-104">In Asset Management, integration to the **Project management and accounting** module is done to optimize cost control, allowing users to track costs on maintenance job type forecasts and work order jobs.</span></span>

<span data-ttu-id="3dcee-105">To innstillinger må gjøres for å spore prognoser for vedlikeholdsjobbtype:</span><span class="sxs-lookup"><span data-stu-id="3dcee-105">To track maintenance job type forecasts, two settings must be made:</span></span>

1. <span data-ttu-id="3dcee-106">Velg et prosjekt i **Aktivastyring** > **Oppsett** > **Parametere for aktivastyring** > **Aktiva** kobling > **Prosjekt**-hurtigfanen> feltet **Vedlikeholdsprognoseprosjekt**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-106">Select a project in **Asset management** > **Setup** > **Asset management parameters** > **Assets** link > **Project** FastTab > **Maintenance forecast project** field.</span></span>

2. <span data-ttu-id="3dcee-107">Når du oppretter en standardlinje for vedlikeholdsjobbtype i **Standarder for vedlikeholdsjobbtype**, opprettes automatisk et aktivitetsnummer for linjen (**Aktivastyring** > **Oppsett** > **Jobber** > **Standarder for vedlikeholdsjobbtype**).</span><span class="sxs-lookup"><span data-stu-id="3dcee-107">In **Maintenance job type defaults**, when you create a mainteance job type default line, an activity number is automatically created for the line (**Asset management** > **Setup** > **Jobs** > **Maintenance job type defaults**).</span></span>

<span data-ttu-id="3dcee-108">Prognoser for vedlikeholdsjobbtype har to formål: Du kan spore kostnader ved prognoser for vedlikeholdsjobbtype i modulen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-108">Maintenance job type forecasts serve two purposes: You are able to track costs on maintenance job type forecasts in the **Project management and accounting** module.</span></span> <span data-ttu-id="3dcee-109">I tillegg overføres prognoser automatisk til et arbeidsordrejobbprosjekt når du velger en vedlikeholdsjobbtype i en arbeidsordrejobb.</span><span class="sxs-lookup"><span data-stu-id="3dcee-109">Furthermore, forecasts are automatically transferred to a work order job project when you select a maintenance job type on a work order job.</span></span>

<span data-ttu-id="3dcee-110">Hvis du vil spore kostnader for arbeidsordrejobber, må du først definere arbeidsordreprosjekter.</span><span class="sxs-lookup"><span data-stu-id="3dcee-110">To track costs on work order jobs, you must first set up work order projects.</span></span> <span data-ttu-id="3dcee-111">Se delen [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md) hvis du vil ha en beskrivelse av fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3dcee-111">Refer to the [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) section for a description of the procedure.</span></span>

## <a name="work-order-job-projects"></a><span data-ttu-id="3dcee-112">Arbeidsordrejobbprosjekter</span><span class="sxs-lookup"><span data-stu-id="3dcee-112">Work order job projects</span></span>

<span data-ttu-id="3dcee-113">Når du oppretter en arbeidsordrejobb i en arbeidsordre, bestemmes arbeidsordreprosjektet av oppsettet for det overordnede prosjektet for arbeidsordrer i **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-113">When you create a work order job on a work order, the work order project is determined by the setup of the parent project for work orders in **Asset management** > **Setup** > **Work orders** > **Project setup**.</span></span>

<span data-ttu-id="3dcee-114">Arbeidsordrejobbprosjekter opprettes ved å bruke en kombinasjon av følgende arbeidsordreinformasjon:</span><span class="sxs-lookup"><span data-stu-id="3dcee-114">Work order job projects are created by using a combination of the following work order information:</span></span>

- <span data-ttu-id="3dcee-115">Arbeidsordretypen som er valgt i arbeidsordren</span><span class="sxs-lookup"><span data-stu-id="3dcee-115">The Work order type selected on the work order</span></span> 
- <span data-ttu-id="3dcee-116">Den funksjonelle lokasjonen som er knyttet til aktivaet i arbeidsordrejobben</span><span class="sxs-lookup"><span data-stu-id="3dcee-116">The functional location related to the asset on the work order job</span></span>
- <span data-ttu-id="3dcee-117">Aktivatypen som er knyttet til aktivaet i arbeidsordrejobben</span><span class="sxs-lookup"><span data-stu-id="3dcee-117">The Asset type related to the asset on the work order job</span></span>  
- <span data-ttu-id="3dcee-118">Det forventede start- og sluttidspunktet som er angitt for arbeidsordren</span><span class="sxs-lookup"><span data-stu-id="3dcee-118">The Expected start and end time set on the work order</span></span>  

<span data-ttu-id="3dcee-119">Det er mulig at ikke all informasjonen som er nevnt ovenfor, blir funnet i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="3dcee-119">It is possible that not all of the information mentioned above is found on a work order.</span></span> <span data-ttu-id="3dcee-120">Derfor utføres søket etter et overordnede prosjekt for arbeidsordre ved å bruke den tilgjengelige kombinasjonen av data og velge prosjekt-IDen som tilsvarer arbeidsordredata.</span><span class="sxs-lookup"><span data-stu-id="3dcee-120">Therefore, the search for a work order parent project is done by using the available combination of data and selecting the project ID that corresponds with work order data.</span></span>

<span data-ttu-id="3dcee-121">Eksempel: I illustrasjonen nedenfor betyr oppsettet av anleggsmiddeltype "lastebilmotor" at alle arbeidsordrejobber som opprettes med denne anleggsmiddeltypen, blir et underprosjekt av prosjekt-ID "000186".</span><span class="sxs-lookup"><span data-stu-id="3dcee-121">Example: In the figure below, the setup of asset type "Truck Engine" means that every work order job created with that asset type will be a sub project of Project ID "000186".</span></span>

![Figur 1](media/01-integration-to-pma.png)

<span data-ttu-id="3dcee-123">Formålet med prosjekt-IDen på arbeidsordrejobben og det relaterte aktivitetsnummeret (**Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** > velg arbeidsordre i liste > **Linjedetaljer** -hurtigfanen **Prosjekt-ID**-feltet og **Aktivitetsnummer**-feltet), er å spore kostnader knyttet til arbeidsordrejobben, og aktivumet som er valgt på arbeidsordrejobben, i modulen **Prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-123">The purpose of the project ID on the work order job, and the related activity number (**Asset management** > **Common** > **Work orders** > **All Work orders** > select work order in list > **Line details** FastTab > **Project ID** field and **Activity number** field), is to track costs related to the work order job, and the asset selected on the work order job, in the **Project management and accounting** module.</span></span> 

<span data-ttu-id="3dcee-124">I figuren nedenfor vises en grafisk oversikt over arbeidsordreprosjekter og relaterte prosjektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="3dcee-124">In the figure below, you see a graphic overview of work order projects and related project activities.</span></span>

![Figur 2](media/02-integration-to-pma.png)

<span data-ttu-id="3dcee-126">Når en ny arbeidsordrejobb blir opprettet i en arbeidsordre, opprettes det automatisk et arbeidsordreprosjekt for jobben.</span><span class="sxs-lookup"><span data-stu-id="3dcee-126">When a new work order job is created on a work order, a work order project is automatically created for the job.</span></span> <span data-ttu-id="3dcee-127">Finansdimensjonene for anleggsmiddelet som er relatert til arbeidsordrejobben, overføres automatisk til arbeidsordreprosjektet.</span><span class="sxs-lookup"><span data-stu-id="3dcee-127">The financial dimensions for the asset related to the work order job are automatically transferred to the work order project.</span></span> <span data-ttu-id="3dcee-128">Prosjektaktiviteten som er opprettet for en arbeidsordrejobb, har relatert informasjon som er knyttet til den for vedlikeholdsjobbtype, variant av vedlikeholdsjobbtype og handel.</span><span class="sxs-lookup"><span data-stu-id="3dcee-128">The project activity created for a work order job has related information attached to it regarding maintenance job type, maintenance job type variant, and trade.</span></span> <span data-ttu-id="3dcee-129">Disse dataene er nyttige hvis du for eksempel oppretter en bestilling fra en arbeidsordre (se [Innkjøp](../work-orders/procurement.md)), eller hvis du bruker modulen **Prosjektstyrings- og Regnskap** for tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="3dcee-129">Those data are useful if, for example, you create a purchase order from a work order (see [Procurement](../work-orders/procurement.md)), or if you use the **Project management and accounting** module for time registration.</span></span>  

<span data-ttu-id="3dcee-130">Hvis anleggsmiddelet ble installert på et arbeidssted, og dette anleggsmiddelet senere installeres på et annet arbeidssted, oppdateres finansdimensjonene som er knyttet til det nye arbeidsstedet, automatisk i anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="3dcee-130">If the asset was installed on a functional location, and that asset is later installed on another functional location, the financial dimensions related to the new functional location is automatically updated on the asset.</span></span> <span data-ttu-id="3dcee-131">Når du deretter oppretter en arbeidsordrejobb for anleggsmiddelet, får arbeidsordreprosjektet for arbeidsordrejobben automatisk finansdimensjonene som nå er knyttet til anleggsmiddelet.</span><span class="sxs-lookup"><span data-stu-id="3dcee-131">Subsequently, when you create a work order job for the asset, the work order project for the work order job automatically gets the financial dimensions that are now related to the asset.</span></span> <span data-ttu-id="3dcee-132">Dette betyr at når du bruker arbeidssteder, kan kostnader alltid spores på arbeidssteder der et aktivum ble installert på et gitt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="3dcee-132">This means that when you use functional locations, costs can always be tracked on the functional locations on which an asset was installed at any given time.</span></span> <span data-ttu-id="3dcee-133">Den automatiske oppdateringen av finansdimensjoner sikrer fullstendig sporing av kostnader for prosjektkontroll og -rapportering.</span><span class="sxs-lookup"><span data-stu-id="3dcee-133">The automatic update of financial dimensions ensures complete traceability of costs for project controlling and reporting.</span></span>  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a><span data-ttu-id="3dcee-134">Arbeidsordreprosjekter, livsløpstilstander for arbeidsordre, prosjektstadier og prosjekttyper</span><span class="sxs-lookup"><span data-stu-id="3dcee-134">Work order projects, work order lifecycle states, project stages, and project types</span></span>

<span data-ttu-id="3dcee-135">For å sikre riktig bruk av livsløpstilstander for arbeidsordre og tilknyttede prosjektstadier på arbeidsordrer, bør du vurdere avhengighetene i relasjon til modulen **Prosjektstyring og regnskap**:</span><span class="sxs-lookup"><span data-stu-id="3dcee-135">To ensure correct use of work order lifecycle states and related project stages on work orders, consider the dependencies in relation to the **Project management and accounting** module:</span></span>

- <span data-ttu-id="3dcee-136">I modulen **Prosjektstyring og regnskap** er prosjektstadier definert for prosjekttyper i **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-136">In the **Project management and accounting** module, project stages are set up on project types in **Project management and accounting parameters**.</span></span>  
- <span data-ttu-id="3dcee-137">I **Parametere for prosjektstyring og regnskap**må du huske å merke av i relevante avmerkingsbokser for prosjektstadiet for alle prosjekttypene du skal bruke.</span><span class="sxs-lookup"><span data-stu-id="3dcee-137">In **Project management and accounting parameters**, remember to select relevant project stage check boxes for all the project types you are going to use.</span></span> <span data-ttu-id="3dcee-138">I figuren nedenfor er de fem stadiene **Opprettet** - **Estimert** - **Planlagt** - **Pågår** - **Fullført** valgt for prosjekttypene "tid og materialer" og "intern".</span><span class="sxs-lookup"><span data-stu-id="3dcee-138">In the figure below, five stages **Created** - **Estimated** - **Scheduled** - **In process** - **Finished** have been selected for the project types "Time and material" and "Internal".</span></span> <span data-ttu-id="3dcee-139">Disse fem stadiene er relevante for både interne vedlikeholdsjobber og servicevedlikeholdsjobber.</span><span class="sxs-lookup"><span data-stu-id="3dcee-139">Those five stages are relevant for both internal maintenance and service maintenance jobs.</span></span>  
- <span data-ttu-id="3dcee-140">I **Aktivastyring** defineres prosjekttyper av prosjektgruppene du definerer i skjemaet **Prosjektoppsett for arbeidsordre** > koblingen **Prosjektgruppe**.</span><span class="sxs-lookup"><span data-stu-id="3dcee-140">In **Asset Management**, project types are defined by the project groups you set up in the **Work order project setup** form > **Project group** link.</span></span>  
- <span data-ttu-id="3dcee-141">Oppsettet av prosjektgrupper i **Prosjektoppsett for arbeidsordre** brukes når du oppretter arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="3dcee-141">The project groups setup in **Work order project setup** are used when you create work orders.</span></span> <span data-ttu-id="3dcee-142">Når en ny arbeidsordre blir opprettet, opprettes det automatisk et arbeidsordreprosjekt for et arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="3dcee-142">When a work order is created, a work order project is automatically created for the work order.</span></span>  
- <span data-ttu-id="3dcee-143">Hver livssyklus for arbeidsordre må ha et tilknyttet prosjektstadium.</span><span class="sxs-lookup"><span data-stu-id="3dcee-143">Work order lifecycle states must each have a related project stage.</span></span>  
- <span data-ttu-id="3dcee-144">Prosjektstadiet som er knyttet til en livsløpstilstand for arbeidsordre, må defineres som en aktiv fase for prosjektgruppen som er definert i arbeidsordreprosjektet.</span><span class="sxs-lookup"><span data-stu-id="3dcee-144">The project stage related to a work order lifecycle state must be defined as an active stage for the project group defined in the work order project.</span></span> <span data-ttu-id="3dcee-145">Arbeidsordreprosjektet opprettes automatisk i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="3dcee-145">The work order project is automatically created on a work order.</span></span>  
- <span data-ttu-id="3dcee-146">Når du oppretter en ny arbeidsordre, er den automatiske tilordningen av et arbeidsordreprosjekt basert på oppsettet i **Prosjektoppsett for arbeidsordre** (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Prosjektoppsett**).</span><span class="sxs-lookup"><span data-stu-id="3dcee-146">When you create a new work order, the automatic allocation of a work order project is based on the setup in **Work order project setup** (**Asset management** > **Setup** > **Work orders** > **Project setup**).</span></span>  

<span data-ttu-id="3dcee-147">Tilknytninger mellom arbeidsordreprosjektgrupper, tilknyttede prosjekttyper, prosjektstadier og livssyklustilstander for arbeidsordre vises i figurene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="3dcee-147">Associations between work order project groups, related project types, project stages, and work order lifecycle states are shown in the figures below.</span></span>  

![Figur 3](media/03-integration-to-pma.png)

![Figur 4](media/04-integration-to-pma.png)

![Figur 5](media/05-integration-to-pma.png)

<span data-ttu-id="3dcee-151">Se [Prosjektoppsett for arbeidsordre](../setup-for-work-orders/work-order-project-setup.md) for informasjon om hvordan du definerer arbeidsordreprosjekter, og [Livssyklustilstander for arbeidsordre](../setup-for-work-orders/work-order-lifecycle-states.md) for informasjon om hvordan du oppretter livssyklustilstander for arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="3dcee-151">Refer to [Work order project setup](../setup-for-work-orders/work-order-project-setup.md) regarding how to set up work order projects, and to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) regarding how to create work order lifecycle states.</span></span>

<span data-ttu-id="3dcee-152">Figuren nedenfor viser en grafisk oversikt over ulike prosjektene som er opprettet i **Aktivastyring**-modulen, for å tillate integrering med modulen **Prosjektstyring og regnskap**, i tillegg til arbeidsprosessene som prosjektene er relatert til.</span><span class="sxs-lookup"><span data-stu-id="3dcee-152">The figure below shows a graphic overview of the various projects that are created in the **Asset management** module to allow integration with the **Project management and accounting** module, as well as the work processes to which the projects are related.</span></span>

![Figur 6](media/06-integration-to-pma.png)

