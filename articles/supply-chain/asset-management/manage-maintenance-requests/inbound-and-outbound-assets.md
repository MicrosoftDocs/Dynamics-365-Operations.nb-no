---
title: Innkommende og utgående aktiva
description: Dette emnet forklarer hvordan du registrerer innkommende og utgående aktiva i Aktivabehandling.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847557"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="da408-103">Innkommende og utgående aktiva</span><span class="sxs-lookup"><span data-stu-id="da408-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="da408-104">Hvis firmaet har reparasjonsjobber eller vedlikeholdsjobber på aktiva som mottas fra andre lokasjoner eller kunder, kan Aktivastyring spore både innkommende aktiva som er på vei til firmaet og utgående aktiva som returneres.</span><span class="sxs-lookup"><span data-stu-id="da408-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="da408-105">Hvis du vil bruke inngående og utgående livsløpstilstander til å administrere aktiva som kommer inn og blir returnert, må du definere livsløpstilstander for vedlikeholdsforespørsler og livsløpsmodeller for å støtte disse handlingene.</span><span class="sxs-lookup"><span data-stu-id="da408-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="da408-106">Hvis du vil ha mer informasjon, kan du se [Oppsett for vedlikeholdsanmodninger](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="da408-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="da408-107">Oppsettet av Aktivastyring bestemmer om du kan arbeide med inngående og utgående aktiva.</span><span class="sxs-lookup"><span data-stu-id="da408-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="da408-108">Registrer aktiva som inngående</span><span class="sxs-lookup"><span data-stu-id="da408-108">Register assets as inbound</span></span>

1. <span data-ttu-id="da408-109">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="da408-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="da408-110">Velg vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="da408-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="da408-111">Velg **Oppdater tilstand for vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="da408-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="da408-112">Velg **Inngående** (eller en annen livsløpstilstand som du har opprettet for innkommende aktiva), og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da408-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Figur 1](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="da408-114">Registrer innkommende aktiva som mottatt</span><span class="sxs-lookup"><span data-stu-id="da408-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="da408-115">Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Innkommende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="da408-116">Velg aktivumet eller vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="da408-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="da408-117">Velg **Motta aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="da408-118">Angi dato og klokkeslett i feltet **Mottatt**.</span><span class="sxs-lookup"><span data-stu-id="da408-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="da408-119">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da408-119">Then select **OK**.</span></span> <span data-ttu-id="da408-120">Posten fjernes fra listesiden **Innkommede aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-120">The record is removed from the **Inbound assets** list page.</span></span>

![Figur 2](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="da408-122">Registrer aktiva som utgående</span><span class="sxs-lookup"><span data-stu-id="da408-122">Register assets as outbound</span></span>

<span data-ttu-id="da408-123">Når du har fullført vedlikeholds- eller reparasjonsjobben, kan du registrere aktivaet som returnert.</span><span class="sxs-lookup"><span data-stu-id="da408-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="da408-124">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="da408-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="da408-125">Velg vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="da408-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="da408-126">Velg **Oppdater tilstand for vedlikeholdsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="da408-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="da408-127">Velg **Utgående** (eller en annen livsløpstilstand som du har opprettet for utgående aktiva), og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da408-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="da408-128">Registrer utgående aktiva som levert</span><span class="sxs-lookup"><span data-stu-id="da408-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="da408-129">Velg **Aktivastyring** \> **Felles** \> **Innkommende/utgående** \> **Utgående aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="da408-130">Velg aktivumet eller vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="da408-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="da408-131">Velg **Lever aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="da408-132">Angi dato og klokkeslett i feltet **Levert**.</span><span class="sxs-lookup"><span data-stu-id="da408-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="da408-133">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="da408-133">Then select **OK**.</span></span> <span data-ttu-id="da408-134">Posten fjernes fra listesiden **Utgående aktiva**.</span><span class="sxs-lookup"><span data-stu-id="da408-134">The record is removed from the **Outbound assets** list page.</span></span>
