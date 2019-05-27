---
title: Servicenivåavtaler
description: I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cffe3a7766502dd5d888a7a99a32150967911301
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562632"
---
# <a name="service-level-agreements"></a><span data-ttu-id="0b6e0-103">Servicenivåavtaler</span><span class="sxs-lookup"><span data-stu-id="0b6e0-103">Service level agreements</span></span>        

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0b6e0-104">En servicenivåavtale er en avtale mellom et servicefirma og en servicekunde.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-104">A service level agreement (SLA) is an agreement between a service company and a service customer.</span></span> <span data-ttu-id="0b6e0-105">I en servicenivåavtale godtar kunden en minimum svartid basert på når servicefirmaet registrerer saken, og når saken er løst.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-105">In a SLA, the customer agrees to a minimum response time based on when the service company records the issue and when the issue is resolved.</span></span>

<span data-ttu-id="0b6e0-106">En servicenivåavtale sørger for et standard servicenivå som tilbys kundene, og gjør det åpenbart for servicefirmaet når en servicejobb bør være ferdig.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-106">A SLA enforces a standard level of service that is offered to customers, and also makes it transparent to a service company when a service job should be completed.</span></span>

<span data-ttu-id="0b6e0-107">Du kan opprette en rekke serviceavtalenivåer for å tilby ulike servicenivå til servicekunder.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-107">Any number of SLAs can be created to offer service customers different levels of service.</span></span>

## <a name="create-a-service-level-agreement"></a><span data-ttu-id="0b6e0-108">Opprett en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-108">Create a service level agreement</span></span>

1.  <span data-ttu-id="0b6e0-109">Klikk **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Servicenivåavtaler**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-109">Click **Service management** \> **Setup** \> **Service agreements** \> **Service level agreements**.</span></span>

2.  <span data-ttu-id="0b6e0-110">Skriv inn navnet på servicenivåavtalen i feltet **Servicenivåavtale**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-110">Type a name for the service level agreement in the **Service level agreement** field.</span></span>

3.  <span data-ttu-id="0b6e0-111">Skriv inn klokkeslettet du ønsker å kunne fullføre servicebesøk som er knyttet til servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-111">Type the time that you want to allow for completion of service calls that are attached to the service level agreement.</span></span> <span data-ttu-id="0b6e0-112">Velg deretter en kalender hvis du vil basere servicenivåavtalen på en bestemt kalender.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-112">Then select a calendar if you want to base the service level agreement on a specific calendar.</span></span>

## <a name="apply-a-service-level-agreement"></a><span data-ttu-id="0b6e0-113">Bruk en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-113">Apply a service level agreement</span></span>

<span data-ttu-id="0b6e0-114">Servicenivåavtalen brukes direkte på en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-114">The SLA is applied directly to a service agreement.</span></span>

<span data-ttu-id="0b6e0-115">Serviceordrer som du oppretter manuelt og knytter til en serivceavtale som har en servicenivåavtale, måles mot denne servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-115">Service orders that you create manually and attach to a service agreement that has an SLA are measured against that SLA.</span></span>

<span data-ttu-id="0b6e0-116">Serviceordrer som du oppretter automatisk, er ikke knyttet til en servicenivåavtale.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-116">Service orders that you create automatically are not attached to an SLA.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a><span data-ttu-id="0b6e0-117">Bruk servicenivåavtalen for serviceavtalen</span><span class="sxs-lookup"><span data-stu-id="0b6e0-117">Apply the service level agreement to the service agreement</span></span>

1.  <span data-ttu-id="0b6e0-118">Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="0b6e0-119">Velg serviceavtalen du vil bruke servicenivåavtalen for, og klikk deretter **Rediger** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-119">Select the service agreement that you want to apply the SLA to, and then click **Edit** on the **Action Pane**.</span></span>

2.  <span data-ttu-id="0b6e0-120">I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-120">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a><span data-ttu-id="0b6e0-121">Bruk servicenivåavtalen for serviceavtalegruppen</span><span class="sxs-lookup"><span data-stu-id="0b6e0-121">Apply the service level agreement to the service agreement group</span></span>

1.  <span data-ttu-id="0b6e0-122">Klikk **Servicestyring** \> **Oppsett** \> **Serviceavtaler** \> **Serviceavtalegrupper**.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-122">Click **Service management** \> **Setup** \> **Service agreements** \> **Service agreement groups**.</span></span>

2.  <span data-ttu-id="0b6e0-123">I feltet **Servicenivåavtale** velger servicenivåavtalen du vil tilordne.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-123">In the **Service level agreement** field, select the SLA that you want to assign.</span></span>

## <a name="track-time-on-a-service-order-against-an-sla"></a><span data-ttu-id="0b6e0-124">Spor tid på en serviceordre mot en servicenivåavtale</span><span class="sxs-lookup"><span data-stu-id="0b6e0-124">Track time on a service order against an SLA</span></span>

<span data-ttu-id="0b6e0-125">Når du oppretter en ny serviceordre for en serviceavtale som en servicenivåavtale er tilordnet til, startes tidsintervallet for levering av tjenesten, og systemet starter å spore leveringstiden.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-125">When you create a new service order for a service agreement that an SLA is assigned to, the time interval for the delivery of the service is initiated, and the system starts to track the delivery time.</span></span> <span data-ttu-id="0b6e0-126">I tillegg har du følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="0b6e0-126">Additionally, you can set the following options:</span></span>

  - <span data-ttu-id="0b6e0-127">Du kan starte og stanse tidsregistrering for serviceordren for å registrere den totale tiden som er brukt på serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-127">You can start and stop time recording on the service order to register the total amount of time that is spent on service orders.</span></span>

  - <span data-ttu-id="0b6e0-128">Du kan overvåke overholdelse av tidsintervallet som er angitt i servicenicåavtalen.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-128">You can monitor compliance with the time interval that is set in the service level agreement.</span></span>

  - <span data-ttu-id="0b6e0-129">Du kan definere årsakskoder som må angis hvis tidsintervallet til servicenivåavtalen overskrides.</span><span class="sxs-lookup"><span data-stu-id="0b6e0-129">You can define reason codes that must be set if the time interval of the service level agreement is exceeded.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b6e0-130">Se også</span><span class="sxs-lookup"><span data-stu-id="0b6e0-130">See also</span></span>

[<span data-ttu-id="0b6e0-131">Vise samsvar med servicenivåavtaler</span><span class="sxs-lookup"><span data-stu-id="0b6e0-131">View compliance with service level agreements</span></span>](view-compliance-with-service-level-agreements.md)

  


