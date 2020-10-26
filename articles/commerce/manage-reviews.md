---
title: Administrere vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du behandler vurderinger og omtaler i Microsoft Dynamics 365 Commerce-områdebygger.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
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
ms.openlocfilehash: 3fc88bc5a5868dce7c0539bf3f0ddc5b751e7b75
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974012"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="c0332-103">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c0332-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0332-104">Dette emnet forklarer hvordan du behandler vurderinger og omtaler i Microsoft Dynamics 365 Commerce-områdebygger.</span><span class="sxs-lookup"><span data-stu-id="c0332-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c0332-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c0332-105">Overview</span></span>

<span data-ttu-id="c0332-106">Dynamics 365 Commerce bruker Microsoft Azure Cognitive Service til å automatisk moderere vurderingstekst ved å fjerne upassende ord.</span><span class="sxs-lookup"><span data-stu-id="c0332-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="c0332-107">I tillegg kan moderatorer bruke Dynamics 365 Commerce-områdebygger til å implementere følgende manuelle oppgaver:</span><span class="sxs-lookup"><span data-stu-id="c0332-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="c0332-108">Sensurere omtaler ved å svare på dem eller fjerne dem.</span><span class="sxs-lookup"><span data-stu-id="c0332-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="c0332-109">Slette omtalene til en kunde på en kundens forespørsel.</span><span class="sxs-lookup"><span data-stu-id="c0332-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="c0332-110">Masseimportere vurderings- og omtaledata for alle produkter i en Microsoft Power BI-mal, slik at tendenser for vurderinger og omtaler kan analyseres.</span><span class="sxs-lookup"><span data-stu-id="c0332-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="c0332-111">Lese en omtale</span><span class="sxs-lookup"><span data-stu-id="c0332-111">Read a review</span></span> 

<span data-ttu-id="c0332-112">Gjør følgende for å lese en omtale i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-113">Gå til **Hjem \> Omtaler \> Sensur** .</span><span class="sxs-lookup"><span data-stu-id="c0332-113">Go to **Home \> Reviews \> Moderation** .</span></span>
1. <span data-ttu-id="c0332-114">Bruk søkefeltet øverst til høyre på siden for å filtrere omtalene som vises etter produkt-ID, produktnavn eller omtaletekst.</span><span class="sxs-lookup"><span data-stu-id="c0332-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="c0332-115">Flere filtre gjør at du kan begrense omtalene etter periode, rangering, kanal eller betydning (fjernet, svart på eller rapportert).</span><span class="sxs-lookup"><span data-stu-id="c0332-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Startside for sensur](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="c0332-117">Svare på en omtale</span><span class="sxs-lookup"><span data-stu-id="c0332-117">Respond to a review</span></span> 

<span data-ttu-id="c0332-118">Noen ganger kan kunder som kjøpte et produkt, uttrykke tilfredshet eller misnøye, eller de forstår ikke hvordan de kan bruke produktet.</span><span class="sxs-lookup"><span data-stu-id="c0332-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="c0332-119">Som moderator kan du legge inn et svar på en omtale.</span><span class="sxs-lookup"><span data-stu-id="c0332-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="c0332-120">Dette svaret vises sammen med omtalen på området.</span><span class="sxs-lookup"><span data-stu-id="c0332-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="c0332-121">Gjør følgende for å svare på en omtale i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-122">Gå til **Hjem \> Omtaler \> Sensur** .</span><span class="sxs-lookup"><span data-stu-id="c0332-122">Go to **Home \> Reviews \> Moderation** .</span></span>
1. <span data-ttu-id="c0332-123">Finn og velg omtalen som krever et svar.</span><span class="sxs-lookup"><span data-stu-id="c0332-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="c0332-124">Velg **Legg til et svar** i egenskapsruten til høyre.</span><span class="sxs-lookup"><span data-stu-id="c0332-124">In the properties pane on the right, select **Add a response** .</span></span>
1. <span data-ttu-id="c0332-125">Skriv inn svarteksten og navnet som skal vises for svareren.</span><span class="sxs-lookup"><span data-stu-id="c0332-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="c0332-126">Standard svarnavn er **Moderator** .</span><span class="sxs-lookup"><span data-stu-id="c0332-126">The default responder name is **Moderator** .</span></span>
1. <span data-ttu-id="c0332-127">Når du er ferdig, velg du **Legg inn svar** .</span><span class="sxs-lookup"><span data-stu-id="c0332-127">When you've finished, select **Post response** .</span></span>

![Svare på en omtale](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="c0332-129">Fjerne en omtale</span><span class="sxs-lookup"><span data-stu-id="c0332-129">Take down a review</span></span> 

<span data-ttu-id="c0332-130">Noen ganger er det en forretningsmessig begrunnelse for at moderatorer fjerner omtaler fra kunder.</span><span class="sxs-lookup"><span data-stu-id="c0332-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="c0332-131">Gjør følgende for å fjerne en omtale i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-132">Gå til **Hjem \> Omtaler \> Sensur** .</span><span class="sxs-lookup"><span data-stu-id="c0332-132">Go to **Home \> Reviews \> Moderation** .</span></span>
1. <span data-ttu-id="c0332-133">Finn og velg gjennomgangen som må fjernes.</span><span class="sxs-lookup"><span data-stu-id="c0332-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="c0332-134">Velg en årsak til fjerningen under **Fjern omtale** , og velg deretter **Fjern** .</span><span class="sxs-lookup"><span data-stu-id="c0332-134">In the properties pane on the right, select a takedown reason under **Takedown Review** , and then select **Take down** .</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="c0332-135">Slette omtalene til en kunde på en kundens forespørsel</span><span class="sxs-lookup"><span data-stu-id="c0332-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="c0332-136">Noen ganger vil kundene ha sine data for vurderinger og omtaler slettet for godt fra et webområde for e-handel.</span><span class="sxs-lookup"><span data-stu-id="c0332-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="c0332-137">En moderator som mottar en forespørsel om fjerning fra en kunde, kan fjerne kundens data ved hjelp av funksjonen for omtalesletting.</span><span class="sxs-lookup"><span data-stu-id="c0332-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="c0332-138">Hvis du vil finne og slette en kundes data, krever moderator e-postadressen som kunden brukte til å logge på og gi omtaler.</span><span class="sxs-lookup"><span data-stu-id="c0332-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="c0332-139">Gjør følgende for å finne og slette kundedata i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-140">Gå til **Hjem \> Omtaler \> Slett** .</span><span class="sxs-lookup"><span data-stu-id="c0332-140">Go to **Home \> Reviews \> Delete** .</span></span>
1. <span data-ttu-id="c0332-141">I boksen **Søk etter brukere etter e-postadresse** angir du kundens e-postadresse, og deretter velger du **Søk** .</span><span class="sxs-lookup"><span data-stu-id="c0332-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search** .</span></span>
1. <span data-ttu-id="c0332-142">Hvis kunden har omtaleaktivitet (for eksempel innsending av omtaler, stemmer om nyttigheten til en annen kundes omtale eller merknader om en annen kundes omtale), vises resultatene.</span><span class="sxs-lookup"><span data-stu-id="c0332-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="c0332-143">For hvert element er det en **Slett** -knapp.</span><span class="sxs-lookup"><span data-stu-id="c0332-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="c0332-144">Velg **Slett** for hvert element som må slettes.</span><span class="sxs-lookup"><span data-stu-id="c0332-144">For each item that must be deleted, select **Delete** .</span></span> <span data-ttu-id="c0332-145">Velg **Ja** når du blir bedt om å bekrefte.</span><span class="sxs-lookup"><span data-stu-id="c0332-145">When you're prompted for confirmation, select **Yes** .</span></span> 
    
![Slette kundedata](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="c0332-147">Det kan ta opptil sju dager før data blir fjernet fra systemet.</span><span class="sxs-lookup"><span data-stu-id="c0332-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="c0332-148">Moderatorer bør varsle kunder om denne forsinkelsen.</span><span class="sxs-lookup"><span data-stu-id="c0332-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="c0332-149">Hvis kundene har endret navnet sitt i kontoinnstillingene, kan flere elementer vises i søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="c0332-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="c0332-150">I dette tilfellet må moderatoren velge **Slett** for hvert element for å slette kundens data fullstendig.</span><span class="sxs-lookup"><span data-stu-id="c0332-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="c0332-151">Laste ned data om vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="c0332-151">Download ratings and reviews data</span></span>

<span data-ttu-id="c0332-152">Commerce-områdebygger lar moderatorer å importere vurderinger og omtaler i gruppe, slik at de kan analysere trender.</span><span class="sxs-lookup"><span data-stu-id="c0332-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="c0332-153">En Power BI-mal som inneholder grunnleggende mål, er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="c0332-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="c0332-154">Moderatorer kan bruke denne malen til å koble sammen masseimporterte data og vise et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="c0332-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="c0332-155">De trenger ikke opprette et egendefinert instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="c0332-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="c0332-156">Moderatorer kan tilpasse Power BI-malen slik at den dekker sine spesielle behov.</span><span class="sxs-lookup"><span data-stu-id="c0332-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="c0332-157">Gjør følgende for å laste ned vurderinger og omtaler i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-158">Gå til **Hjem \> Omtaler \> Rapportering** .</span><span class="sxs-lookup"><span data-stu-id="c0332-158">Go to **Home \> Reviews \> Reporting** .</span></span>
1. <span data-ttu-id="c0332-159">Velg **Last ned omtaledata** for å laste ned data om vurderinger og omtaler i CSV-format (kommadelte verdier).</span><span class="sxs-lookup"><span data-stu-id="c0332-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="c0332-160">Vise trenger for vurderinger og omtaler</span><span class="sxs-lookup"><span data-stu-id="c0332-160">View ratings and reviews trends</span></span>

<span data-ttu-id="c0332-161">Moderatorer kan laste ned Power BI-malen, slik at de kan vise tendenser på et instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="c0332-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="c0332-162">Gjør følgende for å vise trender for vurderinger og omtaler i Commerce-områdebygger:</span><span class="sxs-lookup"><span data-stu-id="c0332-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c0332-163">Gå til **Hjem \> Omtaler \> Rapportering** .</span><span class="sxs-lookup"><span data-stu-id="c0332-163">Go to **Home \> Reviews \> Reporting** .</span></span>
1. <span data-ttu-id="c0332-164">Velg **PowerBI-mal** for å laste ned malen.</span><span class="sxs-lookup"><span data-stu-id="c0332-164">Select **PowerBI template** to download the template.</span></span>

    ![Last ned Power BI-malen](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="c0332-166">Åpne den nedlastede malen ved hjelp av Power BI-appen.</span><span class="sxs-lookup"><span data-stu-id="c0332-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="c0332-167">Lukk dialogboksen **Tilgang til webinnhold** som vises, og lukk deretter "Oppdater"-feilmeldingen som vises.</span><span class="sxs-lookup"><span data-stu-id="c0332-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="c0332-168">Gå til **Hjem** , velg **Rediger spørringer** , og velg deretter **Innstillinger for datakilde** .</span><span class="sxs-lookup"><span data-stu-id="c0332-168">Go to **Home** , select **Edit queries** , and then select **Data source settings** .</span></span>
1. <span data-ttu-id="c0332-169">Velg **Endre kilde** i dialogboksen **Innstillinger for datakilde** .</span><span class="sxs-lookup"><span data-stu-id="c0332-169">In the **Data source settings** dialog box, select **Change Source** .</span></span>
1. <span data-ttu-id="c0332-170">I feltet **URL** angir du banen til omtaledataene du lastet ned i forrige prosedyre (for eksempel **c:\\reviews\\ReviewsData.csv** ).</span><span class="sxs-lookup"><span data-stu-id="c0332-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv** ).</span></span>

    ![URL-felt i dialogboks for kommadelte verdier](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="c0332-172">Velg **OK** , og velg deretter **Bruk endringer** .</span><span class="sxs-lookup"><span data-stu-id="c0332-172">Select **OK** , and then select **Apply changes** .</span></span> <span data-ttu-id="c0332-173">Det vil ta ett til to minutter å bruke endringene i datakilden.</span><span class="sxs-lookup"><span data-stu-id="c0332-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="c0332-174">Velg **Trendark** for å vise trender for vurderinger og omtaler.</span><span class="sxs-lookup"><span data-stu-id="c0332-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Trender for vurderinger og omtaler](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="c0332-176">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c0332-176">Additional resources</span></span>

[<span data-ttu-id="c0332-177">Oversikt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c0332-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c0332-178">Velge å bruke vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c0332-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c0332-179">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="c0332-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="c0332-180">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="c0332-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
