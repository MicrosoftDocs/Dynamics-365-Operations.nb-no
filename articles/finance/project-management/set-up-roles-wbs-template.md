---
title: Definere roller i maler for arbeidsnedbrytningsstruktur
description: Dette emnet gir informasjon om definering av rolleinformasjon om maler for arbeidsnedbrytningsstruktur.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760626"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Definere roller i maler for arbeidsnedbrytningsstruktur

[!include [banner](../includes/banner.md)]

Prosjektledere kan definere maler for arbeidsnedbrytningsstruktur (WBS-maler) som kan gjelde når de oppretter en WBS for nye prosjekter. Prosjektledere kan legge til roller ved oppretting av en mal. Bruk følgende fremgangsmåte for å tilordne en rolle til en WBS-mal. 

1. Velg **Prosjektstyring og regnskap** > **Oppsett** > **Prosjekte** > **Maler for arbeidsnedbrytningsstruktur**.
2. Velg **Detaljer** for en valgt WBS-mal.
3. Velg en oppgave i listen, og deretter i **Rolle**-feltet velger du en rolle for å tildele til aktiviteten.

## <a name="work-with-a-wbs"></a>Arbeide med en WBS

Du kan opprette en ny WBS, eller du kan kopiere en WBS fra en eksisterende WBS-mal. En prosjektleder kan enkelt håndtere ressursene ved å tilordne roller til nye aktiviteter på WBS-en. Roller kan erstattes enten etter at en ressurs er anskaffet eller etter en bekreftet ressurs for å jobbe på oppgaven, identifiseres. Denne fleksibiliteten gjør det mulig for prosjektledere å utføre følgende oppgaver:

- Identifisere antallet ressurser som kreves for WBS-arbeidspakkene.
- Estimere prosjektkostnader.
- Fastsette et foreløpig budsjett.
- Beregne varigheten til aktiviteten, basert på roller og ressurser.
- Utvikle noen prosjektstyringsplaner, basert på den tilgjengelige prosjektinformasjonen.

Flere alternativer er lagt i WBS for bedre ressursberegning.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ressurstilordninger</td>
<td>Vis tildelte ressurser, datoer, antall timer og bestillingstypen for oppgaver på WBS.</td>
</tr>
<tr class="even">
<td>Autogenerer team</td>
<td>Legg automatisk til planlagte ressurser ved hjelp av rollene som er knyttet til en oppgave. Finance foreslår automatisk planlagte ressurser ved hjelp av en beslutningsanalyse med flere kriterier som er basert på roller. Etter at rollene og innsatsen (timer) er satt til oppgavene i en WBS, og etter at strukturen er frigitt, velger du <strong>Autogenerer team</strong>. Antall planlagte ressurser legges til WBS-en og i kategorien <strong>Prosjekt- og teamplanleggingr</strong>.</td>
</tr>
<tr class="odd">
<td>Ressurs (rullegardinliste)</td>
<td>På siden <strong>Start ressurstilordning</strong> kan du velge ressurser til forpliktende eller ikke-forpliktende bestilling, basert på den angitte varigheten. Du kan justere innstillingene for å vise og angi varigheten for ressursaktiviteter. Du kan velge og tilordne ressurser på arbeidspakkenivå ved hjelp av følgende alternativer:
<ul>
<li><strong>Godta</strong> – bekrefte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Avbryt</strong> – avbryte endringene i ressursen som er tilordnet en oppgave.</li>
<li><strong>Tildel automatisk</strong> – en tilgjengelig bemannet ressurs som har en matchende rolle blir automatisk valgt og tilordnet til den valgte oppgaven.</li>
</ul></td>
</tr>
</tbody>
</table>

1. På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.
2. Velg **Plan** > **Aktiviteter** > **Arbeidsnedbrytningsstruktur**.
3. Velg **Ny** for å legge til følgende nivå-en aktiviteter til WBS:

    - Oppstart
    - Planlegging
    - Utfører
    - Overvåking og kontroll
    - Lukk

4. Angi datoene og innsatsen (timer), som vist på den følgende illustrasjonen.

    [![Angi datoene og innsats](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Velg oppgavelinjen **Oppstart**, og deretter, i **Rolle**-feltet velger du **Overordnet prosjektleder**.
6. Velg **Publiser**.
7. På samme linje i feltet **Ressurs**, velg **Daniel Goldschmidt** og velg deretter **Aksepter**.
8. Velg oppgavelinjen **Planlegging**, og deretter, i **Rolle**-feltet velger du **Forretningsanalytiker**.
9. Velg **Publiser** og velg deretter **Autogenerer team**.
10. Velg **Ja** i dialogboksen som dukker opp.
11. I **Ressurs**-feltet må du kontrolle at verdien er **Forretningsanalytiker 1**.
12. For **Forretningsanalytiker 1**-ressursen, åpne oppslag, og velg **Lansere ressursoppgaver**. Velg deretter en medarbeider for oppgaven.
13. Velg **Myk tilordning** &gt; **Full kapasitet**.

    > [!NOTE] 
    > Du får ikke en advarsel om at den spesifikke ressursen nå er 2, fordi nummeret på ressursen fortsatt er 1.

14. På siden **Struktur for arbeidsavbrudd**, valider ressurstilordningen på WBS, og velg deretter **Lagre**.
