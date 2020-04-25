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
# <a name="enable-adls-in-a-dynamics-365-commerce-environment"></a>Aktivere ADLS i et Dynamics 365 Commerce-miljø

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du aktiverer og tester Azure Data Lake Storage (ADLS) for et Dynamics 365 Commerce-miljø, som er en forutsetning for å aktivere produktanbefalinger.

## <a name="overview"></a>Oversikt

I Dynamics 365 Commerce-løsningen spores all produkt- og transaksjonsinformasjon i miljøets enhetslager. Hvis du vil at disse dataene skal være tilgjengelige for andre Dynamics 365-tjenester, for eksempel dataanalyse, forretningsintelligens og tilpassede anbefalinger, må du koble miljøet til en kundeeid Azure Data Lake Storage Gen 2-løsning (ADLS).

Når ADLS er konfigurert i et miljø, blir alle nødvendige data gjenspeilet fra enhetslageret samtidig som de fremdeles beskyttes og er under kundens kontroll.

Hvis produktanbefalinger eller tilpassede anbefalinger også er aktivert i miljøet, får produktanbefalingsstakken tilgang til den dedikerte mappen i ADLS for å hente kundens data og beregne anbefalinger basert på dem.

## <a name="prerequisites"></a>Forutsetninger

Kunder må ha ADLS konfigurert i et Azure-abonnement som de eier. Dette emnet dekker ikke kjøpet av et Azure-abonnement eller oppsettet av en ADLS-aktivert lagringskonto.

Hvis du vil ha mer informasjon om ADLS, kan du se [Offentlig ADLS-dokumentasjon](https://azure.microsoft.com/pricing/details/storage/data-lake).
  
## <a name="configuration-steps"></a>Konfigurasjonstrinn

Denne delen dekker konfigurasjonstrinnene som er nødvendige for å aktivere ADLS i et miljø som er knyttet til produktanbefalinger.
Hvis du vil ha en mer detaljert oversikt over trinnene som kreves for å aktivere ADLS, kan du se [Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).

### <a name="enable-adls-in-the-environment"></a>Aktivere ADLS i miljøet

1. Logg deg på miljøets administrasjonskontorportal.
1. Søk etter **Systemparametere** og naviger til **Datatilkoblinger**-fanen. 
1. Sett **Aktiver Data Lake-integrasjon** til **Ja**.
1. Sett **Oppdater Data Lake fordelt** til **Ja**.
1. Deretter angir du følgende påkrevd informasjon:
    1. **Applikasjons-ID** // **Applikasjonshemmelighet** // **DNS-navn** – Nødvendig for å koble til KeyVault der ADLS-hemmeligheten er lagret.
    1. **Hemmelig navn** – Det hemmelige navnet som er lagret i KeyVault, og som brukes til å autentisere med ADLS.
1. Lagre endringene i sidens øvre venstre hjørne.

Bildet nedenfor viser et eksempel på en ADLS-konfigurasjon.

![Eksempel på ADLS-konfigurasjon](./media/exampleADLSConfig1.png)

### <a name="test-the-adls-connection"></a>Test ADLS-tilkoblingen

1. Test tilkoblingen til KeyVault ved hjelp av **Test Azure Key Vault**-koblingen.
1. Test tilkoblingen til ADLS ved hjelp av **Test Azure Storage**-koblingen.

> [!NOTE]
> Hvis testene mislykkes, dobbeltsjekker du at alle de tilføyde KeyVault-opplysningene ovenfor er korrekte og prøver deretter på nytt.

Når tilkoblingstestene er vellykket, må du aktivere automatisk oppdatering for enhetslageret.

Hvis du vil aktivere automatisk oppdatering for enhetslager, følger du disse trinnene.

1. Søk etter **Enhetslager**.
1. I listen til venstre navigerer du til **RetailSales**-oppføringen og velger **Rediger**.
1. Forsikre deg om at **Automatisk oppdatering aktivert** er satt til **Ja**, velg **Oppdater**, og velg deretter **Lagre**.

Det følgende bildet viser et eksempel på et enhetslager der automatisk oppdatering er aktivert.

![Eksempel på enhetslager med automatisk oppdatering aktivert](./media/exampleADLSConfig2.png)

ADLS er nå konfigurert for miljøet. 

Hvis de ikke er fullført allerede, følger du trinnene for å [aktivere produktanbefalinger og tilpasning](enable-product-recommendations.md) for miljøet.

## <a name="additional-resources"></a>Tilleggsressurser

[Gjøre enhetslager tilgjengelig som Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
