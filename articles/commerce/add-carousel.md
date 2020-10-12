---
title: Karusellmodul
description: Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816992"
---
# <a name="carousel-module"></a>Karusellmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker karusellmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En karusellmodul brukes til å legge flere kampanjevarer (inkludert rike bilder) i et roterende karusellbanner som kunder kan bla gjennom. En forhandler kan for eksempel bruke en karusellmodul på en startside til å vise flere nye produkter eller kampanjer.

Du kan legge til innholdsblokkmoduler i en karusellmodul. Egenskapene for karusellmodulen definerer deretter hvordan disse modulene gjengis.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Eksempler på karusellmoduler i e-handel

- En karusell som har flere kampanjemoduler inni, kan brukes på en startside.
- En karusell som har flere kampanjemoduler inni, kan brukes på en produktdetaljside.
- En karusell kan brukes på en hvilken som helst markedsføringsside for å fremme flere kampanjer eller produkter.

Bildet nedenfor viser et eksempel på en karusellmodul som brukes på en hjemmeside. Denne karusellmodulen inneholder flere innholdsblokkelementer.

![Eksempel på en karusellmodul](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Egenskaper for karusellmodul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Autokjør                  | **Sann** eller **Usann** | Hvis verdien settes til **Sann**, skjer overgangen mellom elementer i karusellen automatisk. Hvis verdien settes til **Usann**, skjer ingen overgang med mindre kunden bruker tastaturet eller musen til å flytte fra ett element til neste element. |
| Intervall for lysbildeovergang | En verdi i sekunder    | Intervallet for overganger mellom elementer. |
| Overgangstype           | **Lysbilde** eller **Toning** | Overgangseffekten mellom varer. |
| Skjul karusellflipper     | **Sann** eller **Usann** | Hvis verdien settes til **Sann**, skjules karusellflipperen og sekvensindikatoren. |
| Tillat å forkaste karusell    | **Sann** eller **Usann** | Hvis verdien settes til **Sann**, kan brukerne forkaste karusellen. |

## <a name="add-a-carousel-module-to-a-page"></a>Legge til en karusellmodul på en side

Hvis du vil legge til en karusellmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Karusellmal**, og velger deretter **OK**.
1. Legg til en **Standardside**-modul i **Meldingstekst**-sporet.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.  
1. Bruk karusellmalen du nettopp opprettet, for å opprette en side som heter **Karusellside**.
1. I **Hoved**-sporet på den nye siden legger du til en containermodul. 
1. I ruten til høyre setter du **Bredde**-verdien til **Fyll skjerm**.
1. Under **Sideoppsett** legger du til en karusellmodul i containermodulen.
1. Legg til en innholdsblokkmodul i karusellmodulen. Angi egenskapene for innholdsblokkmodulen ved å angi **Overskrift**, **Kobling**, **Oppsett** og andre egenskaper.
1. Legg til og konfigurer en ny innholdsblokkmodul.
1. Angi flere egenskaper for karusellmodulen etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Siden skal vise en karusell med to moduler i (en hovedbannermodul og en funksjonsmodul). Du kan endre flere egenskaper for modulene karusell, hovedbanner og funksjon for å oppnå ønsket effekt.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Promobannermodul](add-alert.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Innholdsblokkmodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)
