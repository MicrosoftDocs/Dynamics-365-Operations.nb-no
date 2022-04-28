---
title: Områdevelgermodul
description: Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
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
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551700"
---
# <a name="site-picker-module"></a>Områdevelgermodul

[!include [banner](includes/banner.md)]

Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.

Når en bedrift har forskjellige områder på tvers av markeder, områder og nasjonale innstillinger, trenger områdebrukere en enkel måte å veksle mellom områder og velge foretrukket område for shopping. For å ta hensyn til dette scenarioet lar områdevelgermodulen brukere bla gjennom på tvers av flere områder. En områdevelger anbefales også når [registrering og omadressering av georeplikering](geo-detection-redirection.md) er implementert for e-handelsområdet, slik at kunder kan overstyre områdepreferansene som de angir ved å bruke [land-/områdevelgermodulen](country-region-picker-module.md). 

Områdevelgermodulen må være konfigurert med listen over områder (markeder, områder eller nasjonale innstillinger) som områdebrukere kan bla gjennom. Illustrasjonen nedenfor viser et eksempel på en områdevelgermodul som vises i toppteksten på en områdeside.

![Eksempel på en områdevelgermodul i toppteksten på en områdeside.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Egenskaper for områdevelgermodul

| Egenskapsnavn | Verdi                 | Beskrivelse |
|---------------|-----------------------|-------------|
| Overskrift       | Tekst                  | Overskriften for modulen. |
| Områdealternativer  | Navn, bilde, URL-adresse      | Denne egenskapen angir et navn, en kobling til startsiden for området, og et valgfritt bilde som skal vises for hvert område som er inkludert i modulen. Bildet kan være et flagg, eller en presentasjon av et marked, en region eller et land. |

## <a name="add-a-site-picker-module-to-a-page"></a>Legge til en områdevelgermodul på en side

Områdevelgermodulen kan legges til i [topptekstmodulen](author-header-module.md) under **Områdevelger**-sporet. Etter at en områdevelgermodul er lagt til, kan du definere moduloverskriften og områdealternativene. En topptekstmodul er i et topptekstfragment som kan deles på tvers av e-handelssider for et område. I eksemplet nedenfor har områdevelgermodulen blitt lagt til **Områdevelger**-sporet i en topptekstmodul som er i et topptekstfragment kalt **HeaderContainer**.

![Eksempel på en områdevelgermodul i et topptekstfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md)

[Søkebanemodul](add-breadcrumb.md)

[Navigasjonsmenymodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
