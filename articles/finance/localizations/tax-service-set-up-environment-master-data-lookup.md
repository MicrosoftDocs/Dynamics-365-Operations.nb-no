---
title: Aktiver hoveddataoppslag for mva-beregningskonfigurasjon
description: Dette emnet beskriver hvordan du konfigurerer og aktiverer oppslagsfunksjonen for hoveddata i avgiftsberegning.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 455e8becfdfa910a3733719653e1a91557b2f59a
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867358"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Aktiver hoveddataoppslag for mva-beregningskonfigurasjon 

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer og aktiverer oppslagsfunksjonen for hoveddata i avgiftsberegning. En rullegardinliste er tilgjengelig for å velge verdier i mva-beregningskonfigurasjonen for felter som **Juridisk enhet**, **Leverandørkonto**, **Varekode** og **Leveringsbetingelse**. Disse verdiene kommer fra det tilkoblede Microsoft Dynamics 365 Finance-miljøet ved hjelp av Microsoft Dataverse-datakilden.

> [!NOTE] 
> Funksjonen for hoveddataoppslag for avgiftsberegning er valgfri funksjonalitet. Du kan hoppe over følgende trinn hvis du deaktiverer funksjonen **Støtte for Dataverse-datakilder for avgiftstjeneste** i RCS (Regulatory Configuration Service). I så fall vil imidlertid ikke rullegardinlisten være tilgjengelig i konfigurasjonen for avgiftsberegningen.

1. Konfigurer Microsoft Power Platform-integreringen i Microsoft Dynamics Lifecycle Services (LCS). Hvis du vil ha mer informasjon, kan du se [Microsoft Power Platform-integrering – oversikt over tillegg](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Når du har fullført dette trinnet, vises navnet på et Microsoft Power Platform-miljø i **Power Platform Integrering**-delen.
2. Gå til [Microsoft Power Platform administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), og velg miljønavnet. Miljø-URL-en er angitt.
3. Konfigurer Dynamics 365 Finance og Dataverse. Hvis du vil ha mer informasjon, kan du se [Skaffe løsningen for den virtuelle enheten](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) og [Godkjenning og autorisasjon](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Sett opp følgende enheter. Hvis du vil ha mer informasjon, kan du se [Aktiver Microsoft Dataverse virtuelle enheter](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Konfigurer Regulatory Configuration Service (RCS). Åpne arbeidsområdet **Funksjonsstyring**, og aktiver følgende funksjoner:

    - Støtte for Dataverse-datakilder for elektronisk rapportering
    - Støtte for Dataverse-datakilder for avgiftstjeneste
    - Globaliseringsfunksjoner

6. Logg på RCS ved å bruke en leieradministratorkonto.
7. Gå til **Elektronisk rapportering** > **Tilkoblede programmer**. 
8. Velg **Ny** for å legge til en oppføring, og angi følgende feltinformasjon. 

    - Angi et navn i **Navn**-feltet.
    - I **Type**-feltet velger du **Dataverse**.
    - I **Program**-feltet angir du URL-adressen for Dataverse.
    - I **Leier**-feltet angir du leieren.
    - I feltet **Egendefinert URL-adresse** angir du URL-adressen for Dataverse og legger til "/api/data/v9.1" etter den.

9. Velg **Kontroller tilkobling**, og fullfør tilkoblingsprosessen. 

    [![Kontroller tilkobling-knappen.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Gå til **Elektronisk rapportering** > **Avgiftskonfigurasjoner**, og importer avgiftskonfigurasjoner fra [Avgiftskonfigurasjoner](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Agiftskonfigurasjoner-siden, Avgiftsdatamodell-treet.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Gå til **Tilordning av modell for avgiftsbelagt dokument** eller til **Tilordning av Dataverse-modell** hvis du bruker en Microsoft-konfigurasjon,. og velg deretter oppføringen du opprettet i trinn 7, i feltet **Tilkoblet program**.
12. Sett **Standardalternativ for modelltilordning** til **Ja**.

    [![Modelltilordning-siden.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
