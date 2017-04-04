---
title: Timeregistrering for detaljhandel
description: "Dette emnet beskriver scenarier som støttes for tid og fremmøte management i Microsoft Dynamics 365 for operasjoner - handel."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>Timeregistrering for detaljhandel

Dette emnet beskriver scenarier som støttes for tid og fremmøte management i Microsoft Dynamics 365 for operasjoner - handel. 

<a name="manage-worker-setup-and-scheduling"></a>Behandle arbeideren installasjon og planlegging
----------------------------------

### <a name="initial-configuration"></a> Opprinnelig konfigurasjon

-   Kjør konfigurasjonsveiviseren.
-   Registrer arbeidere som timeregistreringsarbeidere.

### <a name="plan-worker-schedules"></a>Planlegge tidsplaner for arbeidere

-   Bruk profiler ved hjelp av jobbplanleggeren. Hvis du vil ha mer informasjon, se <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Hvis du vil ha informasjon om konfigurasjonstrinnene, kan du se <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Detaljhandelsspesifikk konfigurasjon

-   Aktiver en funksjonalitetsprofil for tidsklokke, for arbeidere som du vil aktivere tidsregistreringer for. Klikk **POS-funksjonalitetsprofiler**&gt;**funksjoner**&gt;**POS tid registreringer**&gt;**Aktiver tidsregistreringer**.
-   Konfigurer grupper for tillatelser for salgssted for å aktivere tillatelsen Vis tidsklokkeoppføringer. Med denne tillatelsen kan en bruker vise tidsklokkeregistreringene for andre arbeidere i butikken (og fra alle andre butikker som brukeren er tilknyttet, via adresseboken). Du vil kanskje aktivere denne tillatelsen for en lederrolle, men ikke en kassererrolle. Klikk **Salgsstedstillatelsesgrupper**&gt;**Vis klokke oppføringer**.

## <a name="register-time"></a>Kassetid
### <a name="cashier-and-non-cashier-time-registrations"></a>Tidsregistreringer for kasserer og ikke-kasserer

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
    -   Hvis du viser tiden fra en annen lokasjon (for kassererens loggbok eller ved hjelp av **Vis tidsklokkeoppføringer** for et lederscenario), og den er i en annen tidssone, blir tidspostene som du ser, konvertert til den lokale tidssonen. Du kan for eksempel er en leder for to butikker, i Arizona og den andre i Nevada. En kasserer registrerer en innstempling klokken 9:00. I Arizona. På dette tidspunktet er klokken 8:00 i Nevada. Derfor, hvis du er i butikken i Nevada og ser på timeregistreringsposter, er timeregistreringen merket som 8:00.

## <a name="view-worker-time-registrations"></a>Vis tidsregistreringer for arbeideren
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Vis tidsregistreringer for arbeider, og filtrer etter butikk eller aktivitetstype

På salgssted:

-   Velg **Vis tidsklokkeoppføringer**.
-   Du kan se aktiviteter for tidsklokkeregistrering fra alle arbeidere som er tilordnet til de samme butikkene som du er tilordnet til.
-   Du kan bruke aktivitetstypen og butikkfiltre for å filtrere etter tidsregistreringer.

## <a name="process-and-manage-time-registrations"></a>Behandle og administrere tidsregistreringer
En Dynamics 365 for operasjoner - Retail bruker følger arbeidsflyten for å beregne, godkjenne og overføre tidsregistreringer til lønn.

### <a name="primary-operations"></a>Primære operasjoner

-   Beregn
-   Godkjenn
-   Send til lønn

### <a name="other-common-operations"></a>Andre vanlige operasjoner

-   Masseutstempling
-   Registrer fravær

Hvis du vil ha mer informasjon om hvordan du behandler tids- og fremmøteregistreringer, se <https://technet.microsoft.com/en-us/library/aa573180.aspx>.


