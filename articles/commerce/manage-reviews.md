---
title: Administrere vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du administrerer vurderinger og omtaler ved hjelp Microsoft Dynamics 365 Commerce-sensurverktøyet for vurderinger og omtaler.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027248"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="942e8-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="942e8-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="942e8-104">Dette emnet forklarer hvordan du administrerer vurderinger og omtaler ved hjelp Microsoft Dynamics 365 Commerce-sensurverktøyet for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="942e8-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="942e8-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="942e8-105">Overview</span></span>

<span data-ttu-id="942e8-106">Dynamics 365 Commerce bruker Microsoft Azure Cognitive Service til å automatisk moderere vurderingstekst ved å fjerne upassende ord.</span><span class="sxs-lookup"><span data-stu-id="942e8-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="942e8-107">Dessuten kan moderatorer bruke sensurverktøyet for vurderinger og omtale til følgende manuelle oppgaver:</span><span class="sxs-lookup"><span data-stu-id="942e8-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="942e8-108">Sensurere omtaler ved å svare på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="942e8-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="942e8-109">Slette omtalene til en kunde på en kundens forespørsel.</span><span class="sxs-lookup"><span data-stu-id="942e8-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="942e8-110">Masseimportere vurderings- og omtaledata for alle produkter i en Microsoft Power BI-mal, slik at tendenser for vurderinger og omtaler kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="942e8-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="942e8-111">Få tilgang til funksjoner for sensur av rangeringer og vurderinger</span><span class="sxs-lookup"><span data-stu-id="942e8-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="942e8-112">For å få tilgang til sensurfunksjoner for rangeringer og vurderinger i administrasjonsverktøyet for e-handelsområdet gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="942e8-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="942e8-113">Logg på [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="942e8-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="942e8-114">Åpne prosjektet som inneholder miljøet der du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="942e8-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="942e8-115">Velg miljøet i delen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="942e8-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="942e8-116">Klikk **Detaljhandelsstyring** under **Miljøfunksjoner**.</span><span class="sxs-lookup"><span data-stu-id="942e8-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="942e8-117">I kategorien **E-handel** under **Koblinger** velger du **Administrasjonsverktøy for e-handelsområde**.</span><span class="sxs-lookup"><span data-stu-id="942e8-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="942e8-118">Lese en omtale</span><span class="sxs-lookup"><span data-stu-id="942e8-118">Read a review</span></span> 

1. <span data-ttu-id="942e8-119">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="942e8-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="942e8-120">Bruk søkefeltet øverst til høyre på siden for å filtrere omtalene som vises etter produkt-ID, produktnavn eller omtaletekst.</span><span class="sxs-lookup"><span data-stu-id="942e8-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="942e8-121">Flere filtre gjør at du kan begrense omtalene etter periode, rangering, kanal eller betydning (fjernet, svart på eller rapportert).</span><span class="sxs-lookup"><span data-stu-id="942e8-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for sensur](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="942e8-123">Svare på en omtale</span><span class="sxs-lookup"><span data-stu-id="942e8-123">Respond to a review</span></span> 

<span data-ttu-id="942e8-124">Noen ganger kan kunder som kjøpte et produkt, uttrykke tilfredshet eller misnøye, eller de forstår ikke hvordan de kan bruke produktet.</span><span class="sxs-lookup"><span data-stu-id="942e8-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="942e8-125">Som moderator kan du legge inn et svar på en omtale.</span><span class="sxs-lookup"><span data-stu-id="942e8-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="942e8-126">Dette svaret vises sammen med omtalen på området.</span><span class="sxs-lookup"><span data-stu-id="942e8-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="942e8-127">Følg denne fremgangsmåten for å svare på en omtale.</span><span class="sxs-lookup"><span data-stu-id="942e8-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="942e8-128">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="942e8-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="942e8-129">Finn og velg omtalen som krever et svar.</span><span class="sxs-lookup"><span data-stu-id="942e8-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="942e8-130">Velg **Legg til et svar** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="942e8-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="942e8-131">Skriv inn svarteksten og navnet som skal vises for svareren.</span><span class="sxs-lookup"><span data-stu-id="942e8-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="942e8-132">Standard svarnavn er **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="942e8-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="942e8-133">Når du er ferdig, velg du **Legg inn svar**.</span><span class="sxs-lookup"><span data-stu-id="942e8-133">When you've finished, select **Post response**.</span></span>

![Svare på en omtale](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="942e8-135">Fjerne en omtale</span><span class="sxs-lookup"><span data-stu-id="942e8-135">Take down a review</span></span> 

<span data-ttu-id="942e8-136">Noen ganger er det en forretningsmessig begrunnelse for at moderatorer fjerner omtaler fra kunder.</span><span class="sxs-lookup"><span data-stu-id="942e8-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="942e8-137">Følg denne fremgangsmåten for å fjerne en omtale.</span><span class="sxs-lookup"><span data-stu-id="942e8-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="942e8-138">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="942e8-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="942e8-139">Finn og velg gjennomgangen som må fjernes.</span><span class="sxs-lookup"><span data-stu-id="942e8-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="942e8-140">Velg en årsak til fjerningen i egenskapsruten til høyre, og velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="942e8-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="942e8-141">Slette omtalene til en kunde på en kundens forespørsel</span><span class="sxs-lookup"><span data-stu-id="942e8-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="942e8-142">Noen ganger vil kundene ha sine data for vurderinger og omtaler slettet for godt fra et webområde for e-handel.</span><span class="sxs-lookup"><span data-stu-id="942e8-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="942e8-143">En moderator som mottar en forespørsel om fjerning fra en kunde, kan fjerne kundens data ved hjelp av funksjonen for omtalesletting.</span><span class="sxs-lookup"><span data-stu-id="942e8-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="942e8-144">Hvis du vil finne og slette en kundes data, krever moderator e-postadressen som kunden brukte til å logge på og gi omtaler.</span><span class="sxs-lookup"><span data-stu-id="942e8-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="942e8-145">Følg denne fremgangsmåten for å finne og slette kundedata.</span><span class="sxs-lookup"><span data-stu-id="942e8-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="942e8-146">Gå til **Hjem \> Omtaler \> Slett**.</span><span class="sxs-lookup"><span data-stu-id="942e8-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="942e8-147">I feltet **Søk etter brukere etter e-postadresse** angir du kundens e-postadresse, og deretter velger du **Søk**.</span><span class="sxs-lookup"><span data-stu-id="942e8-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="942e8-148">Hvis kunden har omtaleaktivitet (for eksempel innsending av omtaler, stemmer om nyttigheten til en annen kundes omtale eller merknader om en annen kundes omtale), vises resultatene.</span><span class="sxs-lookup"><span data-stu-id="942e8-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="942e8-149">For hvert element er det en **Slett**-knapp.</span><span class="sxs-lookup"><span data-stu-id="942e8-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="942e8-150">Velg **Slett**for hvert element som må slettes.</span><span class="sxs-lookup"><span data-stu-id="942e8-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="942e8-151">Velg **Ja** når du blir bedt om å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="942e8-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="942e8-153">Det kan ta opptil sju dager før data blir fjernet fra systemet.</span><span class="sxs-lookup"><span data-stu-id="942e8-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="942e8-154">Moderatorer bør varsle kunder om denne forsinkelsen.</span><span class="sxs-lookup"><span data-stu-id="942e8-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="942e8-155">Hvis kundene har endret navnet sitt i kontoinnstillingene, kan flere elementer vises i søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="942e8-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="942e8-156">I dette tilfellet må moderatoren velge **Slett** for hvert element for å slette kundens data fullstendig.</span><span class="sxs-lookup"><span data-stu-id="942e8-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="942e8-157">Laste ned data om vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="942e8-157">Download ratings and reviews data</span></span>

<span data-ttu-id="942e8-158">Sensurverktøyet for vurderinger og omtaler gjør det mulig for moderatorer å importere vurderinger og omtaler i bulk, slik at de kan analysere trender.</span><span class="sxs-lookup"><span data-stu-id="942e8-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="942e8-159">En Power BI-mal som inneholder grunnleggende mål, er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="942e8-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="942e8-160">Moderatorer kan bruke denne malen til å koble sammen masseimporterte data og vise et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="942e8-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="942e8-161">De trenger ikke opprette et egendefinert instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="942e8-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="942e8-162">Moderatorer kan tilpasse Power BI-malen slik at den dekker sine spesielle behov.</span><span class="sxs-lookup"><span data-stu-id="942e8-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="942e8-163">Følg denne fremgangsmåten for å laste ned data for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="942e8-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="942e8-164">Gå til **Hjem \> Omtaler \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="942e8-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="942e8-165">Velg **Last ned omtaledata** for å laste ned data om vurderinger og omtaler i CSV-format (kommadelte verdier).</span><span class="sxs-lookup"><span data-stu-id="942e8-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="942e8-166">Vise trenger for vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="942e8-166">View ratings and reviews trends</span></span>

<span data-ttu-id="942e8-167">Moderatorer kan laste ned Power BI-malen, slik at de kan vise tendenser på et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="942e8-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="942e8-168">Følg denne fremgangsmåten for å vise trender for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="942e8-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="942e8-169">Gå til **Hjem \> Omtaler \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="942e8-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="942e8-170">Velg **PowerBI-mal** for å laste ned malen.</span><span class="sxs-lookup"><span data-stu-id="942e8-170">Select **PowerBI template** to download the template.</span></span>

    ![Laste ned Power BI-malen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="942e8-172">Åpne den nedlastede malen ved hjelp av Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="942e8-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="942e8-173">Lukk dialogboksen **Tilgang til webinnhold** som vises, og lukk deretter "Oppdater"-feilmeldingen som vises.</span><span class="sxs-lookup"><span data-stu-id="942e8-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="942e8-174">Gå til **Hjem**, velg **Rediger spørringer**, og velg deretter **Innstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="942e8-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="942e8-175">Velg **Endre kilde** i dialogboksen **Innstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="942e8-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="942e8-176">I feltet **URL** angir du banen til omtaledataene du lastet ned i forrige prosedyre (for eksempel **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="942e8-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-felt i dialogboks for kommadelte verdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="942e8-178">Velg **OK**, og velg deretter **Bruk endringer**.</span><span class="sxs-lookup"><span data-stu-id="942e8-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="942e8-179">Det vil ta ett til to minutter å bruke endringene i datakilden.</span><span class="sxs-lookup"><span data-stu-id="942e8-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="942e8-180">Velg **Trendark** for å vise trender for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="942e8-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trender for vurderinger og omtaler](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="942e8-182">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="942e8-182">Additional resources</span></span>

[<span data-ttu-id="942e8-183">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="942e8-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="942e8-184">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="942e8-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="942e8-185">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="942e8-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="942e8-186">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="942e8-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
