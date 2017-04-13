---
title: Konfigurere komponenter av en jobb
description: "Dette emnet beskriver de grunnleggende elementene at et prosjekt kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Konfigurere komponenter av en jobb

Dette emnet beskriver de grunnleggende elementene at et prosjekt kan inneholde, og gir eksempler på hvordan du kan bruke disse elementene i organisasjonen. 

Før du kan opprette jobber, må du definere noen referanseinformasjon. Du kan opprette en jobb med bare et navn. Imidlertid ved å inkludere tilleggsinformasjon, for eksempel en tittel, angi standardverdier for stillinger som er knyttet til jobben. Noe av informasjonen du angir kan dessuten brukes til å filtrere kompensasjonsplaner på bestemte jobber. Hvis du vil definere berettigelse som du kan bruke til å filtrere kompensasjonsplaner på en bestemt jobb, bør du sette opp jobbfunksjoner og jobbtyper før du setter opp jobber. Ved å la disse standardverdiene som er tilgjengelige, sparer du tid når du legger til stillinger for jobben. 

Noen Jobbdetaljer, for eksempel tittel, type og funksjon, er dato-effektiv. Hvis du oppretter en jobb i dag, men ikke Legg til disse detaljene til senere, og du deretter ser på jobb på opprettelsesdatoen, vises ikke disse detaljene. Derfor bør du opprette noen av denne informasjon før du trenger den. På denne måten kan du legge informasjonen til nye jobber når du oppretter dem..

## <a name="job-titles"></a>Stillingsbetegnelser
Før du oppretter jobber, må du definere titler for disse jobbene. Stillinger arver jobbtitler fra jobbene som stillingene er knyttet til. 

Oppretthold jobbtitler ved hjelp av den **titler** side, som du kan åpne ved hjelp av funksjonen Søk. På den ** titler ** side, Skriv inn titlene som du har tenkt å bruke for jobbene.

## <a name="job-types"></a>Jobbtyper
Du kan bruke jobbtyper til å gruppere lignende jobber i kategorier. Jobbtyper er ikke nødvendig. Men hvis du har tenkt å bruke jobbtyper når du definerer rettighetsregler for kompensasjonsstyring, bør du definere jobbtyper før du definerer jobber. Noen eksempler på jobbtyper er heltid og deltid, eller betale lønn og per time. Du opprettholder jobbtyper ved hjelp av den **jobb typer** siden. På den **jobb typer** side, skriver du inn et navn og en kort beskrivelse av jobbtypen. I den **Avgiftsfri status**, velger du ett av følgende alternativer for å angi rettferdig arbeidskraft Standards Act (FLSA) fritatt status for jobber som har denne jobbtypen:

-   **Exempt** – jobber er fritatt fra overtid under FLSA.
-   **Ikke-fritatt** – jobber ikke fritatt fra overtid under FLSA.
-   **Gjelder ikke** – FLSA dekning er ikke tilgjengelig.

## <a name="job-functions"></a>Jobbfunksjoner
Jobben knutepunkter beskrive på høyt nivå, funksjonelle kategorier og relatere avgifter på høyt nivå. Jobbfunksjoner er ikke nødvendig. Du kan bruke jobbfunksjoner sammen med jobbtyper, til å filtrere kompensasjonsplaner på bestemte jobber. Du tilordninger jobbfunksjoner og jobbtyper med kompensasjonsplaner ved å definere rettighetsregler i den **rettighetsregler** siden. Du kan deretter knytte et sett med nivåer til en kompensasjonsplanen som gjelder den bestemte kombinasjonen av jobbtype og jobbfunksjon som du har definert gjennom en rettighetsregel. (Disse funksjonene gjelder både faste kompensasjonsplaner og variable kompensasjonsplaner.) Imidlertid Hvis du planlegger å bruke jobbfunksjoner når du setter opp rettighetsregler for kompensasjonsstyring, bør du konfigurere jobbfunksjoner før du setter opp jobber. Tabellen nedenfor viser noen eksempler på jobbfunksjoner.

| Jobb           | Jobbfunksjon         |
|---------------|----------------------|
| Salgssjef | Mellomstor nivå Manager    |
| Regnskapsfører    | Teknikere        |

Du opprettholder jobbfunksjoner ved hjelp av den **jobbfunksjoner** siden. På den **jobbfunksjoner** side, angir du en kode-ID og en kort beskrivelse av jobbfunksjonen.

## <a name="job-tasks"></a>Jobboppgaver
Prosjektoppgaver beskriver de grunnleggende oppgavene som må fullføre en arbeider som er i en posisjon for en jobb. Samme prosjektoppgaven kan du legge til flere jobber og stillinger for jobbene som bruker disse prosjektoppgavene. Tabellen nedenfor viser noen eksempler på prosjektoppgaver.

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
<li><strong>PERF-gjennomgang</strong> – gå gjennom arbeidsprestasjon for hver selger.</li>
<li><strong>ABS-gjennomgang</strong> – Godkjenn eller Avvis fraværsforespørsler eller registreringer for hver selger.</li>
</ul></td>
</tr>
<tr class="even">
<td>Regnskapsfører</td>
<td><strong>FINSK-rapport</strong> – presentere ukentlige økonomiske rapporter til økonomisjef.</td>
</tr>
</tbody>
</table>

Du opprettholder prosjektoppgaver ved hjelp av den **prosjektoppgavene** siden. På den **prosjektoppgavene** side, skriver du inn et navn og en beskrivelse for prosjektoppgaven. I den **notat** -felt, kan du eventuelt angi tilleggsinformasjon. Notatene kan oppdateres for et bestemt prosjekt uten å endre notatene du har angitt her.

## <a name="areas-of-responsibility"></a>Ansvarsområder
Du bruker ansvarsområder til å angi arbeidsroller, prosesser og produkter som en arbeider som er i en posisjon for en jobb som er ansvarlig for. For eksempel, for et prosjekt som heter "Regnskapsfører", kanskje én ansvarsområdet "Økonomisk rapportering for produkt A." Du opprettholder ansvarsområder ved hjelp av den **ansvarsområder** side, som du finner ved hjelp av funksjonen Søk. På den **ansvarsområder** side, skriver du inn et navn og en beskrivelse av ansvarsområdet. I den **notat** -felt, kan du eventuelt angi tilleggsinformasjon. Notatene kan oppdateres for et bestemt prosjekt uten å endre notatene du har angitt her.


