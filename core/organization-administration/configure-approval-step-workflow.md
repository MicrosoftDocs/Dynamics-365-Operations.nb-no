---
title: Konfigurere et godkjenningstrinn i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene for et godkjenningstrinn.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 052cec3010c0d5ecbb9ed341fb23d0ec64682467
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="configure-an-approval-step-in-a-workflow"></a>Konfigurere et godkjenningstrinn i en arbeidsflyt

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du konfigurerer egenskapene for et godkjenningstrinn.

Når du skal konfigurere et godkjenningstrinn i redigeringsprogrammet for arbeidsflyt, høyreklikker du godkjenningstrinnet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningstrinnet.

## <a name="name-the-step"></a>Gi navn til trinnet
Følg denne fremgangsmåten for å sette et navn på godkjenningstrinnet.

1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  I feltet **Navn** angir du et unikt navn på godkjenningstrinnet.

## <a name="enter-a-subject-line-and-instructions"></a>Legg inn en emnelinje og instruksjoner
Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til godkjenningstrinnet. Hvis du for eksempel konfigurerer et godkjenningstrinn for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til trinnet, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden. Emnelinjen vises i en meldingslinje øverst på siden. Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene. Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.

1.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
2.  I **Emne for arbeidselement**-feltet angir du emnelinjen.
3.  Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:
    1.  I tekstboksen klikker du der plassholderen skal vises.
    2.  Klikk **Sett inn plassholder**.
    3.  I listen som vises, velger du plassholderen du vil sette inn.
    4.  Klikk **Sett inn**.

4.  Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:
    1.  Klikk **Oversettelser**.
    2.  På siden som vises, klikker du **Legg til**.
    3.  I listen som vises, velger du språket teksten angis på.
    4.  I **Oversatt tekst**-feltet legger du inn teksten.
    5.  Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.
    6.  Klikk **Lukk**.

5.  I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.
6.  Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:
    1.  I tekstboksen klikker du der plassholderen skal vises.
    2.  Klikk **Sett inn plassholder**.
    3.  I listen som vises, velger du plassholderen du vil sette inn.
    4.  Klikk **Sett inn**.

7.  Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:
    1.  Klikk **Oversettelser**.
    2.  På siden som vises, klikker du **Legg til**.
    3.  I listen som vises, velger du språket teksten angis på.
    4.  I **Oversatt tekst**-feltet legger du inn teksten.
    5.  Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.
    6.  Klikk **Lukk**.

## <a name="assign-the-approval-step"></a>Tildele godkjenningstrinnet
Følg denne fremgangsmåten for å angi hvem godkjenningstrinnet skal tildeles.

1.  I den venstre ruten klikker du **Tilordning**.
2.  I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Alternativ</th>
    <th>Brukere som godkjenningstrinnet er tilordnet til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Deltaker</td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td><ol>
    <li>Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som trinnet skal tilordnes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som trinnet skal tilordnes til.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som trinnet skal tilordnes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som trinnet kan tilordnes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:
    <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol></li>
    <li>I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som trinnet skal tilordnes til:
    <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Trinnet tilordnes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Trinnet tilordnes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Trinnet tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td><ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Bruker</td>
    <td>Bestemte Microsoft Dynamics 365 for Operations-brukere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Dynamics 365 for Operations-brukere. Velg brukerne du vil tilordne trinnet til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

3.  I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å utføre handlinger på eller svare på dokumenter som kommer til godkjenningstrinnet. Velg ett av følgende alternativer:
    -   **Timer** – Angi antallet timer som brukeren har til å svare. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    -   **Dager** – Angi antallet dager som brukeren har til å svare. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    -   **Uker** – Angi antallet uker som brukeren har til å svare.
    -   **Måneder** – Velg dagen og uken som brukeren må svare innen. Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i måneden.
    -   **År** – Velg dagen, uken og måneden som brukeren må svare innen. Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i desember.

    Hvis brukeren ikke gjør noe med dokumentet innenfor den tillatte tiden, er dokumentet forfalt. Et dokument som er forfalt, videresendes, basert på alternativene du velger i **Eskalering**-området på siden.
4.  Hvis du har tilordnet godkjenningstrinnet til flere brukere eller en gruppe brukere i **Fullføringspolicy**-kategorien, velger du ett av følgende alternativer:
    -   **Én enkelt godkjenner** – Handlingen som utføres på dokumentet, bestemmes av den første personen som svarer. Erik har for eksempel sendt en reiseregning på NOK 15 000. Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn. Hvis Jorunn er den første personen som svarer på dokumentet, brukes handlingen hun bestemmer seg for, på dokumentet. Hvis Jorunn avviser dokumentet, avvises det og sendes tilbake til Erik. Hvis Jorunn godkjenner dokumentet, sendes det til Karen for godkjenning. ![Arbeidsflyt som har en godkjenningsprosess](./media/workflow_multipleusersinstep.gif)
    -   **Flertallet av godkjennere** – Handlingen som skal brukes på dokumentet, fastsettes når de fleste av godkjennerne svarer. Erik har for eksempel sendt en reiseregning på NOK 15 000. Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn. Hvis Jorunn og Johanne er de første to godkjennerne som svarer, utføres handlingen de gjør, på dokumentet.
        -   Hvis Jorunn godkjenner dokumentet, men Johanne avviser det, avvises dokumentet og det sendes tilbake til Erik.
        -   Hvis både Jorunn og Johanne godkjenner dokumentet, sendes det til Karen til godkjenning.
    -   **Prosent av godkjennere** – Handlingen som brukes på dokumentet, bestemmes når en bestemt prosent av godkjennerne svarer. Erik har for eksempel sendt en reiseregning på NOK 15 000. Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn, og du har angitt **50** som prosent. Hvis Jorunn og Johanne er de første to godkjennerne som svarer, brukes handlingen som de gjør, på dokumentet fordi de oppfyller kravene til 50 prosent av godkjennere.
        -   Hvis Jorunn godkjenner dokumentet, men Johanne avviser det, avvises dokumentet og det sendes tilbake til Erik.
        -   Hvis både Jorunn og Johanne godkjenner dokumentet, sendes det til Karen til godkjenning.
    -   **Alle godkjennere** – Alle godkjennerne må godkjenne dokumentet. Ellers kan ikke arbeidsflyten fortsette. Erik har for eksempel sendt en reiseregning på NOK 15 000. Reiseregningen er nå tilordnet Jorunn, Johanne og Bjørn. Hvis Jorunn og Johanne godkjenner dokumentet, men Bjørn avviser det, avvises dokumentet og det sendes tilbake til Erik. Hvis Jorunn, Johanne og Bjørn godkjenner dokumentet, sendes det til Karen til godkjenning.

## <a name="specify-when-the-approval-step-is-required"></a>Angi når godkjenningstrinnet er nødvendig
Du kan angi når godkjenningstrinnet er nødvendig. Godkjenningstrinnet kan alltid være nødvendig, eller det kan bare være nødvendig hvis bestemte betingelser er oppfylt.

### <a name="the-approval-step-is-always-required"></a>Godkjenningstrinnet er alltid nødvendig

Følg disse trinnene hvis godkjenningstrinnet alltid er nødvendig.

1.  I den venstre ruten klikker du **Betingelse**.
2.  Velg alternativet **Kjør alltid dette trinnet**.

### <a name="the-approval-step-is-required-in-specific-conditions"></a>Godkjenningstrinnet er nødvendig ved bestemte betingelser

Godkjenningstrinnet du konfigurerer, kan være nødvendig bare hvis bestemte betingelser er oppfylt. Hvis du for eksempel konfigurerer et godkjenningstrinn for en arbeidsflyt for innkjøpsrekvisisjon, vil du at godkjenningstrinnet bare skal forekomme hvis beløpet i innkjøpsrekvisisjonen er mer enn NOK 10 000. Følg disse trinnene for å angi når godkjenningstrinnet er nødvendig.

1.  I den venstre ruten klikker du **Betingelse**.
2.  Velg alternativet **Kjør bare dette trinnet når følgende betingelse er oppfylt**.
3.  Angi en betingelse.
4.  Angi eventuelle ekstra betingelser som kreves.
5.  Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:
    1.  Klikk **Test**.
    2.  På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post.
    3.  Klikk **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4.  Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.

## <a name="specify-what-happens-when-the-document-is-overdue"></a>Angi hva som skjer når dokumentet er forfalt
Hvis en bruker ikke gjør noe med et dokument innenfor den tillatte tiden, er dokumentet forfalt. Et dokument som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker for godkjenning. Følg denne fremgangsmåten for å videresende dokumentet hvis det er forfalt.

1.  I den venstre ruten klikker du **Eskalering**.
2.  Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane. Systemet tilordner automatisk dokumentet til brukerne som er oppført i videresendingsbanen. Tabellen nedenfor er et eksempel på en videresendingsbane.
    | Sekvens | Videresendingsbane      |
    |----------|----------------------|
    | 1        | Tilordne til: Doris     |
    | 2        | Tilordne til: Elin      |
    | 3        | Endelig handling: Avvis |

    I dette eksempelet tilordnes det forfalte dokumentet til Doris. Hvis Doris ikke svarer innenfor det tillatte tidsrommet, tilordnes dokumentet til Elin. Hvis Elin ikke svarer innenfor det tillatte tidsrommet, avvises dokumentet.
3.  Klikk **Legg til videresending** for å legge til en bruker i videresendingsbanen. I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 4.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Alternativ</th>
    <th>Brukere som dokumentet videresendes til</th>
    <th>Tilleggstrinn</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Hierarki</td>
    <td>Brukere i et bestemt organisasjonshierarki</td>
    <td><ol>
    <li>Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som dokumentet videresendes til.</li>
    <li>Systemet må hente et område med brukernavn fra hierarkiet. Disse navnene representerer brukere som dokumentet kan videresendes til. Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:
    <ol>
    <li>Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</li>
    <li>Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>. Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</li>
    </ol></li>
    <li>I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som dokumentet skal videresendes til:
    <ul>
    <li><strong>Tilordne til alle hentede brukere</strong> – Dokumentet videresendes til alle brukere i området.</li>
    <li><strong>Bare tilordne til den siste hentede brukeren</strong> – Dokumentet videresendes bare til den siste brukeren i området.</li>
    <li><strong>Utelat brukere med følgende vilkår</strong> – Dokumentet videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår. Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Arbeidsflytbruker</td>
    <td>Brukere i den gjeldende arbeidsflyten</td>
    <td><ul>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td>Bruker</td>
    <td>Bestemte Dynamics 365 for Operations-brukere</td>
    <td><ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</li>
    <li><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Dynamics 365 for Operations-brukere. Velg brukerne du vil videresende dokumentet til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å utføre handlinger på eller svare på dokumenter. Velg ett av følgende alternativer:
    -   **Timer** – Angi antallet timer som brukeren har til å svare. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    -   **Dager** – Angi antallet dager som brukeren har til å svare. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    -   **Uker** – Angi antallet uker som brukeren har til å svare.
    -   **Måneder** – Velg dagen og uken som brukeren må svare innen. Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i måneden.
    -   **År** – Velg dagen, uken og måneden som brukeren må svare innen. Det kan for eksempel hende at du vil at brukeren skal svare innen fredag i den tredje uken i desember.

5.  Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen. Du kan endre rekkefølgen på brukerne.
6.  Hvis brukerne i videresendingsbanen ikke svarer innen tidsfristen, vil systemet automatisk utføre en handling med dokumentet. Hvis du vil angi handlingen systemet skal utføre, merker du **Handling**-raden, og velger deretter en handling i kategorien **Avslutt handling**.





