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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853912"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="dfe15-103">Dataintegrering i nær sanntid med Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dfe15-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfe15-104">I dagens digitale verden bruker bedriftsøkosystemer Microsoft Dynamics 365-apper som en helhet.</span><span class="sxs-lookup"><span data-stu-id="dfe15-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="dfe15-105">Fordi data fra personer, kunder, operasjoner og IoT-enheter (tingenes Internett) flyter over i én kilde, finnes det en mulighet for digitale tilbakemeldingsløkker.</span><span class="sxs-lookup"><span data-stu-id="dfe15-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="dfe15-106">For å oppnå denne erfaringen er integrering mellom Finance and Operations-apper og Dynamics 365-apper viktig.</span><span class="sxs-lookup"><span data-stu-id="dfe15-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="dfe15-107">Noen programmer er bygget på toppen av Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dfe15-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="dfe15-108">Integrasjon mellom Finance and Operations-apper med Common Data Service lar andre programmer kommunisere sammenhengende og flytende med Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dfe15-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="dfe15-109">Finance and Operations-apper og Common Data Service gir nær sanntid datasynkronisering mellom Finance and Operations-apper og andre Dynamics 365-programmer via et dual-Write-rammeverk.</span><span class="sxs-lookup"><span data-stu-id="dfe15-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="dfe15-110">Dekningen er bred og spenner over 28 overflateområder av programmet.</span><span class="sxs-lookup"><span data-stu-id="dfe15-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="dfe15-111">Målet er å gi en brukeropplevelse av "Ett Dynamics 365" gjennom sømløse dataflyter som kobler sammen forretningsprosesser på tvers av programmer.</span><span class="sxs-lookup"><span data-stu-id="dfe15-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Oversiktsdiagram over arkitekturen](media/dual-write-overview.jpg)

<span data-ttu-id="dfe15-113">Følgende verdiforslag er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="dfe15-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="dfe15-114">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dfe15-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="dfe15-115">Bedriftskonsept i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="dfe15-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="dfe15-116">Integrerte originalkunde</span><span class="sxs-lookup"><span data-stu-id="dfe15-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="dfe15-117">Integrert finans</span><span class="sxs-lookup"><span data-stu-id="dfe15-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="dfe15-118">Samlet produktopplevelse</span><span class="sxs-lookup"><span data-stu-id="dfe15-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="dfe15-119">Integrert original for leverandør</span><span class="sxs-lookup"><span data-stu-id="dfe15-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="dfe15-120">Integrerte områder og lagre</span><span class="sxs-lookup"><span data-stu-id="dfe15-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="dfe15-121">Integrert hoveddata for avgift</span><span class="sxs-lookup"><span data-stu-id="dfe15-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="dfe15-122">Systemkrav</span><span class="sxs-lookup"><span data-stu-id="dfe15-122">System requirements</span></span>

<span data-ttu-id="dfe15-123">Synkrone, toveis dataflyter i nær sanntid krever følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="dfe15-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="dfe15-124">Microsoft Dynamics 365 for Finance and Operations versjon 10.0.4 (juli 2019) med plattformoppdatering 28 eller senere</span><span class="sxs-lookup"><span data-stu-id="dfe15-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="dfe15-125">Microsoft Dynamics 365 for Customer Engagement, plattformversjon 9.1 (4.2) eller senere</span><span class="sxs-lookup"><span data-stu-id="dfe15-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="dfe15-126">Installasjonsinstruksjoner</span><span class="sxs-lookup"><span data-stu-id="dfe15-126">Setup instructions</span></span>

<span data-ttu-id="dfe15-127">Følg disse trinnene for å konfigurere integrasjonen mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dfe15-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="dfe15-128">For oppsett av dual-Write-systemet, se den [trinnvise veiledningen](https://aka.ms/dualwrite-docs) om kunngjøring av forhåndsvisning av Dual Write.</span><span class="sxs-lookup"><span data-stu-id="dfe15-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="dfe15-129">Last ned og Installer løsningen fra [Fin Ops og CDS/CE-integreringen via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer-gruppen.</span><span class="sxs-lookup"><span data-stu-id="dfe15-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="dfe15-130">Pakken inneholder fem løsninger:</span><span class="sxs-lookup"><span data-stu-id="dfe15-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="dfe15-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="dfe15-131">Dynamics365Company</span></span>
    + <span data-ttu-id="dfe15-132">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="dfe15-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="dfe15-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="dfe15-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="dfe15-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="dfe15-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="dfe15-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="dfe15-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="dfe15-136">Følg utføringsrekkefølgen for [synkronisering av innledende referansedata](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="dfe15-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="dfe15-137">Hvis du støter på problemer med dual-write-skrive synkronisering, kan du se [Feilsøkingsveiledning for dataintegrering](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="dfe15-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfe15-138">Du kan ikke kjøre dual-write og dobbelt-skrive og [Kundeemne til kontanter](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side ved side.</span><span class="sxs-lookup"><span data-stu-id="dfe15-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="dfe15-139">Hvis du kjører Kundeemne til kontanter-løsningen, må du avinstallere den.</span><span class="sxs-lookup"><span data-stu-id="dfe15-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="dfe15-140">Du må også deaktivere dual-write-maler for kunde og leverandør som er en del av Kundeemne til kontanter-løsningen.</span><span class="sxs-lookup"><span data-stu-id="dfe15-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
