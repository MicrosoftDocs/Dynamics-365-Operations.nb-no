---
title: Butikkvelgermodul
description: Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 341312758e0a6da2e918406e09df618e2475811f
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479382"
---
# <a name="store-selector-module"></a>Butikkvelgermodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker butikkvelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.

Kunder kan bruke butikkvelgermodulen til å hente frem et produkt i en valgt butikk etter et elektronisk innkjøp. I Commerce versjon 10.0.13 inneholder butikkvelgermodulen også flere funksjoner som kan vise en **Finn en butikk**-side som viser nærliggende butikker.

Med butikkvelgermodulen kan brukere angi en lokasjon (by, delstat, adresse og så videre) for å søke etter butikker innen en søkeradius. Når modulen åpnes for første gang, brukes kundens nettleserposisjon til å finne butikker (hvis samtykke er gitt).

## <a name="store-selector-module-usage"></a>Bruk av butikkvelgermodul

- En butikkvelgermodul kan brukes på en produktdetaljside (PDP) til å velge en butikk for plukking.
- En butikkvelgermodul kan brukes på en handlevognside til å velge en butikk for plukking.
- En butikkvelgermodul kan brukes på en frittstående side som viser alle tilgjengelige butikker.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Konfigurasjon av oppfyllelsesgrupper i Commerce Headquarters

For at butikkvelgeren skal vise tilgjengelige butikker, må oppfyllelsesgruppen være definert i Commerce Headquarters. Hvis du vil ha mer informasjon, kan du se [Definere oppfyllelsesgrupper](customer-orders-overview.md#set-up-fulfillment-groups).

I tillegg må breddegrad og lengdegrad for butikklokasjonen være definert i hovedkontoret for hver butikk i oppfyllelsesgruppen.

Hvis du vil angi bredde- og lengdegrad for en butikklokasjon i Commerce Headquarters, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Lageroppdeling**.
1. Velg lagerlokasjonen i den venstre ruten.
1. På hurtigfanen **Adresser** velger du **Avansert**.

    ![Eksempel på butikkdetaljer i hovedkontoret.](./media/Store-address.png)

1. I handlingsruten velger du **Rediger**.
1. På hurtigfanen **Generelt** angir du verdier for **Breddegrad** og **Lengdegrad**.

    ![Eksempel på oppsett av breddegrad og lengdegrad for en butikk i hovedkontoret.](./media/Store-latitude-longitude.png)

1. Velg **Lagre** i handlingsruten. 

## <a name="bing-maps-integration"></a>Bing Maps-integrering

Butikkvelgermodulen er integrert med [Bing Maps REST API-er (Application Programming Interface)](/bingmaps/rest-services/) for å bruke Bing-funksjonene for geokoding og autoforslag. En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for Commerce Headquarters. API-et for geokoding brukes til å konvertere en sted til breddegrads- og lengdegradsverdier. Integreringen med API-et for autoforslag brukes til å vise søkeforslag når brukere angir steder i søkefeltet.

Når det gjelder REST API-et for autoforslag, må du kontrollere at følgende URL-adresser er tillatt i henhold til områdets sikkerhetspolicy for innhold (CSP). Dette oppsettet gjøres i Commerce-områdebygger ved å legge til tillatte URL-adresser i CSP-direktiver for nettstedet (for eksempel **img-src**). Hvis du vil ha mer informasjon, se [Innholdssikkerhetspolicy](manage-csp.md). 

- For direktivet **connect-src** legger du til **&#42;.bing.com**.
- For direktivet **img-src** legger du til **&#42;.virtualearth.net**.
- For direktivet **script-src** **legger du til  &#42;.bing.com, &#42;.virtualearth.net**.
- For direktivet **script style-src** legger du til **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Hent i butikk-modus

Butikkvelgermodulen støtter en **Hent i butikk**-modus som viser en liste over butikker der et produkt er tilgjengelig for henting. Den viser også åpningstider og produktbeholdning for hver butikk i listen. Butikkvelgermodulen krever konteksten for et produkt for å gjengi produkttilgjengelighet og for å la brukeren legge til produktet i handlekurven hvis produktets leveringsmåte er satt til **henting** på den valgte butikken. For mer informasjon, se [Beholdningsinnstillinger](inventory-settings.md). 

Butikkvelgermodulen kan legges til en kjøpsboksmodul på en PDP for å vise butikkene der et produkt er tilgjengelig for henting. Den kan også legges til i en handlekurvmodul. I dette tilfellet viser butikkvelgermodulen hentealternativer for hvert vareelement i handlekurven. Butikkvelgermodulen kan også legges til på andre sider eller moduler via utvidelser og tilpassinger.

For at dette scenarioet skal fungere, bør produktene konfigureres slik at leveringsmodusen **henting** brukes. Ellers vil ikke modulen vises på de produktsidene. Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsmodus, kan du se [Definer leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Bildet nedenfor viser et eksempel på en butikkvelgermodul som brukes på en PDP.

![Eksempel på en butikkvelgermodul som brukes på PDP.](./media/BOPIS.PNG)

> [!NOTE]
> I versjon 10.0.16 og nyere kan en ny funksjon aktiveres, noe som gjør at en organisasjon kan definere flere plukkmoduser for leveringsmåter for kunder.  Hvis denne funksjonen er aktivert, vil butikkvelgeren og andre moduler med e-handel bli forbedret slik at kunden kan velge fra potensielt flere leveringsalternativer hvis de er konfigurert.  Hvis du vil vite mer om denne funksjonen, kan du se [denne dokumentasjonen](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Søk etter butikker-modus

Butikkvelgeren støtter også en **Søk etter butikker**-modus. Denne modusen kan brukes til å opprette en side for butikklokasjoner som viser tilgjengelige butikker og tilhørende informasjon. I denne modusen fungerer butikkvelgermodulen uten produktkontekst og kan brukes som en frittstående modul på en områdeside. Hvis de aktuelle innstillingene er aktivert for modulen, kan brukerne også velge en butikk som foretrukket butikk. Når en butikk velges som en brukers foretrukne butikk, opprettholdes butikk-ID-en i informasjonskapselen i leseren. Derfor må brukeren godta en melding om samtykke til informasjonskapsler.

Følgende illustrasjon viser et eksempel på en butikkvelgermodul som brukes sammen med en kartmodul på en side med butikkadresser.

![Eksempel på en butikkvelgermodul og en kartmodul på en side for butikklokasjoner.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Gjengi et kart

Butikkvelgermodulen kan brukes sammen med kartmodulen for å vise butikkadressene på et kart. Hvis du vil ha mer informasjon kartmodulen, kan du se [Kartmodul](map-module.md).

## <a name="store-selector-module-properties"></a>Egenskaper for butikkvelgermodul

| Egenskapsnavn | Verdi | beskrivelse |
|---------------|-------|-------------|
| Overskrift | Tekst | Overskriften for modulen. |
| Modus | **Søk etter butikker** eller **Hent i butikk** | **Søk etter butikker**-modus viser tilgjengelige butikker. **Hent i butikk**-modus lar brukerne velge en butikk for henting. |
| Stil | **Dialogboks** eller **Innebygd** | Modulen kan gjengis enten innebygd eller i en dialogboks. |
| Angi som foretrukket butikk | **Sann** eller **Usann** | Når denne egenskapen er angitt til **Sann**, kan brukerne angi en foretrukket butikk. Denne funksjonen krever at brukerne godtar en samtykkemelding for informasjonskapsler. |
| Vis alle butikker | **Sann** eller **Usann** | Når denne egenskapen er angitt til **Sann**, kan brukerne omgå egenskapen **Søkeradius** og vise alle butikker. |
| Alternativer for autoforslag: maksimalt antall resultater | Tall | Denne egenskapen definerer det maksimale antallet automatisk foreslåtte resultater som kan vises via API-et Bing Autosuggest. |
| Søkeradius | Tall | Denne egenskapen definerer søkeradius for butikkene, i miles. Hvis ingen verdi er angitt, brukes standard søkeradius på 50 engelske mil. |
| Vilkår for bruk | URL |  Denne egenskapen angir vilkårene for bruk av URL-adresser som kreves for å bruke Bing Maps-tjenesten. |

## <a name="site-settings"></a>Områdeinnstillinger

Butikkvelgermodulen overholder [innstillingene for Legg til produkt i handlekurv](add-cart-settings.md). Når en vare er lagt til i handlekurven fra butikkvelgermodulen, vil brukerne se de passende konfigurerte arbeidsflytene.

## <a name="add-a-store-selector-module-to-a-page"></a>Legge til en butikkvelgermodul på en side

For **Hent i butikk**-modus kan modulen bare brukes på PDP-er og handlevognsider. Du må angi modusen til **Hent i butikk** i modulens egenskapsrute.

- Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en kjøpsboksmodul, kan du se [Kjøpsboksmodul](add-buy-box.md). 
- Hvis du vil ha informasjon om hvordan du legger til en butikkvelgermodul i en handlekurvmodul, kan du se [Handlekurvmodul](add-cart-module.md)

Hvis du vil konfigurere butikkvelgermodulen til å vise tilgjengelige butikker for en butikklokasjonsside, som i illustrasjonen tidligere i dette emnet, følger du denne fremgangsmåten.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Markedsføringsmal**, og velger deretter **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I **Velg en mal**-dialogboksen velger du malen **Markedsføringsmal**. Under **Sidenavn** angir du **Butikklokasjoner** og velger deretter **OK**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulen **Beholder med 2 kolonner**, og deretter velger du **OK**.
1. I modulens egenskaperrute setter du **Bredde**-verdien til **Fyll container**.
1. Sett verdien **Konfigurasjon av ekstra liten visningsport** til **100 %**.
1. Sett verdien **Konfigurasjon av liten visningsport** til **100 %**.
1. Sett verdien **Konfigurasjon av medium visningsport** til **33 % til 67 %**.
1. Sett verdien **Konfigurasjon av stor visningsport** til **33 % til 67 %**.
1. I **Beholder med 2 kolonner**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Butikkvelger**-modulen, og deretter velger du **OK**.
1. I modulens egenskaperrute setter du **Modus**-verdien til **Finn butikker**.
1. Angi verdien for **Søkeradius** i miles.
1. Angi andre egenskaper, for eksempel **Angi som foretrukket butikk**, **Vis alle butikker** og **Aktiver automatiske forslag**, etter behov.
1. I **Beholder med 2 kolonner**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Kart**-modulen, og deretter velger du **OK**.
1. I modulens egenskapsrute angir du eventuelle tilleggsegenskaper du trenger.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.
 
## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Hurtiginnføring i PDP](quick-tour-pdp.md)

[Hurtiginnføring i handlekurv og kasse](quick-tour-cart-checkout.md)

[Definer leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Behandle Bing-kart for organisasjonen](dev-itpro/manage-bing-maps.md)

[Bing Maps REST API-er](/bingmaps/rest-services/)

[Kartmodul](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
