---
title: Innholdsrik blokkmodul
description: Dette emnet dekker innholdsrike blokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785427"
---
# <a name="content-rich-block-module"></a>Innholdsrik blokkmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker innholdsrike blokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En innholdsrik blokkmodul er en spesialcontainer som én eller flere innholdsrike blokkelementer kan plasseres i. Innholdsrike blokkmoduler brukes til tekstinnhold på en side. Dette innholdet kan enten være informasjon eller kampanje.

Innholdsrike blokkmoduler drives av data fra innholdsbehandlingssystemet (CMS) og kan plasseres på en hvilken som helst side. De er frittstående moduler som ikke er avhengige av sidekontekst eller andre moduler.

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a>Eksempler på innholdsrike blokkmoduler i e-handel

Innholdsrike blokkmoduler kan brukes på følgende måter:

* For å vise produktfunksjoner på en produktdetaljside.
* Til informasjonsformål på en hvilken som helst side. De kan for eksempel forklare fordelene med fordelsprogrammer, beskrive forsendelses- og returpolicyer, svare på vanlige spørsmål eller gi "om oss"-innhold.
* Legge til egendefinerte meldinger på en produktdetaljside. (for eksempel "Gratis levering ved bestilling over 500 kroner").
* For fraskrivelser og kontaktdetaljer på sider med produktdetaljer, handlekurvsider, utsjekkingssider og andre sider (for eksempel "Levering og returer er underlagt butikkpolicyer").

## <a name="content-rich-block-module-properties"></a>Egenskaper for innholdsrik blokkmodul

| Egenskapsnavn     | Verdi                                 | Egenskap |
|-------------------|---------------------------------------|----------|
| Antall kolonner | Et tall fra **1** til **4**     | Antall kolonner i den innholdsrike blokken. Det kan være opptil fire kolonner. |
| Bredde             | **Fyll container** eller **Fyll skjerm** | Hvis verdien er satt til **Fyll container**, er elementene i containeren begrenset til bredden på containeren. Hvis verdien er satt til **Fyll skjerm**, er ikke elementene begrenset til containerbredden, men de kan gå i fullskjermmodus. Du kan endre verdien for å oppnå det ønskede oppsettet. |

## <a name="content-rich-block-item-module-properties"></a>Egenskaper for innholdsrik blokkelementmodul

| Egenskapsnavn | Verdi          | Beskrivelse |
|---------------|----------------|-------------|
| Avsnitt     | Avsnittstekst | Teksten som følger med alle innholdsrike blokkelementer. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst. |

## <a name="add-a-content-rich-block-module-to-a-page"></a>Legge til en innholdsrik blokkmodul på en side

Hvis du vil legge til en innholdsrik blokkmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en sidemal som heter **Innholdsmal**.
1. I **Hoved**-sporet på standardsiden legger du til en innholdsrik blokkmodul.
1. Sjekk inn malen, og publiser den.
1. Bruk innholdsmalen du nettopp opprettet, for å opprette en side som heter **Innholdsside**.
1. I **Hoved**-sporet på den nye siden legger du til en innholdsrik blokkmodul.
1. I egenskapene til den innholdsrike blokkmodulen angir du antall kolonner til **2**.
1. I den innholdsrike blokkmodulen velger du **Legg til en modul**, og deretter legger til et innholdsrikt blokkelement (for eksempel **element1**).
1. Legg til avsnittstekst i det nye innholdsrike blokkelementet.
1. I den innholdsrike blokkmodulen velger du **Legg til en modul**, og deretter legger til et innholdsrikt blokkelement (for eksempel **element2**).
1. Legg til avsnittstekst i det nye innholdsrike blokkelementet.
1. Lagre siden, og forhåndsvis endringene. Du skal se to riktekstblokker i en visning med to spalter.
1. Sjekk inn siden, og publiser den.

> [!NOTE]
> Hvis du legger til et tredje innholdsrikt blokkelement, blir det stablet under de to elementene som du har lagt til tidligere. Ved å endre antallet kolonner og elementer i containeren, kan du oppnå forskjellige oppsett for tekstinnhold.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Varselmodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Funksjonsmodul](add-feature-module.md)

[Hovedbannermodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)

