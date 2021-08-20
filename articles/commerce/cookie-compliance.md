---
title: Samsvar for informasjonskapsel
description: Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 509ae998b4d0fa8ab6dd5e3d242dfb4abc492952cd66addc04050fbaff949326
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747703"
---
# <a name="cookie-compliance"></a>Informasjonskapselsamsvar

[!include [banner](includes/banner.md)]

Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.

Personvern er en viktig faktor når det brukes sporingsteknologier som påvirker e-handelskunder. På grunn av standarder for overholdelse av personvern, for eksempel EUs personvernforordning (GDPR) i den europeiske union (EU), må det tas hensyn til elektroniske personvernsretningslinjer for alle nettsteder som er aktive i dag. Fordi mange e-handelsområder er globalt tilgjengelige som standard, er det viktig at du går gjennom samsvarsstandardene for e-handelsområdet ditt.

Hvis du vil vite mer om de grunnleggende prinsippene som Microsoft bruker for samsvar for informasjonskapsler, kan du gå til [Microsoft Trust Center](https://www.microsoft.com/trust-center). På dette området kan du også få mer informasjon om samsvarsområder og personvern.

Tabellen nedenfor viser gjeldende referanseliste over informasjonskapsler for Dynamics 365 Commerce-områder.

| Navn på informasjonskapsel                               | Bruk                                                        | Levetid |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Cookies                             | Lagre Microsoft Azure Active Directory (Azure AD)-godkjenningsinformasjonskapsler for enkel pålogging (single sign-on – SSO). Lagrer krypter hovedinformasjon for brukeren (namn, etternavn, e-post). | Økt |
| \_msdyn365___cart_                           | Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst. | Økt |
| \_msdyn365___checkout_cart_                           | Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst. | Økt |
| \_msdyn365___ucc_                            | Sporing av informasjonskapselsamsvar.                          | 1 år |
| ai_session                                  | Registrerer hvor mange økter med brukeraktivitet som har tatt med bestemte sider og funksjoner i appen. | 30 minutter |
| ai_user                                     | Oppdager hvor mange personer som brukte appen og funksjonene i den. Brukere telles ved hjelp av anonyme IDer. | 1 år |
| b2cru                                       | Butikker omadresserer URL dynamisk.                              | Økt |
| JSESSIONID                                  | Brukes av betalingskoblingen Adyen til å lagre brukerøkt.       | Økt |
| OpenIdConnect.nonce.&#42;                       | Godkjenning                                               | 11 minutter |
| x-ms-cpim-cache:.&#42;                          | Brukes til å vedlikeholde forespørselstilstanden.                      | Økt |
| x-ms-cpim-csrf                              | CRSF-token (forfalskning av forespørsler på tvers av nettsteder) som brukes til beskyttelse fra CRSF.     | Økt |
| x-ms-cpim-dc                                | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. | Økt |
| x-ms-cpim-rc.&#42;                              | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. | Økt |
| x-ms-cpim-slice                             | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. | Økt |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Brukes til vedlikehold av SSO-økten.                        | Økt |
| x-ms-cpim-trans                             | Brukes til å spore transaksjoner (antallet åpne faner som godkjennes mot et forretning-til-forbruker-område) (B2C), inkludert den gjeldende transaksjonen. | Økt |
| \_msdyn365___muid_                            | Brukes hvis eksperimentering er aktivert for miljøet, brukt som bruker-ID til eksperimenteringsformål. | 1 år |
| \_msdyn365___exp_                             | Brukes hvis eksperimentering er aktivert for miljøet, brukes til å måle ytelsesbelastningsfordeling.         | 1 time |
| d365mkt                                       | Brukes hvis lokasjonsbasert registrering for å spore en brukers IP-adresse for butikklokasjonsforslag er aktivert i Commerce-områdebygger ved **Områdeinnstillinger \> Generelt \> Aktiver lokasjonsbasert butikkregistrering**.      | 1 time |
| \_msdyn365___tuid_                           | Brukes bare hvis eksperimentering er aktivert for et miljø. Genererer en GUID som skal fungere som en brukeridentifikator. Verdien endres hvis en brukers påloggingsstatus endres.      | 1 år |
| \_msdyn365___aud_0                          | Lagrer segmentverdier som brukes av målretting, og brukes bare hvis målretting er konfigurert på en side eller et fragment forespurt av en områdebruker. Informasjonskapselen plasseres bare når segmentverdiene kommer fra en tredjeparts segmenteringsleverandør.      | 7 dager |
| \_msdyn365___aud_1                           | Lagrer segmentverdier som brukes av målretting, og brukes bare hvis målretting er konfigurert på en side eller et fragment forespurt av en områdebruker. Informasjonskapselen plasseres bare når segmentverdiene kommer fra en tredjeparts segmenteringsleverandør.      | 7 dager |
| \_msdyn365___aud_2                           | Lagrer segmentverdier som brukes av målretting, og brukes bare hvis målretting er konfigurert på en side eller et fragment forespurt av en områdebruker. Informasjonskapselen plasseres bare når segmentverdiene kommer fra en tredjeparts segmenteringsleverandør.      | 7 dager |

Hvis en områdebruker velger noen koblinger på sosiale medier på et område, vil informasjonskapslene som ligger i tabellen nedenfor, også spores i nettleseren.


| Domene                      | Informasjonskapsel               | beskrivelse                                                  | Kilde                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | Synkronisering av ID for LinkedIn-annonser                                      | LinkedIn-oppdatering og innsiktstagg                                |
| .linkedin.com               | li_sugr                  | Nettleser-ID                                           | LinkedIn-innsiktstagg hvis IP-adressen ikke er i et angitt land |
| .linkedin.com               | BizographicsOptOut       | Bestemmer utmeldingsstatusen for tredjepartssporing.              | LinkedIn-gjestekontroller og bransjeutmeldingssider           |
| .linkedin.com               | \_guid                    | Nettleser-ID for Google-annonser.                            | LinkedIn-oppdatering                                                |
| .linkedin.com               | li_oatml                 | Indikrekte medlems-ID for konverteringssporing, ny målretting og analyse. | LinkedIn-annonser og innsiktstagger                                |
| Diverse førstepartsdomener | li_fat_id                | Indikrekte medlems-ID for konverteringssporing, ny målretting og analyse. | LinkedIn-annonser og innsiktstagger                                |
| .adsymptotic.com            | U                        | Nettleser-ID                                           | LinkedIn-innsiktstagg hvis IP-adressen ikke er i et angitt land |
| .linkedin.com                | bcookie                  | Informasjonkapsel for nettleser-ID                                            | Forespørsler til LinkedIn                                         |
| .linkedin.com                | bscookie                 | Informasjonskapsel for sikker nettleser                                        | Forespørsler til LinkedIn                                         |
| .linkedin.com               | lang                     | Angir standard nasjonal innstilling og standardspråk.                                 | Forespørsler til LinkedIn                                         |
| .linkedin.com                | lidc                     | Brukes til ruting.                                             | Forespørsler til LinkedIn                                         |
| .linkedin.com               | aam_uuid                 | Adobe Audience Manager-informasjonskapsel                                                     | Angi for ID-synkronisering                                              |
| .linkedin.com               | \_ga                      | Google Analytics-informasjonskapsel                                            | Google Analytics                                             |
| .linkedin.com               | \_gat                     | Google Analytics-informasjonskapsel                                             | Google Analytics                                             |
| .linkedin.com               | liap                     | Google Analytics-informasjonskapsel                                             | Google Analytics                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Informasjonskapselen inneholder bruker-IDen til den påloggede brukeren.  |   Facebook                                                           |
| .facebook.com               | datr                     | Brukes til å identifisere nettleseren som brukes til tilkobling til Facebook, uavhengig av pålogget bruker. | Facebook                                                             |
| .facebook.com               | wd                       | Lagrer dimensjonene for nettleservinduet og brukes av Facebook til å optimalisere gjengivelsen av siden. | Facebook                                                             |
| .facebook.com               | xs                       | Tosifret tall som representerer øktnummeret. Andre del av verdien er en økthemmelighet. |  Facebook                                                            |
| .facebook.com               | fr                       | Inneholder en unik nettleser- og bruker-ID som brukes til målrettet reklame. |  Facebook                                                            |
| .facebook.com               | sb                       | Brukes til å forbedre venneforslag på Facebook.                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Informasjonskapselen inneholder bruker-IDen til den påloggede brukeren.  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Informasjonskapselen inneholder bruker-IDen til den påloggede brukeren.  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Informasjonskapselen inneholder sider når brukeren velger Pinterest-knappen.      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Informasjonskapselen inneholder sider når brukeren velger Pinterest-knappen.      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | Inneholder en bruker-ID og tidsstemplet da informasjonskapselen ble opprettet. |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Informasjonskapselen inneholder sider når brukeren velger Pinterest-knappen.      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Informasjonskapselen inneholder sider når brukeren velger Pinterest-knappen.      | Pinterest                                                             |
| .pinterest.com              | Lokalt lager            |                                                              |  Pinterest                                                            |
| .pinterest.com              | Tjenestearbeidere          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Godkjenning av områdebrukerens informasjonskapsel på et e-handelsområde 

Hvis en funksjon i et e-handelsområde eller en modul bruker en ikke-vesentlig informasjonskapsel, må du oppnå en brukers tillatelse før informasjonskapselen spores. Hvis du vil tillate at brukere skal kunne tilby informasjonskapseltillatelse på e-handelsområdet, må en områdeforfatter legge til og konfigurere en samtykkemodul for informasjonskapsler i topptekstmodulen for siden for å sikre at samtykke blir bedt om og mottatt. Brukersamtykke for område må gis før en funksjon eller modul som bruker en ikke-vesentlig informasjonskapsel, kan gjengis på en områdeside.

## <a name="additional-resources"></a>Tilleggsressurser

[Funksjoner og egenskaper for tilgjengelighet](accessibility.md)

[Samsvarsoversikt](compliance-overview.md)

[Legge til en side for personvernpolicy](add-privacy-page.md)

[Erstatte bruker-ID-er som er knyttet til sporede innholdsendringer](replace-IDs-tracked-changes.md)

[Samtykkemodul for informasjonskapsel](cookie-consent-module.md) 
 
[Topptekstmodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
