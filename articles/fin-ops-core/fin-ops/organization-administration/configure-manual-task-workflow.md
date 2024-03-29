---
title: Konfigurere manuelle oppgaver i en arbeidsflyt
description: Denne artikkelen forklarer hvordan du konfigurerer egenskapene for en manuell oppgave.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265f127f948aa7425c5eb523abe18986a942cfb0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889214"
---
# <a name="configure-manual-tasks-in-a-workflow"></a>Konfigurere manuelle oppgaver i en arbeidsflyt

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Denne artikkelen forklarer hvordan du konfigurerer egenskapene for en manuell oppgave.

Når du skal konfigurere en manuell oppgave i redigeringsprogrammet for arbeidsflyt, høyreklikker du oppgaven og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den manuelle oppgaven.

## <a name="name-the-task"></a>Gi navn til oppgaven

Følg denne fremgangsmåten for å sette et navn på den manuelle oppgaven.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på oppgaven.

## <a name="enter-a-subject-line-and-instructions"></a>Legg inn en emnelinje og instruksjoner

Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til oppgaven. Hvis du for eksempel konfigurerer en oppgave for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til oppgaven, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden. Emnelinjen vises i en meldingslinje øverst på siden. Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene. Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. I **Emne for arbeidselement**-feltet angir du emnelinjen.
3. Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk på **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk på **Sett inn**.

4. Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:

    1. Klikk på **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.
    6. Klikk på **Lukk**.

5. I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.
6. Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk på **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk på **Sett inn**.

7. Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:

    1. Klikk på **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.
    6. Klikk på **Lukk**.

## <a name="assign-the-task"></a>Tildele oppgaven

Følg denne fremgangsmåten for å angi hvem den manuelle oppgaven skal tildeles.

1. I den venstre ruten klikker du **Tilordning**.
2. I **Tilordningstype**-fanen velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Brukere som oppgaven er tilordnet til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Deltaker</td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-fanen i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som oppgaven skal tilordnes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som oppgaven skal tilordnes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-fanen i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som oppgaven skal tilordnes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som oppgaven kan tilordnes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter: <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol>
    </li>
    <li>I fanen <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som oppgaven skal tilordnes til: <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Oppgaven tilordnes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Oppgaven tilordnes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Oppgaven tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk på <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
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
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil tilordne oppgaven til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Kø</td>
    <td>En arbeidselementkø</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Kø</strong>, klikker du <strong>Købasert</strong>-fanen.</li>
    <li>Gjør følgende for å tilordne oppgaven til en bestemt kø: <ol>
    <li>I <strong>Køtype</strong>-listen velger du <strong>Arbeidselementkøer</strong>.</li>
    <li>Velg køen i <strong>Kønavn</strong>-listen.</li>
    </ol>
    </li>
    <li>Hvis en bestemt betingelse skal bestemme hvilken kø oppgaven skal tilordnes til, følger du denne fremgangsmåten: <ol>
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

3. I **Tidsbegrensning**-fanen i **Varighet**-feltet angir du hvor lang tid brukeren har til å fullføre oppgaven. Velg ett av følgende alternativer:

    - **Timer** – Angi antallet timer som brukeren har til å fullføre oppgaven. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antallet dager som brukeren har til å fullføre oppgaven. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antallet uker som brukeren har til å fullføre oppgaven.
    - **Måneder** – Velg dagen og uken som brukeren senest må fullføre oppgaven. Du vil kanskje at brukeren fullfører oppgaven innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden som brukeren senest må fullføre oppgaven. Du vil kanskje at brukeren svarer innen fredag i den tredje uken i desember.

    Hvis brukeren ikke fullfører oppgaven innenfor den tillatte tiden, er oppgaven forfalt. En oppgave som er forfalt, kan videresendes, basert på alternativene du velger i **Eskalering**-området på siden.

## <a name="specify-what-happens-when-the-task-is-overdue"></a>Angi hva som skal skje når en oppgave er forfalt

Hvis en bruker ikke fullfører den manuelle oppgaven innenfor den tillatte tiden, er oppgaven forfalt. En oppgave som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker. Følg denne fremgangsmåten for å videresende oppgaven hvis den er forfalt.

1. I den venstre ruten klikker du **Eskalering**.
2. Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane. Systemet tilordner automatisk oppgaven til brukerne som er oppført i videresendingsbanen. Tabellen nedenfor er et eksempel på en videresendingsbane.

    | Sekvens | Videresendingsbane      |
    |----------|----------------------|
    | 1        | Tilordne til: Doris     |
    | 2        | Tilordne til: Elin      |
    | 3        | Endelig handling: Avvis |

    I dette eksempelet tilordnes den forfalte oppgaven til Doris. Hvis Doris ikke fullfører oppgaven innen tidsfristen, tilordnes oppgaven til Elin. Hvis Elin ikke fullfører oppgaven innen tidsfristen, vil systemet avvise dokumentet som ble sendt til behandling.

3. Klikk på **Legg til videresending** for å legge til en bruker i videresendingsbanen. I **Tilordningstype**-fanen velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 4.

    <table>
    <thead>
    <tr>
    <th>Alternativ</th>
    <th>Brukere som oppgaven videresendes til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-fanen i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som oppgaven skal videresendes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som oppgaven kan videresendes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter: <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol>
    </li>
    <li>I fanen <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som oppgaven skal videresendes til: <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Oppgaven videresendes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Oppgaven videresendes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Oppgaven videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk på <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
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
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil videresende oppgaven til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. I **Tidsbegrensning**-fanen i **Varighet**-feltet angir du hvor lang tid brukeren har til å fullføre oppgaven. Velg ett av følgende alternativer:

    - **Timer** – Angi antallet timer som brukeren har til å fullføre oppgaven. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antallet dager som brukeren har til å fullføre oppgaven. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antallet uker som brukeren har til å fullføre oppgaven.
    - **Måneder** – Velg dagen og uken som brukeren senest må fullføre oppgaven. Du vil kanskje at brukeren fullfører oppgaven innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden som brukeren senest må fullføre oppgaven. Du vil kanskje at brukeren svarer innen fredag i den tredje uken i desember.

5. Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen. Du kan endre rekkefølgen på brukerne.
6. Hvis brukerne i videresendingsbanen ikke fullfører oppgaven innen tidsfristen, vil systemet utføre en handling med oppgaven. Hvis du vil angi handlingen systemet skal utføre, merker du **Handling**-raden, og velger deretter en handling i fanen **Avslutt handling**.

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a>Angi når systemet skal utføre en handling med oppgaven automatisk

Du kan konfigurere systemet slik at det utfører en handling med den manuelle oppgaven når bestemte betingelser er oppfylt. En oppgave krever for eksempel at noen i reiseregningsavdelingen går gjennom kvitteringene som følger med reiseregningen. I henhold til firmapolicyen må denne oppgaven utføres hvis det totale beløpet for utgiftsrapporten er større enn USD 100. I dette scenariet kan du konfigurere systemet til automatisk å merke oppgaven som **Fullført** når samlet beløp er mindre enn 100. Følg denne fremgangsmåten for å angi når systemet utfører en handling med den manuelle oppgaven.

1. I den venstre ruten klikker du **Automatiske handlinger**.
2. Merk av for **Aktiver automatiske handlinger**.
3. Klikk på **Legg til betingelse**.
4. Angi en betingelse.
5. Angi eventuelle ekstra betingelser som kreves.
6. Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:

    1. Klikk på **Test**.
    2. På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post.
    3. Klikk på **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4. Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.

7. I listen **Autofullføringshandling** velger du den handlingen som systemet skal utføre med oppgaven.

## <a name="specify-when-notifications-are-sent"></a>Angi når varslinger skal sendes

Du kan sende meldinger til personer når en manuell oppgave er delegert, videresendt, fullført eller avvist, eller når det er bedt om en endring. Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.

1. I den venstre ruten klikker du **Varslinger**.
2. Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:

    - **Deleger** – Oppgaven er tilordnet til en annen bruker.
    - **Eskaler** – Den tilordnede brukeren har ikke fullført oppgaven innen fristen.
    - **Fullført** – Den tilordnede brukeren har fullført oppgaven.
    - **Avvis** – Den tilordnede brukeren har avvist dokumentet som ble sendt.
    - **Be om endring** – Den tilordnede brukeren har bedt om en endring i dokumentet som ble sendt.

3. Velg raden for en hendelse du valgte i trinn 2.
4. I tekstfeltet i fanen **Varslingstekst** skriver du inn teksten i meldingen.
5. Hvis du vil tilpasse varslingen, kan du sette inn plassholdere. Plassholdere erstattes med den riktige informasjonen når varslingen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. I tekstboksen klikker du der plassholderen skal vises.
    2. Klikk på **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk på **Sett inn**.

6. Hvis du vil legge til oversettelser av varslingen, gjør du følgende:

    1. Klikk på **Oversettelser**.
    2. På siden som vises, klikker du **Legg til**.
    3. I listen som vises, velger du språket teksten angis på.
    4. I **Oversatt tekst**-feltet legger du inn teksten.
    5. Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 5.
    6. Klikk på **Lukk**.

7. I **Mottaker**-fanen angir du hvem meldingene skal sendes til. Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 8.

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
    <li>Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-fanen i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som meldingene skal sendes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td>
    <ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-fanen i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>Bruker</td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle brukere. Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.

## <a name="set-a-time-limit"></a>Angi en tidsfrist

Følg denne fremgangsmåten hvis den manuelle oppgaven må fullføres innen et bestemt tidspunkt.

> [!NOTE]
> Alternativene du velger i prosedyren, overstyrer alternativene du velger i **Tilordning**- og **Eskalering**-området på siden.

1. Klikk på **Avanserte innstillinger** i ruten til venstre.
2. Merk av for **Angi en tidsgrense for arbeidsflytelementet**.
3. I **Varighet**-feltet angir du når oppgaven må være fullført. Velg ett av følgende alternativer:

    - **Timer** – Angi hvor mange timer det kan gå før oppgaven må være fullført. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi hvor mange dager det kan gå før oppgaven må være fullført. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi hvor mange uker det kan gå før oppgaven må være fullført.
    - **Måneder** – Velg dagen og uken da oppgaven må være fullført. Du vil for eksempel at oppgaven skal fullføres innen fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden da oppgaven må være fullført. Du vil for eksempel at oppgaven skal fullføres innen fredag i den tredje uken i desember.

4. Hvis tidsgrensen overskrides, vil systemet gjøre noe med oppgaven. I listen **Handling** velger du den handlingen som systemet skal utføre.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angi hvilke handlinger som er tilgjengelige for brukeren

Når den manuelle oppgaven tilordnes en bruker, må brukeren utføre en handling med oppgaven. Følg denne fremgangsmåten for å angi hvilke handlinger brukeren kan utføre med oppgaven.

> [!NOTE]
> Handlingene som er tilgjengelige, vil variere avhengig av utformingen av oppgaven.

1. Klikk på **Avanserte innstillinger** i ruten til venstre.
2. Merk av for **Fullført** hvis brukeren skal kunne merke oppgaven som **Fullført**.
3. Merk av for **Avvis** hvis brukeren skal kunne avvise dokumentet som ble sendt.
4. Merk av for **Be om endring** hvis brukeren skal kunne be om endringer av dokumentet som ble sendt.
5. Merk av for **Deleger** hvis brukeren skal kunne tilordne oppgaven til andre brukere.
6. Merk av for **Tilordne på nytt** hvis brukeren skal kunne tilordne oppgaven på nytt til andre brukere i arbeidselementkøen.
7. Merk av for **Frigi** hvis brukeren skal kunne tilordne oppgaven på nytt til arbeidselementkøen. En annen bruker kan deretter fullføre oppgaven.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]