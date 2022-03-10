---
title: Definere komponentene for en jobb
description: Dette emnet beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e2c9421646dacc5523f40b28b550881dc4b25dd
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068165"
---
# <a name="set-up-the-components-of-a-job"></a>Definere komponentene for en jobb


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen. 

Før du kan opprette jobber, må du definere litt referanseinformasjon. Du kan opprette en jobb med bare ett navn. Ved å inkludere tilleggsinformasjon, for eksempel en jobbtittel, angir du imidlertid standardverdier for stillinger som er knyttet til jobben. Noe av informasjonen du angir kan dessuten brukes til å filtrere kompensasjonsplaner på bestemte jobber. Hvis du vil definere berettigelse som du kan bruke til å filtrere kompensasjonsplaner på en bestemt jobb, bør du sette opp jobbfunksjoner og jobbtyper før du setter opp jobber. Ved å ha disse standardverdiene tilgjengelige, sparer du tid når du legger til stillinger for jobben. 

Noen jobbdetaljer, for eksempel tittel, type og funksjon, er datoeffektive. Hvis du oppretter en jobb i dag, men ikke legger til disse detaljene før senere, og du deretter ser på jobben på opprettelsesdatoen, vises ikke disse detaljene. Derfor bør du opprette noe av denne referanseinformasjon før du trenger den. På denne måten kan du legge til informasjonen for nye jobber når du oppretter dem.

## <a name="job-titles"></a>Jobbtitler
Før du oppretter jobber, må du definere titler for disse jobbene. Stillinger arver jobbtitler fra jobbene som stillingene er knyttet til. 

Vedlikehold jobbtitler ved hjelp av **Titler**-siden, som du kan åpne ved hjelp av funksjonen Søk. På **Titler**-siden skriver du inn titlene du har tenkt å bruke for jobbene.

## <a name="job-types"></a>Jobbtyper
Du bruker jobbtyper til å gruppere lignende jobber i kategorier. Jobbtyper er ikke nødvendige. Men hvis du har tenkt å bruke jobbtyper når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbtyper før du definerer jobber. Noen eksempler på jobbtyper er heltid og deltid, eller lønn og timelønn. Du vedlikeholder jobbtyper ved hjelp av **Jobbtyper**-siden. Angi et navn for jobbtypen og en kort beskrivelse av den på **Jobbtyper**-siden. I feltet **Status, fritatt fra avgift** velger du ett av følgende alternativer for å angi fritaksstatusen fra avgifter Fair Labor Standards Act (FLSA) for jobber som har denne jobbtypen:

-   **Avgiftsfri** – Jobber er fritatt fra overtid under FLSA.
-   **Ikke fritatt fra avgift** – Jobber er ikke fritatt fra overtid under FLSA.
-   **Gjelder ikke** – FLSA-dekning er ikke tilgjengelig.

## <a name="job-family"></a>Jobbserie
En jobbfamilie er en gruppe jobber som omfatter lignende arbeid, og som krever lignende opplæring, kunnskap, kompetanse og ekspertise. En jobbfamilie kan kobles til en jobb i hurtigfanen **Jobbklassifisering** på **Jobber**-siden og i hurtigfanen **Generelt** på **Alle stillinger**-siden. Jobbfamilier kan være brede eller spesifikke, avhengig av forretnings- og rapporteringskravene. Noen eksempler på vide jobbfamilier er **faglært arbeid** og **ufaglært arbeid**. Noen eksempler på bestemte jobbfamilier er **regnskap**, **produksjon** og **salg**.

Vedlikehold jobbfamilier ved hjelp av **Jobbfamilie**-siden, som du kan åpne ved hjelp av funksjonen Søk. På **Jobbfamilie**-siden angir du et unikt navn for familien, og skriver inn en detaljert beskrivelse som du planlegger å bruke til jobbene dine.

## <a name="job-functions"></a>Jobbfunksjoner
Jobbfunksjoner beskriver funksjonskategori på høynivåplan og relaterer avgifter på høyt nivå. Jobbfunksjoner er ikke nødvendige. Du kan bruke jobbfunksjoner sammen med jobbtyper for å filtrere kompensasjonsplaner for bestemte jobber. Du tilordninger jobbfunksjoner og jobbtyper med kompensasjonsplaner ved å definere rettighetsregler på siden **Rettighetsregler**. Du kan deretter knytte et sett med nivåer til kompensasjonsplanen som gjelder en kombinasjon av jobbtype og jobbfunksjon som du har definert gjennom en rettighetsregel. (Disse funksjonene gjelder både faste og variable kompensasjonsplaner.) Jobbfunksjoner er ikke nødvendige, men hvis du har tenkt å bruke jobbfunksjoner når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbfunksjoner før du definerer jobber. Tabellen nedenfor viser noen eksempler på jobbfunksjoner.

| Jobb           | Jobbfunksjon         |
|---------------|----------------------|
| Salgssjef | Mellomleder    |
| Regnskapsfører    | Eksperter        |

Du vedlikeholder jobbfunksjoner ved hjelp av **Jobbfunksjoner**-siden. Angi en ID-kode og en kort beskrivelse av jobbfunksjonen på siden **Jobbfunksjoner**.

## <a name="compensation"></a>Kompensasjon
Hvis du vil tilordne en fast kompensasjonsplan til en ansatt som har en stilling i en jobb, må du angi kompensasjonsnivåer for jobben. **Kompensasjonsnivået** brukes når minimums-, midtpunkt- og maksimumsbeløp er angitt i en kompensasjonsstruktur (kompensasjonsrutenett). Når det opprettes en fast kompensasjonsplan, velges kompensasjonsstrukturen. Kompensasjonsstrukturen omfatter også kompensasjonsnivået. Når du velger en fast kompensasjonsplan for en ansatt, avhenger kompensasjonsnivåene som kan velges, av jobben som den ansattes stilling er knyttet til. Hvis du vil ha mer informasjon om hvordan du konfigurerer kompensasjon, kan du se [Kompensasjonsplaner](hr-compensation-overview.md).

## <a name="job-skills"></a>Jobbkompetanse
Jobbkompetanse beskriver ferdighetene som kreves for å utføre en jobb. Et kompetansenivå må knyttes til hver jobbkompetanse. Kompetansenivåene er brukerdefinert. De angir hvor stor kunnskap eller kompetanse som kreves for ferdigheten. Firmaer kan for eksempel definere numeriske nivåer, for eksempel 1 til og med 5, der **1** indikerer en nybegynner og **5** indikerer en ekspert. Firmaer kan eventuelt sette opp nivåer som er merket **Nybegynner**, **Mellomnivå** eller **Ekspert**. Når kompetansenivået er definert, kan du også angi viktigheten av kompetanse. Hvis en regnskapsfører for eksempel må ha stor kunnskap om Microsoft Excel, kan du opprette en kompetanse med navnet **Excel-kunnskap**. Kompetansenivået kan deretter angis til **Mellomnivå**, og viktigheten kan settes til **Mest**.

Kompetansene som er i en jobb, kan brukes i kompetansesøk. Kompetansesøk kan sammenligne kompetansesettet som kreves for en jobb, og kompetansene som er tilknyttet en arbeider. Deretter kan det bestemme et prosentvis samsvar basert på kompetanse som overlapper hverandre. Hvis du vil lære mer om kompetansesøk, kan du se [Konfigurere kompetanse](hr-develop-skills.md). 

## <a name="job-tasks"></a>Jobboppgaver
Jobboppgaver beskriver de grunnleggende oppgavene som må fullføres av en arbeider i en stilling for jobben. Den samme jobboppgaven kan legges til flere jobber, og til stillinger for jobbene som bruker disse jobboppgavene. Tabellen nedenfor viser noen eksempler på jobboppgaver.

<table>
<thead>
<tr class="header">
<th>Jobb</th>
<th>Jobboppgave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salgssjef</td>
<td><ul>
<li><strong>Ytelsesgjennomgang</strong> – Vurder jobbytelsen til hver enkelt selger.</li>
<li><strong>Fraværsgjennomgang</strong> – Godkjenn eller avvis fraværsforespørsler eller registreringer for hver selger.</li>
</ul></td>
</tr>
<tr class="even">
<td>Regnskapsfører</td>
<td><strong>Finansrapport</strong> – Vis ukentlige finansrapporter til økonomisjef.</td>
</tr>
</tbody>
</table>

Du vedlikeholder jobboppgaver ved hjelp av **Jobboppgaver**-siden. Angi et navn for jobboppgaven og en kort beskrivelse av den på **Jobboppgaver**-siden. Du kan legge inn tilleggsinformasjon i **Merknad**-feltet. Notatene kan oppdateres for en bestemt jobb uten å endre notatene du har angitt her.

## <a name="areas-of-responsibility"></a>Ansvarsområder
Du bruker ansvarsområder for å angi arbeidsrollene, prosessene og produktene som en arbeider som er i en stilling for jobben, har ansvaret for. Et eksempel på et ansvarsområde for en jobb med navnet "Regnskap" kan være "Økonomisk rapportering for produkt A". Du vedlikeholder ansvarsområder ved hjelp av **Ansvarsområder**-siden, som du finner ved hjelp av funksjonen Søk. Angi et navn for ansvaret og en kort beskrivelse av det på **Ansvarsområder**-siden. Du kan legge inn tilleggsinformasjon i **Merknad**-feltet. Notatene kan oppdateres for en bestemt jobb uten å endre notatene du har angitt her.

## <a name="steps-for-creating-a-job"></a>Fremgangsmåter for å opprette en jobb
Se artikkelen [Definere nye jobber](./hr-personnel-define-jobs.md) for trinnvis fremgangsmåte for å opprette en ny jobb. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
