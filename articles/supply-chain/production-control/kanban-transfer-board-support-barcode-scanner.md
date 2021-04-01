---
title: Støtte for Kanban-overføringskort for strekkodelesere
description: Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d65430d09c293fd5bca032b8b0e88c971d5a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246099"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Støtte for Kanban-overføringskort for strekkodelesere

[!include [banner](../includes/banner.md)]

Kanban-overføringskortet støtter skannerinndata fra et kontrollprogram for strekkodeskanner for å velge, starte, fylle ut og tømme en kanban-jobb.

<a name="registration-modes"></a>Registreringsmoduser
------------------

I hurtigfanen **Skanner - registrering** kan du velge registreringsmodus, som styrer handlingen når du skanner et Kanban-kortnummer eller skriver inn nummeret manuelt i feltet Kanban-kortnummer.

| Angi registreringsmodus | Beskrivelse                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Starte                 | Registrerer en Kanban-overføringsjobb som pågående.                                                 |
| Fullført              | Registrerer en Kanban-overføringsjobb som fullført.                                                   |
| Tom                 | Registrerer materialhåndteringsenheten som et Kanban-kort refererer til, som tomt.              |
| Velg                | Registrerer et Kanban-kortnummer og velger den refererte jobben automatisk i Kanban-listen. |

 
<a name="registration-mode-select"></a>Registreringsmodusen Velg
------------------------

Når du bruker en strekkodeleser til å velge en jobb, endres visningsmodusen for Kanban-kortet. I denne modusen gjelder følgende betingelser:

-   Bare den skannede Kanban-jobben vises.
-   Detaljene om den valgte jobben vises i hurtigfanen **Detaljer**.
-   **Meldinger**-hurtigfanen viser meldinger bare for den valgte jobben.
-   Du kan endre statusen på jobben ved hjelp av funksjonene som er tilgjengelige i handlingsruten. Kanban-overføringskortet fortsetter å vise bare én jobb i denne perioden.
-   Du kan oppdatere informasjonen i listen over jobber manuelt ved å klikke **Oppdater** (SKIFT+F5) i handlingsruten. Når du oppdaterer informasjonen, vises alle resultatene for jobbfilteret på nytt.

## <a name="job-status-and-possible-actions"></a>Jobbstatus og mulige handlinger
Statusen for den valgte jobben og statusen for tilknyttede jobber for hendelses-Kanbaner, bestemmer om du kan behandle jobben ytterligere. Tabellen nedenfor viser informasjon om disse statusene og oppgavene:
-   Statusene som er tilgjengelige for jobber eller for håndteringsenhetene som jobbene refererer til.
-   Hver oppgave du kan utføre for jobben.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Jobbtype</th>
<th>Jobbstatusen eller statusen for håndteringsenheten</th>
<th>Oppdater plukkliste</th>
<th>Starte</th>
<th>Oppdater registrering</th>
<th>Fullført</th>
<th>Tom</th>
<th>Opprett hendelses-Kanbaner</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Overføring</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Ingen tilknyttede jobber, eller tilknyttede jobber er fullført</li>
</ul></td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Ja</td>
<td>Antall</td>
<td>Ja</td>
</tr>
<tr class="even">
<td>Overføring</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Den tilknyttede jobben er ikke fullført</li>
</ul></td>
<td>Ja</td>
<td>Antall</td>
<td>Ja</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="odd">
<td>Overføring</td>
<td>Pågår</td>
<td>Ja</td>
<td>Antall</td>
<td>Ja</td>
<td>Ja</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="even">
<td>Overføring</td>
<td>Fullført</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Ja</td>
<td>Antall</td>
</tr>
<tr class="odd">
<td>Overføring eller behandling</td>
<td>Tom</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="even">
<td>Overføring eller behandling</td>
<td>Finner ikke et Kanban-kort</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="odd">
<td>Overføring eller behandling</td>
<td>Det er funnet et Kanban-kort, men det er ikke tilordnet til en Kanban</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="even">
<td>Behandle</td>
<td><ul>
<li>Ikke planlagt</li>
<li>Klargjort</li>
<li>Pågår</li>
</ul></td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
<tr class="odd">
<td>Behandle</td>
<td>Fullført</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
<td>Antall</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]