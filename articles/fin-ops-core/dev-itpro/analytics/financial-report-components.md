---
title: Komponenter for finansrapport
description: Denne artikkelen beskriver hvordan komponenter eller byggeblokker i rapportdefinisjoner brukes i finansrapportering.
author: aprilolson
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.form: FinancialReports
ms.openlocfilehash: 180b3c64b9eb506f162071a67b1fa9b728a569ce
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831617"
---
# <a name="financial-report-components"></a>Komponenter for finansrapport

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan komponenter eller byggeblokker i rapportdefinisjoner brukes i finansrapportering. Disse byggeblokkene inkluderer raddefinisjoner, kolonnedefinisjoner og rapporteringstredefinisjoner. Denne artikkelen forklarer hvordan du ordner og låse byggesteiner.

Utformingsfilosofien bak Utforming av finansrapport er å dele informasjonen inn i de minste komponenten eller byggeblokkene, og deretter blande og samsvare komponentene som kreves. Derfor er rapportformateringen atskilt fra dine økonomiske data, og du kan endre utformingen av en rapport uten å endre de økonomiske dataene i Microsoft Dynamics 365 Finance. Ved å bruke denne fremgangsmåten for byggeblokken, kan du kombinere tekst, beløp og beregninger for å lage rapportene du trenger. Denne fleksibiliteten fremmer kreativiteten ved å gjøre det enkelt for deg å vise operasjoner på forskjellige måter. De individuelle byggeblokkene i en rapportdefinisjon ligner på et tredimensjonalt regneark, men de har flere muligheter. En rapportdefinisjon angir raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon som skal brukes for rapporten. Den inneholder også informasjon om hvor den genererte rapporten skal lagres og hvordan den skal formateres.

## <a name="building-blocks-of-a-report"></a>Byggeblokker i en rapport

| Byggeblokk            | beskrivelse | For mer informasjon |
|---------------------------|-------------|----------------------|
| Raddefinisjon            | En raddefinisjon definerer de beskrivende linjene (for eksempel lønn eller salg) i en rapport. Den viser i tillegg segmentverdiene eller dimensjonene som inneholder verdiene for hver linjevare, og inneholder radformatering og beregninger. | [Raddefinisjoner](row-definitions-financial-reporting.md) |
| Kolonnedefinisjon         | En kolonnedefinisjon definerer perioden som skal brukes når data trekkes ut fra finansdimensjonene. Den inneholder også kolonneformatering og beregninger. | [Kolonnedefinisjoner](column-definitions-financial-reports.md) |
| Rapporteringstredefinisjon | En rapporteringtredefinisjon ligner på et organisasjonskart. Den inneholder individuelle rapportenheter som representerer hver boks i diagrammet. Enhetene kan være individuelle avdelinger fra de økonomiske dataene eller overordnet enheter som summerer data fra andre rapporteringsenheter. | [Rapporteringstredefinisjoner](financial-reporting-tree-definitions.md) |
| Rapportdefinisjon         | En rapportdefinisjon bruker en raddefinisjon, kolonnedefinisjon og valgfri rapporteringstredefinisjon for å bygge en rapport. Den inneholder også flere alternativer og innstillinger som du kan bruke for å tilpasse en rapport. | [Rapportdefinisjon](design-financial-report-definitions.md) |

Hvis du ikke har erfaring med å utforme rapporter, kan det hende du vil bruke rapportveiviseren for raskt å opprette en rapportdefinisjon som du kan tilpasse senere. Hvis du har erfaring med å utforme rapporter og vil ha større fleksibilitet for rapportutformingen, kan du kombinere nye eller eksisterende byggeblokker for å opprette en ny rapportdefinisjon. Du trenger ikke forstår fullt ut alle de tilgjengelige alternativene for rapportdefinisjon for å lage kvalitetsrapporter. Når du blir vant med å utforme rapporter, kan du utvide rapportdefinisjonene for å dra nytte av mer avanserte funksjoner. Når du har opprettet en grunnleggende rapport, kan du tilpasse rapportdefinisjonen og eventuelle byggeblokker i rapportdefinisjonen.

## <a name="organize-the-building-blocks"></a>Organisere byggeblokkene
Bruke mapper til å organisere byggeblokkene i Rapportutforming. Alle mappene er spesifikke for typen byggeblokk som de inneholder. Alle mapper som for eksempel inneholder raddefinisjoner, finnes i ruten **Raddefinisjoner** i Report Designer.

### <a name="create-a-folder"></a>Opprette en mappe

1. I Report Designer velger du type byggeblokk å organisere i navigasjonsruten. Hvis du for eksempel vil sortere en raddefinisjon, klikker du **Raddefinisjoner**.
2. I navigasjonsruten velger du den eksisterende mappen som den nye mappen skal opprettes under, og deretter følger du én av disse trinnene:

    - Høyreklikk den overordnede mappen, og klikk deretter **Ny mappe**.
    - Velg den overordnede mappen, klikk **Fil**, og klikk deretter **Ny mappe**.

3. Når den nye mappen vises, angir du deretter navnet på den nye mappen og trykker **Enter**.

## <a name="lock-a-building-block"></a> Låse en byggeblokk
Du kan opprette et passord for å låse og bidra til å beskytte en byggeblokk. På denne måten kan du legge til et sikkerhetsnivå i en rapportkomponent uten å sikre hele systemet. Et passord kan bidra til å beskytte byggeblokkinformasjon som er viktig for rapporteringsprosessen for månedsavslutning. En bruker i en hvilken som helst rolle kan låse en byggeblokk. Andre brukere har imidlertid alltid skrivebeskyttet tilgang til en låst komponent. Brukere kan åpne, endre og lagre den låste komponenten med et nytt navn. En bruker som har rollen administrator har alltid få tilgang til og kan endre en låst byggeblokk.

1. Åpne rapportkomponenten som skal låses i Report Designer, for eksempel en raddefinisjon, kolonnedefinisjon, rapportdefinisjon eller rapporteringstredefinisjon.
2. På **Verktøy**-menyen klikker du **Aktiver/deaktiver beskyttelse**. Du kan også klikke ikonet for **Aktiver/deaktiver beskyttelse** (låseikonet) på verktøylinjen.
3. Angi og bekreft et passord, og klikk deretter **OK** i dialogboksen **Beskytt**. Låseikonet på verktøylinjen utheves når en åpen byggeblokk er låst.

Hvis du vil åpne en låst byggeblokk, åpner du byggeblokken og klikker deretter **Aktiver/deaktiver beskyttelse** på verktøylinjen. Du kan også gå til **Verktøy**-menyen og klikke **Deaktiver beskyttelse**.

## <a name="building-block-groups"></a>Byggeblokkgrupper

Byggeblokker er raddefinisjoner, kolonnedefinisjoner rapporteringstredefinisjoner og rapportdefinisjoner som du oppretter for en rapport. Byggeblokkgrupper er samlinger av definisjonene og dimensjonsverdisettene

### <a name="view-a-building-block-group"></a>Vise en byggeblokkgruppe

Du kan vise alle byggeblokker som er tilordnet til en byggeblokkgruppe. Du kan også eksportere eller importere en byggeblokkgruppe.

1. Klikk **Byggeblokkgrupper** på **Firma**-menyen i Report Designer.
2. I dialogboksen **Byggeblokkgrupper** velger du byggeblokken som skal vises.
3. Klikk på **Vis** for å åpne dialogboksen **Vis byggeblokkgruppe**, der du kan vise innholdet i byggeblokkgruppen.
4. Klikk på **Lukk** for å lukke dialogboksene.

### <a name="export-a-building-block-group"></a>Eksportere en byggeblokkgruppe

Du kan eksportere en byggeblokkgruppe eller bestemte rapportbyggeblokker i en byggeblokkgruppe. Du kan bruke den eksporterte byggeblokkgruppen som en sikkerhetskopi. Du kan også kopiere de eksporterte dataene mellom installasjoner. Report Designer inneholder refererte skriftstiler og dimensjonsverdisett sammen med byggeblokkgruppen.

1. Klikk **Byggeblokkgrupper** på **Firma**-menyen i Report Designer.
2. Velg byggeblokkgruppen som skal eksporteres, i dialogboksen **Byggeblokkgrupper**, og klikk deretter **Eksporter**.
3. I dialogboksen **Eksporter** velger rapportdefinisjonene som skal eksporteres:

    - Hvis du vil eksportere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    - Hvis du vil eksportere bestemte rapporter, rader, kolonner, trær eller dimensjonsverdisett, klikker du deretter den aktuelle fanen og velger elementene som skal eksporteres. Hvis du vil velge flere elementer i en kategori, trykker du og holder nede CTRL-tasten.

    > [!NOTE]
    > Når du velger rapporter som skal eksporteres, velges de tilknyttede radene, kolonnene, trærne og dimensjonsverdisettene.

4. Når du er ferdig med å velge elementene som skal eksporteres, velger **Eksporter**.
5. I dialogboksen **Lagre som** velger du plasseringen byggeblokkgruppen skal eksporteres til.
6. I **Filnavn**-feltet angir du et navn på filen. Rapportutforming legger automatisk til filtypen TDBX.
7. Klikk på **Lagre**. Byggeblokkgruppen lagres på plasseringen som du angav.

### <a name="import-a-building-block-group"></a> Importere en byggeblokkgruppe

Du kan importere en byggeblokkgruppe til en eksisterende byggeblokkgruppe. Alle importerte byggeblokkgrupper beholder sin opprinnelige skriftstiler og referanser for firmaet, og inkluderer de relevante dimensjonsverdisettene.

1. Klikk **Byggeblokkgrupper** på **Firma**-menyen i Report Designer.
2. Velg byggeblokken som en byggeblokkgruppe skal importeres til, i dialogboksen **Byggeblokkgrupper**, og klikk deretter **Importer**.
3. Velg byggeblokkgruppen som skal importeres, i dialogboksen **Åpne**, og klikk deretter **Åpne**.
4. I dialogboksen **Importer** velger rapportdefinisjonene som skal importers:

    - Hvis du vil importere alle rapportdefinisjonene og de tilknyttede byggeblokkene, klikker du **Velg alle**.
    - Hvis du vil importere bestemte rapporter, rader, kolonner, trær eller dimensjonsverdisett, velger du rapporter, rader, kolonner, trær eller dimensjonsverdisett som skal importeres.

5. Når du er ferdig med å velge elementene som skal importeres, velger **Importer**.

### <a name="undo-a-checkout-of-a-building-block"></a> Angre en utsjekking av en byggeblokk

Når du åpner en byggeblokk, har andre brukere skrivebeskyttet tilgang til byggeblokken. Noen ganger glemmer brukere å lukke en byggeblokk eller å avslutte systemet uten å lukke byggeblokken. Derfor forblir byggeblokken utsjekket, og ingen andre brukere kan åpne den. I slike tilfeller kan en administrator for finansrapportering bruke dialogboksen **Utsjekkede elementer** for å sjekke inn byggeblokker som brukere latt være utsjekket.

> [!NOTE]
> Du må ha rollen som administrator for å kunne sjekke inn byggeblokker fra dialogboksen **Utsjekkede elementer**.

1. På **Verktøy**-menyen i Report Designer klikker du **Utsjekkede elementer**.
2. Velg **Vis elementer fra alle brukere** i dialogboksen **Utsjekkede elementer**. Listen oppdateres for å vise alle byggeblokker som er sjekket ut, og brukerne som har sjekket dem ut.
3. Merk en byggeblokk, og klikk deretter **Angre utsjekking**.
4. Klikk på **Ja** for å sjekke inn byggeblokken.

## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
