---
title: Kjøpsboksmodul
description: Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ac29180dbffac4d7db27856b801647aac878bc99
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638031"
---
# <a name="buy-box-module"></a>Kjøpsboksmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker kjøpsboksmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Begrepet *kjøpsboks* refererer vanligvis til området på en produktdetaljside (PDP) som er "over folden", og som er vert for all viktig informasjon som kreves for å opprette et produktinnkjøp. (Et område som er "over folden", er synlig når siden lastes inn for første gang, slik at brukere ikke behøver å rulle ned for å se det.)

En kjøpsboks-modul er en spesiell container som brukes til å være vert for alle modulene som vises i innkjøpsboksområdet på en side i produktdetaljer.

URL-adressen til en produktdetaljside inneholder produkt-IDen. All informasjon som kreves for å vise en kjøpsboksmodul, er avledet fra denne produkt-IDen. Hvis det ikke er angitt noen produkt-ID, vil ikke modulen kjøpsboks vises riktig på en side. Derfor kan en kjøpsboksmodul bare brukes på sider som har produktkontekst. Hvis du vil bruke den på en side som ikke har produktkontekst (for eksempel en startside eller en markedsføringsside), må du gjøre flere tilpasninger.

Bildet nedenfor viser et eksempel på en kjøpsboks-modul på en side med produktinformasjon.

![Eksempel på en kjøpsboks-modul.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Egenskaper og spor for kjøpsboksmodul 

På en produktdetaljside er en kjøpsboks delt inn i to områder: et medieområde til venstre og et innholdsområde til høyre. Som standard er forholdet mellom bredden på medieområdekolonnen og bredden på innholdsområdekolonnen 2:1. På mobilenheter er det stablet to områder, slik at ett område vises under det andre området. Temaer kan brukes til å tilpasse kolonnebreddene og stablet rangering.

En kjøpsboksmodul gjengir tittel, beskrivelse, pris og vurdering av et produkt. Den lar også kunder velge produktvarianter som har forskjellige produktattributter, for eksempel størrelse, stil og farge. Når en produktvariant velges, oppdateres andre egenskaper i kjøpsboksen (for eksempel produktbeskrivelsen og bildene) for å gjenspeile variantinformasjonen. 

Det er angitt en antallsvelger, slik at kunder kan angi antallet varer som skal kjøpes. Det maksimale antallet som kan kjøpes, kan defineres i områdeinnstillingene.

Fra kjøpsboksen kan kunder også utføre handlinger som å legge til produkter i handlekurven, legge til produkter i ønskelisten og velge plukklokasjon. Disse handlingene kan utføres på et produkt eller en produktvariant. For å kunne legge til et produkt i en ønskeliste må kunden være pålogget.

Temaer kan brukes til å fjerne eller endre rekkefølgen på produktegenskaper og handlingskontroller i en kjøpsboks. 

## <a name="module-properties"></a>Modulegenskaper

- **Overskriftsetikett** – Denne egenskapen definerer overskriftsetiketten for produkttittelen. Hvis kjøpsboksen er øverst på siden, bør denne egenskapen settes til **h1** for å oppfylle tilgjengelighetsstandardene. 

- **Aktiver Kjøp lignende utseender-anbefalinger** – denne egenskapen lar innkjøpsboksen vise koblinger til produkter som ligner på det viste elementet. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.13 og nyere.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moduler som kan brukes i kjøpsboksmodulen

- **Mediegalleri** – Denne modulen brukes til å vise bilder av et produkt på en produktdetaljside. Hvis du vil ha mer informasjon om denne modulen, kan du se [Mediegallerimodul](media-gallery-module.md).
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Hvis du vil ha mer informasjon om denne modulen, kan du se [Butikkvelgermodul](store-selector.md).
- **Sosial deling** – denne modulen kan legges til i Kjøp-boksen for å gi brukere muligheten til å dele produktinformasjon på sosiale medier. Hvis du vil ha mer informasjon, se [Sosial deling-modulen](social-share-module.md).

## <a name="buy-box-module-settings"></a>Innstillinger for kjøpsboksmodul

Følgende innstillinger for kjøpsboks-modulen kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Antallsgrense for handlevogn-linjeelement** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Beholdning** – Hvis du vil ha informasjon om hvordan du bruker beholdningsinnstillinger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).
- **Legg til produkt i handlekurv** – Hvis du vil ha informasjon om hvordan du bruker innstillingene for **Legg til produkt i handlekurv**, kan du se [innstillingene for Legg til produkt i handlekurv](add-cart-settings.md).

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Definisjonstillegg for kjøpsboksmodul i Adventure Works-teamet

Kjøpsboksmodulen som Adventure Works-emnet tilbyr, har en moduldefinisjonsforlengelse som støtter implementering av en produktspesifikasjonsmodul i en trekkspillmodul i en PDP-kjøpsboks. Hvis du vil vise produktspesifikasjonsattributter i en PDP-kjøpsboks, legger du til en produktspesifikasjonsmodul i sporet for trekkspillmodulen i kjøpsbokssporet.


> [!IMPORTANT]
> Adventure Works-temaet er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.


## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Modulen kjøpsboks henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Produkt-IDen fra produktdetaljersiden brukes til å hente all informasjon.

## <a name="add-a-buy-box-module-to-a-page"></a>Legge til en kjøpsboksmodul på en side

Hvis du vil legge til en kjøpsboksmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt fragment** velger du **Kjøpsboks**-modulen.
1. Under **Navn på fragment** angir du navnet **Kjøpsboksfragmentet**, og deretter velger du **OK**.
1. I **Mediegalleri**-sporet i kjøpsboksmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Mediegalleri**-modulen, og deretter velger du **OK**.
1. I **Butikkvelger**-sporet i kjøpsboksmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.
1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **PDP-mal**, og velger deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg fragment** velger du **Kjøpsboksfragmentet** du opprettet tidligere, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I **Velg en mal**-dialogboksen velger du **PDP-mal**. Under **Sidenavn** angir du **PDP-side**, og velger deretter **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg fragment** velger du **Kjøpsboksfragmentet** du opprettet tidligere, og deretter velger du **OK**.
1. Lagre og forhåndsvis siden. Legg til spørringsstrengparameteren **?productid=&lt;product id&gt;** i URL-adressen for forhåndsvisningssiden. På den måten brukes produktkonteksten til å laste inn og gjengi forhåndsvisningssiden.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den. En kjøpsboks skal vises på siden for produktdetaljer.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Butikkvelgermodul](store-selector.md)

[Mediegallerimodul](media-gallery-module.md)

[Beholdermodul](add-container-module.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)

[Modul for sosial deling](social-share-module.md)

[Innstillinger for Legg til produkt i handlevogn](add-cart-settings.md)

[Beregn lagertilgjengelighet for detaljhandelskanaler](calculated-inventory-retail-channels.md)

[Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
