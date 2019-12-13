---
title: Varselmodul
description: Dette emnet dekker varselmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785358"
---
# <a name="alert-module"></a>Varselmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker varselmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En varselmodul brukes til å vise meldinger med innebygd informasjon på en side. Varselmoduler støtter en tekstmelding og en kobling. De kan brukes til å vise kampanjer på hele området som vises på alle sider av et e-handelsområde. 

Varselmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Eksempler på varselmoduler i e-handel

Varselmoduler kan brukes på områdehodet for å angi kampanjer eller meldinger på hele området. Her er noen eksempler:

"Årlige salg avsluttes om 10 dager"

"Gjør store besparelse på skolestartsalget. Handle nå. "

## <a name="alert-module-properties"></a>Egenskaper for varselmodul

| Egenskapsnavn  | Verdi                              | Beskrivelse |
|----------------|------------------------------------|-------------|
| Tekst           | Tekst                               | Tekstmeldingen som vises i varselmodulen. |
| Tekstjustering | **Høyre**, **Venstre** eller **Midtstilt** | En verdi som definerer hvordan tekst justeres i varselmodulen. |
| Forkast varsel  | **Sann** eller **Usann**              | Hvis verdien settes til **Sann**, kan kunden forkaste varselet. |
| Sammenkobling           | URL-adresse                                | URL-adresse for valgfri kobling. |

## <a name="add-an-alert-module-to-a-page"></a>Legg til en varselmodul på en side 

Hvis du vil legge til en varselmodul på en side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **varselmal**.
1. I **Hoved**-sporet på standardsiden legger du til en varselmodul.
1. Sjekk inn malen, og publiser den. 
1. Bruk varselmalen du nettopp opprettet, for å opprette en side som heter **varselside**. 
1. I **Hoved**-sporet på den nye siden legger du til en varselmodul.
1. Skriv inn varselteksten i innstillingene for varselmodulen. Du kan redigere de andre egenskapene hvis du vil tilpasse varselmodulen ytterligere.
1. Lagre og forhåndsvis siden. Øverst på siden vil du se et varsel som inneholder teksten du la til.
1. Sjekk inn siden, og publiser den. 

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Funksjonsmodul](add-feature-module.md)

[Hovedbannermodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)
