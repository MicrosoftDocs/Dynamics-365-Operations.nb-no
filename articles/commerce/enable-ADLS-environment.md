---
title: Aktivere ADLS i et Dynamics 365 Commerce-miljø
description: Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.
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
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ba428765babb9ca7566da7a457368959b1c29083
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259754"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="ea93e-103">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="ea93e-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea93e-104">Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="ea93e-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="ea93e-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="ea93e-105">Overview</span></span>

<span data-ttu-id="ea93e-106">I Dynamics 365 Commerce-løsningen spores all produkt- og transaksjonsinformasjon i miljøets enhetslager.</span><span class="sxs-lookup"><span data-stu-id="ea93e-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="ea93e-107">Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen 2-løsning (ADLS).</span><span class="sxs-lookup"><span data-stu-id="ea93e-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="ea93e-108">Når ADLS er konfigurert i et miljø, blir alle nødvendige data gjenspeilet fra enhetslageret samtidig som de fremdeles beskyttes og er under kundens kontroll.</span><span class="sxs-lookup"><span data-stu-id="ea93e-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="ea93e-109">Hvis produktanbefalinger eller tilpassede anbefalinger også er aktivert i miljøet, får produktanbefalingsstakken tilgang til den dedikerte mappen i ADLS for å hente kundens data og beregne anbefalinger basert på dem.</span><span class="sxs-lookup"><span data-stu-id="ea93e-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ea93e-110">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="ea93e-110">Prerequisites</span></span>

<span data-ttu-id="ea93e-111">Kunder må ha ADLS konfigurert i et Azure-abonnement som de eier.</span><span class="sxs-lookup"><span data-stu-id="ea93e-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="ea93e-112">Dette emnet dekker ikke kjøpet av et Azure-abonnement eller oppsettet av en ADLS-aktivert lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="ea93e-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="ea93e-113">Hvis du vil ha mer informasjon om ADLS, kan du se [Offentlig ADLS-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="ea93e-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="ea93e-114">Konfigurasjonstrinn</span><span class="sxs-lookup"><span data-stu-id="ea93e-114">Configuration steps</span></span>

<span data-ttu-id="ea93e-115">Denne delen dekker konfigurasjonstrinnene som er nødvendige for å aktivere ADLS i et miljø som er knyttet til produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="ea93e-115">This section covers the configuration steps necessary for enabling ADLS in an environment as it relates to product recommendations.</span></span>
<span data-ttu-id="ea93e-116">Hvis du vil ha en mer detaljert oversikt over trinnene som kreves for å aktivere ADLS, kan du se [Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="ea93e-116">For a more in-depth overview of the steps required to enable ADLS, see [Make entity store available as a Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="ea93e-117">Aktivere ADLS i miljøet</span><span class="sxs-lookup"><span data-stu-id="ea93e-117">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="ea93e-118">Logg deg på miljøets administrasjonskontorportal.</span><span class="sxs-lookup"><span data-stu-id="ea93e-118">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="ea93e-119">Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="ea93e-119">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="ea93e-120">Sett **Aktiver Data Lake-integrasjon** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ea93e-120">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="ea93e-121">Sett **Oppdater Data Lake fordelt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ea93e-121">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="ea93e-122">Deretter angir du følgende påkrevd informasjon:</span><span class="sxs-lookup"><span data-stu-id="ea93e-122">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="ea93e-123">**Applikasjons-ID** // **Applikasjonshemmelighet** // **DNS-navn** – Nødvendig for å koble til KeyVault der ADLS-hemmeligheten er lagret.</span><span class="sxs-lookup"><span data-stu-id="ea93e-123">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="ea93e-124">**Hemmelig navn** – Det hemmelige navnet som er lagret i KeyVault, og som brukes til å autentisere med ADLS.</span><span class="sxs-lookup"><span data-stu-id="ea93e-124">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="ea93e-125">Lagre endringene i sidens øvre venstre hjørne.</span><span class="sxs-lookup"><span data-stu-id="ea93e-125">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="ea93e-126">Bildet nedenfor viser et eksempel på en ADLS-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="ea93e-126">The following image shows an example ADLS configuration.</span></span>

![Eksempel på ADLS-konfigurasjon](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="ea93e-128">Test ADLS-tilkoblingen</span><span class="sxs-lookup"><span data-stu-id="ea93e-128">Test the ADLS connection</span></span>

1. <span data-ttu-id="ea93e-129">Test tilkoblingen til KeyVault ved hjelp av **Test Azure Key Vault**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="ea93e-129">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="ea93e-130">Test tilkoblingen til ADLS ved hjelp av **Test Azure Storage**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="ea93e-130">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="ea93e-131">Hvis testene mislykkes, dobbeltsjekker du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="ea93e-131">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="ea93e-132">Når tilkoblingstestene er vellykket, må du aktivere automatisk oppdatering for enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="ea93e-132">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="ea93e-133">Hvis du vil aktivere automatisk oppdatering for enhetslager, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="ea93e-133">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="ea93e-134">Søk etter **Enhetslager**.</span><span class="sxs-lookup"><span data-stu-id="ea93e-134">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="ea93e-135">I listen til venstre navigerer du til **RetailSales**-oppføringen og velger **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="ea93e-135">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="ea93e-136">Forsikre deg om at **Automatisk oppdatering aktivert** er satt til **Ja**, velg **Oppdater**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ea93e-136">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="ea93e-137">Det følgende bildet viser et eksempel på et enhetslager der automatisk oppdatering er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ea93e-137">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Eksempel på enhetslager med automatisk oppdatering aktivert](./media/exampleADLSConfig2.png)

<span data-ttu-id="ea93e-139">ADLS er nå konfigurert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="ea93e-139">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="ea93e-140">Hvis de ikke er fullført allerede, følger du trinnene for å [aktivere produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.</span><span class="sxs-lookup"><span data-stu-id="ea93e-140">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea93e-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ea93e-141">Additional resources</span></span>

[<span data-ttu-id="ea93e-142">Gjøre enhetslager tilgjengelig som Data Lake</span><span class="sxs-lookup"><span data-stu-id="ea93e-142">Make entity store available as a data lake</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[<span data-ttu-id="ea93e-143">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ea93e-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ea93e-144">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ea93e-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ea93e-145">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ea93e-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ea93e-146">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ea93e-146">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ea93e-147">Legge til produktanbefalinger i POS</span><span class="sxs-lookup"><span data-stu-id="ea93e-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ea93e-148">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="ea93e-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ea93e-149">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="ea93e-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ea93e-150">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="ea93e-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ea93e-151">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="ea93e-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ea93e-152">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ea93e-152">Product recommendations FAQ</span></span>](faq-recommendations.md)
