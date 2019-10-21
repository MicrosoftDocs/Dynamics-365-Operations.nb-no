---
title: Konfigurere manuelle beslutninger i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene i en manuell beslutning.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f46b875f52d3d3e7c755ee92dcd5faddf0d94356
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179311"
---
# <a name="configure-manual-decisions-in-a-workflow"></a>Konfigurere manuelle beslutninger i en arbeidsflyt

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer egenskapene i en manuell beslutning.

Når du skal konfigurere en manuell beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den manuelle beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den manuelle beslutningen.

## <a name="name-the-decision"></a>Navn på beslutningen

Følg denne fremgangsmåten for å sette et navn på den manuelle beslutningen.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på den manuelle beslutningen.

## <a name="enter-a-subject-line-and-instructions"></a>Legg inn en emnelinje og instruksjoner

Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til den manuelle beslutningen. Hvis du for eksempel konfigurerer en beslutning for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til beslutningen, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden. Emnelinjen vises i en meldingslinje øverst på siden. Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene. Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I **Emne for arbeidselement**-feltet i kategorien **Instruksjoner** angir du emnelinjen.
3. Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk **Sett inn**.

4. Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.
    6. Klikk **Lukk**.

5. I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.
6. Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk **Sett inn**.

7. Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.
    6. Klikk **Lukk**.

## <a name="specify-the-possible-outcomes-of-a-decision"></a>Angi de mulige resultatene av en beslutning

Vanligvis når et dokument tilordnes til en beslutningstaker, får beslutningstakeren et spørsmål. Svaret på dette spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**. Følg denne fremgangsmåten for å angi de mulige resultatene av den manuelle beslutningen.

1. Klikk **Grunnleggende innstillinger** i ruten til venstre.
2. I kategorien **Resultater** i **Resultat 1**-feltet angir du navnet på resultatet eller alternativet.
3. Hvis du vil legge til oversettelser av resultatet, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Klikk **Lukk**.

4. I **Resultat 2**-feltet angir du navnet på resultatet eller alternativet.
5. Hvis du vil legge til oversettelser av resultatet, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Klikk **Lukk**.

## <a name="specify-when-notifications-are-sent"></a>Angi når varslinger skal sendes

Du kan sende varslinger til personer når en beslutning er tatt, delegert eller videresendt. Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.

1. I den venstre ruten klikker du **Varslinger**.
2. Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:

    - **\[Valg 1\]** – Den tilordnede brukeren har valgt **\[Valg 1\]**.
    - **\[Valg 2\]** – Den tilordnede brukeren har valgt **\[Valg 2\]**.
    - **Deleger** – Den tilordnede brukeren har tilordnet beslutningen til en annen bruker.
    - **Eskaler** – Den tilordnede brukeren har ikke tatt beslutningen innen fristen.

3. Velg raden for en hendelse du valgte i trinn 2.
4. I tekstfeltet i kategorien **Varslingstekst** skriver du inn teksten i meldingen.
5. Hvis du vil tilpasse varslingen, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når varslingen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk **Sett inn**.

6. Hvis du vil legge til oversettelser av varslingen, gjør du følgende:

    1. Klikk **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 5.
    6. Klikk **Lukk**.

7. I **Mottaker**-kategorien angir du hvem meldingene skal sendes til. Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 8.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Varslingsmottakere</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltaker</td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som meldingene skal sendes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller som varslingene skal sendes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.

## <a name="assign-a-decision"></a>Tilordne en beslutning

Følg denne fremgangsmåten for å angi hvem en manuell beslutning skal tilordnes til.

1. I den venstre ruten klikker du **Tilordning**.
2. I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Brukere som beslutningen er tilordnet til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltaker</td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som beslutningen skal tilordnes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som beslutningen skal tilordnes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som beslutningen skal tilordnes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som beslutningen kan tilordnes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter: <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol>
    </li>
    <li>I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som beslutningen skal tilordnes til: <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Beslutningen tilordnes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Beslutningen tilordnes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Beslutningen tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil tilordne beslutningen til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kø</td>
    <td>En arbeidselementkø</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Kø</strong>, klikker du <strong>Købasert</strong>-kategorien.</li>
    <li>Gjør følgende for å tilordne beslutningen til en bestemt kø: <ol>
    <li>I <strong>Køtype</strong>-listen velger du <strong>Arbeidselementkøer</strong>.</li>
    <li>Velg køen i <strong>Kønavn</strong>-listen.</li>
    </ol>
    </li>
    <li>Hvis en bestemt betingelse skal bestemme hvilken kø beslutningen skal tilordnes til, følger du denne fremgangsmåten: <ol>
    <li>I <strong>Køtype</strong>-listen velger du <strong>Betingede arbeidselementkøer</strong>.</li>
    <li>I <strong>Kønavn</strong>-listen velger du <strong>Betinget kø</strong>.</li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] Dette alternativet brukes bare i noen få arbeidsflyter, for eksempel saksbehandling.</blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å ta beslutningen. Velg ett av følgende alternativer:

    - **Timer** – Angi antallet timer som brukeren har til å ta beslutningen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antallet dager som brukeren har til å ta beslutningen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antallet uker som brukeren har til å ta beslutningen.
    - **Måneder** – Velg dagen og uken som brukeren senest må ta beslutningen. Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden som brukeren senest må ta beslutningen. Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i desember.

    Hvis brukeren ikke tar beslutningen innen fristen, er beslutningen forfalt. Et beslutning som er forfalt, videresendes, basert på alternativene du velger i **Eskalering**-området på siden.

## <a name="specify-what-happens-when-a-decision-is-overdue"></a>Angi hva som skal skje når en beslutning er forfalt

Hvis en bruker ikke tar beslutningen innen fristen, er beslutningen forfalt. En beslutning som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker. Følg denne fremgangsmåten for å videresende beslutningen hvis den er forfalt.

1. I den venstre ruten klikker du **Eskalering**.
2. Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane. Systemet tilordner automatisk beslutningen til brukerne som er oppført i videresendingsbanen. Tabellen nedenfor er et eksempel på en videresendingsbane.

    | Sekvens | Videresendingsbane            |
    |----------|----------------------------|
    | 1        | Tilordne til: Doris           |
    | 2        | Tilordne til: Elin            |
    | 3        | Endelig handling: \[Valg 1\] |

    I dette eksempelet tilordnes den forfalte beslutningen til Doris. Hvis Doris ikke tar beslutningen innen tidsfristen, tilordnes beslutningen til Elin. Hvis Elin ikke tar beslutningen innen tidsfristen, velges **\[Valg 1\]** som beslutningen.

3. Klikk **Legg til videresending** for å legge til en bruker i videresendingsbanen. Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 4.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Brukere som beslutningen videresendes til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som beslutningen videresendes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som beslutningen kan videresendes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter: <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol>
    </li>
    <li>I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som beslutningen skal videresendes til: <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Beslutningen videresendes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Beslutningen videresendes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Beslutningen videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil videresende beslutningen til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å ta beslutningen. Velg ett av følgende alternativer:

    - **Timer** – Angi antallet timer som brukeren har til å ta beslutningen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antallet dager som brukeren har til å ta beslutningen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antallet uker som brukeren har til å ta beslutningen.
    - **Måneder** – Velg dagen og uken som brukeren senest må ta beslutningen. Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden som brukeren senest må ta beslutningen. Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i desember.

5. Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen. Du kan endre rekkefølgen på brukerne.
6. Hvis brukerne i videresendingsbanen ikke tar beslutningen innen tidsfristen, vil systemet ta beslutningen. Hvis du vil angi alternativet systemet skal velge, merker du **Handling**-raden, og velger deretter et alternativ i kategorien **Avslutt handling**.

## <a name="set-a-time-limit"></a>Angi en tidsfrist

Følg denne fremgangsmåten hvis beslutningen må tas innen et bestemt tidspunkt.

> [!NOTE]
> Alternativene du velger i prosedyren, overstyrer alternativene du velger i **Tilordning**- og **Eskalering**-området på siden.

1. Klikk **Avanserte innstillinger** i ruten til venstre.
2. Merk av for **Angi en tidsgrense for arbeidsflytelementet**.
3. I **Varighet**-feltet angir du når beslutningen må tas. Velg ett av følgende alternativer:

    - **Timer** – Angi antallet timer. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antallet dager. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antallet uker.
    - **Måneder** – Velg dagen og uken da beslutningen må være tatt. Du vil for eksempel at beslutningen skal tas innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden da beslutningen må være tatt. Du vil for eksempel at beslutningen skal tas innen fredag i den tredje uken i desember.

4. Hvis tidsgrensen overskrides, vil systemet ta beslutningen. I listen **Handling** velger du alternativet som systemet skal velge.
