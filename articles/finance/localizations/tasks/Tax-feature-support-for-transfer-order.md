---
title: Støtte for avgiftsfunksjon for overføringsordrer
description: Dette emnet forklarer den nye avgiftsfunksjonsstøtten for overføringsordrer ved å bruke avgiftsberegningstjenesten.
author: kailiang
ms.date: 03/10/2021
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
ms.openlocfilehash: 55597e4f0f40677e793b4c182e4b0ced01057751
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832567"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="fd080-103">Støtte for avgiftsfunksjon for overføringsordrer</span><span class="sxs-lookup"><span data-stu-id="fd080-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fd080-104">Dette emnet gir informasjon om beregning av avgift og posteringsintegrering i overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd080-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="fd080-105">Ved hjelp av denne funksjonaliteten kan du definere avgiftsberegning og -postering i overføringsordrer for lageroverføringer.</span><span class="sxs-lookup"><span data-stu-id="fd080-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="fd080-106">I henhold til mva-regler i EU anses lageroverføringer som fellesskapsforsyning og fellesskapsanskaffelse.</span><span class="sxs-lookup"><span data-stu-id="fd080-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="fd080-107">Hvis du vil konfigurere og bruke denne funksjonaliteten, må du gå gjennom tre hovedtrinn:</span><span class="sxs-lookup"><span data-stu-id="fd080-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="fd080-108">**RCS-oppsett:** I Regulatory Configuration Service setter du opp avgiftsfunksjonen, avgiftskoder og relevans for avgiftskoder for å bestemme avgiftskoden i overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd080-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="fd080-109">**Finance-oppsett:** I Microsoft Dynamics 365 Finance aktiverer du funksjonen **Avgift i overføringsordre**, setter opp avgiftstjenesteparametere for beholdningen og setter opp kjerneavgiftsparametere.</span><span class="sxs-lookup"><span data-stu-id="fd080-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="fd080-110">**Beholdningsoppsett:** Definer beholdningskonfigurasjonen for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="fd080-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="fd080-111">Konfigurer RCS for avgifts- og overføringsordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="fd080-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="fd080-112">Følg denne fremgangsmåten for å definere avgiften som er involvert i en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="fd080-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="fd080-113">I eksemplet som vises her, er overføringsordren fra Nederland til Belgia.</span><span class="sxs-lookup"><span data-stu-id="fd080-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="fd080-114">På siden **Avgiftsfunksjoner**, på **Versjoner**-fanen velger du utkastfunksjonsversjonen, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="fd080-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Valg av Rediger](../media/image1.png)

2. <span data-ttu-id="fd080-116">På siden **Oppsett av avgiftsfunksjoner**, på fanen **Avgiftskoder**, velger du **Legg til** for å opprette nye avgiftskoder.</span><span class="sxs-lookup"><span data-stu-id="fd080-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="fd080-117">For dette eksemplet opprettes det tre avgiftskoder: **NL-Exempt**, **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fd080-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="fd080-118">Når en overføringsordre sendes fra et lager i Nederland, brukes koden for mva-fritak i Nederland (**NL-Exempt**).</span><span class="sxs-lookup"><span data-stu-id="fd080-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="fd080-119">Opprett mva-koden **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="fd080-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="fd080-120">Velg **Legg til**, angi **NL-Exempt** i feltet **Mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="fd080-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fd080-121">Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.</span><span class="sxs-lookup"><span data-stu-id="fd080-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fd080-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-122">Select **Save**.</span></span>
        4. <span data-ttu-id="fd080-123">Velg **Legg til** i **Sats**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fd080-124">Bytt **Er Fritak** til **Ja** i **Generelt**-delen.</span><span class="sxs-lookup"><span data-stu-id="fd080-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![Avgiftskoden NL-Exempt](../media/image2.png)

    - <span data-ttu-id="fd080-126">Når en overføringsordre mottas ved et lager i Belgia, brukes mekanismen for snudd avregning ved hjelp av avgiftskodene **BE-RC-21** og **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fd080-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="fd080-127">Opprett avgiftskoden **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="fd080-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="fd080-128">Velg **Legg til**, angi **BE-RC-21** i feltet **Mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="fd080-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fd080-129">Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.</span><span class="sxs-lookup"><span data-stu-id="fd080-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fd080-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-130">Select **Save**.</span></span>
        4. <span data-ttu-id="fd080-131">Velg **Legg til** i **Sats**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fd080-132">Angi **-21** i **Avgiftssats**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd080-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="fd080-133">Bytt **Er Snudd avregning** til **Ja** i **Generelt**-delen.</span><span class="sxs-lookup"><span data-stu-id="fd080-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="fd080-134">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-134">Select **Save**.</span></span>

        ![BE-RC-21-avgiftskoden for snudd avregning](../media/image3.png)
        
        <span data-ttu-id="fd080-136">Opprett avgiftskoden **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="fd080-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="fd080-137">Velg **Legg til**, angi **BE-RC-21** i feltet **Mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="fd080-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="fd080-138">Velg **Etter nettobeløp** i feltet **Avgiftskomponent**.</span><span class="sxs-lookup"><span data-stu-id="fd080-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="fd080-139">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-139">Select **Save**.</span></span>
        4. <span data-ttu-id="fd080-140">Velg **Legg til** i **Sats**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="fd080-141">Angi **21** i **Avgiftssats**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd080-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="fd080-142">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-142">Select **Save**.</span></span>

        ![BE-RC+21-avgiftskoden for snudd avregning](../media/image4.png)

3. <span data-ttu-id="fd080-144">Definer relevansen for avgiftskodene.</span><span class="sxs-lookup"><span data-stu-id="fd080-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="fd080-145">Velg **Administrer kolonner**, og velg deretter kolonner som skal brukes til å bygge opp relevanstabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fd080-146">Legg til kolonnene **Forretningsprosess** og **Avgiftsretninger** i tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="fd080-147">Begge kolonnene er vesentlige for funksjonaliteten for avgift i overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd080-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="fd080-148">Legg til relevansregler.</span><span class="sxs-lookup"><span data-stu-id="fd080-148">Add applicability rules.</span></span> <span data-ttu-id="fd080-149">Ikke la feltene **Avgiftskoder**, **Avgiftsgruppe** og **Vareavgiftsgruppe** være tomme.</span><span class="sxs-lookup"><span data-stu-id="fd080-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="fd080-150">Legg til en ny regel for forsendelse av overføringsordren.</span><span class="sxs-lookup"><span data-stu-id="fd080-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="fd080-151">Velg **Legg til** i **Relevansregler**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="fd080-152">I feltet **Forretningsprosess** velger du **Beholdning** for å gjøre regelen aktuall for en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="fd080-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="fd080-153">I feltet **Send fra land/område** angir du **NLD**.</span><span class="sxs-lookup"><span data-stu-id="fd080-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="fd080-154">I feltet **Send til land/område** angir du **BEL**.</span><span class="sxs-lookup"><span data-stu-id="fd080-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="fd080-155">I feltet **Avgiftsretning** velger du **Utgang** for å gjøre regelen aktuell for overføringsordreforsendelsen.</span><span class="sxs-lookup"><span data-stu-id="fd080-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="fd080-156">I **Avgiftskoder**-feltet velger du **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="fd080-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="fd080-157">I **Avgiftsgruppe**-feltet og i **Vareavgiftsgruppe** angir du den relatert mva-gruppen og vareavgiftsgruppen som er definert i Finance-systemet ditt.</span><span class="sxs-lookup"><span data-stu-id="fd080-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="fd080-158">Legg til en annen regel for mottak av overføringsordren.</span><span class="sxs-lookup"><span data-stu-id="fd080-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="fd080-159">Velg **Legg til** i **Relevansregler**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fd080-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="fd080-160">I feltet **Forretningsprosess** velger du **Beholdning** for å gjøre regelen aktuall for en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="fd080-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="fd080-161">I feltet **Send fra land/område** angir du **NLD**.</span><span class="sxs-lookup"><span data-stu-id="fd080-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="fd080-162">I feltet **Send til land/område** angir du **BEL**.</span><span class="sxs-lookup"><span data-stu-id="fd080-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="fd080-163">I feltet **Avgiftsretning** velger du **Innkommende** for å gjøre regelen aktuell for overføringsordremottaket.</span><span class="sxs-lookup"><span data-stu-id="fd080-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="fd080-164">I **Avgiftskoder**-feltet velger du **BE-RC+21** og **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="fd080-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="fd080-165">I **Avgiftsgruppe**-feltet og i **Vareavgiftsgruppe** angir du den relatert mva-gruppen og vareavgiftsgruppen som er definert i Finance-systemet ditt.</span><span class="sxs-lookup"><span data-stu-id="fd080-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Relevansregler](../media/image5.png)

4. <span data-ttu-id="fd080-167">Fullfør og publiser den nye avgiftsfunksjonsversjonen.</span><span class="sxs-lookup"><span data-stu-id="fd080-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="fd080-168">[![Endring av statusen for den nye versjonen](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="fd080-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="fd080-169">Konfigurer Finance for avgiftsordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="fd080-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="fd080-170">Følg disse trinnene for å aktivere og konfigurere avgifter for overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd080-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="fd080-171">I Finance går du til **Arbeidsområder** \> **Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="fd080-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="fd080-172">I listen finner du og velger funksjonen **Avgift i overføringsordre**, og deretter velger du **Aktiver nå** for å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="fd080-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fd080-173">Funksjonen **Avgift i overføringsordre** er fullstendig avhengig av avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="fd080-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="fd080-174">Derfor kan den bare aktiveres etter at du har installert avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="fd080-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Funksjonen Avgift i overføringsordre](../media/image7.png)

3. <span data-ttu-id="fd080-176">Aktiver avgiftstjenesten, og velg forretningsprosessen **Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="fd080-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="fd080-177">Du må fullføre dette trinnet for hver juridiske enhet i Finance der du vil at avgiftstjenesten og funksjonaliteten for avgift i overføringsordrer skal være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="fd080-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="fd080-178">Gå til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Oppsett av avgiftstjeneste**.</span><span class="sxs-lookup"><span data-stu-id="fd080-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="fd080-179">I **Forretningsprosess**-feltet velger du **Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="fd080-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Angi Forretningsprosess-feltet](../media/image8.png)

4. <span data-ttu-id="fd080-181">Kontroller at mekanismen for snudd avregning er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="fd080-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="fd080-182">Gå til **Økonomimodul** \> **Oppsett** \> **Parametere**, og gå deretter til fanen **Snudd avregning** og bekreft at **Aktiver snudd avregning** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fd080-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Aktiver alternativet for snudd avregning](../media/image9.png)

5. <span data-ttu-id="fd080-184">Kontroller at de tilknyttede avgiftskodene, avgiftsgruppene, vareavgiftsgruppene og mva-registreringsnumrene er definert i Finance i henhold til retningslinjene for avgiftstjenesten.</span><span class="sxs-lookup"><span data-stu-id="fd080-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="fd080-185">Definer en midlertidig transittkonto.</span><span class="sxs-lookup"><span data-stu-id="fd080-185">Set up an interim transit account.</span></span> <span data-ttu-id="fd080-186">Dette trinnet er bare nødvendig når avgiften som brukes på overføringsordrer, ikke gjelder for en mekanisme for avgiftsfritak eller snudd avregning.</span><span class="sxs-lookup"><span data-stu-id="fd080-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="fd080-187">Gå til **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Finansposteringsgrupper**.</span><span class="sxs-lookup"><span data-stu-id="fd080-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="fd080-188">I feltet **Midlertidig transitt** velger du en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="fd080-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Velge en midlertidig transittkonto](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="fd080-190">Konfigurer enkel beholdning for avgiftsordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="fd080-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="fd080-191">Følg denne fremgangsmåten for å sette opp enkel beholdning for å aktivere overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="fd080-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="fd080-192">Opprett stedene for send fra og sendt til for lagrene dine i forskjellige land eller områder, og legg til primæradressen for hvert område.</span><span class="sxs-lookup"><span data-stu-id="fd080-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="fd080-193">Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Steder**.</span><span class="sxs-lookup"><span data-stu-id="fd080-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="fd080-194">Velg **Ny** for å opprette stedet du vil tilordne til et lager senere.</span><span class="sxs-lookup"><span data-stu-id="fd080-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="fd080-195">Gjenta trinn 2 for alle de andre stedene du må opprette.</span><span class="sxs-lookup"><span data-stu-id="fd080-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd080-196">Ett av stedene du oppretter, bør ha navnet **Transitt**.</span><span class="sxs-lookup"><span data-stu-id="fd080-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="fd080-197">I senere trinn i denne fremgangsmåten tilordner du dette området til transittlageret, slik at avgiftsrelaterte beholdningsbilag kan posteres i "send"- og "motta"-transaksjoner for overføringsordrer.</span><span class="sxs-lookup"><span data-stu-id="fd080-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="fd080-198">Adressen til transittstedet er ikke relevant for avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="fd080-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="fd080-199">Du kan derfor la det stå tomt.</span><span class="sxs-lookup"><span data-stu-id="fd080-199">Therefore, you can leave it blank.</span></span>

    ![Sette opp steder](../media/image11.png)

2. <span data-ttu-id="fd080-201">Opprett lagre for send fra, transitt og send til.</span><span class="sxs-lookup"><span data-stu-id="fd080-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="fd080-202">Alle adresseopplysninger som vedlikeholdes på et lager, vil overstyre stedsadressen under avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="fd080-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="fd080-203">Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fd080-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="fd080-204">Velg **Ny** for å opprette et lager, og tilordne det til det tilsvarende stedet.</span><span class="sxs-lookup"><span data-stu-id="fd080-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="fd080-205">Gjenta trinn 2 for å opprette et lager for hvert sted etter behov.</span><span class="sxs-lookup"><span data-stu-id="fd080-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Definere lagre](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="fd080-207">For et send fra-lager må et transittlager være valgt i i **Transittlager**-feltet for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="fd080-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Velge et transittlager](../media/image13.png)

3. <span data-ttu-id="fd080-209">Kontroller at konfigurasjonen for beholdningspostering er definert for overføringsordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="fd080-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="fd080-210">Gå til **Lagerstyring** \> **Oppsett** \> **Postering** \> **Postering**.</span><span class="sxs-lookup"><span data-stu-id="fd080-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="fd080-211">På **Beholdning**-fanen kontrollerer du at en beholdningskonto er definert både for postering av **Lageravgang** og **Lagertilgang**.</span><span class="sxs-lookup"><span data-stu-id="fd080-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Definere lageravgangs- og lagertilgangspostering](../media/image14.png)

    3. <span data-ttu-id="fd080-213">Kontroller at en finanskonto er satt opp for postering av typen **Overføring, skyldig**.</span><span class="sxs-lookup"><span data-stu-id="fd080-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Definere postering av typen Overføring, skyldig](../media/image15.png)

    4. <span data-ttu-id="fd080-215">Kontroller at en finanskonto er satt opp for postering av typen **Overføring, tilgode**.</span><span class="sxs-lookup"><span data-stu-id="fd080-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Definere postering av typen Overføring, tilgode](../media/image16.png)
