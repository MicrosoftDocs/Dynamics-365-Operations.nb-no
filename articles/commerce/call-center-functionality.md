---
title: Salgsfunksjonalitet for telefonsenter
description: Dette emnet gir en oversikt over telefonsenterspesifikke salgsfunksjoner i Dynamics 365 Commerce.
author: josaw1
ms.date: 04/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f1660399e7e88a8f7c96714f9af271b73a17eca2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799619"
---
# <a name="call-center-sales-functionality"></a><span data-ttu-id="6d55a-103">Salgsfunksjonalitet for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="6d55a-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="6d55a-104">I Dynamics 365 Commerce er et telefonsenter en type kanal som kan defineres i programmet.</span><span class="sxs-lookup"><span data-stu-id="6d55a-104">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="6d55a-105">Ved å definere en bestemt kanal for telefonsenterenheter kan systemet knytte bestemte datastandarder og andre ordrebehandlingsstandarder til salgsordrer som er opprettet av en bruker av lefonsenterkanalen.</span><span class="sxs-lookup"><span data-stu-id="6d55a-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="6d55a-106">Telefonsenterfunksjonene omfatter avansert pris og kampanjer, kataloger, gavekort, lojalitetsprogrammer og kuponger.</span><span class="sxs-lookup"><span data-stu-id="6d55a-106">Call center features include advanced price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="6d55a-107">Telefonsenterordrer utnyttes også av salgsstedsprogrammet (POS) til å støtte ordrefullføring på tvers av kanaler.</span><span class="sxs-lookup"><span data-stu-id="6d55a-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="6d55a-108">Det er viktig å være klar over at selv om telefonsentermodulen kan brukes av andre bransjer utenfor handel, er ikke den gjeldende versjonen av telefonsenterprogrammet optimalisert for bruk i B2B-ordrebehandlingsscenarier (bedrift til bedrift) eller scenarier der ordrer har store mengder salgslinjer.</span><span class="sxs-lookup"><span data-stu-id="6d55a-108">It's important to note that while the call center module can be utilized by other industries outside of Commerce, the current release of the call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large number of sales lines.</span></span> <span data-ttu-id="6d55a-109">Det anbefales at brukere som ønsker å bruke telefonsenterfunksjoner for ordrebehandling utenfor vanlig transaksjonsbehandling direkte til kunde, tar seg tilstrekkelig tid til å teste og validere at aktivering av telefonsenterfunksjonene oppfyller funksjonelle og ytelsesbehov.</span><span class="sxs-lookup"><span data-stu-id="6d55a-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="6d55a-110">I tillegg til støtte for ordreoppretting har telefonsentermodulen også et brukervennlig kundeserviceprogram som gjør det enklere for brukerne å finne kundekontoer og gå gjennom alle tilknyttede ordredata og attributter.</span><span class="sxs-lookup"><span data-stu-id="6d55a-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="6d55a-111">Kundetjenesteskjermen er utformet for at en bruker raskt skal kunne få tilgang til ordrerelaterte data som gjør at de kan svare på de fleste vanlige ordrerelaterte spørsmål fra kunder.</span><span class="sxs-lookup"><span data-stu-id="6d55a-111">The customer service screen is designed to enable a user to quickly access order-related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="6d55a-112">Denne siden inneholder koblinger til relevante dokumentasjon som er knyttet til installasjon, konfigurasjon og funksjonell bruk av telefonsenterfunksjonene.</span><span class="sxs-lookup"><span data-stu-id="6d55a-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features.</span></span>


## <a name="configure-the-call-center"></a><span data-ttu-id="6d55a-113">Konfigurere telefonsenteret</span><span class="sxs-lookup"><span data-stu-id="6d55a-113">Configure the call center</span></span>

[<span data-ttu-id="6d55a-114">Definere telefonsenterkanaler</span><span class="sxs-lookup"><span data-stu-id="6d55a-114">Set up call center channels</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="6d55a-115">Konfigurere ordrebehandling</span><span class="sxs-lookup"><span data-stu-id="6d55a-115">Configure order processing</span></span>

[<span data-ttu-id="6d55a-116">Definere og arbeide med telefonsentersvindelvarsler</span><span class="sxs-lookup"><span data-stu-id="6d55a-116">Set up and work with call center fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="6d55a-117">Konfigurere og arbeide med ordresperrer i telefonsenter</span><span class="sxs-lookup"><span data-stu-id="6d55a-117">Configure and work with call center order holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="6d55a-118">Konfigurere betalingsbehandling</span><span class="sxs-lookup"><span data-stu-id="6d55a-118">Configure payment processing</span></span>

[<span data-ttu-id="6d55a-119">Betalingsmåter i telefonsentre</span><span class="sxs-lookup"><span data-stu-id="6d55a-119">Payment methods in call centers</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="6d55a-120">Konfigurere leveringsmåter</span><span class="sxs-lookup"><span data-stu-id="6d55a-120">Configure delivery modes</span></span>

[<span data-ttu-id="6d55a-121">Konfigurere leveringsmåter og tillegg for telefonsenter</span><span class="sxs-lookup"><span data-stu-id="6d55a-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="6d55a-122">Konfigurere direkte markedsføring</span><span class="sxs-lookup"><span data-stu-id="6d55a-122">Configure direct marketing</span></span>

[<span data-ttu-id="6d55a-123">Telefonsenterkataloger</span><span class="sxs-lookup"><span data-stu-id="6d55a-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="6d55a-124">Definere RFM-analyse (Recency, Frequency, and Monetary)</span><span class="sxs-lookup"><span data-stu-id="6d55a-124">Set up Recency, Frequency, and Monetary (RFM) analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="6d55a-125">Konfigurere kontinuitetsprogrammer</span><span class="sxs-lookup"><span data-stu-id="6d55a-125">Configure continuity programs</span></span>

[<span data-ttu-id="6d55a-126">Definere kontinuitetsprogrammer for telefonsentre</span><span class="sxs-lookup"><span data-stu-id="6d55a-126">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]