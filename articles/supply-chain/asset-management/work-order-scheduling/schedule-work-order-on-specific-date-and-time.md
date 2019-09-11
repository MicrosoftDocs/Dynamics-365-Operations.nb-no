---
title: Planlegge arbeidsordre på bestemt dato og klokkeslett
description: Dette emnet forklarer hvordan du planlegger en arbeidsordre på en bestemt dato og klokkeslett i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 0f818c4c3b669cc94e37cba1e3571c57b5c0dd1b
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887371"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="0eb43-103">Planlegge arbeidsordre på bestemt dato og klokkeslett</span><span class="sxs-lookup"><span data-stu-id="0eb43-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0eb43-104">Hvis en arbeidsordre må planlegges på en bestemt dato *og* klokkeslett, kan du overstyre standard planleggingsprosess i Aktivastyring og opprette en bestemt tidsplan for en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="0eb43-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="0eb43-105">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="0eb43-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0eb43-106">I arbeidsordrelisten klikker du på ID-en for arbeidsordren i kolonnen **Arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="0eb43-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="0eb43-107">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0eb43-107">Click **Edit**.</span></span>

4. <span data-ttu-id="0eb43-108">Sett inn start- og sluttdato og klokkeslett i feltene **Forventet start** og **Forventet slutt** i hurtigfanen **Arbeidsordrehode**.</span><span class="sxs-lookup"><span data-stu-id="0eb43-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

![Figur 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="0eb43-110">I kategorien **Generelt** klikker du på **Planlegg** for å bruke standard planleggingsprosess, eller klikker på **Fordeling** hvis du vil tilordne arbeidsordren til en bestemt arbeider.</span><span class="sxs-lookup"><span data-stu-id="0eb43-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to schedule the work order to a specific worker.</span></span>

6. <span data-ttu-id="0eb43-111">Hvis du vil overstyre eventuelle eksisterende kapasitetsreservasjoner for å sikre at arbeidsordren planlegges i den forventede perioden, gjør du valgene som vist i figuren nedenfor i dialogboksen **Planlegg arbeidsordre** > **Begrenset kapasitet**-delen.</span><span class="sxs-lookup"><span data-stu-id="0eb43-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="0eb43-112">Dette betyr at planleggingsprosessen vil ignorere eksisterende kapasitetsreservasjoner fordi arbeidsordren må starte på forventet starttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="0eb43-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

![Figur 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="0eb43-114">Klikk på **OK** for å starte planleggingen.</span><span class="sxs-lookup"><span data-stu-id="0eb43-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="0eb43-115">Hvis planleggingsprosessen resulterer i dobbeltreservering, vil du se en melding på skjermen, og du kan justere de tilknyttede arbeidsordrene.</span><span class="sxs-lookup"><span data-stu-id="0eb43-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="0eb43-116">Hvis du vil planlegge en vedlikeholdsperson for arbeidsordren, må vedlikeholdspersonen være tilgjengelig på forventet startdato og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="0eb43-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="0eb43-117">Arbeidertilgjengelighet defineres i [arbeiderkalenderen](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="0eb43-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

