---
title: Videospillermodul
description: Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885907"
---
# <a name="video-player-module"></a>Videospillermodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Videospillermoduler brukes til å støtte videoavspilling. To videospillermoduler finnes i startpakken for butikk: modulen for omgivelsesvideospiller og videospillermodulen. Begge spillerne støtter MP4-medietypen.

## <a name="ambient-video-player-module"></a>Omgivelsesvideospillermodul

Omgivelsesvideospillermodulen støtter korte informasjonsvideoer. Den bør brukes for videoer som er mindre enn fem sekunder lange. Denne spilleren støtter funksjoner for begrenset videoavspilling, for eksempel avspilling og pause.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Eksempler på videospillermoduler i e-handel

- Kort informasjonsvideoer som uthever nye produkter på startsiden
- Korte informasjonsvideoer som fremhever produktfunksjoner på en produktdetaljside

### <a name="ambient-video-player-module-properties"></a>Egenskaper for omgivelsesvideospillermodul

| Egenskapsnavn     | Verdi                 | Beskrivelse |
|-------------------|-----------------------|-------------|
| Autokjør          | **Sann** eller **Usann** | Når verdien settes til **Sann**, spilles videoen automatisk. |
| Demp              | **Sann** eller **Usann** | Når verdien settes til **Sann**, dempes lyden. For denne spilleren er standardverdien **Sann**. I Google Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt. |
| Løkke              | **Sann** eller **Usann** | Når verdien settes til **Sann**, gjentas videoen i en løkke. |
| Medier             |  Filbane og -navn for video. | Videofilen som spilles av videospilleren. |
| Avspillingskontroller | **Sann** eller **Usann** | Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen. Hvis verdien er satt til **Usann**, vises ikke knappen spill av / pause, men brukerne kan fremdeles stoppe og fortsette videoen ved hjelp av tastaturet. |

## <a name="video-player-module"></a>Videospillermodul

Videospillermodulen kan brukes til å vise videoer på et e-handelsområde. Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus og teksting for hørselshemmede. Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder. Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.

Videospiller-modulen støtter også sekundære lydspor. Når en video er lastet opp, kan du også laste opp et sekundært lydspor. Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.

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
| Avspillingskontroller     | **Sann** eller **Usann**               | Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen. Hvis verdien er satt til **Usann**, vises ikke knappen spill av / pause, men brukerne kan fremdeles stoppe og fortsette videoen ved hjelp av tastaturet. |
| Spille av fullskjerm       | **Sann** eller **Usann**               | Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus. |
| Kontroller              | **Sann** eller **Usann**               | Når verdien settes til **Sann**, vises alle kontroller. Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og teksting for hørselshemmede. |
| Skjul plakatramme     | **Sann** eller **Usann**               | En video kan ha en plakatramme. Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult. |
| Maskenivå            | Et tall fra **0** til **100** | Masken som brukes på videoen for styling. |
| Fullskjermikonstil | **Firkant** eller **Pil**             | Stilen som brukes på fullskjermsikonet som vises i videospilleren. |

## <a name="add-a-video-player-module-to-a-page"></a>Legge til en videospillermodul på en side

Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **videospillermal**.
1. I **Hoved**-sporet på standardsiden legger du til en containermodul.
1. I containermodulen legger du til videospiller og omgivelsesvideospillermoduler.
1. Sjekk inn malen, og publiser den.
1. Bruk videospillermalen du nettopp opprettet, for å opprette en side som heter **videospillerside**.
1. I **Hoved**-sporet på den nye siden legger du til en omgivelsesvideospillermodul.
1. I innstillingene for omgivelsesvideospillermodul går du til **Media** og laster opp en videofil. Du kan endre **Autokjør**, **Løkke** og andre egenskaper etter behov.
1. Lagre og forhåndsvis siden.
1. I **Hoved**-sporet på den nye siden legger du til en videospillermodul.
1. I innstillingene for videospillermodul går du til **Media** og laster opp en videofil.
1. Lagre og forhåndsvis siden. Du skal se begge videomodulene på siden. Du kan endre flere innstillinger for å tilpasse virkemåten til hver modul.
1. Sjekk inn siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Varselmodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Funksjonsmodul](add-feature-module.md)

[Hovedbannermodul](add-hero-module.md)
