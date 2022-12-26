---
title: Konfigurere Apple Pay med Adyen i Dynamics 365 Commerce
description: Denne artikkelen beskriver hvordan du konfigurerer Apple Pay med Adyen i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 896847cee696e221b2114f7f28a0b56e73fc911b
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838236"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Konfigurere Apple Pay med Adyen i Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer Apple Pay med Adyen i Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Viktige termer

| Semester | Beskrivelse |
|---|---|
| Apple Pay | Apple Pay, også kjent som Apple Pay-"knappen", er et betalingstilbud som støttes via Adyen-koblingen. Det muliggjør kundeopplevelsen og integreringen som støttes av Microsoft Dynamics 365 Apple Pay-koblingen. |
| Lommebok | En betalingstype som ikke omfatter tradisjonelle betalingsegenskaper, for eksempel BIN-området (Bank Identification Number) og utløpsdatoen, som brukes til å skille mellom kreditt- og debetkorttyper. |

Dynamics 365 Commerce tilbyr en bruksklar for integrering for Apple Pay når Adyen-tjenesten for betalingsgateway brukes. Apple Pay er en digital betalingsmetode for som bruker en Apple Pay Merchant-konto i koordinering med Adyen-betalingstjenesten. Når dette er konfigurert, er Apple Pay-knappen en valgbar betalingsmetode som er en del av utsjekkingssiden til en nettbutikk. Knappen Apple Pay presenteres som et betalingsalternativ bare for støttede Apple Pay-enheter. Når brukere velger **Apple Pay** på en nettleser eller enhet som støttes, omdirigeres de til fullføring av betalingen direkte med Apple Pay-tjenesten. De returnerer deretter til nettbutikken for å fullføre bestillingen.

Dynamics 365 Payment Connector for Apple Pay connector-referansen brukes i tillegg til Dynamics 365 Payment Connector for Adyen, for å aktivere Apple Pay and kredittkortbetalinger på et nettsted. Apple Pay kan også konfigureres for bruk i butikker som har Adyen-betalingsterminaler som bruker Dynamics 365 Payment Connector for Adyen med Commerce-salgssted (POS). I dette tilfellet håndterer Dynamics 365 Payment Connector for Adyen Apple-betalingsenheten via terminalen.

## <a name="prerequisites"></a>Forutsetninger

En Apple-forhandlerkonto kreves for å bruke Apple Pay med Adyen i Commerce. Hvis du vil ha mer informasjon om hvordan du definerer Apple Pay i testkundeområdet, kan du se [Apple Pay Drop-integrering](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Hvis du vil ha mer informasjon om hva du kan gjøre når du er klar til å aktivere i produksjonsmiljøet, kan du se [Aktivere](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Apple Pay-betalingsmetoden må også integreres med Adyen-kontoen. Adyen kan hjelpe deg med å konfigurere betalingsmåten, og kan også hjelpe deg med å sikre at domenene du vil bruke sertifikatet til, tilordnes for bruk med sertifikatet.

For å aktivere det forbedrede lommebokfunksjonsflagget i Commerce headquarters, går du til **Arbeidsområder \> Funksjonsbehandling**, og søk etter funksjonen **Forbedret støtte for lommebok og betalingsforbedringer**. Velg funksjonen, og velg deretter **Aktiver**. Når funksjonen er aktivert, kjører du **1110**-distribusjonsplanen for å gjøre endringen tilgjengelig i alle kanaler.

## <a name="map-the-apple-pay-payment-method"></a>Tilordne Apple Pay-betalingsmåten

Apple Pay er en betalingsmetode med digital lommebok. Hvis du vil ha mer informasjon om hvordan du definerer betalingstilordning for Apple Pay, kan du se [Støtte for lommebokbetaling](../wallets.md).

For å tilordne Apple Pay-betalingsmåten i Commerce headquarters, følger du disse trinnene.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Betalingsmetoder \> Korttyper**.
1. Velg **Ny** for å legge til en linje for Apple Pay, og angi deretter følgende verdier:

    - **ID:** ApplePay
    - **Navn på elektronisk betaling:** Apple Pay
    - **Type:** Lommebok
    - **Utsteder:** Apple

1. Velg **Prosessortilordning** for å åpne dialogboksen **Tilordningsmåter for prosessorbetaling**. Kolonnen **Ikke-tilordnede betalingsmåter for prosessor** viser den støttede betalingsmåten for hver tilgjengelige kontakt (Adyen, PayPal og Apple).
1. Tilordne de støttede betalingsmetodene som du vil ha for både **Dynamics 365 Payment Connector for Adyen**-koblingen (for bruk på salgsstedet) og **Dynamics 365 Payment Connector for Apple Pay**-koblingen (for Internett-kanal).
1. For hver tilordningslinje velger du linjen du vil støtte, i kolonnen **Ikke-tilordnede betalingsmåter for prosessor**, og deretter velber du **Legg til** for å flytte valgene til kolonnen **Tilordnede betalingsmåter for prosessor**.
1. Velg **OK**, og velg deretter **Lagre** på siden **Korttyper**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Konfigurere Apple Pay-sertifikatet for området

For hvert område må du laste opp domenetilknytningsfilen (også kalt Apple Pay-sertifikatet) slik det er beskrevet i [Adyen Apple Pay-dokumentasjonen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Du kan bruke Commerce-områdebygger til å laste opp domenetilknytningsfilen til mediebiblioteket for området.

Følg denne fremgangsmåten for å sette opp Apple Pay-sertifikatet i områdebyggeren.

1. Last ned sertifikatet (domenetilknytningsfilen) fra [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Legg til txt-filtypen i domenetilknytningsfilen.
1. I områdebyggeren [laster du opp](../upload-serve-static-files.md) domenetilknytningsfilen til områdets mediebibliotek.
1. Gå til **URLer**.
1. Velg **Ny \> Ny URL-adresse**.
1. Velg **Mediebibliotekressurs** i dialogboksen **Ny URL-adresse**.
1. I feltet for **URL-bane** angir du URL-banen (hvis den ikke allerede er angitt). Etter at domenegrunnlags-URLen er angitt, angir du følgende påkrevde Apple-streng: `<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Velg **Neste**. Mediebiblioteket viser alle opplastede medieressurser av typen **dokument** (.txt).
1. Velg domenetilknytningsfilen som skal betjenes for forespørsler til URL-adressen du definerte tidligere.
1. Velg **Opprett**.

På dette tidspunktet er URL-adressen du opprettet, i utkasttilstand. Publisere URL-adressen for å fullføre prosessen. Filen som URL-adressen peker til, returneres ikke før du publiserer URL-adressen.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Konfigurer en Commerce-nettbutikk for Apple Pay

Følg denne fremgangsmåten for å konfigurere en Commerce-nettbutikk til å bruke Apple Pay.

1. I Commerce headquarters går du til **Retail og Commerce \> Kanaler \> Nettbutikker**.
1. Velg verdien **ID for detaljhandelskanal** for områdets nettbutikkanal.
1. I hurtigfanen **Betalingskontoer** legger du til **Dynamics 365 Payment Connector for Adyen**-koblingen hvis den ikke allerede er satt opp, ved å følge instruksjonene i [Konfigurer Dynamics 365 Payment Connector for Adyen](adyen-connector-setup.md).
1. Når Adyen-koblingen er konfigurert, velger du **Legg til** for å legge til **Dynamics 365 Payment Connector for Apple Pay**-koblingen.
1. Angi verdier for betalingskoblingsegenskaper.

    | Egenskap               | Beskrivelse | Obligatorisk | Angitt automatisk | Eksempelverdi |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Samlingsnavn          | Navnet på samlingen for Dynamics 365 Payment Connector for Apple Pay. | Ja | Ja | Binært navn |
    | Tjenestekonto-ID     | Den unike ID-en for oppsettet av forhandleregenskapene. Denne ID-en stemples på betalingstransaksjoner, og identifiserer forhandleregenskapene som prosessene nedstrøms (for eksempel fakturering) skal bruke. | Ja | Ja | Guid |
    | Forhandlerkonto-ID    | Angi den unike Adyen-forhandler-ID-en. Denne verdien oppgis når du registrerer deg med Adyen, som beskrevet i [Registrering med Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Ja | Nei | MerchantIdentifier |
    | Sky-API-nøkkel          | Angi API-nøkkelen for Adyen-skyen. Du kan hente denne nøkkelen ved å følge instruksjonene i [Slik henter du API-nøkkelen](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Ja | Nei | abcdefg |
    | Gateway-miljø    | Angi Adyen-gatewaymiljøet du skal tilordne til. De mulige verdiene er **Test** og **Live**. Du bør sette dette feltet til **Live** kun for produksjonsenheter og transaksjoner. | Ja | Ja | Live |
    | Valutaer som støttes   | Angi valutaene som koblingen skal behandle. I scenarioer med kort kan Adyen støtte flere valutaer gjennom [dynamisk valutakonvertering](https://www.adyen.com/pos-payments/dynamic-currency-conversion) etter at transaksjonsforespørselen er sendt til betalingsterminalen. Kontakt Adyen-støtte for å få en liste over valutaer som støttes. | Ja | Ja | USD;EUR |
    | Betalingsmidler som støttes | Angi betalingsmiddeltypene som koblingen skal behandle. | Ja | Ja | ApplePay |

1. Når forretningsenhetsinformasjonen er angitt, kjører du planleggingsjobben **1070** for kanalkonfigurasjonsdistribusjon.


### <a name="configure-content-security-policies-in-site-builder"></a>Konfigurere innholdssikkerhetspolicyer i områdekonfigurator

Før du konfigurerer fragmentene eller sidene for å bruke Apple Pay, må du sørge for at retningslinjene for innholdssikkerhet (CSPer) er konfigurert i Commerce-områdebyggeren for området ditt.

Følg denne fremgangsmåten for å konfigurere policyene for innholdssikkerhet er angitt i områdebyggeren.

1. Gå til **Områdeinnstillinger \> Tillegg**.
1. På fanen **Innholdssikkerhetspolicy** velger du **Legg til** for å legge til en linje som har `https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js` for delene **child-src**, **connect-src**, **frame-src**, **img-src**, **script-src** og **style-src**.
1. Når du er ferdig velger du **Lagre og publiser** for å lagre endringene.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Definere Apple Pay som et betalingsmiddelalternativ

Følg denne fremgangsmåten for å konfigurere Apple Pay som et betalingsmiddelalternativ på områdets utsjekkingsside (ikke-ekspress).

1. Velg **Fragmenter** i områdebyggeren, og velg betalingsfragmentet på nettstedet ditt.
1. Velg **Rediger**.
1. I **Beholder for betalingsdel**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg moduler** velger du **Apple Pay**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**.
1. Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.

Innstillinger for **Apple Pay**-modulen er bygd inn i modulen, og knytter den konfigurerte Dynamics 365 Payment Connector for Apple Pay connector som er konfigurert for den elektroniske kanalen i Commerce headquarters.

### <a name="apple-pay-payment-behavior"></a>Apple Pay-betalingsatferd

Betalingsknappen **Apple Pay** vises bare på støttede Apple Pay-enheter (iPhones, iPads og Safari-nettlesere som støtter Apple Pay). Hvis en bruker ikke trenger å bruke en av disse enhetene, er knappen **Apple Pay** skjult.

Når en bruker velger knappen **Apple Pay**, vises en dialogboks for **Apple Pay**. Der kan brukeren autentisere mot Apple Pay-enheten eller -webleseren. Dialogboksen **Apple Pay** viser et sammendrag av ordrebeløpet og betalingsmåten som brukeren har konfigurert mot Apple-lommeboken. Brukeren kan se gjennom disse opplysningene og deretter velge **Betal** å fullføre betalingen. Når betalingen er fullført, sendes brukeren til siden for **bestillingsfullføring** som viser et detaljert ordresammendrag for den fullførte transaksjonen.

## <a name="configure-commerce-pos-for-apple-pay"></a>Konfigurer salgssted i Commerce for Apple Pay

Salgsstedskonfigurasjonen bruker konfigurasjonen for feltet **EFT-tjeneste** i maskinvareprofilen for Dynamics 365 Payment Connector for Adyen. I Commerce headquarters konfigurerer du EFT-tjenesten for Dynamics 365 Payment Connector for Adyen som beskrevet i [Konfigurer en maskinvareprofil for salgssted i Dynamics 365](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Kontroller at du legger til **ApplePay** i listen over betalingsmidler i feltet **Betalingsmidler som støttes**. Bruk semikolon (;) for å skille betalingsmiddelet fra listen.

Prosessortilordningen for Adyen-koblingen registrerer lommebokkorttypene som brukes av Apple Pay på salgsstedsterminalen.

## <a name="additional-resources"></a>Tilleggsressurser

[Vanlige spørsmål om betalinger](payments-retail.md)

[Kassemodul](../add-checkout-module.md)

[Betalingsmodul](../payment-module.md)
