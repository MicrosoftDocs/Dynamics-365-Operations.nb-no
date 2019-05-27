---
title: Avansert synstaks for filtrering og spørringer
description: Denne artikkelen beskriver alternativene for filtrering og spørringer som er tilgjengelige når du bruker operatoren treff i Filterr-ruten eller rutenettet for kolonnehodefiltre.
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547014"
---
# <a name="advanced-filtering-and-query-syntax"></a>Avansert syntaks for filtrering og spørring

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver alternativene for filtrering og spørringer som er tilgjengelige når du bruker operatoren **treff** i Filterr-ruten eller rutenettet for kolonnehodefiltre.

## <a name="advanced-query-syntax"></a>Avansert spørringssyntaks

<table>
<thead>
<tr>
<th>Syntaks</th>
<th>Tegnbeskrivelse</th>
<th>beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>verdi</em></td>
<td>Er lik verdien som er angitt.</td>
<td>Skriv inn verdien du vil søke etter.</td>
<td><strong>Smith</strong> finner &quot;Smith&quot;.</td>
</tr>
<tr>
<td>!<em>verdi</em> (utropstegn)</td>
<td>Ikke lik verdien som er angitt</td>
<td>Skriv inn et utropstegn foran verdien som skal utelates.</td>
<td><strong>!Smith</strong> finner alle verdier unntatt &quot;Smith&quot;.</td>
</tr>
<tr>
<td><em>fra-verdi</em>..<em>til-verdi</em> (dobbelt punktum)</td>
<td>Mellom de to verdiene som er atskilt med doble punktum</td>
<td>Skriv inn fra-verdien, deretter to punktum og så til-verdien.</td>
<td><strong>1..10</strong> finner alle verdier fra 1 til og med 10. I en streng finner imidlertid felt <strong>A..C</strong> alle verdier som begynner med &quot;A&quot; og &quot;B&quot;, og verdier som er nøyaktig lik &quot;C&quot;. Denne spørringen finner for eksempel ikke &quot;Ca&quot;. Hvis du vil finne alle verdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skriver du inn <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>verdi</em> (dobbelt punktum)</td>
<td>Mindre enn eller lik verdien som er angitt</td>
<td>Skriv inn de to punktumene og deretter verdien.</td>
<td><strong>..1000</strong> finner et hvilket som helst tall som er mindre enn eller lik 1 000, for eksempel &quot;100&quot;, &quot;999,95&quot; og &quot;1 000&quot;.</td>
</tr>
<tr>
<td><em>verdi</em>.. (dobbelt punktum)</td>
<td>Større enn eller lik verdien som er angitt</td>
<td>Skriv inn verdien og deretter to punktumene.</td>
<td><strong>1000..</strong> finner et hvilket som helst tall som er større enn eller lik 1 000, for eksempel &quot;1,000&quot;, &quot;1,000,01&quot;, og &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>verdi</em> (større enn-tegn)</td>
<td>Større enn verdien som er angitt</td>
<td>Skriv inn et større enn-tegn (<strong>&gt;</strong>) og deretter verdien.</td>
<td><strong>&gt;1000</strong> finner et hvilket som helst tall som er større enn 1 000, for eksempel &quot;1000,01&quot;, &quot;20,000&quot; og &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>verdi</em> (mindre enn-tegn)</td>
<td>Mindre enn verdien som er angitt</td>
<td>Skriv inn et mindre enn-tegn (<strong>&lt;</strong>) og deretter verdien.</td>
<td><strong>&lt;1000</strong> finner et hvilket som helst tall som er mindre enn 1 000, for eksempel &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>verdi</em>* (stjerne)</td>
<td>Begynner fra verdien som er angitt</td>
<td>Skriv inn startverdien og deretter en stjerne (<strong>*</strong>).</td>
<td><strong>S*</strong> finner en hvilken som helst streng som begynner med &quot;S&quot;, for eksempel &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>verdi</em> (stjerne)</td>
<td>Slutter med verdien som er angitt</td>
<td>Skriv inn en stjerne og deretter sluttverdien.</td>
<td><strong>*øst</strong> finner en hvilken som helst streng som slutter med &quot;øst&quot;, som i &quot;nordøst&quot; og &quot;sydøst&quot;.</td>
</tr>
<tr>
<td>*<em>verdi</em>* (stjerne)</td>
<td>Inneholder verdien som er angitt</td>
<td>Skriv inn en stjerne, deretter en verdi og så en ny stjerne.</td>
<td><strong>*øs*</strong> finner en hvilken som helst streng som inneholder &quot;øs&quot;, som i &quot;nordøst&quot; og &quot;sørøst&quot;.</td>
</tr>
<tr>
<td>? (spørsmålstegn)</td>
<td>Har ett eller flere ukjente tegn</td>
<td>Skriv inn et spørsmålstegn i posisjonen for det ukjente tegnet i verdien.</td>
<td><strong>Sm?th</strong> finner &quot;Smith&quot; og &quot;Smyth&quot;.</td>
</tr>
<tr>
<td><em>verdi</em>,<em>verdi</em> (komma)</td>
<td>Samsvarer med verdiene som er atskilt med komma</td>
<td>Skriv inn alle kriteriene atskilt med komma.</td>
<td><strong>A, D, F, G</strong> finnner &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;. <strong>10, 20, 30, 100</strong> finner &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>(<span class="code">SQL-setning</span>) (SQL-setning i parenteser)</td>
<td>Samsvarer med en definert spørring</td>
<td>Skriv inn en spørring som et SQL-setning i parenteser.</td>
<td><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></td>
</tr>
<tr>
<td>T</td>
<td>Dagens dato</td>
<td>Skriv inn <strong>T</strong>.</td>
<td><strong>T</strong> samsvarer med dagens dato.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-metode i parenteser)</td>
<td>Samsvare verdien eller verdiområdet som er angitt av parameterne for <strong>SysQueryRangeUtil</strong>-metoden</td>
<td>Skriv inn en <strong>SysQueryRangeUtil</strong>-metode med parametere som angir verdien eller verdiområdet.</td>
<td>
<ol>
<li>Klikk <strong>Kunder</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åpne kundefakturaer</strong>.</li>
<li>Trykk Ctrl+Skift+F3 for å åpne <strong>Forespørsel</strong>-siden.</li>
<li>Klikk <strong>Legg til</strong> i kategorien <strong>Område</strong>.</li>
<li>I <strong>Tabell</strong>-feltet velger du <strong>Åpne kundetransaksjoner</strong>.</li>
<li>I <strong>Felt</strong>-feltet velger du <strong>Forfallsdato</strong>.</li>
<li>I <strong>Kriterier</strong>-feltet angir du <strong>(yearRange(-2,0))</strong>.</li>
<li>Klikk <strong>OK</strong>. Listesiden oppdateres for å vise fakturaene som samsvarer med de angitte kriteriene. Når det gjelder dette bestemte eksemplet, vises fakturaer som forfalt i de to forrige årene.</li>
</ol>
Se tabellen i den neste delen hvis du vil ha mer informasjon om <strong>SysQueryRangeUtil</strong>-datometoder og flere eksempler.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Dato for avanserte spørringer som bruker SysQueryRangeUtil-metoder

<table>
<thead>
<tr>
<th>Metode</th>
<th>Beskrivelse</th>
<th>Eksempel</th>
</tr>
</thead>
<tbody>
<tr>
<td>Dag (_relativeDays=0)</td>
<td>Finn en dato relativ til øktdatoen. Positive verdier angir fremtidige datoer, og negative verdier angir tidligere datoer.</td>
<td>
<ul>
<li><strong>I morgen</strong> – skriv inn <strong>(Day(1))</strong>.</li>
<li><strong>I dag</strong> – skriv inn <strong>(Day(0))</strong>.</li>
<li><strong>I går</strong> – skriv inn <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Finn et datointervall relativt til øktdatoen. Positive verdier angir fremtidige datoer, og negative verdier angir tidligere datoer.</td>
<td>
<ul>
<li><strong>Siste 30 dager</strong> – skriv inn <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Foregående 30 dager og neste 30 dager</strong> – skriv inn <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Finn alle datoer etter den angitte relative datoen.</td>
<td>
<ul>
<li><strong>Mer enn 30 dager fra nå</strong> – angi <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Finne alle dato/klokkeslett-oppføringer etter gjeldende klokkeslett.</td>
<td>
<ul>
<li><strong>Alle fremtidige datoer/klokkeslett</strong> – angi <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Finn alle datoer før den angitte relative datoen.</td>
<td>
<ul>
<li><strong>Mindre enn sju dager fra nå</strong> – angi <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Finne alle dato/klokkeslett-oppføringer før gjeldende klokkeslett.</td>
<td>
<ul>
<li><strong>Alle tidligere datoer/klokkeslett</strong> – angi <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Finn et bestemt datoområde, basert på måneder i forhold til den gjeldende måneden.</td>
<td>
<ul>
<li><strong>Forrige to måneder</strong> – angi <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Neste tre måneder</strong> – angi <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Finn et bestemt datoområde, basert på år i forhold til det gjeldende året.</td>
<td>
<ul>
<li><strong>Neste år</strong> – angi <strong>(YearRange(0,1))</strong>.</li>
<li><strong>Forrige år</strong> – angi <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>
