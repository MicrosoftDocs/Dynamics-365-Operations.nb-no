---
title: Komponenter for finansrapport
description: "Denne artikkelen beskriver hvordan komponenter eller byggeblokker i rapportdefinisjoner brukes i finansrapportering. Disse byggeblokkene inkluderer raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner. Artikkelen beskriver hvordan du organiserer og låser byggeblokker og hvordan du arbeider med byggeblokkgrupper."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5c09b1fc061f95cd78e9f18c2bdf846fdbfc7cf1
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Komponenter for finansrapport
<a id="financial-report-components" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan komponenter eller byggeblokker i rapportdefinisjoner brukes i finansrapportering. Disse byggeblokkene inkluderer raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner. Artikkelen beskriver hvordan du organiserer og låser byggeblokker og hvordan du arbeider med byggeblokkgrupper. 

Utformingsfilosofien bak Utforming av finansrapport er å dele informasjonen inn i de minste komponenten eller byggeblokkene, og deretter blande og samsvare komponentene som kreves. Derfor er rapportformateringen atskilt fra dine økonomiske data, og du kan endre utformingen av en rapport uten å endre de økonomiske dataene i Microsoft Dynamics ERP-systemet. Ved å bruke denne fremgangsmåten for byggeblokken, kan du kombinere tekst, beløp og beregninger for å lage rapportene du trenger. Denne fleksibiliteten fremmer kreativiteten ved å gjøre det enkelt for deg å vise operasjoner på forskjellige måter. De individuelle byggeblokkene i en rapportdefinisjon ligner på et tredimensjonalt regneark, men de har flere muligheter. En rapportdefinisjon angir raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon som skal brukes for rapporten. Den inneholder også informasjon om hvor den genererte rapporten skal lagres og hvordan den skal formateres. For bedre gjenbruk og deling kan du opprette en byggeblokkgruppe, som er en samling av eksisterende rapportdefinisjoner, raddefinisjoner, kolonnedefinisjoner, rapporteringstredefinisjoner og dimensjonssett, som er knyttet til et firma.

##  Byggeblokker i en rapport
<a id="building-blocks-of-a-report" class="xliff"></a>
| Byggeblokk            | Beskrivelse                                                                                                                                                                                                                                                                              | For mer informasjon                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Raddefinisjon            | En raddefinisjon definerer de beskrivende linjene (for eksempel lønn eller salg) i en rapport. Den viser i tillegg segmentverdiene eller dimensjonene som inneholder verdiene for hver linjevare, og inneholder radformatering og beregninger.                                                    | [Raddefinisjoner](row-definitions-financial-reporting.md)                       |
| Kolonnedefinisjon         | En kolonnedefinisjon definerer perioden som skal brukes når data trekkes ut fra finansdimensjonene. Den inneholder også kolonneformatering og beregninger.                                                                                                                                 | [Kolonnedefinisjoner](column-definitions-financial-reports.md)         |
| Rapporteringstredefinisjon | En rapporteringtredefinisjon ligner på et organisasjonskart. Den inneholder individuelle rapportenheter som representerer hver boks i diagrammet. Enhetene kan være individuelle avdelinger fra de økonomiske dataene eller overordnet enheter som summerer data fra andre rapporteringsenheter. | [Rapporteringstredefinisjoner](financial-reporting-tree-definitions.md) |
| Rapportdefinisjon         | En rapportdefinisjon bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å bygge en rapport. Den inneholder også flere alternativer og innstillinger som du kan bruke for å tilpasse en rapport.                                                                    | [Rapportdefinisjon](design-financial-report-definitions.md)                  |

Hvis du ikke har erfaring med å utforme rapporter, kan det hende du vil bruke rapportveiviseren for raskt å opprette en rapportdefinisjon som du kan tilpasse senere. Hvis du har erfaring med å utforme rapporter og vil ha større fleksibilitet for rapportutformingen, kan du kombinere nye eller eksisterende byggeblokker for å opprette en ny rapportdefinisjon. Du trenger ikke forstår fullt ut alle de tilgjengelige alternativene for rapportdefinisjon for å lage kvalitetsrapporter. Når du blir vant med å utforme rapporter, kan du utvide rapportdefinisjonene for å dra nytte av mer avanserte funksjoner. Når du har opprettet en grunnleggende rapport, kan du tilpasse rapportdefinisjonen og eventuelle byggeblokker i rapportdefinisjonen.

## Organisere byggeblokkene
<a id="organize-the-building-blocks" class="xliff"></a>
Bruke mapper til å organisere byggeblokkene i Rapportutforming. Alle mappene er spesifikke for typen byggeblokk som de inneholder. Alle mapper som for eksempel inneholder raddefinisjoner, finnes i ruten **Raddefinisjoner** i Rapportutforming.

### Opprette en mappe
<a id="create-a-folder" class="xliff"></a>

1.  I Rapportutforming velger du type byggeblokk å organisere i navigasjonsruten. Hvis du for eksempel vil sortere en raddefinisjon, klikker du **Raddefinisjoner**.
2.  I navigasjonsruten velger du den eksisterende mappen som den nye mappen skal opprettes under, og deretter følger du én av disse trinnene:
    -   Høyreklikk den overordnede mappen, og klikk deretter **Ny mappe**.
    -   Velg den overordnede mappen, klikk **Fil**, og klikk deretter **Ny mappe**..

3.  Når den nye mappen vises, angir du deretter navnet på den nye mappen og trykker Enter.

##  Låse en byggeblokk
<a id="lock-a-building-block" class="xliff"></a>
Du kan opprette et passord for å låse og bidra til å beskytte en byggeblokk. På denne måten kan du legge til et sikkerhetsnivå i en rapportkomponent uten å sikre hele systemet. Et passord kan bidra til å beskytte byggeblokkinformasjon som er viktig for rapporteringsprosessen for månedsavslutning. En bruker i en hvilken som helst rolle kan låse en byggeblokk. Andre brukere har imidlertid alltid skrivebeskyttet tilgang til en låst komponent. Brukere kan åpne, endre og lagre den låste komponenten med et nytt navn. En bruker som har rollen administrator har alltid få tilgang til og kan endre en låst byggeblokk.
1.  Åpne rapportkomponenten som skal låses i Rapportutforming, for eksempel en raddefinisjon, kolonnedefinisjon, rapportdefinisjon eller rapporteringstredefinisjon.
2.  På **Verktøy**-menyen klikker du **Aktiver/deaktiver beskyttelse** > . Du kan også klikke ikonet for **Aktiver/deaktiver beskyttelse** (låseikonet) på verktøylinjen.
3.  Angi og bekreft et passord, og klikk deretter **OK** i dialogboksen **Beskytt**. Låseikonet på verktøylinjen utheves når en åpen byggeblokk er låst.

Hvis du vil åpne en låst byggeblokk, åpner du byggeblokken og klikker deretter **Aktiver/deaktiver beskyttelse** på verktøylinjen. Du kan også gå til **Verktøy**-menyen og klikke **Deaktiver beskyttelse** > .

## Byggeblokkgrupper
<a id="building-block-groups" class="xliff"></a>

Byggeblokker er raddefinisjoner, kolonnedefinisjoner rapporteringstredefinisjoner og rapportdefinisjoner som du oppretter for en rapport. Byggeblokk grupper er samlinger av definisjoner og dimensjonssett som er knyttet til et firma. Byggeblokkgrupper kan være firmaspesifikke eller flere firmaer kan dele samme sett med byggeblokker. Hvis noen av firmaene har ulike kontoplaner, kan du bruke forskjellig byggeblokkgruppe for hvert firma. Du kan også gi navn til alle dine individuelle byggeblokker for å gjenspeile hvilket firma de er kompatible med.
### Opprette en byggeblokkgruppe
<a id="create-a-building-block-group" class="xliff"></a>

1.  På **Firma**-menyen i Rapportutforming klikker du **Byggeblokkgrupper**.
2.  Klikk **Ny** i dialogboksen **Byggeblokkgrupper**.
3.  Angi et unikt navn og en beskrivelse for byggeblokkgruppen. Hvert felt kan inneholde maksimalt 256 tegn. (Dette tallet inkluderer mellomrom.)
4.  Klikk **OK** for å opprette den nye byggeblokkgruppen.

### Tilordne en byggeblokkgruppe
<a id="assign-a-building-block-group" class="xliff"></a>

Når du har oppretter en blokkgruppe, må du tilordne den til minst ett firma. Du kan deretter opprette rapport-, rad-, kolonne- og rapporteringstredefinisjoner og lagre dem i byggeblokkgruppen. Du må lukke alle byggeblokker før du starter fremgangsmåten nedenfor.
1.  På **Firma**-menyen i Rapportutforming klikker du **Firmaer**.
2.  I dialogboksen **Firmaer** velger du firmaet som det skal tilordnes en byggeblokkgruppe til.
3.  Klikk **Endre**.
4.  I dialogboksen **Endre firma**, i feltet **Byggeblokkgruppe**, velger du byggeblokkgruppen å tilordne til firmaet, eller klikker **Ny** for å opprette en ny byggeblokkgruppe.
5.  Klikk **OK** for å tilordne byggeblokkgruppen.
6.  Klikk **Lukk** for å lukke dialogboksen **Firmaer**. Byggeblokkgruppen du valgte, er nå tilordnet til firmaet. Nå vil alle nyopprettede raddefinisjoner, kolonnedefinisjoner og så videre, være en del av byggeblokkgruppen som er tilordnet dette firmaet. Du kan også importere en TDBX-fil eller rapport fra et annet system.

###  Vise en byggeblokkgruppe
<a id="view-a-building-block-group" class="xliff"></a>

Når en byggeblokkgruppen er opprettet og brukes, kan du vise alle byggeblokker som er tilordnet til den. Du kan også eksportere eller importere en byggeblokkgruppe og utføre tilleggsvedlikehold på byggeblokkgrupper.
1.  På **Firma**-menyen i Rapportutforming klikker du **Byggeblokkgrupper**.
2.  I dialogboksen **Byggeblokkgrupper** velger du byggeblokken som skal vises.
3.  Klikk **Vis** for å åpne dialogboksen **Vis byggeblokkgruppe**, der du kan vise innholdet i byggeblokkgruppen.
4.  Klikk **Lukk** for å lukke dialogboksen.

### Lagre en byggeblokkgruppe med et nytt navn
<a id="save-a-building-block-group-under-a-new-name" class="xliff"></a>

Du kan lagre en eksisterende byggeblokkgruppe med et nytt navn. Du kan deretter endre den nye byggeblokkgruppen uten å endre den opprinnelige byggeblokkgruppen.
1.  På **Firma**-menyen i Rapportutforming klikker du **Byggeblokkgrupper**.
2.  I dialogboksen **Byggeblokkgrupper** velger du byggeblokkgruppe som skal lagres med et nytt navn.
3.  Klikk **Lagre som**.
4.  Angi et nytt navn og en beskrivelse for byggeblokkgruppen.
5.  Klikk **OK**. Den nye byggeblokkgruppen vises i dialogboksen **Byggeblokkgrupper**.

###  Eksportere en byggeblokkgruppe
<a id="export-a-building-block-group" class="xliff"></a>

Du kan eksportere en byggeblokkgruppe eller bestemte rapportbyggeblokker i en byggeblokkgruppe. Du kan bruke den eksporterte byggeblokkgruppen som en sikkerhetskopi. Du kan også kopiere de eksporterte dataene mellom byggeblokkgrupper eller Dynamics 365 for Finance and Operations-installasjoner. Rapportutforming inneholder refererte skriftstiler og dimensjonssett sammen med byggeblokkgruppen.
1.  På **Firma**-menyen i Rapportutforming klikker du **Byggeblokkgrupper**.
2.  I dialogboksen **Byggeblokkgrupper** velger du byggeblokkgruppe som skal eksporteres, og deretter klikker du **Eksporter**.
3.  I dialogboksen **Eksporter** velger rapportdefinisjonene som skal eksporteres:
    -   Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, klikker du deretter den aktuelle kategorien og velger elementene som skal eksporteres. Hvis du vil velge flere elementer i en kategori, trykker du og holder nede CTRL-tasten. **Obs!** Når du velger rapporter å eksportere, velges tilhørende rader, kolonner, trær og dimensjonssett.

4.  Når du er ferdig med å velge elementene som skal eksporteres, velger **Eksporter**.
5.  I dialogboksen **Lagre som** velger du plasseringen byggeblokkgruppen skal eksporteres til.
6.  I **Filnavn**-feltet angir du et navn på filen. Rapportutforming legger automatisk til filtypen TDBX.
7.  Klikk **Lagre**. Byggeblokkgruppen lagres på plasseringen som du angav.

###  Importere en byggeblokkgruppe
<a id="import-a-building-block-group" class="xliff"></a>

Du kan importere en byggeblokkgruppe til en eksisterende byggeblokkgruppe, eller du kan opprette en ny byggeblokkgruppe for dataene. Alle importerte byggeblokkgrupper beholder sin opprinnelige skriftstiler og referanser for firmaet, og inkluderer de relevante dimensjonssettene.
1.  På **Firma**-menyen i Rapportutforming klikker du **Byggeblokkgrupper**.
2.  I dialogboksen **Byggeblokkgrupper** velger du byggeblokkgruppe som en byggeblokkgruppe skal importeres til, og deretter klikker du **Importer**.
3.  I dialogboksen **Åpne** velger du byggeblokkgruppe som skal importeres, og deretter klikker du **Åpne**.
4.  I dialogboksen **Importer** velger rapportdefinisjonene som skal importers:
    -   Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    -   Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonssett, velger du rapporter, rader, kolonner, trær eller dimensjonssett som skal importeres.

5.  Når du er ferdig med å velge elementene som skal importeres, velger **Importer**.

###  Angre en utsjekking av en byggeblokk
<a id="undo-a-checkout-of-a-building-block" class="xliff"></a>

Når du åpner en byggeblokk, har andre brukere skrivebeskyttet tilgang til byggeblokken. Noen ganger glemmer brukere å lukke en byggeblokk eller å avslutte systemet uten å lukke byggeblokken. Derfor forblir byggeblokken utsjekket, og ingen andre brukere kan åpne den. I slike tilfeller kan en administrator for finansrapportering bruke dialogboksen **Utsjekkede elementer** for å sjekke inn byggeblokker som brukere latt være utsjekket. **Obs!** Du må ha administratorrolle for å sjekke inn byggeblokker ved hjelp av dialogboksen **Utsjekkede elementer**.
1.  På **Verktøy**-menyen i Rapportutforming klikker du **Utsjekkede elementer**.
2.  I dialogboksen **Utsjekkede elementer** velger du **Vis elementer fra alle brukere**. Listen oppdateres for å vise alle byggeblokker som er sjekket ut og hvilke brukere som har sjekket dem ut.
3.  Velg en byggeblokk, og klikk deretter **Angre utsjekking**.
4.  Klikk **Ja** for å sjekke inn byggeblokken.

# Se også
<a id="see-also" class="xliff"></a>

[Finansrapportering](financial-reporting-intro.md)




