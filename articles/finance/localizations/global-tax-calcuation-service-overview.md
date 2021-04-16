---
title: Avgiftsberegningstjeneste (forhåndsversjon)
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegningstjenesten.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818230"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="c3a4d-103">Avgiftsberegningstjeneste (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="c3a4d-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c3a4d-104">Avgiftsberegningstjenesten er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="c3a4d-105">Avgiftsmotoren er fullt konfigurerbar.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="c3a4d-106">Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="c3a4d-107">Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="c3a4d-108">Tjenesten for avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c3a4d-109">Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="c3a4d-110">Tjenesten for avgiftsberegning er en Microsoft-basert avgiftsmotor som tilbyr eksponenentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="c3a4d-111">Den kan hjelpe dem med å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="c3a4d-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="c3a4d-112">Konfigurer avgiftsberegningstjenesten via RCS (Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="c3a4d-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="c3a4d-113">RCS er en utvidet versjon av ER-designeren (elektronisk rapportering) og er tilgjengelig som en frittstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="c3a4d-114">Konfigurer avgiftsmatrisen slik at avgiftskoder og -satser bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="c3a4d-115">Konfigurer avgiftsmatrisen slik at avgiftsregistreringsnummeret bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="c3a4d-116">Konfigurer avgiftsberegningsdesigneren for å definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="c3a4d-117">Del løsningen for avgiftsfastsettelse og -beregning på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="c3a4d-118">Hvis du vil bruke tjenesten for avgiftsberegning, installerer du tillegget for avgiftsberegningstjenesten fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c3a4d-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c3a4d-119">Deretter fullfører du oppsettet i RCS og aktiverer avgiftsberegningstjenesten i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="c3a4d-120">Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="c3a4d-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="c3a4d-121">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="c3a4d-121">Availability</span></span>

<span data-ttu-id="c3a4d-122">Tjenesten for avgiftsberegning er bare tilgjengelig i sandkassemiljøer og for utvalgte kunder via et program som offentlig forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="c3a4d-123">Til slutt vil det bli allment tilgjengelig for alle kunder og i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="c3a4d-124">Nye funksjoner vil fortsatt bli levert i avgiftsberegningstjenesten.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="c3a4d-125">Pass derfor på at du ofte kontrollerer den mest oppdaterte dokumentasjonen for å finne ut om dekningen og omfanget av funksjoner som støttes.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="c3a4d-126">Tjenesten for avgiftsberegning distribueres i følgende Azure-geografier.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="c3a4d-127">Det vil også bli distribuert til flere Azure-geografier, basert på kundebehov:</span><span class="sxs-lookup"><span data-stu-id="c3a4d-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="c3a4d-128">USA</span><span class="sxs-lookup"><span data-stu-id="c3a4d-128">United States</span></span>
- <span data-ttu-id="c3a4d-129">Europa</span><span class="sxs-lookup"><span data-stu-id="c3a4d-129">Europe</span></span>
- <span data-ttu-id="c3a4d-130">Frankrike</span><span class="sxs-lookup"><span data-stu-id="c3a4d-130">France</span></span>
- <span data-ttu-id="c3a4d-131">Storbritannia</span><span class="sxs-lookup"><span data-stu-id="c3a4d-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="c3a4d-132">Avgiftsberegningstjenesten støtter ikke lokale distribusjoner av Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="c3a4d-133">Den støtter heller ikke tidligere versjoner, for eksempel Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="c3a4d-134">Funksjonsfremhevinger</span><span class="sxs-lookup"><span data-stu-id="c3a4d-134">Feature highlights</span></span>

- <span data-ttu-id="c3a4d-135">En konfigurerbare avgiftsmatrise for automatisk bestemming og beregning av avgifter</span><span class="sxs-lookup"><span data-stu-id="c3a4d-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="c3a4d-136">Støtte for flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="c3a4d-137">Overføringsordrestøtte for fastsettelse og beregning av avgift</span><span class="sxs-lookup"><span data-stu-id="c3a4d-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="c3a4d-138">Støtte for overføringsordre for fastsettelse av flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="c3a4d-139">Transaksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="c3a4d-139">Supported transactions</span></span>

<span data-ttu-id="c3a4d-140">Avgiftsberegningstjenesten kan aktiveres ved hjelp av juridisk enhet og transaksjon.</span><span class="sxs-lookup"><span data-stu-id="c3a4d-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="c3a4d-141">Følgende transaksjoner støttes:</span><span class="sxs-lookup"><span data-stu-id="c3a4d-141">The following transactions are supported:</span></span>

- <span data-ttu-id="c3a4d-142">Salgsprosess</span><span class="sxs-lookup"><span data-stu-id="c3a4d-142">Sales process</span></span>

    - <span data-ttu-id="c3a4d-143">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="c3a4d-143">Sales quotation</span></span>
    - <span data-ttu-id="c3a4d-144">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-144">Sales order</span></span>
    - <span data-ttu-id="c3a4d-145">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="c3a4d-145">Confirmation</span></span>
    - <span data-ttu-id="c3a4d-146">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="c3a4d-146">Picking list</span></span>
    - <span data-ttu-id="c3a4d-147">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="c3a4d-147">Packing slip</span></span>
    - <span data-ttu-id="c3a4d-148">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="c3a4d-148">Sales invoice</span></span>
    - <span data-ttu-id="c3a4d-149">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="c3a4d-149">Credit note</span></span>
    - <span data-ttu-id="c3a4d-150">Returordre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-150">Return order</span></span>
    - <span data-ttu-id="c3a4d-151">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="c3a4d-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c3a4d-152">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="c3a4d-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="c3a4d-153">Innkjøpsprosess</span><span class="sxs-lookup"><span data-stu-id="c3a4d-153">Purchase process</span></span>

    - <span data-ttu-id="c3a4d-154">Bestilling</span><span class="sxs-lookup"><span data-stu-id="c3a4d-154">Purchase order</span></span>
    - <span data-ttu-id="c3a4d-155">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="c3a4d-155">Confirmation</span></span>
    - <span data-ttu-id="c3a4d-156">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="c3a4d-156">Receipts list</span></span>
    - <span data-ttu-id="c3a4d-157">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="c3a4d-157">Product receipt</span></span>
    - <span data-ttu-id="c3a4d-158">Innkjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="c3a4d-158">Purchase invoice</span></span>
    - <span data-ttu-id="c3a4d-159">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="c3a4d-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c3a4d-160">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="c3a4d-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="c3a4d-161">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="c3a4d-161">Credit note</span></span>
    - <span data-ttu-id="c3a4d-162">Returordre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-162">Return order</span></span>
    - <span data-ttu-id="c3a4d-163">Innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="c3a4d-163">Purchase requisition</span></span>
    - <span data-ttu-id="c3a4d-164">Diverse tillegg på innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="c3a4d-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="c3a4d-165">Tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="c3a4d-165">Request for quotation</span></span>
    - <span data-ttu-id="c3a4d-166">Diverse tillegg på tilbudsforespørselshode</span><span class="sxs-lookup"><span data-stu-id="c3a4d-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="c3a4d-167">Diverse tillegg på tilbudsforespørselslinje</span><span class="sxs-lookup"><span data-stu-id="c3a4d-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="c3a4d-168">Beholdningsprosess</span><span class="sxs-lookup"><span data-stu-id="c3a4d-168">Inventory process</span></span>

    - <span data-ttu-id="c3a4d-169">Overføringsordre – send</span><span class="sxs-lookup"><span data-stu-id="c3a4d-169">Transfer order – ship</span></span>
    - <span data-ttu-id="c3a4d-170">Overføringsordre – motta</span><span class="sxs-lookup"><span data-stu-id="c3a4d-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="c3a4d-171">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="c3a4d-171">Related resources</span></span>

[<span data-ttu-id="c3a4d-172">Komme i gang med avgiftstjenesten</span><span class="sxs-lookup"><span data-stu-id="c3a4d-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="c3a4d-173">Flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="c3a4d-174">Støtte for avgiftsfunksjon for overføringsordre</span><span class="sxs-lookup"><span data-stu-id="c3a4d-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="c3a4d-175">Slik bygger du utvidelse i avgiftstjeneste</span><span class="sxs-lookup"><span data-stu-id="c3a4d-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
