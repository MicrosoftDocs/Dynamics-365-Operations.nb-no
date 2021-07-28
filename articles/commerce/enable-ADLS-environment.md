---
title: Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø
description: Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.
author: bebeale
ms.date: 04/13/2020
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
ms.openlocfilehash: 9ac440362379475b05c6a37019c25e3a96be3739
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349502"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.

I Dynamics 365 Commerce-løsningen spores all produkt- og transaksjonsinformasjon i miljøets enhetslager. Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen 2-løsning.

Når Azure Data Lake Storage er konfigurert i et miljø, blir alle nødvendige data gjenspeilet fra enhetslageret samtidig som de fremdeles beskyttes og er under kundens kontroll.

Hvis produktanbefalinger eller tilpassede anbefalinger også er aktivert i miljøet, får produktanbefalingsstakken tilgang til den dedikerte mappen i Azure Data Lake Storage for å hente kundens data og beregne anbefalinger basert på dem.

## <a name="prerequisites"></a>Forutsetninger

Kunder må ha Azure Data Lake Storage konfigurert i et Azure-abonnement som de eier. Dette emnet dekker ikke kjøpet av et Azure-abonnement eller oppsettet av en Azure Data Lake Storage-aktivert lagringskonto.

Hvis du vil ha mer informasjon om Azure Data Lake Storage, kan du se [Offentlig Azure Data Lake Storage Gen2-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurasjonstrinn

Denne delen dekker konfigurasjonstrinnene som er nødvendige for å aktivere Azure Data Lake Storage i et miljø som er knyttet til produktanbefalinger.
Hvis du vil ha en mer detaljert oversikt over trinnene som kreves for å aktivere Azure Data Lake Storage, kan du se [Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>Aktivere Azure Data Lake Storage i miljøet

1. Logg deg på miljøets administrasjonskontorportal.
1. Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen. 
1. Sett **Aktiver Data Lake-integrasjon** til **Ja**.
1. Sett **Oppdater Data Lake fordelt** til **Ja**.
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
> Hvis testene mislykkes, dobbeltsjekker du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.

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
