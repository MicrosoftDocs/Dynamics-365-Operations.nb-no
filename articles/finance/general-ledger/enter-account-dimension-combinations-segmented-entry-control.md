---
title: Angi kombinasjoner av konto og dimensjon (segmentert oppføringskontroll)
description: Denne artikkelen beskriver hvordan du registrerer konto- og dimensjonkombinasjoner eller finanskontoer. Registreringsopplevelsen kalles ofte segmentert oppføringskontroll.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186653"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a>Angi kombinasjoner av konto og dimensjon (segmentert oppføringskontroll)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du registrerer konto- og dimensjonkombinasjoner eller finanskontoer. Registreringsopplevelsen kalles ofte segmentert oppføringskontroll.

Brukere angir kombinasjoner av konto og dimensjon på ulike sider, for eksempel sider for økonomijournaler, budsjettering og posteringsdefinisjoner. De gyldige kombinasjonene av konto og dimensjon avhenger av kontostrukturene som tilordnes finans, og de avanserte reglene som er tilordnet kontostrukturene. Når brukere angir en kombinasjon, kan de skrive inn verdiene manuelt eller bruke en omfattende oppslagsfunksjon. Når du angir feltet, kan du begynne å skrive inn, så søkes det etter verdien og beskrivelsen. Hvis du for eksempel skriver inn 180, søkes det etter alle verdier som begynner med denne nummerkombinasjonen. Eller du kan skrive inn kontant, så søkes det etter en verdi som har en beskrivelse som begynner med kontant. Du kan også bruke jokertegn, som \*kontant eller \*180 for å søke hvis verdien eller beskrivelsen inneholder søkevilkåret. 

Tabellen nedenfor beskriver hurtigtastene som kan brukes når oppslaget er lukket.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Hurtigtast</th>
<th>Handling</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Alt+Pil ned</td>
<td>Åpne oppslaget. Hvis du trykker Alt+Pil ned på nytt, flyttes fokus til segmentene på undermenyen.</td>
</tr>
<tr class="even">
<td><ul>
<li>Enter og Skift+Enter</li>
<li>Skilletegn for kontoplan</li>
<li>Pil høyre og Pil venstre</li>
</ul></td>
<td>Gå til neste eller forrige segment.</td>
</tr>
<tr class="odd">
<td>Kategori</td>
<td>Flytt til neste felt i rutenettet.</td>
</tr>
</tbody>
</table>

Tabellen nedenfor beskriver hurtigtastene som kan brukes når oppslaget er åpent.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Hurtigtast</th>
<th>Handling</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ESC</td>
<td>Lukk oppslaget.</td>
</tr>
<tr class="even">
<td><ul>
<li>Pil opp eller Pil ned</li>
<li>PgUp og PgDn</li>
<li>Home og End</li>
</ul></td>
<td>Flytt til forrige eller neste verdi i listen, til forrige eller neste gruppe med verdier eller til første eller siste element i oppslaget.</td>
</tr>
<tr class="odd">
<td><ul>
<li>Skilletegn for kontoplan</li>
<li>Pil høyre og Pil venstre</li>
</ul></td>
<td>Gå til neste eller forrige segment.</td>
</tr>
<tr class="even">
<td>Kategori</td>
<td>Flytt til neste felt i rutenettet.</td>
</tr>
<tr class="odd">
<td>Alt+W</td>
<td>Veksle mellom <strong>Vis alle</strong> og <strong>Vis gyldig</strong>.</td>
</tr>
</tbody>
</table>





