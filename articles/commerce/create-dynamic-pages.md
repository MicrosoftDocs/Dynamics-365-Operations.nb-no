---
title: Opprette dynamiske e-handelssider basert på URL-parametere
description: Dette emnet beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795817"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Opprette dynamiske e-handelssider basert på URL-parametere

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.

En e-handelsside kan konfigureres til å ha forskjellig innhold, basert på et segment i URL-banen. Derfor kalles siden en dynamisk side. Segmentet brukes som en parameter for å hente sideinnholdet. Det vil for eksempel opprettes en side med navnet **blogg\_fremviser** som knyttes til URL-adressen `https://fabrikam.com/blog`. Denne siden kan deretter brukes til å vise forskjellig innhold, basert på det siste segmentet i URL-banen. Eksempelvis er det siste segmentet i URL-adressen `https://fabrikam.com/blog/article-1` **artikkel-1**.

Separate egendefinerte sider som overstyrer den dynamiske siden, kan også knyttes til segmenter i URL-banen. Det vil for eksempel opprettes en side med navnet **blogg\_sammendrag** som knyttes til URL-adressen `https://fabrikam.com/blog/about-this-blog`. Når denne URL-adressen forespørres, returneres **blogg\_sammendrag**-siden som er knyttet til paramenteren **/about-this-blog** i stedet for siden **blogg\_fremviser**.

> [!NOTE]
> Funksjonaliteten for mottak, henting og visning av dynamisk sideinnhold implementeres ved hjelp av en egendefinert modul. Hvis du vil ha mer informasjon, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Definere en dynamisk e-handelsside

Hvis du vil definere en dynamisk e-handelside, må du opprette den dynamiske siden, opprette basis-URLen og konfigurere ruten til den dynamiske siden.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Opprette en side som inneholder dynamisk innhold

Følg trinnene i [Legg til en ny områdeside](add-new-page.md) for å opprette en side som inneholder dynamisk innhold. Siden du oppretter, krever implementering av en modul som bruker det siste segmentet i URL-banen til å hente innhold fra en ekstern datakilde. Hvis du vil ha mer informasjon om utvikling av egendefinerte moduler, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Opprette basis-URLen for den dynamiske siden

Følg denne fremgangsmåten for å opprette basis-URLen for den dynamiske siden i Commerce-områdebyggeren.

1. Gå til **URL-adresser**, og velg **Ny \> Ny URL-adresse**.
1. Velg **Intern side** i dialogboksen **Opprett ny URL-adresse**. Under **URL-bane** angir du banen som skal fungere som roten for den dynamiske siden (i dette eksemplet **/blogg**). Velg deretter **Neste**.
1. I dialogboksen **Velg en side** velger du siden du opprettet som dynamisk side, og deretter velger du **Lagre**.
1. Velg **Publiser**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Konfigurere ruten til den dynamiske siden

Følg denne fremgangsmåten for å konfigurere ruten til den dynamiske siden i Commerce-områdebyggeren.

1. Gå til **Områdeinnstillinger \> Tillegg**.
1. Under **Parameteriserte URL-baner** velger du **Legg til**, og deretter legger du inn URL-banen du skrev inn da du opprettet URL-adressen (i dette eksemplet **/blogg**).
1. Velg **Lagre og publiser**.

Når ruten er konfigurert, vil alle forespørsler til den parameteriserte URL-banen returnere siden som er knyttet til denne URL-adressen. Hvis det finnes forespørsler som inneholder et ekstra segment, returneres den tilknyttede siden, og innholdet på siden hentes ved å bruke segmentet som en parameter. Eksempelvis vil `https://fabrikam.com/blog/article-1` returnere siden **blogg\_sammendrag**, og sideinnholdet hentes ved hjelp av parameteren **/artikkel-1**.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Overstyre en parameterisert URL-adresse med en egendefinert side

Følg denne fremgangsmåten for å overstyre en parameterisert URL-adresse med en egendefinert side i Commerce-områdebyggeren.

1. Gå til **URL-adresser**, og velg **Ny \> Ny URL-adresse**.
1. Velg **Intern side** i dialogboksen **Opprett ny URL-adresse**. Under **URL-bane** angir du banen som inkluderer segmentet som skal overstyres (i dette eksemplet **/blogg/about-this-blog**). Velg deretter **Neste**.
1. Velg den egendefinerte siden, og velg deretter **Lagre** i dialogboksen **Velg en side**.
1. Velg **Publiser**.
1. Hvis den egendefinerte siden ennå ikke er publisert, kan du gå til **Sider**, velge den egendefinerte siden og deretter velge **Publiser**.

Når den egendefinerte siden er publisert, blir den vist i stedet for den dynamiske siden som har parameterisert innhold.

## <a name="additional-resources"></a>Tilleggsressurser

[Endre en eksisterende områdeside](modify-existing-page.md)

[Legg til en ny områdeside](add-new-page.md)

[Velge sideoppsett](select-page-layouts.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)

[Lagre, forhåndsvise og publisere en side](save-preview-publish-page.md)

[Supplere en produktside](enrich-product-page.md)

[Supplere en kategorimålside](enrich-category-page.md)

[Kontrollere tilgjengelighet for sideinnhold](verify-accessibility.md)

[Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
