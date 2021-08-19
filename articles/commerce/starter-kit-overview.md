---
title: Oversikt over modulbibliotek
description: Dette emnet viser en oversikt over modulbiblioteket for Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f1301f61e6bc0d408d4883b238808f66b14abc2d372e97671c71ba7dd5174124
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721982"
---
# <a name="module-library-overview"></a>Oversikt over modulbibliotek

[!include [banner](includes/banner.md)]

Dette emnet viser en oversikt over modulbiblioteket for Microsoft Dynamics 365 Commerce.

Modulbiblioteket for Dynamics 365 Commerce er en samling moduler som kan brukes til å bygge et webområde for e-handel. Moduler har både brukergrensesnittaspekter (UI) og funksjonelle virkemåteaspekter.

Temaer kan brukes på modulene i modulbiblioteket for å endre utseende og virkemåte. Temaene bruker gjennomgripende stilark (CSS). Et tema for et fiktivt e-handelsområde med navnet "Fabrikam" leveres som en del av modulbiblioteket og kan brukes som referanse.

## <a name="module-library-modules"></a>Modulbibliotekmoduler

Følgende modultyper finnes i modulbiblioteket:

- **Containermodul** – En containermodul er en enkel modul som fungerer som vert for andre moduler. Den kontrollerer oppsettet til modulene som er i det.
- **Markedsføringsmoduler** – Markedsføringsmoduler omfatter moduler for innholdsblokk, tekstblokk, videospiller og karusell. Alle disse modulene kan brukes til å vise innhold. De kan plasseres på en hvilken som helst side og er drevet av data fra et innholdsbehandlingssystem (CMS).
- **Topptekst- og bunntekstmoduler** – Topptekst- og bunntekstmoduler vises i topp- og bunnteksten på alle områdesider. Disse modulene kan konfigureres som obligatoriske via egenskaper.
- **Søkemoduler** – Produkter kan oppdages ved hjelp av søkemodulen i toppteksten. Søkeresultatene vises på søkeresultatsiden. Produkter kan også oppdages på kategorisider, som er dedikerte sider for hver kategori som støttes i kanalnavigeringshierarkiet. I tillegg kan presiseringsmoduler brukes til å filtrere resultater på søkeresultat- og kategorisider ytterligere.
- **Moduler for produktdetaljside** – Produktdetaljsider bruker flere moduler til å vise produktinformasjon. Kjøpsboksmodulen lar kundene vise produkter og legge dem til handlekurven. Andre moduler, som modulen for tekniske spesifikasjoner, viser produktdetaljene. Modulen for vurderinger og omtale kan brukes til å vise og gi vurderinger.
- **Modulen Kjøpe på Internett og hente i butikk** – Modulen Kjøpe på Internett og hente i butikk er integrert med Bing-kart. Den kan brukes til å finne nærliggende butikker der kunder kan plukke opp produkter de har kjøpt.
- **Innkjøpsmoduler** – Innkjøpsmoduler inkluderer handlekurvmodulen, som kan brukes til å legge varer i handlekurven. I kassemodulen registreres leveringsadresse, leveringsalternativer, gavekort, fordelsprogram og kredittkortinformasjon, slik at en ordre kan behandles. Etter at en ordre er lagt inn, kan ordrebekreftelsesmodulen brukes til å vise bekreftelsesdetaljene.
- **Kontobehandlingsmoduler** – Påloggingsmodulen lar kundene logge seg på en eksisterende konto, og registreringsmodulen lar dem opprette en ny konto. Når en konto er opprettet, kan du bruke ordrehistorikkmodulen til å vise de siste ordrene, og ordredetaljmodulen kan brukes til å vise ordredetaljer.
- **Anbefalinger-modulen** – Anbefalinger vises ved hjelp av produktplasseringsmodulen. Denne modulen støtter algoritmer og redigeringslister som kan vises på alle sider.

## <a name="additional-resources"></a>Tilleggsressurser

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]