---
title: Ordredetaljermodulen
description: Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026023"
---
# <a name="order-details-module"></a>Ordredetaljermodulen


[!include [banner](includes/banner.md)]

Dette emnet dekker ordredetaljmoduler og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Ordredetaljmodulen brukes til å vise ordrebekreftelsesdetaljer etter at en ordre er lagt inn. Den viser ID-en for ordrebekreftelse, ordrekontaktinformasjon og andre ordredetaljer, for eksempel varene som ble kjøpt, betalingsinformasjon og forsendelsesmetoden.

## <a name="order-confirmation-module-properties"></a>Egenskaper for ordrebekreftelsesmodul

| Egenskapsnavn  | Verdier | Beskrivelse |
|----------------|--------|-------------|
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekreftelsesmodulen kan ha en overskrift. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Kontaktnummer | Text | Et kontaktnummer kan angis for spørsmål som er knyttet til ordren. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduler som kan brukes på en ordredetaljside

Når du oppretter en ordredetaljside, kan du legge til andre relevante moduler i tillegg til ordredetaljmodulen. Her er noen eksempler:

- **Anbefalingsmodulen** – Anbefalingsmodulen kan legges til på ordredetaljsiden for å foreslå andre produkter for kunden.
- **Markedsføringsmoduler** – Enhver markedsføringsmodul kan legges til på ordredetaljsiden for å vise markedsføringsinnhold.

## <a name="create-an-order-details-page-module"></a>Opprette en modul for ordredetaljside

1. Opprett en sidemal som heter **Ordredetaljer**.
1. I **Hoved**-sporet på standardsiden legger du til en ordredetaljmodul.
1. I ordredetaljmodulen legger du til en anbefalingsmodul.
1. Lagre og forhåndsvis malen. Ordredetaljmodulen blir ikke gjengitt, fordi den krever konteksten til ordrebekreftelsesnummeret.
1. Fullfør redigeringen av malen, og publiser den.
1. Bruk ordredetaljmalen du nettopp opprettet, til å opprette en side som heter **ordredetaljside**.
1. Legg til standardsiden i sidedisposisjonen.
1. Legg til et topptekstfragment i **Hode**-sporet.
1. Legg til et bunntekstfragment i **Bunntekst**-sporet.
1. I **Hoved**-sporet legger du til en ordredetaljmodul.
1. I egenskapsruten for ordredetaljmodulen legger du til overskriften **Ordredetaljer**.
1. Under ordredetaljmodulen legger du til en anbefalingsmodul og konfigurerer den slik at den bruker innstillingene for **Nye** og **Bestselgere**.
1. Lagre og forhåndsvis siden.
1. Fullfør redigeringen av siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
