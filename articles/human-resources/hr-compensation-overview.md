---
title: Kompensasjonsplaner
description: Kompensasjons- og fordelsansvarlige kan bruke kompensasjonsstyring til å vedlikeholde og behandle faste og variable kompensasjonsplaner for ansatte i organisasjonen.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1be212cae4b0df136bb19b9521fd80aa29f7e094
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793759"
---
# <a name="compensation-plans"></a>Kompensasjonsplaner

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kompensasjons- og fordelsansvarlige kan bruke kompensasjonsstyring til å vedlikeholde og behandle faste og variable kompensasjonsplaner for ansatte i organisasjonen.

### <a name="introduction"></a>Innledning

Kompensasjonsstyring brukes til å kontrollere levering av grunnlønn og bonuser. En ansatts faste grunnlønn og personlige tilleggsøkninger styres via faste kompensasjonsplaner. Betaling av insitamentutbetalinger, for eksempel bonuser, ytelsestillegg, aksjeopsjoner og tilskudd, og også engangsbonuser, kontrolleres via variable kompensasjonsplaner. 

Ansatte kan knyttes til én eller flere planer av begge typer. En ansatt må oppfylle følgende krav for å være kvalifisert for registrering i en kompensasjonsplan:
-   Den ansatte må ha en aktiv stillingstilordningen.
-   Den ansatte må overholde kriteriene som er definert av rettighetsreglene for en kompensasjonsplan.

## <a name="compensation-setup"></a> Kompensasjonsoppsett
Tabellen nedenfor viser komponenter i kompensasjonsprosessen som kan være integrert i oppsettet av selskapets kompensasjonsplaner.

<table>
<thead>
<tr class="header">
<th>Komponent</th>
<th>Mer informasjon ...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Handlinger for fast kompensasjon</td>
<td>Faste kompensasjonshandlinger har to formål:
<ul>
<li>Handlinger kan angi hvilken type informasjon som må registreres når kompensasjonen til en ansatt endres. Du kan for eksempel kreve at årsaken til at en endring, for eksempel en forfremmelse eller degradering, registreres.</li>
<li>Handlinger kan sikre at en beregning brukes når planer for fast kompensasjon er behandlet.  Eksempelvis vil handlinger av typen Egenkapital sammenligne ansattbetalingen med minste referansepunkt for nivået for den ansatte og sikre at den ansatte betales minst minimum.</li>
</ul></td>
</tr>
<tr class="even">
<td>Nivåer</td>
<td>Nivåer er tilknyttet jobber og stillinger som er relatert til en jobbreferanse. Du kan opprette atskilte nivåer for tre typer kompensasjonsplaner: Segment, Klasse og Trinn.</td>
</tr>
<tr class="odd">
<td>Områdeutnyttelsesmatrise</td>
<td>En områdeutnyttelsesmatrise hjelper deg med å overføre ansatte til kontrollpunktet for jobben. Du kan også bruke områdeutnyttelse til å kontrollere lønnssatsens egenkapital i firmaet uten å ta hensyn til enkeltansattes ytelse eller firmaets totale ytelse. Eksempelvis får ansatte som mottar lavere betaling i sitt område, høyere prosentøkninger enn ansatte som blir betalt høyere i området. På denne måten kan du systematisk forskyve egenkapitalforskjeller. Områdeutnyttelsen beregnes på følgende måte: (fast lønnssats - minimumsområde) ÷ (maksimumsområde - minimumsområde).</td>
</tr>
<tr class="even">
<td>Referansepunktoppsett</td>
<td>Et referansepunktoppsett inneholder et sett med referansepunkt som utgjør områder i en matrise. Hvert område kan knyttes til en lønnssats. Eksempelvis har segmentplaner often referansepunktene Minimum, Midtpunkt og Maksimum.</td>
</tr>
<tr class="odd">
<td>Kompensasjonsmatrise</td>
<td>En kompensasjonsmatrise er et sett med referansepunkt og nivåer du bruker til å opprette en kompensasjonsstruktur.</td>
</tr>
<tr class="even">
<td>Kompensasjonsstruktur</td>
<td>En kompensasjonsstruktur er en kompensasjonsmatrise med lønnssatser som er knyttet til referansepunkt for hvert nivå.</td>
</tr>
<tr class="odd">
<td>Rettighetsregler</td>
<td>Rettighetsregler brukes til å identifisere ansatte i bestemte jobber, jobbfunksjoner, jobbtyper, avdelinger, fagforeninger eller kompensasjonsområder som dekkes av spesifikke kompensasjonsplaner. Du må opprette rettighetsregler for både variable og faste kompensasjonsplaner for å registrere ansatte i planen. Når du har angitt rettighetsregler for en kompensasjonsplan, kan du definere nivåene som skal gjelde for jobbene som dekkes av planen.</td>
</tr>
<tr class="even">
<td>Lønnsfrekvenser</td>
<td>Lønnsfrekvenser brukes til å definere tidsperioden som er angitt for kompensasjon.  Eksempelvis hjelper lønnsfrekvensen deg med å forstå om kompensasjonsbeløpet er angitt som en årslønn kontra en timelønn. Lønnsfrekvenser er også brukt til å definere omregningsfaktorer for å konvertere kompensasjonsbeløp fra frekvensen månedlig, ukentlig, lønn annenhver uke og timelønn til en årlig lønnsfrekvens.</td>
</tr>
<tr class="odd">
<td>Kompensasjonsregioner</td>
<td>Kompensasjonsregioner brukes til å angi ansattkompensasjon på grunnlag av arbeidsstedets lokasjon.</td>
</tr>
<tr class="even">
<td>Kontrollpunkt</td>
<td>Kontrollpunktet angir hva du anser som ideell lønnssats for alle ansatte på et gitt kompensasjonsnivå. Kontrollpunkt er normalt områdenes midtpunkt for kategoriplanstrukturer. Segmentstrukturer bruker sjelden kontrollpunkt. Du kan angi kontrollpunktet for en fast kompensasjonsplan i skjemaet Faste kompensasjonsplaner.</td>
</tr>
<tr class="odd">
<td>Jobbfunksjoner</td>
<td>Jobbfunksjoner brukes til å klassifisere og filtrere kompensasjonsplaner til bestemte jobber.</td>
</tr>
<tr class="even">
<td>Jobbtyper</td>
<td>Jobbtyper brukes til å klassifisere og filtrere kompensasjonsplaner til bestemte jobber.</td>
</tr>
<tr class="odd">
<td>Typer av variabel kompensasjon</td>
<td>Typer av variabel kompensasjon, for eksempel aksjebelønninger eller kontantbonusbelønninger, blir brukt i variable kompensasjonsplaner.</td>
</tr>
<tr class="even">
<td>Kompensasjonsrutenett</td>
<td>Kompensasjonsrutenett inneholder kompensasjonsstrukturen.  Kompensasjonsrutenett kan brukes av én eller flere kompensasjonsplaner.</td>
</tr>
<tr class="odd">
<td>Ytelsesplaner</td>
<td>Ytelsesplaner brukes til å knytte ytelse til en fordelingsmatrise slik at du kan bruke planen i en betal-for-ytelse-strategi.</td>
</tr>
<tr class="even">
<td>Ytelsesvurdering</td>
<td>Ytelsesvurderinger brukes i ytelsesplaner for å fastsette belønningsbeløp i form av personlige tillegg eller ytelsestillegg.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Prosesshendelser
En prosesshendelse beregner kompensasjonsinformasjon for en bestemt periode for alle ansatte som er registrert i én eller flere faste eller variable kompensasjonsplaner. Du kan kjøre en prosesshendelse gjentatte ganger for å teste eller oppdatere beregnede kompensasjonsresultater.

<a name="compensation-events"></a>Kompensasjonshendelser
-------------------

Hver gang en prosesshendelse kjøres, opprettes en kompensasjonshendelse.  Kompensasjonshendelser inneholder resultatene av kompensasjonsprosessen for hver ansatt som er inkludert i prosesshendelsen.  Når beregningene er riktige, kan du laste inn kompensasjonshendelsen for å oppdatere kompensasjonsposter for ansatte som er berørt av prosesshendelsen.

## <a name="recommendations"></a> Anbefalinger
Når du kjører en prosesshendelse, kan du anbefale justeringer for en ansatts personlige tilleggsøkning eller bonusbeløp basert på de beregnede retningslinjeøkningene for prosesshendelsen. Hvis du gjøre anbefalinger for ansatte, må du aktivere anbefalinger når du definerer kompensasjonsplaner, eller når du definerer prosesshendelsen.





[!INCLUDE[footer-include](../includes/footer-banner.md)]