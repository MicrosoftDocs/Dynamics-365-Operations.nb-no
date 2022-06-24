---
title: Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø
description: Denne artikkelen inneholder instruksjoner om hvordan du kobler en Azure Data Lake Storage Gen 2-løsning til et Dynamics 365 Commerce miljøs enhetsbutikk. Dette er et nødvendig trinn før du aktiverer produktanbefalinger.
author: bebeale
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6e0c84dd6b173a111b70a8adb6036be946149f7c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885177"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Denne artikkelen inneholder instruksjoner om hvordan du kobler en Azure Data Lake Storage Gen2-løsning til et Dynamics 365 Commerce-miljøs enhetsbutikk. Dette er et nødvendig trinn før du aktiverer produktanbefalinger.

I Dynamics 365 Commerce løsningen samles dataene som er nødvendige for å beregne anbefalinger, produkter og transaksjoner, i miljøets enhetsbutikk. Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen2-løsning.

Når trinnene ovenfor er fullført, gjenspeiles alle kundedata i miljøets enhetsbutikk automatisk til kundens Azure Data Lake Storage Gen 2-løsning. Når funksjoner for anbefalinger er aktivert via arbeidsområdet for funksjonsstyring i Commerce Headquarters, får anbefalingsstakken tilgang til den samme Azure Data Lake Storage Gen2-løsningen.

I løpet av hele prosessen forblir kundenes data beskyttet og under deres kontroll.

## <a name="prerequisites"></a>Forutsetninger

Et Dynamics 365 Commerce miljøs enhetsbutikk må være koblet til en Azure Data Lake Gen Storage Gen2-konto og tilhørende tjenester.

Hvis du vil ha mer informasjon om Azure Data Lake Storage Gen2 og hvordan du konfigurerer den, kan du se [Azure Data Lake Storage Offentlig Gen2-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurasjonstrinn

Denne delen dekker konfigurasjonstrinnene som er nødvendige for å aktivere Azure Data Lake Storage Gen2 i et miljø som er knyttet til produktanbefalinger.
Hvis du vil ha en mer detaljert oversikt over trinnene som kreves for å aktivere Azure Data Lake Storage Gen2, kan du se [Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivere Azure Data Lake Storage i miljøet

1. Logg deg på miljøets administrasjonskontorportal.
1. Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen. 
1. Sett **Aktiver Data Lake-integrasjon** til **Ja**.
1. Deretter angir du følgende påkrevd informasjon:
    1. **Applikasjons-ID** // **Applikasjonshemmelighet** // **DNS-navn** – Nødvendig for å koble til KeyVault der Azure Data Lake Storage-hemmeligheten er lagret.
    1. **Hemmelig navn** – Det hemmelige navnet som er lagret i KeyVault, og som brukes til å autentisere med Azure Data Lake Storage.
1. Lagre endringene i sidens øvre venstre hjørne.

Bildet nedenfor viser et eksempel på en Azure Data Lake Storage-konfigurasjon.

![Eksempel på Azure Data Lake Storage-konfigurasjon.](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Test Azure Data Lake Storage-tilkoblingen

1. Test tilkoblingen til KeyVault ved hjelp av **Test Azure Key Vault**-koblingen.
1. Test tilkoblingen til Azure Data Lake Storage ved hjelp av **Test Azure Storage**-koblingen.

> [!NOTE]
> Hvis en av testene over mislykkes, bekrefter du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.

Når tilkoblingstestene er vellykket, må du aktivere automatisk oppdatering for enhetslageret.

Hvis du vil aktivere automatisk oppdatering for enhetslager, følger du disse trinnene.

1. Søk etter **Enhetslager**.
1. I listen til venstre navigerer du til **RetailSales**-oppføringen og velger **Rediger**.
1. Forsikre deg om at **Automatisk oppdatering aktivert** er satt til **Ja**, velg **Oppdater**, og velg deretter **Lagre**.

Det følgende bildet viser et eksempel på et enhetslager der automatisk oppdatering er aktivert.

![Eksempel på enhetslager med automatisk oppdatering aktivert.](./media/exampleADLSConfig2.png)

Azure Data Lake Storage er nå konfigurert for miljøet. 

Hvis de ikke er fullført allerede, følger du trinnene for å [aktivere produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.

## <a name="additional-resources"></a>Tilleggsressurser

[Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Legge til produktanbefalinger på salgssted](product.md)

[Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
