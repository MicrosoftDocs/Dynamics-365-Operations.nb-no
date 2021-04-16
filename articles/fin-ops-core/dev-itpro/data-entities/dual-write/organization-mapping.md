---
title: Organisasjonshierarki i Dataverse
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8b147c27b9309b1b3597f1194c415fbb2e2b7ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750818"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="dc75b-103">Organisasjonshierarki i Dataverse</span><span class="sxs-lookup"><span data-stu-id="dc75b-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dc75b-104">Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="dc75b-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="dc75b-105">Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="dc75b-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="dc75b-106">Selv om Dataverse ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="dc75b-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="dc75b-107">Som en del av Dataverse-integreringen legges datastrukturen for organisasjonshierarkiet til i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dc75b-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="dc75b-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="dc75b-108">Data flow</span></span>

<span data-ttu-id="dc75b-109">Et forretningsøkosystem som består av Finance and Operations-apper og Dataverse, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="dc75b-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="dc75b-110">Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Dataverse for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="dc75b-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="dc75b-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Dataverse, som en énveis dataflyt fra Finance and Operations-apper til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dc75b-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

<span data-ttu-id="dc75b-113">Tabeltilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Dataverse.</span><span class="sxs-lookup"><span data-stu-id="dc75b-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="dc75b-114">Maler</span><span class="sxs-lookup"><span data-stu-id="dc75b-114">Templates</span></span>

<span data-ttu-id="dc75b-115">Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="dc75b-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="dc75b-116">Som følgende tabell viser opprettes en samling tabelltilordning for å synkronisere produkter og beslektet informasjon.</span><span class="sxs-lookup"><span data-stu-id="dc75b-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="dc75b-117">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="dc75b-117">Finance and Operations apps</span></span> | <span data-ttu-id="dc75b-118">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="dc75b-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="dc75b-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="dc75b-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="dc75b-120">Formål for organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="dc75b-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="dc75b-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="dc75b-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="dc75b-122">Denne malen gir enveis synkronisering av formålstabellen for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="dc75b-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="dc75b-123">Type organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="dc75b-123">Organization hierarchy type</span></span> | <span data-ttu-id="dc75b-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="dc75b-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="dc75b-125">Denne malen gir enveis synkronisering av typetabellen for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="dc75b-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="dc75b-126">Organisasjonshierarki – publisert</span><span class="sxs-lookup"><span data-stu-id="dc75b-126">Organization hierarchy - published</span></span> | <span data-ttu-id="dc75b-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="dc75b-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="dc75b-128">Denne malen gir enveis synkronisering av den publiserte tabellen for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="dc75b-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="dc75b-129">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="dc75b-129">Operating unit</span></span> | <span data-ttu-id="dc75b-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="dc75b-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="dc75b-131">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="dc75b-131">Legal entities</span></span> | <span data-ttu-id="dc75b-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="dc75b-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="dc75b-133">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="dc75b-133">Legal entities</span></span> | <span data-ttu-id="dc75b-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="dc75b-134">cdm_companies</span></span> | <span data-ttu-id="dc75b-135">Gir toveis synkronisering av informasjon om juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="dc75b-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="dc75b-136">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="dc75b-136">Internal Organization</span></span>

<span data-ttu-id="dc75b-137">Informasjon om intern organisasjon i Dataverse kommer fra to tabeller, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="dc75b-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]