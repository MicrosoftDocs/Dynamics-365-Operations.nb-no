---
title: Samsvar for informasjonskapsel
description: Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
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
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796033"
---
# <a name="cookie-compliance"></a>Informasjonskapselsamsvar

[!include [banner](includes/banner.md)]

Dette emnet beskriver vurderinger for overholdelse av informasjonskapsler og standardpolicyene som er inkludert i Microsoft Dynamics 365 Commerce.

Personvern er en viktig faktor når det brukes sporingsteknologier som påvirker e-handelskunder. På grunn av standarder for overholdelse av personvern, for eksempel EUs personvernforordning (GDPR) i den europeiske union (EU), må det tas hensyn til elektroniske personvernsretningslinjer for alle nettsteder som er aktive i dag. Fordi mange e-handelsområder er globalt tilgjengelige som standard, er det viktig at du går gjennom samsvarsstandardene for e-handelsområdet ditt.

Hvis du vil vite mer om de grunnleggende prinsippene som Microsoft bruker for samsvar for informasjonskapsler, kan du gå til [Microsoft Trust Center](https://www.microsoft.com/trust-center). På dette området kan du også få mer informasjon om samsvarsområder og personvern.

Tabellen nedenfor viser gjeldende referanseliste over informasjonskapsler for Dynamics 365 Commerce-områder.

| Navn på informasjonskapsel                               | Bruk                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | Lagre Microsoft Azure Active Directory (Azure AD)-godkjenningsinformasjonskapsler for enkel pålogging (single sign-on – SSO). Lagrer krypter hovedinformasjon for brukeren (namn, etternavn, e-post). |
| &#95;msdyn365___cart&#95;                           | Handlekurv-ID som brukes til å hente liste over produkter som er lagt til i handlekurvforekomst. |
| &#95;msdyn365___ucc&#95;                            | Sporing av informasjonskapselsamsvar.                          |
| ai_session                                  | Registrerer hvor mange økter med brukeraktivitet som har tatt med bestemte sider og funksjoner i appen. |
| ai_user                                     | Oppdager hvor mange personer som brukte appen og funksjonene i den. Brukere telles ved hjelp av anonyme IDer. |
| b2cru                                       | Butikker omadresserer URL dynamisk.                              |
| JSESSIONID                                  | Brukes av betalingskoblingen Adyen til å lagre brukerøkt.       |
| OpenIdConnect.nonce.&#42;                       | Godkjenning                                               |
| x-ms-cpim-cache:.&#42;                          | Brukes til å vedlikeholde forespørselstilstanden.                      |
| x-ms-cpim-csrf                              | CRSF-token (forfalskning av forespørsler på tvers av nettsteder) som brukes til beskyttelse fra CRSF.     |
| x-ms-cpim-dc                                | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. |
| x-ms-cpim-rc.&#42;                              | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. |
| x-ms-cpim-slice                             | Brukes til å rute forespørsler til den aktuelle serverforekomsten for produksjonsgodkjenning. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Brukes til vedlikehold av SSO-økten.                        |
| x-ms-cpim-trans                             | Brukes til å spore transaksjoner (antallet åpne faner som godkjennes mot et forretning-til-forbruker-område) (B2C), inkludert den gjeldende transaksjonen. |

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
