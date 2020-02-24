---
title: Tekstblokkmodul
description: Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025603"
---
# <a name="text-block-module"></a>Tekstblokkmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker tekstblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En tekstblokkmodul er en modul som brukes til å legge til tekstinnhold. Dette innholdet kan være informasjon eller kampanje.

Tekstblokkmoduler drives av data fra et innholdsbehandlingssystem (CMS) og kan plasseres på en hvilken som helst side. De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Eksempler på tekstblokkmoduler i e-handel

Tekstblokkmoduler kan brukes på følgende måter:

* For å vise produktfunksjoner på en produktdetaljside.
* Til informasjonsformål på en hvilken som helst side. De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.
* Legge til egendefinerte meldinger på en produktdetaljside. (for eksempel "Gratis levering ved bestilling over 500 kroner").
* For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").

## <a name="text-block-module-properties"></a>Egenskaper for tekstblokkmodul

| Egenskapsnavn     | Value                                            | Beskrivelse |
|-------------------|--------------------------------------------------|-------------|
| Rik tekst         | Rik tekst                                        | Avsnittstekst. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst. |
| Egendefinert klassenavn | Et CSS-klassenavn (Cascading Style Sheets)        | Navnet på en egendefinert CSS-klasse som en utvikler tilbyr for å formatere denne modulen. Klassenavnet bør defineres i temapakken. |
| Skriftstørrelse         | **Liten**, **middels**, **stor** eller **ekstra stor** | Skriftstørrelse for innholdet. |

## <a name="add-a-text-block-module-to-a-page"></a>Legge til en tekstblokkmodul på en side

Hvis du vil legge til en tekstblokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **Innholdsmal**. 
1. Legg til en **Standardside**-modul i **Meldingstekst**-sporet.
1. Fullfør redigeringen av malen, og publiser den.
1. Bruk innholdsmalen du nettopp opprettet, for å opprette en side som heter **Innholdsside**.
1. I **Hoved**-sporet på den nye siden legger du til en containermodul.
1. I egenskapsruten for containermodulen setter du **Bredde**-egenskapen til **Fyll container**.
1. Legg til en tekstblokkmodul i containermodulen. 
1. I egenskapsruten for tekstblokkmodulen legger du til tekst i feltet **Rik tekst**.
1. Fullfør redigeringen av siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Kampanjebannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsblokkmodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)

