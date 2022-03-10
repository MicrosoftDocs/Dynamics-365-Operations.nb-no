---
title: Oversikt over produktkonfigurasjonsmodeller
description: Denne artikkelen definerer termer og begreper som er relevante for produktkonfigurasjonsmodeller. Produktkonfigurasjonsmodeller lar deg bygge en generell produktstruktur som kan brukes til å konfigurere mange produktvarianter for ett enkelt produkt.
author: t-benebo
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage, PCModalWaitDialog, PCTemplateConfigurationManager, PCConfigurationUIGrouping
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "4031"
- intro-internal
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fddad1fffd61ef0cf78977721bdf2da51aa4c682
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984652"
---
# <a name="product-configuration-models-overview"></a>Oversikt over produktkonfigurasjonsmodeller

[!include [banner](../includes/banner.md)]

Denne artikkelen definerer termer og begreper som er relevante for produktkonfigurasjonsmodeller. Produktkonfigurasjonsmodeller lar deg bygge en generell produktstruktur som kan brukes til å konfigurere mange produktvarianter for ett enkelt produkt.

Produktkonfigurasjonsmodeller opprettes for å representere en generell produktstruktur. Når du har konfigurert en produktkonfigurasjonsmodell, kan du konfigurere en spesifikk produktvariant som har en unik stykkliste og rute. Produktkonfigurasjonsmodeller bruker både deklarative begrensninger og imperative beregninger til å håndtere relasjoner og begrensninger mellom ulike produktvarianter. Du kan konfigurere varer på salgsordrer, salgstilbud, bestillinger og produksjonsordrer. Tabellen nedenfor beskriver tabellbegrensningsbaserte uttrykk og begreper.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponenter</td>
<td>Komponenter er hovedbyggeblokkene for en produktkonfigurasjonsmodell. Komponenter vises i en trestruktur på siden <strong>Detaljer om restriksjonsbasert produktkonfigurasjonsmodell</strong>. Komponenter kan inneholde følgende elementer:
<ul>
<li>Attributter</li>
<li>Begrensninger</li>
<li>Beregninger</li>
<li>Underkomponenter</li>
<li>Brukerkrav</li>
<li>Stykklistelinjer</li>
<li>Ruteoperasjoner</li>
</ul></td>
</tr>
<tr class="even">
<td>Attributter</td>
<td>Attributter beskriver alle funksjonene til produktkonfigurasjonsmodellen. Du kan bruke attributter til å angi funksjonene som kan velges når et spesifikt produkt konfigureres. Attributter brukes i begrensninger og betingelser. Når attributter oppretter og legges til i en produktkonfigurasjonsmodell, refereres de relaterte attributtypene. Det kan angis en standardverdi for et attributtet. Standardverdien brukes i brukergrensesnittet for konfigurasjon når produktkonfigurasjonsmodellen konfigureres. Du kan angi at et attributt er obligatorisk, skrivebeskyttet eller skjult.
<ul>
<li><strong>Obligatorisk</strong> – Det må angis en verdi for attributtet når produktet konfigureres.</li>
<li><strong>Skrivebeskyttet</strong> – Attributtverdien vises under en konfigurasjonsøkt, men kan ikke endres.</li>
<li><strong>Skjult</strong> – Attributtverdien inkluderes i begrensninger og betingelser, men vises ikke under en konfigurasjonsøkt.</li>
</ul>
Du kan også angi en betingelse for attributter. Hvis betingelsen er oppfylt, må det angis en verdi for det obligatoriske attributtet. Betingelser er uttrykk som må oppfylles for at attributter, stykklistelinjer og ruteoperasjoner skal inkluderes i en produktkonfigurasjonsmodell. Alle attributter som er referert i en betingelse blir obligatorisk. Det anbefales at du velger attributtene som obligatoriske på fanen <strong>Attributer</strong>. Dette kan gjøre det enklere å identifisere obligatoriske attributter. Attributtverdier er en viktig del av gjenbruk av konfigurasjoner. Systemet bruker attributtverdier til å avgjøre om det finnes en konfigurasjon som samsvarer valgene en bruker foretar under en konfigurasjonsøkt.</td>
</tr>
<tr class="odd">
<td>Attributtyper</td>
<td>Attributtyper spesifiserer hvilke datatyper for attributter som brukes i en produktkonfigurasjonsmodell. Følgende attributtyper brukes:
<ul>
<li><strong>Heltall</strong> med eller uten et område</li>
<li><strong>Desimal</strong></li>
<li><strong>Tekst</strong> med eller uten en fast liste</li>
<li><strong>Boolsk</strong></li>
</ul>
Hvis attributtypen er <strong>Boolsk</strong>, <strong>Heltall</strong> med et område eller <strong>Tekst</strong> med en fast liste, er et sett med verdier tilgjengelig når en produktkonfigurasjonsmodell er definert. <strong>Obs! </strong> Produktkonfigurasjonløseren gjenkjenner bare følgende attributtyper: <strong>Boolsk</strong>, <strong>Tekst</strong> med en fast liste og <strong>Heltall</strong> med et område. Derfor kan bare disse attributtypene brukes i uttrykksbegrensninger og -betingelse.</td>
</tr>
<tr class="even">
<td>Begrensninger</td>
<td>Begrensninger beskriver begrensningene for produktmodellkonfigurasjonen. Begrensninger brukes til å garantere at bare gyldige brukere velges når et produkt konfigureres. Begrensninger kan være uttrykksbegrensninger eller tabellbegrensninger:
<ul>
<li>Uttrykksbegrensninger kan bare brukes for komponenten som de er tilknyttet. Uttrykksbegrensningene for en komponent kan referere attributter for delkomponenter for komponenten. Produktkonfigurasjonsløseren brukes til å løse begrensningene, og du må bruke problemløsersyntaksen når du skriver begrensningene. Hvis du vil ha mer informasjon, kan du se emnekoblingen om uttrykksbegrensninger og tabellbegrensninger.</li>
<li>Tabellbegrensninger må defineres før de kan brukes på en komponent i en produktkonfigurasjonsmodell. Tabellbegrensninger kan være enten brukerdefinerte eller systemdefinerte. En brukerdefinert tabellbegrensning er en matrisetype som kan brukes til å beskrive settet med kombinasjoner for attributtverdiene som er angitt av attributtyper. Hvis for eksempel høyttalere blir produsert, kan matrisen for en brukerdefinert tabellbegrensningen inneholde kolonner for høyttalerutførelse og grill.</li>
</ul>
<strong>Eksempel</strong> Høyttalere som er tilgjengelige i fire utførelser: svart, eik, Rosewood og hvitt. Høyttalerne kan ha én av tre frontgriller: svart, metall eller hvit. Svart er tilgjengelig for alle griller, men de andre utførelsene er begrenset til spesifikke griller. Tabellen nedenfor viser et eksempel på informasjonen som vises i fanen <strong>Tillatte kombinasjoner</strong> på siden <strong>Rediger tabellbegrensning</strong>.
<table>
<thead>
<tr class="header">
<th>Kabinettyper</th>
<th>Frontgrill</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Svart</td>
<td>Svart</td>
</tr>
<tr class="even">
<td>Svart</td>
<td>Metall</td>
</tr>
<tr class="odd">
<td>Svart</td>
<td>Hvit</td>
</tr>
<tr class="even">
<td>Eik</td>
<td>Svart</td>
</tr>
<tr class="odd">
<td>Rosewood</td>
<td>Hvit</td>
</tr>
<tr class="even">
<td>Hvit</td>
<td>Svart</td>
</tr>
<tr class="odd">
<td>Hvit</td>
<td>Hvit</td>
</tr>
</tbody>
</table>
En systemdefinert tabellbegrensning representerer en tilordning mellom et attributtype og et felt i en Supply Chain Management-tabell. En systemdefinert tabellbegrensning kobler dynamisk attributtypen til feltet. Koblingen gjør det mulig for attributtet i en produktkonfigurasjonsmodell å gjenspeile dataene i feltet i Supply Chain Management-tabellen.</td>
</tr>
<tr class="odd">
<td>Beregninger</td>
<td>Beregninger representerer et supplement til begrensninger. Du kan bruke en beregning til å utføre aritmetiske operasjoner på attributtene av typen <strong>Desimal</strong> og <strong>Heltall</strong> eller logiske operasjoner som involverer attributter av <strong>Tekst</strong> med en fast liste og <strong>Boolske</strong> typer. En beregning har et målattributt som inneholder resultatet av beregningsuttrykket. Beregningsuttrykket bygges ved hjelp av uttrykksredigering.</td>
</tr>
<tr class="even">
<td>Underkomponenter</td>
<td>Delkomponenter gjenspeiler strukturen til produktkonfigurasjonsmodellen. Du kan bruke delkomponenter til å bygge strukturen til produktkonfigurasjonsmodellen. Delkomponenter refererer eksisterende komponenter. Delkomponenter oppfordrer derfor til gjenbruk av komponenter i flere produktkonfigurasjonsmodeller. På siden <strong>Detaljer om stykklistelinje</strong> for en delkomponent kan du velge en spesifikk verdi for delkomponenten. Du kan også velge et attributt som du velger verdi for under konfigurasjonen av produktkonfigurasjonsmodellen. Hvis du vil inkludere en komponent eller delkomponent, må du angi følgende informasjon på siden <strong>Opprett produkt</strong> når du oppretter produktet:
<ul>
<li>Velg <strong>Element</strong> i feltet <strong>Produkttype</strong>.</li>
<li>Velg <strong>Produktstandard</strong> i feltet <strong>Produktets undertype</strong>.</li>
<li>I feltet <strong>Konfigurasjonsteknologi</strong> velger du <strong>Restriksjonsbasert konfigurasjon</strong>.</li>
</ul>
Du kan vise om et utgitt produkt kan brukes som en komponent eller delkomponent i fanen <strong>Generelt</strong> på siden <strong>Detaljer om frigitt produkt</strong>. Hvis <strong>Restriksjonsbasert konfigurasjon</strong> er valgt i feltet <strong>Konfigurasjonsteknologi</strong>, kan produktet brukes som en komponent eller delkomponent. Du kan skjule delkomponenter, slik at de ikke vises for brukeren under en konfigurasjonsøkt. Attributter, delkomponenter og brukerkrav som er tilknyttet delkomponenten, skjules også.</td>
</tr>
<tr class="odd">
<td>Brukerkrav</td>
<td>Brukerkrav representerer en abstraksjon mellom brukerkrav og spesifikke komponenter og attributter. Du kan ikke tilordne brukerkrav til en vare. En kunde er for eksempel på jakt et etter hjemmekinosystem. Selgeren kan spørre om størrelsen på rommet det kunden skal montere systemet, for å finne avgjøre hvor mange watt som kreves. I dette eksemplet kan romstørrelsen være et brukerkrav som bidrar til å finne riktig attributtverdi for en spesifikk komponent. Du kan skjule brukerkrav, slik at de ikke vises for brukeren under en konfigurasjonsøkt. Attributter, delkomponenter og brukerkrav som er tilknyttet brukerkravet, skjules også. Du kan skrive en betingelse for å styre om et brukerkrav kan skjules. Du må skrive betingelsen ved hjelp av OML-modellsyntaks (Optimization Modeling Language).</td>
</tr>
<tr class="even">
<td>Stykklistelinjer</td>
<td>Stykklistelinjer representerer de individuelle materialene for komponentene i produktkonfigurasjonsmodellen. På siden <strong>Detaljer om stykklistelinje</strong> er alle varer valgbare. Det kan legges til en betingelse på stykklistelinjen, slik at stykklistelinjer som velges for en spesifikk produktvariant, kan variere basert på brukerens valg når produktkonfigurasjonsmodellen konfigureres. Betingelser er uttrykk som må oppfylles for at attributter, stykklistelinjer og ruteoperasjoner skal inkluderes i en produktkonfigurasjonsmodell. På siden <strong>Detaljer om stykklistelinje</strong> kan du velge en spesifikk verdi. Du kan også tilordne til et attributt at verdien er valgt når produktkonfigurasjonsmodellen konfigureres.</td>
</tr>
<tr class="odd">
<td>Ruteoperasjoner</td>
<td>På siden <strong>Detaljer om ruteoperasjon</strong> kan du velge en spesifikk verdi. Du kan også tilordne til et attributt at verdien er valgt når produktkonfigurasjonsmodellen konfigureres. Betingelser skrives som uttrykksbegrensninger. Betingelser er uttrykk som må oppfylles for at attributter, stykklistelinjer og ruteoperasjoner skal inkluderes i en produktkonfigurasjonsmodell.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]