---
title: "Angi kombinasjoner av konto og dimensjon (segmentert oppføringskontroll)"
description: "Denne artikkelen beskriver hvordan du registrerer konto- og dimensjonkombinasjoner eller finanskontoer. Registreringsopplevelsen kalles ofte segmentert oppføringskontroll."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 610b21069d9f13a511f8017d0069fda0371abf10
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="16516-104">Angi kombinasjoner av konto og dimensjon (segmentert oppføringskontroll)</span><span class="sxs-lookup"><span data-stu-id="16516-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="16516-105">Denne artikkelen beskriver hvordan du registrerer konto- og dimensjonkombinasjoner eller finanskontoer.</span><span class="sxs-lookup"><span data-stu-id="16516-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="16516-106">Registreringsopplevelsen kalles ofte segmentert oppføringskontroll.</span><span class="sxs-lookup"><span data-stu-id="16516-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="16516-107">Brukere angir kombinasjoner av konto og dimensjon på ulike sider, for eksempel sider for økonomijournaler, budsjettering og posteringsdefinisjoner.</span><span class="sxs-lookup"><span data-stu-id="16516-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="16516-108">De gyldige kombinasjonene av konto og dimensjon avhenger av kontostrukturene som tilordnes finans, og de avanserte reglene som er tilordnet kontostrukturene.</span><span class="sxs-lookup"><span data-stu-id="16516-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="16516-109">Når brukere angir en kombinasjon, kan de skrive inn verdiene manuelt eller bruke en omfattende oppslagsfunksjon.</span><span class="sxs-lookup"><span data-stu-id="16516-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="16516-110">Når du angir feltet, kan du begynne å skrive inn, så søkes det etter verdien og beskrivelsen.</span><span class="sxs-lookup"><span data-stu-id="16516-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="16516-111">Hvis du for eksempel skriver inn 180, søkes det etter alle verdier som begynner med denne nummerkombinasjonen.</span><span class="sxs-lookup"><span data-stu-id="16516-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="16516-112">Eller du kan skrive inn kontant, så søkes det etter en verdi som har en beskrivelse som begynner med kontant.</span><span class="sxs-lookup"><span data-stu-id="16516-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="16516-113">Du kan også bruke jokertegn, som \*kontant eller \*180 for å søke hvis verdien eller beskrivelsen inneholder søkevilkåret.</span><span class="sxs-lookup"><span data-stu-id="16516-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="16516-114">Tabellen nedenfor beskriver hurtigtastene som kan brukes når oppslaget er lukket.</span><span class="sxs-lookup"><span data-stu-id="16516-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16516-115">Hurtigtast</span><span class="sxs-lookup"><span data-stu-id="16516-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="16516-116">Handling</span><span class="sxs-lookup"><span data-stu-id="16516-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16516-117">Alt+Pil ned</span><span class="sxs-lookup"><span data-stu-id="16516-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="16516-118">Åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="16516-118">Open the lookup.</span></span> <span data-ttu-id="16516-119">Hvis du trykker Alt+Pil ned på nytt, flyttes fokus til segmentene på undermenyen.</span><span class="sxs-lookup"><span data-stu-id="16516-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="16516-120">Enter og Skift+Enter</span><span class="sxs-lookup"><span data-stu-id="16516-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="16516-121">Skilletegn for kontoplan</span><span class="sxs-lookup"><span data-stu-id="16516-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="16516-122">Pil høyre og Pil venstre</span><span class="sxs-lookup"><span data-stu-id="16516-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="16516-123">Gå til neste eller forrige segment.</span><span class="sxs-lookup"><span data-stu-id="16516-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16516-124">Kategori</span><span class="sxs-lookup"><span data-stu-id="16516-124">Tab</span></span></td>
<td><span data-ttu-id="16516-125">Flytt til neste felt i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="16516-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="16516-126">Tabellen nedenfor beskriver hurtigtastene som kan brukes når oppslaget er åpent.</span><span class="sxs-lookup"><span data-stu-id="16516-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16516-127">Hurtigtast</span><span class="sxs-lookup"><span data-stu-id="16516-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="16516-128">Handling</span><span class="sxs-lookup"><span data-stu-id="16516-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16516-129">ESC</span><span class="sxs-lookup"><span data-stu-id="16516-129">Esc</span></span></td>
<td><span data-ttu-id="16516-130">Lukk oppslaget.</span><span class="sxs-lookup"><span data-stu-id="16516-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="16516-131">Pil opp eller Pil ned</span><span class="sxs-lookup"><span data-stu-id="16516-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="16516-132">PgUp og PgDn</span><span class="sxs-lookup"><span data-stu-id="16516-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="16516-133">Home og End</span><span class="sxs-lookup"><span data-stu-id="16516-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="16516-134">Flytt til forrige eller neste verdi i listen, til forrige eller neste gruppe med verdier eller til første eller siste element i oppslaget.</span><span class="sxs-lookup"><span data-stu-id="16516-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="16516-135">Skilletegn for kontoplan</span><span class="sxs-lookup"><span data-stu-id="16516-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="16516-136">Pil høyre og Pil venstre</span><span class="sxs-lookup"><span data-stu-id="16516-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="16516-137">Gå til neste eller forrige segment.</span><span class="sxs-lookup"><span data-stu-id="16516-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16516-138">Kategori</span><span class="sxs-lookup"><span data-stu-id="16516-138">Tab</span></span></td>
<td><span data-ttu-id="16516-139">Flytt til neste felt i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="16516-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16516-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="16516-140">Alt+W</span></span></td>
<td><span data-ttu-id="16516-141">Veksle mellom <strong>Vis alle</strong> og <strong>Vis gyldig</strong>.</span><span class="sxs-lookup"><span data-stu-id="16516-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>

 




