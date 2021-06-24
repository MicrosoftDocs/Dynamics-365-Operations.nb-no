---
title: Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid
description: Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123849"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="f6b82-103">Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid</span><span class="sxs-lookup"><span data-stu-id="f6b82-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="f6b82-104">Feilkode: WAX515</span><span class="sxs-lookup"><span data-stu-id="f6b82-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="f6b82-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f6b82-105">Symptoms</span></span>

<span data-ttu-id="f6b82-106">Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="f6b82-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f6b82-107">Forsendelsen av lasten %1 kan ikke bekreftes fordi alt arbeid for lasten må være fullført.</span><span class="sxs-lookup"><span data-stu-id="f6b82-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="f6b82-108">Derfor kan du ikke bekrefte forsendelsen for belastningen.</span><span class="sxs-lookup"><span data-stu-id="f6b82-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f6b82-109">Årsak</span><span class="sxs-lookup"><span data-stu-id="f6b82-109">Cause</span></span>

<span data-ttu-id="f6b82-110">Lasten eller forsendelsen er for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="f6b82-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="f6b82-111">Før du kan bekrefte forsendelsen, må det minst finnes noe arbeid for lasten, og alt arbeidet må ha statusen *Lukket* eller *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="f6b82-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="f6b82-112">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="f6b82-112">Resolution</span></span>

<span data-ttu-id="f6b82-113">Kontroller de tilknyttede salgsordrene eller overføringsordrene for lasten eller forsendelsen, og kontroller at alt tilknyttet arbeid er fullført eller avbrutt.</span><span class="sxs-lookup"><span data-stu-id="f6b82-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="f6b82-114">Du kan arbeide med forsendelser og laster på flere sider.</span><span class="sxs-lookup"><span data-stu-id="f6b82-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="f6b82-115">De følgende underdelene gir noen eksempler.</span><span class="sxs-lookup"><span data-stu-id="f6b82-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="f6b82-116">Alle laster-siden</span><span class="sxs-lookup"><span data-stu-id="f6b82-116">All loads page</span></span>

1. <span data-ttu-id="f6b82-117">Gå til **Lagerstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="f6b82-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f6b82-118">Velg belastningen som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="f6b82-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f6b82-119">I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.</span><span class="sxs-lookup"><span data-stu-id="f6b82-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="f6b82-120">Kontroller statusen til hver arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="f6b82-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="f6b82-121">En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="f6b82-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="f6b82-122">Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="f6b82-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="f6b82-123">Alle forsendelser-siden</span><span class="sxs-lookup"><span data-stu-id="f6b82-123">All shipments page</span></span>

1. <span data-ttu-id="f6b82-124">Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="f6b82-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="f6b82-125">Velg forsendelsen som ikke kan bekreftes.</span><span class="sxs-lookup"><span data-stu-id="f6b82-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="f6b82-126">Velg **Arbeidsdetaljer** i gruppen **Arbeid** i fanen **Forsendelser** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f6b82-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="f6b82-127">Kontroller statusen til hver arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="f6b82-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="f6b82-128">En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="f6b82-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="f6b82-129">Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="f6b82-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="f6b82-130">Alt arbeid-siden</span><span class="sxs-lookup"><span data-stu-id="f6b82-130">All work page</span></span>

1. <span data-ttu-id="f6b82-131">Gå til **Lagerstyring \> Arbeid \> Alt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="f6b82-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="f6b82-132">Velg arbeidet for ordrenummeret som forsendelsen ikke kan bekreftes for.</span><span class="sxs-lookup"><span data-stu-id="f6b82-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f6b82-133">Velg **Bekreft forsendelse** i gruppen **Forsendelse** i fanen **Forsendelse** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f6b82-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="f6b82-134">Kontroller statusen til hver arbeids-ID.</span><span class="sxs-lookup"><span data-stu-id="f6b82-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="f6b82-135">En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.</span><span class="sxs-lookup"><span data-stu-id="f6b82-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="f6b82-136">Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="f6b82-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
