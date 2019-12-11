---
title: Produktsamlingsmoduler
description: Dette emnet gir en oversikt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785473"
---
# <a name="product-collection-modules"></a>Produktsamlingsmoduler  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over produktsamlingsmoduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Produktgjenkjenning er et primærverktøy som forhandlere bruker for å engasjere seg med kundene på et webområde for e-handel. Produktsamlingsmoduler hjelper forhandlere med å bygge overbevisende handleopplevelser ved å tilby et intuitivt, visuelt grensesnitt som kan brukes til å utforme produktsamlinger raskt.

Produktsamlingsmoduler representerer fysiske produkter og tjenester på webområdet. En produktsamlingsmodul er vanligvis koblet til en detaljside der kunder kan kjøpe et produkt eller en tjeneste, eller lære mer om den. 

Kildene for produktsamlinger kan være lister med tre typer:

- Redigeringslister med produkter som er manuelt definert i Dynamics 365 Retail som tilknyttede produkter for et produkt, eller produktlister
- Lister over algoritmer, for eksempel lister over nye, bestselgende eller tendenser
- Anbefalingslister som er basert på maskinopplæring

Følgende illustrasjon viser de ulike typene produktsamlinger som brukes på et e-handelsområde.

![Eksempel på de ulike typene produktsamlinger på et e-handelsområde](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Bruk alltid produktsamlingsmoduler til å vise en gruppe med produkter av en lignende type eller et lignende tema.

## <a name="product-collection-modules-and-types"></a>Produktsamlingsmoduler og -typer

Følgende tabell beskriver ulike typer produktsamlingsmoduler i Dynamics 365 Commerce.

| Produktsamlingsmodul  | Type | Beskrivelse |
|----------------------------|------|-------------|
| Kategorisøk            | Redaksjonell | Denne typen produktsamlingsmodul bruker navigasjonskategorihierarkiet som detaljhandeleren opprettet for en detaljhandelskanal, til å vise en nettleserflyt for produkter som tilbys i en bestemt områdekategori. |
| Søkeresultater             | Søkespørring | Denne typen produktsamlingsmodul viser en liste over produkter som passer best til søkespørringen som kunden har angitt. |
| Relaterte produkter           | Redaksjonell | Denne typen produktsamlingsmodul viser en liste over produkter som en salgssjef har konfigurert som tilknyttede produkter i detaljhandel for relasjonstypen som forfatteren valgte. |
| Kuraterte produktlister      | Redaksjonell | Denne typen produktsamlingsmodul viser egendefinerte lister som forhandlere og redaktører har opprettet i Retail. |
| Nye                        | Algoritme | Denne typen produktsamlingsmodul viser en liste over de nyeste produktene som er assortert til kanaler og kataloger. |
| Bestselgere               | Algoritme | Denne typen produktsamlingsmodul viser en liste over produkter som er rangert av det høyeste salgsantallet. |
| Populære                   | Algoritme | Denne typen produktsamlingsmodul viser en oversikt over produkter med høyest ytelse for en gitt periode. |
| Kjøpes ofte sammen | Kunstig intelligens / maskinlæring | Denne typen produktsamlingsmodul bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale relaterte varer som kjøpes ofte sammen med et gitt produkt. |
| Andre liker også           | Kunstig intelligens / maskinlæring | Denne typen produktsamlingsmodul bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale varer som er relatert til et gitt produkt. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Legge til en produktsamlingsmodul på en kategoriside

Følg disse trinnene for å legge til en produktsamlingsmodul på en kategoriside.

1. I Dynamics 365 Commerce går du til området og oppretter en side som bruker den samme malen som standard kategoriside.
1. På sideoppsettet velger du sporet for **Underbunntekst**, velger ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Container**, og deretter velger du **OK**.
1. I containermodulen velger du ellipseknappen, og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Produktsamling**, og deretter velger du **OK**.
1. Konfigurer innstillinger for å velge aktuell datakilde og inndata for produktsamlingen.
1. I egenskapsruten for produktsamlingsmodulen velger du **Legg til en produktliste**.
1. I dialogboksen **Velg produktlistekonfigurasjon** velger du listetype, angir antall varer og velger eventuelle andre alternativer som er tilgjengelige for listetypen. Hvis du vil ha mer informasjon om listetyper, kan du se tabellen nedenfor. 
1. Velg **OK**.
1. Lagre siden, og publiser den.

Følgende tabell viser listetypene som er tilgjengelige for valg i dialogboksen **Velg produktlistekonfigurasjon**.
   
| Type                       | Beskrivelse | Generell fremgangsmåte | Kontekst som kan avledes fra sidekonteksten | Kontekst som forfatteren kan overstyre sidekonteksten med |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Produkter etter kategori       | En liste over produkter som tilhører en gitt kategori. Denne kategorien bestemmes enten fra sidekonteksten eller konteksten som forfatteren gir. | Supplere kategoriside, startside, betalings- og handlekurvsider, og produktsider | Kategori | Kategori bestemmes av forfatter |
| Relaterte produkter           | En liste over produkter som en varehandelsleder har konfigurert som tilknyttede produkter i Retail for relasjonstypen. | Produktsider, betalings- og handlekurvsider, ønskelisteside og kundekontoside | Produkt, relasjonstype (obligatorisk)  | Produkt, relasjonstype |
| Kuratert                    | En egendefinert liste som forhandlere og redaktører har opprettet i Retail. | Supplere kategoriside, startside, betalings- og handlekurvsider, og produktsider | Gjelder ikke | Listeplukker |
| Algoritme                | <ul><li>**Ny** – En liste over de nyeste produktene som er assortert til kanaler og kataloger.</li><li>**Bestselgere** – En liste over produkter som er rangert etter det høyeste salgstallet.</li><li>**Stjerneskudd** – En liste over produkter med høyest ytelse for en gitt periode.</li></ul> | Startside, suppler kategoriside, og betalings- og handlekurvsider | Kategori | Kategori bestemmes av forfatter |
| Kjøpes ofte sammen | En liste som bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale relaterte varer som kjøpes ofte sammen med et gitt produkt. | Produktsider og betalings- og handlekurvsider | Produkt, handlekurv | Inkluder handlekurv |
| Andre liker også           | En liste som bruker maskinopplæring til å analysere forbrukskjøpsmønstre og anbefale varer som er relatert til et gitt produkt. | Produktsider og betalings- og handlekurvsider | Produkt, handlekurv | Gjelder ikke |

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

