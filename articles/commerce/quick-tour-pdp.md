---
title: Oversikt over produktdetaljsider
description: Denne artikkelen gir en oversikt over produktdetaljsider (PDP-er) i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4856e6e208834d7dcc16d19ad4afb63c329a5868
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278507"
---
# <a name="product-details-pages-overview"></a>Oversikt over produktdetaljsider

[!include [banner](includes/banner.md)]

Denne artikkelen gir en oversikt over produktdetaljsider (PDP-er) i Microsoft Dynamics 365 Commerce.

En PDP gir detaljert informasjon om et produkt og lar kundene velge produktalternativer, for eksempel størrelse, stil og farge. En PDP bør vise all produktinformasjonen som en kunde må ha for å ta en kjøpsbeslutning.

Illustrasjonen nedenfor viser et eksempel på en PDP.

![Eksempel på en produktdetaljside.](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a>Moduler for topptekst og bunntekst

Toppen av en PDP har en topptekst som viser alle produktkategoriene og andre sider som forhandleren vil at kunder skal bla gjennom. Bunnen på siden har en bunntekst som inneholder hurtigkoblinger til ulike artikler som kan være av interesser for kunder.

## <a name="buy-box-module"></a>Kjøpsboksmodul

Den viktigste modulen på en PDP er kjøpsboksmodulen, som vises som første element i hoveddelen på siden. En kjøpsboksmodul viser viktig produktinformasjon, for eksempel produktnavnet, produktbeskrivelsen, produktprisen, produktbilder og produktklassifiseringer.

Modulen for kjøpsboks lar kunden velge produktalternativer (for eksempel størrelse, stil og farge) og legger til produktet i handlekurven. Den gjør også det mulig for kunden å kjøpe produktet på Internett og hente det i en butikk. Modulen for kjøp på Internett og henting i butikk bruker integrasjon med Bing-kart-API til å finne nærliggende butikker eller butikker i en annen lokasjon som kunden angir.

En kjøpsboksmodul krever en produkt-ID. Denne IDen er avledet fra sidekonteksten. Hvis en kjøpsboksmodul legges til en side der sidekonteksten ikke inneholder en produkt-ID, gjengis ikke informasjonen riktig.

## <a name="product-specifications-module"></a>Produktspesifikasjonsmodul

Modulen for produktspesifikasjoner kan brukes til å vise flere detaljer om produktet. Disse detaljene hentes fra produktattributter i Commerce. Modulen for produktspesifikasjoner viser alle attributter der **visible** -egenskapen er satt til **sann**. Det krever en produkt-ID for å hente produktattributter.

## <a name="recommendations-module"></a>Anbefalingsmodul

Anbefalingsmodulen er en viktig modul på en PDP. Mens kunder søker etter produkter skal flere produktalternativer presenteres for dem, slik at de kan finne det riktige produktet og foreta et kjøp. Anbefalinger hjelper kundene å finne relatert innhold på en enkel måte og fortsette å handle.

Ulike typer anbefalingslister er tilgjengelige:

- Listen **Folk liker også** er basert på maskinopplæring. Den bruker transaksjonsloggen for andre kunder til å gi anbefalinger. Denne listen er generert av anbefalingstjenesten og ligner på listene "Kunder som har kjøpt denne varen, kjøpte også...". Det kreves en produkt-ID for å generere denne listen.
- En **beslektet**-liste kan konfigureres for et produkt i Commerce. For en brun reiseveske kan for eksempel flere reisevesker av skinn eller som er utformet for reiseformål, konfigureres for den tilknyttede listen. Andre typer relaterte lister, for eksempel **Tilbehør** og **Mer som dette**, kan også konfigureres i Commerce. Det kreves en produkt-ID for å generere denne listen. Hvis den legges til på en startside, der sidekonteksten ikke inneholder en produkt-ID, vil listen derfor være tom.
- Algoritmisk genererte anbefalingslister, for eksempel **Stjerneskudd**, **Bestselgere** og **Ny**, kan brukes på PDPer. Selv om disse listene ikke er direkte relatert til produktet på PDP, er de en annen måte å finne produkter på som kan ha interesse for kundene. Denne typen lister krever ikke en produkt-ID. De er generiske lister som genereres basert på handlemønstre på tvers av området.
- Redaksjonelle lister er manuelt kuraterte lister. En forhandler kan for eksempel bestemme deg for å kuratere lister over produkter som vedkommende vil vise.

## <a name="ratings-and-reviews-modules"></a>Vurderings- og omtalemoduler

Tre moduler kan brukes til å vise og legge til omtaler:

- **Omtaler** – Denne modulen viser vurderinger og omtaler som er levert av andre kunder. Kunder kan sortere og filtrere omtalene. I denne modulen kan kunder også like eller mislike omtaler og rapportere problemer.
- **Skriv omtale** – I denne modulen kan kundene skrive sine egne omtaler av et produkt.
- **Vurderingshistogram** – Denne modulen inneholder et histogram som viser vurderingstendensen for et produkt.

Hvis du vil ha mer informasjon, se [Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md).

## <a name="marketing-modules"></a>Markedsføringsmoduler

Hvis markedsføringsinnhold er unikt for et bestemt produkt, kan hvilke som helst markedsføringsmoduler legges til i PDP. Du kan legge til markedsføringsmoduler i en PDP ved å "supplere" siden. Hvis du vil ha mer informasjon, kan du se [Supplere en produktside](enrich-product-page.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over startside](quick-tour-home-page.md)

[Oversikt over sider for handlekurv og kasse](quick-tour-cart-checkout.md)

[Oversikt over kontobehandlingssider](quick-tour-account-management.md)

[Supplere en produktdetaljside](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
