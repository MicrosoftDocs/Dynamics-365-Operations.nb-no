---
title: Konfigurere godkjenningsprosesser i en arbeidsflyt
description: Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen.
author: ChrisGarty
manager: AnnBe
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195643
ms.assetid: f853f57b-83ae-4fb0-a9fa-06ea3fc34fa1
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37a079ee98495a27c1462df32f2973b012069ca8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562819"
---
# <a name="configure-approval-processes-in-a-workflow"></a>Konfigurere godkjenningsprosesser i en arbeidsflyt

[!include [banner](../includes/banner.md)]

Bruk fremgangsmåten nedenfor for å konfigurere egenskapene for godkjenningsprosessen.

Når du skal konfigurere en godkjenningsprosess i redigeringsprogrammet for arbeidsflyt, høyreklikker du godkjenningstrinnet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.

## <a name="name-the-approval-process"></a>Gi navn til godkjenningsprosessen

Bruk fremgangsmåten nedenfor for å sette et navn på godkjenningsprosessen.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på godkjenningsprosessen.

## <a name="specify-when-the-system-automatically-acts-on-the-document"></a>Angi når systemet skal utføre en handling med dokumentet automatisk

Du kan konfigurere systemet slik at det automatisk utfører en handling på dokumenter som oppfyller bestemte betingelser. Systemet kan for eksempel godkjenne reiseregninger med totalsummer som er mindre enn USD 100. Følg denne fremgangsmåten for å angi når systemet utfører en handling på dokumentet.

1. I den venstre ruten klikker du **Automatiske handlinger**.
2. Merk av for **Aktiver automatiske handlinger**.
3. Klikk på **Legg til betingelse**.
4. Angi en betingelse.
5. Angi flere betingelser om nødvendig.
6. Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:

    1. Klikk på **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.
    2. Velg en post i **Valider betingelse**-området i skjemaet.
    3. Klikk på **Test**. Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.
    4. Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.

7. I listen **Autofullføringshandling** velger du handlingen som systemet skal utføre på dokumentet.

## <a name="specify-when-notifications-are-sent"></a>Angi når varslinger skal sendes

Du kan sende meldinger til personer når et dokument er godkjent, avvist, delegert eller videresendt, eller når det er bedt om en endring. Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.

1. I den venstre ruten klikker du **Varslinger**.
2. Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:

    - **Representant** – Når et dokument er tilordnet til en annen bruker for godkjenning.
    - **Videresend** – Når den tilordnede brukeren ikke har gjort noe på et dokument i tildelt tidsrom.
    - **Godkjenn** – Når et dokument er godkjent.
    - **Avvis** – Når et dokument er avvist.
    - **Be om endring** – Når den tilordnede brukeren har bedt om en endring i et dokument som ble sendt.

3. Velg raden for en hendelse du valgte i trinn 2.
4. Klikk på fanen **Varslingstekst**.
5. I tekstboksen angir du teksten for varslingen.
6. Du kan tilpasse teksten ved å sette inn plassholdere som vil bli erstattet med de aktuelle dataene når de vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

    1. Klikk på i tekstboksen der plassholderen skal vises.
    2. Klikk på **Sett inn plassholder**.
    3. I listen som vises, velger du plassholderen du vil sette inn.
    4. Klikk på **Sett inn**.

7. Hvis du vil legge til oversettelser av varslingen, klikker du **Oversettelser**. I skjemaet som vises, gjør du følgende:

    1. Klikk på **Legg til**.
    2. I listen som vises, velger du språket teksten skal angis på.
    3. I tekstboksen **Oversatt tekst** legger du inn teksten.
    4. Hvis du vil tilpasse teksten, kan du sette inn plassholdere.
    5. Klikk på **Lukk**.

8. Klikk på fanen **Mottaker**.
9. Angi hvem varslingene skal sendes til. Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for alternativet før du går til trinn 10.

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
    <td><strong>Deltaker</strong></td>
    <td>Brukere som er tilordnet til en bestemt gruppe eller rolle</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Deltaker</strong>, klikker du <strong>Rollebasert</strong>-fanen.</li>
    <li>I <strong>Type deltaker</strong>-listen velger du typen gruppe eller rolle som varslingene skal sendes til.</li>
    <li>I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som varslingene skal sendes til.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Arbeidsflytbruker</strong></td>
    <td>Brukere som deltar i den gjeldende arbeidsflyten</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Arbeidsflytbruker</strong>, klikker du <strong>Arbeidsflytbruker</strong>-fanen.</li>
    <li>I <strong>Arbeidsflytbruker</strong>-listen velger du en bruker som deltar i arbeidsflyten.</li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><strong>Bruker</strong></td>
    <td>Bestemte brukere</td>
    <td>
    <ol>
    <li>Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-fanen.</li>
    <li>Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

10. Gjenta trinn 3 til 9 for hver hendelse du valgte i trinn 2.

## <a name="specify-a-final-approver"></a> Angi en endelig godkjenner

Du kan angi en endelig godkjenner for scenarier der godkjenneren er personen som sendte dokumentet til godkjenning, og Sperr godkjenning av innsender brukes. Hvis du vil angi en endelig godkjenner, følger du fremgangsmåten nedenfor.

1. I redigeringsprogrammet for arbeidsflyt høyreklikker du godkjenningselementet og velger deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.
2. Klikk på **Avanserte innstillinger** i ruten til venstre.
3. Merk av for **Bruk siste godkjenner**.
4. Velg en bruker som skal være den endelig godkjenneren, fra listen.

## <a name="set-a-time-limit"></a>Angi en tidsfrist

Følg denne fremgangsmåten hvis godkjenningsprosessen må fullføres innen et bestemt tidspunkt.

> [!NOTE]
> Alternativene du velger her, overstyrer alternativene du valgte i områdene **Tildeling** og **Eskalering** i hvert godkjenningstrinn.

1. Klikk på **Avanserte innstillinger** i ruten til venstre.
2. Merk av for **Angi en tidsgrense for arbeidsflyt** **-element**.
3. I **Varighet**-feltet angir du når godkjenningsprosessen må være fullført. Velg ett av følgende alternativer:

    - **Timer** – Angi antall timer godkjenningsprosessen må være fullført innen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Dager** – Angi antall dager godkjenningsprosessen må være fullført innen. Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.
    - **Uker** – Angi antall uker godkjenningsprosessen må være fullført innen.
    - **Måneder** – Velg dagen og uken godkjenningsprosessen må være fullført innen. Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i måneden.
    - **År** – Velg dagen, uken og måneden godkjenningsprosessen må være fullført innen. Det kan for eksempel hende du vil at godkjenningsprosessen skal være fullført fredag i den tredje uken i desember.

4. Hvis tidsgrensen overskrides, vil systemet gjøre noe med dokumentet. I listen **Handling** velger du den handlingen som systemet skal utføre.

## <a name="specify-which-actions-are-available-to-the-user"></a>Angi hvilke handlinger som er tilgjengelige for brukeren

Når et dokument tilordnes en bruker for godkjenning, må brukeren utføre en handling med dokument. Følg denne fremgangsmåten for å angi hvilke handlinger brukeren kan utføre med det sendte dokumentet.

1. Klikk på **Avanserte innstillinger** i ruten til venstre.
2. Merk av for **Godkjenn** hvis brukeren kan godkjenne dokumentet.
3. Merk av for **Avvis** hvis brukeren kan avvise dokumentet.
4. Merk av for **Be om endring** hvis du brukeren kan be om endringer av dokumentet.
5. Merk av for **Representant** hvis brukeren kan tilordne dokumentet til en annen bruker for godkjenning.

> [!NOTE]
> Avmerkingsboksen **Aktiver handlinger fra arbeidslisten i Enterprise Portal** er utgått.

## <a name="configure-the-approval-steps"></a> Konfigurere godkjenningstrinnene

En godkjenningsprosess består av godkjenningstrinn. Fullfør fremgangsmåten nedenfor for å legge til trinn i godkjenningsprosessen og konfigurere trinnene.

1. Dobbeltklikk godkjenningsprosessen i redigeringsprogrammet for arbeidsflyt. Redigeringsprogrammet for arbeidsflyt viser trinnene i godkjenningsprosessen.
2. Hvis du vil legge til et godkjenningstrinn, kan du dra trinnet fra **Arbeidsflytelementer** området til lerretet.
3. Hvis du vil konfigurere et godkjenningstrinn, kan du se [Konfigurere godkjenningstrinn i en arbeidsflyt](configure-approval-step-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]