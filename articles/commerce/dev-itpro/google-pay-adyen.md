---
title: Konfigurer Google Pay med Adyen
description: Denne artikkelen beskriver hvordan du konfigurerer Google Pay med Adyen i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cdf950fc7b3720543d93e108d4e3c3c2ab254e09
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838398"
---
# <a name="configure-google-pay-with-adyen"></a>Konfigurer Google Pay med Adyen

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Google Pay med Adyen i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce tilbyr en bruksklar for integrering for Google Pay når Adyen-tjenesten for betalingsgateway brukes. Google Pay er en digital betalingsmetode for som bruker en Google Pay Merchant-konto i koordinering med Adyen-betalingstjenesten. Når dette er konfigurert, er Google Pay-knappen tilgjengelig som en valgbar betalingsmetode under betaling av bestillinger på nettet. Når brukere velger **Google Pay** i en nettleser eller enhet som støttes, omdirigeres de til fullføring av betalingen direkte med Google Pay-tjenesten. De returnerer deretter til nettbutikken for å fullføre bestillingen.

Når Google Pay brukes med betalingsmodulen for ekspressbetaling i Commerce, er brukerens betalingskontoinformasjon automatisk fylt ut på forhånd i betalingsskjemaet for å hjelpe brukeren med å gå raskere gjennom betalingsprosessen. Commerce inkluderer en modul for ekspressbetaling som muliggjør ekspressbetaling. Modulen for ekspressbetaling kan brukes i et fragment som er inkludert på betalings- eller handlekurvsiden. Dynamics 365 Payment Connector for referansen til Google Pay-koblingen brukes i tillegg til Dynamics 365 Payment Connector for Adyen, slik at alternativer både for ekspressbetaling og vanlig betaling aktiveres når PayPal er konfigurert. Google Pay kan også konfigureres med Adyen-betalingsterminaler og Commerce-salgssteder (POS) for bruk i butikken.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Google Pay | Google Pay, også kjent som Google Pay-"knappen", er et betalingstilbud som støttes via Adyen-koblingen. Det muliggjør kundeopplevelsen og integreringen som støttes av Dynamics Google Pay Connector. |
| Lommebok | En betalingstype som ikke omfatter tradisjonelle betalingsegenskaper, for eksempel BIN-området (Bank Identification Number) og utløpsdatoen, som brukes til å skille mellom kreditt- og debetkorttyper. |
| Modul for ekspressbetaling | En Dynamics 365 Commerce-modul som støtter raskere betalingsfunksjonalitet med støttede betalingsmetoder. |

## <a name="prerequisites"></a>Forutsetninger

Bruk av Google Pay med Adyen i Commerce krever en Google Merchant-konto. Hvis du vil ha mer informasjon om hvordan du konfigurerer Google Merchant-kontoen, kan du se [Adyen-dokumentasjonen på Google Pay](https://docs.adyen.com/payment-methods/google-pay/) og Googles [Integreringssjekkliste](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist).

Google Pay-betalingsmetoden må også integreres med Adyen-kontoen. For instruksjoner om integreringskoblingen, se [Adyen Google Pay](https://www.adyen.com/payment-methods/google-pay).

Du må også aktivere den utvidede lommebokfunksjonen i Dynamics 365 Commerce Headquarters. Gå til **Arbeidsområder \> Funksjonsbehandling**, søk etter funksjonen **Forbedret støtte for lommebok og betalingsforbedringer**, velg funksjonen, og velg deretter **Aktiver**. Når funksjonen er aktivert, kjører du **1110**-distribusjonsplanen for å gjøre endringen tilgjengelig i alle kanaler.

## <a name="map-the-google-pay-payment-method"></a>Tilordne Google Pay-betalingsmåten

Google Pay er en betalingsmetode med digital lommebok. Hvis du vil ha mer informasjon om hvordan du definerer betalingstilordning for Google Pay, kan du se [Støtte for lommebokbetaling](../wallets.md).

Følg denne fremgangsmåten for å tilordne Google Pay-betalingsmetoden til kortbetalingsmidler både for salgssteder og nettkanaler.

1. I Commerce Headquarters, går du til **Retail og Commerce \> Kanaloppsett \> Betalingsmetoder \> Korttyper**.
1. Velg **Ny** for å legge til en linje for Google Pay.
1. I **ID**-feltet angir du **GooglePay**.
1. I feltet **Navn på elektronisk betaling** angir du **Google Pay**.
1. I **Type**-feltet angir du **Lommebok**.
1. I **Utsteder**-feltet angir du **Google**.
1. Velg **Tilordningsmåter for prosessorbetaling** i handlingsruten for å åpne dialogboksen **Tilordningsmåter for prosessorbetaling**.
1. Under **Ikke-tilordnede betalingsmåter for prosessor** vises en liste over ikke-tilordnede betalingsmetoder for behandlere, der hver av dem er paret med den riktige koblingen. For å tilordne ikke-tilordnede Google Pay-betalingsmetoder for behandlere til kortbetalingsmidler, følger du disse trinnene for hvert kortbetalingsmiddel:

    1. Velg et kortbetalingsmiddel under **Kortbetalingsmidler**.
    1. I kolonnen **Ikke-tilordnede betalingsmåter for prosessor** velger du både **Dynamics 365 Payment Connector for Adyen**-koblingen (for bruk på salgsstedet) og **Dynamics 365 Payment Connector for Google Pay**-koblingen (for bruk i nettkanaler).
    1. Velg **Legg til**. Valgene legges til i kolonnen **Tilordnede betalingsmåter for prosessor**.

1. Når du er ferdig, med å tilordne betalingsmetoder, velger du **Lagre**.
1. På **Korttyper**-siden velger du **Lagre**.

## <a name="configure-a-commerce-online-store-for-google-pay"></a>Konfigurer en Commerce-nettbutikk for Google Pay

Følg denne fremgangsmåten for å konfigurere en Commerce-nettbutikk til å bruke Google Pay.

1. I Commerce headquarters går du til **Retail og Commerce \> Kanaler \> Nettbutikker**.
1. Velg nettstedets nettbutikkanal ved å velge kanalens verdi for **ID for detaljhandelskanal**.
1. På hurtigfanen **Betalingskontoer**, under **Kobling**, bekrefter du at koblingen **Dynamics 365 Payment Connector for Adyen** er oppført. Hvis den ikke er oppført, følger du instruksjonene i [Konfigurer Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md) for å legge den til.

    > [!NOTE]
    > I de fleste tilfeller må koblingen **Dynamics 365 Payment Connector for Adyen** være oppført som den første koblingen for kanalen din (den første koblingen kalles også hovedkoblingen). Deretter må den følges av andre koblinger som skal brukes, for eksempel koblingene **Dynamics 365 Payment Connector for PayPal** og **Dynamics 365 Payment Connector for GooglePay**.

1. Når koblingen **Dynamics 365 Payment Connector for Adyen** er lagt til, velger du **Legg til** for å legge til kolingen **Dynamics 365 Payment Connector forPayPay**. Angi deretter følgende egenskaper for koblingen:

    | Felt                  | Beskrivelse | Obligatorisk | Angitt automatisk | Eksempelverdi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Samlingsnavn          | Navnet på samlingen for Dynamics 365 Payment Connector for Google Pay. | Ja | Ja | *Binært navn* |
    | Tjenestekonto-ID     | Den unike ID-en for oppsettet av forhandleregenskapene. Denne ID-en stemples på betalingstransaksjoner, og identifiserer forhandleregenskapene som prosessene nedstrøms (for eksempel fakturering) skal bruke. | Ja | Ja | *GUID* |
    | Google-forhandler-ID     | Angi Google-forhandler-ID-en som er tilordnet Google-forhandlerkontoen. Denne egenskapen er obligatorisk for produksjonsmiljøer, men er valgfri for testmiljøer. Hvis du vil ha mer informasjon, kan du se <https://pay.google.com/>. | Ja | Nei | *Numerisk ID* |
    | Forhandlerkonto-ID    | Angi den unike Adyen-forhandler-ID-en. Denne verdien oppgis når du registrerer deg med Adyen, som beskrevet i [Registrering med Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nei | *Forhandler-ID* |
    | Sky-API-nøkkel          | Angi API-nøkkelen for Adyen-skyen. Hvis du vil hente denne nøkkelen, følger du instruksjonene i [Slik henter du API-nøkkelen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ja | Nei | "abcdefg" |
    | Gateway-miljø    | Adyen-gatewaymiljøet du skal tilordne til. De mulige verdiene er **Test** og **Live**. Du bør sette dette feltet til **Live** kun for produksjonsenheter og transaksjoner. | Ja | Ja | "Live" |
    | Valutaer som støttes   | Valutaene som koblingen skal behandle. I scenarioer med kort kan Adyen støtte flere valutaer gjennom [dynamisk valutakonvertering](https://www.adyen.com/pos-payments/dynamic-currency-conversion) etter at transaksjonsforespørselen er sendt til betalingsterminalen. Kontakt Adyen-støtte for å få en liste over valutaer som støttes. | Ja | Ja | "USD;EUR" |
    | Betalingsmidler som støttes | Betalingsmiddeltypene som koblingen skal behandle. | Ja | Ja | "GooglePay" |

1. Når du er ferdig med å angi koblingsegenskapene, kjører du distribusjonsplanjobben **1070 (Kanalkonfigurasjon**).


### <a name="use-the-payment-express-module-with-google-pay"></a>Bruk betalingsekspressmodulen med Google Pay

Betalingsekspressmodulen i Commerce fungerer med støttende betalingsmetoder, slik at kunder på nettstedet kan betale raskere ved å bruke kontoinformasjonen for betalingstjenesten i løpet av betalingsprosessen. Betalingsekspressmodulen referer til knappen for den konfigurerte betalingskoblingen og returnerer med bestillingsdetaljene som brukeren velger (adresse, kontaktinformasjon og betalingsmetode), for å fylle ut betalingsskjemaet.

Når betalingsekspressmodulen brukes med Google Pay, og en kunde velger Google Pay-knappen i delen **Betalingsekspress**, åpnes iFrame-vinduet for Google Pay. Brukere kan logge seg på Google-kontoen for å bruke kontoens leveringsadresse, faktureringsadresse, e-postadresse og den valgte Google Pay-betalingsmetoden for å betale for transaksjonen.

Når brukeren fullfører handlingen i Google Pal-vinduet, sendes brukeren tilbake til betalingssiden på Commerce-nettstedet, der betalingsskjemaet er forhåndsutfylt med detaljene om Google Pay-kontoen. Når brukern kommer tilbake til kassen fra Google Pay-vinduet, får de se følgende detaljer:

- I betalingsekspressflyten blir det første leveringsalternativet som er tilgjengelig for leveringsadressen som ble returnert, valgt på forhånd for kunden.
- Når Google Pay brukes, returneres ingen e-postadresse for kontakten. Gjestebrukere må angi en e-postadresse i kontaktdelen på betalingssiden. Påloggede brukere vil ha kontaktdataene automatisk fylt ut fra Dynamics-kundekontoen (den primære e-postadressen de brukte til godkjenning).

Kundene kan se gjennom bestillinger og endre betalingsdetaljer før vedkommende velger **Bestill** for å fullføre bestillingen.

### <a name="configure-google-pay-in-site-builder"></a>Konfigurer Google Pay i områdebyggeren 

Før du konfigurerer fragmentene eller sidene dine med Google Pay, må du sørge for at retningslinjene for innholdssikkerhet for området er angitt i Commerce-områdebyggeren.

Følg denne fremgangsmåten for å sikre at policyene for innholdssikkerhet er angitt i områdebyggeren.

1. Gå til **Områdeinnstillinger \> Tillegg** på området.
1. På fanen **Innholdssikkerhetspolicy** legger du til en linje for `*.google.com` i direktivene **child-src**, **connect-src**, **frame-ancestors**, **frame-src**, **img-src**, **script-src** og **style-src**.
1. Når du er ferdig, velg du **Lagre og publiser**.

### <a name="configure-the-payment-express-fragment-with-google-pay-in-site-builder"></a>Konfigurer betalingsekspressfragmentet med Google Pay i områdebyggeren

Følg denne fremgangsmåten for å definere betalingsekspressfragmentet med Google Pay for nettbutikken.

1. Gå til **Fragmenter** i områdebyggeren.
1. Velg **Ny**.
1. I dialogboksen **Nytt fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet (for eksempel **Ekspressbetaling**) og velger **OK**. 
1. Velg sporet **Standard beholder** for det nye fragmentet.
1. Angi egenskapene for beholdermodulen i egenskapsruten til høyre:

    - **Overskrift** – Angi en overskrift som skal vises for ekspressbetalingsdelen på området (for eksempel **Ekspressbetaling**).
    - **Beholderoppsett** – Velg **Flyt**.
    - **Bredde** – Velg **Fyll beholder**.
    - **Underordnede som vises** – Velg **Tre** tre for å angi antall underordnede enheter som det skal være plass til i en rad i ekspressbetalingsdelen på betalingssiden (for eksempel en tekstboks, betalingsekspress for PayPal og betalingsekspress for Google Pay).
    - **CSS-klassenavn** – Angi **msc-express-payment-container** (obligatorisk).

    > [!IMPORTANT]
    > - Verdien for **CSS-klassenavn** må være angitt til **msc-express-payment-container** for å styre virkemåten til beholderen under betaling. Denne virkemåten omfatter skjuling og andre handlinger som gjelder for ekspressbetalingsdelen under betalingsflyten. Klassen **msc-express-payment-container** fungerer med standardoperasjonene som frigis med betalingsmodulen fra modulbiblioteket.
    > - Flere stiler kan inkluderes mot **CSS-klassenavn**. Hvis du tilpasser virkemåten til modulen, må du krysskontrollere stilkontrollene hvis du bruker samme kodet virkemåte for modulbibliotek i betalingsmodulen for ekspressbetalingsvirkemåten.

1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Betalingsekspress**-modulen, og deretter velger du **OK**.
1. I egenskapsruten i **Betalingsekspress**-modulen angir du eller justerer verdien **Høyden på iFrame** i piksler (for eksempel **60**).
1. Angi **GooglePay** i feltet **Støttede betalingsmiddeltyper**. Verdien må samsvare med strengen **Betalingsmidler som støttes** som er konfigurert for kanalen (som beskrevet i delen [Konfigurer en Commerce-nettbutikk for Google Pay](#configure-a-commerce-online-store-for-google-pay) tidligere i denne artikkelen).

    > [!NOTE]
    > Du kan gjenta trinn 6 til 9 for å legge til **Betalingsekspress**-moduler for andre betalingsmetoder. Juster verdien for **Betalingsmidler som støttes**, med de ekstra konfigurerte betalingstypene (for eksempel **Paypal**).

1. Valgfritt: Du kan legge til en tekstblokkmodul i den standard beholdermodulen for å inkludere instruksjoner eller kunngjøre informasjon. Når du har lagt til modulen, angir du den ønskede teksten i **Rik tekst**-feltet i egenskapsruten. Du kan plassere teksten over eller under betalingsekspressmodulene ved å velge ellipsen (**...**) i **Tekstblokk**-sporet og deretter velge **Flytt opp** eller **Flytt ned**.
1. Velg **Lagre** for å lagre endringene, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere fragmentet.

### <a name="add-the-payment-express-fragment-to-the-checkout-page"></a>Legge til betalingsekspressfragmentet på betalingssiden

Følg denne fremgangsmåten for å legge til betalingsekspressfragmentet på betalingssiden.

1. Velg **Sider** i områdebyggeren, og velg deretter betalingssiden på nettstedet ditt.
1. Velg **Rediger**.
1. I **Hoved**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. Angi egenskapene for beholdermodulen i egenskapsruten til høyre:

    - **Beholderoppsett** – Velg **Stablet**.
    - **Bredde** – Velg **Fyll beholder**.
    - **Underordnede som vises** – Velg **Tre** tre for å angi antall underordnede enheter som det skal være plass til i en rad i ekspressbetalingsdelen på betalingssiden (for eksempel en tekstboks, betalingsekspress for PayPal og betalingsekspress for Google Pay).

1. I **Beholder**-sporet i modulen velger du ellipsen (**…**), og deretter velger du **Legg til fragment**.
1. I dialogboksen **Velg et fragment** velger du ekspressbetalingsfragmentet du opprettet, og deretter velger du **OK**.
1. Velg **Lagre** for å lagre endringene, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere siden.

> [!NOTE]
> Hvis betalingssiden allerede inneholder en beholder som har betalingsfragmentet, og du vil at betalingsekspressmodulen skal gjengis over den vanlige betalingsbeholderen, kan du plassere den over eller under den eksisterende betalingen ved å velge ellipsen (**...**) i **Hovedspor** og deretter velge **Flytt opp** eller **Flytt ned**.

### <a name="add-the-payment-express-fragment-to-the-cart-page"></a>Legge til betalingsekspressfragmentet på handlekurvsiden

Følg denne fremgangsmåten for å legge til betalingsekspressfragmentet på handlekurvsiden.

1. Velg **Sider** i områdebyggeren, og velg deretter handlekurvsiden på nettstedet ditt.
2. Velg **Rediger**.
3. I disposisjonsvisningen utvider du **Hovedspor** i trevisningen og finner beholderen som inneholder **Handlekurv**-modulen.
4. I **Handlekurv**-modulen velger du **Betalingsekpress**-sporet. Velg ellipsen (**...**), og velg deretter **Legg til modul**.
5. I dialogboksen **Velg moduler** velger du **Betalingsekspress**-modulen, og deretter velger du **OK**.
6. Velg **Betalingsekspress**-modulsporet. Under **Betalingsmidler som støttes** i egenskapsruten til høyre angir du deretter **GooglePay**. Verdien må samsvare med strengen **Betalingsmidler som støttes** som ble konfigurert for kanalen (som beskrevet i delen [Konfigurer en Commerce-nettbutikk for Google Pay](#configure-a-commerce-online-store-for-google-pay) tidligere i denne artikkelen).
1. Velg **Lagre** for å lagre endringene, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere siden.

Brukere kan inkludere opptil tre støttede **Betalingsekspress**-moduler som støttes (med andre ord tre tilgjengelige støttede betalingsalternativer) i **Betalingsekspress**-sporet i handlekurven.

### <a name="set-up-google-pay-as-an-option-in-the-checkout-payment-section"></a>Konfigurer Google Pay som et alternativ i betalingsdelen

Du kan definere Google Pay som et alternativ i betalingsdelen kun for betaling, ikke for ekspressfunksjonalitet. Betalingsskjemaet fylles ut av brukeren, og Google Pay-betalingssiden klargjør kun varene for betaling via Google Pay. Ingen Google-kontoinformasjon blir brukt til å overskrive de utfylte betalingsdetaljene.

> [!NOTE]
> Følgende fremgangsmåte forutsetter at området bruker et betalingsfragment som er konfigurert med plukkinformasjon, en leveringsadresse, leveringsalternativer, kontaktinformasjon, valgfrie vilkår og betingelser og en del for betalingselementer. Standard betalingsmodul fra modulbiblioteket frigis med en beholder en betalingsdelen, som har tekstblokk, fordelspoeng, gavekort og betalingsmoduler. Hvis du vil ha mer informasjon, se [Betalingsmodul](../payment-module.md).

Følg denne fremgangsmåten for å konfigurere Google Pay som et vanlig betalingsalternativ i delen **Betalingsmetode** på betalingssiden.

1. Velg **Fragmenter** i områdebyggeren, og velg deretter betalingsfragmentet på nettstedet ditt.
1. Velg **Rediger**.
1. I **Kasseinformasjon**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Betaling**-modulen, og deretter velger du **OK**.
1. Angi egenskapene for beholdermodulen i egenskapsruten til høyre i **Betaling**-modulen:

    - **Overskrift** – Angi en overskrift som skal vises for ekspressbetalingsdelen på området (for eksempel **Google Pay**).
    - **Høyden på iFrame** – Endre verdien til den foretrukne utformingshøyden i piksler (for eksempel **75**). 
    - **Betalingsmidler som støttes** – Angi **Google Pay** for å samsvare med konfigurasjonen for Google Pay-koblingen i Commerce headquarters.
    - **Er primærbetaling** – La avmerkingsboksen stå tom. (Denne egenskapen er vanligvis aktivert for Adyen-betalingsmodulen.)
    - **Overstyring av betalingsstil** – Denne egenskapen støttes ikke for Google Pay-konfigurasjonen.
    - **Bruk koblings-ID** – Denne egenskapen må velges hvis flere betalingskoblinger brukes på siden.

1. Plasser modulen over eller under endre betalingsmoduler ved å velge ellipsen (**...**) i **Betaling**-sporet og deretter velge **Flytt opp** eller **Flytt ned**.
1. Velg **Lagre** for å lagre endringene, og velg deretter **Fullfør redigering**.
1. Velg **Publiser**.

### <a name="modes-of-delivery"></a>Leveringsmåter

Med betalingsekspressmodulen som bruker Google Pay, blir det første leveringsalternativet som returneres mot den valgte leveringsadressen fra Google Pay-kontoen, valgt på forhånd. Brukere kan justere leveringsadressen til et annet alternativ hvis de ønsker det.

Visningsrekkefølgen for leveringsmåtene i betalingsekspressmodulen konfigureres på kanalens **Leveringsmåter**-side i Commerce headquarters. I Commerce headquarters går du til **Retail og Commerce \> Kanaler \> Nettbutikker** og velger verdien **ID for detaljhandelskanal** for butikken din. Velg **Leveringsmåter** i fanen **Oppsett** i handlingsruten. Leveringsmåtene som vises på listen, vises i samme rekkefølge i betalingsekspressmodulen. Hvis du vil legge til eller fjerne leveringsmåter for en detaljhandelskanal eller et produkt, velger du **Behandle leveringsmåter** i handlingsruten. Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsmoduser, kan du se [Definer leveringsmåter](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Betalingsmodulen bruker også modulen for leveringsalternativer når leveringsmåter gjengis under betalingen. Hvis du vil ha mer informasjon, kan du se [Modul for leveringsalternativer](../delivery-options-module.md).

Leveringsmåter vises etter hvert som de legges til i listen **Leveringsmåter** i nettbutikken.

## <a name="configure-commerce-pos-for-google-pay"></a>Konfigurer salgssted i Commerce for Google Pay

Salgsstedskonfigurasjonen bruker innstillingen for feltet **EFT-tjeneste** i maskinvareprofilen for Dynamics 365 Payment Connector for Adyen. Hvis du vil ha informasjon om hvordan du konfigurerer tjenesten for elektronisk pengeoverføring (EFT) for Dynamics 365 Payment Connector for Adyen i Commerce headquarters, kan du se [Konfigurer en maskinvareprofil for salgssted i Dynamics 365](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Prosessortilordningen for Adyen-koblingen registrerer lommebokkorttypene som Google Pay bruker på salgsstedsterminalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](payments-retail.md)

[Kassemodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
