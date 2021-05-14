---
title: Konfigurer et miljø for hoveddataoppslag
description: Dette emnet beskriver hvordan du konfigurerer miljøet for å bruke oppslagsfunksjonen for hoveddata i avgiftsberegning.
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924160"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="540f2-103">Konfigurer et miljø for hoveddataoppslag</span><span class="sxs-lookup"><span data-stu-id="540f2-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="540f2-104">Dette emnet beskriver hvordan du konfigurerer miljøet for å bruke oppslagsfunksjonen for hoveddata i avgiftsberegning.</span><span class="sxs-lookup"><span data-stu-id="540f2-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="540f2-105">Konfigurer Power Platform-integrering i Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="540f2-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="540f2-106">Hvis du vil ha mer informasjon, kan du se [Microsoft Power Platform-integrering – oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span><span class="sxs-lookup"><span data-stu-id="540f2-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="540f2-107">Konfigurer Dynamics 365 Finance og Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="540f2-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="540f2-108">Hvis du vil ha mer informasjon, kan du se [Skaffe løsningen](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) og [Godkjenning og autorisasjon](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span><span class="sxs-lookup"><span data-stu-id="540f2-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="540f2-109">Sett opp følgende enheter.</span><span class="sxs-lookup"><span data-stu-id="540f2-109">Set up the following entities.</span></span> <span data-ttu-id="540f2-110">Hvis du vil ha mer informasjon, kan du se [Aktivere virtuelle enheter](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="540f2-110">For more information, see [Enabling virtual entities](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities).</span></span>
      - <span data-ttu-id="540f2-111">CompanyInfoEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-111">CompanyInfoEntity</span></span>
      - <span data-ttu-id="540f2-112">CurrencyEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-112">CurrencyEntity</span></span>
      - <span data-ttu-id="540f2-113">CustCustomerV3Entity</span><span class="sxs-lookup"><span data-stu-id="540f2-113">CustCustomerV3Entity</span></span>
      - <span data-ttu-id="540f2-114">DeliveryTermsEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-114">DeliveryTermsEntity</span></span>
      - <span data-ttu-id="540f2-115">EcoResProductCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-115">EcoResProductCategoryEntity</span></span>
      - <span data-ttu-id="540f2-116">EcoResReleasedProductV2Entity</span><span class="sxs-lookup"><span data-stu-id="540f2-116">EcoResReleasedProductV2Entity</span></span>
      - <span data-ttu-id="540f2-117">LogisticsAddressCityEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-117">LogisticsAddressCityEntity</span></span>
      - <span data-ttu-id="540f2-118">LogisticsAddressCountryRegionTranslationEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-118">LogisticsAddressCountryRegionTranslationEntity</span></span>
      - <span data-ttu-id="540f2-119">LogisticsAddressStateEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-119">LogisticsAddressStateEntity</span></span>
      - <span data-ttu-id="540f2-120">PurchProcurementChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-120">PurchProcurementChargeCDSEntity</span></span>
      - <span data-ttu-id="540f2-121">SalesChargeCDSEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-121">SalesChargeCDSEntity</span></span>
      - <span data-ttu-id="540f2-122">TaxGroupEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-122">TaxGroupEntity</span></span>
      - <span data-ttu-id="540f2-123">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="540f2-123">TaxItemGroupHeadingEntity</span></span>
      - <span data-ttu-id="540f2-124">VendVendorV2Entity</span><span class="sxs-lookup"><span data-stu-id="540f2-124">VendVendorV2Entity</span></span>
4. <span data-ttu-id="540f2-125">Konfigurer Dynamics 365 Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="540f2-125">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="540f2-126">Opprett en serviceforespørsel for at Microsoft skal kunne aktivere testversjonering av følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="540f2-126">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="540f2-127">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="540f2-127">ERCdsFeature</span></span>
      - <span data-ttu-id="540f2-128">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="540f2-128">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="540f2-129">Gå til arbeidsområdet **Funksjonsstyring**, og aktiver følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="540f2-129">Go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="540f2-130">(Forhåndsversjon) Støtte for Dataverse-datakilder for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="540f2-130">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="540f2-131">(Forhåndsversjon) Støtte for Dataverse-datakilder for avgiftstjeneste</span><span class="sxs-lookup"><span data-stu-id="540f2-131">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="540f2-132">(Forhåndsvisning) Globaliseringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="540f2-132">(Preview) Globalization features</span></span>

5. <span data-ttu-id="540f2-133">Logg på RCS ved å bruke en leieradministratorkonto.</span><span class="sxs-lookup"><span data-stu-id="540f2-133">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="540f2-134">Gå til **Elektronisk rapportering** > **Tilkoblede programmer**.</span><span class="sxs-lookup"><span data-stu-id="540f2-134">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="540f2-135">Velg **Ny** for å legge til en oppføring, og angi følgende feltinformasjon.</span><span class="sxs-lookup"><span data-stu-id="540f2-135">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="540f2-136">Angi et navn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="540f2-136">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="540f2-137">I **Type**-feltet velger du **Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="540f2-137">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="540f2-138">I **Program**-feltet angir du URL-adressen for Dataverse.</span><span class="sxs-lookup"><span data-stu-id="540f2-138">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="540f2-139">I **Leier**-feltet angir du leieren.</span><span class="sxs-lookup"><span data-stu-id="540f2-139">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="540f2-140">I feltet **Egendefinert URL-adresse** angir du URL-adressen for Dataverse og legger til "/api/data/v9.1" etter den.</span><span class="sxs-lookup"><span data-stu-id="540f2-140">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="540f2-141">Velg **Kontroller tilkobling**, og fullfør tilkoblingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="540f2-141">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="540f2-142">[![Kontroller tilkobling-knappen](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="540f2-142">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="540f2-143">Gå til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**, og importer avgiftskonfigurasjoner fra [Avgiftskonfigurasjoner](https://go.microsoft.com/fwlink/?linkid=2158352).</span><span class="sxs-lookup"><span data-stu-id="540f2-143">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="540f2-144">[![Agiftskonfigurasjoner-siden, Avgiftsdatamodell-treet](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="540f2-144">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="540f2-145">Gå til **Tilordning av modell for avgiftsbelagt dokument** eller til **Tilordning av Dataverse-modell** hvis du bruker en Microsoft-konfigurasjon,. og velg deretter oppføringen du opprettet i trinn 7, i feltet **Tilkoblet program**.</span><span class="sxs-lookup"><span data-stu-id="540f2-145">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="540f2-146">Sett **Standardalternativ for modelltilordning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="540f2-146">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="540f2-147">[![Modelltilordning-siden](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="540f2-147">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
