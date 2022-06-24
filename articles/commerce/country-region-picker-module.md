---
title: Land-/områdevelgermodul
description: Denne artikkelen beskriver land/områdevelgermodulen og beskriver hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: d20b3be008a37b1c86e6fefe0ccc90c581e18340
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861998"
---
# <a name="countryregion-picker-module"></a>Land-/områdevelgermodul

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver land/områdevelgermodulen og beskriver hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Land-/områdevelgermodulen bruker funksjonen for [registrering og omadressering av georeplikering](geo-detection-redirection.md) i Dynamics 365 Commerce for å vise anbefalte nettsteder til kunder som ber om en URL-adresse for e-handel som ikke er knyttet til landet eller regionen deres.

En kunde i Canada ber for eksempel om en URL-adresse som er tilknyttet et annet land enn Canada. I dette tilfellet viser land-/områdevelgermodulen en dialogboks som anbefaler URL-adresser for områder som er tilknyttet Canada. 

## <a name="how-it-works"></a>Hvordan det fungerer

Når registrering og omadressering av georeplikering er aktivert for et nettsted, og en kunde ber om en URL-adresse, brukes landet som er registrert for kunden og URL-adressen kunden har bedt om, til å fastslå om URL-adressen er tilordnet landet der kunden er. Tilordningen mellom URL-adresser og land er definert på **Kanaler**-siden under **Områdeinnstillinger** i Commerce Site Builder. 

Hvis den forespurte URL-adressen ikke samsvarer med en URL-adresse som er tilordnet kundens land, blir listen over én eller flere URL-adresser som er tilordnet dette landet, returnert i svaret. Land-/områdevelgeren sammenligner hver URL-adresse i den listen med URL-adressene som er konfigurert i land-/områdemodulen. For hvert nøyaktige treff som blir funnet, gjengir land-/områdevelgeren visningsoverskriften, underoverskriften og bildet for denne URL-adressen, og hyperkobler disse elementene ved hjelp av URL-adressen.

Når en kunde velger et alternativ i land-/områdevelgeren, tas de til den hyperkoblede URL-adressen. Denne URL-adressen skrives til informasjonskapselen **\_msdyn365\_\_\_nettsted\_**, slik at den kan brukes som kundens nettstedspreferanse. Neste gang kunden ber om en URL-adresse som ikke er knyttet til kundens land eller område, blir kunden automatisk sendt videre til det foretrukkede landet. Derfor anbefaler vi at du også bruker [områdevelgermodulen](site-selector.md) på e-handelsområdet ditt, slik at kunder kan overstyre eller oppdatere områdepreferansene sine. 

Hvis en kunde lukker dialogboksen med land-/områdevelgeren, skrives det ikke en informasjonskapsel, og kunden blir værende på det gjeldende nettstedet. 

Illustrasjonen nedenfor viser et eksempel på dialogboksen for land/områdevelger.

![Eksempel på dialogboksen for land/områdevelger på en hjemmeside.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Egenskaper for Land-/områdevelgermodul

| Egenskapsnavn              | Verdi       | beskrivelse                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Overskrift                    | Tekst        | Overskriften som vises øverst i dialogboksen.       |
| Underoverskrift                 | Tekst        | Underoverskriften som vises under overskriften.               |
| Land: Visningsstreng    | Tekst        | Visningsnavnet for et URL-alternativ (for eksempel "Canada").   |
| Land: Visningsunderstreng | Tekst        | Valgfri visningsunderstreng for et URL-alternativ (for eksempel "engelsk" eller "fransk"). |
| Land: Landsbilde     | Medieaktivum | Et valgfritt bilde som er knyttet til et URL-alternativ (for eksempel et bilde av det kanadiske flagget). |
| Land: Lands-URL       | Tekst        | URL-adressen for landet/området som konfigureres. Denne URL-adressen må samsvare nøyaktig med URL-adressen du angav for landet/området på **Kanaler**-siden under **Områdeinnstillinger** i Commerce Site Builder. I tillegg må domenet for URL-adressen være det egendefinerte domenet som er angitt i feltet **Samsvar domene** på **Kanaler**-siden, og ikke den fungerende adressen for nettstedet som Commerce gir deg når du oppretter e-handelsmiljøet (for eksempel URL-adressen `https://<yourcompany>.commerce.dynamics.com/`). |
| Handlingskobling                | Handlingskobling | En valgfri kobling som vises nederst i dialogboksen. Denne koblingen kan for eksempel peke til en intern side som inneholder en liste over alle land og områder som området støtter. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Legge til en land-/områdevelgermodul på en side

Land-/områdevelgermodulen kan legges til i hodemodulen enten direkte eller via et delt fragment. Hvis du vil ha mer informasjon om topptekstmoduler, kan du se [Topptekstmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurere land-/områdevelgermodulen i Commerce-områdebygger

> [!NOTE]
> URL-ene som du anbefaler til kundene, må konfigureres som landobjekter i land-/områdevelgermodulen.

For hver URL-adresse du vil vise og anbefale til kunder, følger du denne fremgangsmåten i Commerce Site Builder.

1. Velg land-/områdevelgermodul-sporet.
1. I egenskapsruten under **Landliste** velger du **Legg til land**.
1. Velg den nye **Land**-boksen.
1. I **Visningsstreng**-feltet angir du et visningsnavn (for eksempel **Canada**).
1. Valgfritt: I feltet **Visningsunderstreng** angir du en visningsunderstreng (for eksempel **Fransk** eller **fr-ca**).
1. Valgfritt: Velg et bilde fra mediebiblioteket.
1. Angi en URL-adresse i **URL-adresse for land**-feltet. Denne URL-adressen må samsvare med URL-adressen som vises på **Kanaler**-siden, og som er tilordnet kanalen, inkludert de nasjonale innstillingene som er tilknyttet landet eller området. 
1. Velg **OK**.
1. Gjenta disse trinnene for eventuelle andre land-URL-er som du vil at land-/områdevelgermodulen skal vise.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere registrering og omadressering av georeplikering](geo-detection-redirection.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md)

[Områdevelgermodul](site-selector.md)

[Søkebanemodul](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
