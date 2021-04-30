---
title: Forsendelse av småpakker
description: Dette emnet inneholder informasjon om funksjonen for forsendelse av småpakker. Denne funksjonen gjør at Microsoft Dynamics 365 Supply Chain Management kan sende informasjon om en pakket container til transportøren, og deretter motta en forsendelsesetikett, en forsendelsessats og et sporingsnummer tilbake fra denne transportøren.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910215"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="f70de-104">Forsendelse av småpakker</span><span class="sxs-lookup"><span data-stu-id="f70de-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f70de-105">Med funksjonen for forsendelse av småpakker kan Microsoft Dynamics 365 Supply Chain Management kommunisere direkte med transportører ved å sørge for et rammeverk for kommunikasjon via transportør-API-er.</span><span class="sxs-lookup"><span data-stu-id="f70de-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="f70de-106">Denne funksjonaliteten er nyttig når du sender individuelle salgsordrer via kommersielle transportører i stedet for å bruke containerforsendelse eller LTL-forsendelse (Less-than-truckload).</span><span class="sxs-lookup"><span data-stu-id="f70de-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="f70de-107">Funksjonen for forsendelse av småpakker kommuniserer med transportøren via en egen *ratemotor*.</span><span class="sxs-lookup"><span data-stu-id="f70de-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="f70de-108">Organisasjonen må utvikle denne ratemotoren i samarbeid med transportørtjenesten.</span><span class="sxs-lookup"><span data-stu-id="f70de-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="f70de-109">Ratemotoren gjør at Supply Chain Management kan sende informasjon om en pakket container til transportøren, og deretter motta en forsendelsesetikett, en forsendelsessats og et sporingsnummer tilbake fra denne transportøren.</span><span class="sxs-lookup"><span data-stu-id="f70de-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="f70de-110">Forsendelsessatsen som returneres, legges til i den tilknyttede salgsordren som et tillegg.</span><span class="sxs-lookup"><span data-stu-id="f70de-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="f70de-111">Forsendelsesetiketten som returneres, kan deretter skrives ut automatisk ved hjelp av en ZPL-skriver (Zebra Programming Language) og brukes på forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="f70de-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="f70de-112">Transportøren skanner denne forsendelsesetiketten når vedkommende henter pakkene på lageret.</span><span class="sxs-lookup"><span data-stu-id="f70de-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="f70de-113">Klargjøre systemet slik at det støtter forsendelse av småpakker</span><span class="sxs-lookup"><span data-stu-id="f70de-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="f70de-114">Før du kan begynne å bruke funksjonen for forsendelse av småpakker, må du aktivere den i Funksjonsbehandling, legge til ratemotoren og definere modulene **Transportstyring** og **Lagerstyring** for å støtte den.</span><span class="sxs-lookup"><span data-stu-id="f70de-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="f70de-115">Aktivere funksjonen for forsendelse av småpakker</span><span class="sxs-lookup"><span data-stu-id="f70de-115">Turn on the SPS feature</span></span>

<span data-ttu-id="f70de-116">Før du kan bruke funksjonen for forsendelse av småpakker, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="f70de-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="f70de-117">Administratorer kan bruke arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere statusen for funksjonen og aktivere den om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="f70de-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f70de-118">Funksjonen vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="f70de-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f70de-119">**Modul:** *Transportstyring*</span><span class="sxs-lookup"><span data-stu-id="f70de-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="f70de-120">**Funksjonsnavn:** *Forsendelse av småpakker*</span><span class="sxs-lookup"><span data-stu-id="f70de-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="f70de-121">Distribuere og definere ratemotorer</span><span class="sxs-lookup"><span data-stu-id="f70de-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="f70de-122">Supply Chain Management inneholder ingen ratemotorer.</span><span class="sxs-lookup"><span data-stu-id="f70de-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="f70de-123">Du må skaffe eller opprette alle ratemotorer du trenger, og deretter legge dem til i systemet.</span><span class="sxs-lookup"><span data-stu-id="f70de-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="f70de-124">Microsoft tilbyr imidlertid en demoratemotor du kan bruke til testing.</span><span class="sxs-lookup"><span data-stu-id="f70de-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="f70de-125">Laste ned og distribuere demoratemotoren</span><span class="sxs-lookup"><span data-stu-id="f70de-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="f70de-126">Følg denne fremgangsmåten for å hente demoratemotoren.</span><span class="sxs-lookup"><span data-stu-id="f70de-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="f70de-127">Last ned [biblioteket for dynamiske koblinger (DLL) for demoratemotoren](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) på GitHub.</span><span class="sxs-lookup"><span data-stu-id="f70de-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="f70de-128">På Supply Chain Management-serveren lagrer du DLL-filen i mappen **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="f70de-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="f70de-129">Opprette og distribuere praktiske ratemotorer</span><span class="sxs-lookup"><span data-stu-id="f70de-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="f70de-130">Hvis du vil ha informasjon om hvordan du oppretter og distribuerer praktiske ratemotorer slik at de kan brukes i et produksjons- eller testmiljø, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="f70de-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="f70de-131">Opprette en ny transportstyringsmotor</span><span class="sxs-lookup"><span data-stu-id="f70de-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="f70de-132">Definere transportbehandlingsmotorer</span><span class="sxs-lookup"><span data-stu-id="f70de-132">Set up transportation management engines</span></span>](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="f70de-133">Hvis du vil ha mer informasjon om hvordan du oppretter en ratemotor for forsendelse av småpakker, kan du se følgende blogginnlegg: [Forsendelse av småpakker: utnytte funksjonen for forsendelse av småpakker i Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="f70de-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="f70de-134">Definere en ratemotor i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="f70de-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="f70de-135">Etter at du har opprettet og distribuert en ratemotor for forsendelse av småpakker, følger du fremgangsmåten nedenfor for å definere den.</span><span class="sxs-lookup"><span data-stu-id="f70de-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="f70de-136">Gå til **Transportstyring \> Oppsett \> Motorer \> Ratemotor**.</span><span class="sxs-lookup"><span data-stu-id="f70de-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="f70de-137">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="f70de-138">I den nye raden angir du følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f70de-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="f70de-139">**Ratemotor** – Angi et unikt navn for ratemotoren.</span><span class="sxs-lookup"><span data-stu-id="f70de-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="f70de-140">Hvis du bruker demoratemotoren, angir du *Demoratemotor*.</span><span class="sxs-lookup"><span data-stu-id="f70de-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="f70de-141">**Navn** – Angi en kort beskrivelse av ratemotoren.</span><span class="sxs-lookup"><span data-stu-id="f70de-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="f70de-142">Hvis du bruker demoratemotoren, angir du *Demoratemotor*.</span><span class="sxs-lookup"><span data-stu-id="f70de-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="f70de-143">**ID for metadata for vurdering** – Velg grunnlaget som skal brukes til å beregne satsen.</span><span class="sxs-lookup"><span data-stu-id="f70de-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="f70de-144">Satsen kan for eksempel beregnes basert på avstand.</span><span class="sxs-lookup"><span data-stu-id="f70de-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="f70de-145">Hvis du bruker demoratemotoren, kan du la dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="f70de-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="f70de-146">**Motormontering** – Angi filnavnet på DLL-pakken du distribuerte.</span><span class="sxs-lookup"><span data-stu-id="f70de-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="f70de-147">Hvis du bruker demoratemotoren, angir du *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="f70de-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="f70de-148">**Motorklasse** – Angi klassenavnet som ble opprettet for ratemotoren.</span><span class="sxs-lookup"><span data-stu-id="f70de-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="f70de-149">Hvis du bruker demoratemotoren, angir du *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="f70de-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f70de-150">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="f70de-150">Example scenario</span></span>

<span data-ttu-id="f70de-151">Dette eksempelscenarioet viser hvordan du definerer og bruker forsendelse av småpakker etter at du har klargjort systemet som beskrevet tidligere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="f70de-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="f70de-152">Dette scenarioet bruker den tidligere nevnte demoratemotoren.</span><span class="sxs-lookup"><span data-stu-id="f70de-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f70de-153">Gjøre demodata tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="f70de-153">Make demo data available</span></span>

<span data-ttu-id="f70de-154">For å kunne arbeide deg gjennom dette scenariet ved å bruke de angitte demopostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert.</span><span class="sxs-lookup"><span data-stu-id="f70de-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="f70de-155">Du må også velge den juridiske enheten **USMF** før du begynner.</span><span class="sxs-lookup"><span data-stu-id="f70de-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="f70de-156">Definer scenariet</span><span class="sxs-lookup"><span data-stu-id="f70de-156">Set up the scenario</span></span>

<span data-ttu-id="f70de-157">I dette eksempelscenarioet må du ha en demotransportør, transportørgruppe, pakkepolicy og pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="f70de-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="f70de-158">De følgende underdelene forklarer hvordan du klargjør postene som kreves for scenarioet.</span><span class="sxs-lookup"><span data-stu-id="f70de-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="f70de-159">I et produksjonsscenario ligner fremgangsmåten for konfigurasjon vanligvis på fremgangsmåten som er beskrevet her.</span><span class="sxs-lookup"><span data-stu-id="f70de-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="f70de-160">Du angir imidlertid andre verdier.</span><span class="sxs-lookup"><span data-stu-id="f70de-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="f70de-161">Definere transportører</span><span class="sxs-lookup"><span data-stu-id="f70de-161">Set up carriers</span></span>

<span data-ttu-id="f70de-162">Følg denne fremgangsmåten for å definere en transportør.</span><span class="sxs-lookup"><span data-stu-id="f70de-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="f70de-163">Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.</span><span class="sxs-lookup"><span data-stu-id="f70de-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="f70de-164">I handlingsruten velger du **Ny** for legge til en transportør.</span><span class="sxs-lookup"><span data-stu-id="f70de-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="f70de-165">I hodet angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f70de-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="f70de-166">**Transportør:** *Demotransportør*</span><span class="sxs-lookup"><span data-stu-id="f70de-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="f70de-167">**Navn:** *Demotransportør*</span><span class="sxs-lookup"><span data-stu-id="f70de-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="f70de-168">**Modus:** *Landtransport*</span><span class="sxs-lookup"><span data-stu-id="f70de-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="f70de-169">Angi følgende verdier i **Oversikt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="f70de-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f70de-170">**Aktiver transportør:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="f70de-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="f70de-171">**Aktiver transportørrangering:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="f70de-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="f70de-172">I hurtigfanen **Tjenester** velger du **Ny** for å legge til en tjeneste i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="f70de-173">Angi følgende verdier for den nye tjenesten:</span><span class="sxs-lookup"><span data-stu-id="f70de-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="f70de-174">**Transportørtjeneste:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="f70de-175">**Navn:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="f70de-176">**Transportmetode:** *Landtransport*</span><span class="sxs-lookup"><span data-stu-id="f70de-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="f70de-177">Angi vilkårlige verdier i alle de andre feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f70de-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="f70de-178">(Når du lagrer den nye transportørposten, opprettes det en ny leveringsmåte, og **Leveringsmåte**-feltet angis automatisk.)</span><span class="sxs-lookup"><span data-stu-id="f70de-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="f70de-179">Velg **Ny** i hurtigfanen **Vurderingsprofiler** for å legge til en vurderingsprofil i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="f70de-180">Angi følgende verdier for den nye profilen:</span><span class="sxs-lookup"><span data-stu-id="f70de-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="f70de-181">**Vurderingsprofil:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="f70de-182">**Navn:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="f70de-183">**Ratemotor:** *Demoratemotor*</span><span class="sxs-lookup"><span data-stu-id="f70de-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="f70de-184">Angi vilkårlige verdier i alle de andre feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="f70de-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="f70de-185">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="f70de-186">Hvis du vil ha mer informasjon om hvordan du definerer transportører, kan du se [Definere transportører](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="f70de-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="f70de-187">Definere transportørtjenestekontoer</span><span class="sxs-lookup"><span data-stu-id="f70de-187">Set up carrier service accounts</span></span>

<span data-ttu-id="f70de-188">Følg denne fremgangsmåten for å definere en transportørtjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="f70de-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="f70de-189">Gå til **Transportstyring \> Oppsett \> Vurdering \> Transportørtjenestekonto**.</span><span class="sxs-lookup"><span data-stu-id="f70de-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="f70de-190">I handlingsruten velger du **Ny** for å legge til en transportørtjenestekonto.</span><span class="sxs-lookup"><span data-stu-id="f70de-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="f70de-191">Angi følgende verdier for den nye kontoen:</span><span class="sxs-lookup"><span data-stu-id="f70de-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="f70de-192">**Transportør:** *Demotransportør*</span><span class="sxs-lookup"><span data-stu-id="f70de-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="f70de-193">**Transportørtjeneste:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="f70de-194">**Kundekontonummer for transportør:** Kundekontonummeret for transportøren som brukes til å bekrefte og autentisere tilkoblingen til transportøren.</span><span class="sxs-lookup"><span data-stu-id="f70de-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="f70de-195">Transportøren sørger for denne verdien.</span><span class="sxs-lookup"><span data-stu-id="f70de-195">Your carrier will provide this value.</span></span> <span data-ttu-id="f70de-196">Hvis du bruker demotjenesten, kan du angi en vilkårlig verdi.</span><span class="sxs-lookup"><span data-stu-id="f70de-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="f70de-197">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="f70de-197">**Site:** *6*</span></span>
    - <span data-ttu-id="f70de-198">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="f70de-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="f70de-199">Verdien for **Kundekontonummer for transportør** er ofte den eneste verdien som kreves for å autentisere tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="f70de-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="f70de-200">Hvis transportøren imidlertid krever flere autentiseringsparametere, bør organisasjonen tilpasse denne siden for å legge til ekstra felter etter behov.</span><span class="sxs-lookup"><span data-stu-id="f70de-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="f70de-201">Definere en policy for containerpakking</span><span class="sxs-lookup"><span data-stu-id="f70de-201">Set up a container packing policy</span></span>

<span data-ttu-id="f70de-202">Følg denne fremgangsmåten for å definere en policy for containerpakking.</span><span class="sxs-lookup"><span data-stu-id="f70de-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="f70de-203">Hvis du ikke allerede har konfigurert en ZPL-skriverdefinisjon, bruker du programmet Dokumentrutingsagent til å konfigurere den.</span><span class="sxs-lookup"><span data-stu-id="f70de-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="f70de-204">Hvis du vil ha mer informasjon, kan du se [Oversikt over utskrift av dokument](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og beslektede emner.</span><span class="sxs-lookup"><span data-stu-id="f70de-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="f70de-205">Gå til **Lagerstyring \> Oppsett \> Containere \> Policyer for containerpakking**.</span><span class="sxs-lookup"><span data-stu-id="f70de-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="f70de-206">I handlingsruten velger du **Ny** for å legge til en policy for containerpakking.</span><span class="sxs-lookup"><span data-stu-id="f70de-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="f70de-207">I toppteksten i den nye policyen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f70de-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="f70de-208">**Policy for containerpakke:** *Demopakkepolicy*</span><span class="sxs-lookup"><span data-stu-id="f70de-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="f70de-209">**Beskrivelse:** en beskrivelse av policyen</span><span class="sxs-lookup"><span data-stu-id="f70de-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="f70de-210">Angi følgende verdier i **Oversikt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="f70de-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f70de-211">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="f70de-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="f70de-212">**Standardlokasjon for endelig forsendelse:** *Rampedør*</span><span class="sxs-lookup"><span data-stu-id="f70de-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="f70de-213">**Vektenhet:** *kg*</span><span class="sxs-lookup"><span data-stu-id="f70de-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="f70de-214">**Policy for containerlukking:** *Automatisk frigivelse*</span><span class="sxs-lookup"><span data-stu-id="f70de-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="f70de-215">**Policy for containerfrigivelse:** *Gjør tilgjengelig på endelig leveringslokasjon*</span><span class="sxs-lookup"><span data-stu-id="f70de-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="f70de-216">I hurtigfanen **Containermanifest** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f70de-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f70de-217">**Automatisk manifest ved containerlukking:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="f70de-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="f70de-218">**Manifestkrav for container:** *Transportstyring*</span><span class="sxs-lookup"><span data-stu-id="f70de-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="f70de-219">**Skriv ut containerinnhold:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="f70de-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="f70de-220">I hurtigfanen **Utskrift av transportøretikett** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f70de-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f70de-221">**Skriv ut containerforsendelsesetikett:** *Alltid*</span><span class="sxs-lookup"><span data-stu-id="f70de-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="f70de-222">**Skrivernavn:** Navnet på ZPL-skriveren som skal skrive ut forsendelsesetiketter</span><span class="sxs-lookup"><span data-stu-id="f70de-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="f70de-223">Definere en pakkeprofil</span><span class="sxs-lookup"><span data-stu-id="f70de-223">Set up a packing profile</span></span>

<span data-ttu-id="f70de-224">Følg denne fremgangsmåten for å definere en pakkeprofil.</span><span class="sxs-lookup"><span data-stu-id="f70de-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="f70de-225">Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="f70de-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="f70de-226">I handlingsruten velger du **Ny** for å legge til en pakkeprofil i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="f70de-227">Angi følgende verdier for den nye profilen:</span><span class="sxs-lookup"><span data-stu-id="f70de-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="f70de-228">**Pakkeprofil-ID:** *Demopakkeprofil*</span><span class="sxs-lookup"><span data-stu-id="f70de-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="f70de-229">**Beskrivelse:** en beskrivelse av profilen</span><span class="sxs-lookup"><span data-stu-id="f70de-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="f70de-230">**Policy for containerpakke:** *Demopakkepolicy*</span><span class="sxs-lookup"><span data-stu-id="f70de-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="f70de-231">**Modus for container-ID:** *Automatisk*</span><span class="sxs-lookup"><span data-stu-id="f70de-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="f70de-232">**Containertype:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="f70de-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="f70de-233">Definere en kunde som kan bruke transportøren for forsendelse av småpakker</span><span class="sxs-lookup"><span data-stu-id="f70de-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="f70de-234">Følg denne fremgangsmåten for å definere en kunde, slik at vedkommende kan bruke transportøren du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="f70de-235">Gå til **Kunder \> kunder \> Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="f70de-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="f70de-236">Finn og velg kunden *US-027* i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="f70de-237">Gå til handlingsruten, **Generelt**-fanen, **Oppsett**-gruppen, og velg **Kundekontoer for transportør**.</span><span class="sxs-lookup"><span data-stu-id="f70de-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="f70de-238">Velg **Ny** i handlingsruten på siden **Kundekontoer for transportør** for å legge til en konto i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="f70de-239">Angi følgende verdier for den nye kontoen:</span><span class="sxs-lookup"><span data-stu-id="f70de-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="f70de-240">**Transportør:** *Demotransportør*</span><span class="sxs-lookup"><span data-stu-id="f70de-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="f70de-241">**Kundekontonummer for transportør:** *12345* (Verdien er ikke viktig i dette scenarioet, men vi henviser til den i neste del.)</span><span class="sxs-lookup"><span data-stu-id="f70de-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="f70de-242">Gå gjennom eksempelscenarioet</span><span class="sxs-lookup"><span data-stu-id="f70de-242">Go through the example scenario</span></span>

<span data-ttu-id="f70de-243">Når du har definert alle eksempeldataene som beskrevet i forrige del, er du klar til å gå gjennom eksempelscenarioet.</span><span class="sxs-lookup"><span data-stu-id="f70de-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="f70de-244">Opprette en salgsordre og behandle arbeidet</span><span class="sxs-lookup"><span data-stu-id="f70de-244">Create a sales order and process the work</span></span>

<span data-ttu-id="f70de-245">Følg denne fremgangsmåten for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f70de-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="f70de-246">Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="f70de-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f70de-247">Velg **Ny** for å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="f70de-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="f70de-248">I dialogboksen **Opprett salgsordre** angir du *US-027* i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f70de-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="f70de-249">Velg **OK** for å opprette salgsorden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f70de-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="f70de-250">Den nye salgsordren åpnes.</span><span class="sxs-lookup"><span data-stu-id="f70de-250">The new sales order is opened.</span></span> <span data-ttu-id="f70de-251">I hurtigfanen **Salgsordrehode** angir du verdien du valgte for denne kunden tidligere (*12345*), i feltet **Kundekontonummer for transportør**.</span><span class="sxs-lookup"><span data-stu-id="f70de-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="f70de-252">Legg til en salgslinje i delen **Salgsordrelinjer**, og angi følgende verdier for den:</span><span class="sxs-lookup"><span data-stu-id="f70de-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="f70de-253">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f70de-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f70de-254">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="f70de-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="f70de-255">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="f70de-255">**Site:** *6*</span></span>
    - <span data-ttu-id="f70de-256">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="f70de-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f70de-257">Bytt til **Topptekst**-visningen.</span><span class="sxs-lookup"><span data-stu-id="f70de-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="f70de-258">Angi følgende verdier i hurtigfanen **Levering**:</span><span class="sxs-lookup"><span data-stu-id="f70de-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="f70de-259">**Transportør:** *Demotransportør*</span><span class="sxs-lookup"><span data-stu-id="f70de-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="f70de-260">**Transportørtjeneste:** *Demotransportørtjeneste*</span><span class="sxs-lookup"><span data-stu-id="f70de-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="f70de-261">Gå tilbake til **Linjer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="f70de-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="f70de-262">Hvis du blir bedt om å oppdatere leveringsmåten for salgslinjene, velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f70de-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="f70de-263">Velg ordrelinjen du definerte tidligere, i delen **Salgsordrelinjer**, og velg deretter **Lager \> Reservasjon**.</span><span class="sxs-lookup"><span data-stu-id="f70de-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="f70de-264">På **Reservasjon**-siden velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.</span><span class="sxs-lookup"><span data-stu-id="f70de-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="f70de-265">Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f70de-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="f70de-266">Velg **Frigi til lager** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f70de-267">Det opprettes arbeid for å flytte varer fra plukklokasjonen til pakkestasjonen.</span><span class="sxs-lookup"><span data-stu-id="f70de-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="f70de-268">I delen **Salgsordrelinje** velger du **Lager \> Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="f70de-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="f70de-269">Noter deg forsendelses-ID-en på siden **Forsendelsesdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="f70de-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="f70de-270">Du trenger denne når du pakker forsendelsen ved pakkestasjonen.</span><span class="sxs-lookup"><span data-stu-id="f70de-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="f70de-271">Lukk siden **Forsendelsesdetaljer** for å gå tilbake til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="f70de-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="f70de-272">Noter deg salgsordrenummeret, og gå deretter til **Lagerstyring \> Arbeid \> Alt arbeid**.</span><span class="sxs-lookup"><span data-stu-id="f70de-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="f70de-273">Bruk salgsordrenummeret til å finne og velge arbeidet som ble opprettet for ordren.</span><span class="sxs-lookup"><span data-stu-id="f70de-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="f70de-274">Velg **Fullfør arbeid** i **Arbeid**-fanen i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="f70de-275">Velg en bruker-ID i **Bruker-ID**-feltet på siden **Arbeidsfullføring**.</span><span class="sxs-lookup"><span data-stu-id="f70de-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="f70de-276">Velg deretter **Valider arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="f70de-277">Hvis arbeidet består valideringen, velger du **Fullfør arbeid** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="f70de-278">Arbeidet merkes som fullført for å simulere flyttingen av varer til pakkestasjonen.</span><span class="sxs-lookup"><span data-stu-id="f70de-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="f70de-279">Pakke forsendelsen</span><span class="sxs-lookup"><span data-stu-id="f70de-279">Pack the shipment</span></span>

<span data-ttu-id="f70de-280">Følg denne fremgangsmåten for å pakke forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="f70de-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="f70de-281">Gå til **Lagerstyring \> Oppsett \> Arbeider**, og kontroller at brukerkontoen din er knyttet til en arbeiderkonto for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="f70de-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="f70de-282">Gå til **Lagerstyring \> Plukking og containerbruk \> Pakke**.</span><span class="sxs-lookup"><span data-stu-id="f70de-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="f70de-283">I dialogboksen **Velg pakkstasjon** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="f70de-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f70de-284">**Område:** *6*</span><span class="sxs-lookup"><span data-stu-id="f70de-284">**Site:** *6*</span></span>
    - <span data-ttu-id="f70de-285">**Lager:** *62*</span><span class="sxs-lookup"><span data-stu-id="f70de-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="f70de-286">**Plassering:** *Pakke*</span><span class="sxs-lookup"><span data-stu-id="f70de-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="f70de-287">**Pakkeprofil-ID:** *Demopakkeprofil*</span><span class="sxs-lookup"><span data-stu-id="f70de-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="f70de-288">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f70de-288">Select **OK**.</span></span>
1. <span data-ttu-id="f70de-289">**Pakke**-siden vises.</span><span class="sxs-lookup"><span data-stu-id="f70de-289">The **Pack** page appears.</span></span> <span data-ttu-id="f70de-290">I et produksjonsscenario skanner en arbeider et nummerskilt eller en forsendelses-ID.</span><span class="sxs-lookup"><span data-stu-id="f70de-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="f70de-291">I dette scenariet åpner du i stedet siden **Alle forsendelser** og slår opp forsendelsesnummeret for forsendelsen du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="f70de-292">Deretter angir du denne verdien i feltet **Nummerskilt eller forsendelse** på **Pakke**-siden.</span><span class="sxs-lookup"><span data-stu-id="f70de-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="f70de-293">Du kan også angi forsendelses-ID-en du noterte tidligere.</span><span class="sxs-lookup"><span data-stu-id="f70de-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="f70de-294">I handlingsruten velger du **Ny container**.</span><span class="sxs-lookup"><span data-stu-id="f70de-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="f70de-295">Dialogboksen som vises, inneholder detaljer om den nye containeren.</span><span class="sxs-lookup"><span data-stu-id="f70de-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="f70de-296">La standardverdiene stå, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f70de-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="f70de-297">Gå til **Pakke**-siden og deretter hurtigfanen **Varepakking**, og velg *A0002* i **Identifikator**-feltet for å pakke denne varen.</span><span class="sxs-lookup"><span data-stu-id="f70de-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="f70de-298">Varen legges til i containeren.</span><span class="sxs-lookup"><span data-stu-id="f70de-298">The item is added to the container.</span></span>
1. <span data-ttu-id="f70de-299">Velg **Containere til forsendelse** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f70de-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="f70de-300">Siden **Containere til forsendelse** som vises, har en rad for containeren du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="f70de-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="f70de-301">Feltet **ID for containermanifest** i denne raden er imidlertid tomt fordi du ennå ikke har mottatt forsendelsesetiketten og sporingsnummeret fra transportøren.</span><span class="sxs-lookup"><span data-stu-id="f70de-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="f70de-302">I handlingsruten velger du **Lukk container**.</span><span class="sxs-lookup"><span data-stu-id="f70de-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="f70de-303">I dialogboksen **Lukk container** angir du *1 kg* i **Bruttovekt**-feltet og velger deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f70de-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="f70de-304">Forsendelsesetiketten skal nå skrives ut på ZPL-skriveren du valgte tidligere.</span><span class="sxs-lookup"><span data-stu-id="f70de-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="f70de-305">Den skal ligne følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="f70de-305">It should resemble the following example.</span></span>

    <span data-ttu-id="f70de-306">![Eksempel på forsendelsesetikett](media/sps-label-example.png "Eksempel på forsendelsesetikett")</span><span class="sxs-lookup"><span data-stu-id="f70de-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="f70de-307">Legg merke til at verdiene for **ID for containermanifest** og **Total frakt** er lagt til som mottatt fra transportøren.</span><span class="sxs-lookup"><span data-stu-id="f70de-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]