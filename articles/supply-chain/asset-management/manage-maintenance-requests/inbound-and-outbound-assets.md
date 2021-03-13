---
title: Innkommende og utgående aktiva
description: Dette emnet forklarer hvordan du registrerer innkommende og utgående aktiva i Aktivabehandling.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018077"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="60071-103">Innkommende og utgående aktiva</span><span class="sxs-lookup"><span data-stu-id="60071-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="60071-104">Hvis firmaet har reparasjonsjobber eller vedlikeholdsjobber på aktiva som mottas fra andre lokasjoner eller kunder, kan Aktivastyring spore både innkommende aktiva som er på vei til firmaet og utgående aktiva som returneres.</span><span class="sxs-lookup"><span data-stu-id="60071-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="60071-105">Hvis du vil bruke inngående og utgående livssyklustilstander til å administrere aktiva som kommer inn og blir returnert, må du definere livssyklustilstander for vedlikeholdsforespørsler og livssyklusmodeller for å støtte disse handlingene.</span><span class="sxs-lookup"><span data-stu-id="60071-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="60071-106">Hvis du vil ha mer informasjon, kan du se [Meldinger](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="60071-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="60071-107">Oppsettet av Aktivastyring bestemmer om du kan arbeide med inngående og utgående aktiva.</span><span class="sxs-lookup"><span data-stu-id="60071-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="60071-108">Registrer aktiva som inngående</span><span class="sxs-lookup"><span data-stu-id="60071-108">Register assets as inbound</span></span>

1. <span data-ttu-id="60071-109">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="60071-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="60071-110">Velg vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="60071-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="60071-111">Velg **Oppdater tilstand for vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="60071-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="60071-112">Velg **Inngående** (eller en annen livssyklustilstand som du har opprettet for innkommende aktiva), og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="60071-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registrer aktiva som inngående](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="60071-114">Registrer innkommende aktiva som mottatt</span><span class="sxs-lookup"><span data-stu-id="60071-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="60071-115">Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Innkommende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="60071-116">Velg aktivumet eller vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="60071-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="60071-117">Velg **Motta aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="60071-118">Angi dato og klokkeslett i feltet **Mottatt**.</span><span class="sxs-lookup"><span data-stu-id="60071-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="60071-119">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="60071-119">Then select **OK**.</span></span> <span data-ttu-id="60071-120">Posten fjernes fra listesiden **Innkommede aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registrer innkommende aktiva som mottatt](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="60071-122">Registrer aktiva som utgående</span><span class="sxs-lookup"><span data-stu-id="60071-122">Register assets as outbound</span></span>

<span data-ttu-id="60071-123">Når du har fullført vedlikeholds- eller reparasjonsjobben, kan du registrere aktivumet som returnert.</span><span class="sxs-lookup"><span data-stu-id="60071-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="60071-124">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="60071-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="60071-125">Velg vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="60071-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="60071-126">Velg **Oppdater tilstand for vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="60071-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="60071-127">Velg **Utgående** (eller en annen livssyklustilstand som du har opprettet for utgående aktiva), og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="60071-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="60071-128">Registrer utgående aktiva som levert</span><span class="sxs-lookup"><span data-stu-id="60071-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="60071-129">Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Utgående aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="60071-130">Velg aktivumet eller vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="60071-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="60071-131">Velg **Lever aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="60071-132">Angi dato og klokkeslett i feltet **Levert**.</span><span class="sxs-lookup"><span data-stu-id="60071-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="60071-133">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="60071-133">Then select **OK**.</span></span> <span data-ttu-id="60071-134">Posten fjernes fra listesiden **Utgående aktiva**.</span><span class="sxs-lookup"><span data-stu-id="60071-134">The record is removed from the **Outbound assets** list page.</span></span>
