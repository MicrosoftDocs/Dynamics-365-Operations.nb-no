---
title: Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø
description: Dette emnet forklarer hvordan du konfigurerer "kjøp på nett, hent i butikk" (BOPIS) i en evaluering av Microsoft Dynamics 365 Commerce-miljøet etter at det er klargjort.
author: rubendel
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 219504da62fd4637ed01f9acbab32f873cef81b0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795961"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="9992f-103">Konfigurere BOPIS i et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9992f-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9992f-104">Dette emnet forklarer hvordan du konfigurerer "kjøp på nett, hent i butikk" (BOPIS) i en evaluering av Microsoft Dynamics 365 Commerce-miljøet etter at miljøet er klargjort.</span><span class="sxs-lookup"><span data-stu-id="9992f-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="9992f-105">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="9992f-105">Prerequisite</span></span>

<span data-ttu-id="9992f-106">Fullfør prosedyrene i dette emnet bare etter at evalueringsmiljøet i Commerce er klargjort og konfigurert.</span><span class="sxs-lookup"><span data-stu-id="9992f-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="9992f-107">Hvis du vil ha informasjon om hvordan du klargjør og konfigurerer miljøet, kan du se [Klargjøre et Dynamics 365 Commerce-evalueringsmiljø](provisioning-guide.md) og [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="9992f-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="9992f-108">Når Commerce-miljøet er klargjort og konfigurert ende til ende, kan du bruke dette emnet til å aktivere BOPIS-scenarioer.</span><span class="sxs-lookup"><span data-stu-id="9992f-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="9992f-109">Konfigurere salgsstedet</span><span class="sxs-lookup"><span data-stu-id="9992f-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="9992f-110">Konfigurere Modern POS</span><span class="sxs-lookup"><span data-stu-id="9992f-110">Configure Modern POS</span></span>

<span data-ttu-id="9992f-111">BOPIS -scenarier som involverer en kredittkortbetaling, krever en maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="9992f-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="9992f-112">Maskinvarestasjonen er bygget inn i Modern POS for Windows- og Android-klienter.</span><span class="sxs-lookup"><span data-stu-id="9992f-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="9992f-113">Hvis du bruker Cloud POS eller Modern POS for iOS, må salgsstedsklienten være forbundet med en delt maskinvarestasjon.</span><span class="sxs-lookup"><span data-stu-id="9992f-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="9992f-114">Dette emnet beskriver hvordan du konfigurerer BOPIS for Windows- og Android-klienter.</span><span class="sxs-lookup"><span data-stu-id="9992f-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="9992f-115">Hvis du vil ha informasjon om hvordan du installerer en delt maskinvarestasjonen, kan du se [Konfigurere og installere Retail Hardware Station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="9992f-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="9992f-116">Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Kasser**.</span><span class="sxs-lookup"><span data-stu-id="9992f-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="9992f-117">Velg register **SANFRAN-5**, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="9992f-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="9992f-118">Endre verdien for feltet **Maskinvareprofil** fra **HW002** til **HW001**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9992f-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="9992f-119">Gå til **Detaljhandel og handel \> IT for Detaljhandel og handel \> Distribusjonsplan** for å synkronisere endringene.</span><span class="sxs-lookup"><span data-stu-id="9992f-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="9992f-120">Velg distribusjonsplanen **1090**, og velg deretter **Kjør nå** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="9992f-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="9992f-121">Velg **Ja** og deretter **OK** for å starte datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="9992f-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="9992f-122">Installere Modern POS</span><span class="sxs-lookup"><span data-stu-id="9992f-122">Install Modern POS</span></span>

1. <span data-ttu-id="9992f-123">Gå til **Detaljhandel og handel \> Kanaloppsett \> Salgsstedsoppsett \> Enheter**.</span><span class="sxs-lookup"><span data-stu-id="9992f-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="9992f-124">Velg enhet **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="9992f-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="9992f-125">I Handlingsvinduet, velg **Last ned**, og velg deretter **Konfigrasjonsfil**.</span><span class="sxs-lookup"><span data-stu-id="9992f-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="9992f-126">Velg **Last ned**, og velg deretter **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="9992f-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="9992f-127">Når nedlastingen av **ModernPOSSetup.exe**-filen er fullført, velger du **Åpne fil**.</span><span class="sxs-lookup"><span data-stu-id="9992f-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Åpne fil](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="9992f-129">Velg **Neste** for å gå gjennom installasjonsprosessen.</span><span class="sxs-lookup"><span data-stu-id="9992f-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="9992f-130">Når installasjonen er fullført, velger du **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="9992f-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="9992f-131">Aktivere Modern POS</span><span class="sxs-lookup"><span data-stu-id="9992f-131">Activate Modern POS</span></span>

1. <span data-ttu-id="9992f-132">Velg **start**-knappen på Windows-skrivebordet, og skriv deretter inn **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="9992f-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="9992f-133">Velg **Retail Modern POS**-programmet som skal initiere aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="9992f-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="9992f-134">Velg **Neste**.</span><span class="sxs-lookup"><span data-stu-id="9992f-134">Select **Next**.</span></span> <span data-ttu-id="9992f-135">Feltene **Server-URL**, **Enhets-ID** og **Kassenummer** skal være forhåndsutfylt ved hjelp av informasjon fra konfigurasjonsfilen du lastet ned i forrige prosedyre.</span><span class="sxs-lookup"><span data-stu-id="9992f-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="9992f-136">Velg **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="9992f-136">Select **Activate**.</span></span>
5. <span data-ttu-id="9992f-137">En godkjenningsdialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="9992f-137">An authentication dialog box appears.</span></span> <span data-ttu-id="9992f-138">Velg kontoen som bruker e-postadressen som tidligere var tilknyttet arbeider **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="9992f-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9992f-139">Hvis du ennå ikke har knyttet til en arbeider med din identitet, vil ikke aktiveringen lykkes.</span><span class="sxs-lookup"><span data-stu-id="9992f-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="9992f-140">I dette tilfellet følger du trinnene under "Knytt en arbeider til din identitet" i emnet [Konfigurere et Dynamics 365 Commerce-evalueringsmiljø](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="9992f-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="9992f-141">Når du blir bedt om å gjøre det mulig for organisasjonen å administrere enheten, velger du **Bare denne appen**.</span><span class="sxs-lookup"><span data-stu-id="9992f-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="9992f-142">Når aktiveringen er fullført, velger du **Komme i gang**.</span><span class="sxs-lookup"><span data-stu-id="9992f-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="9992f-143">Aktivere BOPIS i Modern POS</span><span class="sxs-lookup"><span data-stu-id="9992f-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="9992f-144">Logg inn på Modern POS ved å bruke **000713** som operatør-ID og **123** som passord.</span><span class="sxs-lookup"><span data-stu-id="9992f-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="9992f-145">Mens den innledende gjennomgangsvideoen spilles av, merker du av for de to avmerkingsboksene nederst i venstre hjørne i dialogboksen, og deretter lukker du dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="9992f-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="9992f-146">Hvis du ikke blir bedt om å lukke skiftet, blar du til høyre på **velkomstsiden**, velger **Lukk skift** og logger deretter på POS.</span><span class="sxs-lookup"><span data-stu-id="9992f-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="9992f-147">Når du er logget på, velger du **Utfør en ikke-skuff-operasjon** når du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="9992f-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="9992f-148">Rull til høyre på **velkomstsiden**, og velg operasjonen **Velg maskinvarestasjon**.</span><span class="sxs-lookup"><span data-stu-id="9992f-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="9992f-149">Velg **Behandle**, angi alternativet **Bruk maskinvarestasjon** til **På**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="9992f-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="9992f-150">Logg av salgsstedet, og logg deretter på.</span><span class="sxs-lookup"><span data-stu-id="9992f-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="9992f-151">Når du er logget på, velger du **Åpne et nytt skift**, og deretter velger du **Skuff**.</span><span class="sxs-lookup"><span data-stu-id="9992f-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="9992f-152">Fullføre et BOPIS-scenario</span><span class="sxs-lookup"><span data-stu-id="9992f-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="9992f-153">Opprette en butikkfasadeordre for henting i butikk</span><span class="sxs-lookup"><span data-stu-id="9992f-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="9992f-154">Gå til URL-adressen du angav i trinnet [Initialisere e-handel](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) under miljøkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="9992f-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="9992f-155">Velg en vare, og velg **Legg til i handlevogn**.</span><span class="sxs-lookup"><span data-stu-id="9992f-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="9992f-156">På handlepose-siden velger du **Plukk opp dette** for ordrelinjen du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="9992f-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="9992f-157">I dialogboksen **Velg en butikk** angir du **San Francisco**, og deretter velger du **Søk**-knappen.</span><span class="sxs-lookup"><span data-stu-id="9992f-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="9992f-158">Finn San Francisco-butikken i resultatlisten, og velg **Plukk her**.</span><span class="sxs-lookup"><span data-stu-id="9992f-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="9992f-159">Velg **Utsjekking som gjest** på handlepose-siden.</span><span class="sxs-lookup"><span data-stu-id="9992f-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9992f-160">Du må godta informasjonskapselmeldingen for å fortsette med utsjekkingen.</span><span class="sxs-lookup"><span data-stu-id="9992f-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="9992f-161">Denne merknaden vises som et banner øverst på betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="9992f-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="9992f-162">Angi følgende detaljer for kredittkortbetalingsmåten:</span><span class="sxs-lookup"><span data-stu-id="9992f-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="9992f-163">**Navn på kortinnehaver:** Skriv inn et hvilket som helst navn.</span><span class="sxs-lookup"><span data-stu-id="9992f-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="9992f-164">**Kortnummer:** Angi **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="9992f-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="9992f-165">**Utløpsdato:** Angi **10/20**.</span><span class="sxs-lookup"><span data-stu-id="9992f-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="9992f-166">**Verdi for kortbekreftelse (CVV-kode):** Angi **737**.</span><span class="sxs-lookup"><span data-stu-id="9992f-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="9992f-167">Du bør ikke prøve å bruke faktisk kredittkortinformasjon på testområdet under noen omstendigheter!</span><span class="sxs-lookup"><span data-stu-id="9992f-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="9992f-168">Fortsett med kassen ved å angi detaljer for faktureringsadressen, og velg deretter **Lagre og fortsett**.</span><span class="sxs-lookup"><span data-stu-id="9992f-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="9992f-169">Når ordren er klar til å plasseres, velger du **Utsjekking**.</span><span class="sxs-lookup"><span data-stu-id="9992f-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="9992f-170">Synkronisere elektroniske ordrer til Back Office</span><span class="sxs-lookup"><span data-stu-id="9992f-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="9992f-171">Hvis du vil ha informasjon om hvordan du synkroniserer elektroniske ordrer, kan du se [Postering av elektroniske salg og betalinger](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="9992f-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="9992f-172">Hente en ordre i butikken</span><span class="sxs-lookup"><span data-stu-id="9992f-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="9992f-173">Logg på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="9992f-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="9992f-174">På **velkomstskjermen** velger du **Ordreoppfyllelse**</span><span class="sxs-lookup"><span data-stu-id="9992f-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="9992f-175">I listen over varer for plukking velger du linjen fra bestillingen som ble lagt inn elektronisk.</span><span class="sxs-lookup"><span data-stu-id="9992f-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="9992f-176">Når ordrelinjen er valgt, velger du **Hent**.</span><span class="sxs-lookup"><span data-stu-id="9992f-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="9992f-177">Linjeelementet legges til i transaksjonsskjermbildet, og **$0,00** vises som forfalt saldo.</span><span class="sxs-lookup"><span data-stu-id="9992f-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="9992f-178">Velg den forfalt saldoen **$0,00**, eller velg en hvilken som helst betalingsmåte for å fullføre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="9992f-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9992f-179">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="9992f-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="9992f-180">Elektroniske ordrer som er hentet på salgsstedet, har en saldo som ikke er null</span><span class="sxs-lookup"><span data-stu-id="9992f-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="9992f-181">Når en ordre hentes for plukking i butikk og forfalt saldo ikke er 0 (null), må du kontrollere at det er brukt Modern POS og at maskinvarestasjonen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="9992f-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="9992f-182">Hvis Cloud POS eller Modern POS for iOS brukes, må du kontrollere at en delt maskinvarestasjon er aktiv.</span><span class="sxs-lookup"><span data-stu-id="9992f-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="9992f-183">En form for aktiv maskinvarestasjon er nødvendig for å hente betalinger som ble gjort tilkoblet.</span><span class="sxs-lookup"><span data-stu-id="9992f-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="9992f-184">Generelle problemer med betalingsregistrering</span><span class="sxs-lookup"><span data-stu-id="9992f-184">General issues with payment capture</span></span>

<span data-ttu-id="9992f-185">For alle generelle problemer bør du alltid se hendelsesloggene for maskinvarestasjoner i Modern POS eller Internet Information Services (IIS) som første trinn.</span><span class="sxs-lookup"><span data-stu-id="9992f-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="9992f-186">Du finner disse loggene under følgende noder i Windows-hendelsesloggen:</span><span class="sxs-lookup"><span data-stu-id="9992f-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="9992f-187">Program- og tjenestelogger \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="9992f-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="9992f-188">Program- og tjenestelogger \> Microsoft \> Dynamics \> Commerce-Hardware Station</span><span class="sxs-lookup"><span data-stu-id="9992f-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9992f-189">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9992f-189">Additional resources</span></span>

[<span data-ttu-id="9992f-190">Oversikt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="9992f-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="9992f-191">Klargjøre et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9992f-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="9992f-192">Konfigurere valgfrie funksjoner for et evalueringsmiljø for Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="9992f-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="9992f-193">Vanlige spørsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="9992f-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="9992f-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9992f-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="9992f-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="9992f-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="9992f-196">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="9992f-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="9992f-197">Dynamics 365 Commerce-webområde</span><span class="sxs-lookup"><span data-stu-id="9992f-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="9992f-198">Betalingskobling for Ayden</span><span class="sxs-lookup"><span data-stu-id="9992f-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="9992f-199">Lagre betalingsmåter på nett med Adyen-koblingen</span><span class="sxs-lookup"><span data-stu-id="9992f-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="9992f-200">Oversikt over betalinger for omnikanal</span><span class="sxs-lookup"><span data-stu-id="9992f-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)


[!INCLUDE[footer-include](../includes/footer-banner.md)]