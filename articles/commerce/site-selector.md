---
title: Områdevelgermodul
description: Denne artikkelen dekker områdevelgermodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: efd58206d88618aedb6b574afb47da1e9e578ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276755"
---
# <a name="site-picker-module"></a>Områdevelgermodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker områdevelgermodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

Når en bedrift har forskjellige områder på tvers av markeder, områder og nasjonale innstillinger, trenger områdebrukere en enkel måte å veksle mellom områder og velge foretrukket område for shopping. For å ta hensyn til dette scenarioet lar områdevelgermodulen brukere bla gjennom på tvers av flere områder. En områdevelger anbefales også når [registrering og omadressering av georeplikering](geo-detection-redirection.md) er implementert for e-handelsområdet, slik at kunder kan overstyre områdepreferansene som de angir ved å bruke [land-/områdevelgermodulen](country-region-picker-module.md). 

Områdevelgermodulen må være konfigurert med listen over områder (markeder, områder eller nasjonale innstillinger) som områdebrukere kan bla gjennom. Illustrasjonen nedenfor viser et eksempel på en områdevelgermodul som vises i toppteksten på en områdeside.

![Eksempel på en områdevelgermodul i toppteksten på en områdeside.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Egenskaper for områdevelgermodul

| Egenskapsnavn | Verdi                 | Beskrivelse |
|---------------|-----------------------|-------------|
| Overskrift       | Tekst                  | Overskriften for modulen. |
| Områdealternativer  | Navn, bilde, URL-adresse      | Denne egenskapen angir et navn, en kobling til startsiden for området, og et valgfritt bilde som skal vises for hvert område som er inkludert i modulen. Bildet kan være et flagg, eller en presentasjon av et marked, en region eller et land. |

## <a name="add-a-site-picker-module-to-a-page"></a>Legge til en områdevelgermodul på en side

Områdevelgermodulen kan legges til i [topptekstmodulen](author-header-module.md) under **Områdevelger**-sporet. Etter at en områdevelgermodul er lagt til, kan du definere moduloverskriften og områdealternativene. En topptekstmodul er i et topptekstfragment som kan deles på tvers av e-handelssider for et område. 

Følg fremgangsmåten nedenfor hvis du vil legge til områdevelgermodulen i en topptekstmodul.

1. I **Områdevelger**-sporet i topptekstmodulen for topptekstfragmentet velger du ellipsen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du en **Områdevelger**-modul, og deretter velger du **OK**.
1. Velg **Legg til liste over områdealternativer** i **Områdevelger**-listen. Det redigerbare alternativet **Liste over områdealternativer** vises.
1. Velg **Liste over områdealternativer**. Dialogboksen **Liste over områdealternativer** vises.
1. Under **Områdenavn** angir du teksten for områdenavn som skal vises i rullegardinlisten for områdevelger.
1. Velg **Legg til en kobling** under **Nettadresse for omadressering**. Underruten **Legg til en kobling** vises.
1. Velg **Egendefinert side** i underruten **Legg til en kobling**, og velg deretter **Neste**.
1. Velg nettadressen med banen du opprettet da du la til kanalen på området, fra listen over nettadresser (for eksempel `www.adventure-works.com/fr-ca`), og velg deretter **Bruk**.
1. Velg **OK**.
1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere siden.

I eksemplet nedenfor har områdevelgermodulen blitt lagt til **Områdevelger**-sporet i en topptekstmodul som er i et topptekstfragment kalt **HeaderContainer**.

![Eksempel på en områdevelgermodul i et topptekstfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md)

[Søkebanemodul](add-breadcrumb.md)

[Navigasjonsmenymodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
