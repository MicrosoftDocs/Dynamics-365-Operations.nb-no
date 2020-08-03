---
title: Konfigurere egenskaper for arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer de ulike egenskapene i en arbeidsflyt.
author: sericks007
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 268448049955170b8eb9e64cbd50416565a041b1
ms.sourcegitcommit: 561d06c2a74602dfaa40334d8afac5053aebc055
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2020
ms.locfileid: "3541115"
---
# <a name="configure-workflow-properties"></a>Konfigurere egenskaper for arbeidsflyt

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer de ulike egenskapene i en arbeidsflyt.

Hvis du vil konfigurere egenskapene for en arbeidsflyt, kan du åpne arbeidsflyten i redigeringsprogrammet for arbeidsflyt. Klikk lerretet i redigeringsprogrammet for arbeidsflyt, og klikk deretter **Egenskaper** for å åpne **Egenskaper**-siden. Du kan deretter bruke fremgangsmåten nedenfor for å konfigurere de ulike egenskapene for arbeidsflyten.

## <a name="name-the-workflow"></a>Sette navn på arbeidsflyten

Følg denne fremgangsmåten for å sette et navn på arbeidsflyten.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I **Navn**-feltet angir du et unikt navn på arbeidsflyten. Hvis du for eksempel oppretter en arbeidsflyt for innkjøpsrekvisisjon for hvert land eller område du opererer i, kan du kalle arbeidsflyten **Innkjøpsrekvisisjoner Danmark** eller **Innkjøpsrekvisisjoner Spania**.

## <a name="specify-the-workflow-owner"></a>Angi arbeidsflyteieren

Arbeidsflyteieren er personen som administrerer og vedlikeholder arbeidsflyten. Følg fremgangsmåten nedenfor for å angi arbeidsflyteieren.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I **Eier**-listen velger du navnet på personen som skal administrere arbeidsflyten.

## <a name="select-an-email-template"></a>Velg en e-postmal

Følg denne fremgangsmåten for å velge e-postmalen som brukes til å generere meldinger om arbeidsflyten.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I listen **E-postmal for arbeidsflytvarsler** velger du malen.

## <a name="enter-instructions-for-users"></a>Skrive inn instruksjoner til brukerne

Du kan gi instruksjoner til brukere som sender dokumenter til behandling og godkjenning. Disse brukerne omtales også som *avsendere*. Du oppretter for eksempel en arbeidsflyt for innkjøpsrekvisisjon og du angir instruksjoner. Disse instruksjonene kan deretter vises av brukere som registrerer innkjøpsrekvisisjoner på **Innkjøpsrekvisisjoner**-siden. Klikk ikonet på meldingslinjen for arbeidsflyt for å vise instruksjoner. Følg fremgangsmåten nedenfor for å skrive inn instruksjoner for brukere.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I **Sendeinstruksjoner**-feltet angir du instruksjonene.
3. Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. Klikk i **Sendeinstruksjoner**-feltet for å angi hvor plassholderen skal vises.
    2. Klikk **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk **Sett inn**.

4. Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten skal angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere. Hvis du vil ha instruksjoner om hvordan du skriver inn en plassholder, kan du se trinn 3.
    6. Klikk **Lukk**.

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a>Angi når denne arbeidsflyten brukes gjennom aktiveringsbetingelser

Du kan opprette flere arbeidsflyter som er basert på den samme arbeidsflyttypen. Når du har flere arbeidsflyter som er basert på den samme typen, må du angi når hver arbeidsflyt skal brukes, ved hjelp av aktiveringsbetingelser. Hvis aktiveringsbetingelser ikke er oppfylt, brukes standard arbeidsflyt. Hvis det bare er definert én arbeidsflytkonfigurasjon for en arbeidsflyttype, blir denne arbeidsflytkonfigurasjonen brukt uavhengig av aktiveringsbetingelsene.

Du kan for eksempel opprette en arbeidsflyt for innkjøpsrekvisisjon for hvert land eller område du opererer i, for eksempel Innkjøpsrekvisisjoner Danmark og Innkjøpsrekvisisjoner Spania, med følgende betingelser:

- Innkjøpsrekvisisjoner Danmark brukes når land/område = DK
- Innkjøpsrekvisisjoner Spania brukes når land/område = ES

Følg fremgangsmåten nedenfor for å angi at arbeidsflyten du konfigurerer, skal brukes.

1. I den venstre ruten klikker du **Aktivering**.
2. Merk av for **Angi betingelsene for å kjøre denne arbeidsflyten**.
3. Klikk **Legg til betingelse**.
4. Angi en betingelse.
5. Angi eventuelle ekstra betingelser som kreves.
6. Kjør gjennom arbeidsflyten med noen målposter for å bekrefte at betingelsen inneholder og utelater poster på riktig måte.

## <a name="specify-when-notifications-are-sent"></a>Angi når varslinger skal sendes

Når et dokument sendes til behandling, opprettes det en arbeidsflytforekomst. Du kan sende meldinger til brukere når arbeidsflytforekomster som er basert på arbeidsflyten, startes, fullføres, avbrytes eller stoppes på grunn av en feil. Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes.

1. I den venstre ruten klikker du **Varslinger**.
2. Merk av for hver hendelse som skal utløse varslinger:

    - **Startet** – Send meldinger når en arbeidsflytforekomst er startet.
    - **Stanset** – Send meldinger når en arbeidsflytforekomst er stoppet på grunn av en feil.
    - **Fullført** – Send meldinger når en arbeidsflytforekomst er fullført.
    - **Uopprettelig** – Send meldinger når en arbeidsflytforekomst er stoppet på grunn av en uopprettelig feil.
    - **Avsluttet** – Send meldinger når en arbeidsflytforekomst er avsluttet.

3. Velg raden for en hendelse du valgte i trinn 2.
4. I kategorien **Varslingstekst** skriver du inn teksten i meldingen.
5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når teksten vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. Klikk i feltet for å angi hvor plassholderen skal vises.
    2. Klikk **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk **Sett inn**.
    5. Et felles **Varslingstekst**-plassholder for å inkludere "Siste merknader: %Arbeidsflyt.Siste merknad%", som viser eventuelle merknader fra det forrige trinnet.

6. Hvis du vil legge til oversettelser av teksten, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten skal angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere. Hvis du vil ha instruksjoner om hvordan du skriver inn en plassholder, kan du se trinn 5.
    6. Klikk **Lukk**.

7. I kategorien **Mottaker** bruker du følgende alternativer til å angi hvem som skal motta meldingene.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Varslinger sendes til disse brukerne</th>
    <th>Følg denne fremgangsmåten for å sende varslinger</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltaker</td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>I kategorien <strong>Mottaker</strong> klikker du <strong>Deltaker</strong>.</li>
    <li>I kategorien <strong>Rollebasert</strong> i <strong>Type deltaker</strong>-listen velger du typen gruppe eller rolle som varslingene skal sendes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbeidsflytbruker</td>
    <td>Brukere som er deltakere i denne arbeidsflyten</td>
    <td>
    <ol>
    <li>I kategorien <strong>Mottaker</strong> klikker du <strong>Arbeidsflytbruker</strong>.</li>
    <li>I kategorien <strong>Arbeidsflytbruker</strong> i <strong>Arbeidsflytbruker</strong>-listen velger du en deltaker i denne arbeidsflyten.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>I kategorien <strong>Mottaker</strong> klikker du <strong>Bruker</strong>.</li>
    <li>I kategorien <strong>Bruker</strong> inkluderer <strong>Tilgjengelige brukere</strong>-listen alle brukere. Velg brukerne du vil sende varslinger til, og flytt disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Angi kommentarer om endringene du gjorde i arbeidsflyten.

Hvis du vil angi kommentarer om endringene du gjorde i arbeidsflyten, følger du fremgangsmåten nedenfor.

1. I den venstre ruten klikker du **Notater**.
2. I feltet **Skriv inn kommentarer om arbeidsflyten** angir du kommentarene dine.
3. Gå gjennom kommentarene dine. Når du har lagt til kommentarer, kan du ikke endre dem.
4. Klikk **Legg til** for å legge til kommentarene dine i **Kommentarlogg**-området.
