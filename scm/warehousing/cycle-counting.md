---
title: Syklustelling
description: "Denne artikkelen beskriver hvordan du kan bruke syklustelling med datalagerstyringsløsningen som er tilgjengelig i Lagerstyring. Denne artikkelen gjelder ikke for datalagerstyringsløsningen som er tilgjengelig i Beholdningsstyring."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4446dfec1fa8eabb45e14b3f2ff685b3b1d68e2c
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="cycle-counting"></a>Syklustelling

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du kan bruke syklustelling med datalagerstyringsløsningen som er tilgjengelig i Lagerstyring. Denne artikkelen gjelder ikke for datalagerstyringsløsningen som er tilgjengelig i Beholdningsstyring.

Syklustelling er en lagerprosess som du kan bruke til å overvåke varer i lagerbeholdning. Prosessen for syklustelling kan beskrives i tre trinn:

1.  **Opprette syklustellingsarbeid** – Syklustellingsarbeid kan opprettes automatisk basert på terskelparameterne for varer, eller ved å bruke en syklustellingsplan. Du kan også opprette syklustellingsarbeid manuelt ved hjelp av vare- eller lagerparameterne på siden **Syklustellingsarbeid etter vare** eller siden **Syklustellingsarbeid etter lokasjon**.
2.  **Behandle syklustellingen** – Når du har opprettet syklustellingsarbeid, utfører du syklustellingsarbeidet ved å telle varene på en lagerlokasjon og bruker deretter en mobilenhet til å angi resultatet i Microsoft Dynamics 365 for Operations. Alternativt kan du telle varer i en lagerlokasjon uten å opprette syklustellingsarbeid. Denne prosessen kalles *spotsyklustelling*.
3.  **Rette opp differanser i tellingsverdien** – Etter en syklustelling får alle varer som har differanser i tellingsverdien, arbeidsstatusen **Venter på gjennomgang** på **Alt arbeid**-siden. Du kan løse disse forskjellene på siden **Syklustellingsarbeid venter på gjennomgang**.

Illustrasjonen nedenfor viser syklustellingsprosessen. ![Behandle flyt for syklustelling](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Forhåndskrav for syklustelling
Tabellen nedenfor viser forutsetninger som må være på plass før du kan bruke syklustelling.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forutsetning</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vare</td>
<td>Varn må aktiveres for lagerstyringsprosesser.</td>
</tr>
<tr class="even">
<td>Lager</td>
<td>Lageret må aktiveres for lagerstyringsprosesser. Hvis du vil aktivere lageret for lagerstyringsprosesser, går du til siden <strong>Lagre</strong>, velger lageret og merker deretter av for <strong>Bruk lagerstyringsprosesser</strong>. Hvis du vil gi brukerne mulighet til å flytte paller under en syklustelling, går du til hurtigkategorien <strong>Lagerstyring</strong> og merker av for <strong>Tillat flytting av pall under syklustelling</strong>.</td>
</tr>
<tr class="odd">
<td>Arbeidsutvalg</td>
<td>Valgfritt: Opprett et arbeidsutvalg for å skille lagerarbeidet, basert på typen arbeid (i dette tilfellet syklusopptellingsarbeid).</td>
</tr>
<tr class="even">
<td>Lokasjoner</td>
<td>Aktiver syklustelling for lokasjoner. Hvis du vil aktivere syklustelling for en lagerlokasjon, går du til siden <strong>Lokasjonsprofiler</strong> og merker av for <strong>Tillat syklustelling</strong>.</td>
</tr>
<tr class="odd">
<td>Lagerstyringsparametere</td>
<td>Konfigurer parametere for syklustelling. På siden <strong>Lagerstyringsparametere</strong> angir du standard justeringstypekode, arbeidsklasse-ID og arbeidsprioriteten for syklustelling.</td>
</tr>
<tr class="even">
<td>Mobilenhet</td>
<td><ul>
<li>Opprett et menyelement for én av følgende metoder på siden <strong>Menyelementer på mobilenheten</strong>:
<ul>
<li>Brukerstyrt syklustelling</li>
<li>Systemstyrt syklustelling</li>
<li>Gruppering av syklustelling</li>
<li>Spotsyklustelling</li>
</ul>
</li>
<li>Konfigurer en meny for mobilenheten.</li>
<li>Opprett en arbeidsbrukerkonto, og tilordne en meny for mobilenhet arbeidsbruker-IDen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Relatert oppgave for oppsett</td>
<td>Definer en syklustellingsplan for en lagerlokasjon.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Opprett syklustellingsarbeid automatisk
Det finnes to metoder for å planlegge regelmessig oppretting av syklustellingsarbeid: definere grenseverdier for syklustelling, eller definere planer for syklustelling.

-   En syklustellingsterskel angir antall- eller prosentgrensen for lagervarer. Syklustellingsarbeid opprettes automatisk når terskelgrensen er nådd.
-   En syklustellingsplan oppretter syklustellingsarbeid umiddelbart eller med jevne mellomrom gjennom en satsvis jobb. Når syklustellingsarbeid opprettes, inneholder tellingsarbeidslinjen informasjon om lokasjonen som skal telles. Lagerbeholdningen som er knyttet til denne lokasjonen, er ikke blokkert, og er derfor tilgjengelig for reservering og utgående behandling, selv om det finnes åpent tellingsarbeid.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Opprette syklustellingsarbeid basert på terskelparameterne for varer

Syklustellingsarbeid kan opprettes når antallet varer synker under en bestemt terskelverdi på en lokasjon. Det finnes for eksempel 60 elementer på en lokasjon der terskelverdien for syklustelling er 40. Under en salgsordretransaksjon plukkes 25 varer fra lokasjonen og plasseres i en oppsamlingslokasjon. Siden det nye vareantallet på 35 er mindre enn terskelantallet, opprettes syklustellingsarbeid automatisk for lokasjonen.

### <a name="schedule-cycle-counting-work"></a>Planlegge syklustellingsarbeid

Du kan planlegge at syklustellingsplaner skal opprette syklustellingsarbeid umiddelbart eller med jevne mellomrom. Ved å definere planer for syklustelling kan du styre arbeidsutvalget som syklustellingsarbeidet er opprettet for, det maksimale antallet syklusentellinger som opprettes for varer på forskjellige lokasjoner, og antallet dager før en lagerlokasjon telles på nytt. Eksempel: En vare er tilgjengelig på tre lokasjoner i lageret, og det maksimale antallet syklustellinger er satt til **2**. Når du kjører syklustellingsplanen i dette tilfellet, opprettes to syklustellinger for de to lokasjonene der varen finnes. Et annet eksempel: Du angir antall dager mellom syklustellingene til **5**. I så fall opprettes syklustellingsarbeid hver femte dag. Hvis syklustellingsarbeid imidlertid behandles på dag tre, opprettes neste syklustellingsarbeid fem dager etter den siste syklustellingen ble behandlet, på dag åtte.

## <a name="create-cycle-counting-work-manually"></a>Opprette syklustellingsarbeid manuelt
Hvis du vil opprette syklustellingsarbeid manuelt, kan du bruke siden **Syklustellingsarbeid etter vare** eller **Syklustellingsarbeid etter lokasjon**. Du kan angi det maksimale antallet syklustellinger som kan opprettes om gangen. Hvis lagersjefen for eksempel angir en verdi på fem, opprettes syklustellingsarbeid for **fem** lokasjoner selv om varen finnes på ti lokasjoner. Du kan også velge en arbeisdpulje-ID som syklustellingsarbeids-ID-ene som er opprettet, skal tilordnes til. Når en arbeidspulje-ID behandles for syklustelling, vil arbeids-ID-en for syklustellingen som er tilordnet denne arbeidspuljen bli behandlet som en gruppe.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Utføre en syklustelling ved hjelp av en mobilenhet
Det finnes flere metoder for å behandle syklustellingsarbeid ved hjelp av Microsoft 365 for Operations på en mobilenhet:

-   **Brukerstyrt** – Arbeideren kan angi en arbeids-ID for syklustelling som har statusen **Åpen**.
-   **Systemstyrt** – Dynamics 365 for Operations tilordner en arbeids-ID for syklustelling til arbeideren.
-   **Gruppering av syklustelling** – Arbeideren kan gruppere ID-er for syklustellingsarbeid som er spesifikke for en bestemt lokasjon, sone eller arbeidspulje.
-   **Spotsyklustelling** – Arbeideren kan telle varer på en lagerlokasjon når som helst, uten å opprette syklustellingsarbeid, ved å angi en lokasjons-ID. For å utføre syklustelling på en lokasjon, må arbeideren angi ID-en for lokasjonen.

Følgende eksempel viser hvordan du kan utføre spotsyklustelling ved hjelp av en mobilenhet. Instruksjonene som arbeideren ser på enheten, varierer avhengig av oppsettet av menyelementet for spotsyklustelling.

1.  På mobilenheten velger du menyelementet for å behandle spotsyklustellingsarbeid.
2.  Registrere lokasjonen som spotsyklustelling skal utføres for.
3.  Registrer og bekreft varenummeret og vareantallet som er telt opp. **Obs!** Statusen for syklustellingsarbeidet oppdateres til **Venter på gjennomgang** eller **Lukket** på **Alt arbeid**-siden, avnehgig av parameterne som er angitt på **Arbeider**-siden.
4.  Valgfritt: Gjenta trinn 3 for de gjenværende varene på lokasjonen, og bekreft at det ikke finnes flere varer som er tilgjengelig for opptelling.

## <a name="resolve-cycle-counting-differences"></a>Løse syklustellingsdifferanser
Det oppstår en syklustellingsdifferanse i følgende scenarier: hvis **Er en syklustellingsansvarlig** er angitt til **Nei** for en arbeidsbruker-ID:

-   Verdien for syklustellingen ikke er innenfor avviksgrensene som er angitt i feltene **Grense for største prosent** eller **Grense for største antall** på siden **Arbeidsbrukere**. Lagerbeholdningsantallet på en lokasjon er for eksempel 50, og avviksgrensen for arbeidsbrukeren er 10. Hvis arbeidsbrukeren angir en verdi som ikke er mellom 40 og 60, oppstår det en forskjell.
-   Den opptalte verdien avviker fra lagerbeholdningsantallet, og det er ikke angitt avviksgrenser.

Du kan justere forskjeller i den opptelte verdien og deretter godta den opptelte verdien på siden **Syklustelling venter på gjennomgang**. Du kan kontrollere den endrede tellingen av vareantallet på siden **Beholdning etter lokasjon**. Tellingsverdien avvises hvis forskjellen ikke kan godkjennes.

# <a name="see-also"></a>Se også
[Konfigurere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md)




