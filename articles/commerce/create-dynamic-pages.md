---
title: Opprette dynamiske e-handelssider basert på URL-parametere
description: Denne artikkelen beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.
author: bicyclingfool
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 718bc099347f2924b299ccd4562d9d7055c43187
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282883"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>Opprette dynamiske e-handelssider basert på URL-parametere

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer en e-handelside i Microsoft Dynamics 365 Commerce som kan ha dynamisk innhold basert på URL-parametere.

En e-handelsside kan konfigureres til å ha forskjellig innhold, basert på et segment i URL-banen. Derfor kalles siden en dynamisk side. Segmentet brukes som en parameter for å hente sideinnholdet. For eksempel vil en side som opprettes i områdebyggeren og kalt **blogg\_fremviser** tilordnes til URLen `https://fabrikam.com/blog`. Denne siden kan deretter brukes til å vise forskjellig innhold, basert på det siste segmentet i URL-banen. Eksempelvis er det siste segmentet i URL-adressen `https://fabrikam.com/blog/article-1` **artikkel-1**.

Du kan også overstyre et parameterisert URL-segment med en side for områdekonfigurator. For eksempel kan en side som opprettes i områdebyggeren og kalt **blogg\_sammendrag** tilordnes til URLen `https://fabrikam.com/blog/about-this-blog`. Når URL-adressen `https://fabrikam.com/blog` forespørres med segmentet `/about-this-blog` på slutten, returneres siden **blogg\_sammendrag** i stedet for at segmentet `/about-this-blog` som tolkes som en parameter som brukes av siden `https://fabrikam.com/blog`. 

Når du velger navn for parameterne som skal sendes til den dynamiske siden, kan navnet på den dynamiske siden slik det vises i URL-adressen (`/blog` i eksempelet ovenfor) ikke brukes som et parameternavn eller en understreng av et parameternavn. 

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

Når ruten er konfigurert, vil alle forespørsler til den parameteriserte URL-banen returnere siden som er knyttet til denne URL-adressen. Hvis det finnes forespørsler som inneholder et ekstra segment, returneres den tilknyttede siden, og innholdet på siden hentes ved å bruke segmentet som en parameter. Eksempelvis vil `https://fabrikam.com/blog/article-1` returnere siden `https://fabrikam.com/blog` som viser innholdet som hentes ved hjelp av parameteren **/artikkel-1**.

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
