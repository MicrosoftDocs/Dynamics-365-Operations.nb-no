---
title: Modul for innholdsplassering
description: Dette emnet dekker innholdsplasserings- og innholdsplasseringselementmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785306"
---
# <a name="content-placement-module"></a>Modul for innholdsplassering

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker innholdsplasserings- og innholdsplasseringselementmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En innholdsplasseringsmodul er en spesiell container som andre moduler kan plasseres innenfor i et bestemt oppsett. Innholdsplasseringsmoduler støtter følgende typer moduler som underordnede moduler: innholdsplasseringselement og velkomstelement, ønskelisteelement og profilelement for konto.

Innholdsplasseringsmoduler henter data fra de underordnede modulene de støtter. Derfor kan innholdsplasseringsmoduler brukes på ulike måter, avhengig av modulene som er lagt til i den.

Modulene for innholdsplasseringselementer bruker både bilder og tekst til å vise kampanjer, policyer og produktfunksjoner. En modul for innholdsplasseringselement kan for eksempel brukes på en startside til å vise butikkpolicyer eller forsendelsesinformasjon. Moduler for innholdsplasseringselementer drives av data fra innholdsbehandlingssystemet (CMS) og kan plasseres på en hvilken som helst side. De kan imidlertid bare brukes i en innholdsplasseringsmodul.

## <a name="examples-of-content-placement-modules-in-e-commerce"></a>Eksempler på innholdsplasseringsmoduler i e-handel

* Moduler for innholdsplassering som inneholder moduler for innholdsplasseringselementer, kan brukes på en startside eller markedsføringsside til å vise produktfunksjoner, kampanjer, butikkpolicyer, forsendelsesinformasjon og annen informasjon gjennom både bilder og tekst.
* Moduler for innholdsplassering som inneholder moduler for innholdsplasseringselementer, kan brukes på sider med produktdetaljer for å vise produktfunksjoner.
* Moduler for innholdsplassering som inneholder velkomstelement eller ordreelementmoduler for konto, kan brukes på kontobehandlingssider.

## <a name="content-placement-module-properties"></a>Egenskaper for innholdsplasseringmodul

| Egenskapsnavn | Verdi | Beskrivelse |
|---------------|-------|-------------|
| Bredde         | **Tilpass container** eller **Fyll skjerm** | Hvis verdien er satt til **Tilpass container**, er elementene i innholdsplasseringsmodulen begrenset til bredden på innholdsplasseringsmodulen. Hvis verdien er satt til **Fyll skjerm**, er ikke elementene begrenset til bredden på innholdsplasseringsmodulen, men de kan gå i fullskjermmodus. |

## <a name="content-placement-item-module-properties"></a>Egenskaper for modulen for innholdsplasseringelementer

| Egenskapsnavn | Verdi | Beskrivelse |
|---------------|-------|-------------|
| Overskrift       | Overskriftstekst og overskriftskoder (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Hver modul for innholdsplasseringelement kan ha en overskrift. Egenskapen **Overskrift** støtter overskriftskoder. Som standard brukes **H2**-overskriftskoden, men overskriftskoden kan endres for å imøtekomme tilgjengelighetskrav. |
| Avsnitt     | Avsnittstekst | Moduler for innholdsplasseringelementer støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Bilde         | Bildefil | Et bilde kan tilknyttes teksten. |
| Sammenkobling          | Koble URL-adresse og koblingstekst | Du kan legge til en kobling i teksten for å omadressere brukere til en bestemt side. |
| Flisstørrelse     | Et tall fra **1** til **12** | For hvert innholdsplasseringselement definerer denne egenskapen antallet spor som elementet skal fylle i innholdsplasseringsmodulen. Den maksimale størrelsen til innholdsplasseringsmodulen er 12 spor. Hvis den totale flisstørrelsen for de første *n* elementene i modulen for innholdsplassering overskrider 12 spor, brytes elementene til neste rad. |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a>Legge til en innholdsplasseringsmodul som inneholder en modul for innholdsplasseringselement på en side

Hvis du vil legge til en modul for innholdsplassering som inneholder en modul for innholdsplasseringselement, til en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett en mal som heter **innholdsplasseringsmal**.
1. I **Hoved**-sporet på standardsiden legger du til en innholdsplasseringsmodul.
1. I innholdsplasseringsmodulen legger du til en modul for innholdsplasseringselement.
1. Sjekk inn malen, og publiser den.
1. Bruk innholdsplasseringsmalen du nettopp opprettet, for å opprette en side som heter **Innholdsplasseringsside**.
1. I **Hoved**-sporet på den nye siden legger du til en innholdsplasseringsmodul.
1. I innholdsplasseringsmodulen legger du til en modul for innholdsplasseringselement.
1. I egenskapsruten for modulen for innholdsplasseringelement velger du et bilde, legger til en overskrift, legger til et avsnitt, legger til en kobling, angir URL-adressen for koblingen og setter flisstørrelsen til **6**.
1. Gjenta trinn 7 og 8 for å legge til en annen modul for innholdsplasseringselement med samme flisstørrelse.
1. Lagre og forhåndsvis siden. Du skal se to innholdsplasseringselementer som vises side ved side. Du kan justere egenskapen **Flisstørrelse** for hver innholdsplasseringselementmodul eller legge til flere moduler for å oppnå ønsket oppsett.
1. Sjekk inn siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Varselmodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Funksjonsmodul](add-feature-module.md)

[Hovedbannermodul](add-hero-module.md)

[Videospillermodul](add-video-player.md)
