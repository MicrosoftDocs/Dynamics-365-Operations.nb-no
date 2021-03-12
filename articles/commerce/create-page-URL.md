---
title: Opprette en URL-adresse for side
description: Dette emnet dekker de grunnleggende konseptene og prosedyrene for oppretting av en URL-adresse på området.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 062a49df93e442dbe402ac9a78244c966958aaa2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965259"
---
# <a name="create-a-page-url"></a><span data-ttu-id="e83d8-103">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="e83d8-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e83d8-104">Dette emnet dekker de grunnleggende konseptene og prosedyrene for oppretting av en URL-adresse på området.</span><span class="sxs-lookup"><span data-stu-id="e83d8-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="e83d8-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e83d8-105">Overview</span></span>

<span data-ttu-id="e83d8-106">Den fullstendige eller absolutte URL-adressen som peker til en side på området, består av forskjellige deler.</span><span class="sxs-lookup"><span data-stu-id="e83d8-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="e83d8-107">For eksempel har URL-adressen `https://www.contoso.com/en-us/contactus` følgende deler:</span><span class="sxs-lookup"><span data-stu-id="e83d8-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="e83d8-108">`https://www.contoso.com` – HTTP-protokollen og områdedomenet.</span><span class="sxs-lookup"><span data-stu-id="e83d8-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="e83d8-109">`/en-us` – Områdets språkbane.</span><span class="sxs-lookup"><span data-stu-id="e83d8-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="e83d8-110">`/contactus` – Den relative URL-adressen til siden **Kontakt oss**.</span><span class="sxs-lookup"><span data-stu-id="e83d8-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="e83d8-111">En relativ URL-adresse kalles også en URL-*plassholder*.</span><span class="sxs-lookup"><span data-stu-id="e83d8-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="e83d8-112">Du bestemmer områdets domene og valgfri språkbane når du konfigurerer området.</span><span class="sxs-lookup"><span data-stu-id="e83d8-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="e83d8-113">Du kan legge til flere domener og språkbaner til området via nettbutikkens side i områdeinnstillingene.</span><span class="sxs-lookup"><span data-stu-id="e83d8-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="e83d8-114">URL-plassholderen for en side finnes som en frittstående enhet i sideredigeringsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="e83d8-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="e83d8-115">En URL-adresse for side består av to deler: et navn som representerer URL-plassholderen, og en peker til en side på området eller et eksternt område.</span><span class="sxs-lookup"><span data-stu-id="e83d8-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="e83d8-116">En URL-adresse for side kan også konfigureres til å fungere som en omadressering til en annen side, enten på området eller på et eksternt område.</span><span class="sxs-lookup"><span data-stu-id="e83d8-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="e83d8-117">Opprette en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="e83d8-117">Create a page URL</span></span>

<span data-ttu-id="e83d8-118">Det finnes to måter å opprette side-URL-adresser på:</span><span class="sxs-lookup"><span data-stu-id="e83d8-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="e83d8-119">Automatisk når du oppretter en side</span><span class="sxs-lookup"><span data-stu-id="e83d8-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="e83d8-120">Manuelt fra siden **URL-adresser**</span><span class="sxs-lookup"><span data-stu-id="e83d8-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="e83d8-121">Opprette en URL-adresse for side når du oppretter en side</span><span class="sxs-lookup"><span data-stu-id="e83d8-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="e83d8-122">Hvis du angir et navn i feltet **URL-adresse** når du oppretter en ny side, opprettes det automatisk en side-URL-adresse som peker til denne siden på siden **URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="e83d8-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="e83d8-123">Når du har publisert URL-adressen og siden den peker til, kan brukere av området (kundene) få tilgang til siden som er knyttet til URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="e83d8-124">Hvis du publiserer en URL-adresse uten å publisere siden den peker til, mottar områdebrukere en 404-feil når de prøver å få tilgang til siden.</span><span class="sxs-lookup"><span data-stu-id="e83d8-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="e83d8-125">Hvis du publiserer en side uten å publisere URL-adressen som peker til den, får du ikke tilgang til siden ved hjelp av en URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e83d8-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="e83d8-126">Opprette en URL-adresse for side manuelt</span><span class="sxs-lookup"><span data-stu-id="e83d8-126">Manually create a page URL</span></span>

<span data-ttu-id="e83d8-127">Når du oppretter nye sider, trenger du ikke angi en URL-adresse for side.</span><span class="sxs-lookup"><span data-stu-id="e83d8-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="e83d8-128">Hvis du lar URL-feltet være tomt, opprettes siden i en ikke-koblet tilstand.</span><span class="sxs-lookup"><span data-stu-id="e83d8-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="e83d8-129">I så fall får ikke kundene tilgang til siden, selv om den er publisert.</span><span class="sxs-lookup"><span data-stu-id="e83d8-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="e83d8-130">Hvis du vil at siden skal være tilgjengelig, må du manuelt opprette URL-adressen og koble den til siden.</span><span class="sxs-lookup"><span data-stu-id="e83d8-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="e83d8-131">Hvis du vil opprette side-URL-adressen manuelt for en side, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e83d8-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="e83d8-132">Velg **Ny** på siden **URL-adresser**.</span><span class="sxs-lookup"><span data-stu-id="e83d8-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="e83d8-133">Velg områdesiden som URL-adressen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="e83d8-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="e83d8-134">Angi URL-plassholderen, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e83d8-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="e83d8-135">På dette tidspunktet er URL-adressen i utkasttilstand.</span><span class="sxs-lookup"><span data-stu-id="e83d8-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="e83d8-136">Den må publiseres før områdebrukere kan få tilgang til den tilknyttede siden.</span><span class="sxs-lookup"><span data-stu-id="e83d8-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="e83d8-137">Oppdatere en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="e83d8-137">Update a page URL</span></span>

<span data-ttu-id="e83d8-138">Hvis du vil oppdatere målsiden til en side-URL-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e83d8-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="e83d8-139">På siden **URL-adresser** velger du URL-adressen som skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="e83d8-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="e83d8-140">I egenskapsruten til høyre velger du ellipseknappen (**...**) ved siden av målsidefeltet.</span><span class="sxs-lookup"><span data-stu-id="e83d8-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="e83d8-141">I dialogboksen velger du en annen side, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="e83d8-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="e83d8-142">Lagre og publiser URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="e83d8-143">Omadressere en URL-adresse for side</span><span class="sxs-lookup"><span data-stu-id="e83d8-143">Redirect a page URL</span></span>

<span data-ttu-id="e83d8-144">Noen ganger kan det hende at du vil at kundene skal vise en annen side når de ber om en bestemt URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e83d8-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="e83d8-145">I disse tilfellene er beste og enkleste fremgangsmåte ofte å endre siden som URL-adressen peker til.</span><span class="sxs-lookup"><span data-stu-id="e83d8-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="e83d8-146">Du kan imidlertid ha legitime årsaker til å bruke HTTP 301- eller 3023-omadresseringer for å omadressere forespørsler for en URL-adresse til en annen URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e83d8-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="e83d8-147">Hvis du vil omadressere en URL-adresse til en annen URL-adresse, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="e83d8-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="e83d8-148">På siden **URL-adresser** velger du URL-adressen som skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="e83d8-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="e83d8-149">Deretter velger du **Omadresser** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="e83d8-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="e83d8-150">Velg en destinasjon for omadresseringen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="e83d8-151">Hvis du vil peke til en annen side på området, velger du **Intern URL-adresse** og deretter ellipseknappen (**...**), og velg deretter URL-adressen det skal omadresseres til.</span><span class="sxs-lookup"><span data-stu-id="e83d8-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="e83d8-152">Hvis du vil peke til en side på det eksterne området, velger du **Ekstern URL**, og deretter angir du full URL-adresse for denne siden.</span><span class="sxs-lookup"><span data-stu-id="e83d8-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="e83d8-153">Husk å ta med protokollen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-153">Be sure to include the protocol.</span></span> <span data-ttu-id="e83d8-154">Skriv for eksempel inn `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="e83d8-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="e83d8-155">Hvis URL-adressen allerede omadresseres til en intern URL-adresse, må du velge **Fjern utvalg** før du kan angi en ekstern URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="e83d8-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="e83d8-156">Velg en omadresseringstype:</span><span class="sxs-lookup"><span data-stu-id="e83d8-156">Select a redirect type:</span></span>

    - <span data-ttu-id="e83d8-157">**Permanent omadressering (301)** – Velg dette alternativet når du vet at innholdet flyttes permanent og ikke går tilbake til den forrige URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="e83d8-158">Søkemotorer tilordner verdien for søkemotoroptimaliseringen for URL-adressen for omadressering til URL-adressen som det omadresseres til, og oppdaterer oppføringen slik at den viser den nye URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="e83d8-159">**Midlertidig omadressering (302)** – Velg dette alternativet for å omadressere trafikk uten å oppdatere søkemotorer.</span><span class="sxs-lookup"><span data-stu-id="e83d8-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="e83d8-160">Denne fremgangsmåten brukes vanligvis hvis innholdet vil gå snart tilbake til den forrige URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="e83d8-161">Når du er klar til å implementere omadresseringen, må du lagre og publisere URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="e83d8-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e83d8-162">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e83d8-162">Additional resources</span></span>

[<span data-ttu-id="e83d8-163">Tilpasse områdenavigering</span><span class="sxs-lookup"><span data-stu-id="e83d8-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="e83d8-164">Legg til en ny områdeside</span><span class="sxs-lookup"><span data-stu-id="e83d8-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e83d8-165">Konfigurere domenenavnet</span><span class="sxs-lookup"><span data-stu-id="e83d8-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e83d8-166">Legge til språk på området</span><span class="sxs-lookup"><span data-stu-id="e83d8-166">Add languages to your site</span></span>](add-languages-to-site.md)
