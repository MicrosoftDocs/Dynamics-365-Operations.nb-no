---
title: Digitale gavekort for e-handel
description: Dette emnet beskriver hvordan digitale gavekort fungerer i e-handelsimplementeringen av Microsoft Dynamics 365 Commerce. Det gir også en oversikt over viktige konfigurasjonstrinn.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982672"
---
# <a name="e-commerce-digital-gift-cards"></a>Digitale gavekort for e-handel

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan digitale gavekort fungerer i e-handelsimplementeringen av Microsoft Dynamics 365 Commerce. Det gir også en oversikt over viktige konfigurasjonstrinn.

I Dynamics 365 Commerce følger kjøpet av digitale gavekort samme flyt som kjøpet av andre produkter i systemet. Ingen tilleggsmoduler må konfigureres. Hvis det er lagt til flere gavekort i handlekurven, samles ikke gavekortvarer på én enkelt salgslinje. Denne virkemåten er nødvendig fordi hver salgslinje faktureres ved hjelp av et eget gavekortnummer.

Innkjøp av digitale gavekort støttes i Dynamics 365 Commerce 10.0.16-versjonen og senere.

Illustrasjonen nedenfor viser et eksempel på produktdetaljersiden (PDP) for et digitalt gavekort på Fabrikams e-handelsområde.

![Eksempel på produktdetaljersiden for digitalt gavekort på Fabrikams e-handelsområde](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Slå på den digitale gavekortfunksjonen i Commerce Headquarters

For at innkjøpsflyten for digitale gavekort skal fungere i Dynamics 365 Commerce, må funksjonen **Innkjøp av gavekort på e-handel** være aktivert i Commerce Headquarters. Du finner funksjonen i arbeidsområdet **Funksjonsbehandling** i Commerce headquarters, som vist i følgende illustrasjon.

![Arbeidsområdet for funksjonsbehandling i Commerce Headquarters](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Konfigurere et digital gavekort i Commerce Headquarters

Digitale gavekortprodukter konfigureres i Commerce Headquarters. Prosessen ligner på prosessen for andre produkter. Følgende viktige trinn er imidlertid spesifikke for konfigurasjonen av gavekort for kjøp. Hvis du vil ha mer informasjon om hvordan du oppretter og konfigurerer produkter, kan du se [Opprette et nytt produkt i Commerce](create-new-product-commerce.md).

- Når du konfigurerer digitale gavekortprodukter i dialogboksen **Nytt produkt**, angir du **Produkttype**-feltet til **Tjeneste**. (Hvis du vil åpne dialogboksen, kan du gå til **Detaljhandel og handel \> Produkter og kategorier \> Produkter etter kategori** og velge **Nytt**.) Produkter av typen **Tjeneste** kontrolleres ikke for tilgjengelig lager før det legges inn en ordre. Hvis du vil ha mer informasjon, kan du se [Opprette et nytt produkt](create-new-product-commerce.md#create-a-new-product).
- På siden **Commerce-parametere**, i kategorien **Postering**, må feltet **Gavekortprodukt** være satt til **Digitalt gavekort**, som vist i illustrasjonen nedenfor. Hvis produktet er et eksternt gavekort, kan du se [Støtte for eksterne gavekort](./dev-itpro/gift-card.md) hvis du vil ha mer informasjon.

    ![Gavekortproduktfelt i Commerce headquarters](./media/PostGiftcard.png)

- Hvis et gavekort må ha støtte for flere forhåndsdefinerte beløp (for eksempel $25, $50 og $100), må dimensjonen **Størrelse** brukes til å definere disse forhåndsdefinerte beløpene. Hvert forhåndsdefinerte beløp er en variant. Hvis du vil ha mer informasjon, kan du se [Produktdimensjoner](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).
- Hvis kunder må kunne angi et egendefinert beløp for et gavekort, må du først definere en variant som gir rom for et egendefinert beløp. Deretter åpner du produktet fra siden **Frigitte produkter i kategori**, og deretter, i hurtigfanen **Commerce**, angir du feltet **Tast inn pris** til **Må taste inn ny pris**, som vist i illustrasjonen nedenfor. Denne innstillingen sikrer at kunder kan angi en pris når de blar gjennom produktet på en PDP.

    ![Tast inn pris-feltet i Commerce Headquarters](./media/KeyInPrice.png)

- Leveringsmåten for et digitalt gavekort må settes til **Elektronisk**. På **Leveringsmåter**-siden (**Retail og Commerce \> Kanaloppsett \> Leveringsmåter**) velger du leveringsmåten **Elektronisk** i listeruten, og deretter legger du til det digitale gavekortproduktet i rutenettet i hurtigfanen **Produkter**, som vist i illustrasjonen nedenfor. Hvis du vil ha mer informasjon, kan du se [Definere leveringsmåter](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Digitale gavekortprodukter på siden Leveringsmåte i Commerce Headquarters](./media/ElectronicMode.PNG)

- Kontroller at det er opprettet en online funksjonalitetsprofil som er knyttet til den elektroniske butikken i Commerce Headquarters. I funksjonalitetsprofilen angir du alternativet **Slå sammen produkter** til **Ja**. Denne innstillingen sikrer at alle varer unntatt gavekort slås sammen. Hvis du vil ha mer informasjon, kan du se [Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md).
- Hvis du vil sikre at kundene mottar en e-post etter at et gavekort er fakturert, oppretter du en ny type e-postvarsling på siden **E-postvarslingsprofiler** og setter feltet **E-postvarslingstype** til **Utsted gavekort**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for e-postvarsling](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Legge til produktbilder i mediebiblioteket for Commerce-områdebygger

Du må legge til produktbilder for digitale gavekortprodukter i mediebiblioteket for Commerce-områdebygger. Kontroller at filnavnene til gavekortbildefilene følger områdets navngivningskonvensjoner for produktbilder. Hvis du vil ha mer informasjon, kan du se [Laste opp bilder](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Konfigurere et egendefinert beløp for et digitalt gavekort i Commerce-områdebygger

Hvis et digitalt gavekort er konfigurert for å tillate et egendefinert beløp, må denne virkemåten også være aktivert i [kjøpsboks-modulen](add-buy-box.md) som brukes i områdets PDPer. Innkjøpsboksmodulen støtter modulkonfigurasjon for å tillate egendefinerte beløp. Du kan også definere minimums- og maksimumsbeløpene som er tillatt for egendefinerte beløp.

Følg denne fremgangsmåten for å konfigurere et egendefinert beløp for et digitalt gavekort i Commerce-områdebyggeren.

1. Gå til innkjøpsboksmodulen som brukes på områdets PDPer. Denne innkjøpsboksmodulen kan være implementert i et fragment, i en mal eller på en side.
1. Velg **Rediger**.
1. Merk av for **Tillat egendefinert pris** i egenskapsruten til høyre.
1. Valgfritt: Hvis du vil definere minimums- og maksimumsbeløp for egendefinerte beløp, angir du beløp under **Minimumspris** og **Maksimumspris**.
1. Velg **Fullfør redigering**, og velg deretter **Publiser**.

## <a name="additional-resources"></a>Tilleggsressurser

[Kjøpsboksmodul](add-buy-box.md)

[Kassemodul](add-checkout-module.md)

[Handlekurvmodul](add-cart-module.md)

[Opprette et nytt produkt i Commerce](create-new-product-commerce.md)

[Definer leveringsmåter](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Produktdimensjoner](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[Definere en profil for e-postvarsling](email-notification-profiles.md)

[Opprette en nettbasert funksjonalitetsprofil](online-functionality-profile.md)

[Støtte for eksterne gavekort](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]