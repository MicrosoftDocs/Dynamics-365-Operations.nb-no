---
title: Arbeide med CSS-overstyringsfiler
description: Dette emnet beskriver hvorfor, når og hvordan du bruker gjennomgripende stilark (CSS-overstyringsfiler) i Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799499"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="97950-103">Arbeide med CSS-overstyringsfiler</span><span class="sxs-lookup"><span data-stu-id="97950-103">Work with CSS override files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97950-104">Dette emnet beskriver hvorfor, når og hvordan du bruker gjennomgripende stilark (CSS-overstyringsfiler) i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97950-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="97950-105">Permanente områdestiler bør vanligvis håndteres gjennom et områdetema.</span><span class="sxs-lookup"><span data-stu-id="97950-105">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="97950-106">Temaer gir grunnleggende CSS og stilinnstillinger for modulene på en hvilken som helst side på nettstedet.</span><span class="sxs-lookup"><span data-stu-id="97950-106">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="97950-107">Temaene opprettes ved hjelp av Dynamics 365 Commerce Online Software Development Kit (SDK), og de distribueres til nettstedene gjennom Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="97950-107">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="97950-108">Feilsøkingsfunksjoner for temaer og modulgrensesnittkonfigurasjoner i SDK hjelper nettstedsutviklere med å opprette tilpasningsmulige og sammenhengende områdeutformingspakker.</span><span class="sxs-lookup"><span data-stu-id="97950-108">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="97950-109">Når disse utformingspakkene distribueres til et område, kan områdeforfattere fokusere på å opprette, redigere og publisere innhold i stedet for områdeutvikling.</span><span class="sxs-lookup"><span data-stu-id="97950-109">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="97950-110">Gitt den vanlige livssyklusen til et tema kan avhengighetsforholdet til utviklere for å gjøre stilendringer gjennom SDK- og LCS-distribusjonsforløpet, skape hindringer i enkelte scenarier.</span><span class="sxs-lookup"><span data-stu-id="97950-110">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="97950-111">Områdeprototyper eller hurtigreparasjoner kan virke tungvint hvis SDK ikke er konfigurert, eller hvis du ikke har tid til å vente på en LCS-distribusjon.</span><span class="sxs-lookup"><span data-stu-id="97950-111">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="97950-112">I disse scenariene kan CSS-overstyringsfiler hjelpe.</span><span class="sxs-lookup"><span data-stu-id="97950-112">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="97950-113">I redigeringsverktøyene for handel kan godkjente brukere laste opp en CSS-fil, forhåndsvise den og deretter aktivere den for å overstyre temaet for et område.</span><span class="sxs-lookup"><span data-stu-id="97950-113">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="97950-114">Det er ikke nødvendig å distribuere administrasjonskostnader for SDK eller LCS.</span><span class="sxs-lookup"><span data-stu-id="97950-114">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="97950-115">Overstyringer som er angitt i en CSS-overstyringsfil, kan være så liten som en endring i en enkelt tekststil eller så omfattende som en fullstendig merkevareoverhaling.</span><span class="sxs-lookup"><span data-stu-id="97950-115">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="97950-116">Før du bruker CSS-overstyringsfiler, må du være oppmerksom på følgende begrensninger:</span><span class="sxs-lookup"><span data-stu-id="97950-116">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="97950-117">Bare én CSS-overstyringsfil kan være aktiv på et område om gangen.</span><span class="sxs-lookup"><span data-stu-id="97950-117">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="97950-118">Derfor må alle aktive overstyringer være til stede i én enkelt overstyringsfil.</span><span class="sxs-lookup"><span data-stu-id="97950-118">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="97950-119">Selv om du kan forhåndsvise overstyringer i redigeringsverktøyene for handel, er det ingen dedikerte feilsøkingsfunksjoner som hjelper deg med å identifisere eventuelle feil som overstyres.</span><span class="sxs-lookup"><span data-stu-id="97950-119">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="97950-120">Med andre ord, når du bruker CSS-overstyringsfiler, har du ikke det samme verktøysettet som SDK gir for modul- og redigeringsvalidering.</span><span class="sxs-lookup"><span data-stu-id="97950-120">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="97950-121">CSS-overstyringsfiler gir likevel en rask måte å prototype en design eller implementere en hurtigreparasjon på før en full temaoppdatering er utviklet og distribuert.</span><span class="sxs-lookup"><span data-stu-id="97950-121">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="97950-122">Opprette en CSS-overstyringsfil</span><span class="sxs-lookup"><span data-stu-id="97950-122">Create a CSS override file</span></span>

<span data-ttu-id="97950-123">Hvis du vil opprette en CSS-overstyringsfil, kan du bruke et hvilket som helst integrert utviklingsmiljø (IDE), tekstredigeringsprogram eller redigeringsprogram for kildekode.</span><span class="sxs-lookup"><span data-stu-id="97950-123">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="97950-124">En typisk fremgangsmåte er å bruke standard Web-feilsøkere i webleseren til å identifisere stilvelgere, egenskaper og verdier på det eksisterende området.</span><span class="sxs-lookup"><span data-stu-id="97950-124">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="97950-125">I de fleste weblesere kan du endre verdier og forhåndsvise dem i feilsøkingsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="97950-125">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="97950-126">Når du har identifisert endringene du vil gjøre, kan du lagre dem i din egen CSS-fil.</span><span class="sxs-lookup"><span data-stu-id="97950-126">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="97950-127">Last opp en CSS-overstyringsfil</span><span class="sxs-lookup"><span data-stu-id="97950-127">Upload a CSS override file</span></span>

<span data-ttu-id="97950-128">Hvis du vil laste opp en CSS-fil til webområdet ditt i Commerce, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="97950-128">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="97950-129">Gå til området ditt i redigeringsverktøyet.</span><span class="sxs-lookup"><span data-stu-id="97950-129">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="97950-130">Velg **Utforming** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="97950-130">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="97950-131">Avhengig av hvilken versjon av redigeringsverktøyene for handel du bruker, må du kanskje utvide **Innstillinger** i navigasjonsruten før du kan velge **Utforming**.</span><span class="sxs-lookup"><span data-stu-id="97950-131">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="97950-132">Øverst i hovedutformingsruten velger du **CSS-overstyring**-kategorien, hvis den ikke allerede er valgt.</span><span class="sxs-lookup"><span data-stu-id="97950-132">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="97950-133">Under **Tilgjengelige CSS-ovestyringer** velger du **Last opp CSS-fil**.</span><span class="sxs-lookup"><span data-stu-id="97950-133">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="97950-134">Et Filutforsker-vindu vises.</span><span class="sxs-lookup"><span data-stu-id="97950-134">A File Explorer window appears.</span></span>
1. <span data-ttu-id="97950-135">Bla til og velg en CSS-fil i Filutforsker, og velg deretter **Åpne**</span><span class="sxs-lookup"><span data-stu-id="97950-135">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="97950-136">Den opplastede CSS-filen vises nå under **Tilgjengelige CSS-overstyringer**.</span><span class="sxs-lookup"><span data-stu-id="97950-136">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="97950-137">Forhåndsvise en CSS-overstyringsfil</span><span class="sxs-lookup"><span data-stu-id="97950-137">Preview a CSS override file</span></span>

<span data-ttu-id="97950-138">Hvis du vil forhåndsvise en CSS-overstyringsfil før du gjør den aktiv på det aktive området, følger du fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="97950-138">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="97950-139">I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil forhåndsvise.</span><span class="sxs-lookup"><span data-stu-id="97950-139">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="97950-140">Ved siden av CSS-filnavnet velger du **Forhåndsvis område**.</span><span class="sxs-lookup"><span data-stu-id="97950-140">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="97950-141">I dialogboksen **Velg en URL-adresse** velger du URL-adressen for området du vil bruke overstyring for, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="97950-141">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="97950-142">Hvis det finnes flere varianter for den valgte URL-adressen, velger du den ønskede varianten i dialogboksen **Forhåndsvisningsvarianter** som vises.</span><span class="sxs-lookup"><span data-stu-id="97950-142">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="97950-143">En ny nettleserfane eller et nytt vindu åpnes, der du kan validere stiloverstyringer mot området.</span><span class="sxs-lookup"><span data-stu-id="97950-143">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="97950-144">Du kan deretter dele URL-adressen med andre godkjente Commerce-brukere for gjennomgang og tilbakemelding.</span><span class="sxs-lookup"><span data-stu-id="97950-144">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="97950-145">Aktivere en CSS-overstyringsfil på det aktive webområdet</span><span class="sxs-lookup"><span data-stu-id="97950-145">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="97950-146">Når du har forhåndsvist og godkjent CSS-overstyringsfilen, kan du aktivere den på det aktive webområdet.</span><span class="sxs-lookup"><span data-stu-id="97950-146">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="97950-147">Bare én CSS-overstyringsfil kan være aktiv på området om gangen.</span><span class="sxs-lookup"><span data-stu-id="97950-147">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="97950-148">Hvis du aktiverer en ny overstyringsfil, deaktiveres den forrige overstyringsfilen.</span><span class="sxs-lookup"><span data-stu-id="97950-148">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="97950-149">Derfor må du kontrollere at alle nødvendige overstyringer er til stede i én enkelt CSS-overstyringsfil.</span><span class="sxs-lookup"><span data-stu-id="97950-149">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="97950-150">Hvis du vil aktivere en CSS-overstyringsfil, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="97950-150">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="97950-151">I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil aktivere.</span><span class="sxs-lookup"><span data-stu-id="97950-151">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="97950-152">Under CSS-filnavn velger du **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="97950-152">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="97950-153">Overstyringsfilen blir umiddelbart aktiv på det aktive nettstedet ditt.</span><span class="sxs-lookup"><span data-stu-id="97950-153">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="97950-154">Deaktivere en CSS-overstyringsfil på det aktive webområdet</span><span class="sxs-lookup"><span data-stu-id="97950-154">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="97950-155">Følg denne fremgangsmåten for å deaktivere en CSS-overstyringsfil på nettstedet ditt.</span><span class="sxs-lookup"><span data-stu-id="97950-155">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="97950-156">I navigasjonsruten til venstre velger du **Utforming**, og deretter, i kategorien **CSS-overstyring** under **Tilgjengelige CSS-overstyringer**, finner du CSS-filen du vil deaktivere.</span><span class="sxs-lookup"><span data-stu-id="97950-156">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="97950-157">Under CSS-filnavn velger du **Deaktiver**.</span><span class="sxs-lookup"><span data-stu-id="97950-157">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="97950-158">Overstyringsfilen blir umiddelbart inaktiv på det aktive nettstedet ditt.</span><span class="sxs-lookup"><span data-stu-id="97950-158">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="97950-159">Hvis du vil ha tilgang til flere alternativer for CSS-overstyringsfiler, velger du ellipsen (**...**) ved siden av CSS-filnavnet.</span><span class="sxs-lookup"><span data-stu-id="97950-159">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="97950-160">Alternativene **Last ned**, **Gi nytt navn** og **Erstatt** er nyttige for hurtigendringer i en eksisterende CSS-overstyringsfil.</span><span class="sxs-lookup"><span data-stu-id="97950-160">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97950-161">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="97950-161">Additional resources</span></span>

[<span data-ttu-id="97950-162">Legge til en logo</span><span class="sxs-lookup"><span data-stu-id="97950-162">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="97950-163">Velge et områdetema</span><span class="sxs-lookup"><span data-stu-id="97950-163">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="97950-164">Arbeide med forhåndsinnstillinger for stil</span><span class="sxs-lookup"><span data-stu-id="97950-164">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="97950-165">Legge til et favorittikon</span><span class="sxs-lookup"><span data-stu-id="97950-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="97950-166">Legge til en velkomstmelding</span><span class="sxs-lookup"><span data-stu-id="97950-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="97950-167">Legge til en opphavsrettserklæring</span><span class="sxs-lookup"><span data-stu-id="97950-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="97950-168">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="97950-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="97950-169">Legge til skript kode i områdes ID-er for å støtte telemetri</span><span class="sxs-lookup"><span data-stu-id="97950-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
