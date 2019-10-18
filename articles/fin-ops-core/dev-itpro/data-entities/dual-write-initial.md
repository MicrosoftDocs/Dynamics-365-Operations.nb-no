---
title: Utføringsordre for innledende synkronisering av Finance and Operations-apper og Common Data Service
description: Dette emnet angir rekkefølgen for synkroniseringen du må følge for å opprette de opprinnelige dataene.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 3110cb809558d168e9d97f640701b249caf73f6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184514"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="825a0-103">Utføringsordre for innledende synkronisering av Finance and Operations-apper og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="825a0-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="825a0-104">Før du bruker dataintegrering, må du opprette de første dataene som kreves for kunder, leverandører og kontakter.</span><span class="sxs-lookup"><span data-stu-id="825a0-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="825a0-105">Du vil for eksempel opprette en ny **Leverandørgruppe**-vare og sette **Betalingsvilkår**-verdien til **Net30**.</span><span class="sxs-lookup"><span data-stu-id="825a0-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="825a0-106">Før du prøver å opprette **Leverandørgruppe**-varen, må du i dette tilfellet kontrollere at **Net30** finnes i både programmet og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="825a0-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="825a0-107">(I fremtiden vil Microsoft gi ut en dobbel skrive plattform funksjonalitet kalt Initial Sync. Denne funksjonaliteten vil gjøre en éngangs datasynkronisering mellom programmet og Common Data Service som en del av dual-Write-oppsettet.)</span><span class="sxs-lookup"><span data-stu-id="825a0-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="825a0-108">Microsoft lanserer et dual-Write-kart for alle referansedata, inkludert **betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="825a0-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="825a0-109">Hvis du allerede har de opprinnelige dataene i ett system, kan en liten oppdateringsoperasjon på en oppføring utløse dobbel skriving på denne oppføringen.</span><span class="sxs-lookup"><span data-stu-id="825a0-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="825a0-110">Du må følge følgende prioritetsrekkefølge og kontrollere at de opprinnelige dataene er tilgjengelige både i programmet og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="825a0-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="825a0-111">Leverandør</span><span class="sxs-lookup"><span data-stu-id="825a0-111">Vendor</span></span>

<span data-ttu-id="825a0-112">Her er utførelsesrekkefølgen for **Leverandør**-enheten:</span><span class="sxs-lookup"><span data-stu-id="825a0-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="825a0-113">Leverandørgruppe</span><span class="sxs-lookup"><span data-stu-id="825a0-113">Vendor group</span></span>

    1. <span data-ttu-id="825a0-114">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="825a0-114">Terms of payment</span></span>

        1. <span data-ttu-id="825a0-115">Betalingsdag og linjer</span><span class="sxs-lookup"><span data-stu-id="825a0-115">Payment day and lines</span></span>
        2. <span data-ttu-id="825a0-116">Betalingsplan</span><span class="sxs-lookup"><span data-stu-id="825a0-116">Payment schedule</span></span>

2. <span data-ttu-id="825a0-117">Betalingsmåte for leverandør</span><span class="sxs-lookup"><span data-stu-id="825a0-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="825a0-118">Kunde (organisasjon)</span><span class="sxs-lookup"><span data-stu-id="825a0-118">Customer (Organization)</span></span>

<span data-ttu-id="825a0-119">Her er utførelsesrekkefølgen for **Kunde**-enheten:</span><span class="sxs-lookup"><span data-stu-id="825a0-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="825a0-120">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="825a0-120">Customer group</span></span>

    1. <span data-ttu-id="825a0-121">Betalingsbetingelser</span><span class="sxs-lookup"><span data-stu-id="825a0-121">Terms of payment</span></span>

        1. <span data-ttu-id="825a0-122">Betalingsdag og linjer</span><span class="sxs-lookup"><span data-stu-id="825a0-122">Payment day and lines</span></span>
        2. <span data-ttu-id="825a0-123">Betaling</span><span class="sxs-lookup"><span data-stu-id="825a0-123">Payment</span></span> 

2. <span data-ttu-id="825a0-124">Kundebetalingsmåte</span><span class="sxs-lookup"><span data-stu-id="825a0-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="825a0-125">Kontakt (person)</span><span class="sxs-lookup"><span data-stu-id="825a0-125">Contact (Person)</span></span>

<span data-ttu-id="825a0-126">Her er utførelsesrekkefølgen for **Kontakt**-enheten:</span><span class="sxs-lookup"><span data-stu-id="825a0-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="825a0-127">Kunde</span><span class="sxs-lookup"><span data-stu-id="825a0-127">Customer</span></span>
2. <span data-ttu-id="825a0-128">Leverandør</span><span class="sxs-lookup"><span data-stu-id="825a0-128">Vendor</span></span>
