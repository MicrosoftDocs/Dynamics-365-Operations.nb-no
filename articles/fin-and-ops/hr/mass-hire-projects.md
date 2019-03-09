---
title: Masseansettelsesprosjekter
description: Med masseansettelsesprosjekter kan personalespesialister å opprette flere stillinger og effektivt ansette arbeidere i disse stillingene.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4c1bd382fa803f90a251c8c45acc556bee627d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "361550"
---
# <a name="mass-hire-projects"></a>Masseansettelsesprosjekter

[!include [banner](../includes/banner.md)]

Med masseansettelsesprosjekter kan personalespesialister å opprette flere stillinger og effektivt ansette arbeidere i disse stillingene.

## <a name="overview"></a>Oversikt

Bruk masseansettelsesprosjekter når du leier inn flere arbeidere samtidig, for eksempel når du leier for å møte sesongbaserte behov. Opprette et masseansettelsesprosjekt er nyttig fordi du kan opprette stillingsposter, arbeiderposter og arbeidertilordninger for stillinger samtidig. Når du oppretter stillinger for et masseansettelsesprosjekt, kan du angi følgende informasjon:

- Antall stillinger som skal opprettes
- Typen arbeider for personene som du vil ansette for stillingene
- Avdelingen og jobben som er knyttet til stillingene
- Verdien for fulltidsansatt for stillingen

## <a name="example"></a>Eksempel

Om sommeren bruker du vanligvis 15 – 20 deltid studenter til å fylle tilgjengelige praktikantstillinger i firmaet. I år vil du leie inn fem regnskapsførere, fem ordrebehandlere og fem kasserere. Du oppretter et masseansettelsesprosjekt kalt "Sommerjobber" i stedet for å opprette hver stillingspost og arbeiderpost separat. Prosjektets start- og sluttdatoer samsvarer med start- og sluttdatoene for stillingsvarighetene for stillingene du oppretter for masseansettelsesprosjektet.

På siden **Masseansettelsesprosjekter** velger du "Sommerjobber"-prosjektet og klikker deretter **Åpne prosjekt**. I det åpne masseansettelsesprosjektet klikker du **Opprett stillinger** og angir informasjon om regnskapsfører stillingen. Du kan angi at fem regnskapsførerstillinger skal opprettes ved hjelp av den samme informasjonen for hver enkelt, og klikk deretter OK. Gjenta denne prosessen for ordrebehandler- og kassererstillingene.

Når du har valgt studenter som du vil ansette i praktikantstillingene, angir du hver students informasjon i **Stillingsdetaljer** for stillingen som du ansetter dem i. Når du har angitt alle detaljene, velger du stillingen på Masseansettelsesprosjekter-siden, og klikk deretter **Ansett**. En stillingspost opprettes for hver stilling, og en arbeiderpost opprettes og tilordnes til riktig stilling for hver person du ansetter.

## <a name="mass-hire-project-statuses"></a>Statuser for masseansettelsesprosjekt

Et masseansettelsesprosjekt kan ha følgende statuser.

- Opprettet
- Åpen
- Lukket

På siden **Masseansettelsesprosjekt** klikker du **Åpne prosjekt** eller **Lukk prosjekt** for å endre statusen for et masseansettelsesprosjekt. I tabellen nedenfor ser du hva du kan gjøre med et prosjekt i henhold til statusen.

<table>
<thead>
<tr>
<th>Status</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr>
<td>Opprettet</td>
<td>Du kan opprette og redigere informasjon, men kan ikke opprette stillinger for prosjektet. Dette er standardstatus for nye prosjekter.</td>
</tr>
<tr>
<td>Åpen</td>
<td>Du kan endre prosjektdetaljene, opprette stillinger for masseansettelsesprosjektet og ansette personer i stillingene. Dette er statusen for aktive prosjekter.</td>
</tr>
<tr>
<td>Lukket</td>
<td>Du kan ikke legge til stillinger i prosjektet. Hvis du vil legge til stillinger i masseansettelsesprosjektet, åpner du prosjektet på nytt. Dette er statusen for ferdige prosjekter.
<blockquote>[!NOTE] Før du kan lukke et masseansettelsesprosjekt må alle stillinger i prosjektet ha statusen Opprettet eller Lukket.</blockquote>
</td>
</tr>
</tbody>
</table>
