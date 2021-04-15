---
title: Opprette og oppdatere en retur- og refusjonspolicy for en kanal
description: Dette emnet beskriver hvordan du definerer en retur- og refusjonspolicy for en kanal.
author: ShalabhjainMSFT
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: e23291130d55fdfb5c2e2077b78c221866d72c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792081"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="f1a74-103">Opprette og oppdatere en retur- og refunderingspolicy for en kanal</span><span class="sxs-lookup"><span data-stu-id="f1a74-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1a74-104">Kanalreturpolicyen i Dynamics 365 Commerce gjør det mulig for forhandlere å angi håndhevelser der betalingsmidler kan tillates for å behandle en retur på en salgsstedsenhet (POS).</span><span class="sxs-lookup"><span data-stu-id="f1a74-104">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="f1a74-105">Dette emnet beskriver trinnene for å definere en retur- og refusjonspolicy for en kanal.</span><span class="sxs-lookup"><span data-stu-id="f1a74-105">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="f1a74-106">Omfanget av policyen er for øyeblikket begrenset til å angi betalingsmidlene som kan være tillatt for en kanal.</span><span class="sxs-lookup"><span data-stu-id="f1a74-106">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="f1a74-107">"Tillatt"-listen er basert på betalingsmåtene som ble brukt til å utføre innkjøpet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-107">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="f1a74-108">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="f1a74-108">For example:</span></span>

- <span data-ttu-id="f1a74-109">Hvis et innkjøp ble foretatt ved hjelp av et gavekort, er butikkpolicyen å bare behandle refusjoner til et nytt gavekort eller gi butikkreditt.</span><span class="sxs-lookup"><span data-stu-id="f1a74-109">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="f1a74-110">Hvis et salg er produsert ved hjelp av kontanter, er alternativene som er tillatt for refusjon, kontanter, gavekort og kundekonto, men ikke kredittkort.</span><span class="sxs-lookup"><span data-stu-id="f1a74-110">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="f1a74-111">Aktivere returpolicy</span><span class="sxs-lookup"><span data-stu-id="f1a74-111">Enable return policy</span></span>

<span data-ttu-id="f1a74-112">Hvis du vil aktivere returpolicyfunksjonaliteten for en kanal, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f1a74-112">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="f1a74-113">Gå til arbeidsområdet **Funksjonsbehandling** i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1a74-113">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="f1a74-114">Søk etter funksjonen **Aktiver kanalreturpolicyer** i listen over funksjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="f1a74-114">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="f1a74-115">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="f1a74-115">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="f1a74-116">Konfigurere returpolicy</span><span class="sxs-lookup"><span data-stu-id="f1a74-116">Configure return policy</span></span>

<span data-ttu-id="f1a74-117">Følg denne fremgangsmåten for å konfigurere en returpolicy for en detaljhandelsbutikk eller en detaljhandelskanal på nettet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-117">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="f1a74-118">Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Returner** \> **Kanalreturpolicy**.</span><span class="sxs-lookup"><span data-stu-id="f1a74-118">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="f1a74-119">Velg **Ny** for å opprette en ny returpolicymal.</span><span class="sxs-lookup"><span data-stu-id="f1a74-119">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="f1a74-120">Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="f1a74-120">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="f1a74-121">For nye maler legger du til et navn og en beskrivelse som gjør det enklere å identifisere policyen når den brukes i kanalen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-121">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="f1a74-122">![Legg til ny returpolicy](media/Return-policy-page1.png "Legge til ny returpolicy")</span><span class="sxs-lookup"><span data-stu-id="f1a74-122">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="f1a74-123">I delen **Tillatte betalingsmåter for refusjoner** definerer du **Tillatte** returbetalingsmidler som er spesifikke for hver betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="f1a74-123">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="f1a74-124">![Legge til betalingsmåter](media/Return-policy-page2.PNG "Angi tillatte betalingsmåter per betalingstype")</span><span class="sxs-lookup"><span data-stu-id="f1a74-124">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="f1a74-125">Betalingsmåtene er avledet fra betalingsmåtene som er angitt for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-125">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="f1a74-126">Hvis du legger til en tillatt returbetalingstype for hver oppførte betalingsmåte, må du sørge for at returer kan gjøres til den tillatte returbetalingstypen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-126">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="f1a74-127">Knytt returpolicymalen til butikkene der den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="f1a74-127">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="f1a74-128">Velg **Legg til** i kategorien **Detaljhandelskanaler**, og knytt til de tilgjengelige kanalene.</span><span class="sxs-lookup"><span data-stu-id="f1a74-128">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="f1a74-129">I dialogboksen **Velg organisasjonsnoder** velger du butikkene, områdene og organisasjonene som malen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="f1a74-129">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="f1a74-130">Bare én returpolicymal kan knyttes til hver butikk.</span><span class="sxs-lookup"><span data-stu-id="f1a74-130">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="f1a74-131">Bruk pilknappene til å velge butikker, områder eller organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="f1a74-131">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="f1a74-132">Ikrafttredelsesdatoen på policyen vil være datoen da policyene brukes på kanalene og kanaljobbene kjøres.</span><span class="sxs-lookup"><span data-stu-id="f1a74-132">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="f1a74-133">![Dialogboksen Velg organisasjonsnoder](media/Return-policy-page3.PNG "Dialogboksen Velg organisasjonsnoder")</span><span class="sxs-lookup"><span data-stu-id="f1a74-133">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="f1a74-134">På siden **Distribusjonsplan** kjører du jobben **1070** for å vise at kanalreturpolicyen er tilgjengelig for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-134">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="f1a74-135">Forhåndsvise kanalreturpolicyen på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="f1a74-135">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="f1a74-136">Følg trinnene i et av følgende eksempler for å vise de tillatte returbetalingsmidlene på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="f1a74-136">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="f1a74-137">Logg deg på salgsstedet som en kasserer eller en leder.</span><span class="sxs-lookup"><span data-stu-id="f1a74-137">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="f1a74-138">Under **Skift og skuff** velger du **Vis Journal**.</span><span class="sxs-lookup"><span data-stu-id="f1a74-138">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="f1a74-139">Velg transaksjonen som er del av returen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-139">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="f1a74-140">Velg varene som skal refunderes, og velg deretter betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="f1a74-140">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="f1a74-141">Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-141">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="f1a74-142">Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="f1a74-142">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="f1a74-143">Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.</span><span class="sxs-lookup"><span data-stu-id="f1a74-143">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="f1a74-144">- eller -</span><span class="sxs-lookup"><span data-stu-id="f1a74-144">-or-</span></span>

1. <span data-ttu-id="f1a74-145">Logg deg på salgsstedet som en kasserer eller en leder.</span><span class="sxs-lookup"><span data-stu-id="f1a74-145">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="f1a74-146">Velg **Returtransaksjon**, og angi kvitterings-ID-en ved hjelp av strekkodeskanning eller manuell oppføring.</span><span class="sxs-lookup"><span data-stu-id="f1a74-146">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="f1a74-147">Velg transaksjonen som er del av returen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-147">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="f1a74-148">Velg varene som skal refunderes, og velg deretter betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="f1a74-148">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="f1a74-149">Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="f1a74-149">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="f1a74-150">Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="f1a74-150">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="f1a74-151">Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.</span><span class="sxs-lookup"><span data-stu-id="f1a74-151">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="f1a74-152">![Refusjon ikke tillatt](media/Return-policy-page6.png "Refusjonstype ikke tillatt")</span><span class="sxs-lookup"><span data-stu-id="f1a74-152">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="f1a74-153">![Liste over betalingsmåter](media/Return-policy-page5.PNG "Refusjonstyper tillatt")</span><span class="sxs-lookup"><span data-stu-id="f1a74-153">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
