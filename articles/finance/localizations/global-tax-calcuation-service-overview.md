---
title: Avgiftsberegning (forhåndsversjon)
description: Dette emnet forklarer det helhetlige omfanget og funksjonene i avgiftsberegning.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184107"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="66996-103">Avgiftsberegning (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="66996-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="66996-104">Avgiftsberegning er en hyperskalerbar flerleiertjeneste som gjør det mulig for Global Tax Engine å automatisere og forenkle fastsettelses- og beregningsprosessen for avgifter.</span><span class="sxs-lookup"><span data-stu-id="66996-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="66996-105">Avgiftsmotoren er fullt konfigurerbar.</span><span class="sxs-lookup"><span data-stu-id="66996-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="66996-106">Elementene som kan konfigureres, inkluderer, men er ikke begrenset til avgiftspliktig datamodell, avgiftskode, relevansmatrise og avgiftsberegningsformel.</span><span class="sxs-lookup"><span data-stu-id="66996-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="66996-107">Avgiftsmotoren kjører på Microsoft Azure-kjernetjenesteplattformen og tilbyr teknologi og eksponentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="66996-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="66996-108">Avgiftsberegning er integrert med Dynamics 365 Finance og Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="66996-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="66996-109">Til slutt vil den også integreres med Dynamics 365 Project Operations, Dynamics 365 Commerce og andre førsteparts- og tredjepartsprogrammer.</span><span class="sxs-lookup"><span data-stu-id="66996-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66996-110">Når du aktiverer avgiftsberegningstjenesten, kan det hende at enkelte operasjoner på tilknyttede data utføres i et annet datasenter enn datasenteret som vedlikeholder tjenestedataene.</span><span class="sxs-lookup"><span data-stu-id="66996-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="66996-111">Gå gjennom [Vilkår og betingelser](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) før du aktiverer avgiftsberegningstjenesten.</span><span class="sxs-lookup"><span data-stu-id="66996-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="66996-112">Personvernet er viktig for oss.</span><span class="sxs-lookup"><span data-stu-id="66996-112">Your privacy is important to us.</span></span> <span data-ttu-id="66996-113">Les [personvernerklæringen](https://go.microsoft.com/fwlink/?LinkId=521839) for å finne ut mer.</span><span class="sxs-lookup"><span data-stu-id="66996-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="66996-114">Avgiftsberegning er en Microsoft-basert avgiftsmotor på mikrotjenestenivå som tilbyr eksponenentiell skalerbarhet.</span><span class="sxs-lookup"><span data-stu-id="66996-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="66996-115">Den kan hjelpe dem med å utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="66996-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="66996-116">Konfigurer avgiftsberegning via RCS (Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="66996-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="66996-117">RCS er en utvidet versjon av ER-designeren (elektronisk rapportering) og er tilgjengelig som en frittstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="66996-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="66996-118">Konfigurer avgiftsmatrisen slik at avgiftskoder og -satser bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="66996-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="66996-119">Konfigurer avgiftsmatrisen slik at avgiftsregistreringsnummeret bestemmes automatisk.</span><span class="sxs-lookup"><span data-stu-id="66996-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="66996-120">Konfigurer avgiftsberegningsdesigneren for å definere formler og betingelser.</span><span class="sxs-lookup"><span data-stu-id="66996-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="66996-121">Del løsningen for avgiftsfastsettelse og -beregning på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="66996-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="66996-122">Hvis du vil bruke tjenesten for avgiftsberegning, installerer du tillegget for avgiftsberegningstjenesten fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="66996-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="66996-123">Deretter fullfører du oppsettet i RCS og aktiverer avgiftsberegningstjenesten i Finance og Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="66996-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="66996-124">Hvis du vil ha mer informasjon, kan du se [Komme i gang med avgiftstjenesten](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="66996-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="66996-125">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="66996-125">Availability</span></span>

<span data-ttu-id="66996-126">Avgiftsberegning er bare tilgjengelig i sandkassemiljøer og for utvalgte kunder via et program som offentlig forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="66996-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="66996-127">Til slutt vil det bli allment tilgjengelig for alle kunder og i produksjonsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="66996-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="66996-128">Nye funksjoner vil bli levert fortløpende, så pass derfor på at du ofte kontrollerer den mest oppdaterte dokumentasjonen for å finne ut om dekningen og omfanget av funksjoner som støttes.</span><span class="sxs-lookup"><span data-stu-id="66996-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="66996-129">Avgiftsberegning distribueres i følgende Azure-geografier.</span><span class="sxs-lookup"><span data-stu-id="66996-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="66996-130">Det vil også bli distribuert til flere Azure-geografier, basert på kundebehov:</span><span class="sxs-lookup"><span data-stu-id="66996-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="66996-131">USA</span><span class="sxs-lookup"><span data-stu-id="66996-131">United States</span></span>
- <span data-ttu-id="66996-132">Europa</span><span class="sxs-lookup"><span data-stu-id="66996-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="66996-133">Avgiftsberegning støtter ikke lokale distribusjoner av Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="66996-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="66996-134">Den støtter heller ikke tidligere versjoner, for eksempel Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="66996-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="66996-135">Funksjonsfremhevinger</span><span class="sxs-lookup"><span data-stu-id="66996-135">Feature highlights</span></span>

- <span data-ttu-id="66996-136">En konfigurerbare avgiftsmatrise for automatisk bestemming og beregning av avgifter</span><span class="sxs-lookup"><span data-stu-id="66996-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="66996-137">Støtte for flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="66996-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="66996-138">Overføringsordrestøtte for fastsettelse og beregning av avgift</span><span class="sxs-lookup"><span data-stu-id="66996-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="66996-139">Støtte for overføringsordre for fastsettelse av flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="66996-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="66996-140">Transaksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="66996-140">Supported transactions</span></span>

<span data-ttu-id="66996-141">Avgiftsberegning kan aktiveres ved hjelp av juridisk enhet og transaksjon.</span><span class="sxs-lookup"><span data-stu-id="66996-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="66996-142">Følgende transaksjoner støttes:</span><span class="sxs-lookup"><span data-stu-id="66996-142">The following transactions are supported:</span></span>

- <span data-ttu-id="66996-143">Salgsprosess</span><span class="sxs-lookup"><span data-stu-id="66996-143">Sales process</span></span>

    - <span data-ttu-id="66996-144">Salgstilbud</span><span class="sxs-lookup"><span data-stu-id="66996-144">Sales quotation</span></span>
    - <span data-ttu-id="66996-145">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="66996-145">Sales order</span></span>
    - <span data-ttu-id="66996-146">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="66996-146">Confirmation</span></span>
    - <span data-ttu-id="66996-147">Plukkliste</span><span class="sxs-lookup"><span data-stu-id="66996-147">Picking list</span></span>
    - <span data-ttu-id="66996-148">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="66996-148">Packing slip</span></span>
    - <span data-ttu-id="66996-149">Salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="66996-149">Sales invoice</span></span>
    - <span data-ttu-id="66996-150">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="66996-150">Credit note</span></span>
    - <span data-ttu-id="66996-151">Returordre</span><span class="sxs-lookup"><span data-stu-id="66996-151">Return order</span></span>
    - <span data-ttu-id="66996-152">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="66996-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="66996-153">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="66996-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="66996-154">Innkjøpsprosess</span><span class="sxs-lookup"><span data-stu-id="66996-154">Purchase process</span></span>

    - <span data-ttu-id="66996-155">Bestilling</span><span class="sxs-lookup"><span data-stu-id="66996-155">Purchase order</span></span>
    - <span data-ttu-id="66996-156">Bekreftelse</span><span class="sxs-lookup"><span data-stu-id="66996-156">Confirmation</span></span>
    - <span data-ttu-id="66996-157">Tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="66996-157">Receipts list</span></span>
    - <span data-ttu-id="66996-158">Produktkvittering</span><span class="sxs-lookup"><span data-stu-id="66996-158">Product receipt</span></span>
    - <span data-ttu-id="66996-159">Innkjøpsfaktura</span><span class="sxs-lookup"><span data-stu-id="66996-159">Purchase invoice</span></span>
    - <span data-ttu-id="66996-160">Diverse tillegg for overskrift</span><span class="sxs-lookup"><span data-stu-id="66996-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="66996-161">Diverse linjetillegg</span><span class="sxs-lookup"><span data-stu-id="66996-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="66996-162">Kreditnota</span><span class="sxs-lookup"><span data-stu-id="66996-162">Credit note</span></span>
    - <span data-ttu-id="66996-163">Returordre</span><span class="sxs-lookup"><span data-stu-id="66996-163">Return order</span></span>
    - <span data-ttu-id="66996-164">Innkjøpsrekvisisjon</span><span class="sxs-lookup"><span data-stu-id="66996-164">Purchase requisition</span></span>
    - <span data-ttu-id="66996-165">Diverse tillegg på innkjøpsrekvisisjonslinje</span><span class="sxs-lookup"><span data-stu-id="66996-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="66996-166">Tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="66996-166">Request for quotation</span></span>
    - <span data-ttu-id="66996-167">Diverse tillegg på tilbudsforespørselshode</span><span class="sxs-lookup"><span data-stu-id="66996-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="66996-168">Diverse tillegg på tilbudsforespørselslinje</span><span class="sxs-lookup"><span data-stu-id="66996-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="66996-169">Beholdningsprosess</span><span class="sxs-lookup"><span data-stu-id="66996-169">Inventory process</span></span>

    - <span data-ttu-id="66996-170">Overføringsordre – send</span><span class="sxs-lookup"><span data-stu-id="66996-170">Transfer order – ship</span></span>
    - <span data-ttu-id="66996-171">Overføringsordre – motta</span><span class="sxs-lookup"><span data-stu-id="66996-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="66996-172">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="66996-172">Related resources</span></span>

[<span data-ttu-id="66996-173">Komme i gang med avgiftstjenesten</span><span class="sxs-lookup"><span data-stu-id="66996-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="66996-174">Flere mva-registreringsnumre</span><span class="sxs-lookup"><span data-stu-id="66996-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="66996-175">Støtte for avgiftsfunksjon for overføringsordre</span><span class="sxs-lookup"><span data-stu-id="66996-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="66996-176">Slik bygger du utvidelse i avgiftstjeneste</span><span class="sxs-lookup"><span data-stu-id="66996-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
