---
title: Formeldesigner
description: "Dette emnet forklarer hvordan du bruker formeldesigneren til å analysere og vedlikehold formler i en trevisning."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 159aa0fd5d057ed4105a79f11b3658133f417319
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="formula-designer"></a>Formeldesigner

[!include[banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker formeldesigneren til å analysere og vedlikehold formler i en trevisning.

Når du åpner  **formeldesigner**-siden fra  **frigitte produkter**-siden, viser treet i venstre rute en liste over koprodukter og hierarkiet av ingrediensene for det frigitte produktet. Strukturen er avledet fra et hierarki av formler som er aktive og godkjente for den valgte varen og ingrediensene, varens standard bestillingsområde og den faktiske datoen.

Klikk **Konfigurer** for å velge ulike konfigurasjoner og angi hvilken informasjon som skal vises på linjene i treet.

Klikk **Filter** for å endre det første utvalget i visningen. Hvis du setter visningsprinsippet til **Valgte/aktive** eller **Valgte**, kan du velge enkelte versjoner av formelen eller ruten som skal brukes i visningen. Du kan velge ikke-godkjente og ikke-aktive formelversjoner som skal vises eller vedlikeholdes i formelutformingen.  

> [!NOTE]
> Hvis du åpner **Formeldesigner**-siden fra fra listesiden **Stykklister**, viser den ikke ruteinformasjon. Valget av en formel- eller ruteversjon gjelder for øyeblikket for alle forekomster av formeldesigneren.  

Avsnittene nedenfor beskriver hvilke funksjoner som er tilgjengelige i stykklisteutformingen.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Analysere en formelstruktur ved hjelp av formeldesigneren
Formelutforming har to deler:

-   Trevisningen av formelstrukturen.
-   Detaljdelen som viser detaljene for de valgte dataene. Når du velger en node i trevisningen, oppdateres hurtigfanene i detaljdelen basert på denne noden:
    -   **Detaljer om formellinjen** – Viser detaljer for formellinjen som er valgt i trevisningen.
    -   **Varedata** – Viser informasjon om hovedvaren eller varen som brukes i den valgte noden. Du kan klikke **Rediger frigitt produkt** for å vedlikeholde den valgte varen.
    -   **Formel** – Viser overskriften for formelen som er knyttet til den valgte noden.
    -   **Rute** – Viser overskriften for ruten som er knyttet til den valgte noden.
    -   **Ruteoperasjoner** – Viser en forhåndsvisning av operasjonene for ruten. Når det velges en stykklistelinje som er tilordnet en bestemt operasjon, merkes operasjonen som **Komponent kreves ved operasjoner**.

## <a name="select-a-formula-and-route"></a>Velge en formel og rute
Filteret som brukes for formelen og ruten, vises i overskriften til formeldesigneren. Du kan endre filteret ved hjelp av dialogboksen **Filter**. Tabellen nedenfor beskriver feltene i denne dialogboksen.

<table>
<thead>
<tr class="header">
<th>Felt</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produktdimensjoner</td>
<td>Hvis det valgte ferdige produktet er en produktstandard, kan du definere de aktive produktdimensjonene for hovedutvalget. Legg merke til at hvis du åpner formeldesigneren for et produkt som ikke er en produktstandard, kan ingen produktdimensjoner velges i <strong>Filter</strong>-dialogboksen.</p></td>
</tr>
<tr class="even">
<td>Område</td>
<td>Endre området som ingredienstreet vises for. Standardområdet er standard lagerområde for den ferdige varen.</td>
</tr>
<tr class="odd">
<td>Visningsprinsipp</td>
<td><p>Velg versjonvisningsprinsippet som skal brukes for den gjeldende formelstrukturen og ruten:</p>
<ul>
<li>Når prinsippet er satt til <strong>Aktiv</strong> eller <strong>Valgte/aktive</strong>, blir gyldig formel- eller ruteversjon funnet for denne datoen.</li>
<li>Når prinsippet er satt til <strong>Valgte/aktive</strong> eller <strong>Valgte</strong>, kan du velge en formelversjon eller ruteversjonen ved å klikke <strong>Formel</strong> &gt; <strong>Formelversjoner</strong> eller <strong>Rute</strong> &gt; <strong>Ruteversjoner</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versjonsdato</td>
<td>Angi versjonsdatoen for formelen og ruten. Versjonen identifiserer hvilken formelversjon som skal brukes på en bestemt dato, basert på versjonsdatoene i formelversjonsoppsettet.</td>
</tr>
<tr class="odd">
<td>Fra-antall</td>
<td>Filtrer versjonene ved å velge et bestemt «minsteantall». Hvis du angir en verdi, kan du velge forskjellige versjoner av formel- og ruteversjonen.</td>
</tr>
<tr class="even">
<td>Bare vis gyldige</td>
<td>Når du merker av for avmerkingsboksen, viser trestrukturen bare formellinjer som har gyldige datoer. Høyreklikk eller dobbeltklikk en formellinje for å åpne siden <strong>Rediger formellinje</strong> der du kan vise gyldighetsdatoene for denne formellinjen.</td>
</tr>
</tbody>
</table>

Når du bruker formeldesigneren for å se gjennom eller redigere formler som består av én eller flere nivåer av fantomer, vil ruten som er knyttet til den øverste varen vanligvis strekke seg over hele formelhierarkiet. Hvis du vil forenkle oversikten, kan du låse ruten på øverste nivå i visningen ved å klikke **Vis** &gt; **Lås rute**. Hvis du vil låse opp ruten, klikker du **Vis** &gt; **Lås opp rute**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Legge til og redigere formler og formellinjer
Bruk funksjonene **Stykklistelinjer** eller **Formel** til å endre fomrellinjene eller formelen. Når du velger en node i treet, bestemmer nodetypen funksjonene som er tilgjengelige.

| Funksjon                            | beskrivelse                                                                                               | Nodetype og betingelser |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Stykklistelinjer &gt; Rediger                 | Åpne en dialogboks der du kan redigere attributtene for formellinjen.                                         | Denne funksjonen er tilgjengelig når det velges en node for formellinjen. |
| Stykklistelinjer &gt; Slett               | Slett en formellinje fra den valgte formelen.                                                          | Denne funksjonen er tilgjengelig når det velges en node for formellinje og formelen ikke er låst for redigering. |
| Stykklistelinjer &gt; Legg til før linje      | Åpne en dialogboks der du kan velge en produktvariant ha før den valgte formellinjen.     | Denne funksjonen er tilgjengelig når det velges en node for formellinjen. |
| Stykklistelinjer &gt; Legg til i komponentstykkliste | Åpne en dialogboks der du kan velge en produktvariant ha på slutten av den valgte formelen.   | Denne funksjonen er tilgjengelig når noden som er valgt, har en valgt formel. Hvis denne funksjonen ikke er tilgjengelig, kan det hende en formelversjon mangler for den valgte varevarianten. I så fall kan du klikke **Formel** &gt; **Opprett versjon** for å opprette den manglende versjonen for den valgte noden. |
| Stykklistelinjer &gt; Legg til etter linje       | Åpne en dialogboks der du kan velge en produktvariant ha etter den valgte formellinjen.      | Denne funksjonen er tilgjengelig når det velges en node for formellinjen. |
| Formel &gt; Opprette versjon         | Opprett en ny formelversjon eller formel for produktvarianten for den valgte noden.                     | Denne funksjonen er tilgjengelig når den valgte noden for formellinjen er koblet til en vare som har produksjonstypen **Stykkliste** eller **Formel**. |
| Formel &gt; Beregning            | Åpne en dialogboks der du kan kjøre kost- eller salgsprisberegning for den valgte produktvarianten. | Denne funksjonen er tilgjengelig når noden som er valgt, er knyttet til en formelversjon. |
| Formel &gt; Kontroller                  | Valider og kontroller den valgte formelen.                                                                  | Denne funksjonen er tilgjengelig når noden som er valgt, er knyttet til en formelversjon. |

## <a name="configuring-the-tree-view"></a>Konfigurere trevisningen
Klikk **Oppsett** for å tilpasse informasjonen som vises i trevisningen i formeldesigneren.

| Feltgruppe | beskrivelse |
|-------------|-------------|
| Stykkliste         | Bruk avmerkingsboksene for å velge kriteriene som vises i trestrukturen. Formeldesigneren viser de valgte kriteriene nederst i begge kategorier. |
| Rute       | Bruk avmerkingsboksene for å velge kriteriene som vises for rutene. |

