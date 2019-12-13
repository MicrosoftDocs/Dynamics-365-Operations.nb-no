---
title: Ordrebekreftelsesmodul
description: Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698332"
---
# <a name="order-confirmation-module"></a>Ordrebekreftelsesmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker ordrebekreftelsesmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En ordrebekreftelsesmodul brukes til å vise en bekreftelsesmelding på en ordrebekreftelsesside etter at en ordre er plassert. Ordrebekreftelsesmodulen viser ordrebekreftelsesnummeret og kundens e-postadresse som ble angitt ved utsjekking.

Når en ordre blir lagt inn under utsjekking, sendes ordrebekreftelsesnummeret og kundens e-postadresse til ordrebekreftelsessiden som en spørringsstreng i URL-adressen til siden. Ordrebekreftelsesmodulen mottar denne informasjonen og gjengir ordrestatusen på ordrebekreftelsessiden. Ordrebekreftelsesmodulen krever denne sidekonteksten for å angi statusen for ordren.

## <a name="order-confirmation-module-properties"></a>Egenskaper for ordrebekreftelsesmodul

| Egenskapsnavn | Verdier | Beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Ordrebekreftelsesmodulen kan ha en overskrift. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a>Moduler som kan brukes i en modul for ordrebekreftelsesside 

- **Anbefalinger** – Anbefalingsmodulen kan plasseres på ordrebekreftelsessiden for å foreslå andre produkter for kunden.
- **Markedsføring** – Markedsføringsmodulen kan legge til markedsføringsinnhold på ordrebekreftelsessiden.

## <a name="create-an-order-confirmation-page-module"></a>Opprette en modul for ordrebekreftelsesside

1. Opprett en sidemal som heter **ordrebekreftelsesmal**.
1. I **Hoved**-sporet på standardsiden legger du til en ordrebekreftelsesmodul.
1. I ordrebekreftelsesmodulen legger du til en anbefalingsmodul.
1. Lagre og forhåndsvis malen. Ordrebekreftelsesmodulen skal ikke gjengis, fordi den krever konteksten til ordrebekreftelsesnummeret.
1. Sjekk inn malen, og publiser den.
1. Bruk ordrebekreftelsesmalen du nettopp opprettet, til å opprette en side som heter **ordrebekreftelsesside**.
1. Legg til standardsiden i sidedisposisjonen.
1. Legg til et topptekstfragment i **Hode**-sporet.
1. Legg til et bunntekstfragment i **Bunntekst**-sporet.
1. I **Hoved**-sporet legger du til en ordrebekreftelsesmodul.
1. I egenskapsruten i ordrebekreftelsesmodulen legger du til overskriften **Ordrebekreftelse**.
1. Under ordrebekreftelsesmodulen legger du til en anbefalingsmodul og konfigurerer den slik at den bruker innstillingene for **Nye** og **Bestselgere**.
1. Lagre og forhåndsvis siden, sjekk det inn, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
