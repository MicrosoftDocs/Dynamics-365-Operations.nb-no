---
title: Timeregistrering for detaljhandel
description: "Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Microsoft Dynamics 365 for Retail."
author: MargoC
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: b458d1938f49a2f33f7dd3ce3062880f0d4d7bfc
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017



---

# Timeregistrering for detaljhandel
<a id="retail-time-and-attendance" class="xliff"></a>

[!include[banner](includes/banner.md)]


Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Microsoft Dynamics 365 for Retail. 

Behandle konfigurasjon og planlegging for arbeider
<a id="manage-worker-setup-and-scheduling" class="xliff"></a>
----------------------------------

###  Opprinnelig konfigurasjon
<a id="initial-configuration" class="xliff"></a>

-   Kjør konfigurasjonsveiviseren.
-   Registrer arbeidere som timeregistreringsarbeidere.

### Planlegge tidsplaner for arbeidere
<a id="plan-worker-schedules" class="xliff"></a>

-   Bruk profiler ved hjelp av jobbplanleggeren. Hvis du vil ha mer informasjon, se <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Hvis du vil ha informasjon om konfigurasjonstrinnene, kan du se <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### Detaljhandelsspesifikk konfigurasjon
<a id="retail-specific-configuration" class="xliff"></a>

-   Aktiver en funksjonalitetsprofil for tidsklokke, for arbeidere som du vil aktivere tidsregistreringer for. Klikk på **Funksjonalitetsprofiler for salgssted** &gt; **Funksjoner** &gt; **Tidsregistreringer for salgssted** &gt; **Aktiver tidsregistreringer**.
-   Konfigurer grupper for tillatelser for salgssted for å aktivere tillatelsen Vis tidsklokkeoppføringer. Med denne tillatelsen kan en bruker vise tidsklokkeregistreringene for andre arbeidere i butikken (og fra alle andre butikker som brukeren er tilknyttet, via adresseboken). Du vil kanskje aktivere denne tillatelsen for en lederrolle, men ikke en kassererrolle. Klikk på **Salgsstedstillatelsesgrupper** &gt; **Vis tidsklokkeoppføringer**.

## Kassetid
<a id="register-time" class="xliff"></a>
### Tidsregistreringer for kasserer og ikke-kasserer
<a id="cashier-and-non-cashier-time-registrations" class="xliff"></a>

-   På salgssted:
    -   Stemple inn operasjoner:
        -   Logg på med en ikke-skuff-operasjon eller et nytt skift.
        -   Velg en tidsklokkeoperasjon.
        -   Velg en ønsket operasjon:
            -   Innstempling
            -   Arbeidspause
            -   Lunsjpause
            -   Utstempling

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Gjeldende tilstand</th>
    <th>Tilgjengelige operasjoner</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Innstempling</td>
    <td><ul>
    <li>Arbeidspause</li>
    <li>Lunsjpause</li>
    <li>Utstempling</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Arbeidspause</td>
    <td>Innstempling</td>
    </tr>
    <tr class="odd">
    <td>Lunsjpause</td>
    <td>Innstempling</td>
    </tr>
    <tr class="even">
    <td>Utstempling</td>
    <td>Innstempling</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Vis bekreftelsesmeldingen, og valider at den gjeldende aktivitetstiden er riktig.
-   Loggbok:
    -   Klikk **Loggbok** for å vise tidsklokkeaktiviteten.
    -   Bruk tidsfiltre for å velge forskjellige tidsvinduer.
    -   Hvis du arbeider på flere butikklokasjoner, kan du se tidsregistreringene fra alle butikkene der du har registrert tid. Du kan bruke butikkfilteret for å vise tidsregistreringer fra en valgt butikk.

<!-- -->

-   Ulike tidssoner:
    -   Hvis du viser tiden fra en annen lokasjon (for kassererens loggbok eller ved hjelp av **Vis tidsklokkeoppføringer** for et lederscenario), og den er i en annen tidssone, blir tidspostene som du ser, konvertert til den lokale tidssonen. Du er for eksempel en leder for to butikker, én i Arizona og den andre i Nevada. En kasserer registrerer en innstempling klokken 9:00 i Arizona. På dette tidspunktet er klokken 8:00 i Nevada. Derfor, hvis du er i butikken i Nevada og ser på timeregistreringsposter, er timeregistreringen merket som 8:00.

## Vise tidsregistrering for arbeidere
<a id="view-worker-time-registrations" class="xliff"></a>
### Vis tidsregistreringer for arbeider, og filtrer etter butikk eller aktivitetstype
<a id="view-worker-time-registrations-and-filter-by-store-or-activity-type" class="xliff"></a>

På salgssted:

-   Velg **Vis tidsklokkeoppføringer**.
-   Du kan se aktiviteter for tidsklokkeregistrering fra alle arbeidere som er tilordnet til de samme butikkene som du er tilordnet til.
-   Du kan bruke aktivitetstypen og butikkfiltre for å filtrere etter tidsregistreringer.

## Behandle og administrere tidsregistreringer
<a id="process-and-manage-time-registrations" class="xliff"></a>
En Dynamics 365 for Retail bruker følger arbeidsflyten for å beregne, godkjenne og overføre tidsregistreringer til lønn.

### Primære operasjoner
<a id="primary-operations" class="xliff"></a>

-   Beregn
-   Godkjenn
-   Send til lønn

### Andre vanlige operasjoner
<a id="other-common-operations" class="xliff"></a>

-   Masseutstempling
-   Registrer fravær

Hvis du vil ha mer informasjon om hvordan du behandler tids- og fremmøteregistreringer, se <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




