---
title: Oversikt over servicestyring
description: Bruk Servicestyring til å opprette serviceavtaler og serviceabonnementer, håndtere serviceordrer og kundeforespørsler og til å behandle og analysere levering av tjenester til kunder.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 20751acfc012e2ac1eef99c778c5b0353baf1827
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865855"
---
# <a name="service-management-overview"></a><span data-ttu-id="0bda7-103">Oversikt over servicestyring</span><span class="sxs-lookup"><span data-stu-id="0bda7-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0bda7-104">Bruk **Servicestyring** til å opprette serviceavtaler og serviceabonnementer, håndtere serviceordrer og kundeforespørsler og til å behandle og analysere levering av tjenester til kunder.</span><span class="sxs-lookup"><span data-stu-id="0bda7-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="0bda7-105">Du kan bruke serviceavtaler til å definere ressursene som brukes i et vanlig servicebesøk.</span><span class="sxs-lookup"><span data-stu-id="0bda7-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="0bda7-106">Du kan også bruke serviceavtaler til å vise hvordan disse ressursene skal faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="0bda7-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="0bda7-107">En serviceavtale kan også inkludere en servicenivåavtale som angir standard svartider, og inneholder verktøy for å registrere faktisk tid.</span><span class="sxs-lookup"><span data-stu-id="0bda7-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="0bda7-108">Du kan opprette serviceordrer for å administrere informasjon om planlagte og ikke-planlagte besøk av en servicetekniker hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="0bda7-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="0bda7-109">Serviceordrer inneholder informasjon som:</span><span class="sxs-lookup"><span data-stu-id="0bda7-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="0bda7-110">Antall arbeidstimer som serviceteknikeren skal utføre</span><span class="sxs-lookup"><span data-stu-id="0bda7-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="0bda7-111">Typen service eller reparasjon</span><span class="sxs-lookup"><span data-stu-id="0bda7-111">The type of service or repair</span></span>

3.  <span data-ttu-id="0bda7-112">Varen du vil reparere, inkludert informasjon om symptomer og diagnose</span><span class="sxs-lookup"><span data-stu-id="0bda7-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="0bda7-113">Utgifter og gebyrer knyttet til service eller reparasjon</span><span class="sxs-lookup"><span data-stu-id="0bda7-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="0bda7-114">Du kan motta, behandle og fordele tjenesteforespørsler.</span><span class="sxs-lookup"><span data-stu-id="0bda7-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="0bda7-115">Når du har opprettet en serviceordre, kan du bruke servicestadier til å overvåke fremdriften og angi regler som styrer hvilke handlinger som skal aktiveres på hvert stadium.</span><span class="sxs-lookup"><span data-stu-id="0bda7-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="0bda7-116">Når en serviceordre fullføres, kan du godkjenne ordren for å bekrefte at den er fullført, og deretter kan du bokføre ordren for å starte faktureringen.</span><span class="sxs-lookup"><span data-stu-id="0bda7-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="0bda7-117">Bruk rapporteringsverktøyene for å overvåke serviceordremarginer og abonnementstransaksjoner, og skriv ut arbeidsbeskrivelser og arbeidsmottak.</span><span class="sxs-lookup"><span data-stu-id="0bda7-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="0bda7-118">Forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="0bda7-118">Business processes</span></span>

<span data-ttu-id="0bda7-119">Diagrammet nedenfor illustrerer høynivå-forretningsprosessene for **Servicestyring**, og viser hvor serviceprosesser integreres med andre moduler i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0bda7-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="0bda7-120">[![Diagram over forretningsprosess for servicestyring](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="0bda7-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="0bda7-121">Et raskt blikk på servicestyring</span><span class="sxs-lookup"><span data-stu-id="0bda7-121">Service management at a glance</span></span>

|<span data-ttu-id="0bda7-122">Viktige oppgaver</span><span class="sxs-lookup"><span data-stu-id="0bda7-122">Important tasks</span></span>           | <span data-ttu-id="0bda7-123">Hovedsidene</span><span class="sxs-lookup"><span data-stu-id="0bda7-123">Primary pages</span></span>                         |<span data-ttu-id="0bda7-124">Populære rapporter</span><span class="sxs-lookup"><span data-stu-id="0bda7-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="0bda7-125">Oppfylle serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="0bda7-125">Fulfill service agreements</span></span>|<span data-ttu-id="0bda7-126">Serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="0bda7-126">Service agreements</span></span>                     |<span data-ttu-id="0bda7-127">Serviceordremargin</span><span class="sxs-lookup"><span data-stu-id="0bda7-127">Service order margin</span></span>         |
|<span data-ttu-id="0bda7-128">Behandle kundeforespørsler</span><span class="sxs-lookup"><span data-stu-id="0bda7-128">Handle customer inquiries</span></span> |<span data-ttu-id="0bda7-129">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="0bda7-129">Service orders</span></span>                         |<span data-ttu-id="0bda7-130">Arbeidsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="0bda7-130">Work description</span></span>             |
|                          |<span data-ttu-id="0bda7-131">Tjenestefordeling</span><span class="sxs-lookup"><span data-stu-id="0bda7-131">Dispatch board</span></span>                         |<span data-ttu-id="0bda7-132">Transaksjon - abonnement</span><span class="sxs-lookup"><span data-stu-id="0bda7-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="0bda7-133">Abonnementsavgiftstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0bda7-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="0bda7-134">Integrering av servicestyring</span><span class="sxs-lookup"><span data-stu-id="0bda7-134">Integration of Service management</span></span>

<span data-ttu-id="0bda7-135">Servicestyring kan integreres med følgende moduler:</span><span class="sxs-lookup"><span data-stu-id="0bda7-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="0bda7-136">Salg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="0bda7-136">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="0bda7-137">Personale</span><span class="sxs-lookup"><span data-stu-id="0bda7-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

