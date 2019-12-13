---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785243"
---
# <a name="carousel-module"></a>Karusellmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En karusellmodul brukes til å legge flere kampanjevarer i en karusell som kunder kan bla gjennom. Det er en spesiell containermodul som er vert for andre moduler. En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.

Du kan legge til hovedbanner- og funksjonsmoduler i en karusellmodul. Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Eksempler på karusellmoduler i e-handel

- En karusell som har flere kampanjemoduler inni, kan brukes på en startside.
- En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.
- En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.

## <a name="carousel-module-properties"></a>Egenskaper for karusellmodul

| Egenskapsnavn             | Verdi                                | Beskrivelse |
|---------------------------|--------------------------------------|-------------|
| Autokjør                  | **Sann** eller **Usann**                | Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk. Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element. |
| Intervall for lysbildeovergang | En verdi i sekunder                   | Intervallet for overganger mellom elementer. |
| Overgangsanimasjon      | **Lysbilde** eller **Toning**                | Overgangseffekten. |
| Bredde                     | **Tilpass container** eller **Fyll skjerm** | Hvis verdien er satt til **Tilpass container**, er elementene i karusellen begrenset til bredden på karusellen. Hvis verdien er satt til **Fyll skjerm**, er ikke elementene begrenset til karusellbredden, men de kan gå i fullskjermmodus. Du kan endre verdien for å oppnå det ønskede oppsettet. |

## <a name="add-a-carousel-module-to-a-page"></a>Legge til en karusellmodul på en side

Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **karusellmal**.
1. I **Hoved**-sporet på standardsiden legger du til en karusellmodul.
1. Legg til en hovedbannermodul i karusellmodulen.
1. Legg til en funksjonsmodul i karusellmodulen.
1. Sjekk inn malen, og publiser den. 
1. Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **karusellside**.
1. I **Hoved**-sporet på den nye siden legger du til en karusellmodul.
1. Angi egenskapen **Bredde** for karusellmodulen for å **fylle skjermen**. 
1. Angi egenskapen **Overgangsanimasjon** til **Lysbilde**.
1. Legg til en hovedbannermodul i karusellmodulen.
1. Legg til et bilde og en overskrift i hovedbannermodulen, og velg deretter **Lagre**.
1. Legg til en funksjonsmodul i karusellmodulen.
1. I funksjonsmodulen legger du til et bilde, en overskrift og et avsnitt med tekst.
1. Lagre og forhåndsvis siden. Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul). Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.
1. Sjekk inn siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Varselmodul](add-alert.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Funksjonsmodul](add-feature-module.md)

[Hovedbannermodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)
