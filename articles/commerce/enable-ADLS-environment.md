---
title: Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø
description: Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5887ae7983fd817a929a185327671b301808b354
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478242"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="a4a2f-103">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="a4a2f-103">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4a2f-104">Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-104">This topic explains how to enable and test Azure Data Lake Storage for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

<span data-ttu-id="a4a2f-105">I Dynamics 365 Commerce-løsningen spores all produkt- og transaksjonsinformasjon i miljøets enhetslager.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-105">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="a4a2f-106">Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen 2-løsning.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-106">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 solution.</span></span>

<span data-ttu-id="a4a2f-107">Når Azure Data Lake Storage er konfigurert i et miljø, blir alle nødvendige data gjenspeilet fra enhetslageret samtidig som de fremdeles beskyttes og er under kundens kontroll.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-107">As Azure Data Lake Storage is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="a4a2f-108">Hvis produktanbefalinger eller tilpassede anbefalinger også er aktivert i miljøet, får produktanbefalingsstakken tilgang til den dedikerte mappen i Azure Data Lake Storage for å hente kundens data og beregne anbefalinger basert på dem.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-108">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in Azure Data Lake Storage to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a4a2f-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-109">Prerequisites</span></span>

<span data-ttu-id="a4a2f-110">Kunder må ha Azure Data Lake Storage konfigurert i et Azure-abonnement som de eier.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-110">Customers need to have Azure Data Lake Storage configured in an Azure subscription that they own.</span></span> <span data-ttu-id="a4a2f-111">Dette emnet dekker ikke kjøpet av et Azure-abonnement eller oppsettet av en Azure Data Lake Storage-aktivert lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-111">This topic does not cover the purchase of an Azure subscription or the setup of an Azure Data Lake Storage-enabled storage account.</span></span>

<span data-ttu-id="a4a2f-112">Hvis du vil ha mer informasjon om Azure Data Lake Storage, kan du se [Offentlig Azure Data Lake Storage Gen2-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="a4a2f-112">For more information about Azure Data Lake Storage, see [Azure Data Lake Storage Gen2 official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="a4a2f-113">Konfigurasjonstrinn</span><span class="sxs-lookup"><span data-stu-id="a4a2f-113">Configuration steps</span></span>

<span data-ttu-id="a4a2f-114">Denne delen dekker konfigurasjonstrinnene som er nødvendige for å aktivere Azure Data Lake Storage i et miljø som er knyttet til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-114">This section covers the configuration steps necessary for enabling Azure Data Lake Storage in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="a4a2f-115">Hvis du vil ha en mer detaljert oversikt over trinnene som kreves for å aktivere Azure Data Lake Storage, kan du se [Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="a4a2f-115">For a more in-depth overview of the steps required to enable Azure Data Lake Storage, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-azure-data-lake-storage-in-the-environment"></a><span data-ttu-id="a4a2f-116">Aktivere Azure Data Lake Storage i miljøet</span><span class="sxs-lookup"><span data-stu-id="a4a2f-116">Enable Azure Data Lake Storage in the environment</span></span>

1. <span data-ttu-id="a4a2f-117">Logg deg på miljøets administrasjonskontorportal.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="a4a2f-118">Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="a4a2f-119">Sett **Aktiver Data Lake-integrasjon** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="a4a2f-120">Sett **Oppdater Data Lake fordelt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="a4a2f-121">Deretter angir du følgende påkrevd informasjon:</span><span class="sxs-lookup"><span data-stu-id="a4a2f-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="a4a2f-122">**Applikasjons-ID** // **Applikasjonshemmelighet** // **DNS-navn** – Nødvendig for å koble til KeyVault der Azure Data Lake Storage-hemmeligheten er lagret.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the Azure Data Lake Storage secret is stored.</span></span>
    1. <span data-ttu-id="a4a2f-123">**Hemmelig navn** – Det hemmelige navnet som er lagret i KeyVault, og som brukes til å autentisere med Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with Azure Data Lake Storage.</span></span>
1. <span data-ttu-id="a4a2f-124">Lagre endringene i sidens øvre venstre hjørne.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="a4a2f-125">Bildet nedenfor viser et eksempel på en Azure Data Lake Storage-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-125">The following image shows an example Azure Data Lake Storage configuration.</span></span>

![Eksempel på Azure Data Lake Storage-konfigurasjon](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a><span data-ttu-id="a4a2f-127">Test Azure Data Lake Storage-tilkoblingen</span><span class="sxs-lookup"><span data-stu-id="a4a2f-127">Test the Azure Data Lake Storage connection</span></span>

1. <span data-ttu-id="a4a2f-128">Test tilkoblingen til KeyVault ved hjelp av **Test Azure Key Vault**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="a4a2f-129">Test tilkoblingen til Azure Data Lake Storage ved hjelp av **Test Azure Storage**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-129">Test the connection to Azure Data Lake Storage using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="a4a2f-130">Hvis testene mislykkes, dobbeltsjekker du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="a4a2f-131">Når tilkoblingstestene er vellykket, må du aktivere automatisk oppdatering for enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="a4a2f-132">Hvis du vil aktivere automatisk oppdatering for enhetslager, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="a4a2f-133">Søk etter **Enhetslager**.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="a4a2f-134">I listen til venstre navigerer du til **RetailSales**-oppføringen og velger **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="a4a2f-135">Forsikre deg om at **Automatisk oppdatering aktivert** er satt til **Ja**, velg **Oppdater**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="a4a2f-136">Det følgende bildet viser et eksempel på et enhetslager der automatisk oppdatering er aktivert.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Eksempel på enhetslager med automatisk oppdatering aktivert](./media/exampleADLSConfig2.png)

<span data-ttu-id="a4a2f-138">Azure Data Lake Storage er nå konfigurert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-138">Azure Data Lake Storage is now configured for the environment.</span></span> 

<span data-ttu-id="a4a2f-139">Hvis de ikke er fullført allerede, følger du trinnene for å [aktivere produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.</span><span class="sxs-lookup"><span data-stu-id="a4a2f-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4a2f-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a4a2f-140">Additional resources</span></span>

[<span data-ttu-id="a4a2f-141">Gjøre enhetslager tilgjengelig som Data Lake</span><span class="sxs-lookup"><span data-stu-id="a4a2f-141">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="a4a2f-142">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a4a2f-143">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a4a2f-144">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-144">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a4a2f-145">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-145">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a4a2f-146">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a4a2f-147">Legge til produktanbefalinger på salgssted</span><span class="sxs-lookup"><span data-stu-id="a4a2f-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a4a2f-148">Legge til anbefalinger i transaksjonsskjermbildet</span><span class="sxs-lookup"><span data-stu-id="a4a2f-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a4a2f-149">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="a4a2f-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a4a2f-150">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="a4a2f-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a4a2f-151">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="a4a2f-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a4a2f-152">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a4a2f-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
