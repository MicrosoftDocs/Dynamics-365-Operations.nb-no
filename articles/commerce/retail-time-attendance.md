---
title: Administrere tid og fremmøte i Retail
description: Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Dynamics 365 Commerce.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cca5e3232450e75f931a621b278c134129fc745c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414762"
---
# <a name="time-and-attendance-management-in-retail"></a>Administrere tid og fremmøte i Retail

[!include [banner](includes/banner.md)]

Dette emnet beskriver scenarier som støttes for administrasjon av tid og fremmøte i Dynamics 365 Commerce.

## <a name="manage-worker-setup-and-scheduling"></a>Behandle konfigurasjon og planlegging for arbeider

### <a name="initial-configuration"></a> Opprinnelig konfigurasjon

- Kjør konfigurasjonsveiviseren.
- Registrer arbeidere som timeregistreringsarbeidere.

### <a name="plan-worker-schedules"></a>Planlegge tidsplaner for arbeidere

- Bruk profiler ved hjelp av jobbplanleggeren. Hvis du vil ha mer informasjon, kan du se [Bruke profiler ved hjelp av jobbplanlegger](https://technet.microsoft.com/library/aa551234.aspx).

Hvis du vil ha informasjon om konfigurasjonstrinnene, kan du se [Definere timeregistrering](https://technet.microsoft.com/library/aa496971.aspx).

### <a name="commerce-specific-configuration"></a>Spesifikk konfigurasjon for Commerce

- Aktiver en funksjonalitetsprofil for tidsklokke, for arbeidere som du vil aktivere tidsregistreringer for. Klikk på **Funksjonalitetsprofiler for salgssted** &gt; **Funksjoner** &gt; **Tidsregistreringer for salgssted** &gt; **Aktiver tidsregistreringer**.
- Konfigurer grupper for tillatelser for salgssted for å aktivere tillatelsen Vis tidsklokkeoppføringer. Med denne tillatelsen kan en bruker vise tidsklokkeregistreringene for andre arbeidere i butikken (og fra alle andre butikker som brukeren er tilknyttet, via adresseboken). Du vil kanskje aktivere denne tillatelsen for en lederrolle, men ikke en kassererrolle. Klikk på **Salgsstedstillatelsesgrupper** &gt; **Vis tidsklokkeoppføringer**.

## <a name="register-time"></a>Kassetid

### <a name="cashier-and-non-cashier-time-registrations"></a>Tidsregistreringer for kasserer og ikke-kasserer

- På salgssted:

    - Stemple inn operasjoner:

        - Logg på med en ikke-skuff-operasjon eller et nytt skift.
        - Velg en tidsklokkeoperasjon.
        - Velg en ønsket operasjon:

            - Innstempling
            - Arbeidspause
            - Lunsjpause
            - Utstempling

        <table>
        <thead>
        <tr>
        <th>Gjeldende tilstand</th>
        <th>Tilgjengelige operasjoner</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>Innstempling</td>
        <td>
        <ul>
        <li>Arbeidspause</li>
        <li>Lunsjpause</li>
        <li>Utstempling</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>Arbeidspause</td>
        <td>Innstempling</td>
        </tr>
        <tr>
        <td>Lunsjpause</td>
        <td>Innstempling</td>
        </tr>
        <tr>
        <td>Utstempling</td>
        <td>Innstempling</td>
        </tr>
        </tbody>
        </table>

        [![Tidsklokketilstander](./media/timeclockstates.png)](./media/timeclockstates.png)

- Vis bekreftelsesmeldingen, og valider at den gjeldende aktivitetstiden er riktig.
- Loggbok:

    - Klikk **Loggbok** for å vise tidsklokkeaktiviteten.
    - Bruk tidsfiltre for å velge forskjellige tidsvinduer.
    - Hvis du arbeider på flere butikklokasjoner, kan du se tidsregistreringene fra alle butikkene der du har registrert tid. Du kan bruke butikkfilteret for å vise tidsregistreringer fra en valgt butikk.

- Ulike tidssoner:

    - Hvis du viser tiden fra en annen lokasjon (for kassererens loggbok eller ved hjelp av **Vis tidsklokkeoppføringer** for et lederscenario), og den er i en annen tidssone, blir tidspostene som du ser, konvertert til den lokale tidssonen. Du er for eksempel en leder for to butikker, én i Arizona og den andre i Nevada. En kasserer registrerer en innstempling klokken 9:00 i Arizona. På dette tidspunktet er klokken 8:00 i Nevada. Derfor, hvis du er i butikken i Nevada og ser på timeregistreringsposter, er timeregistreringen merket som 8:00.

## <a name="view-worker-time-registrations"></a>Vise tidsregistrering for arbeidere

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Vis tidsregistreringer for arbeider, og filtrer etter butikk eller aktivitetstype

På salgssted:

- Velg **Vis tidsklokkeoppføringer**.
- Du kan se aktiviteter for tidsklokkeregistrering fra alle arbeidere som er tilordnet til de samme butikkene som du er tilordnet til.
- Du kan bruke aktivitetstypen og butikkfiltre for å filtrere etter tidsregistreringer.

## <a name="process-and-manage-time-registrations"></a>Behandle og administrere tidsregistreringer

En Commerce-bruker følger arbeidsflyten for å beregne, godkjenne og overføre tidsregistreringer til lønn.

### <a name="primary-operations"></a>Primære operasjoner

- Beregn
- Godkjenn
- Send til lønn

### <a name="other-common-operations"></a>Andre vanlige operasjoner

- Masseutstempling
- Registrer fravær

Hvis du vil ha mer informasjon om hvordan du behandler registreringer av timeregistrering, kan du se [Behandle registreringer av timeregistrering](https://technet.microsoft.com/library/aa573180.aspx).


[!INCLUDE[footer-include](../includes/footer-banner.md)]