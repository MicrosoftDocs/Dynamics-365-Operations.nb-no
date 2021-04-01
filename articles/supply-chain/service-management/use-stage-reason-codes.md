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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 220012011e6fb1818cffa3992a3c39f46e5c071a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259632"
---
# <a name="use-stage-reason-codes"></a><span data-ttu-id="b384a-103">Bruke stadieårsakskoder</span><span class="sxs-lookup"><span data-stu-id="b384a-103">Use stage reason codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b384a-104">Du kan bruke en årsakskode til å angi hvorfor en servicenivåavtale (SLA) har blitt annullert, eller hvorfor en serviceordre har overskredet tidsbegrensningen som er definert i servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="b384a-104">You use a reason code to indicate why a service level agreement (SLA) has been canceled, or why a service order has exceeded the time limit that is you define in the SLA.</span></span>

<span data-ttu-id="b384a-105">Eu kan også angi at en årsakskode kreves når en når en servicenivåavtale annulleres eller når tidsbegrensningen overskrider tiden som er angitt i serviceavtalen vor serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b384a-105">You can also specify that a reason code is required when an SLA is canceled, or when the time limit exceeds the time that is specified in the SLA for the service order.</span></span>

<span data-ttu-id="b384a-106">Hvis tidsbegrensningen er overskredet på en serviceavtale, må du angi en årsakskode i følgende situasjoner:</span><span class="sxs-lookup"><span data-stu-id="b384a-106">If you have specified that a reason code is required, you must enter a reason code in the following situations:</span></span>

  - <span data-ttu-id="b384a-107">Når en serviceordre flyttes til et stadium som stopper tidsregistreringen mot servicenivåavtalen for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="b384a-107">When a service order is moved to a stage that stops time recording against the SLA for the service order.</span></span>

  - <span data-ttu-id="b384a-108">Når serviceordren godkjennes.</span><span class="sxs-lookup"><span data-stu-id="b384a-108">When the service order is signed off.</span></span>

  - <span data-ttu-id="b384a-109">Når tidsregistrering stoppes manuelt.</span><span class="sxs-lookup"><span data-stu-id="b384a-109">When time recording is manually stopped.</span></span>

## <a name="set-up-reason-codes"></a><span data-ttu-id="b384a-110">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="b384a-110">Set up reason codes</span></span>

1.  <span data-ttu-id="b384a-111">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceordrer** \> **Stadieårsakskoder**.</span><span class="sxs-lookup"><span data-stu-id="b384a-111">Click **Service management** \> **Setup** \> **Service orders** \> **Stage reason codes**.</span></span>

2.  <span data-ttu-id="b384a-112">I skjemaet **Stadieårsakskoder** klikker du **Ny** for å opprette en ny årsakskode.</span><span class="sxs-lookup"><span data-stu-id="b384a-112">In the **Stage reason codes** form, click **New** to create a new reason code.</span></span>

3.  <span data-ttu-id="b384a-113">I feltet **Stadieårsakskode** angir du en unik årsakskode for stadium.</span><span class="sxs-lookup"><span data-stu-id="b384a-113">In the **Stage reason code** field, enter a unique stage reason code.</span></span>

4.  <span data-ttu-id="b384a-114">I **Beskrivelse**-feltet angir du en beskrivelse av stadieårsakskoden.</span><span class="sxs-lookup"><span data-stu-id="b384a-114">In the **Description** field, enter a description of the stage reason code.</span></span>

5.  <span data-ttu-id="b384a-115">Lukk skjemaet for å lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="b384a-115">Close the form to save your changes.</span></span>

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a><span data-ttu-id="b384a-116">Kreve årsakskoder når en servicenivåavtale annulleres</span><span class="sxs-lookup"><span data-stu-id="b384a-116">Require reason codes when a service level agreement is canceled</span></span>

1.  <span data-ttu-id="b384a-117">Klikk på **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="b384a-117">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="b384a-118">I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for avbrudd**.</span><span class="sxs-lookup"><span data-stu-id="b384a-118">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on canceling** check box.</span></span>

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a><span data-ttu-id="b384a-119">Kreve årsakskoder når en serviceordre overskrider tidsbegrensningen som er definert i servicenivåavtalen.</span><span class="sxs-lookup"><span data-stu-id="b384a-119">Require reason codes when the a service order exceeds the time limit that is set by the service level agreement</span></span>

1.  <span data-ttu-id="b384a-120">Klikk på **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="b384a-120">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

2.  <span data-ttu-id="b384a-121">I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for tidsoverskridelse**.</span><span class="sxs-lookup"><span data-stu-id="b384a-121">In the **Service management parameters** form, click the **General** link, and then select the **Reason code on exceeding time** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="b384a-122">Se også</span><span class="sxs-lookup"><span data-stu-id="b384a-122">See also</span></span>

[<span data-ttu-id="b384a-123">Starte og stoppe tidsregistrering på en serviceordre</span><span class="sxs-lookup"><span data-stu-id="b384a-123">Start and stop time recording on a service order</span></span>](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]