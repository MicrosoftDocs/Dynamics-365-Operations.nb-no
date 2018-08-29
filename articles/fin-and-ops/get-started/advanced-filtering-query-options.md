---
title: "Avansert synstaks for filtrering og spørringer"
description: "Denne artikkelen beskriver alternativene for filtrering og spørringer som er tilgjengelige når du bruker operatoren **treff** i Filterr-ruten eller rutenettet for kolonnehodefiltre."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: edff2fba7e231ae52abf7828d55c1fe4841ccd7f
ms.openlocfilehash: 3e7127a9412dcf9324872c06fbf6cc3cf61bf063
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="b7abf-103">Avansert syntaks for filtrering og spørring</span><span class="sxs-lookup"><span data-stu-id="b7abf-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7abf-104">Denne artikkelen beskriver alternativene for filtrering og spørringer som er tilgjengelige når du bruker operatoren **treff** i Filterr-ruten eller rutenettet for kolonnehodefiltre.</span><span class="sxs-lookup"><span data-stu-id="b7abf-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span> 

<a name="advanced-query-syntax"></a><span data-ttu-id="b7abf-105">Avansert spørringssyntaks</span><span class="sxs-lookup"><span data-stu-id="b7abf-105">Advanced query syntax</span></span>
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7abf-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b7abf-106">Syntax</span></span></th>
<th><span data-ttu-id="b7abf-107">Tegnbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7abf-107">Character description</span></span></th>
<th><span data-ttu-id="b7abf-108">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7abf-108">Description</span></span></th>
<th><span data-ttu-id="b7abf-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b7abf-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7abf-110"><em>verdi</em></span><span class="sxs-lookup"><span data-stu-id="b7abf-110"><em>value</em></span></span></td>
<td><span data-ttu-id="b7abf-111">Er lik verdien som er angitt.</span><span class="sxs-lookup"><span data-stu-id="b7abf-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-112">Skriv inn verdien du vil søke etter.</span><span class="sxs-lookup"><span data-stu-id="b7abf-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="b7abf-113"><strong>Smith</strong> finner &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-114">!<em>verdi</em> (utropstegn)</span><span class="sxs-lookup"><span data-stu-id="b7abf-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="b7abf-115">Ikke lik verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-116">Skriv inn et utropstegn foran verdien som skal utelates.</span><span class="sxs-lookup"><span data-stu-id="b7abf-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="b7abf-117"><strong>!Smith</strong> finner alle verdier unntatt &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-118"><em>fra-verdi</em>..<em>til-verdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="b7abf-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="b7abf-119">Mellom de to verdiene som er atskilt med doble punktum</span><span class="sxs-lookup"><span data-stu-id="b7abf-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="b7abf-120">Skriv inn fra-verdien, deretter to punktum og så til-verdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="b7abf-121"><strong>1..10</strong> finner alle verdier fra 1 til og med 10.</span><span class="sxs-lookup"><span data-stu-id="b7abf-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="b7abf-122">I en streng finner imidlertid felt <strong>A..C</strong> alle verdier som begynner med &quot;A&quot; og &quot;B&quot;, og verdier som er nøyaktig lik &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="b7abf-123">Denne spørringen finner for eksempel ikke &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-123">For example, this query won&#39;t find &quot;Ca&quot;.</span></span> <span data-ttu-id="b7abf-124">Hvis du vil finne alle verdier fra &quot;A<em>&quot; til og med &quot;C</em>&quot;, skriver du inn <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-125">..<em>verdi</em> (dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="b7abf-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="b7abf-126">Mindre enn eller lik verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-127">Skriv inn de to punktumene og deretter verdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="b7abf-128"><strong>..1000</strong> finner et hvilket som helst tall som er mindre enn eller lik 1 000, for eksempel &quot;100&quot;, &quot;999,95&quot; og &quot;1 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-129"><em>verdi</em>..</span><span class="sxs-lookup"><span data-stu-id="b7abf-129"><em>value</em>..</span></span> <span data-ttu-id="b7abf-130">(dobbelt punktum)</span><span class="sxs-lookup"><span data-stu-id="b7abf-130">(double period)</span></span></td>
<td><span data-ttu-id="b7abf-131">Større enn eller lik verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-132">Skriv inn verdien og deretter to punktumene.</span><span class="sxs-lookup"><span data-stu-id="b7abf-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="b7abf-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="b7abf-133"><strong>1000..</strong></span></span> <span data-ttu-id="b7abf-134">finner et hvilket som helst tall som er større enn eller lik 1 000, for eksempel &quot;1,000&quot;, &quot;1,000,01&quot;, og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-135">&gt;<em>verdi</em> (større enn-tegn)</span><span class="sxs-lookup"><span data-stu-id="b7abf-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="b7abf-136">Større enn verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-137">Skriv inn et større enn-tegn (<strong>&gt;</strong>) og deretter verdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="b7abf-138"><strong>&gt;1000</strong> finner et hvilket som helst tall som er større enn 1 000, for eksempel &quot;1000,01&quot;, &quot;20,000&quot; og &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-139">&lt;<em>verdi</em> (mindre enn-tegn)</span><span class="sxs-lookup"><span data-stu-id="b7abf-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="b7abf-140">Mindre enn verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-141">Skriv inn et mindre enn-tegn (<strong>&lt;</strong>) og deretter verdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="b7abf-142"><strong>&lt;1000</strong> finner et hvilket som helst tall som er mindre enn 1 000, for eksempel &quot;999,99&quot;, &quot;1&quot; og &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-143"><em>verdi</em>\* (stjerne)</span><span class="sxs-lookup"><span data-stu-id="b7abf-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="b7abf-144">Begynner fra verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-145">Skriv inn startverdien og deretter en stjerne (<strong><em></strong>).</span><span class="sxs-lookup"><span data-stu-id="b7abf-145">Type the starting value and then an asterisk (<strong><em></strong>).</span></span></td>
<td><span data-ttu-id="b7abf-146"><strong>S</em></strong> finner en hvilken som helst streng som begynner med &quot;S&quot;, som i &quot;Stockholm&quot;, &quot;Sydney&quot; og &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-146"><strong>S</em></strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-147"><em><em>verdi</em> (stjerne)</span><span class="sxs-lookup"><span data-stu-id="b7abf-147"><em><em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="b7abf-148">Slutter med verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-149">Skriv inn en stjerne og deretter sluttverdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="b7abf-150"><strong></em>øst</strong> finner en hvilken som helst streng som slutter med &quot;øst&quot;, som i &quot;nordøst&quot; og &quot;sydøst&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-150"><strong></em>east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-151"><em><em>verdi</em></em> (stjerne)</span><span class="sxs-lookup"><span data-stu-id="b7abf-151"><em><em>value</em></em> (asterisk)</span></span></td>
<td><span data-ttu-id="b7abf-152">Inneholder verdien som er angitt</span><span class="sxs-lookup"><span data-stu-id="b7abf-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="b7abf-153">Skriv inn en stjerne, deretter en verdi og så en ny stjerne.</span><span class="sxs-lookup"><span data-stu-id="b7abf-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="b7abf-154"><strong><em>øs</em></strong> finner en hvilken som helst streng som inneholder &quot;øs&quot;, som i &quot;nordøst&quot; og &quot;sørøst&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-154"><strong><em>th</em></strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-155">?</span><span class="sxs-lookup"><span data-stu-id="b7abf-155">?</span></span> <span data-ttu-id="b7abf-156">(spørsmålstegn)</span><span class="sxs-lookup"><span data-stu-id="b7abf-156">(question mark)</span></span></td>
<td><span data-ttu-id="b7abf-157">Har ett eller flere ukjente tegn</span><span class="sxs-lookup"><span data-stu-id="b7abf-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="b7abf-158">Skriv inn et spørsmålstegn i posisjonen for det ukjente tegnet i verdien.</span><span class="sxs-lookup"><span data-stu-id="b7abf-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="b7abf-159"><strong>Sm?th</strong> finner &quot;Smith&quot; og &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-160"><em>verdi</em>,<em>verdi</em> (komma)</span><span class="sxs-lookup"><span data-stu-id="b7abf-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="b7abf-161">Samsvarer med verdiene som er atskilt med komma</span><span class="sxs-lookup"><span data-stu-id="b7abf-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="b7abf-162">Skriv inn alle kriteriene atskilt med komma.</span><span class="sxs-lookup"><span data-stu-id="b7abf-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="b7abf-163"><strong>A, D, F, G</strong> finnner &quot;A&quot;, &quot;D&quot;, &quot;F&quot; og &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="b7abf-164"><strong>10, 20, 30, 100</strong> finner &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="b7abf-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-165">(<span class="code">SQL-setning</span>) (SQL-setning i parenteser)</span><span class="sxs-lookup"><span data-stu-id="b7abf-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="b7abf-166">Samsvarer med en definert spørring</span><span class="sxs-lookup"><span data-stu-id="b7abf-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="b7abf-167">Skriv inn en spørring som et SQL-setning i parenteser.</span><span class="sxs-lookup"><span data-stu-id="b7abf-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="b7abf-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="b7abf-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-169">T</span><span class="sxs-lookup"><span data-stu-id="b7abf-169">T</span></span></td>
<td><span data-ttu-id="b7abf-170">Dagens dato</span><span class="sxs-lookup"><span data-stu-id="b7abf-170">Today&#39;s date</span></span></td>
<td><span data-ttu-id="b7abf-171">Skriv inn <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="b7abf-172"><strong>T</strong> samsvarer med dagens dato.</span><span class="sxs-lookup"><span data-stu-id="b7abf-172"><strong>T</strong> matches today&#39;s date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-metode i parenteser)</span><span class="sxs-lookup"><span data-stu-id="b7abf-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="b7abf-174">Samsvare verdien eller verdiområdet som er angitt av parameterne for <strong>SysQueryRangeUtil</strong>-metoden</span><span class="sxs-lookup"><span data-stu-id="b7abf-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="b7abf-175">Skriv inn en <strong>SysQueryRangeUtil</strong>-metode med parametere som angir verdien eller verdiområdet.</span><span class="sxs-lookup"><span data-stu-id="b7abf-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7abf-176">Klikk <strong>Kunder</strong> &gt; <strong>Fakturaer</strong> &gt; <strong>Åpne kundefakturaer</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-177">Trykk Ctrl+Skift+F3 for å åpne <strong>Forespørsel</strong>-siden.</span><span class="sxs-lookup"><span data-stu-id="b7abf-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="b7abf-178">Klikk <strong>Legg til</strong> i kategorien <strong>Område</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-179">I <strong>Tabell</strong>-feltet velger du <strong>Åpne kundetransaksjoner</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-180">I <strong>Felt</strong>-feltet velger du <strong>Forfallsdato</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-181">I <strong>Kriterier</strong>-feltet angir du <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-182">Klikk <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="b7abf-183">Listesiden oppdateres for å vise fakturaene som samsvarer med de angitte kriteriene.</span><span class="sxs-lookup"><span data-stu-id="b7abf-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="b7abf-184">Når det gjelder dette bestemte eksemplet, vises fakturaer som forfalt i de to forrige årene.</span><span class="sxs-lookup"><span data-stu-id="b7abf-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="b7abf-185">Se tabellen i den neste delen hvis du vil ha mer informasjon om <strong>SysQueryRangeUtil</strong>-datometoder og flere eksempler.</span><span class="sxs-lookup"><span data-stu-id="b7abf-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="b7abf-186">Dato for avanserte spørringer som bruker SysQueryRangeUtil-metoder</span><span class="sxs-lookup"><span data-stu-id="b7abf-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7abf-187">Metode</span><span class="sxs-lookup"><span data-stu-id="b7abf-187">Method</span></span></th>
<th><span data-ttu-id="b7abf-188">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b7abf-188">Description</span></span></th>
<th><span data-ttu-id="b7abf-189">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b7abf-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7abf-190">Dag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="b7abf-191">Finn en dato relativ til øktdatoen.</span><span class="sxs-lookup"><span data-stu-id="b7abf-191">Find a date relative to the session date.</span></span> <span data-ttu-id="b7abf-192">Positive verdier angir fremtidige datoer, og negative verdier angir tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="b7abf-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-193"><strong>I morgen</strong> – skriv inn <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-194"><strong>I dag</strong> – skriv inn <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-195"><strong>I går</strong> – skriv inn <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="b7abf-197">Finn et datointervall relativt til øktdatoen.</span><span class="sxs-lookup"><span data-stu-id="b7abf-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="b7abf-198">Positive verdier angir fremtidige datoer, og negative verdier angir tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="b7abf-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-199"><strong>Siste 30 dager</strong> – skriv inn <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-200"><strong>Foregående 30 dager og neste 30 dager</strong> – skriv inn <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="b7abf-202">Finn alle datoer etter den angitte relative datoen.</span><span class="sxs-lookup"><span data-stu-id="b7abf-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-203"><strong>Mer enn 30 dager fra nå</strong> – angi <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="b7abf-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="b7abf-205">Finne alle dato/klokkeslett-oppføringer etter gjeldende klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b7abf-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-206"><strong>Alle fremtidige datoer/klokkeslett</strong> – angi <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="b7abf-208">Finn alle datoer før den angitte relative datoen.</span><span class="sxs-lookup"><span data-stu-id="b7abf-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-209"><strong>Mindre enn sju dager fra nå</strong> – angi <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="b7abf-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="b7abf-211">Finne alle dato/klokkeslett-oppføringer før gjeldende klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b7abf-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-212"><strong>Alle tidligere datoer/klokkeslett</strong> – angi <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7abf-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="b7abf-214">Finn et bestemt datoområde, basert på måneder i forhold til den gjeldende måneden.</span><span class="sxs-lookup"><span data-stu-id="b7abf-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-215"><strong>Forrige to måneder</strong> – angi <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-216"><strong>Neste tre måneder</strong> – angi <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7abf-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="b7abf-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="b7abf-218">Finn et bestemt datoområde, basert på år i forhold til det gjeldende året.</span><span class="sxs-lookup"><span data-stu-id="b7abf-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="b7abf-219"><strong>Neste år</strong> – angi <strong>(YearRange(0,1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="b7abf-220"><strong>Forrige år</strong> – angi <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7abf-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






