---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcb3b542d290e01a3cddc73ae163ed2ef420771b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238803"
---
# <a name="enable-product-recommendations"></a>Aktiver produktanbefalinger

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Anbefalinger, forhåndssjekk

Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Commerce-kunder som har migrert lagringen til å bruke Azure Data Lake Storage. 

Følgende konfigurasjoner må aktiveres i Back Office før aktivering av anbefalinger:

1. Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet. For mer informasjon, se [Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet](enable-ADLS-environment.md).
2. Kontroller at oppdateringen av enhetslageret er automatisert. For mer informasjon, se [Kontroller at oppdateringen av enhetslageret er automatisert](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
3. Kontroller at Azure AD-identitetskonfigurasjonen inneholder en oppføring for anbefalinger. Du finner mer informasjon om hvordan du utfører denne handlingen nedenfor.

Kontroller også at RetailSale-mål er aktivert. Hvis du vil lære mer om denne konfigureringsprosessen, kan du se [Arbeide med mål](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).

## <a name="azure-ad-identity-configuration"></a>Azure AD-identitetskonfigurasjon

Dette trinnet er nødvendig for alle kunder som kjører en IaaS-konfigurasjon (infrastruktur som tjeneste). For kunder som kjører på Service Fabric (SF), bør dette trinnet være automatisk, og vi anbefaler at du kontrollerer at innstillingen er konfigurert som forventet.

### <a name="setup"></a>Installasjon

1. Fra Back Office, søk etter siden **Azure Active Directory-apper**.
2. Kontroller om det finnes en oppføring for "RecommendationSystemApplication-1".

Hvis oppføringen ikke finnes, legger du til en ny oppføring med følgende informasjon:

- **Klient-ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **Navn** - RecommendationSystemApplication-1
- **Bruker-ID** - RetailServiceAccount

Lagre og lukk siden. 

## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Gjør følgende for å aktivere produktanbefalinger.

1. I Commerce Headquarters søker du etter **Funksjonsbehandling**.
1. Velg **Alle** for å vise en liste over tilgjengelige funksjoner. 
1. Skriv inn **Anbefalinger** i søkeboksen.
1. Velg funksjonen **Produktanbefalinger**.
1. I egenskapsruten **Produktanbefalinger** velger du **Aktiver nå**.

![Aktivere anbefalinger](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister. Det kan ta flere timer kan være nødvendig før listene er tilgjengelige og kan vises ved salgsstedet (POS) eller i Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametere for anbefalingsliste

Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier. Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten. Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vis anbefalinger på salgsstedsenheter

Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet. Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Aktivere personlige anbefalinger

I Dynamics 365 Commerce kan forhandlere få tilpassede produktanbefalinger (også kjent som personalisering). På denne måten kan tilpassede anbefalinger bygges inn i kundeopplevelsen på nettet og ved salgsstedet (POS). Når funksjonaliteten for personalisering er aktivert, kan systemet tilknytte en brukers innkjøps- og produktinformasjon, slik at de genererer indivduelle produktanbefalinger.

Hvis du vil finne ut mer om tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]