---
title: Velge bort personlige produktanbefalinger
description: Dette emnet beskriver hvordan du kan la kundene velge bort mottak av personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025270"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="e7512-103">Velge bort personlige produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e7512-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7512-104">Dette emnet beskriver hvordan du kan la kundene velge bort mottak av personlige anbefalinger i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7512-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7512-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="e7512-105">Overview</span></span>

<span data-ttu-id="e7512-106">Under kontooppretting konfigureres nye kunder automatisk for å motta personlige anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="e7512-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="e7512-107">Dynamics 365 Commerce har imidlertid flere metoder som forhandlere kan bruke til å la brukere velge bort mottak av disse anbefalingene og begrense behandlingen av sine personlige data.</span><span class="sxs-lookup"><span data-stu-id="e7512-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="e7512-108">Godkjente brukere som velger bort mottak av personlige anbefalinger, vil umiddelbart stoppe å se personlige lister.</span><span class="sxs-lookup"><span data-stu-id="e7512-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="e7512-109">I tillegg vil alle personlige data som samles inn for personlig tilpasning, bli fjernet fra tilpassede anbefalingsmodeller.</span><span class="sxs-lookup"><span data-stu-id="e7512-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="e7512-110">Hvis du vil ha mer informasjon om tilpassede produktanbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e7512-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="e7512-111">Måter som forhandlere kan bruke til å implementere mulighet for brukere å velge bort ting</span><span class="sxs-lookup"><span data-stu-id="e7512-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="e7512-112">Forhandlere kan implementere mulighet for brukere å velge bort ting på tre måter.</span><span class="sxs-lookup"><span data-stu-id="e7512-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="e7512-113">Velge bort på vegne av brukeren</span><span class="sxs-lookup"><span data-stu-id="e7512-113">Opting out on behalf of users</span></span>

<span data-ttu-id="e7512-114">I Kontobehandling i Commerce-administrasjonskontoret kan forhandlere velge bort på vegne av brukeren.</span><span class="sxs-lookup"><span data-stu-id="e7512-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="e7512-115">Fra startsiden til administrasjonskontoret søker du etter **alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="e7512-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="e7512-116">Søk etter og velg en kunde, og velg deretter hurtigfanen **Detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="e7512-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Hurtigfanen Detaljhandel](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="e7512-118">Under **Personvern** angir du alternativet **Deaktiver tilpassing** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e7512-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Personverninnstillinger](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="e7512-120">Velg **Lagre**, og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e7512-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="e7512-121">Modulbasert bortvalgsopplevelse</span><span class="sxs-lookup"><span data-stu-id="e7512-121">Module-based opt-out experience</span></span>

<span data-ttu-id="e7512-122">Forhandlere kan la godkjente brukere velge bort personlige anbefalinger selv.</span><span class="sxs-lookup"><span data-stu-id="e7512-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="e7512-123">Hvis du vil gi denne bortvalgsopplevelsen, legger du til en bortvalgsmodul for brukerne på profilsidene for kundekontoer.</span><span class="sxs-lookup"><span data-stu-id="e7512-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="e7512-124">Egendefinerte tillegg</span><span class="sxs-lookup"><span data-stu-id="e7512-124">Custom extensions</span></span>

<span data-ttu-id="e7512-125">Forhandlere kan opprette egne tillegg for å administrere bortvalgsopplevelsen for brukere.</span><span class="sxs-lookup"><span data-stu-id="e7512-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="e7512-126">Hvis du vil ha mer informasjon, kan du se [Kalle API-er for Retail Server](e-commerce-extensibility/call-retail-server-apis.md) og [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7512-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="e7512-127">Få tak i en digital kopi av personlige anbefalingsdata på vegne av en godkjent bruker</span><span class="sxs-lookup"><span data-stu-id="e7512-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="e7512-128">Kunder vil kanskje skaffe en seg digital kopi av sine personlige opplysninger og også se en eksportert visning av anbefalingsresultatene.</span><span class="sxs-lookup"><span data-stu-id="e7512-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="e7512-129">Hvis en kunde ber om denne informasjonen, må forhandleren opprette en egendefinert utvidelse som kaller API-et for Retail Server og spør etter det fullstendige resultatet fra listen **Plukkinger for deg**, basert på kundens kunde-ID.</span><span class="sxs-lookup"><span data-stu-id="e7512-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="e7512-130">Resultatene kan deretter eksporteres i CSV-format (kommadelte verdier) og deles med kunden.</span><span class="sxs-lookup"><span data-stu-id="e7512-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="e7512-131">Følgende eksempel viser hvordan en forhandler kan utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="e7512-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="e7512-132">Forhandleren oppretter en egendefinert utvidelse for å hente personlige anbefalingsdata på vegne av brukeren.</span><span class="sxs-lookup"><span data-stu-id="e7512-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="e7512-133">Hvis du vil ha informasjon om hvordan du oppretter moduler, kloner eksisterende moduler, kaller API-er for Retail Server og kaller datahandlinger, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7512-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="e7512-134">Den egendefinerte utvidelsen foretar et kall til kjernedatahandlingen **get-recommendations** og sender den nødvendige informasjonen til den, basert på kravene i listen.</span><span class="sxs-lookup"><span data-stu-id="e7512-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="e7512-135">Når det gjelder listen **Plukkinger for deg**, må utvidelsen sende riktig listenavn og kunde-ID til datahandlingen.</span><span class="sxs-lookup"><span data-stu-id="e7512-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="e7512-136">En måte å opprette den egendefinerte utvidelsen på er å klone den eksisterende produktsamlingsmodulen som brukes til å returnere anbefalingsresultater.</span><span class="sxs-lookup"><span data-stu-id="e7512-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="e7512-137">Ved å klone denne eksisterende modulen kan en forhandler endre den eksisterende koden og legge til en ny knapp som eksporterer anbefalingsresultatene til en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="e7512-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="e7512-138">Hvis du vil ha mer informasjon, kan du se [Klone en startsettmodul](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7512-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="e7512-139">For en fullstendig visning av API-biblioteket for Retail Server, se [Kunde- og forbruker-API-er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="e7512-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="e7512-140">Når den egendefinerte utvidelsen er opprettet, kan forhandleren eksportere en CSV-fil av alle anbefalingsresultatene, basert på den unike kunde-ID-en til den godkjente brukeren.</span><span class="sxs-lookup"><span data-stu-id="e7512-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="e7512-141">Forhandleren kan dele den eksporterte CSV-filen som inneholder den fullstendige, tilpassede listen over anbefalte produkter, med den godkjente brukeren.</span><span class="sxs-lookup"><span data-stu-id="e7512-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7512-142">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e7512-142">Additional resources</span></span>

[<span data-ttu-id="e7512-143">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e7512-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e7512-144">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="e7512-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e7512-145">Aktivere tilpassede anbefalinger</span><span class="sxs-lookup"><span data-stu-id="e7512-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e7512-146">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="e7512-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="e7512-147">Legge til anbefalingspanel til POS-enheter</span><span class="sxs-lookup"><span data-stu-id="e7512-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e7512-148">Oversikt over produktsamlingsmodul</span><span class="sxs-lookup"><span data-stu-id="e7512-148">Product collection module overview</span></span>](product-collection-module-overview.md)