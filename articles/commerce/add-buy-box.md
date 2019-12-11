---
title: Kjøpsboksmodul
description: Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811147"
---
# <a name="buy-box-module"></a>Kjøpsboksmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Begrepet *kjøpsboks* refererer vanligvis til området på en produktdetaljside som er "over folden", og som er vert for all viktig informasjon som kreves for å opprette et produktinnkjøp. (Et område som er "over folden", er synlig når siden lastes inn for første gang, slik at brukere ikke behøver å rulle ned for å se det.)

En kjøpsboks-modul er en spesiell container som brukes til å være vert for alle modulene som vises i innkjøpsboksområdet på en side i produktdetaljer.

URL-adressen til en produktdetaljside inneholder produkt-IDen. All informasjon som kreves for å vise en kjøpsboksmodul, er avledet fra denne produkt-IDen. Hvis det ikke er angitt noen produkt-ID, vil ikke modulen kjøpsboks vises riktig på en side. Derfor kan ikke en modul for kjøpsboks brukes på sider som ikke har produktkontekst (for eksempel en hjemmeside eller en markedsføringsside).

## <a name="buy-box-module-properties-and-slots"></a>Egenskaper og spor for kjøpsboksmodul 

Som en container styrer en kjøpsboksmodul enkelte grunnleggende egenskaper, for eksempel bredden. Breddeinnstillingen bestemmer om modulene i beholderen må passe i denne beholderen, eller om de kan fylle skjermen.

På en produktdetaljside er en kjøpsboks delt inn i to områder: et medieområde til venstre og et innholdsområde til høyre. Disse to områdene representeres av spor i kjøpsboksmodulen. Hvert spor forhåndskonfigurers til å bare godta bestemte moduler som støttes av sporet. Et **Medie**-spor støtter for eksempel bare mediegallerimodulen.

Som standard er raten for kolonnebredder for medieområdet og innholdsområdet 2:1. Kolonnebreddene kan imidlertid overstyres av temaet. På mobilenheter er det i tillegg stablet to regioner, slik at én region vises under det andre området.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler som kan brukes i kjøpsboksmodulen

- **Mediegalleri** – Denne modulen brukes til å vise bilder av et produkt på en produktdetaljside. Den kan støtte ett til mange bilder. Den støtter også miniatyrbilder. Miniatyrbildene kan ordnes enten vannrett (som en rad under bildet) eller loddrett (som en kolonne ved siden av bildet). Mediegalleri-modulen kan legges til i **Medie**-sporet i kjøpsboksmodulen. Den støtter for øyeblikket bare bilder og videoer.
- **Produkttittel** – Denne modulen viser tittelen på produktet på en produktdetaljside. Som standard **H1**-overskriftskoden, men overskriftskoden kan endres etter behov.
- **Produktvurdering** – Denne modulen viser stjerneklassifiseringer basert på kundevurderinger for et produkt. Modulen for kjøpsboks henter produktvurderingene for hvert av produktene fra sensurtjenesten.
- **Produktpris** – Denne modulen viser prisen på produktet. Prisen omfatter gjennomstreking av priser og rabatter.
- **Produktbeskrivelse** – Denne modulen viser beskrivelsen av produktet.
- **Produktkonfigurasjon** – Denne modulen viser størrelse, stil og dimensjoner for produktet. Dimensjonsvelgerne kan stables loddrett, eller de kan vises side ved side. Når en produktvariant velges, oppdateres andre egenskaper i kjøpsboksen (for eksempel produktbeskrivelsen og bildene) for å gjenspeile variantinformasjonen.
- **Produktantall** – Denne modulen brukes til å konfigurere antallet for produktet. En innstilling begrenser antallet av en vare eller variant som kan legges til i handlekurven.
- **Legg i handlekurv** – Denne modulen brukes til å utføre handlingen "legg til i handlekurven". Bare en vare eller en variant kan legges til i handlekurven. Et hovedprodukt kan med andre ord ikke legges til i handlekurven. Modulen har en **Naviger til handlekurv**-egenskap som områdeforfatteren kan angi. Når denne egenskapen er satt til **Sann**, tas brukeren til handlekurvsiden hver gang en "legg til en handlekurv"-handling utløses. Når den er satt til **Usann**, kan kunden fortsette å bla på produktdetaljsiden etter at varene er lagt til i handlekurven.
- **Legg til på ønskeliste** – Denne modulen brukes til å legge til en vare i kundens ønskeliste. Bare en vare eller en variant kan legges til i en ønskeliste. I tillegg må kunden være logget på området. Modulen inneholder en feilbehandlingslogikk for å sikre at begge disse vilkårene oppfylles.
- **Finn i butikk** – Denne modulen utløser flyten "Kjøpe på Internett og hente i butikk".
- **Hent i butikk** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Som standard viser denne modulen butikker som er innen en 50 kilometers radius til kundenslokasjonen. Radiusen for søk kan imidlertid tilpasses i modulen. For hver butikk utføres det en lagerkontroll, hvis lagerkontrollfunksjonaliteten er aktivert, og det vises en gjeldende på lager- eller tomt-melding.
- **Butikksøk etter Bing-kart** – Denne modulen kan brukes i hente i butikk-modulen. Den lar kunder søke etter butikker ved å angi en lokasjon. APIen (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet brukes til å konvertere den angitte lokasjonen til en breddegrad og en lengdegrad. Hvis denne modulen brukes, vises bare butikker som er nær kundens gjeldende lokasjon, og kunden kan ikke søke etter en annen lokasjon.
- **Innholdsrik blokk** – Denne modulen kan vise en melding som områdeforfatteren eller forhandleren vil vise i kjøpsboksen, for eksempel "For problemer med ordren, kontakt 1-800-FABRIKAM" eller "Gratis frakt for ordrer over 1000 kroner. " Meldingene drives av innholdsbehandlingssystemet (CMS).

## <a name="buy-box-module-settings"></a>Innstillinger for kjøpsboksmodul

Kjøpsboksmoduler har tre innstillinger som kan konfigureres:

- **Maksimalt antall** – Maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager. Denne lagerkontrollen utføres både for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken. Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.
- **Lagerbuffer** – Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall. Derfor kan en buffer defineres for lager. Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager. Derfor, når salget skjer raskt i flere kanaler, slik at lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.

## <a name="retail-server-interaction"></a>Interaksjon med detaljhandelsserver

Modulen kjøpsboks henter produktinformasjon ved hjelp av API-er for Retail Server. Produkt-IDen fra produktdetaljersiden brukes til å hente all informasjon.

## <a name="add-a-buy-box-module-to-a-page"></a>Legge til en kjøpsboksmodul på en side

Hvis du vil legge til en kjøpsboksmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett et fragment kalt **kjøpsboksfragment**, og legg til en kjøpsboksmodul i den.
1. I **Media**-sporet i kjøpsboksmodulen legger du til en mediegallerimodul.
1. I **Innhold**-sporet i modulen kjøpsboks legger du til følgende moduler: produkttittel, produktvurdering, produktpris, produktbeskrivelse, produktkonfigurasjon, legge til i handlekurv, legge til i ønskeliste og finn i butikk. Du kan ordne modulene i **Innhold**-sporet på nytt for å oppnå ønsket oppsett.
1. Velg Finn i butikk-modulen. Legg til en plukking i butikkmodulen i sporet i denne modulen.
1. I sporet i plukkingen i butikkmodulen legger du til et butikksøk etter Bing-kart-modulen.
1. Sjekk inn siden, og publiser den.
1. Opprett en mal for en produktdetaljside, og gi den navnet **PDP-mal**.
1. Legg til en standardside.
1. I **Hoved**-sporet på standardsiden legger du til et kjøpsboksfragment.
1. Lagre malen, sjekk den inn og publiser den.
1. Bruk malen du nettopp opprettet, for å opprette en side som heter **PDP-side**.
1. I **Hoved**-sporet på den nye siden legger du til et kjøpsboksfragment.
1. Lagre og forhåndsvis siden. Legg til spørringsstrengparameteren **?productid=&lt;product id&gt;** i URL-adressen for forhåndsvisningssiden. På den måten brukes produktkonteksten til å laste inn og gjengi forhåndsvisningssiden.
1. Sjekk inn siden, og publiser den. En kjøpsboks skal vises på siden for produktdetaljer.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
