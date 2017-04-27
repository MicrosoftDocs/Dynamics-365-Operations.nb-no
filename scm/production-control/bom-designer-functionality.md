---
title: Funksjonaliteten for stykklisteutforming
description: "Denne artikkelen beskriver hvordan du kan bruke siden Stykklisteutforming til å utforme og arbeide med trestrukturer for stykklister. Du kan klikke Konfigurer for å velge ulike konfigurasjoner og angi hvilken informasjon som skal vises på linjene i treet."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-08 21 - 09 - 22
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 2c98039c9fa8179408394f9f66b9fca0f8cad3fe
ms.lasthandoff: 03/29/2017


---

# <a name="bom-designer-functionality"></a>Funksjonaliteten for stykklisteutforming

Denne artikkelen beskriver hvordan du kan bruke siden Stykklisteutforming til å utforme og arbeide med trestrukturer for stykklister. Du kan klikke Konfigurer for å velge ulike konfigurasjoner og angi hvilken informasjon som skal vises på linjene i treet.

Når du åpner siden **Stykklisteutforming** fra siden **Frigitte produkter**, viser den hierarkiet for stykklistene som er aktive og godkjente for den valgte varen, standard bestillingsområde for varen og den faktiske datoen.  

Klikk **Filter** for å endre det første utvalget i visningen. Ved å angi visningsprinsippet **Valgte/aktive eller Valgte**, kan du velge enkelte versjoner av stykklisten eller ruten som skal brukes i visningen. Du kan velge ikke-godkjente og ikke-aktive stykklisteversjoner som skal vises eller vedlikeholdes i stykklisteutforming.  

**Obs!**  Hvis du åpne stykklisteutformingen fra listesiden **Stykklister**, viser ikke ruteinformasjon. Valg av en stykkliste- eller ruteversjon er en egenskap for stykkliste- og ruteversjonen, og gjelder for alle forekomster av stykklisteutformingen.  

Avsnittene nedenfor beskriver hvilke funksjoner som er tilgjengelige i de forskjellige kategorier i stykklisteutformingen.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Analysere en stykklistestruktur ved hjelp av stykklisteutforming
Stykklisteutforming har to deler:

-   Trevisningen av stykklistestrukturen.
-   Detaljdelen som viser detaljene for de valgte dataene. Når du velger en node i trevisningen, oppdateres hurtigfanene i detaljdelen basert på denne noden:
    -   **Detaljer om stykklistelinje** – Viser detaljer for stykklistelinjen som er valgt i trevisningen.
    -   **Varedata** – Viser informasjon om hovedvaren eller varen som brukes i den valgte noden. Du kan klikke **Rediger frigitt produkt** for å vedlikeholde den valgte varen.
    -   **Stykkliste** – Viser overskriften for stykklisten som er knyttet til den valgte noden.
    -   **Rute** – Viser overskriften for ruten som er knyttet til den valgte noden.
    -   **Ruteoperasjoner** – Viser en forhåndsvisning av operasjonene for ruten. Når det velges en stykklistelinje som er tilordnet en bestemt operasjon, merkes operasjonen som **Komponent kreves ved operasjoner**.

## <a name="selecting-a-bom-and-route"></a>Velge en stykkliste og rute
Filteret som brukes for stykklisten og ruten, vises i overskriften for stykklisteutforming. Du kan endre filteret ved hjelp av dialogboksen **Filter**. Tabellen nedenfor beskriver feltene i denne dialogboksen.

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
<td>Hvis det valgte ferdige produktet er en produktstandard, kan du definere de aktive produktdimensjonene for hovedvalget. <strong>Obs!</strong>  Hvis du åpne stykklisteutformingen for et produkt som ikke er en produktstandard, kan ingen produktdimensjoner velges i dialogboksen <strong>Filter</strong>.</td>
</tr>
<tr class="even">
<td>Område</td>
<td>Endre området som stykklistetreet vises for. Standardområdet er standard lagerområde for den ferdige varen.</td>
</tr>
<tr class="odd">
<td>Visningsprinsipp</td>
<td>Velg versjonvisningsprinsippet som skal brukes for gjeldende stykklistestruktur og rute:
<ul>
<li>Når prinsippet er satt til <strong>Aktiv eller Valgte/aktive</strong>, blir gyldig stykkliste- eller ruteversjon funnet for denne datoen.</li>
<li>Når prinsippet er satt til <strong>Valgte/aktive eller Valgte</strong>, kan du velge en stykklisteversjon eller ruteversjonen ved å klikke <strong>Stykkliste</strong> &gt; <strong>Stykklisteversjoner</strong> eller <strong>Rute</strong> &gt;<strong>Ruteversjoner</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versjonsdato</td>
<td>Angi versjonsdatoen for stykklisten og ruten. Versjonen identifiserer hvilken stykklisteversjon som brukes på en bestemt dato, som bestemt av versjonsdatoene i stykklisteversjonsoppsettet.</td>
</tr>
<tr class="odd">
<td>Fra antall</td>
<td>Filtrer versjonene ved å velge et bestemt antall. Hvis du angir en verdi, kan du velge forskjellige versjoner av stykkliste- og ruteversjonen.</td>
</tr>
<tr class="even">
<td>Bare vis gyldige</td>
<td>Når du merker av for avmerkingsboksen, viser trestrukturen bare stykklistelinjer som har gyldige datoer. Høyreklikk eller dobbeltklikk en stykklistelinje for å åpne siden <strong>Rediger stykklistelinje</strong> der du kan vise gyldighetsdatoene for denne stykklistelinjen.</td>
</tr>
</tbody>
</table>

Når du bruker stykklisteutformingen for å se gjennom eller redigere stykklister som består av én eller flere nivåer av fantomer, vil ruten som er knyttet til den øverste varen vanligvis strekke seg over hele stykklistehierarkiet. Hvis du vil forenkle oversikten, kan du låse ruten på øverste nivå i visningen ved å klikke **Vis** &gt; **Lås rute**. Hvis du vil låse opp ruten, klikker du **Vis** &gt; **Lås opp rute**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Legge til og redigere stykklister og stykklistelinjer
Bruk funksjonene **Stykklistelinjer ** eller **Stykkliste** til å endre stykklistelinjene eller stykklisten. Når du velger en node i treet, bestemmer nodetypen funksjonene som er tilgjengelige.

| Funksjon                            | beskrivelse                                                                                               | Nodetype og betingelser                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stykklistelinjer &gt; Rediger                 | Åpne en dialogboks der du kan redigere attributtene for stykklistelinjen.                                             | Denne funksjonen er tilgjengelig når det velges en node for stykklistelinjen.                                                                                                                                                                                                                                   |
| Stykklistelinjer &gt; Slett               | Slett en stykklistelinje fra den valgte stykklisten.                                                                  | Denne funksjonen er tilgjengelig når det velges en node for stykklistelinje og stykklisten ikke er låst for redigering.                                                                                                                                                                                             |
| Stykklistelinjer &gt; Legg til før linje      | Åpne en dialogboks der du kan velge en produktvariant ha før den valgte stykklistelinjen.         | Denne funksjonen er tilgjengelig når det velges en node for stykklistelinjen.                                                                                                                                                                                                                                   |
| Stykklistelinjer &gt; Legg til i komponentstykkliste | Åpne en dialogboks der du kan velge en produktvariant ha på slutten av den valgte stykklisten.       | Denne funksjonen er tilgjengelig når noden som er valgt, har en valgt stykkliste. Hvis denne funksjonen ikke er tilgjengelig, kan det hende en stykklisteversjon mangler for den valgte varevarianten. I så fall kan du klikke **Stykkliste** &gt; **Opprett versjon** for å opprette den manglende versjonen for den valgte noden. |
| Stykklistelinjer &gt; Legg til etter linje       | Åpne en dialogboks der du kan velge en produktvariant ha etter den valgte stykklistelinjen.          | Denne funksjonen er tilgjengelig når det velges en node for stykklistelinjen.                                                                                                                                                                                                                                   |
| Stykkliste &gt; Opprett versjon             | Opprett en ny stykklisteversjon eller stykkliste for produktvarianten for den valgte noden.                             | Denne funksjonen er tilgjengelig når den valgte noden for stykklistelinjen er koblet til en vare som har produksjonstypen **Stykkliste** eller **Formel**.                                                                                                                                                  |
| Stykkliste&gt;beregning                | Åpne en dialogboks der du kan kjøre kost- eller salgsprisberegning for den valgte produktvarianten. | Denne funksjonen er tilgjengelig når noden som er valgt, er knyttet til en stykklisteversjon.                                                                                                                                                                                                         |
| Stykkliste &gt; Kontroller                      | Valider og kontroller den valgte stykklisten.                                                                      | Denne funksjonen er tilgjengelig når noden som er valgt, er knyttet til en stykklisteversjon.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Konfigurere trevisningen
Klikk **Oppsett** for å tilpasse informasjonen som vises i trevisningen i Stykklisteutforming.

| Feltgruppe | Beskrivelse                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stykkliste         | Bruk avmerkingsboksene for å velge kriteriene som vises i trestrukturen. Stykklisteutforming viser de valgte kriteriene nederst i begge kategorier. |
| Rute       | Bruk avmerkingsboksene for å velge kriteriene som vises for rutene.                                                                                    |




