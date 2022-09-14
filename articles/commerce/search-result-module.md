---
title: Modul for søkeresultater
description: Denne artikkelen dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405300"
---
# <a name="search-results-module"></a>Modul for søkeresultater

[!include [banner](includes/banner.md)]

Denne artikkelen dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

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

Følg denne fremgangsmåten for å legge til søkeresultatmodulen på en kategorisiden i områdebyggeren.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal** angir du navnet på **Søkeresultater**, og velg deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg moduler** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. I **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (...), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søkebane**-modulen, og deretter velger du **OK**.
1. Skriv inn verdien **1** for **Minimum antall forekomster** i egenskapsruten **Brødsmule**.
1. I **Beholder**-sporet velger du ellipsen (…), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søkeresultater**-modulen, og deretter velger du **OK**.
1. I ruten for egenskaper i **Søkeresultater** angir du verdien **1** for **Minimum antall forekomster**, og deretter angir du andre nødvendige egenskaper for søkeresultatmodulen. Ved å angi disse egenskapene i malen, sikrer du at alle tilpasninger til en bestemt kategoriside automatisk inneholder disse innstillingene.
1. Velg **Fullfør redigering**, og velg deretter **Publiser** for å publisere malen.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du en **Kategoriside**, og velger deretter **Neste**.
1. Under **Velg en mal** velger du **Søkeresultater**-malen du opprettet, og velg deretter **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du har behov for å redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="inventory-aware-search-results-module"></a>Modul for beholdningsfølsomme søkeresultater

Modulen for søkeresultater kan konfigureres til å inneholde lagerdata og gir følgende erfaringer:

- Vis etiketter på lagernivå sammen med produkter.
- Skjul produkter ikke på lager fra produktlisten.
- Vis produkter som ikke er på lager, nederst i produktlisten.
- Støtt lagerbasert produktfiltrering.

Hvis du vil aktivere disse funksjonene, må du først aktivere funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme** og deretter konfigurere noen innstillinger som kreves i Commerce headquarters. Hvis du vil ha mer informasjon, kan du se [Beholdningsfølsom produktoversikt](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Hurtigvisningsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
