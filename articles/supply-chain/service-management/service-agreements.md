---
title: Oversikt over å utvikle og etablere serviceavtaler
description: Serviceavtaler lar deg definere ressursene som brukes ved et vanlig servicebesøk, og hvordan disse ressursene skal faktureres til kunden.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86855e8893cdf5d6e53cb34465480ade06a6da95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258500"
---
# <a name="develop-and-establish-service-agreements-overview"></a><span data-ttu-id="208f9-103">Oversikt over å utvikle og etablere serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="208f9-103">Develop and establish service agreements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="208f9-104">Serviceavtaler lar deg definere ressursene som brukes ved et vanlig servicebesøk, og hvordan disse ressursene skal faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="208f9-104">Service agreements let you define the resources that are used in a typical service visit and how those resources are invoiced to the customer.</span></span>

<span data-ttu-id="208f9-105">Hver serviceavtale knyttes til et prosjekt, som transaksjoner posteres og faktureres gjennom.</span><span class="sxs-lookup"><span data-stu-id="208f9-105">Every service agreement is attached to a project through which transactions are posted and invoiced.</span></span> <span data-ttu-id="208f9-106">Du kan imidlertid også fakturere serviceordretransaksjoner direkte gjennom prosjektet uten først å måtte knytte serviceordren til en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="208f9-106">However, you can also invoice service order transactions directly through the project without first having to connect the service order to a service agreement.</span></span> <span data-ttu-id="208f9-107">Dette kan være en praktisk løsning hvis serviceordren gjelder et enkelt besøk og behovet for en rask behandling av transaksjonen veier tyngre enn behovet for å opprettholde detaljerte serviceavtaleopplysninger for kunden over en lengre periode.</span><span class="sxs-lookup"><span data-stu-id="208f9-107">You might decide to do this if the service order is for a one-time-only service visit and the need for processing the service transactions quickly outweighs the need for maintaining detailed service-agreement information about the customer over a period of time.</span></span>

## <a name="service-agreement"></a><span data-ttu-id="208f9-108">Serviceavtale</span><span class="sxs-lookup"><span data-stu-id="208f9-108">Service agreement</span></span>

<span data-ttu-id="208f9-109">I hver serviceavtale må du angi et prosjekt, en serviceavtale-ID og en serviceavtalegruppe.</span><span class="sxs-lookup"><span data-stu-id="208f9-109">In each service agreement, you must specify a project, a service-agreement ID, and a service-agreement group.</span></span> <span data-ttu-id="208f9-110">Serviceavtalegruppen kan brukes til å sortere og organisere serviceavtaler.</span><span class="sxs-lookup"><span data-stu-id="208f9-110">The service-agreement group can be used to sort and organize service agreements.</span></span>

<span data-ttu-id="208f9-111">Et serviceavtalehode inneholder innstillinger som gjelder alle tilknyttede avtalelinjer:</span><span class="sxs-lookup"><span data-stu-id="208f9-111">A service agreement header contains settings that apply to all attached agreement lines:</span></span>

-  <span data-ttu-id="208f9-112">Om serviceavtalen er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="208f9-112">Whether the service agreement is suspended.</span></span> <span data-ttu-id="208f9-113">Hvis en serviceavtale deaktiveres, vil du ikke kunne generere serviceordrer fra serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-113">If the service agreement is suspended, you cannot generate service orders from the service agreement.</span></span>
-  <span data-ttu-id="208f9-114">Varigheten på serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-114">The duration of the service agreement.</span></span>
-  <span data-ttu-id="208f9-115">Hvordan serviceordrelinjer kombineres med serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="208f9-115">How service-order lines are to be combined into service orders.</span></span>
-  <span data-ttu-id="208f9-116">Om serviceavtalen er en mal.</span><span class="sxs-lookup"><span data-stu-id="208f9-116">Whether the service agreement is a template.</span></span>

<span data-ttu-id="208f9-117">I serviceavtalehodet definerer du også alle serviceobjektene og serviceoppgavene som kan brukes med serviceavtalen ved å angi de bestemte serviceoppgavene eller serviceobjektene som skal knyttes til de ulike linjene i avtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-117">In the service-agreement header, you also set up all the service objects and service tasks that can be used with the service agreement by entering the specific service tasks or service objects that are to be attached to the various lines of the agreement.</span></span>

<span data-ttu-id="208f9-118">Fra serviceavtalehodet kan du kopiere serviceavtalelinjer og servicemallinjer til den gjeldende serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-118">From the service-agreement header, you can also copy service-agreement lines or service-template lines into the current service agreement.</span></span>

<span data-ttu-id="208f9-119">Du kan suspendere serviceavtaler og stoppe enkle serviceavtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="208f9-119">You can suspend service agreements and stop individual service agreement lines.</span></span>

<span data-ttu-id="208f9-120">Hvis du merker av for **Avbrutt** på en serviceavtale, kan du ikke gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="208f9-120">If you select the **Suspended** check box on a service agreement, you cannot:</span></span>

-    <span data-ttu-id="208f9-121">Opprett serviceordrer automatisk eller manuelt fra serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-121">Create service orders automatically or manually from the service agreement.</span></span>

<span data-ttu-id="208f9-122">Hvis du merker av for **Stoppet** på en serviceavtalelinje, kan du ikke gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="208f9-122">If you select the **Stopped** check box on a service agreement line, you cannot:</span></span>

-    <span data-ttu-id="208f9-123">Opprett serviceordrer automatisk eller manuelt fra serviceavtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="208f9-123">Create service orders automatically or manually from the service agreement line.</span></span>
-    <span data-ttu-id="208f9-124">Kopier serviceavtalelinjen til en annen serviceavtale eller serviceordre.</span><span class="sxs-lookup"><span data-stu-id="208f9-124">Copy the service agreement line into another service agreement or service order.</span></span>


> [!NOTE]
> <span data-ttu-id="208f9-125">Hvis en serviceavtale suspenderes, stoppes alle de tilknyttede linjene uansett enkeltstatus.</span><span class="sxs-lookup"><span data-stu-id="208f9-125">If a service agreement is suspended, all the attached lines are stopped, regardless of their individual status.</span></span>

## <a name="service-agreement-lines"></a><span data-ttu-id="208f9-126">Serviceavtalelinjer</span><span class="sxs-lookup"><span data-stu-id="208f9-126">Service-agreement lines</span></span>

<span data-ttu-id="208f9-127">Hver serviceavtalelinje beskriver innholdet i det foreslåtte vedlikeholdsarbeidet i detalj.</span><span class="sxs-lookup"><span data-stu-id="208f9-127">Each service-agreement line describes in detail the content of the proposed service work.</span></span> <span data-ttu-id="208f9-128">Linjene inneholder følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="208f9-128">The lines contain the following settings:</span></span>

-  <span data-ttu-id="208f9-129">Transaksjonstypen og en beskrivelse av transaksjonstypen.</span><span class="sxs-lookup"><span data-stu-id="208f9-129">The transaction type and the description of the transaction type.</span></span>
-  <span data-ttu-id="208f9-130">Den ansatte som utfører vedlikeholdsarbeidet.</span><span class="sxs-lookup"><span data-stu-id="208f9-130">The employee who performs the service work.</span></span>
-  <span data-ttu-id="208f9-131">Objektene vedlikeholdet skal utføres på i henhold til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="208f9-131">The objects on which service must be performed for the service agreement.</span></span>
-  <span data-ttu-id="208f9-132">Hvor ofte det forskjellige arbeidet skal utføres og tilknyttede vare-, utgifts- og gebyrtransaksjoner skal registreres.</span><span class="sxs-lookup"><span data-stu-id="208f9-132">The frequency with which work is performed and associated item, expense, and fee transactions are registered.</span></span>
-  <span data-ttu-id="208f9-133">Tidsvinduet når serviceordrelinjene kan grupperes til en serviceordre.</span><span class="sxs-lookup"><span data-stu-id="208f9-133">The time window within which service-order lines can be grouped into a service order.</span></span>
-  <span data-ttu-id="208f9-134">Serviceoppgavene som brukes til å gruppere sett med avtalelinjer til arbeidsoppgaver og til å summere hvilke serviceoppgaver som vil bli utført, for teknikere og kunder.</span><span class="sxs-lookup"><span data-stu-id="208f9-134">The service tasks that are used to group sets of agreement lines together into work tasks and to summarize for service technicians and customers what service task is to be provided.</span></span>
-  <span data-ttu-id="208f9-135">Om en linje er stoppet.</span><span class="sxs-lookup"><span data-stu-id="208f9-135">Whether a line is stopped.</span></span> <span data-ttu-id="208f9-136">Hvis en linje stoppes, kan du ikke opprette serviceordrer for den bestemte linjen.</span><span class="sxs-lookup"><span data-stu-id="208f9-136">If a line is stopped, you cannot create service orders for that individual line.</span></span>
-  <span data-ttu-id="208f9-137">Prosjektinnstillinger som kategori og linjeegenskap.</span><span class="sxs-lookup"><span data-stu-id="208f9-137">Project settings, such as the category and the line property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="208f9-138">Relaterte emner</span><span class="sxs-lookup"><span data-stu-id="208f9-138">Related topics</span></span>

[<span data-ttu-id="208f9-139">Opprette serviceavtaler</span><span class="sxs-lookup"><span data-stu-id="208f9-139">Create service agreements</span></span>](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]