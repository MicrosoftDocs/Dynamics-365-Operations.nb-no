---
title: Konfigurere app feltnavn i Warehousing app
description: Dette emnet beskriver hvordan du definerer og konfigurerer lager app-feltnavn og prioriteter i Dynamics 365 for operasjoner.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurere app feltnavn i Warehousing app

Dette emnet beskriver hvordan du definerer og konfigurerer lager app-feltnavn og prioriteter i Dynamics 365 for operasjoner. 

**Merk:** dette emnet gjelder for funksjonene i Lagerstyring. Den gjelder ikke for funksjoner i Lagerstyring. Dynamics 365 for operasjoner - lager er et program som du kan bruke til å utføre oppgaver på lageret. Du kan definere og konfigurere feltnavnene som brukes i programmet, i tillegg konfigurere prioriteten feltnavnene skal tilordnes. Dette emnet forklarer hvordan du definerer og konfigurerer disse feltnavnene i lageret app og prioriteter, og hvordan de brukes i Dynamics 365 for operasjoner - lager. For detaljert informasjon om hvordan du konfigurerer tilkoblingen til Dynamics 365 for operasjoner - lager, kan du se opplæringen [installere og konfigurere Dynamics 365 for operasjoner - lager](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurere lageret app feltnavn
===================================

Når du bruker Dynamics 365 for operasjoner - lager på den mobile enheten, kan du konfigurere hvordan metadata skal vises på enheten på den **lager app feltnavn** siden. I et nytt selskap i Dynamics 365 for operasjoner, velger du **opprette standardoppsett for** til å generere alle feltnavn som skal brukes i lageret mobilenhet arbeidsflyter, og deretter tilordne en foretrukket inndatamodus og Inndatatype dem. Når du har generert alle feltnavn, kan du velge følgende alternativer for inndata.

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
<td>Dette alternativet angir om en skanning feltet eller et inndatafelt for manuell registrering skal vises for navnet på valgte feltet. Dette er nyttig for å skille feltene, avhengig om strekkoder er brukt for feltet. <strong>Merk:</strong> For feltnavnene med foretrukket inndatamodus satt til <strong>skanning</strong>, kan du angi informasjon manuelt hvis strekkoden er uleselig eller skadet.</td>
</tr>
<tr class="even">
<td>Inndatatype</td>
<td>Dette alternativet angir hvilken inndatatypen som skal brukes for navnet på valgte feltet. Det finnes fire alternativer:
<ul>
<li><strong>Valg</strong> - inneholder en liste over alternativer å velge mellom. Navn på felt med dette alternativet kan ikke redigeres.</li>
<li><strong>Datoen</strong> - feltnavn som er angitt som dato, vises et datoformat med etiketten. På denne måten lagermedarbeidere kan du se hvilket format for å angi datoer. Navn på felt med dette alternativet kan ikke redigeres.</li>
<li><strong>Alpha</strong> - Hvis valgt, tastaturet enheten vil bli brukt når du oppgir opplysninger manuelt i programmet. Tastatur-opplevelse kan endres avhengig av hvilken enhet som brukes.</li>
<li><strong>Numerisk</strong> - For feltnavnene som Bruk numeriske inndata bare, kan du velge dette alternativet for å vise et egendefinert numerisk tastatur med inndata-feltet i stedet for tastaturet enheten.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurere lageret app feltet prioritet
======================================

På den **lager app feltet Prioritet** siden, kan du legge feltnavnene i grupper for ulike prioritet. Dette gjør det mulig å bestemme hvilken informasjon som skal vises på siden Hovedoppgaven når lagermedarbeidere utfører oppgaver ved hjelp av programmet. Hvis du klikker **opprette standardoppsett for**, et standardsett med grupper prioritet vil bli generert. Det er mulig å opprette så mange prioritet grupper etter behov, men bare tre prioritet grupper vises på siden for aktiviteten. Det blir tilordnet hvert felt en relativ prioritet avhengig av gruppen prioritet når Dynamics 365 for operasjoner sender metadata til programmet, og programmet vil vise i metadata på oppgavesiden gruppene første tre prioritet. Resten av overflødig metadata vises på en sekundær Detaljer-siden. Tabellen nedenfor viser et eksempel på fem prioritet-grupper.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritet-gruppen</th>
<th>Tilordnede felt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Prioriteten 10</td>
<td><ul>
<li>Vare</li>
<li>Antall</li>
<li>Måleenhet</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioriteten 20</td>
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
<td> Priority 50</td>
<td><ul>
<li>Plassering</li>
<li>Nummerskilt</li>
</ul></td>
</tr>
</tbody>
</table>

For eksempel når lagermedarbeider utfører en oppgave på en mobil enhet, hvis metadataene som vises i programmet består av følgende felt:

-   Vare
-   Antall
-   Måleenhet
-   Varebeskrivelse
-   Størrelse og plassering

Basert på lageret app feltet prioritet er definert i tabellen ovenfor, vises følgende 3 rader med informasjon på siden aktiviteten:

-   Rad 1: Vare, antall, enhet
-   Rad 2: Beskrivelse
-   Rad 3: størrelse

Gjenstående metadata, for eksempel plassering, vises ikke på siden aktiviteten, men vises på detaljer-siden. Hvis du vil vite mer, og se eksempler på brukergrensesnittet, kan du referere til blogginnlegget [annonserer Dynamics 365 for operasjoner - lager](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Se også
--------

[Installere og konfigurere Microsoft Dynamics 365 for operasjoner – lager](install-configure-warehousing-app.md)


