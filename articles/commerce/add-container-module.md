---
title: Containermodul
description: Dette emnet dekker containermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 93c16da0988cc955835231bdd1f7342f19063f85
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025534"
---
# <a name="container-module"></a>Containermodul


[!include [banner](includes/banner.md)]

Dette emnet dekker containermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En containermodul er en modul som er vert for andre moduler i den. Hovedformålet med en containermodul er å definere, gjennom egenskapene som er angitt for den, oppsettet til modulene som den inneholder. Disse modulene kan for eksempel vises side ved side i et oppsett med to kolonner, tre kolonner, fire kolonner eller seks kolonner. De kan også begrenses til bredden på containeren, eller de kan fylle skjermen. En overskrift kan også legges til i hver containermodul.

Tre containermoduler støttes: container, container med 2 spor og container med 3 spor. Moduler av alle typer kan plasseres i disse containerne. 

> [!NOTE] 
> Vi anbefaler at du alltid plasserer moduler i en containermodul, slik at de kan begrenses til bredden på containeren.

## <a name="examples-of-container-modules-in-e-commerce"></a>Eksempler på containermoduler i e-handel

- En områdeforfatter vil ha et oppsett med tre kolonner, der tre moduler vises side om side. Derfor bruker områdeforfatteren en containermodul av containertypen med 3 spor.
- En områdeforfatter vil ha et oppsett med seks kolonner, der seks moduler vises side om side. Derfor bruker områdeforfatteren en container med containertypen med seks kolonner.
- En områdeforfatter vil legge en modul på en side, men vil ikke at den skal fylle skjermen. Derfor legger områdeforfatteren til modulen i en containermodul og setter containerens **Bredde**-egenskap til **Tilpass container**.

## <a name="container-module-properties"></a>Egenskaper for containermodul

| Egenskapsnavn     | Verdier | Beskrivelse |
|-------------------|--------|-------------|
| Overskrift           | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift kan angis for containeren. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Bredde             | **Tilpass container** eller **Fyll skjerm** | Hvis verdien er satt til **Tilpass container** (standardverdien), er modulene i containeren begrenset til bredden på containeren. Hvis verdien er satt til **Fyll skjerm**, er ikke modulene begrenset til containerbredden, men de kan fylle skjermen. |
| Antall kolonner | **1**, **2**, **3**, **4**, **6** eller **12** | Denne egenskapen definerer antallet kolonner i containeren. En container kan ha opptil 12 kolonner. |

## <a name="container-with-2-slots"></a>Beholder med 2 spor

Containertypen med 2 spor er optimalisert for et oppsett med to kolonner. Denne typen container har to spor for å tillate en side-ved-side-visning av modulene som er inni.

Du kan bruke flere egenskaper til å optimalisere oppsettet for forskjellige visningsporter (mobilenheter, nettbrett, datamaskiner og så videre). Bredden på hver kolonne kan defineres for hver visningsport. Følgende kolonnebreddeinnstillinger er tilgjengelige:

- **75%/25%** – Den første modulen har en kolonnebredde på 75 prosent, og den andre modulen har en kolonnebredde på 25 prosent. Et **25%/75%**-alternativ er også tilgjengelig.
- **50%/50%** – begge modulene har samme kolonnebredde.
- **67%/33%** – Den første modulen har en kolonnebredde på 67 prosent, og den andre modulen har en kolonnebredde på 33 prosent. Et **33%/67%**-alternativ er også tilgjengelig.
- **100%** – begge modulene har full kolonnebredde. Modulene stables derfor loddrett i én enkelt kolonne. Selv om dette oppsettet til en enkeltkolonne går mot formålet til containertypen med 2 spor, kan det være ønskelig for noen visningsporter (for eksempel ekstra små visningsporter som mobilenheter).

### <a name="container-with-2-slots-properties"></a>Container med 2-sporsegenskaper

| Egenskapsnavn                   | Verdier | Beskrivelse |
|---------------------------------|--------|-------------|
| Overskrift                         | Overskriftstekst og overskriftskode | En valgfri kan angis for containeren. |
| Konfigurasjon av ekstra liten visningsport | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%** | Denne egenskapen definerer oppsettet for ekstra små visningsporter. |
| Konfigurasjon av liten visningsport   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%** | Denne egenskapen definerer oppsettet for små visningsporter, for eksempel mobilenheter. |
| Konfigurasjon av medium visningsport  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%** | Denne egenskapen definerer oppsettet for medium visningsporter, for eksempel nettbrett. |
| Konfigurasjon av stor visningsport   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** eller **100%** | Denne egenskapen definerer oppsettet for store visningsporter, for eksempel datamaskiner. |

## <a name="container-with-3-slots"></a>Beholder med 3 spor

Containertypen med 3-sporsmoduler er optimalisert for et oppsett med tre kolonner.

Du kan bruke flere egenskaper til å optimalisere oppsettet for forskjellige visningsporter. Bredden på hver kolonne kan defineres for hver visningsport. Følgende kolonnebreddeinnstillinger er tilgjengelige:

- **33%/33%/33%** – Alle tre moduler har samme kolonnebredde.
- **50%/25%/25%** – Den første modulen har en kolonnebredde på 50 prosent, og hver av de to gjenværende modulene har en kolonnebredde på 25 prosent. **25%/50%/25%**- og **25%/25%/50%**-alternativer er også tilgjengelige.
- **16%/16%/67%** – Hver av de to første modulen har en kolonnebredde på 16 prosent, og den tredje modulen har en kolonnebredde på 67 prosent. **16%/67%/16%**- og **67%/16%/16%**-alternativer er også tilgjengelige.

### <a name="container-with-3-slots-properties"></a>Container med 3-sporsegenskaper

| Egenskapsnavn                   | Verdier | Beskrivelse |
|---------------------------------|--------|-------------|
| Overskrift                         | Overskriftstekst og overskriftskode | En valgfri overskrift kan legges til i containeren. |
| Konfigurasjon av ekstra liten visningsport | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%** | Denne egenskapen definerer oppsettet for ekstra små visningsporter. |
| Konfigurasjon av liten visningsport   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%** | Denne egenskapen definerer oppsettet for små visningsporter, for eksempel mobilenheter. |
| Konfigurasjon av medium visningsport  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%** | Denne egenskapen definerer oppsettet for medium visningsporter, for eksempel nettbrett. |
| Konfigurasjon av stor visningsport   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** eller **67%/16%/16%** | Denne egenskapen definerer oppsettet for store visningsporter, for eksempel datamaskiner. |

## <a name="add-a-container-module-to-a-page"></a>Legge til en containermodul på en side

Hvis du vil legge til en containerspillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **containermal**. 
1. Legg til en **Standardside**-modul i **Meldingstekst**-sporet.
1. Fullfør redigeringen av malen, og publiser den.
1. Bruk containermalen du nettopp opprettet, for å opprette en side som heter **containerside**.
1. I **Hoved**-sporet på den nye siden legger du til en containermodul.
1. I egenskapsruten for containermodulen settes **Antall kolonner**-egenskapen til **1** og **Bredde**-egenskapen til **Fyll container**.
1. Legg til en innholdsblokkmodul i containermodulen.
1. I egenskapsruten for innholdsblokkmodulen konfigurerer du overskriften, bildet og oppsettet.
1. Lagre og forhåndsvis siden. Du skal se én funksjonsmodul som passer innenfor bredden til containermodulen.
1. I egenskapsruten for containermodulen endrer du verdien til egenskapen **Antall kolonner** til **3**.
1. Legg til to innholdsblokkmoduler til i containermodulen.
1. Lagre og forhåndsvis siden. Nå skal du se tre innholdsblokkmoduler som vises side ved side.
1. Når du har fått oppsettet du vil bruke, fullfører du redigeringen av siden og publiserer den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Karusellmodul](add-carousel.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
