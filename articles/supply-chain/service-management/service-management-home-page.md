---
title: Servicestyring
description: "Bruk Servicestyring til å opprette serviceavtaler og serviceabonnementer, håndtere serviceordrer og kundeforespørsler og til å behandle og analysere levering av tjenester til kunder."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: nb-no
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="fe9b3-103">Servicestyring</span><span class="sxs-lookup"><span data-stu-id="fe9b3-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fe9b3-104">Bruk **Servicestyring** til å opprette serviceavtaler og serviceabonnementer, håndtere serviceordrer og kundeforespørsler og til å behandle og analysere levering av tjenester til kunder.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="fe9b3-105">Du kan bruke serviceavtaler til å definere ressursene som brukes i et vanlig servicebesøk.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="fe9b3-106">Du kan også bruke serviceavtaler til å vise hvordan disse ressursene skal faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="fe9b3-107">En serviceavtale kan også inkludere en servicenivåavtale som angir standard svartider, og inneholder verktøy for å registrere faktisk tid.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="fe9b3-108">Du kan opprette serviceordrer for å administrere informasjon om planlagte og ikke-planlagte besøk av en servicetekniker hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="fe9b3-109">Serviceordrer inneholder informasjon som:</span><span class="sxs-lookup"><span data-stu-id="fe9b3-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="fe9b3-110">Antall arbeidstimer som serviceteknikeren skal utføre</span><span class="sxs-lookup"><span data-stu-id="fe9b3-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="fe9b3-111">Typen service eller reparasjon</span><span class="sxs-lookup"><span data-stu-id="fe9b3-111">The type of service or repair</span></span>

3.  <span data-ttu-id="fe9b3-112">Varen du vil reparere, inkludert informasjon om symptomer og diagnose</span><span class="sxs-lookup"><span data-stu-id="fe9b3-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="fe9b3-113">Utgifter og gebyrer knyttet til service eller reparasjon</span><span class="sxs-lookup"><span data-stu-id="fe9b3-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="fe9b3-114">Kunder kan sende serviceforespørsler via Internett ved hjelp av Enterprise Portal.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="fe9b3-115">Du kan motta, behandle og fordele disse forespørslene.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="fe9b3-116">Når du har opprettet en serviceordre, kan du bruke servicestadier til å overvåke fremdriften og angi regler som styrer hvilke handlinger som skal aktiveres på hvert stadium.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="fe9b3-117">Når en serviceordre fullføres, kan du godkjenne ordren for å bekrefte at den er fullført, og deretter kan du bokføre ordren for å starte faktureringen.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="fe9b3-118">Bruk rapporteringsverktøyene for å overvåke serviceordremarginer og abonnementstransaksjoner, og skriv ut arbeidsbeskrivelser og arbeidsmottak.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="fe9b3-119">Forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="fe9b3-119">Business processes</span></span>

<span data-ttu-id="fe9b3-120">Diagrammet nedenfor illustrerer forretningsprosessene på høyt nivå for **Servicestyring** og viser hvor serviceprosesser integrerer med andre moduler i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fe9b3-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="fe9b3-121">[![Diagram over forretningsprosess for servicestyring](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="fe9b3-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="fe9b3-122">Et raskt blikk på servicestyring</span><span class="sxs-lookup"><span data-stu-id="fe9b3-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe9b3-123">Viktige oppgaver</span><span class="sxs-lookup"><span data-stu-id="fe9b3-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="fe9b3-124">Hovedskjemaer</span><span class="sxs-lookup"><span data-stu-id="fe9b3-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="fe9b3-125">Populære rapporter</span><span class="sxs-lookup"><span data-stu-id="fe9b3-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe9b3-126">Oppfylle serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="fe9b3-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="fe9b3-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Serviceavtaler (skjema)</a></span><span class="sxs-lookup"><span data-stu-id="fe9b3-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="fe9b3-128"><strong>Serviceordremargin</strong></span><span class="sxs-lookup"><span data-stu-id="fe9b3-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe9b3-129">Behandle kundeforespørsler</span><span class="sxs-lookup"><span data-stu-id="fe9b3-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="fe9b3-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Serviceordrer (skjema)</a></span><span class="sxs-lookup"><span data-stu-id="fe9b3-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="fe9b3-131"><strong>Arbeidsbeskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="fe9b3-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="fe9b3-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Tjenestefordeling (skjema)</a></span><span class="sxs-lookup"><span data-stu-id="fe9b3-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="fe9b3-133"><strong>Transaksjon - abonnement</strong></span><span class="sxs-lookup"><span data-stu-id="fe9b3-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="fe9b3-134"><strong>Abonnementsavgiftstransaksjoner</strong></span><span class="sxs-lookup"><span data-stu-id="fe9b3-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="fe9b3-135">Integrering av servicestyring</span><span class="sxs-lookup"><span data-stu-id="fe9b3-135">Integration of Service management</span></span>

<span data-ttu-id="fe9b3-136">Servicestyring kan integreres med følgende moduler i Microsoft Dynamics 365 for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="fe9b3-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="fe9b3-137">Salg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="fe9b3-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="fe9b3-138">Personale</span><span class="sxs-lookup"><span data-stu-id="fe9b3-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


