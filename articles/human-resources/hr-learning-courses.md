---
title: Definer opplæringskurs
description: Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429342"
---
# <a name="set-up-training-courses"></a>Definer opplæringskurs

Personaladministratorer og ledere kan bruke kursfunksjonene til å vedlikeholde opplysningene om opplæringen som tilbys ansatte.

 <a name="set-up-prerequisites"></a> Definer forutsetninger
---------------------

Følgende informasjon er obligatorisk og må defineres før du oppretter kurs.
-   **Kurstyper**

Følgende informasjon er valgfri informasjon som du kan angi for kurs. Hvis du vet at du skal skrive inn denne informasjonen for kursene, bør du få denne informasjonen på plass før du oppretter kursposter.
-   **Kurslokalegrupper**
-   **Kursgrupper**
-   **Kurslokasjoner**
-   **Kurslokaler**
-   **Instruktører**

## <a name="course-types"></a>Kurstyper
Du kan bruke kurstyper til å kategorisere kurs i henhold til strukturen eller innholdet i kurset. Du kan opprette kurstyper på siden **Kurstyper**. Du må velge en kurstype når du oppretter en kurspost.

## <a name="course-setup-type"></a>Oppsettype for kurs
Tabellen nedenfor viser de tre typene oppsett for kurs. Oppsettyper bestemme strukturen for kurset.

<table>
<thead>
<tr class="header">
<th>Oppsettype</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standard</strong></td>
<td>Velg denne typen for kurs som ikke har en daglig agenda. Dette er standard oppsettypen når du oppretter et nytt kurs.</td>
</tr>
<tr class="even">
<td><strong>Agenda</strong></td>
<td>Velg denne typen for å planlegge detaljene for hver dag i et kurs som foregår over flere dager.</td>
</tr>
<tr class="odd">
<td><strong>Agenda + økt</strong></td>
<td>Velg denne typen for mer komplekse kurs. Du kan for eksempel dele agendaen for kurset i spor og økter.
<ul>
<li><strong>Spor</strong> – Spor er spesifikke emneområder for et kurs.</li>
<li><strong>Økter</strong> – Økter deler opp spor og hjelper med å identifisere bestemte prosesser eller teknikker som er relevante for sporet.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kursoppgaver
For hvert kurs kan du for eksempel utføre følgende oppgaver.
- Registrere deltakere
- Spesifisere en registreringsfrist
- Definere minste og største antall deltakere
- Tilordne en kurslokasjon og et klasserom
- Anbefale hoteller for kursdeltakere
- Opprette en kursbeskrivelse som du deretter annonserer i Ansattselvbetjening

  >**Obs!** Du kan slette et kurs bare hvis ingen er registrert for kurset. 

## <a name="course-statuses"></a>Kursstatuser
Tabellen nedenfor viser de mulige kursstatusene og handlingene du kan fullføre når kurset er en bestemt status.

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Handlinger</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Opprettet</strong></td>
<td><ul>
<li>Skriv inn og endre kursinformasjon.</li>
<li>Endre kursstatusen til <strong>Åpen</strong> slik at arbeidere kan melde seg på kurset.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Åpne</strong></td>
<td><ul>
<li>Registrer deltakere på kurset.</li>
<li>Fjern deltakere fra kurset.</li>
<li>Bekreft deltakere for kurset.</li>
<li>Endre kursstatus til<strong> Lukket</strong> eller <strong>Avbrutt</strong>.</li>
<li>Planlegg spørreskjemaer for deltakere med statusen <strong>Bekreftet</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Lukket</strong></td>
<td>Du kan åpne kurset på nytt.</td>
</tr>
<tr class="even">
<td><strong>Avbrutt</strong></td>
<td>Du kan åpne kurset på nytt.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kursdeltakere
Kursdeltakere er arbeidere som deltar på et opplæringskurs eller et arrangement. Du kan bare registrere deltakere for åpne kurs. Det største og minste antallet deltakere som kan meldes på et kurs, er definert på hurtigfanen **Generelt** på siden **Kurs**.

<a name="workflow"></a>Arbeidsflyt
--------

Ansatte som registrerer seg for et kurs via siden **Ansattselvbetjening**, kan rute registreringen gjennom arbeidsflyt for godkjenning. Du kan tilordne en arbeidsflyt til et kurs i hurtigfanen **Generelt** på **Kurs**-siden.





