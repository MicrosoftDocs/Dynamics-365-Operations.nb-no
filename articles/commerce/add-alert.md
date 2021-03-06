---
title: Kampanjebannermodul
description: Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796252"
---
# <a name="promo-banner-module"></a>Promobannermodul

[!include [banner](includes/banner.md)]

Dette emnet dekker kampanjebannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Kampanjebannermoduler brukes til å vise meldinger med innebygd informasjon på en side. De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde. 

Kampanjebannermoduler støtter en tekstmelding og en kobling. Hvis det legges til flere meldinger i en kampanjebannermodul, blir den en roterende karusellbanner som lar kundene gå gjennom alle meldingene. 

Kampanjebannermoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Eksempler på bruk av kampanjebannere i e-handel

Kampanjebannere kan brukes i områdehodet til å vise kampanjer eller meldinger på hele området, som i følgende eksempler.

"Årlige salg avsluttes om 10 dager"

"Gjør store besparelse på skolestartsalget. Handle nå. "

"Nyttårssalget er her!" 

Bildet nedenfor viser et eksempel på en kampanjebanner.

![Eksempel på en kampanjebannermodul](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Egenskaper for kampanjebannermodul

| Egenskapsnavn             | Verdi                              | beskrivelse |
|---------------------------|------------------------------------|-------------|
| Bannermeldinger           | Tekst og koblinger                     | En matrise med tekst og koblinger. |
| Automatisk avspilling                  | **Sann** eller **Usann**              | En verdi som angir om meldinger gås gjennom automatisk hvis flere meldinger er konfigurert. |
| Intervall for lysbildeovergang | Et tall i millisekunder (ms)      | Intervallet som brukes til å bla gjennom meldinger. |
| Tillat forkastelse             | **Sann** eller **Usann**              | Hvis verdien settes til **Sann**, kan kundene forkaste varselet. |
| Vis karusellflipper     | **Sann** eller **Usann**              | En verdi som angir om karusellflipperne skal vises, slik at kunder manuelt kan gå gjennom flere bannerelementer. |
| Tekstjustering            | **Høyre**, **Venstre** eller **Midtstilt** | Tekstjusteringen i kampanjebannermodulen. |
| Sammenkobling                      | En URL                              | URL-adresse for valgfri kobling. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Legge til en kampanjebannermodul på en side 

Hvis du vil legge til en kampanjebannermodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Kampanjebannermal**, og velger deretter **OK**.
1. Under **Sideoppsett** legger du til en **Standardside**-modul i **Meldingstekst**-sporet. 
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den. 
1. Bruk malen du nettopp opprettet, for å opprette en side som heter **Kampanjebannerside**. 
1. I **Hoved**-sporet på den nye siden legger du til en containermodul. 
1. I ruten til høyre setter du **Bredde**-verdien til **Fyll container**.
1. Under **Sideoppsett** legger du til en kampanjebannermodul i containermodulen.
1. Legg til en eller flere bannermeldinger i innstillingene for bannermodulen. Hver melding kan inneholde tekst sammen med en kobling. Du kan redigere de andre egenskapene hvis du vil tilpasse modulen ytterligere.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Øverst på siden vil du se et varsel som angir teksten du la til.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

> [!NOTE]
> Et kampanjebanner brukes vanligvis i sporet for sideoverskrift eller et spor for underoverskrift.


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Karusellmodul](add-carousel.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Innholdsblokkmodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]