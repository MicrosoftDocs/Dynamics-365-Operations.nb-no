---
title: Produktsamlingsmoduler
description: Dette emnet gir en oversikt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 01/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7bc76aa8d5728005711ee8f9758532a989e3568c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984550"
---
# <a name="product-collection-modules"></a>Produktsamlingsmoduler

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.

Produktgjenkjenning er et primærverktøy som forhandlere bruker for å engasjere seg med kundene på et webområde for e-handel. Produktsamlingsmoduler hjelper forhandlere med å bygge overbevisende handleopplevelser ved å tilby et intuitivt, visuelt grensesnitt som kan brukes til å utforme produktsamlinger raskt.

Produktsamlingsmoduler representerer fysiske produkter og tjenester på webområdet. En produktsamlingsmodul er vanligvis koblet til en detaljside der kunder kan kjøpe et produkt eller en tjeneste, eller lære mer om den. 

Kildene for produktsamlinger kan være lister med følgende fire typer:

- Redigeringslister med produkter som er manuelt definert i Dynamics 365 Commerce som tilknyttede produkter for et produkt, eller produktlister
- Lister over algoritmer, for eksempel lister over nye, bestselgende eller tendenser
- Anbefalingslister som er basert på maskinopplæring
- Tilpasningslister som støtter personlige resultater for en kunde. Kunder må være logget på webområdet for e-handel for å se personlige resultater. Gjestebrukere ser ikke personlige resultater. Kunder kan velge bort personlig tilpasning fra [siden for kontoadministrasjon](account-management.md).

Følgende illustrasjon viser de ulike typene produktsamlinger som brukes på et e-handelsområde.

![Eksempel på de ulike typene produktsamlinger på et e-handelsområde.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Bruk alltid produktsamlingsmoduler til å vise en gruppe med produkter av en lignende type.

## <a name="product-collection-modules-and-types"></a>Produktsamlingsmoduler og -typer

Følgende tabell beskriver ulike typer produktsamlingsmoduler i Dynamics 365 Commerce.

| Produktsamlingsmodul  | Type | Beskrivelse |
|----------------------------|------|-------------|
| Kategori                   | Kategori | Denne modulen viser en liste over produkter i en kategori, som definert av navigasjonskategorihierarkiet som forhandleren opprettet for en kanal. |
| Relaterte produkter           | Redaksjonell | Denne modulen viser en liste over produkter som en salgssjef har konfigurert som tilknyttede produkter i Commerce for relasjonstypen som forfatteren har valgt. |
| Søkeresultater             | Søkespørring | Denne typen produktsamlingsmodul viser en liste over produkter som passer best til søkespørringen som kunden har angitt. |
| Kuraterte produktlister      | Redaksjonell | Denne modulen viser egendefinerte lister som forhandlere og redaktører har opprettet i Commerce. |
| Nye                        | Algoritme | Denne modulen viser en liste over de nyeste produktene som er assortert til kanaler og kataloger. Denne listen kan vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet. |
| Bestselgere               | Algoritme | Denne modulen viser en liste over produkter som er rangert etter det høyeste salgstallet. Denne listen kan vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet. |
| Populære                   | Algoritme | Denne modulen viser en liste over produkter med høyest ytelse for en gitt periode. Denne listen kan vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet. |
| Kjøpes ofte sammen | Kunstig intelligens / maskinlæring | Denne modulen bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale relaterte varer som kjøpes ofte sammen med et gitt produkt. Denne listen kan vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet. |
| Andre liker også           | Kunstig intelligens / maskinlæring | Denne modulen bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale varer som er relatert til et gitt produkt. Denne listen kan vise personlige resultater for en pålogget bruker hvis områdeforfatteren velger dette alternativet. |
| Plukkinger for deg              | Kunstig intelligens / maskinlæring | Denne modulen bruker maskinlæring til å analysere kjøpsmønstrene for den påloggede brukeren og gi personlige anbefalinger som er basert på disse kjøpsmønstrene. For en gjestebruker vil denne listen være skjult. |

## <a name="supported-modules"></a>Støttede moduler 

Produktsamlingsmodulen støtter [hurtigvisningsmodulen](quick-view-module.md), som gjør det mulig for brukere å vise produktinformasjon og legge til varer i handlekurven fra en produktsamlingsside.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Legge til en produktsamlingsmodul på en kategoriside

Følg disse trinnene for å legge til en produktsamlingsmodul på en kategoriside.

1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du den samme malen som brukes av standardkategorisiden. Under **Sidenavn** angir du et egnet navn og deretter **OK**.
1. I **Underbunntekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Produktsamling**-modulen, og deretter velger du **OK**.  
1. I egenskapsruten for produktsamlingsmodulen velger du **Legg til en produktliste**.
1. I dialogboksen **Velg produktlistekonfigurasjon** velger du listetype, listekilden, og deretter angir du antall varer. Konfigurer eventuelle andre alternativer som er tilgjengelige for listetypen. Hvis du vil ha mer informasjon om listetyper, kan du se tabellen nedenfor. 
1. Velg **OK**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

Følgende tabell viser listetypene som er tilgjengelige for valg i dialogboksen **Velg produktlistekonfigurasjon**.

| Type                       | Beskrivelse | Bruk | Sidekontekst | Bestemt kontekst | Tilpassing |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produkter etter kategori       | En liste over produkter som tilhører en gitt kategori. Denne kategorien bestemmes enten fra sidekonteksten eller konteksten som forfatteren gir. | Denne typen liste kan brukes på en hvilken som helst side (for eksempel en startside, en kategoriside, en markedsføringsside eller en produktdetaljside \[PDP\]) for å promotere en bestemt kategori av produkter. | Kategori fra sidekonteksten, der det er tilgjengelig (for eksempel en kategoriside) | Forfatteren kan gi en bestemt kategori som kontekst for listen. | Gjelder ikke |
| Relaterte produkter           | En liste over produkter som en varehandelsleder har konfigurert som tilknyttede produkter i Commerce for relasjonstypen. | Denne typen liste brukes først og fremst på PDP-er, men den kan brukes på alle sider hvis et overordnet produkt er angitt. | Produkt fra siden, relasjonstype (obligatorisk) | Produktet kan velges i velgeren, og relasjonstypen brukes. | Gjelder ikke |
| Kuratert                    | En egendefinert liste som forhandlere og redaktører har opprettet i Commerce. | Supplere kategoriside, startside, betalings- og handlekurvsider, og produktsider | Gjelder ikke | Gjelder ikke | Gjelder ikke |
| Algoritme                | <ul><li>**Ny** – En liste over de nyeste produktene som er assortert til kanaler og kataloger.</li><li>**Bestselgere** – En liste over produkter som er rangert etter det høyeste salgstallet.</li><li>**Stjerneskudd** – En liste over produkter med høyest ytelse for en gitt periode.</li></ul> | Startside, suppler kategoriside, og betalings- og handlekurvsider | Kategori fra sidekonteksten (for eksempel en kategoriside) | Kategorien som bestemmes av områdeforfatteren | Støttes |
| Kjøpes ofte sammen | En liste som bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale relaterte varer som kjøpes ofte sammen med et gitt produkt. | Denne typen liste er bare tilgjengelig for handlevognsiden. | Handlekurv | Gjelder ikke | Støttes |
| Andre liker også           | En liste som bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale varer som er relatert til et gitt produkt. | Denne typen liste brukes på PDP-er for å vise produkter som andre kunder har kjøpt. | Produktkontekst fra siden | Produktet som leveres av områdeforfatteren | Støttes |
| Plukkinger for deg              | En liste som bruker maskinlæring til å avgjøre kundenes preferanser. | Denne typen liste kan brukes på en hvilken som helst side. | Gjelder ikke| Gjelder ikke | Støttes | 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokkmodul](add-content-rich-block.md)

[Beholdermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Oversikt over produktanbefalinger](product-recommendations.md)

[Hurtigvisningsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
