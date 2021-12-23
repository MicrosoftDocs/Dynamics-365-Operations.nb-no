---
title: Registrere et integreringspunkt i webportalen for ID-porten
description: Dette emnet beskriver hvordan du registrerer et integreringspunkt i ID-porten-webportalen i Norge.
author: liza-golub
ms.author: elgolu
ms.date: 11/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.search.validFrom: 2022-11-15
ms.openlocfilehash: 6bcdd5350683d2b582e625b57baab1ae852be2db
ms.sourcegitcommit: a11e8f4e764ff0bb210875401ae0671bc6412bde
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2021
ms.locfileid: "7866808"
---
# <a name="register-an-integration-point-in-the-id-porten-web-portal"></a>Registrere et integreringspunkt i webportalen for ID-porten

[!include [banner](../includes/banner.md)]

Firmaer som er registrert for merverdiavgift i Norge, har sine kontoer i webportalen [ID-porten](https://samarbeid.digdir.no/id-porten/ta-i-bruk-id-porten/94). Hvis du vil aktivere direkte innsending av mva-returer til Altinn, må du opprette et [integreringspunkt](https://docs.digdir.no/oidc_index.html) på firmaets konto i ID-porten. Hvis du vil ha mer informasjon, kan du se [ID-Porten og godkjenning](https://skatteetaten.github.io/mva-meldingen/english/idportenauthentication/).

Vi anbefaler at du definerer følgende parametere for integreringspunktet for direkte innsending av mva-returer til Altinn fra Microsoft Dynamics 365 Finance.

| Parameternavn (norsk) | Parameternavn (engelsk) | Beskrivelse av parameteren | Parameterverdi |
|---|---|---|---|
| Difi-tjeneste | Difi-tjeneste | Velg tjenesten som skal tilordnes riktige områder. | Velg **API-klient**. |
| Områder | Områder | APIer/ressurser som integreringen har tilgang til. | <p>Velg følgende områder:</p><ul><li>**openid**</li><li>**skatteetaten:mvameldinginnsending**</li><li>**skatteetaten:mvameldingvalidering**</li></ul> |
| Kundens org.nr. | Kundens organisasjonsnummer | Organisasjonsnummeret til tjenesteeieren. | Du behøver ikke å angi noen verdi i dette feltet. Den obligatoriske verdien angis automatisk når oppsettet av integreringspunktet lagres. |
| Integrasjonens identifikator | Integrasjonens identifikator | Den unike identifikatoren for tjenesten. Identifikatoren genereres automatisk. | Du behøver ikke å angi noen verdi i dette feltet. Den obligatoriske verdien angis automatisk når oppsettet av integreringspunktet lagres. |
| Navn på integrasjonen | Navn på integrasjonen | Navnet på integrasjonen slik det vises i påloggingsvinduet. | Angi **Microsoft Dynamics 365 Finance**. |
| Beskrivelse | Beskrivelse | En kort beskrivelse av tjenesten (for eksempel "Møteportal for NN-kommune"). | Angi **Integrering med Microsoft Dynamics 365 Finance**. |
| Tillatte tilskuddstyper | Tillatte tilskuddstyper | Et tilskudd representerer brukerens tillatelse til å hente et tilgangstoken. Ved å velge bestemte tilskudd godtar du de tilsvarende metodene for å hente et tilgangstoken. | <p>Velg følgende tilskuddstyper:</p><ul><li>**authorization_code**</li><li>**refresh_token**</li></ul> |
| Klientautentiseringsmetode | Godkjenningsmetode for klient | Godkjenningsmetode for klienten. | Angi **client_secret_post**. |
| Applikasjonstype | Programtype | Programtypen (eller klienten) er typen kjøretidsmiljø som klienten kjører under. OAuth2-kapitlet 2.1 viser de tilgjengelige alternativene. Valget av klienttype er en sikkerhetsvurdering som kunden vil utføre. | Velg **web**. |
| Gyldig(e) omdirigerings-uri-er | Gyldige omdirigerings-URIer | Denne parameteren gjelder bare for personlige påloggingsintegreringer. Den angir URIene som klienten har tillatelse til å gå til etter pålogging. | I Finance kan du gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**, kopiere URL-adressen (HTTPS-internettadressen) fra leserens adresselinje og lime den inn i dette feltet. |
| Gyldig(e) post logout redirect uri-er | Gyldig(e) post logout redirect URI-er | Denne parameteren gjelder bare for personlige påloggingsintegreringer. Den angir URIene som klienten har tillatelse til å gå til etter avlogging. | Angi `https://skatteetaten.no`. |
| Frontchannel logout uri | URI for Frontchannel-avlogging | URI-en som leverandøren sender en forespørsel til ved avlogging som utløses av en annen klient i den samme økten. Hvis du ikke angir denne parameteren, er det fare for at brukeren fremdeles kan være logget på tjenesten når de logger seg av ID-porten. | Angi `https://skatteetaten.no`. |
| Frontchannel logout krever sesjons-id | Frontchannel-avlogging krever økt-ID | Denne parameteren gjelder bare for personlige påloggingsintegreringer. Det er et flagg som bestemmer om utsteder- og økt-ID-parameterne sendes sammen med **frontchannel_logout_uri**. | La denne boksen stå tom. |
| Tilbake-uri | Tilbake-URI | Denne parameteren gjelder bare for personlige påloggingsintegreringer. Den angir URI-en som en bruker blir sendt tilbake til når de avbryter påloggingen. | Angi `https://skatteetaten.no`. |
| Authorization levetid (sekunder) | Autorisasjonslevetid (sekunder) | Levetiden for den registrerte autorisasjonen. I en OpenID Connect-kontekst vil denne autorisasjonen få tilgang til sluttpunktet userinfo. Verdien må angis i sekunder. | Angi **31536000** (= ett år). |
| Tilgangstoken levetid (sekunder) | Tilgangstokenlevetid (sekunder) | Levetiden for utstedte **access_token** i sekunder. | Angi **7200** (= to timer). |
| Refresh token levetid (sekunder) | Oppdateringstokenlevetid (sekunder) | Levetiden for det utstedte **refresh_token** i sekunder. | Angi **0** (null). |
| Oppdater tokentype | Oppdater tokentype | <ul><li>**Én gang** – Du får en ny **refresh_token** hver gang du oppdaterer **access_token**.</li><li>**Kan brukes på nytt** – En oppdatering av **access_token** endrer ikke **refresh_token**.</li></ul> | Angi **Engangs**. |

![Registrer et integreringspunkt i webportalen for ID-porten.](media/emea-nor-vat-return-integration-point.png)

> [!IMPORTANT]
> Pass på at du trygt lagrer klient-IDen og klienthemmeligheten for integreringspunktet som du oppretter for samhandling med ID-porten. Du trenger disse legitimasjonene i trinnet [Definere klient-IDen og klienthemmelighet for integreringspunktet for ID-porten i Finance ](emea-nor-vat-return-setup.md#client-credentials) i forberedelsene til direkte innsending av mva-returer til Altinn i Finance.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
