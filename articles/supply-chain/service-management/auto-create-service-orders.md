---
title: Automatisk opprette serviceordrer
description: Du kan generere serviceordrer som er basert på serviceavtale, for den gyldige perioden for serviceavtalen.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824636"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="1914d-103">Automatisk opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="1914d-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1914d-104">Du kan generere serviceordrer som er basert på serviceavtale, for den gyldige perioden for serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="1914d-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="1914d-105">Serviceordrer du genererer fra en serviceavtale, vil alle være knyttet til den aktuelle serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="1914d-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="1914d-106">Serviceordrer genereres automatisk fra følgende innstillinger:</span><span class="sxs-lookup"><span data-stu-id="1914d-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="1914d-107">Serviceavtaleintervallet som er definert på serviceavtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="1914d-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="1914d-108">Serviceavtaleintervallet angir hvor ofte det opprettes serviceordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="1914d-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="1914d-109">Hvis du vil ha mer informasjon om serviceintervaller, se [Serviceintervaller](service-intervals.md).</span><span class="sxs-lookup"><span data-stu-id="1914d-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="1914d-110">Perioden du angir for å definere serviceperioden i feltene **Fra dato** og **Til dato** i skjemaet **Opprett serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="1914d-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="1914d-111">Hvis du vil ha mer informasjon om å kombinere serviceordrer, se [Opprette serviceordrer automatisk](create-service-orders-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="1914d-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="1914d-112">Alternativet **Kombiner serviceordrer** i serviceavtalehodet.</span><span class="sxs-lookup"><span data-stu-id="1914d-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="1914d-113">Dette alternativet definerer om serviceordrelinjer som er generert fra en serviceavtale, kombinerer serviceordrer i henhold til ansatt, serviceoppgave, serviceobjekt eller serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="1914d-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="1914d-114">Hvis du vil ha mer informasjon, se [Kombinere serviceordrer](combine-service-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1914d-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="1914d-115">Alternativet **Tidsvindu** på serviceavtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="1914d-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="1914d-116">Tidsvinduet definerer hvor langt en serviceordrelinje kan flyttes i forhold til den beregnede datoen.</span><span class="sxs-lookup"><span data-stu-id="1914d-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="1914d-117">Hvis du vil har mer informasjon, se [Tidsvinduer](time-windows.md).</span><span class="sxs-lookup"><span data-stu-id="1914d-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="1914d-118">Hvis dagen som er angitt for en serviceordre, ikke er åpen i kalenderen du har valgt i skjemaet <STRONG>Servicestyringsparametere</STRONG>, får du en melding om at det er en konflikt med kalenderen.</span><span class="sxs-lookup"><span data-stu-id="1914d-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="1914d-119">Du kan trygt ignorere denne meldingen. Srviceordren opprettes selv om dagen er lukket i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="1914d-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="1914d-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="1914d-120">Example 1</span></span>

<span data-ttu-id="1914d-121">Serviceavtalen varer fra 1. januar 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="1914d-122">Hvis serviceperioden du angir i skjemaet **Opprett serviceordrer**, går fra 1. november 2012 til 1. februar 2013, opprettes det serviceordrer fra 1. november 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="1914d-123">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="1914d-123">Example 2</span></span>

<span data-ttu-id="1914d-124">Serviceavtalen varer fra 1. januar 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="1914d-125">To serviceavtalelinjer er knyttet til serviceavtalen.</span><span class="sxs-lookup"><span data-stu-id="1914d-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="1914d-126">Den første serviceavtalelinjen har startdatoen 2. januar 2012 og sluttdatoen 1. mars 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="1914d-127">Den andre serviceavtalelinjen har startdatoen 1. april 2012 og sluttdatoen 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="1914d-128">Du kan angi en periode i skjemaet **Opprett serviceordrer** som går fra 1. oktober 2012 til 31. desember 2012.</span><span class="sxs-lookup"><span data-stu-id="1914d-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="1914d-129">Det genereres derfor bare serviceordrer for den andre avtalelinjen, siden startdatoen og sluttdatoen for den første avtalelinjen er før perioden du angav for serviceordren.</span><span class="sxs-lookup"><span data-stu-id="1914d-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]