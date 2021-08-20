---
title: Konfigurere automatiserte oppgaver i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene for en automatisert oppgave.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192061
ms.assetid: c0aceb57-b5e6-4ef3-91e7-89a21c9f048a
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cc7097d956b0fabdc8cf16cfb99b065e3e03f21e9cfd56c4b4b91930dbef2b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764389"
---
# <a name="configure-automated-tasks-in-a-workflow"></a>Konfigurere automatiserte oppgaver i en arbeidsflyt

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer egenskapene for en automatisert oppgave.

Når du skal konfigurere en automatisert oppgave i redigeringsprogrammet for arbeidsflyt, høyreklikker du oppgaven og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden. Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den automatiserte oppgaven.

## <a name="name-the-task"></a>Gi navn til oppgaven

Følg denne fremgangsmåten for å sette et navn på den automatiserte oppgaven.

1. Klikk på **Grunnleggende innstillinger** i ruten til venstre.
2. I feltet **Navn** angir du et unikt navn på oppgaven.

## <a name="specify-when-notifications-are-sent"></a>Angi når varslinger skal sendes

Du kan sende meldinger til personer når en automatisert oppgave er kjørt eller avbrutt. Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.

1. I den venstre ruten klikker du **Varslinger**.
2. Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:

    - **Utførelse** – Meldinger blir sendt når oppgaven er kjørt.
    - **Avbrutt** – Meldinger blir sendt når oppgaven er avbrutt.

3. Velg raden for en hendelse du valgte i trinn 2.
4. I tekstfeltet i fanen **Varslingstekst** skriver du inn teksten i meldingen.
5. Hvis du vil tilpasse varslingen, kan du sette inn plassholdere. Plassholdere erstattes med de riktige dataene når varslingen vises til brukerne. Følg denne fremgangsmåten for å sette inn en plassholder:

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
    <td>Brukere som deltar i den gjeldende arbeidsflyten</td>
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]