---
title: Flislistemodul
description: Dette emnet dekker flislistemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.openlocfilehash: 10bf7139ba89f5089d288e78fab9e3d63249aac9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638910"
---
# <a name="tile-list-module"></a>Flislistemodul

[!include [banner](includes/banner.md)]

Dette emnet dekker flislistemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

En flislistemodul er en samling fliser i en karusell. Den brukes til å markedsførte produktkategorier eller produktmerker gjennom bilder og tekst. En forhandler kan for eksempel legge til en flislistemodul på hjemmesiden til et e-handelsområde for å fremme alle toppsalgskategoriene.

Flislistemodulen styres av data fra CMS (Content Management System). Den avhenger ikke av andre moduler eller data fra Commerce Headquarters. Flislistemodulen kan legges til på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, kategorier eller merker).

Illustrasjonen nedenfor viser et eksempel på en flislistemodul og flismoduler på Adventure Works-hjemmesiden.

![Eksempel på en flislistemodul og flismoduler på Adventure Works-hjemmesiden](./media/Tile_list.PNG)

> [!IMPORTANT]
> Flislistemodulen er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.
> Flislistemodulen presenteres i Adventure Works-emnet.

## <a name="tile-list-modules-and-themes"></a>Flislistemoduler og -temaer

Flislistemodulen kan støtte ulike oppsett og stiler basert på et tema. I Adventure Works-emnet viser f.eks. flisene en animasjonseffekt når områdebrukere holder pekeren over dem. Hvert tema kan inneholde flere egenskaper for flislisten og flismodulene. Temautviklere kan også bygge flere oppsett for flislisten og flismodulene.

## <a name="tile-list-module-properties"></a>Flislistemodul-egenskaper

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode | Tekstoverskrift for flislistemodulen. |

## <a name="tile-module-properties"></a>Egenskaper for flismodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Bilde         | Bildefil | Et bilde kan brukes til å vise et produkt eller en kategori. Bildet kan lastes opp til mediebiblioteket i Commerce-områdebyggeren, eller du kan bruke et eksisterende bilde. |
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard brukes **H2**-overskriftskoden, men koden kan endres for å imøtekomme tilgjengelighetskrav. |
| Avsnitt     | Avsnittstekst | Modulen støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel hyperkoblinger og fet, understreket og kursivert tekst. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling          | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori** | Moduler støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |
| Fliskobling     | Koblingstekst, URL for kobling, ARIA-etikett og **Åpne kobling i ny kategori**-velger | Denne egenskapen brukes til å definere en "handlingsoppfordring"-koblinhg. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane.|
| Ikon          | Bilde | I tillegg til et produkt- eller kategoribilde, kan du legge til et ikonsymbol. Ikonsymbolet vises over produktet eller kategoribildet. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Legge til en flislistemodul på en ny side

Hvis du vil legge til en flislistemodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og åpne markedsføringsmalen for områdets hjemmeside (eller opprett en ny markedsføringsmal).
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Flisliste**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne områdets hjemmeside (eller opprett en ny hjemmeside ved hjelp av markedsføringsmalen).
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Flisliste**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for flislistemodulen legger du til en overskrift.
1. Velg ellipseknappen (**...**) for **Flisliste**-sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Flisliste**-modulen, og deretter velger du **OK**.
1. I egenskapsruten til flismodulen legger du til et bilde, en overskrift og et ikonsymbolbilde.
1. Legg til og konfigurer flere flismoduler etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
