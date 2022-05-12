---
title: Vanlige spørsmål om handelskataloger for B2B
description: Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-kataloger.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 776820e8e77cd0884b3df5412bb95e6e80ca4fc7
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656853"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Vanlige spørsmål om handelskataloger for B2B

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet gir svar på vanlige spørsmål om Microsoft Dynamics 365 Commerce-[kataloger for bedrift-til-bedrift (B2B)](catalogs-b2b-sites.md).

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Hvorfor kan jeg ikke konfigurere et katalogspesifikt navigasjonshierarki eller se et alternativ for å tilknytte et kundehierarki?

Kontroller at funksjonen **Aktiver bruk av flere kataloger på detaljhandelskanaler** er aktivert i arbeidsområdet **Funksjonsstyring** i Commerce Headquarters. I tillegg må du kontrollere at miljøet bruker Commerce-versjon 10.0.26 eller nyere.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kan jeg vise det katalogspesifikke hierarkiet og supplere kategorisidene i Commerce-områdebygger?

Ja, Commerce-områdebyggerbrukere som har tilgang til **Produkter**-siden i områdebyggeren, velge en katalog og vise det katalogspesifikke hierarkiet. Brukere kan også legge inn en kategoriside for en bestemt kategori i katalogen, fra **Produkter**-siden. Hvis du vil ha mer informasjon, se [Supplere en kategorimålside](enrich-category-page.md). Hvis du vil ha en registrering som er spesifikk for en katalog, anbefaler vi at du har et atskilt og unikt navigasjonshierarki for katalogen.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kan et B2B-bruker kjøpe fra flere kataloger på én enkelt sjekk?

Ja, kjøp flere kataloger på én enkelt sjekk er tillatt. B2B-brukere kan bruke katalogindikatoren i handlekurvvisningen for å bestemme hvilke varer som er lagt til fra hvilke kataloger.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Hva er forventet atferd hvis en B2B-bruker kjøper den samme varen fra ulike kataloger?

Selv om en gitt bruker kan ha tilgang til flere kataloger på et gitt tidspunkt, er forventningen at produkter i disse katalogene vil være gjensidig utelukkende. Det samme produktet bør med andre ord ikke være en del av mer enn én katalog for en gitt bruker.

Hvis det oppstår en situasjon der det samme produktet tilhører flere kataloger, vil systemet beholde flere handlekurvlinjer for dette produktet. Det finnes en egen linje for hver katalog. Det samme produktet fra to ulike kataloger slås ikke sammen ved betaling.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Når en B2B-bruker skal handle, finnes det noen validering for katalogtilgjengelighet?

Ja. En B2B-bruker vil bare ha tillatelse til å gå videre til betaling hvis alle varer i handlekurven er fra gyldige kataloger. Hvis noen handlekurvvarer kommer fra kataloger som er utløpt eller trukket tilbake, fjernes de, og brukeren blir varslet.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Under handleopplevelse kan jeg søke og oppdage produkter (inkludert relaterte og anbefalte produktsamlinger) katalogspesifikt?

Ja. Så snart en bruker velger en bestemt katalog, blir hele handleprosessen katalogspesifikk. Denne tilknytningen omfatter erfaringer med produktoppdagelse, søkeforslag, søkeresultater, kategoriresultater, forbedringer, prissetting, attributter og anbefalte produkter (for eksempel nye, bestselgere, trendy, ofte kjøpt sammen og relaterte produkter).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kan en B2B-bruker kjøpe fra standardsortimentet (catalogID=0)?

Nei, en B2B-bruker har ikke tillatelse til å kjøpe fra standardsortimentet. Dette sortimentet er bare ment for anonym blaing. Hvis en B2B-bruker mangler katalogtildelinger (venter på oppdateringer fra administrasjonen), kan de ikke se noen kataloger de kan velge fra, og ingen kategorihierarki vil være synlige.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kan markedsføringsinnhold herdes for et produkt som er spesifikk for en katalog?

For øyeblikket støttes bare produktforbedring på område- og kanalnivå. Hvis et produkt er integrert, deles det med andre ord på tvers av flere kataloger, og den tilsvarende produktdetaljsiden (PDP) for dette produktet gjengis på samme måte i alle katalogene for et angitt område.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Er katalogstøtte tilgjengelig for både B2B- og B2C-nettbaserte kanaler (bedrift-til-kunde)?

Handelskataloger skal for øyeblikket bare fungere med B2B-kanaler.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kan vi konfigurere katalogspesifikk mersalg/kryssalgsvarer?

For øyeblikket støttes bare funksjonen for relaterte produkter. Mersalg- og kryssalgsvarekonfigurasjoner er imidlertid tilgjengelige for telefonsentre.

Følgende funksjoner støttes også bare for telefonsentre:

- Katalogkildekoder
- Bruk kilde-ID-er til å spore kostnader og svarrater
- Katalogspesifikke ordre- og vareskript
- Katalogsideanalyse
- Katalogforespørsler
- Betalingsplaner
- Gratisprodukter basert på kildekoder

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Kan vi bruke katalogkildekoder for B2B-ordrer via netthandelsportalen?

Nei Katalogkildekoder støttes bare for samtalesenterkanaler.

## <a name="additional-resources"></a>Tilleggsressurser

[Opprett handelskataloger for B2B-områder](catalogs-b2b-sites.md)

[Påvirkning av handelskataloger for B2B-tilpasninger](catalogs-b2b-sites-dev.md)
