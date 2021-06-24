---
title: Åpne URL-adresse på salgssted
description: Dette emnet gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193209"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="671cc-103">Åpne URL-adresse på salgssted</span><span class="sxs-lookup"><span data-stu-id="671cc-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="671cc-104">Dette emnet beskriver hvordan du kan konfigurere en knapp i POS i Dynamics 365 Commerce for å åpne en nettadresse.</span><span class="sxs-lookup"><span data-stu-id="671cc-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="671cc-105">Denne funksjonen krever ikke tilpasning av koden og kan konfigureres av en person i en ikke-utviklerrolle.</span><span class="sxs-lookup"><span data-stu-id="671cc-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="671cc-106">Denne funksjonen tillater konfigurasjon av en knapp på salgsstedet ved hjelp av knappgruppedesigneren for å åpne en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="671cc-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="671cc-107">Dette støttes for øyeblikket i følgende konfigurasjoner:</span><span class="sxs-lookup"><span data-stu-id="671cc-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="671cc-108">Åpne i nytt vindu.</span><span class="sxs-lookup"><span data-stu-id="671cc-108">Open in new window.</span></span>
- <span data-ttu-id="671cc-109">Åpne på salgssted.</span><span class="sxs-lookup"><span data-stu-id="671cc-109">Open within POS.</span></span>
- <span data-ttu-id="671cc-110">Åpne i innebygd program.</span><span class="sxs-lookup"><span data-stu-id="671cc-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="671cc-111">Åpne i nytt vindu</span><span class="sxs-lookup"><span data-stu-id="671cc-111">Open in new window</span></span>

<span data-ttu-id="671cc-112">Denne konfigurasjonen definerer om du vil åpne URL-adressen i et nytt vindu eller i programmet.</span><span class="sxs-lookup"><span data-stu-id="671cc-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="671cc-113">Når den konfigureres for å åpne en URL-adresse i programmet, er sidenavigasjonspanelet og den øverste linjen på salgsstedet synlige og tilgjengelige for brukersamhandling.</span><span class="sxs-lookup"><span data-stu-id="671cc-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="671cc-114">Når den er konfigurert til å åpnes i et nytt vindu, åpnes URL-adressen i et nytt appvindu på Modern POS for Windows og i en ny webleserkategori på alle andre salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="671cc-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="671cc-115">For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.</span><span class="sxs-lookup"><span data-stu-id="671cc-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="671cc-116">Åpne på salgssted</span><span class="sxs-lookup"><span data-stu-id="671cc-116">Open within POS</span></span>

<span data-ttu-id="671cc-117">Åpning av en URL-adresse på salgsstedet støttes for tiden bare for Modern POS på Windows.</span><span class="sxs-lookup"><span data-stu-id="671cc-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="671cc-118">På andre klienter er denne funksjonen under utvikling og planlagt for frigivelse i fremtidige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="671cc-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="671cc-119">For å aktivere dette må du konfigurere URL-adressen når **Åpne i nytt vindu**-alternativet ikke er valgt.</span><span class="sxs-lookup"><span data-stu-id="671cc-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="671cc-120">Åpne i innebygd program</span><span class="sxs-lookup"><span data-stu-id="671cc-120">Open a native app</span></span>

<span data-ttu-id="671cc-121">Med denne funksjonen kan du også angi at ikke-URL-adresser skal åpne et opprinnelig program.</span><span class="sxs-lookup"><span data-stu-id="671cc-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="671cc-122">Du kan for eksempel angi URL-protokoller, for eksempel MailTo, SIP, IM eller MSTEAMS, som kan behandles av respektive opprinnelige programmer på vertsenheten.</span><span class="sxs-lookup"><span data-stu-id="671cc-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="671cc-123">For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.</span><span class="sxs-lookup"><span data-stu-id="671cc-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="671cc-124">For Windows-datamaskiner kan du se [Eksportere eller importere standard programtilknytninger](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) for å angi standard protokollytilknytninger hvis du setter opp datamaskinen ved å bruke Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="671cc-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="671cc-125">Hvis du bruker MDM, for eksempel Intune, til å administrere Windows-datamaskiner, kan du se [Policy for CSP - programstandarder](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="671cc-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="671cc-126">Hvis du er en utvikler som bygger et egendefinert webområde, kan du se [Starte standardappen for en URI](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="671cc-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="671cc-127">Åpne i innebygd program sømløst</span><span class="sxs-lookup"><span data-stu-id="671cc-127">Open a native app seamlessly</span></span>

<span data-ttu-id="671cc-128">Windows, iOS og Android tillater også åpning av programmer mer sømløst basert på approtokolltilknytning.</span><span class="sxs-lookup"><span data-stu-id="671cc-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="671cc-129">Hvis ditt program ikke allerede er konfigurert for å håndtere åpning fra en webleser, må du kanskje få en utvikler til å konfigurere dette.</span><span class="sxs-lookup"><span data-stu-id="671cc-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="671cc-130">For Windows kan du se [Aktivere apper for nettsteder ved hjelp av URI-behandlingsprogrammer](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="671cc-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="671cc-131">For iOS kan du se [Universielle koblinger for utviklere](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="671cc-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="671cc-132">For Android kan du se [Behandle Android-appkoblinger](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="671cc-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="671cc-133">Kunde</span><span class="sxs-lookup"><span data-stu-id="671cc-133">Client</span></span>                | <span data-ttu-id="671cc-134">Åpne i nytt vindu</span><span class="sxs-lookup"><span data-stu-id="671cc-134">Open in new window</span></span> | <span data-ttu-id="671cc-135">Åpne innebygd program</span><span class="sxs-lookup"><span data-stu-id="671cc-135">Open native app</span></span> | <span data-ttu-id="671cc-136">Åpne på salgssted</span><span class="sxs-lookup"><span data-stu-id="671cc-136">Open within POS</span></span> | <span data-ttu-id="671cc-137">Detaljer</span><span class="sxs-lookup"><span data-stu-id="671cc-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="671cc-138">Modern POS på Windows</span><span class="sxs-lookup"><span data-stu-id="671cc-138">Modern POS on Windows</span></span> | <span data-ttu-id="671cc-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="671cc-139">✓\*</span></span>                | <span data-ttu-id="671cc-140">✓</span><span class="sxs-lookup"><span data-stu-id="671cc-140">✓</span></span>               | <span data-ttu-id="671cc-141">✓</span><span class="sxs-lookup"><span data-stu-id="671cc-141">✓</span></span>              | <span data-ttu-id="671cc-142">\* Åpner i nytt Modern POS-vindu</span><span class="sxs-lookup"><span data-stu-id="671cc-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="671cc-143">Skybasert salgssted</span><span class="sxs-lookup"><span data-stu-id="671cc-143">Cloud POS</span></span>             | <span data-ttu-id="671cc-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="671cc-144">✓\*</span></span>                | <span data-ttu-id="671cc-145">✓</span><span class="sxs-lookup"><span data-stu-id="671cc-145">✓</span></span>               | <span data-ttu-id="671cc-146">X</span><span class="sxs-lookup"><span data-stu-id="671cc-146">X</span></span>              | <span data-ttu-id="671cc-147">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="671cc-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="671cc-148">Modern POS på iOS</span><span class="sxs-lookup"><span data-stu-id="671cc-148">Modern POS on iOS</span></span>     | <span data-ttu-id="671cc-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="671cc-149">✓\*</span></span>                | <span data-ttu-id="671cc-150">✓</span><span class="sxs-lookup"><span data-stu-id="671cc-150">✓</span></span>               | <span data-ttu-id="671cc-151">X</span><span class="sxs-lookup"><span data-stu-id="671cc-151">X</span></span>              | <span data-ttu-id="671cc-152">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="671cc-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="671cc-153">Modern POS på Android</span><span class="sxs-lookup"><span data-stu-id="671cc-153">Modern POS on Android</span></span> | <span data-ttu-id="671cc-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="671cc-154">✓\*</span></span>                | <span data-ttu-id="671cc-155">✓</span><span class="sxs-lookup"><span data-stu-id="671cc-155">✓</span></span>               | <span data-ttu-id="671cc-156">X</span><span class="sxs-lookup"><span data-stu-id="671cc-156">X</span></span>              | <span data-ttu-id="671cc-157">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="671cc-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="671cc-158">Før du begynner</span><span class="sxs-lookup"><span data-stu-id="671cc-158">Before you begin</span></span>

<span data-ttu-id="671cc-159">Før du begynner kan du se hvordan du konfigurerer [Skjermoppsett for salgssted (POS)](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="671cc-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="671cc-160">Åpne URL-adresse på salgssted</span><span class="sxs-lookup"><span data-stu-id="671cc-160">Open URL in POS</span></span>

<span data-ttu-id="671cc-161">Hvis du vil konfigurere en URL-adresse som skal åpnes i POS, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="671cc-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="671cc-162">På hovedkontoret går du til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="671cc-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="671cc-163">Velg **Knappegrupper \> Designer**.</span><span class="sxs-lookup"><span data-stu-id="671cc-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="671cc-164">Opprett en ny knapp.</span><span class="sxs-lookup"><span data-stu-id="671cc-164">Create a new button.</span></span>
4. <span data-ttu-id="671cc-165">Velg **Knapp**-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="671cc-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="671cc-166">Velg **Åpne URL** som handling.</span><span class="sxs-lookup"><span data-stu-id="671cc-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="671cc-167">Skriv inn URL-en du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="671cc-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="671cc-168">Konfigurer om du vil åpne URL-adressen i et nytt vindu.</span><span class="sxs-lookup"><span data-stu-id="671cc-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
