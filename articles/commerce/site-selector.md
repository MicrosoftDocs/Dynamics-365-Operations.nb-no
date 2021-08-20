---
title: Områdevelgermodul
description: Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: a5f6f6e3ff459447aa4b3c0058b5526c9e8d1038a5d2629eefbed197012aebf0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772234"
---
# <a name="site-selector-module"></a>Områdevelgermodul

[!include [banner](includes/banner.md)]

Dette emnet dekker områdevelgermodulen og beskriver hvordan du legger den til områdesider i Microsoft Dynamics 365 Commerce.

Når en bedrift har forskjellige områder på tvers av markeder, områder og nasjonale innstillinger, trenger områdebrukere en enkel måte å veksle mellom områder og velge foretrukket område for shopping. For å få plass til dette scenarioet lar områdevelgermodulen brukere bla gjennom flere områder.

Områdevelgermodulen må være konfigurert med listen over områder (markeder, regioner eller nasjonale innstillinger) som områdebrukere kan bla gjennom.

> [!NOTE]
> Områdevelgermodulen er tilgjengelig i Dynamics 365 Commerce 10.0.14-versjonen.

Illustrasjonen nedenfor viser et eksempel på en områdevelgermodul som vises i hodet på en områdeside.

![Eksempel på en områdevelgermodul i toppteksten på en områdeside.](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Egenskaper for områdevelgermodul

| Egenskapsnavn | Verdi                 | beskrivelse |
|---------------|-----------------------|-------------|
| Overskrift       | Tekst                  | Overskriften for modulen. |
| Områdealternativer  | Navn, bilde, URL-adresse      | Denne egenskapen angir et navn, en kobling til startsiden for området, og et valgfritt bilde som skal vises for hvert område som er inkludert i modulen. Bildet kan være et flagg, eller en presentasjon av et marked, en region eller et land. |

## <a name="add-a-site-selector-module-to-a-page"></a>Legge til en områdevelgermodul på en side

Områdevelgermodulen kan legges til i [topptekstmodulen](author-header-module.md) under områdevelgersporet. Når den er lagt til, kan du definere moduloverskriften og områdealternativene.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Topptekstmodul](author-header-module.md)

[Søkebanemodul](add-breadcrumb.md)

[Navigasjonsmenymodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]