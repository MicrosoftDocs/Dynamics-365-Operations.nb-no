---
title: Administrere vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du administrerer vurderinger og omtaler ved hjelp Microsoft Dynamics 365 Commerce-sensurverktøyet for vurderinger og omtaler.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: e9becdce5ae36ac637043b9d0febfbbff2392aa9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698032"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="47bbc-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="47bbc-103">Manage ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="47bbc-104">Dette emnet forklarer hvordan du administrerer vurderinger og omtaler ved hjelp Microsoft Dynamics 365 Commerce-sensurverktøyet for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="47bbc-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="47bbc-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="47bbc-105">Overview</span></span>

<span data-ttu-id="47bbc-106">Dynamics 365 Commerce bruker Microsoft Azure Cognitive Service til å automatisk moderere vurderingstekst ved å fjerne upassende ord.</span><span class="sxs-lookup"><span data-stu-id="47bbc-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="47bbc-107">Dessuten kan moderatorer bruke sensurverktøyet for vurderinger og omtale til følgende manuelle oppgaver:</span><span class="sxs-lookup"><span data-stu-id="47bbc-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="47bbc-108">Sensurere omtaler ved å svare på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="47bbc-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="47bbc-109">Slette omtalene til en kunde på en kundens forespørsel.</span><span class="sxs-lookup"><span data-stu-id="47bbc-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="47bbc-110">Masseimportere vurderings- og omtaledata for alle produkter i en Microsoft Power BI-mal, slik at tendenser for vurderinger og omtaler kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="47bbc-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="47bbc-111">Lese en omtale</span><span class="sxs-lookup"><span data-stu-id="47bbc-111">Read a review</span></span> 

1. <span data-ttu-id="47bbc-112">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-112">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47bbc-113">Bruk søkefeltet øverst til høyre på siden for å filtrere omtalene som vises etter produkt-ID, produktnavn eller omtaletekst.</span><span class="sxs-lookup"><span data-stu-id="47bbc-113">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="47bbc-114">Flere filtre gjør at du kan begrense omtalene etter periode, rangering, kanal eller betydning (fjernet, svart på eller rapportert).</span><span class="sxs-lookup"><span data-stu-id="47bbc-114">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for sensur](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="47bbc-116">Svare på en omtale</span><span class="sxs-lookup"><span data-stu-id="47bbc-116">Respond to a review</span></span> 

<span data-ttu-id="47bbc-117">Noen ganger kan kunder som kjøpte et produkt, uttrykke tilfredshet eller misnøye, eller de forstår ikke hvordan de kan bruke produktet.</span><span class="sxs-lookup"><span data-stu-id="47bbc-117">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="47bbc-118">Som moderator kan du legge inn et svar på en omtale.</span><span class="sxs-lookup"><span data-stu-id="47bbc-118">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="47bbc-119">Dette svaret vises sammen med omtalen på området.</span><span class="sxs-lookup"><span data-stu-id="47bbc-119">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="47bbc-120">Følg denne fremgangsmåten for å svare på en omtale.</span><span class="sxs-lookup"><span data-stu-id="47bbc-120">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="47bbc-121">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-121">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47bbc-122">Finn og velg omtalen som krever et svar.</span><span class="sxs-lookup"><span data-stu-id="47bbc-122">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="47bbc-123">Velg **Legg til et svar** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="47bbc-123">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="47bbc-124">Skriv inn svarteksten og navnet som skal vises for svareren.</span><span class="sxs-lookup"><span data-stu-id="47bbc-124">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="47bbc-125">Standard svarnavn er **Moderator**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-125">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="47bbc-126">Når du er ferdig, velg du **Legg inn svar**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-126">When you've finished, select **Post response**.</span></span>

![Svare på en omtale](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="47bbc-128">Fjerne en omtale</span><span class="sxs-lookup"><span data-stu-id="47bbc-128">Take down a review</span></span> 

<span data-ttu-id="47bbc-129">Noen ganger er det en forretningsmessig begrunnelse for at moderatorer fjerner omtaler fra kunder.</span><span class="sxs-lookup"><span data-stu-id="47bbc-129">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="47bbc-130">Følg denne fremgangsmåten for å fjerne en omtale.</span><span class="sxs-lookup"><span data-stu-id="47bbc-130">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="47bbc-131">Gå til **Hjem \> Omtaler \> Sensur**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-131">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47bbc-132">Finn og velg gjennomgangen som må fjernes.</span><span class="sxs-lookup"><span data-stu-id="47bbc-132">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="47bbc-133">Velg en årsak til fjerningen i egenskapsruten til høyre, og velg **Fjern**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-133">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="47bbc-134">Slette omtalene til en kunde på en kundens forespørsel</span><span class="sxs-lookup"><span data-stu-id="47bbc-134">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="47bbc-135">Noen ganger vil kundene ha sine data for vurderinger og omtaler slettet for godt fra et webområde for e-handel.</span><span class="sxs-lookup"><span data-stu-id="47bbc-135">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="47bbc-136">En moderator som mottar en forespørsel om fjerning fra en kunde, kan fjerne kundens data ved hjelp av funksjonen for omtalesletting.</span><span class="sxs-lookup"><span data-stu-id="47bbc-136">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="47bbc-137">Hvis du vil finne og slette en kundes data, krever moderator e-postadressen som kunden brukte til å logge på og gi omtaler.</span><span class="sxs-lookup"><span data-stu-id="47bbc-137">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="47bbc-138">Følg denne fremgangsmåten for å finne og slette kundedata.</span><span class="sxs-lookup"><span data-stu-id="47bbc-138">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="47bbc-139">Gå til **Hjem \> Omtaler \> Slett**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-139">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="47bbc-140">I feltet **Søk etter brukere etter e-postadresse** angir du kundens e-postadresse, og deretter velger du **Søk**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-140">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="47bbc-141">Hvis kunden har omtaleaktivitet (for eksempel innsending av omtaler, stemmer om nyttigheten til en annen kundes omtale eller merknader om en annen kundes omtale), vises resultatene.</span><span class="sxs-lookup"><span data-stu-id="47bbc-141">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="47bbc-142">For hvert element er det en **Slett**-knapp.</span><span class="sxs-lookup"><span data-stu-id="47bbc-142">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="47bbc-143">Velg **Slett**for hvert element som må slettes.</span><span class="sxs-lookup"><span data-stu-id="47bbc-143">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="47bbc-144">Velg **Ja** når du blir bedt om å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="47bbc-144">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="47bbc-146">Det kan ta opptil sju dager før data blir fjernet fra systemet.</span><span class="sxs-lookup"><span data-stu-id="47bbc-146">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="47bbc-147">Moderatorer bør varsle kunder om denne forsinkelsen.</span><span class="sxs-lookup"><span data-stu-id="47bbc-147">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="47bbc-148">Hvis kundene har endret navnet sitt i kontoinnstillingene, kan flere elementer vises i søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="47bbc-148">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="47bbc-149">I dette tilfellet må moderatoren velge **Slett** for hvert element for å slette kundens data fullstendig.</span><span class="sxs-lookup"><span data-stu-id="47bbc-149">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="47bbc-150">Laste ned data om vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="47bbc-150">Download ratings and reviews data</span></span>

<span data-ttu-id="47bbc-151">Sensurverktøyet for vurderinger og omtaler gjør det mulig for moderatorer å importere vurderinger og omtaler i bulk, slik at de kan analysere trender.</span><span class="sxs-lookup"><span data-stu-id="47bbc-151">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="47bbc-152">En Power BI-mal som inneholder grunnleggende mål, er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="47bbc-152">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="47bbc-153">Moderatorer kan bruke denne malen til å koble sammen masseimporterte data og vise et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="47bbc-153">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="47bbc-154">De trenger ikke opprette et egendefinert instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="47bbc-154">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="47bbc-155">Moderatorer kan tilpasse Power BI-malen slik at den dekker sine spesielle behov.</span><span class="sxs-lookup"><span data-stu-id="47bbc-155">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="47bbc-156">Følg denne fremgangsmåten for å laste ned data for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="47bbc-156">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="47bbc-157">Gå til **Hjem \> Omtaler \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-157">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="47bbc-158">Velg **Last ned omtaledata** for å laste ned data om vurderinger og omtaler i CSV-format (kommadelte verdier).</span><span class="sxs-lookup"><span data-stu-id="47bbc-158">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="47bbc-159">Vise trenger for vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="47bbc-159">View ratings and reviews trends</span></span>

<span data-ttu-id="47bbc-160">Moderatorer kan laste ned Power BI-malen, slik at de kan vise tendenser på et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="47bbc-160">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="47bbc-161">Følg denne fremgangsmåten for å vise trender for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="47bbc-161">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="47bbc-162">Gå til **Hjem \> Omtaler \> Rapportering**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-162">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="47bbc-163">Velg **PowerBI-mal** for å laste ned malen.</span><span class="sxs-lookup"><span data-stu-id="47bbc-163">Select **PowerBI template** to download the template.</span></span>

    ![Laste ned Power BI-malen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="47bbc-165">Åpne den nedlastede malen ved hjelp av Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="47bbc-165">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="47bbc-166">Lukk dialogboksen **Tilgang til webinnhold** som vises, og lukk deretter "Oppdater"-feilmeldingen som vises.</span><span class="sxs-lookup"><span data-stu-id="47bbc-166">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="47bbc-167">Gå til **Hjem**, velg **Rediger spørringer**, og velg deretter **Innstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-167">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="47bbc-168">Velg **Endre kilde** i dialogboksen **Innstillinger for datakilde**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-168">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="47bbc-169">I feltet **URL** angir du banen til omtaledataene du lastet ned i forrige prosedyre (for eksempel **c:\\reviews\\ReviewsData.csv**).</span><span class="sxs-lookup"><span data-stu-id="47bbc-169">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-felt i dialogboks for kommadelte verdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="47bbc-171">Velg **OK**, og velg deretter **Bruk endringer**.</span><span class="sxs-lookup"><span data-stu-id="47bbc-171">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="47bbc-172">Det vil ta ett til to minutter å bruke endringene i datakilden.</span><span class="sxs-lookup"><span data-stu-id="47bbc-172">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="47bbc-173">Velg **Trendark** for å vise trender for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="47bbc-173">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trender for vurderinger og omtaler](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="47bbc-175">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="47bbc-175">Additional resources</span></span>

[<span data-ttu-id="47bbc-176">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="47bbc-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="47bbc-177">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="47bbc-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="47bbc-178">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="47bbc-178">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="47bbc-179">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="47bbc-179">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
