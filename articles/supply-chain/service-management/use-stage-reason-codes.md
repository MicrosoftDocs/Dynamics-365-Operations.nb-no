---
title: Bruke stadieårsakskoder
description: Du kan bruke en årsakskode til å angi hvorfor en servicenivåavtale (SLA) har blitt annullert, eller hvorfor en serviceordre har overskredet tidsbegrensningen som er definert i servicenivåavtalen.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54dae6edb6681e1ba29709ebeeea2e5094262257
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206479"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="ece07-103">Bruke stadieårsakskoder</span><span class="sxs-lookup"><span data-stu-id="ece07-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ece07-104">Du kan bruke en årsakskode til å angi hvorfor en servicenivåavtale (SLA) har blitt annullert, eller hvorfor en serviceordre har overskredet tidsbegrensningen som er definert i servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="ece07-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="ece07-105">Eu kan også angi at en årsakskode kreves når en når en servicenivåavtale annulleres eller når tidsbegrensningen overskrider tiden som er angitt i serviceavtalen vor serviceordren.</span><span class="sxs-lookup"><span data-stu-id="ece07-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="ece07-106">Hvis tidsbegrensningen er overskredet på en serviceavtale, må du angi en årsakskode i følgende situasjoner:</span><span class="sxs-lookup"><span data-stu-id="ece07-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="ece07-107">Når en serviceordre flyttes til et stadium som stopper tidsregistreringen mot servicenivåavtalen for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="ece07-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="ece07-108">Når serviceordren godkjennes.</span><span class="sxs-lookup"><span data-stu-id="ece07-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="ece07-109">Når tidsregistrering stoppes manuelt.</span><span class="sxs-lookup"><span data-stu-id="ece07-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="ece07-110">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="ece07-110">Set up reason codes</span></span>

1.  <span data-ttu-id="ece07-111">Klikk **Servicestyring** \> **Oppsett** \> **Serviceordrer** \> **Stadieårsakskoder**.</span><span class="sxs-lookup"><span data-stu-id="ece07-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="ece07-112">I skjemaet **Stadieårsakskoder** klikker du **Ny** for å opprette en ny årsakskode.</span><span class="sxs-lookup"><span data-stu-id="ece07-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="ece07-113">I feltet **Stadieårsakskode** angir du en unik årsakskode for stadium.</span><span class="sxs-lookup"><span data-stu-id="ece07-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="ece07-114">I **Beskrivelse**-feltet angir du en beskrivelse av stadieårsakskoden.</span><span class="sxs-lookup"><span data-stu-id="ece07-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="ece07-115">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="ece07-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="ece07-116">Kreve årsakskoder når en servicenivåavtale annulleres</span><span class="sxs-lookup"><span data-stu-id="ece07-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="ece07-117">Klikk **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="ece07-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="ece07-118">I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for avbrudd**.</span><span class="sxs-lookup"><span data-stu-id="ece07-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="ece07-119">Kreve årsakskoder når en serviceordre overskrider tidsbegrensningen som er definert i servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="ece07-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="ece07-120">Klikk **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="ece07-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="ece07-121">I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for tidsoverskridelse**.</span><span class="sxs-lookup"><span data-stu-id="ece07-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="ece07-122">Se også</span><span class="sxs-lookup"><span data-stu-id="ece07-122">See also</span></span>

[<span data-ttu-id="ece07-123">Starte og stoppe tidsregistrering på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="ece07-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  


