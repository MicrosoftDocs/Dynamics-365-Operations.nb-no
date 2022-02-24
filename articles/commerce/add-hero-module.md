---
title: Innholdsblokkmodul
description: Dette emnet dekker innholdsblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 7a8b1c214ba31b7c47cecbe67bef493f5fa450fc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414582"
---
# <a name="content-block-module"></a>Innholdsblokkmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker innholdsblokkmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En innholdsblokkmodul brukes til å markedsføre produkter eller kampanjer ved hjelp av en kombinasjon av bilder og tekst. En forhandler kan for eksempel legge til en innholdsblokkmodul på startsiden for et område for e-handel for å fremme et nytt produkt og tiltrekke oppmerksomheten til kundene.

En innholdsblokkmodul styres av data fra CMS (Content Management System). Det er en frittstående modul som ikke er avhengig av andre moduler på siden. En innholdsblokkmodul kan være plassert på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, salg eller funksjoner).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Eksempler på innholdsblokkmodul i e-handel

- En innholdsblokkmodul kan brukes på startsiden for et e-handelsområde for å utheve kampanjer og nye produkter.
- En innholdsblokkmodul kan brukes på en produktdetaljside for å vise produktinformasjon.
- Flere innholdsblokkmoduler kan plasseres i en karusellmodul for å utheve flere produkter eller kampanjer.

## <a name="content-block-modules-and-themes"></a>Innholdsblokkmoduler og temaer

Innholdsblokkmoduler kan støtte ulike oppsett og stiler basert på et tema. For eksempel støtter Fabrikam-temaet tre oppsettsvariasjoner av en innholdsblokkmodul: hovedbanner, funksjon og flis. Hovedbanneroppsettet viser et bilde på bakgrunnen med tekstoverlegg. Funksjonsoppsettet viser et bilde og tekst side ved side. Flisoppsettet tillater flere innholdsblokker i flisformat.

I tillegg kan temaet vise forskjellige egenskaper for hvert oppsett. En temautvikler kan bygge flere oppsett med flere stiler ved hjelp av innholdsblokkmodulen.

Bildet nedenfor viser et eksempel på en innholdsblokkmodul med et hovedbanneroppsett.

![Eksempel på en hovedbannermodul](./media/Hero.PNG)

Bildet nedenfor viser et eksempel på en innholdsblokkmodul med et funksjonsoppsett.

![Eksempler på funksjonsmoduler](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Egenskaper for innholdsblokkmodul

| Egenskapsnavn  | Verdier | Beskrivelse |
|----------------|--------|-------------|
| Bilde          | Bildefil | Et bilde kan brukes til å vise et produkt eller en kampanje. Et bilde kan lastes opp til bildegalleriet, eller det kan brukes et eksisterende bilde. |
| Overskrift        | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Alle hovedbannermoduler kan ha en overskrift. Som standard brukes **H2**-overskriftskoden for overskriften. Koden kan imidlertid endres for å oppfylle tilgjengelighetskravene. |
| Avsnitt      | Avsnittstekst | Hovedbannermoduler støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel fet, understreket og kursivert tekst, og hyperkoblinger. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling           | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori** | Hovedbannermoduler støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Egenskaper for innholdsblokkmodul vist med Fabrikam-temaet 

| Egenskapsnavn  | Verdier | Beskrivelse |
|----------------|--------|-------------|
| Tekstplassering | **Venstre**, **Høyre**, **Midtstilt** | Denne egenskapen angir plasseringen av teksten i bildet. Den gjelder bare for hovedbanneroppsettet. |
| Teksttema     | **Lys** eller **Mørk** | Du kan definere et fargevalg for teksten basert på bakgrunnsbildet. Hvis bildet for eksempel har en mørk bakgrunn, kan du bruke et lyst tema for å få teksten til å være mer synlig, og for å imøtekomme fargekontrastforhold for tilgjengelighetsformål. Den gjelder bare for hovedbanneroppsettet.|
| Bildeplassering       | **Venstre**, **Høyre** | Denne egenskapen angir om bildet skal være til venstre eller høyre for teksten. Den gjelder bare for funksjonsoppsettet.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Legge til en innholdsblokkmodul på en ny side

Hvis du vil legge til en hovedbannermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og opprett en sidemal kalt **innholdsblokkmal**.
1. I **Hoved**-sporet på standardsiden legger du til en hovedbannermodul.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Bruk hovedbannermalen du nettopp opprettet, for å opprette en side som heter **innholdsblokkside**.
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** under **Velg moduler** velger du hovedbannermodulen, og deretter velger du **OK**.
1. I disposisjonstreet til venstre velger du innholdsblokkmodulen.
1. Velg **Legg til et bilde** i egenskapsruten til høyre. Velg enten et eksisterende bilde, eller last opp et nytt bilde.
1. Velg **Overskrift**.
1. I dialogboksen **Overskrift** legger du til overskiftsteksten, velger overskiftsnivået og velger **OK**.
1. Under **Rik tekst** legger du til tekst etter behov.
1. Velg **Legg til kobling**.
1. I dialogboksen **Kobling** legger du til koblingstekst, en URL-adresse for kobling og en ARIA-etikett for koblingen, og deretter velger du **OK**.
1. Velg **Hovedbanner**-oppsettet.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Promobannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Videospillermodul](add-video-player.md)
