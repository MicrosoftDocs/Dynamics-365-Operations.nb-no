---
title: Interaktiv funksjonsmodul
description: Dette emnet dekker interaktive funksjonsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b1d00b9173fd1d5faee71e0fec6c9d1546989e41
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638860"
---
# <a name="interactive-feature-module"></a>Interaktiv funksjonsmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker interaktive funksjonsmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Interaktive funksjonsmoduler er mønskelignende moduler som kan brukes til å markedsføre flere produktkategorier eller produktmerker ved hjelp av en kombinasjon av bilder og tekst. En forhandler kan for eksempel legge til en interaktiv funksjonsmodul på hjemmesiden til et e-handelsområde for å fremme toppsalgskategoriene. Den interaktive funksjonsmodulen ligner på flislistemodulen, men den har et annet oppsett og forskjellig samhandlingsfunksjonalitet.

Hver interaktive funksjonsmodul er en samling med interaktive moduler for funksjonselement. Hver funksjonselementmodul styres av data fra CMS (Content Management System). Den avhenger ikke av andre moduler eller data fra Commerce Headquarters. Den interaktive funksjonsmodulen kan legges til på en hvilken som helst områdeside der en forhandler vil markedsføre eller fremme noe (for eksempel produkter, kategorier eller merker).

> [!IMPORTANT]
> - Den interaktive funksjonsmodulen er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.
> - Den interaktive funksjonsmodulen presenteres i Adventure Works-emnet.

Illustrasjonen nedenfor viser et eksempel på en interaktive funksjonsmodulen på Adventure Works-hjemmesiden.

![Eksempel på en interaktiv funksjonsmodul på Adventure Works-hjemmesiden](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktiv funksjonsmodul og temaer

Den interaktive funksjonsmodulen kan støtte ulike oppsett og stiler basert på et tema. I for eksempel Adventure Works-emnet har den interaktive funksjonsmodulen et tokolonners oppsett som viser animasjonseffekter når en områdebruker holder pekeren over hvert element. Den interaktive funksjonsmodulen er optimert for et likt antall bilder som er ordnet i et oppsett med to kolonner.

## <a name="interactive-feature-module-properties"></a>Egenskaper for interaktiv funksjonsmodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Tekstoverskrift for den interaktive funksjonsmodulen. |

## <a name="interactive-feature-item-module-properties"></a>Egenskaper for interaktiv funksjonselementmodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Bilde         | Bildefil | Bilde som representerer et produkt eller en kategori. Bildet kan lastes opp til mediebiblioteket i Commerce-områdebyggeren, eller du kan bruke et eksisterende bilde. |
| Overskrift       | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard brukes **H2**-overskriftskoden, men koden kan endres for å imøtekomme tilgjengelighetskrav. |
| Avsnitt     | Avsnittstekst | Modulen støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel hyperkoblinger og fet, understreket og kursivert tekst. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling          | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**-velger | Modulen støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Legge til en interaktiv funksjonsmodul på en ny side

Hvis du vil legge til en interaktiv funksjonsmodul på en ny side og angi de nødvendige egenskapene i Commerce-områdebyggeren, følger du disse trinnene.

1. Gå til **Maler**, og åpne markedsføringsmalen for områdets hjemmeside (eller opprett en ny markedsføringsmal).
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Interaktiv funksjon**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne områdets hjemmeside (eller opprett en ny hjemmeside ved hjelp av markedsføringsmalen).
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** under **Velg moduler** velger du den **interaktive funksjons**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for den interaktive funksjonsmodulen legger du til en overskrift.
1. Velg ellipseknappen (**...**) i **Interaktiv funksjon**-sporet, og velg deretter **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Interaktiv funksjonselement**-modulen, og deretter velger du **OK**.
1. Legg til et bilde, en overskriftstekst, en avsnittetstekst og en URL i egenskapsruten for den interaktive funksjonselementmodulen.
1. Legg til og konfigurer flere interaktive funksjonselementmoduler etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
