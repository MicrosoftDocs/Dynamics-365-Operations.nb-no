---
title: Administrere robots.txt-filer
description: Dette emnet beskriver hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ce49f2968030ca4656a01c7646819c01635e12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003493"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="f2710-103">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="f2710-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f2710-104">Dette emnet beskriver hvordan du administrerer robots.txt-filer i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f2710-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f2710-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="f2710-105">Overview</span></span>

<span data-ttu-id="f2710-106">Robotutelukkelsestandarden, eller robots.txt, er en standard som nettsteder bruker for å kommunisere med Web-roboter.</span><span class="sxs-lookup"><span data-stu-id="f2710-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="f2710-107">Den instruerer Web-roboter om alle områder av et nettsted som ikke bør besøkes.</span><span class="sxs-lookup"><span data-stu-id="f2710-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="f2710-108">Roboter brukes ofte av søkemotorer til å indeksere nettsteder.</span><span class="sxs-lookup"><span data-stu-id="f2710-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="f2710-109">Hvis du vil utelate roboter fra en server, oppretter du en fil på serveren.</span><span class="sxs-lookup"><span data-stu-id="f2710-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="f2710-110">I denne filen angir du en tilgangspolicy for roboter.</span><span class="sxs-lookup"><span data-stu-id="f2710-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="f2710-111">Filen må være tilgjengelig via HTTP på den lokale URL-adressen **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="f2710-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="f2710-112">Robots.txt-filen hjelper søkemotorene med å indeksere innholdet på nettstedet ditt.</span><span class="sxs-lookup"><span data-stu-id="f2710-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="f2710-113">Dynamics 365 Commerce lar deg laste opp en robots. txt-fil for domenet ditt.</span><span class="sxs-lookup"><span data-stu-id="f2710-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="f2710-114">For hvert domene i Commerce-miljøet kan du laste opp én robots. txt-fil og knytte den til dette domenet.</span><span class="sxs-lookup"><span data-stu-id="f2710-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="f2710-115">Hvis du vil ha mer informasjon om robots.txt-filen, kan du gå til [siden Web-roboter](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="f2710-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="f2710-116">Laste opp en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="f2710-116">Upload a robots.txt file</span></span>

<span data-ttu-id="f2710-117">Etter at du har opprettet og redigert robots.txt-filen i henhold til [robotutelukkelsestandarden](https://www.robotstxt.org/orig.html), må du kontrollere at filen er tilgjengelig på datamaskinen der du skal bruke verktøyene for handelsredigering.</span><span class="sxs-lookup"><span data-stu-id="f2710-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="f2710-118">Filen må hete **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="f2710-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="f2710-119">For best resultat må den være i formatet som er notert i standarden.</span><span class="sxs-lookup"><span data-stu-id="f2710-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="f2710-120">Hver Commerce-kunde er ansvarlig for å validere og vedlikeholde innholdet i robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="f2710-121">Hvis du vil laste opp en robots.txt-fil, må du være logget på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="f2710-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="f2710-122">Hvis du vil laste opp en robots.txt-fil i Commerce, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f2710-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f2710-123">Logg på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="f2710-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f2710-124">I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="f2710-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f2710-125">Velg **robots.txt** under **Leierinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f2710-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f2710-126">En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.</span><span class="sxs-lookup"><span data-stu-id="f2710-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f2710-127">Velg **Administrer** for å laste opp en robots.txt-fil for et domene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="f2710-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f2710-128">På menyen til høyre velger du **Last opp**-knappen (pilen som peker oppover) ved siden av domenet som er knyttet til robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f2710-129">En filleser-dialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="f2710-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="f2710-130">I dialogboksen blar du til og velger robots.txt-filen du vil laste opp for det tilknyttede domenet, og deretter velger du **Åpne** for å fullføre opplastingen.</span><span class="sxs-lookup"><span data-stu-id="f2710-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2710-131">Under opplasting kontrollerer Commerce at filen er en tekstfil, men den validerer ikke innholdet i filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="f2710-132">Laste ned en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="f2710-132">Download a robots.txt file</span></span>

<span data-ttu-id="f2710-133">Hvis du vil laste ned en robots.txt-fil i Commerce, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f2710-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f2710-134">Logg på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="f2710-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f2710-135">I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="f2710-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f2710-136">Velg **robots.txt** under **Leierinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f2710-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f2710-137">En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.</span><span class="sxs-lookup"><span data-stu-id="f2710-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f2710-138">Velg **Administrer** for å laste ned en robots.txt-fil for et domene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="f2710-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f2710-139">På menyen til høyre velger du **Last ned**-knappen (pilen som peker nedover) ved siden av domenet som er knyttet til robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f2710-140">En filleser-dialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="f2710-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="f2710-141">I dialogboksen går du til ønsket plassering på den lokale stasjonen, bekrefter eller skriver inn et filnavn, og deretter velger du **Lagre** for å fullføre nedlastingen.</span><span class="sxs-lookup"><span data-stu-id="f2710-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="f2710-142">Denne fremgangsmåten kan brukes til å laste ned bare robots.txt-filer som tidligere ble lastet opp via redigeringsverktøyene for handel.</span><span class="sxs-lookup"><span data-stu-id="f2710-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="f2710-143">Slette en robots.txt-fil</span><span class="sxs-lookup"><span data-stu-id="f2710-143">Delete a robots.txt file</span></span>

<span data-ttu-id="f2710-144">Hvis du vil slette en robots.txt-fil i Commerce, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="f2710-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f2710-145">Logg på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="f2710-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f2710-146">I den venstre navigasjonsruten velger **Leierinnstillinger** (ved siden av tannhjulsymbolet) for å utvide den.</span><span class="sxs-lookup"><span data-stu-id="f2710-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f2710-147">Velg **robots.txt** under **Leierinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f2710-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f2710-148">En liste over alle domenene som er knyttet til miljøet ditt, vises i hoveddelen av vinduet.</span><span class="sxs-lookup"><span data-stu-id="f2710-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f2710-149">Velg **Administrer** for å slette en robots.txt-fil for et domene i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="f2710-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f2710-150">På menyen til høyre velger du **Slett**-knappen (papirkurvsymbolet) ved siden av domenet som er knyttet til robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f2710-151">Et filleser-vindu vises.</span><span class="sxs-lookup"><span data-stu-id="f2710-151">A file browser window appears.</span></span>
6. <span data-ttu-id="f2710-152">I filleser-vinduet blar du til og velger robots.txt-filen du vil slette for domenet, og deretter velger du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="f2710-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="f2710-153">En advarselsboks vises.</span><span class="sxs-lookup"><span data-stu-id="f2710-153">A warning message box appears.</span></span>
7. <span data-ttu-id="f2710-154">I meldingsboksen velger du **Slett** for å bekrefte slettingen av robots.txt-filen.</span><span class="sxs-lookup"><span data-stu-id="f2710-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="f2710-155">Denne fremgangsmåten kan brukes til å slette bare robots.txt-filer som tidligere ble lastet opp via redigeringsverktøyene for handel.</span><span class="sxs-lookup"><span data-stu-id="f2710-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2710-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f2710-156">Additional resources</span></span>

[<span data-ttu-id="f2710-157">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="f2710-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f2710-158">Distribuere et nytt e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="f2710-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f2710-159">Opprette et e-handelsområde</span><span class="sxs-lookup"><span data-stu-id="f2710-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f2710-160">Knytte et nettområde til en kanal</span><span class="sxs-lookup"><span data-stu-id="f2710-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f2710-161">Definere egendefinerte sider for brukerpålogginger</span><span class="sxs-lookup"><span data-stu-id="f2710-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f2710-162">Legge til støtte for et innholdsleveringsnettverk (CDN)</span><span class="sxs-lookup"><span data-stu-id="f2710-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f2710-163">Aktivere stedsbasert butikkregistrering</span><span class="sxs-lookup"><span data-stu-id="f2710-163">Enable location-based store detection</span></span>](enable-store-detection.md)
