---
title: Definere komponentene for en jobb
description: Denne artikkelen beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: anbichse
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88dc3cec4880fdcb4d4f8d54b03037f738d2a57a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056575"
---
# <a name="set-up-the-components-of-a-job"></a>Definere komponentene for en jobb

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver de grunnleggende elementene som en jobb kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen. 

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

## <a name="job-functions"></a>Jobbfunksjoner
Jobbfunksjoner beskriver funksjonskategori på høynivåplan og relaterer avgifter på høyt nivå. Jobbfunksjoner er ikke nødvendige. Du kan bruke jobbfunksjoner sammen med jobbtyper for å filtrere kompensasjonsplaner for bestemte jobber. Du tilordninger jobbfunksjoner og jobbtyper med kompensasjonsplaner ved å definere rettighetsregler på siden **Rettighetsregler**. Du kan deretter knytte et sett med nivåer til kompensasjonsplanen som gjelder en kombinasjon av jobbtype og jobbfunksjon som du har definert gjennom en rettighetsregel. (Disse funksjonene gjelder både faste og variable kompensasjonsplaner.) Jobbfunksjoner er ikke nødvendige, men hvis du har tenkt å bruke jobbfunksjoner når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbfunksjoner før du definerer jobber. Tabellen nedenfor viser noen eksempler på jobbfunksjoner.

| Jobb           | Jobbfunksjon         |
|---------------|----------------------|
| Salgssjef | Mellomleder    |
| Regnskapsfører    | Eksperter        |

Du vedlikeholder jobbfunksjoner ved hjelp av **Jobbfunksjoner**-siden. Angi en ID-kode og en kort beskrivelse av jobbfunksjonen på siden **Jobbfunksjoner**.

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