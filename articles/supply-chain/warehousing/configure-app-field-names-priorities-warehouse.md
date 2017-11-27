---
title: "Konfigurere navn på appfelt i lagerapp"
description: "Dette emnet beskriver hvordan du definerer og konfigurerer navn på lagerappfelt og prioriteter i Finance and Operations."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2fbf9d84fa0fec32004936542003115cf580d91c
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurere navn på appfelt i lagerapp

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du definerer og konfigurerer navn på lagerappfelt og prioriteter i Finance and Operations. 

**Obs!** Dette emnet artikkelen gjelder funksjoner i Lagerstyring. Den gjelder ikke for funksjoner i Beholdningsstyring. Finance and Operations – Lager er en app som du kan bruke til å utføre lageroppgaver. Du kan definere og konfigurere feltnavnene som brukes i appen, samt konfigurere prioriteten som feltnavnene skal tilordnes. Dette emnet forklarer hvordan du definerer og konfigurerer disse navnene og prioriteringene for lagerappfelt, og hvordan de brukes i Finance and Operations – Warehousing. Hvis du vil ha detaljert informasjon om hvordan du konfigurerer tilkoblingen til Finance and Operations – Warehousing, kan du se opplæringen [Installere og konfigurere Finance and Operations – Warehousing](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurere navn på lagerappfelt
===================================

Når du bruker Finance and Operations – Warehousing på den mobile enheten, kan du konfigurere hvordan metadata skal vises på enheten på siden **Navn på lagerappfelt**. I et nytt firma i Finance and Operations velger du **Opprett standardoppsett** for å generere alle feltnavn som skal brukes i arbeidsflyter for mobilenheter i lageret, og deretter tilordner du en foretrukket inndatamodus og inndatatype til dem. Når du har generert alle feltnavn, kan du velge følgende alternativer for inndata.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alternativ</th>
<th>beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Foretrukket inndatamodus</td>
<td>Dette alternativet angir om et skanningsfelt eller et manuelt inndatafelt skal vises for det valgte feltnavnet. Dette er nyttig for å skille feltene, avhengig om strekkoder er brukt for feltet. <strong>Merk:</strong> For feltnavnene med foretrukket inndatamodus satt til <strong>Skanning</strong>, kan du angi informasjon manuelt hvis strekkoden er uleselig eller skadet.</td>
</tr>
<tr class="even">
<td>Inndatatype</td>
<td>Dette alternativet angir hvilken inndatatype som skal brukes for det valgte feltnavnet. Fire alternativer er tilgjengelige:
<ul>
<li><strong>Utvalg</strong> - Inneholder en liste med alternativer å velge mellom. Feltnavn med dette alternativet kan ikke redigeres.</li>
<li><strong>Dato</strong> - Feltnavn som er oppgitt som dato, viser et datoformat med etiketten. På denne måten kan lagermedarbeidere se hvilket format datoen skal angis i. Feltnavn med dette alternativet kan ikke redigeres.</li>
<li><strong>Alpha</strong> - Hvis dette er valgt vil enhetens tastatur brukes ved innskriving av informasjon manuelt i appen. Tastaturopplevelsen kan endres avhengig av hvilken enhet som brukes.</li>
<li><strong>Numerisk</strong> - For feltnavn som bare bruker numerisk inngang, kan du velge dette alternativet for å vise et egendefinert numerisk tastatur med inntastingsfeltet, i stedet for enhetens tastatur.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurere prioritet for lagerappfelt
======================================

På siden **Prioritet for lagerappfelt** kan du legge feltnavn i ulike prioritetsgrupper. Dette gjør det mulig å bestemme hvilken informasjon som skal vises på hovedoppgavesiden når lagermedarbeidere utfører oppgaver ved hjelp av appen. Hvis du klikker **Opprett standardoppsett**, genereres et standardsett med prioritetsgrupper. Det er mulig å opprette så mange prioritetsgrupper som nødvendig, men bare tre prioritetsgrupper vises på oppgavesiden. Når Finance and Operations sender metadata til appen, tilordnes hvert felt en relativ prioritet avhengig av prioritetsgruppen, og appen viser de første tre prioritetsgruppene i metadataene på oppgavesiden. Resten av overflytmetadataene vises på en sekundær detaljside. Tabellen nedenfor viser et eksempel på fem prioritetsgrupper.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritetsgruppe</th>
<th>Tilordnede felt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioritet 10</td>
<td><ul>
<li>Vare</li>
<li>Antall</li>
<li>Måleenhet</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritet 20</td>
<td><ul>
<li>Gruppestilling</li>
<li>Gruppe</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioritet 30</td>
<td><ul>
<li>Varebeskrivelse</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritet 40</td>
<td><ul>
<li>Konfigurasjon</li>
<li>Farge</li>
<li>Størrelse</li>
<li>Stil</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioritet 50</td>
<td><ul>
<li>Plassering</li>
<li>Nummerskilt</li>
</ul></td>
</tr>
</tbody>
</table>

Når en lagermedarbeider for eksempel utfører en oppgave på en mobil enhet, og metadataene som vises i appen, består av følgende felt:

-   Vare
-   Antall
-   Måleenhet
-   Varebeskrivelse
-   Størrelse og lokasjon

Basert på prioriteten for lagerappfelt som er definert i tabellen ovenfor, vises følgende 3 rader med informasjon på oppgavesiden:

-   Rad 1: vare, antall, måleenhet
-   Rad 2: varebeskrivelse
-   Rad 3: størrelse

Gjenstående metadata, for eksempel lokasjon, vises ikke på oppgavesiden, men vises på detaljsiden. Hvis du vil vite mer og se eksempler på brukergrensesnittet, kan du se blogginnlegget [Kunngjøring av Finance and Operations – Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Se også
--------

[Installere og konfigurere Microsoft Dynamics 365 for Finance and Operations – Warehousing](install-configure-warehousing-app.md)




