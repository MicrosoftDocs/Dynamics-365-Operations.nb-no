---
title: Aktivere ADLS i et Dynamics 365 Commerce-miljø
description: Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.
author: bebeale
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 068eb522bd44e02dd31d3337a051691a956637fc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025269"
---
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="0e847-103">Aktivere ADLS i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="0e847-103">Enable ADLS in a Dynamics 365 Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e847-104">Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.</span><span class="sxs-lookup"><span data-stu-id="0e847-104">This topic explains how to enable and test Azure Data Lake Storage (ADLS) for a Dynamics 365 Commerce environment, which is a prerequisite for enabling product recommendations.</span></span>

## <a name="overview"></a><span data-ttu-id="0e847-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0e847-105">Overview</span></span>

<span data-ttu-id="0e847-106">I Dynamics 365 Commerce-løsningen spores all produkt- og transaksjonsinformasjon i miljøets enhetslager.</span><span class="sxs-lookup"><span data-stu-id="0e847-106">In the Dynamics 365 Commerce solution, all product and transaction information is tracked in the environment's Entity store.</span></span> <span data-ttu-id="0e847-107">Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen 2-løsning (ADLS).</span><span class="sxs-lookup"><span data-stu-id="0e847-107">To make this data accessible to other Dynamics 365 services, such as data analytics, business intelligence, and personalized recommendations, it is necessary to connect the environment to a customer-owned Azure Data Lake Storage Gen 2 (ADLS) solution.</span></span>

<span data-ttu-id="0e847-108">Når ADLS er konfigurert i et miljø, blir alle nødvendige data gjenspeilet fra enhetslageret samtidig som de fremdeles beskyttes og er under kundens kontroll.</span><span class="sxs-lookup"><span data-stu-id="0e847-108">As ADLS is configured in an environment, all necessary data is mirrored from the Entity store while still being protected and under customer's control.</span></span>

<span data-ttu-id="0e847-109">Hvis produktanbefalinger eller tilpassede anbefalinger også er aktivert i miljøet, får produktanbefalingsstakken tilgang til den dedikerte mappen i ADLS for å hente kundens data og beregne anbefalinger basert på dem.</span><span class="sxs-lookup"><span data-stu-id="0e847-109">If product recommendations or personalized recommendations are also enabled in the environment, then the product recommendations stack will be granted access to the dedicated folder in ADLS to retrieve the customer’s data and compute recommendations based on it.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0e847-110">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="0e847-110">Prerequisites</span></span>

<span data-ttu-id="0e847-111">Kunder må ha ADLS konfigurert i et Azure-abonnement som de eier.</span><span class="sxs-lookup"><span data-stu-id="0e847-111">Customers need to have ADLS configured in an Azure subscription that they own.</span></span> <span data-ttu-id="0e847-112">Dette emnet dekker ikke kjøpet av et Azure-abonnement eller oppsettet av en ADLS-aktivert lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="0e847-112">This topic does not cover the purchase of an Azure subscription or the setup of an ADLS-enabled storage account.</span></span>

<span data-ttu-id="0e847-113">Hvis du vil ha mer informasjon om ADLS, kan du se [Offentlig ADLS-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).</span><span class="sxs-lookup"><span data-stu-id="0e847-113">For more information about ADLS, see [ADLS official documentation](https://azure.microsoft.com/pricing/details/storage/data-lake).</span></span>
  
## <a name="configuration-steps"></a><span data-ttu-id="0e847-114">Konfigurasjonstrinn</span><span class="sxs-lookup"><span data-stu-id="0e847-114">Configuration steps</span></span>

<span data-ttu-id="0e847-115">Dette avsnittet dekker de nødvendige konfigurasjonstrinnene for aktivering av ADLS i et miljø.</span><span class="sxs-lookup"><span data-stu-id="0e847-115">This section covers the configuration steps necessary for enabling ADLS in an environment.</span></span>

### <a name="enable-adls-in-the-environment"></a><span data-ttu-id="0e847-116">Aktivere ADLS i miljøet</span><span class="sxs-lookup"><span data-stu-id="0e847-116">Enable ADLS in the environment</span></span>

1. <span data-ttu-id="0e847-117">Logg deg på miljøets administrasjonskontorportal.</span><span class="sxs-lookup"><span data-stu-id="0e847-117">Log in to the environment's back office portal.</span></span>
1. <span data-ttu-id="0e847-118">Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="0e847-118">Search for **System Parameters** and navigate to the **Data connections** tab.</span></span> 
1. <span data-ttu-id="0e847-119">Sett **Aktiver Data Lake-integrasjon** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0e847-119">Set **Enable Data Lake integration** to **Yes**.</span></span>
1. <span data-ttu-id="0e847-120">Sett **Oppdater Data Lake fordelt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="0e847-120">Set **Trickle update Data Lake** to **Yes**.</span></span>
1. <span data-ttu-id="0e847-121">Deretter angir du følgende påkrevd informasjon:</span><span class="sxs-lookup"><span data-stu-id="0e847-121">Next, enter the following required information:</span></span>
    1. <span data-ttu-id="0e847-122">**Applikasjons-ID** // **Applikasjonshemmelighet** // **DNS-navn** – Nødvendig for å koble til KeyVault der ADLS-hemmeligheten er lagret.</span><span class="sxs-lookup"><span data-stu-id="0e847-122">**Application ID** // **Application Secret** // **DNS Name** - Needed to connect to KeyVault where the ADLS secret is stored.</span></span>
    1. <span data-ttu-id="0e847-123">**Hemmelig navn** – Det hemmelige navnet som er lagret i KeyVault, og som brukes til å autentisere med ADLS.</span><span class="sxs-lookup"><span data-stu-id="0e847-123">**Secret name** - The secret name stored in KeyVault and used to authenticate with ADLS.</span></span>
1. <span data-ttu-id="0e847-124">Lagre endringene i sidens øvre venstre hjørne.</span><span class="sxs-lookup"><span data-stu-id="0e847-124">Save your changes in the top left corner of the page.</span></span>

<span data-ttu-id="0e847-125">Bildet nedenfor viser et eksempel på en ADLS-konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="0e847-125">The following image shows an example ADLS configuration.</span></span>

![Eksempel på ADLS-konfigurasjon](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a><span data-ttu-id="0e847-127">Test ADLS-tilkoblingen</span><span class="sxs-lookup"><span data-stu-id="0e847-127">Test the ADLS connection</span></span>

1. <span data-ttu-id="0e847-128">Test tilkoblingen til KeyVault ved hjelp av **Test Azure Key Vault**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e847-128">Test the connection to KeyVault using the **Test Azure Key Vault** link.</span></span>
1. <span data-ttu-id="0e847-129">Test tilkoblingen til ADLS ved hjelp av **Test Azure Storage**-koblingen.</span><span class="sxs-lookup"><span data-stu-id="0e847-129">Test the connection to ADLS using the **Test Azure Storage** link.</span></span>

> [!NOTE]
> <span data-ttu-id="0e847-130">Hvis testene mislykkes, dobbeltsjekker du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.</span><span class="sxs-lookup"><span data-stu-id="0e847-130">If the tests fail, double-check that all of the KeyVault information added above is correct, then try again.</span></span>

<span data-ttu-id="0e847-131">Når tilkoblingstestene er vellykket, må du aktivere automatisk oppdatering for enhetslageret.</span><span class="sxs-lookup"><span data-stu-id="0e847-131">Once the connection tests are successful, you must enable automatic refresh for Entity store.</span></span>

<span data-ttu-id="0e847-132">Hvis du vil aktivere automatisk oppdatering for enhetslager, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0e847-132">To enable automatic refresh for Entity store, follow these steps.</span></span>

1. <span data-ttu-id="0e847-133">Søk etter **Enhetslager**.</span><span class="sxs-lookup"><span data-stu-id="0e847-133">Search for **Entity Store**.</span></span>
1. <span data-ttu-id="0e847-134">I listen til venstre navigerer du til **RetailSales**-oppføringen og velger **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="0e847-134">In the list on the left, navigate to the **RetailSales** entry, and select **Edit**.</span></span>
1. <span data-ttu-id="0e847-135">Forsikre deg om at **Automatisk oppdatering aktivert** er satt til **Ja**, velg **Oppdater**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0e847-135">Ensure that **Automatic Refresh Enabled** is set to **Yes**, select **Refresh**, and then select **Save**.</span></span>

<span data-ttu-id="0e847-136">Det følgende bildet viser et eksempel på et enhetslager der automatisk oppdatering er aktivert.</span><span class="sxs-lookup"><span data-stu-id="0e847-136">The following image shows an example of Entity store with automatic refresh enabled.</span></span>

![Eksempel på enhetslager med automatisk oppdatering aktivert](./media/exampleADLSConfig2.png)

<span data-ttu-id="0e847-138">ADLS er nå konfigurert for miljøet.</span><span class="sxs-lookup"><span data-stu-id="0e847-138">ADLS is now configured for the environment.</span></span> 

<span data-ttu-id="0e847-139">Hvis de ikke er fullført allerede, følger du trinnene for å [aktivere produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.</span><span class="sxs-lookup"><span data-stu-id="0e847-139">If not completed already, follow the steps for [enabling product recommendations and personalization](enable-product-recommendations.md) for the environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e847-140">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0e847-140">Additional resources</span></span>

[<span data-ttu-id="0e847-141">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="0e847-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="0e847-142">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="0e847-142">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="0e847-143">Legge til produktanbefalingslisten på sider</span><span class="sxs-lookup"><span data-stu-id="0e847-143">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="0e847-144">Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="0e847-144">Add a recommendations control to the transaction screen on POS devices</span></span>](../retail/add-recommendations-control-pos-screen.md?toc=/dynamics365/commerce/toc.json)


