---
title: Oversikt over servicenivåavtaler
description: I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b06e537b010b6b32799f76964cb85af892bc3f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216143"
---
# <a name="service-level-agreements-overview"></a><span data-ttu-id="c0b68-103">Oversikt over servicenivåavtaler</span><span class="sxs-lookup"><span data-stu-id="c0b68-103">Service level agreements overview</span></span>       

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c0b68-104">En servicenivåavtale er en avtale mellom et servicefirma og en servicekunde.</span><span class="sxs-lookup"><span data-stu-id="c0b68-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="c0b68-105">I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.</span><span class="sxs-lookup"><span data-stu-id="c0b68-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="c0b68-106">En servicenivåavtale sørger for et standard servicenivå som tilbys kundene, og gjør det åpenbart for servicefirmaet når en servicejobb bør være ferdig.</span><span class="sxs-lookup"><span data-stu-id="c0b68-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="c0b68-107">Du kan opprette en rekke serviceavtalenivåer for å tilby ulike servicenivå til servicekunder.</span><span class="sxs-lookup"><span data-stu-id="c0b68-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="c0b68-108">Opprett en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="c0b68-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="c0b68-109">Klikk **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Servicenivåavtaler**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="c0b68-110">Skriv inn navnet på servicenivåavtalen i feltet **Servicenivåavtale**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="c0b68-111">Skriv inn klokkeslettet du ønsker å kunne fullføre servicebesøk som er knyttet til servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="c0b68-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="c0b68-112">Velg deretter en kalender hvis du vil basere servicenivåavtalen på en bestemt kalender.</span><span class="sxs-lookup"><span data-stu-id="c0b68-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="c0b68-113">Bruk en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="c0b68-113">Apply a service level agreement</span></span>

<span data-ttu-id="c0b68-114">Servicenivåavtalen brukes direkte på en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="c0b68-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="c0b68-115">Serviceordrer som du oppretter manuelt og knytter til en serivceavtale som har en servicenivåavtale, måles mot denne servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="c0b68-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="c0b68-116">Serviceordrer som du oppretter automatisk, er ikke knyttet til en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="c0b68-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="c0b68-117">Bruk servicenivåavtalen for serviceavtalen</span><span class="sxs-lookup"><span data-stu-id="c0b68-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="c0b68-118">Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="c0b68-119">Velg serviceavtalen du vil bruke servicenivåavtalen for, og klikk deretter **Rediger** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="c0b68-120">I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="c0b68-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="c0b68-121">Bruk servicenivåavtalen for serviceavtalegruppen</span><span class="sxs-lookup"><span data-stu-id="c0b68-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="c0b68-122">Klikk **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Serviceavtalegrupper**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="c0b68-123">I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="c0b68-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="c0b68-124">Spor tid på en serviceordre mot en servicenivåavtale</span><span class="sxs-lookup"><span data-stu-id="c0b68-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="c0b68-125">Når du oppretter en ny serviceordre for en serviceavtale som en servicenivåavtale er tilordnet til, startes tidsintervallet for levering av tjenesten, og systemet starter å spore leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="c0b68-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="c0b68-126">I tillegg har du følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="c0b68-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="c0b68-127">Du kan starte og stanse tidsregistrering for serviceordren for å registrere den totale tiden som er brukt på serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="c0b68-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="c0b68-128">Du kan overvåke overholdelse av tidsintervallet som er angitt i servicenicåavtalen.</span><span class="sxs-lookup"><span data-stu-id="c0b68-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="c0b68-129">Du kan definere årsakskoder som må angis hvis tidsintervallet til servicenivåavtalen overskrides.</span><span class="sxs-lookup"><span data-stu-id="c0b68-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0b68-130">Se også</span><span class="sxs-lookup"><span data-stu-id="c0b68-130">See also</span></span>

[<span data-ttu-id="c0b68-131">Vise samsvar med servicenivåavtaler</span><span class="sxs-lookup"><span data-stu-id="c0b68-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


