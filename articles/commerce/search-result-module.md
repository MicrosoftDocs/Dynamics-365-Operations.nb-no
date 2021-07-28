---
title: Søkeresultatmodul
description: Dette emnet dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 04ffa8e56b72727c079db07f38bfae675ae2abb1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344962"
---
# <a name="search-results-module"></a>Modul for søkeresultater

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Modulen for søkeresultater returnerer produktsøkeresultater og en liste over gjeldende presiseringer for produktene. Søkeresultatmoduler på Dynamics 365 Commerce-områder kan brukes til å gjengi sider for følgende scenarier:

- Søkeresultater som startes ved hjelp av et brukersøk
- Søkeresultater som viser et bestemt sett med produkter, for eksempel "Kjøp lignende utseende"
- Liste over produkter som tilhører en kategori

Hvis du vil ha mer informasjon om kategori- og søkeresultatsider, kan du se [Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md).

Følgende illustrasjon viser et eksempel på en søkeresultatside for en kategori på Fabrikam-området.

![Eksempel på en søkeresultatside på Fabrikam-området.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Egenskaper for søkeresultatmodul

I tabellen nedenfor finner du en oversikt over egenskaper for søkeresultatmoduler sammen med verdier og beskrivelser.

| Egenskap | Verdier | beskrivelse |
|----------|--------|-------------|
| Varer per side | Heltall | Antallet elementer som skal vises på hver side. |
| Tillat tilbake på PDP | **Sann** eller **Usann** | Hvis denne egenskapen settes til **Sann**, vil brødsmulenavigasjonen på produktdetaljsiden (PDP) som åpnes, vise koblingen "Tilbake til resultater" når en bruker velger et produkt på søkeresultatsiden. |
| Utvid presiseringer | **Alle**, **1**, **2**, **3** eller **4** | Antallet toppresiseringer som skal utvides når en side lastes inn. Hvis for eksempel denne egenskapen er satt til **3**, utvides de første tre presiseringene på siden. |
| Skjul visning av kategorihierarki | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vil kategorihierarkivisningen på siden være skjult. Denne egenskapen bør settes til **Sann** hvis du bruker [brødsmulemodulen](add-breadcrumb.md) for å vise kategorihierarkiet.|
| Inkluder produktattributter i søkeresultater | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, blir attributter returnert for produktene i søkeresultatene. Selv om disse attributtene kan vises på et Commerce-område, kreves det en utvidelse.|
| Vis tilknytningspriser | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vises tilknytningspriser for produkter i søkeresultatene når en pålogget bruker blar gjennom siden. |
| Oppdatere presiseringspanel | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, oppdateres presiseringspanelet når presiseringer velges. I denne modusen vil noen flervalgspresiseringer fungere som enkeltvalgpresiseringer når presiseringspanelet oppdateres. |

> [!IMPORTANT]
> I Commerce-versjon 10.0.16 og senere kan konfigurasjonen **Vis tilknytningspriser** brukes til å vise tilknytningspriser på siden.
>
> I Commerce versjon 10.0.20-versjonen og senere kan du bruke **Oppdatere presiseringspanel**-konfigurasjonen til å oppdatere presiseringspanelet under presiseringsvalg.

## <a name="supported-modules"></a>Støttede moduler

Søkeresultatmodulen støtter [hurtigvisningsmodulen](quick-view-module.md), som gjør det mulig for brukere å vise produktinformasjon og legge til varer i handlekurven fra søkeresultatsiden.

## <a name="add-a-search-results-module-to-a-category-page"></a>Legge til en søkeresultatmodul på en kategoriside

For å legge til en søkeresultatmodul på en kategoriside, følg disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal** angir du navnet på **Søkeresultater**, og velg deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. I **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (...), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.
1. Skriv inn verdien **1** for **Minimum antall forekomster** i egenskapsruten **Brødsmule**.
1. I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Søkeresultater**-modulen, og deretter velger du **OK**.
1. I ruten for egenskaper i **Søkeresultater** angir du verdien **1** for **Minimum antall forekomster**, og deretter angir du andre nødvendige egenskaper for søkeresultatmodulen. Ved å angi disse egenskapene i malen, sikrer du at alle tilpasninger til en bestemt kategoriside automatisk inneholder disse innstillingene.
1. Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Velg en mal** velger du malen **Søkeresultater** som du opprettet, angir **Kategoriside** for **Sidenavn**, og deretter velger du **OK**. Siden alle verdiene er angitt i malen, er siden klar til å publiseres.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Hurtigvisningsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
