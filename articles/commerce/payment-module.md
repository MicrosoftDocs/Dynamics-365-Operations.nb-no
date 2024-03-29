---
title: Betalingsmodul
description: Denne artikkelen dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: fa1482cb73a40df5f9bc9d3037196def71accf18
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279482"
---
# <a name="payment-module"></a>Betalingsmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Betalingsmodulen lar kunder betale for ordrer ved å bruke et kredittkort eller et debetkort. Betalingsintegrasjon for denne modulen leveres av Dynamics 365-betalingskoblingen for Adyen. Hvis du vil ha mer informasjon om hvordan du setter opp og konfigurerer betalingskoblingen, kan du se [Adyen-betalingskobling i Dynamics 365](dev-itpro/adyen-connector.md).  

Per Commerce-utgivelsen 10.0.14 er betalingsmodulen også integrert med Dynamics 365 Payment Connector for PayPal slik at kunder kan betale for bestillinger ved å bruke PayPal. Hvis du vil ha mer informasjon om hvordan du setter opp og konfigurerer Dynamics 365 Payment Connector for PayPal, kan du se [Dynamics 365 Payment Connector for PayPal](paypal.md). 

## <a name="dynamics-365-payment-connector-for-adyen"></a>Dynamics 365 Payment Connector for Adyen 

Betalingsmodulen er vert for betalingsinformasjonen som leveres via Adyen i en HTML-innebygd ramme (iframe). Betalingsmodulen fungerer sammen med Commerce Scale Unit for å hente Adyen-betalingsinformasjonen. Som en del av samhandlingen med Commerce Scale Unit kan betalingsmodulen tillate at informasjon om faktureringsadresse blir behandlet enten i iFrame via Adyen eller som en separat modul. I Fabrikam-temaet er faktureringsadressen aktivert som en egen modul. Denne fremgangsmåten gjør at du får mer fleksibilitet i formateringen, fordi adresselinjene kan gjengis slik at de ligner på linjene i leveringsadressen.

Betalingsmodulen lar også de påloggede kundene lagre betalingsinformasjonen. Betalingsinformasjonen og faktureringsadressen lagres og administreres via Adyen-betalingskoblingen.

Betalingsmodulen dekker eventuelle ordretillegg som ikke allerede dekkes av fordelspoeng eller et gavekort. Hvis totalen for en ordre er dekket av fordelspoeng eller gavekortkreditt, vil betalingsmodulen være skjult, og kunden kan plassere ordren uten den.

Adyen-betalingskoblingen støtter også sterk kundegodkjenning (SCA). En del av PSD2-direktiv (Revised Payment Services Directive) i EU krever at netthandlere godkjennes utenfor den elektroniske handleopplevelsen når de bruker en elektronisk betalingsmetode. Under utsjekkingsflyten blir kunder omadressert til banknettstedet, og deretter etter godkjenning, blir de omadressert tilbake til utsjekkingsflyten for Commerce. Under denne omadresseringen vil informasjonen som en kunde har angitt i betalingsflyten (for eksempel leveringsadresse, leveringsalternativer, informasjon om gavekort og fordelsinformasjon), beholdes. Før du kan aktivere funksjonen for Adyen-betalingskobling, må betalingskoblingen være konfigurert for SCA i Commerce Headquarters. Hvis du vil ha mer informasjon, kan du se [Sterk kundegodkjenning ved hjelp av Adyen](adyen_redirect.md). Denne funksjonen ble aktivert i Commerce-utgivelsen 10.0.12.

> [!NOTE]
> For Adyen-betalingskoblingen kan iframe-modulen i betalingsmodulen bare vises hvis du legger til Adyen-URL-adressen i områdets tillatelsesliste. Hvis du vil fullføre dette trinnet, legger du til **\*.adyen.com** i direktivene **child-src**, **connect-src**, **img-src**, **script-src** og **style-src** for områdes sikkerhetspolicy for innhold. Hvis du vil ha mer informasjon, se [Behandle policy for innholdssikkerhet](manage-csp.md). 

Følgende illustrasjon viser et eksempel på en gavekort-, fordels- og Adyen-betalingsmodul på en kasseside.

![Eksempel på en gavekort-, fordelspoeng- og Adyen-betalingsmodul på en kasseside.](./media/ecommerce-payments.PNG)

## <a name="dynamics-365-payment-connector-for-paypal"></a>Dynamics 365 Payment Connector for PayPal

Per Commerce-utgivelsen 10.0.14 er betalings modulen også integrert med Dynamics 365 Payment Connector for PayPal. Hvis du vil ha mer informasjon om hvordan du setter opp og konfigurerer denne betalingskoblingen, kan du se [Dynamics 365 Payment Connector for PayPal](paypal.md).
 
På utsjekkingssiden kan du ha både Adyen- og PayPal-koblingene konfigurert. Betalingsmodulen er forbedret med tilleggsegenskaper for å hjelpe med å finne ut hvilken kobling den skal fungere med. Hvis du vil ha mer informasjon, kan du se modulegenskapene for **Støttede betalingsmiddeltyper** og **Er primærbetaling** i tabellen nedenfor.
  
Når betalingsmodulen er konfigurert til å bruke PayPal-betalingskoblingen, vises en PayPal-knapp på betalingssiden. Når betalingsmodulen aktiveres av kunden, vil den gjengi en iframe som inneholder PayPal-informasjon. Kunden kan logge seg på og oppgi PayPal-informasjonen innenfor denne iframe for å fullføre transaksjonen. Når en kunde velger å betale med PayPal, blir den gjenværende saldoen på ordren belastet via PayPal.

PayPal-betalingskoblingen krever ikke en faktureringsadressemodul fordi alle faktureringsrelaterte opplysninger håndteres av PayPal i dens iframe. Du trenger imidlertid modulene leveringsadresse og leveringsalternativer.

Følgende illustrasjon viser et eksempel på to betalingsmoduler på en utsjekkingsside, en som er konfigurert med Adyen-betalingskoblingen og den andre med PayPal-betalingskoblingen.
![Eksempel på Adyen- og PayPay-betalingsmoduler på en kasseside.](./media/ecommerce-paypal.png)

Følgende illustrasjon viser et eksempel på PayPal iframe som aktiveres ved hjelp av PayPal-knappen. 
![Eksempel på Paypal iframe på en utsjekkingsside.](./media/ecommerce-paypal-iframe.png)

## <a name="payment-module-properties"></a>Egenskaper for betalingsmodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst | En valgfri overskrift for betalingsmodulen. |
| Høyden på iFrame | Piksler | IFrame-høyden, i piksler. Høyden kan imidlertid justeres etter behov. |
| Vis faktureringsadresse | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vil faktureringsadressen bli betjent av Adyen inne i betalingsmodulen iFrame. Hvis den er satt til **Usann**, blir faktureringsadressen ikke betjent av Adyen, og en Commerce-bruker må konfigurere en modul til å vise faktureringsadressen på betalingssiden. I PayPal-betalingskoblingen har ikke dette feltet innvirkning, fordi faktureringsadressen er bare håndteres i PayPal. |
| Overstyring av betalingsstil | CSS-kode (gjennomgripende stilark) | Fordi betalingsmodulen ligger i en iFrame, er det begrenset stilfunksjonalitet. Du kan oppnå en viss stil ved hjelp av denne egenskapen. Hvis du vil overstyre områdestiler, må du lime inn CSS-koden som verdien for denne egenskapen. Områdebygger for CSS overstyrer dette, og stiler gjelder ikke for denne modulen. |
|Støttede betalingsmiddeltyper| Streng| Hvis det er konfigurert flere betalingskoblinger, bør du oppgi betalingsmiddelstrengen som støttes, slik den er definert i konfigurasjonen av betalingskoblingen til Commerce Headquarters (se bildet nedenfor). Hvis den er tom, brukes Adyen-betalingskoblingen som standard. Lagt til i Commerce-versjon 10.0.14.|
|Er primærbetaling|  **Sann** eller **Usann** | Hvis den er **sann**, vil eventuelle feilmeldinger bli generert fra primærbetalingskoblingen på betalingssiden. Hvis både Adyen- og PayPal-betalingskoblingene er konfigurert, setter du Adyen til **sann**, som ble lagt til i Commerce-utgivelsen 10.0.14.|
|Bruk koblings-ID| **Sann** eller **Usann** | Bruk denne egenskapen hvis flere betalingskoblinger er konfigurert for området. Hvis **Sann**, må koblinger bruke koblings-ID-en for betalingskorrelasjon.|
|Bruk nettleserens angitte språkkode for iFrame|  **Sann** eller **Usann** | (Bare Adyen) Hvis **Sann**, gjengir Adyen iFrame-språket basert på områdebrukerens nettleserkontekst, i stedet for å bruke språkkoden for Commerce-kanalen som er konfigurert for området. Lagt til i Commerce-versjon 10.0.27.|

Følgende illustrasjon viser et eksempel på **Støttede betalingsmiddeltyper**-verdien som er satt til PayPal i betalingskoblingskonfigurasjonen i Commerce Headquarters.
![Eksempel på støttede betalingsmiddeltyper i Commerce Headquarters.](./media/ecommerce-paymenttendertypes.png)

## <a name="billing-address"></a>Faktureringsadresse

En faktureringsadressemodul kan brukes på utsjekkingssiden hvis faktureringsadresselinjene for Adyen-betalingskoblingen samsvarer tilstrekkelig med utseendet på resten av området. 

Hvis du vil bruke en faktureringsadressemodul på utsjekkingssiden når betalingsmodulen er integrert med Adyen-betalingskoblingen, setter du egenskapen **Vis faktureringsadresse** til **Usann** slik at en egen faktureringsadressemodul kan brukes i stedet for standard Adyen-faktureringsadresse. I dette tilfellet bør områdeforfatteren ha en faktureringsadressemodul på betalingssiden. Adyen-betalingskoblingen gjør det også mulig å bruke leveringsadressen som faktureringsadresse for å redusere antall trinn for områdebrukeren.

På samme måte som betalingsmoduler er en egenskap for **Støttede betalingsmiddeltyper** lagt til i faktureringsadressemodulen i Commerce-utgivelse 10.0.14. Verdien til denne egenskapen bør være identisk med verdien som er angitt i betalingsmodulen, for å sikre at de arbeider sammen. For Adyen-betalingskoblingen må både betalingsmodulen og faktureringsadressemodulen la denne verdien være tom (standardtilstanden). Det er ikke nødvendig med en egen faktureringsadressemodul for PayPal-koblingen. For andre typer betalingskoblinger bør strengen angis som konfigurert i Commerce Headquarters.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Legge til en betalingsmodul på en kasseside og angi de nødvendige egenskapene

En betalingsmodul kan bare legges til i en kassemodul. Hvis du vil ha mer informasjon om hvordan du konfigurerer en betalingsmodul for en kasseside, se [Kassemodul](add-checkout-module.md).

## <a name="configure-the-adyen-and-paypal-payment-connectors-when-both-are-used"></a>Konfigurere betalingskontaktene Adyen og PayPal når begge brukes

Hvis betalingskontaktene Adyen og PayPal vil bli brukt for området, følger du denne fremgangsmåten i Commerce-områdebyggeren for å legge til betalingsmoduler for hver kobling i utsjekkingsmodulen, og deretter konfigurere egenskapene for hver modul.

1. Følg denne fremgangsmåten i egenskapsruten for PayPal-betalingsmodulen:

    1. I feltet for egenskapen **Støttede betalingsmiddeltyper**, angir du **PayPal**.
    1. Fjern merket i avmerkingsboksen for egenskapen **Er primærbetaling**.
    1. Merk av for egenskapen **Bruk koblings-ID**.

1. Følg denne fremgangsmåten i egenskapsruten for Adyen-betalingsmodulen:

    1. La feltet for egenskapen **Støttede betalingsmiddeltyper** stå tom.
    1. Merk av i avmerkingsboksen for egenskapen **Er primærbetaling**.
    1. Merk av for egenskapen **Bruk koblings-ID**.

> [!NOTE]
> Når du konfigurerer Adyen- og PayPal-koblingene som skal brukes sammen, må konfigurasjonen **Dynamics 365 Payment Connector for Adyen** være i første posisjon i den elektroniske kanalens koblingskonfigurasjon for **Betalingskontoer** i Commerce Headquarters. Hvis du vil bekrefte eller endre koblingsrekkefølgen, kan du gå til **Nettbutikker** og velge kanalen for området. I kategorien for **Oppsett** i hurtigkategorien **Betalingskontoer** under **Kobling** kontrollerer du at **Dynamics 365 Payment Connector for Adyen**-konfigurasjonen er i første posisjon (det vil si på den øverste linjen), og at **Dynamics 365 Payment Connector for PayPal**-konfigurasjonen står på den andre linjen. Legg til eller fjern koblinger etter behov for å bestille dem på nytt.

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)

[Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md)

[Dynamics 365 Payment Connector for PayPal](paypal.md)

[Sterk kundegodkjenning ved hjelp av Adyen](adyen_redirect.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
