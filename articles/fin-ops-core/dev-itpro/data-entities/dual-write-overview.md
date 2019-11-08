---
title: Dataintegrering i nær sanntid med Common Data Service
description: Dette emnet inneholder en oversikt over integreringen mellom Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: d70bce4e47c05a7974c1b974fdca17682e5370aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550863"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="82351-103">Dataintegrering i nær sanntid med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="82351-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="82351-104">I dagens digitale verden bruker bedriftsøkosystemer Microsoft Dynamics 365-apper som en helhet.</span><span class="sxs-lookup"><span data-stu-id="82351-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="82351-105">Fordi data fra personer, kunder, operasjoner og IoT-enheter (tingenes Internett) flyter over i én kilde, finnes det en mulighet for digitale tilbakemeldingsløkker.</span><span class="sxs-lookup"><span data-stu-id="82351-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="82351-106">For å oppnå denne erfaringen er integrering mellom Finance and Operations-apper og Dynamics 365-apper viktig.</span><span class="sxs-lookup"><span data-stu-id="82351-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="82351-107">Noen programmer er bygget på toppen av Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="82351-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="82351-108">Integrasjon mellom Finance and Operations-apper med Common Data Service lar andre programmer kommunisere sammenhengende og flytende med Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82351-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="82351-109">Finance and Operations-apper og Common Data Service gir nær sanntid datasynkronisering mellom Finance and Operations-apper og andre Dynamics 365-programmer via et dual-Write-rammeverk.</span><span class="sxs-lookup"><span data-stu-id="82351-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="82351-110">Dekningen er bred og spenner over 28 overflateområder av programmet.</span><span class="sxs-lookup"><span data-stu-id="82351-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="82351-111">Målet er å gi en brukeropplevelse av "Ett Dynamics 365" gjennom sømløse dataflyter som kobler sammen forretningsprosesser på tvers av programmer.</span><span class="sxs-lookup"><span data-stu-id="82351-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Oversiktsdiagram over arkitekturen](media/dual-write-overview.jpg)

<span data-ttu-id="82351-113">Følgende verdiforslag er tilgjengelige for kunder:</span><span class="sxs-lookup"><span data-stu-id="82351-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="82351-114">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="82351-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="82351-115">Bedriftskonsept i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="82351-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="82351-116">Integrerte originalkunde</span><span class="sxs-lookup"><span data-stu-id="82351-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="82351-117">Integrert original for leverandør</span><span class="sxs-lookup"><span data-stu-id="82351-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="82351-118">Ensartet produktstandard</span><span class="sxs-lookup"><span data-stu-id="82351-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="82351-119">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="82351-119">System requirements</span></span>

<span data-ttu-id="82351-120">Synkrone, toveis dataflyter i nær sanntid krever følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="82351-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="82351-121">Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) med plattformoppdatering 28 eller senere</span><span class="sxs-lookup"><span data-stu-id="82351-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="82351-122">Microsoft Dynamics 365 for Customer Engagement, plattformversjon 9.1 (4.2) eller senere</span><span class="sxs-lookup"><span data-stu-id="82351-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="82351-123">Installasjonsinstruksjoner</span><span class="sxs-lookup"><span data-stu-id="82351-123">Setup instructions</span></span>

<span data-ttu-id="82351-124">Følg disse trinnene for å konfigurere integrasjonen mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="82351-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="82351-125">For oppsett av dual-Write-systemet, se den [trinnvise veiledningen](https://aka.ms/dualwrite-docs) om kunngjøring av forhåndsvisning av Dual Write.</span><span class="sxs-lookup"><span data-stu-id="82351-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="82351-126">Last ned og installer løsningen fra gruppen [Finance and Operations, Common Data Service Customer Engagement-integrasjon](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer.</span><span class="sxs-lookup"><span data-stu-id="82351-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="82351-127">Pakken inneholder fem løsninger:</span><span class="sxs-lookup"><span data-stu-id="82351-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="82351-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="82351-128">Dynamics365Company</span></span>
    + <span data-ttu-id="82351-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="82351-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="82351-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="82351-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="82351-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="82351-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="82351-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="82351-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="82351-133">Følg utføringsrekkefølgen for [synkronisering av innledende referansedata](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="82351-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="82351-134">Hvis du støter på problemer med dual-write-skrive synkronisering, kan du se [Feilsøkingsveiledning for dataintegrering](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="82351-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82351-135">Du kan ikke kjøre dual-write og dobbelt-skrive og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side ved side.</span><span class="sxs-lookup"><span data-stu-id="82351-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="82351-136">Hvis du kjører Kundeemne til kontanter-løsningen, må du avinstallere den.</span><span class="sxs-lookup"><span data-stu-id="82351-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="82351-137">Du må også deaktivere dual-write-maler for kunde og leverandør som er en del av Kundeemne til kontanter-løsningen.</span><span class="sxs-lookup"><span data-stu-id="82351-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
