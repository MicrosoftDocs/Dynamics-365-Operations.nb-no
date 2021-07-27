---
title: Aktivere personlige produktanbefalinger
description: Dette emnet beskriver hvordan du gjør tilpassede produktanbefalinger tilgjengelig for kunder i Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 08/18/2020
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
ms.openlocfilehash: b6d68d62636b5750cdcdca3f8ccbe155dc249b72
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352306"
---
# <a name="enable-personalized-recommendations"></a>Aktivere personlige anbefalinger

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du gjør tilpassede produktanbefalinger tilgjengelig for kunder i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce kan forhandlere få tilpassede produktanbefalinger (også kjent som personalisering). På denne måten kan tilpassede anbefalinger bygges inn i kundeopplevelsen på nettet og ved salgsstedet (POS). Når funksjonaliteten for personalisering er aktivert, kan systemet tilknytte en brukers innkjøps- og produktinformasjon, slik at de genererer indivduelle produktanbefalinger.

## <a name="personalization-prerequisites"></a>Forhåndskrav for personlige tilpasninger

Før du kan lage tilpassede produktanbefalinger som er tilgjengelige for kundene, bør du være oppmerksom på at produktanbefalinger bare støttes for Commerce-brukere som har migrert lagringsplassen til Azure Data Lake Store. Før kunder kan motta personlige produktanbefalinger, må forhandlere [aktivere produktanbefalinger](enable-product-recommendations.md).

> [!NOTE]
> Ved å aktivere produktanbefalinger aktiverer du også personalisering. Hvis du imidlertid deaktiverer personalisering, deaktiverer du ikke de andre typene produktanbefalinger.

Hvis du vil ha mer informasjon om produktanbefalinger, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="turn-on-personalization"></a>Aktivere tilpassing

Følg denne fremgangsmåten for å aktivere tilpassing.

1. I Commerce Headquarters søker du etter **Funksjonsbehandling**.
1. Velg **Alle** for å vise en liste over tilgjengelige funksjoner. 
1. Skriv inn **Anbefalinger** i søkeboksen.
1. Velg funksjonen **Personlige produktanbefalinger**.
1. I egenskapsruten **Personlige produktanbefalinger** velger du **Aktiver nå**.

![Aktivere tilpassing.](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Når du aktiverer tilpassing, startes prosessen for generering av tilpassede produktanbefalingslister. Det kan være nødvendig med opptil én dag før listene er tilgjengelige og synlige på Internett og salgsstedet.

## <a name="personalized-lists"></a>Tilpassede lister

I tillegg til å tillate tilpassing av eksisterende, maskingenererte lister kan du bruke anbefalingstjenesten til å tilpasse produktgjenkjenningsopplevelsen både på Internett og salgsstedet.

Når tilpassing er aktivert, kan forhandlere vise personlige lister av typen "Plukkinger for deg" eller "Anbefalt for kunder" på salgsstedsterminaler. I tillegg kan forhandlere bruke tilpassing på eksisterende produktanbefalingslister og gi bortvalgsopplevelser som følger EUs personvernforordning, til godkjente brukere. Hvis du deaktiverer tilpassing, deaktiverer du også disse funksjonene.

### <a name="online-picks-for-you-lists"></a>"Plukkinger for deg"-lister på Internett

En "Plukkinger for deg"-liste er en liste basert på kunstig intelligens og maskinlæring som viser en godkjent bruker en personlig tilpasset liste over foreslåtte produkter. Denne listen er basert på brukerens kjøpshistorikk i omnikanalen. Tilpassede anbefalinger oppdateres dynamisk etter hvert som brukeren gjør flere kjøp. Denne listetypen støtter også kategorifiltrering, slik at forhandlerne kan vise populære valg basert på navigasjonshierarkier.

Før "Plukkinger for deg"-listen kan vises på en e-handelsside, må følgende brukerkrav oppfylles:

- Brukere må være logget på. Anonyme brukere kan ikke se tilpassede anbefalinger.
- Brukere må ha minst ett innkjøp på kontoen.
- Brukere må velge å motta personlige anbefalinger.

Illustrasjonen nedenfor viser et eksempel på en "Plukkinger for deg"-liste på en nettbutikkside.

!["Plukkinger for deg"-liste på Internett.](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>"Anbefalt for kunde"-lister på salgsstedet

For å forbedre klientopplevelsen kan forhandlerne personliggjøre eksisterende kundedetaljsider ved å legge til en kontekstbasert "Anbefalt for kunde"-liste.

Illustrasjonen nedenfor viser et eksempel på en "Anbefalt for kunde"-liste på en salgsstedsterminal.

!["Anbefalt for kunde"-liste på salgsstedet.](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Bruke tilpassing på eksisterende anbefalingslister

Forhandlere kan bruke tilpassing for eksisterende anbefalingslister, for eksempel "Ny", "Tendenser", "Besteselgere", "Andre liker også" og "Ofte kjøpt sammen". Når tilpassing brukes på eksisterende lister, fjernes varer som en pålogget bruker tidligere har kjøpt, fra disse listene. For både anonyme brukere og brukere som har valgt bort mottak av tilpasssede anbefalinger, vises standardversjoner av de eksisterende listene. Derfor trenger ikke forhandlere å opprettholde separate sideopplevelser manuelt.

En pålogget bruker har for eksempel allerede kjøpt den svarte klokken og de brune arbeidsstøvlene som vises i listen "Tendenser – standard" i følgende illustrasjon. Derfor vil brukeren se nye produkter i stedet for disse produktene, som vist i listen "Tendenser – tilpasset".

![Bruke tilpassing.](./media/applypersonalization.png)

Hvis du vil bruke tilpassing på en eksisterende anbefalingsliste i områdebygger for handel, følger du denne fremgangsmåten.

1. Åpne en eksisterende områdebyggerside som inneholder en produktsamlingsmodul.
1. Velg produktsamlingsmodulen i den venstre navigasjonsruten.
1. Velg listen i den høyre navigasjonsruten under **Produkter**.
1. I dialogboksen **Velg produktlistekonfigurasjon**, under **Type**, velger du listetypen.
1. Merk av for **Bruk tilpassing**, og velg deretter **OK**.

    ![Bruke tilpassing på en tendensliste.](./media/ApplyPersonalizationToTrending.PNG)

1. Lagre siden, fullfør redigeringen av den, og publiser den. Når siden er publisert, vil påloggede brukere se tilpassede tendenslister.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere Kjøp lignende utseender-anbefalinger](shop-similar-looks.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
