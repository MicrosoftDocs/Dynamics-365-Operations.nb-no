---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4a7be82b3a40aba621693f080ff41767fdaea474
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466322"
---
# <a name="enable-product-recommendations"></a>Aktiver produktanbefalinger

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Anbefalinger, forhåndssjekk

1. Kontroller at du har en gyldig Dynamics 365 Commerce lisens for anbefalinger.
1. Kontroller at enhetsbutikken er knyttet til en kundeeid Azure Data Lake Storage Gen2-konto. For mer informasjon, se [Kontroller at Azure Data Lake Storage er kjøpt og korrekt verifisert i miljøet](enable-ADLS-environment.md).
1. Kontroller at Azure AD-identitetskonfigurasjonen inneholder en oppføring for anbefalinger. Du finner mer informasjon om hvordan du utfører denne handlingen nedenfor.
1. Kontroller at daglig oppdatering for enhetsbutikk til Azure Data Lake Storage Gen2 er planlagt. For mer informasjon, se [Kontroller at oppdateringen av enhetslageret er automatisert](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).
1. Aktiver RetailSale-målinger for enhetsbutikken. Hvis du ha mer informasjon om denne konfigureringsprosessen, kan du se [Arbeide med mål](/dynamics365/ai/customer-insights/pm-measures).

Når trinnene ovenfor er fullført, er du klar til å aktivere anbefalinger.

## <a name="azure-ad-identity-configuration"></a>Azure AD-identitetskonfigurasjon

Dette trinnet er bare nødvendig for kunder som kjører en IaaS-konfigurasjon (infrastruktur som tjeneste). Azure AD Identitetskonfigurasjon er automatisk for kunder som kjører på Azure Service Fabric, men det anbefales at du kontrollerer at innstillingen er konfigurert som forventet.

### <a name="setup"></a>Installasjon

1. Søk etter **Azure Active Directory program**-siden i Commerce Headquarters.
1. Kontroller at det finnes en oppføring for **RecommendationSystemApplication-1**. Hvis det ikke finnes en oppføring, oppretter du en ved hjelp av følgende informasjon:

    - **Klient-ID**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **Navn**: RecommendationSystemApplication-1
    - **Bruker-ID**: RetailServiceAccount

1. Lagre og lukk siden. 

## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Gjør følgende for å aktivere produktanbefalinger.

1. I Commerce Headquarters søker du etter **Funksjonsbehandling**.
1. Velg **Alle** for å vise en liste over tilgjengelige funksjoner. 
1. Skriv inn **Anbefalinger** i søkeboksen.
1. Velg funksjonen **Produktanbefalinger**.
1. I egenskapsruten **Produktanbefalinger** velger du **Aktiver nå**.

![Aktivere anbefalinger.](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister. Det kan ta flere timer kan være nødvendig før listene er tilgjengelige og kan vises ved salgsstedet (POS) eller i Dynamics 365 Commerce.
> - Denne konfigurasjonen aktiverer ikke alle anbefalinger. Avanserte funksjoner, for eksempel tilpassede anbefalinger, "kjøp lignende utseender" og "kjøp med lignende beskrivelse", styres av dedikerte funksjonsadministrasjonsoppføringer. Hvis du vil ha informasjon om aktivering av disse funksjonene i Commerce Headquarters, kan du se [Aktivere personlige anbefalinger](personalized-recommendations.md), [Aktivere "kjøp lignende utseender-anbefalinger](shop-similar-looks.md) og [Aktivere "kjøp med lignende beskrivelse"-anbefalinger](shop-similar-description.md).

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametere for anbefalingsliste

Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier. Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten. Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="include-recommendations-in-e-commerce-experiences"></a>Inkluder anbefalinger i e-handelopplevelser

Når anbefalinger er aktivert i Commerce Headquarters, er Commerce-modulene som brukes til å vise anbefalingsresultater for erfaringer fra e-handel, klare til å konfigureres. Hvis du vil ha mer informasjon, kan du se [Produktsamlingsmoduler](product-collection-module-overview.md).

## <a name="show-recommendations-on-pos-devices"></a>Vis anbefalinger på salgsstedsenheter

Når du har aktivert anbefalinger i Commerce Headquarters, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet. Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md). 

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
