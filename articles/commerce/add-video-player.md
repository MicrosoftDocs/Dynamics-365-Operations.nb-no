---
title: Videospillermodul
description: Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025667"
---
# <a name="video-player-module"></a>Videospillermodul


[!include [banner](includes/banner.md)]

Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Videospillermodulen brukes til å støtte videoavspilling. Den kan legges til på en hvilken som helst side, forutsatt at videoinnhold lastes opp til og er tilgjengelig i innholdsbehandlingssystemet (CMS). Videospillermodulen støtter MP4-medietypen.

## <a name="video-player-module"></a>Videospillermodul

Videospillermodulen kan brukes til å vise videoer på et e-handelsområde. Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus, lydbeskrivelser og teksting for hørselshemmede. Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder. Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.

Videospiller-modulen støtter også sekundære lydspor. Når en video er lastet opp til CMS, kan du også laste opp et sekundært lydspor. Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Eksempler på omgivelsesvideospillermoduler i e-handel

- Instruksjonsvideoer på produktdetaljsider eller markedsføringssider
- Kampanjevideoer eller videoer om policyer på en hvilken som helst markedsføringsside
- Markedsføringsvideoer som fremhever produktfunksjoner på sider med produktdetaljer eller markedsføringssider

### <a name="video-player-module-properties"></a>Egenskaper for videospillermodul

| Egenskapsnavn         | Verdi                               | Beskrivelse |
|-----------------------|-------------------------------------|-------------|
| Automatisk avspilling             | **Sann** eller **Usann**               | Når verdien settes til **Sann**, spilles videoen automatisk. |
| Demp                  | **Sann** eller **Usann**               | Når verdien settes til **Sann**, dempes lyden. For denne spilleren er standardverdien **Usann**. I Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt. |
| Løkke                  | **Sann** eller **Usann**               | Når verdien settes til **Sann**, gjentas videoen i en løkke. |
| Medier                 | Filbane og -navn for video. | Videofilen som spilles av i videospilleren. |
| Spille av fullskjerm       | **Sann** eller **Usann**               | Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus. |
| Utløser for avspilling/pause    | **Sann** eller **Usann**               | Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen. |
| Kontroller for videospiller | **Sann** eller **Usann**               | Når verdien settes til **Sann**, vises alle videospillerkontroller. Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og alternativer for teksting for hørselshemmede. |
| Skjul plakatbilde     | **Sann** eller **Usann**               | En video kan ha en plakatramme. Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult. |
| Maskenivå            | Et tall fra **0** til **100** | Masken som brukes på videoen for styling. |

## <a name="add-a-video-player-module-to-a-page"></a>Legge til en videospillermodul på en side

> [!NOTE] 
> Før du oppretter en videospillermodul, må du først laste opp en video til mediebiblioteket.

Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **videospillermal**.
1. I **Hoved**-sporet på standardsiden legger du til en containermodul.
1. I containermodulen legger du til videospiller og omgivelsesvideospillermoduler.
1. Fullfør redigeringen av malen, og publiser den.
1. Bruk videospillermalen du opprettet, for å opprette en side som heter **videospillerside**.
1. I **Hoved**-sporet på den nye siden legger du til en videospillermodul.
1. Velg **Legg til en video** i egenskapsruten for videospillermodulen.
1. Velg en video i dialogboksen **Medievelger**, og velg deretter **Last opp nytt medieelement** .
1. Lagre og forhåndsvis siden. Du skal se videomodulen på siden. Du kan endre flere innstillinger for å tilpasse virkemåten til modulen.
1. Fullfør redigeringen av siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Kampanjebannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Innholdsblokkmodul](add-hero-module.md)
