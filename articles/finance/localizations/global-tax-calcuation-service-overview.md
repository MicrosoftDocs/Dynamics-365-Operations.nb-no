---
title: Avgiftsberegning (forhåndsversjon)
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegning.
author: wangchen
ms.date: 04/12/2021
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
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892355"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="008e0-103">Avgiftsberegning (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="008e0-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="008e0-104">Avgiftsberegning er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter.</span><span class="sxs-lookup"><span data-stu-id="008e0-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="008e0-105">Avgiftsmotoren er fullt konfigurerbar.</span><span class="sxs-lookup"><span data-stu-id="008e0-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="008e0-106">Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel.</span><span class="sxs-lookup"><span data-stu-id="008e0-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="008e0-107">Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="008e0-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="008e0-108">Avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="008e0-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="008e0-109">Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="008e0-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="008e0-110">Avgiftsberegning er en Microsoft-basert avgiftsmotor på mikrotjenestenivå som tilbyr eksponenentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="008e0-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="008e0-111">Den kan hjelpe dem med å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="008e0-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="008e0-112">Konfigurer avgiftsberegning via RCS (Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="008e0-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="008e0-113">RCS er en utvidet versjon av ER-designeren (elektronisk rapportering) og er tilgjengelig som en frittstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="008e0-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="008e0-114">Konfigurer avgiftsmatrisen slik at avgiftskoder og -satser bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="008e0-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="008e0-115">Konfigurer avgiftsmatrisen slik at avgiftsregistreringsnummeret bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="008e0-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="008e0-116">Konfigurer avgiftsberegningsdesigneren for å definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="008e0-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="008e0-117">Del løsningen for avgiftsfastsettelse og -beregning på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="008e0-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="008e0-118">Hvis du vil bruke tjenesten for avgiftsberegning, installerer du tillegget for avgiftsberegningstjenesten fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="008e0-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="008e0-119">Deretter fullfører du oppsettet i RCS og aktiverer avgiftsberegningstjenesten i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="008e0-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="008e0-120">Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="008e0-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="008e0-121">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="008e0-121">Availability</span></span>

<span data-ttu-id="008e0-122">Avgiftsberegning er bare tilgjengelig i sandkassemiljøer og for utvalgte kunder via et program som offentlig forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="008e0-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="008e0-123">Til slutt vil det bli allment tilgjengelig for alle kunder og i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="008e0-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="008e0-124">Nye funksjoner vil bli levert fortløpende, så pass derfor på at du ofte kontrollerer den mest oppdaterte dokumentasjonen for å finne ut om dekningen og omfanget av funksjoner som støttes.</span><span class="sxs-lookup"><span data-stu-id="008e0-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="008e0-125">Avgiftsberegning distribueres i følgende Azure-geografier.</span><span class="sxs-lookup"><span data-stu-id="008e0-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="008e0-126">Det vil også bli distribuert til flere Azure-geografier, basert på kundebehov:</span><span class="sxs-lookup"><span data-stu-id="008e0-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="008e0-127">USA</span><span class="sxs-lookup"><span data-stu-id="008e0-127">United States</span></span>
- <span data-ttu-id="008e0-128">Europa</span><span class="sxs-lookup"><span data-stu-id="008e0-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="008e0-129">Avgiftsberegning støtter ikke lokale distribusjoner av Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="008e0-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="008e0-130">Den støtter heller ikke tidligere versjoner, for eksempel Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="008e0-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="008e0-131">Funksjonsfremhevinger</span><span class="sxs-lookup"><span data-stu-id="008e0-131">Feature highlights</span></span>

- <span data-ttu-id="008e0-132">En konfigurerbare avgiftsmatrise for automatisk bestemming og beregning av avgifter</span><span class="sxs-lookup"><span data-stu-id="008e0-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="008e0-133">Støtte for flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="008e0-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="008e0-134">Overføringsordrestøtte for fastsettelse og beregning av avgift</span><span class="sxs-lookup"><span data-stu-id="008e0-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="008e0-135">Støtte for overføringsordre for fastsettelse av flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="008e0-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="008e0-136">Transaksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="008e0-136">Supported transactions</span></span>

<span data-ttu-id="008e0-137">Avgiftsberegning kan aktiveres ved hjelp av juridisk enhet og transaksjon.</span><span class="sxs-lookup"><span data-stu-id="008e0-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="008e0-138">Følgende transaksjoner støttes:</span><span class="sxs-lookup"><span data-stu-id="008e0-138">The following transactions are supported:</span></span>

- <span data-ttu-id="008e0-139">Salgsprosess</span><span class="sxs-lookup"><span data-stu-id="008e0-139">Sales process</span></span>

    - <span data-ttu-id="008e0-140">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="008e0-140">Sales quotation</span></span>
    - <span data-ttu-id="008e0-141">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="008e0-141">Sales order</span></span>
    - <span data-ttu-id="008e0-142">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="008e0-142">Confirmation</span></span>
    - <span data-ttu-id="008e0-143">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="008e0-143">Picking list</span></span>
    - <span data-ttu-id="008e0-144">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="008e0-144">Packing slip</span></span>
    - <span data-ttu-id="008e0-145">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="008e0-145">Sales invoice</span></span>
    - <span data-ttu-id="008e0-146">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="008e0-146">Credit note</span></span>
    - <span data-ttu-id="008e0-147">Returordre</span><span class="sxs-lookup"><span data-stu-id="008e0-147">Return order</span></span>
    - <span data-ttu-id="008e0-148">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="008e0-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="008e0-149">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="008e0-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="008e0-150">Innkjøpsprosess</span><span class="sxs-lookup"><span data-stu-id="008e0-150">Purchase process</span></span>

    - <span data-ttu-id="008e0-151">Bestilling</span><span class="sxs-lookup"><span data-stu-id="008e0-151">Purchase order</span></span>
    - <span data-ttu-id="008e0-152">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="008e0-152">Confirmation</span></span>
    - <span data-ttu-id="008e0-153">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="008e0-153">Receipts list</span></span>
    - <span data-ttu-id="008e0-154">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="008e0-154">Product receipt</span></span>
    - <span data-ttu-id="008e0-155">Innkjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="008e0-155">Purchase invoice</span></span>
    - <span data-ttu-id="008e0-156">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="008e0-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="008e0-157">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="008e0-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="008e0-158">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="008e0-158">Credit note</span></span>
    - <span data-ttu-id="008e0-159">Returordre</span><span class="sxs-lookup"><span data-stu-id="008e0-159">Return order</span></span>
    - <span data-ttu-id="008e0-160">Innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="008e0-160">Purchase requisition</span></span>
    - <span data-ttu-id="008e0-161">Diverse tillegg på innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="008e0-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="008e0-162">Tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="008e0-162">Request for quotation</span></span>
    - <span data-ttu-id="008e0-163">Diverse tillegg på tilbudsforespørselshode</span><span class="sxs-lookup"><span data-stu-id="008e0-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="008e0-164">Diverse tillegg på tilbudsforespørselslinje</span><span class="sxs-lookup"><span data-stu-id="008e0-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="008e0-165">Beholdningsprosess</span><span class="sxs-lookup"><span data-stu-id="008e0-165">Inventory process</span></span>

    - <span data-ttu-id="008e0-166">Overføringsordre – send</span><span class="sxs-lookup"><span data-stu-id="008e0-166">Transfer order – ship</span></span>
    - <span data-ttu-id="008e0-167">Overføringsordre – motta</span><span class="sxs-lookup"><span data-stu-id="008e0-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="008e0-168">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="008e0-168">Related resources</span></span>

[<span data-ttu-id="008e0-169">Komme i gang med avgiftstjenesten</span><span class="sxs-lookup"><span data-stu-id="008e0-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="008e0-170">Flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="008e0-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="008e0-171">Støtte for avgiftsfunksjon for overføringsordre</span><span class="sxs-lookup"><span data-stu-id="008e0-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="008e0-172">Slik bygger du utvidelse i avgiftstjeneste</span><span class="sxs-lookup"><span data-stu-id="008e0-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)