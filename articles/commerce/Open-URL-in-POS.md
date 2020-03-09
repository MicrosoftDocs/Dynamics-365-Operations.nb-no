---
title: Åpne URL-adresse på salgssted
description: Dette emnet gir en oversikt over forbedringer som har blitt gjort for produkt- og kundesøkfunksjonalitet i Dynamics 365 Commerce.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 137b699d5f60b9b62a5ce9501e3b2a262e60a88f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023495"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="0e533-103">Åpne URL-adresse i POS</span><span class="sxs-lookup"><span data-stu-id="0e533-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e533-104">Dette emnet beskriver hvordan du kan konfigurere en knapp på salgsstedet for detaljhandel (POS) for å åpne en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="0e533-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="0e533-105">Denne funksjonen krever ikke tilpasning av koden og kan konfigureres av en person i en ikke-utviklerrolle.</span><span class="sxs-lookup"><span data-stu-id="0e533-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="0e533-106">Denne funksjonen tillater konfigurasjon av en knapp på salgsstedet ved hjelp av knappgruppedesigneren for å åpne en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="0e533-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="0e533-107">Dette støttes for øyeblikket i følgende konfigurasjoner:</span><span class="sxs-lookup"><span data-stu-id="0e533-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="0e533-108">Åpne i nytt vindu.</span><span class="sxs-lookup"><span data-stu-id="0e533-108">Open in new window.</span></span>
- <span data-ttu-id="0e533-109">Åpne på salgssted.</span><span class="sxs-lookup"><span data-stu-id="0e533-109">Open within POS.</span></span>
- <span data-ttu-id="0e533-110">Åpne i innebygd program.</span><span class="sxs-lookup"><span data-stu-id="0e533-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="0e533-111">Åpne i nytt vindu</span><span class="sxs-lookup"><span data-stu-id="0e533-111">Open in new window</span></span>

<span data-ttu-id="0e533-112">Denne konfigurasjonen definerer om du vil åpne URL-adressen i et nytt vindu eller i programmet.</span><span class="sxs-lookup"><span data-stu-id="0e533-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="0e533-113">Når den konfigureres for å åpne en URL-adresse i programmet, er sidenavigasjonspanelet og den øverste linjen på salgsstedet synlige og tilgjengelige for brukersamhandling.</span><span class="sxs-lookup"><span data-stu-id="0e533-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="0e533-114">Når den er konfigurert til å åpnes i et nytt vindu, åpnes URL-adressen i et nytt appvindu på Modern POS for Windows og i en ny webleserkategori på alle andre salgsstedsklienter.</span><span class="sxs-lookup"><span data-stu-id="0e533-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="0e533-115">For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.</span><span class="sxs-lookup"><span data-stu-id="0e533-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="0e533-116">Åpne på salgssted</span><span class="sxs-lookup"><span data-stu-id="0e533-116">Open within POS</span></span>

<span data-ttu-id="0e533-117">Åpning av en URL-adresse på salgsstedet støttes for tiden bare for Modern POS på Windows.</span><span class="sxs-lookup"><span data-stu-id="0e533-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="0e533-118">På andre klienter er denne funksjonen under utvikling og planlagt for frigivelse i fremtidige oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="0e533-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="0e533-119">For å aktivere dette må du konfigurere URL-adressen når **Åpne i nytt vindu**-alternativet ikke er valgt.</span><span class="sxs-lookup"><span data-stu-id="0e533-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="0e533-120">Åpne i innebygd program</span><span class="sxs-lookup"><span data-stu-id="0e533-120">Open a native app</span></span>

<span data-ttu-id="0e533-121">Med denne funksjonen kan du også angi at ikke-URL-adresser skal åpne et opprinnelig program.</span><span class="sxs-lookup"><span data-stu-id="0e533-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="0e533-122">Du kan for eksempel angi URL-protokoller, for eksempel MailTo, SIP, IM eller MSTEAMS, som kan behandles av respektive opprinnelige programmer på vertsenheten.</span><span class="sxs-lookup"><span data-stu-id="0e533-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="0e533-123">For å aktivere dette må du konfigurere URL-adressen med **Åpne i nytt vindu**-alternativet valgt.</span><span class="sxs-lookup"><span data-stu-id="0e533-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="0e533-124">For Windows-datamaskiner kan du se [Eksportere eller importere standard programtilknytninger](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) for å angi standard protokollytilknytninger hvis du setter opp datamaskinen ved å bruke Deployment Image Servicing and Management (DISM).</span><span class="sxs-lookup"><span data-stu-id="0e533-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="0e533-125">Hvis du bruker MDM, for eksempel Intune, til å administrere Windows-datamaskiner, kan du se [Policy for CSP - programstandarder](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="0e533-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="0e533-126">Hvis du er en utvikler som bygger et egendefinert webområde, kan du se [Starte standardappen for en URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="0e533-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="0e533-127">Åpne i innebygd program sømløst</span><span class="sxs-lookup"><span data-stu-id="0e533-127">Open a native app seamlessly</span></span>

<span data-ttu-id="0e533-128">Windows, iOS og Android tillater også åpning av programmer mer sømløst basert på approtokolltilknytning.</span><span class="sxs-lookup"><span data-stu-id="0e533-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="0e533-129">Hvis ditt program ikke allerede er konfigurert for å håndtere åpning fra en webleser, må du kanskje få en utvikler til å konfigurere dette.</span><span class="sxs-lookup"><span data-stu-id="0e533-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="0e533-130">For Windows kan du se [Aktivere apper for nettsteder ved hjelp av URI-behandlingsprogrammer](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="0e533-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="0e533-131">For iOS kan du se [Universielle koblinger for utviklere](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="0e533-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="0e533-132">For Android kan du se [Behandle Android-appkoblinger](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="0e533-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="0e533-133">Kunde</span><span class="sxs-lookup"><span data-stu-id="0e533-133">Client</span></span>                | <span data-ttu-id="0e533-134">Åpne i nytt vindu</span><span class="sxs-lookup"><span data-stu-id="0e533-134">Open in new window</span></span> | <span data-ttu-id="0e533-135">Åpne innebygd program</span><span class="sxs-lookup"><span data-stu-id="0e533-135">Open native app</span></span> | <span data-ttu-id="0e533-136">Åpne på salgssted</span><span class="sxs-lookup"><span data-stu-id="0e533-136">Open within POS</span></span> | <span data-ttu-id="0e533-137">Detaljer</span><span class="sxs-lookup"><span data-stu-id="0e533-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="0e533-138">Modern POS på Windows</span><span class="sxs-lookup"><span data-stu-id="0e533-138">Modern POS on Windows</span></span> | <span data-ttu-id="0e533-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="0e533-139">✓\*</span></span>                | <span data-ttu-id="0e533-140">✓</span><span class="sxs-lookup"><span data-stu-id="0e533-140">✓</span></span>               | <span data-ttu-id="0e533-141">✓</span><span class="sxs-lookup"><span data-stu-id="0e533-141">✓</span></span>              | <span data-ttu-id="0e533-142">\* Åpner i nytt Modern POS-vindu</span><span class="sxs-lookup"><span data-stu-id="0e533-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="0e533-143">Skybasert salgssted</span><span class="sxs-lookup"><span data-stu-id="0e533-143">Cloud POS</span></span>             | <span data-ttu-id="0e533-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="0e533-144">✓\*</span></span>                | <span data-ttu-id="0e533-145">✓</span><span class="sxs-lookup"><span data-stu-id="0e533-145">✓</span></span>               | <span data-ttu-id="0e533-146">X</span><span class="sxs-lookup"><span data-stu-id="0e533-146">X</span></span>              | <span data-ttu-id="0e533-147">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="0e533-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="0e533-148">Modern POS på iOS</span><span class="sxs-lookup"><span data-stu-id="0e533-148">Modern POS on iOS</span></span>     | <span data-ttu-id="0e533-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="0e533-149">✓\*</span></span>                | <span data-ttu-id="0e533-150">✓</span><span class="sxs-lookup"><span data-stu-id="0e533-150">✓</span></span>               | <span data-ttu-id="0e533-151">X</span><span class="sxs-lookup"><span data-stu-id="0e533-151">X</span></span>              | <span data-ttu-id="0e533-152">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="0e533-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="0e533-153">Modern POS på Android</span><span class="sxs-lookup"><span data-stu-id="0e533-153">Modern POS on Android</span></span> | <span data-ttu-id="0e533-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="0e533-154">✓\*</span></span>                | <span data-ttu-id="0e533-155">✓</span><span class="sxs-lookup"><span data-stu-id="0e533-155">✓</span></span>               | <span data-ttu-id="0e533-156">X</span><span class="sxs-lookup"><span data-stu-id="0e533-156">X</span></span>              | <span data-ttu-id="0e533-157">\* Åpnes i ny nettleserfane</span><span class="sxs-lookup"><span data-stu-id="0e533-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="0e533-158">Før du begynner</span><span class="sxs-lookup"><span data-stu-id="0e533-158">Before you begin</span></span>

<span data-ttu-id="0e533-159">Før du begynner kan du se hvordan du konfigurerer [Skjermoppsett for salgssted (POS)](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="0e533-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="0e533-160">Åpne URL-adresse på salgssted</span><span class="sxs-lookup"><span data-stu-id="0e533-160">Open URL in POS</span></span>

<span data-ttu-id="0e533-161">Hvis du vil konfigurere en URL-adresse som skal åpnes i POS, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="0e533-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="0e533-162">På hovedkontoret går du til **Retail og Commerce \> Kanaloppsett \> Salgsstedsoppsett \> Salgssted \> Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="0e533-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="0e533-163">Velg **Knappegrupper \> Designer**.</span><span class="sxs-lookup"><span data-stu-id="0e533-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="0e533-164">Opprett en ny knapp.</span><span class="sxs-lookup"><span data-stu-id="0e533-164">Create a new button.</span></span>
4. <span data-ttu-id="0e533-165">Velg **Knapp**-egenskaper.</span><span class="sxs-lookup"><span data-stu-id="0e533-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="0e533-166">Velg **Åpne URL** som handling.</span><span class="sxs-lookup"><span data-stu-id="0e533-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="0e533-167">Skriv inn URL-en du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="0e533-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="0e533-168">Konfigurer om du vil åpne URL-adressen i et nytt vindu.</span><span class="sxs-lookup"><span data-stu-id="0e533-168">Configure whether to open the URL in a new window.</span></span>