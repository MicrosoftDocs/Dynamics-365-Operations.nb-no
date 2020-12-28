---
title: Opprette og oppdatere en retur- og refusjonspolicy for en kanal
description: Dette emnet beskriver hvordan du definerer en retur- og refusjonspolicy for en kanal.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414744"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="2f109-103">Opprette og oppdatere en retur- og refusjonspolicy for en kanal</span><span class="sxs-lookup"><span data-stu-id="2f109-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="2f109-104">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2f109-104">Overview</span></span>

<span data-ttu-id="2f109-105">Kanalreturpolicyen i Dynamics 365 Commerce gjør det mulig for forhandlere å angi håndhevelser der betalingsmidler kan tillates for å behandle en retur på en salgsstedsenhet (POS).</span><span class="sxs-lookup"><span data-stu-id="2f109-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="2f109-106">Dette emnet beskriver trinnene for å definere en retur- og refusjonspolicy for en kanal.</span><span class="sxs-lookup"><span data-stu-id="2f109-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="2f109-107">Omfanget av policyen er for øyeblikket begrenset til å angi betalingsmidlene som kan være tillatt for en kanal.</span><span class="sxs-lookup"><span data-stu-id="2f109-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="2f109-108">"Tillatt"-listen er basert på betalingsmåtene som ble brukt til å utføre innkjøpet.</span><span class="sxs-lookup"><span data-stu-id="2f109-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="2f109-109">For eksempel:</span><span class="sxs-lookup"><span data-stu-id="2f109-109">For example:</span></span>

- <span data-ttu-id="2f109-110">Hvis et innkjøp ble foretatt ved hjelp av et gavekort, er butikkpolicyen å bare behandle refusjoner til et nytt gavekort eller gi butikkreditt.</span><span class="sxs-lookup"><span data-stu-id="2f109-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="2f109-111">Hvis et salg er produsert ved hjelp av kontanter, er alternativene som er tillatt for refusjon, kontanter, gavekort og kundekonto, men ikke kredittkort.</span><span class="sxs-lookup"><span data-stu-id="2f109-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="2f109-112">Aktivere returpolicy</span><span class="sxs-lookup"><span data-stu-id="2f109-112">Enable return policy</span></span>

<span data-ttu-id="2f109-113">Hvis du vil aktivere returpolicyfunksjonaliteten for en kanal, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="2f109-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="2f109-114">Gå til arbeidsområdet **Funksjonsbehandling** i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2f109-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="2f109-115">Søk etter funksjonen **Aktiver kanalreturpolicyer** i listen over funksjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="2f109-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="2f109-116">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="2f109-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="2f109-117">Konfigurere returpolicy</span><span class="sxs-lookup"><span data-stu-id="2f109-117">Configure return policy</span></span>

<span data-ttu-id="2f109-118">Følg denne fremgangsmåten for å konfigurere en returpolicy for en detaljhandelsbutikk eller en detaljhandelskanal på nettet.</span><span class="sxs-lookup"><span data-stu-id="2f109-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="2f109-119">Gå til **Retail og Commerce** \> **Kanaloppsett** \> **Returner** \> **Kanalreturpolicy**.</span><span class="sxs-lookup"><span data-stu-id="2f109-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="2f109-120">Velg **Ny** for å opprette en ny returpolicymal.</span><span class="sxs-lookup"><span data-stu-id="2f109-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="2f109-121">Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="2f109-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="2f109-122">For nye maler legger du til et navn og en beskrivelse som gjør det enklere å identifisere policyen når den brukes i kanalen.</span><span class="sxs-lookup"><span data-stu-id="2f109-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="2f109-123">![Legg til ny returpolicy](media/Return-policy-page1.png "Legge til ny returpolicy")</span><span class="sxs-lookup"><span data-stu-id="2f109-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="2f109-124">I delen **Tillatte betalingsmåter for refusjoner** definerer du **Tillatte** returbetalingsmidler som er spesifikke for hver betalingsmåte.</span><span class="sxs-lookup"><span data-stu-id="2f109-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="2f109-125">![Legge til betalingsmåter](media/Return-policy-page2.PNG "Angi tillatte betalingsmåter per betalingstype")</span><span class="sxs-lookup"><span data-stu-id="2f109-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="2f109-126">Betalingsmåtene er avledet fra betalingsmåtene som er angitt for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="2f109-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="2f109-127">Hvis du legger til en tillatt returbetalingstype for hver oppførte betalingsmåte, må du sørge for at returer kan gjøres til den tillatte returbetalingstypen.</span><span class="sxs-lookup"><span data-stu-id="2f109-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="2f109-128">Knytt returpolicymalen til butikkene der den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="2f109-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="2f109-129">Velg **Legg til** i kategorien **Detaljhandelskanaler**, og knytt til de tilgjengelige kanalene.</span><span class="sxs-lookup"><span data-stu-id="2f109-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="2f109-130">I dialogboksen **Velg organisasjonsnoder** velger du butikkene, områdene og organisasjonene som malen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="2f109-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="2f109-131">Bare én returpolicymal kan knyttes til hver butikk.</span><span class="sxs-lookup"><span data-stu-id="2f109-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="2f109-132">Bruk pilknappene til å velge butikker, områder eller organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="2f109-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="2f109-133">Ikrafttredelsesdatoen på policyen vil være datoen da policyene brukes på kanalene og kanaljobbene kjøres.</span><span class="sxs-lookup"><span data-stu-id="2f109-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="2f109-134">![Dialogboksen Velg organisasjonsnoder](media/Return-policy-page3.PNG "Dialogboksen Velg organisasjonsnoder")</span><span class="sxs-lookup"><span data-stu-id="2f109-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="2f109-135">På siden **Distribusjonsplan** kjører du jobben **1070** for å vise at kanalreturpolicyen er tilgjengelig for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="2f109-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="2f109-136">Forhåndsvise kanalreturpolicyen på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="2f109-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="2f109-137">Følg trinnene i et av følgende eksempler for å vise de tillatte returbetalingsmidlene på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="2f109-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="2f109-138">Logg deg på salgsstedet som en kasserer eller en leder.</span><span class="sxs-lookup"><span data-stu-id="2f109-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="2f109-139">Under **Skift og skuff** velger du **Vis Journal**.</span><span class="sxs-lookup"><span data-stu-id="2f109-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="2f109-140">Velg transaksjonen som er del av returen.</span><span class="sxs-lookup"><span data-stu-id="2f109-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="2f109-141">Velg varene som skal refunderes, og velg deretter betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="2f109-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="2f109-142">Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="2f109-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="2f109-143">Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="2f109-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="2f109-144">Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.</span><span class="sxs-lookup"><span data-stu-id="2f109-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="2f109-145">- eller -</span><span class="sxs-lookup"><span data-stu-id="2f109-145">-or-</span></span>

1. <span data-ttu-id="2f109-146">Logg deg på salgsstedet som en kasserer eller en leder.</span><span class="sxs-lookup"><span data-stu-id="2f109-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="2f109-147">Velg **Returtransaksjon**, og angi kvitterings-ID-en ved hjelp av strekkodeskanning eller manuell oppføring.</span><span class="sxs-lookup"><span data-stu-id="2f109-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="2f109-148">Velg transaksjonen som er del av returen.</span><span class="sxs-lookup"><span data-stu-id="2f109-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="2f109-149">Velg varene som skal refunderes, og velg deretter betalingsmåten.</span><span class="sxs-lookup"><span data-stu-id="2f109-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="2f109-150">Hvis valgt betalingsmiddelet er i listen over tillatte returbetalingstyper, kan kassereren fullføre transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="2f109-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="2f109-151">Hvis det valgte betalingsmiddelet ikke er tillatt, vises en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="2f109-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="2f109-152">Velg **Beløp å betale** for å vise en liste over alle tillatte returbetalingstyper.</span><span class="sxs-lookup"><span data-stu-id="2f109-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="2f109-153">![Refusjon ikke tillatt](media/Return-policy-page6.png "Refusjonstype ikke tillatt")</span><span class="sxs-lookup"><span data-stu-id="2f109-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="2f109-154">![Liste over betalingsmåter](media/Return-policy-page5.PNG "Refusjonstyper tillatt")</span><span class="sxs-lookup"><span data-stu-id="2f109-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
