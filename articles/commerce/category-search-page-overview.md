---
title: Oversikt over standard kategorimålside og søkeresultatside
description: Dette emnet gir en oversik over standard kategorimålside og søkeresultatside i Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f380f3f56727d927d7cd328fef3c9d999afa2873
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794355"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Oversikt over standard kategorimålside og søkeresultatside

[!include [banner](includes/banner.md)]

Dette emnet gir en oversik over standard kategorimålside og søkeresultatside i Microsoft Dynamics 365 Commerce e-Commerce.

## <a name="default-category-landing-page"></a>Standard kategorimålside

Standard kategorimålside er siden som brukere av webområder vanligvis kommer til når de velger en kategori i navigasjonshierarkiet. Kategorisiden lar deg bla gjennom, og du kan også sortere og presisere de kategoriserte produktene.

![Standard kategorimålside](./media/SimpleCategoryLandingDressCategory.png)

Øverst på siden er det en topptekst som viser alle produktkategoriene og andre sider som varehandelslederen har kategorisert. Konfigurasjon utføres som en del av konfigurasjonen av kanalnavigeringshierarkiet. På bunnen av siden er det en bunntekst som inneholder hurtigkoblinger til ulike emner som en kunde kan være interessert i.

Følgende komponenter er grunnleggende for en kategori:

- **Produktplasseringsfliser** viser produktene som varehandelslederen har definert i en kategori som en del av konfigurasjonen av navigasjonshierarkiet.
- **Sammendrag av presiseringer og valg** er filtre som angir antall, og som kan brukes til å finjustere varer. Varehandelslederen konfigurerer dem som en del av konfigurasjonen av metadataene som er relatert til kanalkategorier og produktattributter.
- **Sorteringsalternativer** brukes av besøkende på webområder til å sortere produktene. Som standard er følgende sorteringsalternativer tilgjengelige:

    - Pris: – lav til høy
    - Pris: – høy til lav
    - Produktnavn – \[A–Å\]
    - Produktnavn – – \[Å–A\]
    - Vurderinger – lav til høy
    - Vurderinger – høy til lav

- **Sidenummerering** lar besøkende på webområdet flytte fra én side med kategoriserte produktresultater til en annen side.
- **Totalt antall** inneholder totalt antall produkter som er definert i en kategori.

## <a name="enrich-a-category-landing-page"></a>Supplere en kategorimålside

Hvis du vil at en kategorimålside skal ha en mer skreddersydd opplevelse for en bestemt kategori, kan du "supplere" kategorimålsiden for denne kategorien. Du kan for eksempel legge til en markedsføringsvideo og enkelte kategoribeskrivelser for å få en kundes oppmerksomhet. Hvis du vil ha mer informasjon, se [Supplere en kategorimålside](enrich-category-page.md).

![Supplere kategorimålside](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automatisk foreslå og søke på resultatsider

Brukere av webområder kan utforske et område enten ved å gå til en kategori fra navigasjonshierarkiet eller ved å skrive inn et søkeord i søkefeltet.

Så snart brukerne begynner å skrive inn søkefeltet, får de oppleve den dyptgående funksjonaliteten for automatiske foreslag som foreslår søkeord.

Her er noen av forslagstypene som kan vises:

- **Nøkkelord** brukes til å finne frem til varer på tvers av alle produkter som er assortert til kanalen.
- **Produkter** gir deg direkte koblinger til siden for produktdetaljer.
- **Søkeforslag for kategoriområde** viser ulike kategorier og lar brukere søke etter nøkkelordet i en bestemt kategori.

![Dyptgående automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

Når brukere velger et av nøkkelordene eller kategorisøkforslag for område, eller når det ikke er forslag til søkeordet de legger inn, omdirigeres de til en søkeresultatside. Brukerne kan deretter bla gjennom, sortere og begrense listen over søkeresultater for å finne ønsket element.

![Søkemålside](./media/SearchLanding.png)

Følgende komponenter er grunnleggende for en søkeresultatside:

- **Produktplasseringsfliser** viser produktene for brukerens søk. Som standard er disse flisene sortert etter skydrevet søkerelevanssum for brukersøket.
- **Sammendrag av presiseringer og valg** er filtre som angir antall, og som kan brukes til å finjustere varer. Varehandelslederen konfigurerer dem som en del av konfigurasjonen av metadataene for "kanalkategorier og produktattributter".
- **Sorteringsalternativer** brukes av besøkende på webområder til å sortere produktene. Som standard er følgende sorteringsalternativer tilgjengelige:

    - Pris: – lav til høy
    - Pris: – høy til lav
    - Produktnavn – \[A–Å\]
    - Produktnavn – – \[Å–A\]
    - Vurderinger – lav til høy
    - Vurderinger – høy til lav
    - Standard

- **Sidenummerering** lar besøkende på webområdet flytte fra én side med kategoriserte produktresultater til en annen side.
- **Totalt antall** inneholder totalt antall produkter som er definert i en kategori, og som samsvarer med søkevilkårene.

>[!NOTE]
>Disse skydrevne søkefunksjonene er tilgjengelige fra versjon 10.0.8. Kontroller at det under **Handelsparametere > Konfigurasjonsparametere** finnes en oppføring for ProductSearch. UseAzureSearch satt til true. 
![Konfigurasjonsparametere for skydrevet søk](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over skybaserte søk](cloud-powered-search-overview.md)

[Oversikt over startside](quick-tour-home-page.md)

[Oversikt over produktdetaljsider](quick-tour-pdp.md)

[Oversikt over sider for handlekurv og kasse](quick-tour-cart-checkout.md)

[Oversikt over kontobehandlingssider](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]