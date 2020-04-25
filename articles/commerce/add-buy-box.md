---
title: Kjøpsboksmodul
description: Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261404"
---
# <a name="buy-box-module"></a>Kjøpsboksmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Begrepet *kjøpsboks* refererer vanligvis til området på en produktdetaljside som er "over folden", og som er vert for all viktig informasjon som kreves for å opprette et produktinnkjøp. (Et område som er "over folden", er synlig når siden lastes inn for første gang, slik at brukere ikke behøver å rulle ned for å se det.)

En kjøpsboks-modul er en spesiell container som brukes til å være vert for alle modulene som vises i innkjøpsboksområdet på en side i produktdetaljer.

URL-adressen til en produktdetaljside inneholder produkt-IDen. All informasjon som kreves for å vise en kjøpsboksmodul, er avledet fra denne produkt-IDen. Hvis det ikke er angitt noen produkt-ID, vil ikke modulen kjøpsboks vises riktig på en side. Derfor kan en kjøpsboksmodul bare brukes på sider som har produktkontekst. Hvis du vil bruke den på en side som ikke har produktkontekst (for eksempel en startside eller en markedsføringsside), må du gjøre flere tilpasninger.

## <a name="buy-box-module-properties-and-slots"></a>Egenskaper og spor for kjøpsboksmodul 

På en produktdetaljside er en kjøpsboks delt inn i to områder: et medieområde til venstre og et innholdsområde til høyre. Som standard er forholdet mellom bredden på medieområdekolonnen og bredden på innholdsområdekolonnen 2:1. På mobilenheter er det stablet to områder, slik at ett område vises under det andre området. Temaer kan brukes til å tilpasse kolonnebreddene og stablet rangering.

En kjøpsboksmodul gjengir tittel, beskrivelse, pris og vurdering av et produkt. Den lar også kunder velge produktvarianter som har forskjellige produktattributter, for eksempel størrelse, stil og farge. Når en produktvariant velges, oppdateres andre egenskaper i kjøpsboksen (for eksempel produktbeskrivelsen og bildene) for å gjenspeile variantinformasjonen. 

Det er angitt en antallsvelger, slik at kunder kan angi antallet varer som skal kjøpes. Det maksimale antallet som kan kjøpes, kan defineres i områdeinnstillingene.

Fra kjøpsboksen kan kunder også utføre handlinger som å legge til produkter i handlekurven, legge til produkter i ønskelisten og velge plukklokasjon. Disse handlingene kan utføres på et produkt eller en produktvariant. For å kunne legge til et produkt i en ønskeliste må kunden være pålogget.

Temaer kan brukes til å fjerne eller endre rekkefølgen på produktegenskaper og handlingskontroller i en kjøpsboks. 

## <a name="module-properties"></a>Modulegenskaper

- **Overskriftsetikett** – Denne egenskapen definerer overskriftsetiketten for produkttittelen. Hvis kjøpsboksen er øverst på siden, bør denne egenskapen settes til **h1** for å oppfylle tilgjengelighetsstandardene. 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler som kan brukes i kjøpsboksmodulen

- **Mediegalleri** – Denne modulen brukes til å vise bilder av et produkt på en produktdetaljside. Den kan støtte ett til mange bilder. Den støtter også miniatyrbilder. Miniatyrbildene kan ordnes enten vannrett (som en rad under bildet) eller loddrett (som en kolonne ved siden av bildet). Mediegalleri-modulen kan legges til i **Medie**-sporet i kjøpsboksmodulen. Den støtter for øyeblikket bare bilder. 
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).

## <a name="buy-box-module-settings"></a>Innstillinger for kjøpsboksmodul

Kjøpsboksmoduler har tre innstillinger som kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager. Denne lagerkontrollen utføres for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken. Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres. Hvis du vil ha informasjon om hvordan du konfigurerer lagerinnstillinger i back office, kan du se [Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md).

- **Lagerbuffer** – Denne egenskapen brukes til å angi et bufferantall for lageret. Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall. Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager. Derfor, når salget skjer raskt i flere kanaler og lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Modulen kjøpsboks henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Produkt-IDen fra produktdetaljersiden brukes til å hente all informasjon.

## <a name="add-a-buy-box-module-to-a-page"></a>Legge til en kjøpsboksmodul på en side

Hvis du vil legge til en kjøpsboksmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett et fragment kalt **kjøpsboksfragment**, og legg til en kjøpsboksmodul i den.
1. I **Media**-sporet i kjøpsboksmodulen legger du til en mediegallerimodul.
1. I **Butikkvelger**-sporet i kjøpsboksmodulen legger du til en butikkvelgermodul.
1. Sjekk inn siden, og publiser den.
1. Opprett en mal for en produktdetaljside, og gi den navnet **PDP-mal**.
1. Legg til en standardside.
1. I **Hoved**-sporet på standardsiden legger du til et kjøpsboksfragment.
1. Lagre malen, fullfør redigeringen av den, og publiser den.
1. Bruk malen du nettopp opprettet, for å opprette en side som heter **PDP-side**.
1. I **Hoved**-sporet på den nye siden legger du til et kjøpsboksfragment.
1. Lagre og forhåndsvis siden. Legg til spørringsstrengparameteren **?productid=&lt;product id&gt;** i URL-adressen for forhåndsvisningssiden. På den måten brukes produktkonteksten til å laste inn og gjengi forhåndsvisningssiden.
1. Lagre siden, fullfør redigeringen av den, og publiser den. En kjøpsboks skal vises på siden for produktdetaljer.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Butikkvelgermodul](store-selector.md)

[Containermodul](add-container-module.md)

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)
