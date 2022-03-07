---
title: Land-/områdevelgermodul
description: Dette emnet beskriver land/områdevelgermodulen og beskriver hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
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
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 35d78cdcc356d35776940147e9b0afee0f0be2a2
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674729"
---
# <a name="countryregion-picker-module"></a>Land-/områdevelgermodul

[!include [banner](includes/banner.md)]

Dette emnet beskriver land/områdevelgermodulen og beskriver hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Land-/områdevelgermodulen bruker funksjonen for [registrering og omadressering av georeplikering](geo-detection-redirection.md) i Dynamics 365 Commerce for å vise anbefalte URL-adresser til kunder som ber om en URL-adresse for e-handel som ikke er knyttet til landet eller regionen deres.

En kunde i Canada ber for eksempel om en URL-adresse som ikke er tilknyttet Canada. I dette tilfellet viser land-/områdevelgermodulen en dialogboks som anbefaler URL-adresser for områder som er tilknyttet Canada. Illustrasjonen nedenfor viser et eksempel på dialogboksen for land/områdevelger.

![Eksempel på dialogboksen for land/områdevelger på en hjemmeside.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Egenskaper for Land-/områdevelgermodul

| Egenskapsnavn              | Verdi       | beskrivelse |
| -------------------------- | ----------- | ----------- |
| Overskrift                    | Tekst        | Overskriften som vises øverst i dialogboksen. |
| Underoverskrift                 | Tekst        | Underoverskriften som vises under overskriften. |
| Land: Visningsstreng    | Tekst        | Visningsnavnet for et URL-alternativ (for eksempel "Canada"). |
| Land: Visningsunderstreng | Tekst        | Valgfri visningsunderstreng for et URL-alternativ (for eksempel "engelsk" eller "fransk"). |
| Land: Landsbilde     | Medieaktivum | Et valgfritt bilde som er knyttet til et URL-alternativ (for eksempel et bilde av det kanadiske flagget). |
| Land: Lands-URL       | Tekst        | URL-adressen som tilsvarer kanalen og de nasjonale innstillingene som er konfigurert for landet eller området på **Kanaler**-siden i Commerce-områdebygger (**Områdeinnstillinger \> Kana<ler**). Denne URL-adressen må samsvare med URL-adressen som er konfigurert på **Kanaler**-siden. |
| Handlingskobling                | Handlingskobling | En valgfri kobling som vises nederst i dialogboksen. Denne koblingen kan for eksempel peke til en intern side som inneholder en liste over alle land og områder som området støtter. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Legge til en land-/områdevelgermodul på en side

Land-/områdevelgermodulen kan legges til i hodemodulen enten direkte eller via et delt fragment. Hvis du vil ha mer informasjon om topptekstmoduler, kan du se [Topptekstmodul](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Konfigurere land-/områdevelgermodulen i Commerce-områdebygger

> [!NOTE]
> URL-ene som du anbefaler til kundene, må konfigureres som landobjekter i land-/områdevelgermodulen.

For hver URL-adresse du vil vise og anbefale til kunder, følger du denne fremgangsmåten i Commerce-områdebygger.

1. Velg land-/områdevelgermodul-sporet.
1. I egenskapsruten under **Landliste** velger du **Legg til land**.
1. Velg den nye **Land**-boksen.
1. I **Visningsstreng**-feltet angir du et visningsnavn (for eksempel **Canada**).
1. Valgfritt: I feltet **Visningsunderstreng** angir du en visningsunderstreng (for eksempel **Fransk** eller **fr-ca**).
1. Valgfritt: Velg et bilde fra mediebiblioteket.
1. Angi en URL-adresse i **URL-adresse for land**-feltet. Denne URL-adressen må samsvare med URL-adressen som vises på **Kanaler**-siden, og er tilordnet kanalen, inkludert de nasjonale innstillingene som er tilknyttet landet eller området.
1. Velg **OK**.
1. Gjenta disse trinnene for eventuelle andre land-URL-er som du vil at land-/områdevelgermodulen skal vise.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere registrering og omadressering av georeplikering](geo-detection-redirection.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
