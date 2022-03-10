---
title: Søkeresultatmodul
description: Dette emnet dekker søkeresultatmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
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
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919480"
---
# <a name="search-results-module"></a>Modul for søkeresultater

[!include [banner](includes/banner.md)]


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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Aktivere lagerkjennskap for søkeresultatmodulen

Kunder forventer vanligvis at et e-handelsområde er beholdningsfølsomt gjennom hele leseropplevelsen, slik at de kan bestemme hva de skal gjøre hvis det ikke er noe lager for et produkt. Modulen for søkeresultater kan utvides slik at den inneholder lagerdata og gir følgende erfaringer:

- Vis en lagertilgjengelighetsetikett sammen med produkter.
- Skjul produkter som ikke er på lager.
- Vis produkter som ikke er på lager, nederst i søkeresultatlisten.
    
Hvis du vil aktivere disse erfaringene, må du konfigurere følgende forutsetningsinnstillinger i Commerce Headquarters.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Aktivere funksjonen Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme

> [!NOTE]
> Funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme** er tilgjengelig fra Commerce versjon 10.0.20.

Følg denne fremgangsmåten for å aktivere funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme** i Commerce Headquarters.

1. Gå til **Arbeidsområder \> Funksjonsbehandling**.
1. Søk etter og aktiver funksjonen **Forbedret produktoppdaging for e-handel slik at de er beholdningsfølsomme**.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigurer jobben Fyll ut produktattributter med lagernivå

Jobben **Fyll ut produktattributtene med lagernivå** oppretter et nytt produktattributt for å registrere lagertilgjengelighet, og setter deretter dette attributtet til den siste lagernivåverdien for hvert hovedprodukt. Siden lagertilgjengeligheten for et produkt eller et assortement som selges, endres konstant, anbefaler vi på det sterkeste at du planlegger jobben som en satsvis prosess.

Følg denne fremgangsmåten for å konfigurere jobben **Fyll ut produktattributter med lagernivå** i Commerce Headquarters.

1. Gå til **Retail og Commerce \> IT for Retail og Commerce \> Produkter og beholdning**.
1. Velg **Fyll ut produktattributter med lagernivå**.
1. Følg denne fremgangsmåten i dialogboksen **Fyll ut produktattributter med lagernivå**:

    1. Under **Parametere** i feltet **Produktattributt og typenavn** angir du et navn for det dedikerte produktattributtet som vil bli opprettet for å registrere lagertilgjengelighet.
    1. Under **Parametere** i feltet **Lagertilgjengelighet basert på** velger du antallet som lagernivåberegningen skal baseres på (for eksempel **Fysisk tilgjengelig**).
    1. Under **Kjør i bakgrunnen** konfigurerer du jobben til å kjøre i bakgrunnen, og eventuelt slår på alternativet for **Satsvis behandling**. 

> [!NOTE]
> For konsekvent beregning av lagernivå i hele PDPene og produktlistesidene på e-handelsområdet, må du huske på å velge samme antallsalternativ for både **Lagertilgjengelighet basert på**-innstillingen i Commerce Headquarters og **Beholdningsnivå basert på**-innstillingen i Commerce-områdebygger. Hvis du vil ha informasjon om beholdningsinnstillinger i områdebygger, kan du se [Bruk beholdningsinnstillinger](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Konfigurere det nye produktattributtet

Når jobben **Fyll ut produktattributter med lagernivå** er kjørt, må du konfigurere det nyopprettede produktattributtet på e-handelsområdet der du vil aktivere lagerkjennskap for søkeresultatmodulen.

Følg denne fremgangsmåten for å konfigurere det nye produktattributtet i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**, og velg et e-handelsområde.
1. Velg og åpne en tilknyttet attributtgruppe, legg til det nyopprettede produktattributtet, og lukk deretter siden.
1. Velg **Angi attributtmetadata**, velg produktattributtene som nylig er lagt til, og slå deretter på alternativene **Vis attributt i kanal**, **Kan hentes**, **Kan finjusteres** og **Kan spørres**.

> [!NOTE]
> For produkter som vises i søkeresultatmodulen, angis lagernivået på hovedproduktnivået i stedet for på det individuelle variantnivået. Det har bare to mulige verdier: "tilgjengelig" og "ikke på lager". Den faktiske teksten for verdiene hentes fra definisjonen [beholdningsnivåprofil](inventory-buffers-levels.md). Et hovedprodukt betraktes som ikke på lager når alle variantene er ikke på lager. Lagernivået for en variant bestemmes basert på produktets definisjon av beholdningsnivåprofil. 

Når alle de forrige konfigurasjonstrinnene er fullført, vil finjusteringene på søkeresultatsider vise et lagerbasert filter, og søkeresultatmodulen henter lagerdata i bakgrunnen. Deretter kan du konfigurere innstillingen **Beholdningsinnstillinger for produktlistesider** i Commerce-områdebygger for å styre hvordan søkeresultatmodulen viser produkter som ikke er på lager. For mer informasjon, se [Bruke beholdningsinnstillinger](inventory-settings.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Hurtigvisningsmodul](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
