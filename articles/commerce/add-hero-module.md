---
title: Hovedbannermodul
description: Dette emnet dekker hovedbannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785402"
---
# <a name="hero-module"></a>Hovedbannermodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker hovedbannermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En hovedbannermodul brukes til å markedsføre produkter eller kampanjer ved hjelp av en kombinasjon av bilder og tekst. En forhandler kan for eksempel legge til en hovedbannermodul på startsiden for et område for e-handel for å fremme et nytt produkt og tiltrekke oppmerksomheten til kundene.

En hovedbannermodul styres av data fra CMS (Content Management System). Det er en frittstående modul som ikke er avhengig av andre moduler på siden. En hovedbannermodul kan være plassert på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, salg eller funksjoner).

## <a name="examples-of-hero-module-in-e-commerce"></a>Eksempler på hovedbannermodul i e-handel

- En hovedbannermodul kan brukes på startsiden for et e-handelsområde for å utheve kampanjer og nye produkter.
- En hovedbannermodul kan brukes på en produktdetaljside for å vise produktinformasjon.
- Flere hovedbannermoduler kan plasseres i en karusellmodul for å utheve flere produkter eller kampanjer.

## <a name="hero-module-properties"></a>Egenskaper for hovedbannermodul

| Egenskapsnavn  | Verdier | Beskrivelse |
|----------------|--------|-------------|
| Bilde          | Bildefil | Et bilde kan brukes til å vise et produkt eller en kampanje. Et bilde kan lastes opp til bildegalleriet, eller det kan brukes et eksisterende bilde. |
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Alle hovedbannermoduler kan ha en overskrift. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Avsnitt      | Avsnittstekst | Hovedbannermoduler støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling           | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori** | Hovedbannermoduler støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |
| Tekstplassering | **Øverst til venstre**, **Øverst til høyre**, **Øverst i midten**, **Nederst til venstre**, **Nederst til høyre**, **Nederst i midten**, **Midtstilt til venstre**, **Midtstilt til høyre** eller **Midtstilt i midten** | Denne egenskapen angir plasseringen av bildet i forhold til teksten. Hvis for eksempel **Høyre** er valgt, vises bildet til høyre for teksten. |
| Teksttema     | **Lys** eller **Mørk** | Du kan definere et fargevalg for teksten basert på bakgrunnsbildet. Hvis bildet for eksempel har en mørk bakgrunn, kan du bruke et lyst tema for å få teksten til å være mer synlig, og for å imøtekomme fargekontrastforhold for tilgjengelighetsformål. |
| Gradering       | **Sann** eller **Usann** | En gradering kan brukes på bildet for å imøtekomme fargekontrastforhold for tilgjengelighetsformål. |

## <a name="add-a-hero-module-to-a-new-page"></a>Legge til en hovedbannermodul på en ny side

Hvis du vil legge til en hovedbannermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og opprett en sidemal kalt **hovedbannermal**.
1. I **Hoved**-sporet på standardsiden legger du til en hovedbannermodul.
1. Sjekk inn malen, og publiser den.
1. Bruk hovedbannermalen du nettopp opprettet, for å opprette en side som heter **hovedbannerside**.
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** under **Velg moduler** velger du hovedbannermodulen, og deretter velger du **OK**.
1. I disposisjonstreet til venstre velger du hovedbannermodulen.
1. Velg **Legg til et bilde** i egenskapsruten til høyre. Velg enten et eksisterende bilde, eller last opp et nytt bilde.
1. Velg **Overskrift**.
1. I dialogboksen **Overskrift** legger du til overskiftsteksten, velger overskiftsnivået og velger **OK**.
1. Under **Rik tekst** legger du til tekst etter behov.
1. Velg **Legg til handlingskobling**.
1. I dialogboksen **Handlingskobling** legger du til koblingstekst, en URL-adresse for kobling og en ARIA-etikett for koblingen, og deretter velger du **OK**.
1. Lagre siden, og forhåndsvis endringene.
1. Sjekk inn siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Varselmodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Innholdsrik blokk-modul](add-content-rich-block.md)

[Modul for innholdsplassering](add-content-placement-modules.md)

[Funksjonsmodul](add-feature-module.md)

[Videospillermodul](add-video-player.md)
