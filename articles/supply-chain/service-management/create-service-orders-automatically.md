---
title: Opprette serviceordrer automatisk
description: Du kan opprette serviceordrer for én serviceavtale eller for flere serviceavtaler.
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
ms.openlocfilehash: cc06536827320a35a691330d852ba64532604935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817611"
---
# <a name="create-service-orders-automatically"></a><span data-ttu-id="ff42a-103">Opprette serviceordrer automatisk</span><span class="sxs-lookup"><span data-stu-id="ff42a-103">Create service orders automatically</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ff42a-104">Du kan opprette serviceordrer for én serviceavtale eller for flere serviceavtaler.</span><span class="sxs-lookup"><span data-stu-id="ff42a-104">You can create service orders for one service agreement or for several service agreements.</span></span> <span data-ttu-id="ff42a-105">Når de er opprettet, kan du vise serviceordrene i **Serviceordrer**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="ff42a-105">When they are created, you can view your service orders in the **Service orders** form.</span></span>

<span data-ttu-id="ff42a-106">Serviceordrer opprettes bare for serviceavtalens gyldighetsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff42a-106">Service orders are created only for the valid period of the service agreement.</span></span> <span data-ttu-id="ff42a-107">Hvis intervallet du angir i skjemaet **Opprett serviceordrer**, er før startdatoen eller etter sluttdatoen for serviceavtalen, opprettes det bare serviceordrer for den delen av intervallet som er innenfor serviceavtalens gyldighetsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff42a-107">If the interval that you specify in the **Create service orders** form is before the starting date or after the ending date of the service agreement, service orders are created only for the part of the interval that is within the service agreement dates.</span></span>

<span data-ttu-id="ff42a-108">Når du oppretter serviceordrer manuelt eller automatisk fra serviceavtalelinjen, må serviceordren falle innenfor tidsintervallet som er definert av start- og sluttdatoen for linjen, med mindre du ikke angir en sluttdato på linjen.</span><span class="sxs-lookup"><span data-stu-id="ff42a-108">When you create service orders manually or automatically from the service agreement line, the service order must be in the time interval that is defined by the starting and ending dates for the line, unless you do not specify an ending date on the line.</span></span>

## <a name="create-service-orders-automatically-for-a-service-agreement"></a><span data-ttu-id="ff42a-109">Opprette serviceordrer for en serviceavtale automatisk</span><span class="sxs-lookup"><span data-stu-id="ff42a-109">Create service orders automatically for a service agreement</span></span>

1.  <span data-ttu-id="ff42a-110">Klikk på **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-110">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="ff42a-111">Velg en serviceavtale.</span><span class="sxs-lookup"><span data-stu-id="ff42a-111">Select a service agreement.</span></span>

3.  <span data-ttu-id="ff42a-112">Klikk på fanen **Lever**, og klikk deretter **Planlagte serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-112">Click the **Deliver** tab, and then click **Planned service orders**.</span></span>

4.  <span data-ttu-id="ff42a-113">Angi datoer i feltene **Fra dato** og **Til dato** for å definere serviceavtalens gyldighetsperiode.</span><span class="sxs-lookup"><span data-stu-id="ff42a-113">Specify dates in the **From date** and **To date** fields to define the service period.</span></span>

5.  <span data-ttu-id="ff42a-114">Merk av for **Vis infologg** for å vise en liste over serviceordrene som opprettes.</span><span class="sxs-lookup"><span data-stu-id="ff42a-114">Select the **Show Infolog** check box to display a list of the service orders that are created.</span></span>

6.  <span data-ttu-id="ff42a-115">Velg transaksjonstypene i feltgruppen **Inkluder transaksjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-115">Select transaction types in the **Include transaction types** field group.</span></span> <span data-ttu-id="ff42a-116">Transaksjonstypene representerer linjene som opprettes i serviceavtalen, og hver transaksjonstype du velger, genererer flere serviceordrer, avhengig av serviceintervallet som er angitt for serviceavtalelinjen.</span><span class="sxs-lookup"><span data-stu-id="ff42a-116">The transaction types represent the lines that are created in the service agreement, and each transaction type that you select generates several service orders, depending on the service interval that is specified on the service agreement line.</span></span>

7.  <span data-ttu-id="ff42a-117">Merk av for **Kontinuerlig** hvis du vil opprette eventuelle serviceordrer som mangler i en kontinuerlig serie av serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="ff42a-117">To create any service orders that are missing from continuous series of service orders, select the **Continuous** check box.</span></span>

8.  <span data-ttu-id="ff42a-118">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-118">Click **OK**.</span></span>

## <a name="create-service-orders-automatically-for-several-service-agreements"></a><span data-ttu-id="ff42a-119">Opprette serviceordrer for flere serviceavtaler automatisk</span><span class="sxs-lookup"><span data-stu-id="ff42a-119">Create service orders automatically for several service agreements</span></span>

1.  <span data-ttu-id="ff42a-120">Klikk på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Opprett serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-120">Click **Service management** \> **Periodic** \> **Service orders** \> **Create service orders**.</span></span>

2.  <span data-ttu-id="ff42a-121">Klikk på **Velg** for å angi valg for å legge til eller fjerne kriterier som skal brukes til å opprette serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="ff42a-121">Click **Select** to make selections to add or remove criteria to use to create service orders.</span></span>

3.  <span data-ttu-id="ff42a-122">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff42a-122">Click **OK**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff42a-123">Se også</span><span class="sxs-lookup"><span data-stu-id="ff42a-123">See also</span></span>

[<span data-ttu-id="ff42a-124">Serviceordrer</span><span class="sxs-lookup"><span data-stu-id="ff42a-124">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="ff42a-125">Automatisk opprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="ff42a-125">Automatically create service orders</span></span>](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]