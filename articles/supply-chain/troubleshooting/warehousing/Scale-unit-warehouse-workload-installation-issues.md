---
title: Behandlingsproblemer oppstår etter at en lagerarbeidsbelastning for en storskalaenhet er installert
description: Dette emnet beskriver problemer som kan oppstå rett etter at en lagerarbeidsbelastning for en storskalaenhet er installert, og gir veiledning for å løse dem.
author: perlynne
ms.date: 1/13/2022
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningWorkbench, WHSOutboundLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-01-13
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f589ffed61b695f471989ab1dd693f30cd5d5262
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071656"
---
# <a name="processing-issues-occur-after-a-scale-unit-warehouse-workload-is-installed"></a>Behandlingsproblemer oppstår etter at en lagerarbeidsbelastning for en storskalaenhet er installert

Dette emnet beskriver problemer som kan oppstå rett etter at en lagerarbeidsbelastning for en storskalaenhet er installert, og gir veiledning for å løse dem.

## <a name="issue-1-error-after-a-load-is-released-from-a-load-planning-workbench"></a>Problem 1: Feil etter at en belastning er frigitt fra en workbench for belastningsplanlegging

### <a name="symptoms-of-issue-1"></a>Symptomer på problem 1

Når du frigir en belastning fra siden **Workbench for belastningsplanlegging** eller **Workbench for utgående belastningsplanlegging**, får du en feilmelding i følgende format:

> Det ble registrert et unntak ved postering av belastning %1. Belastningen kan ikke frigis.
> 
> OPPDATER WHSSHIPMENTTABLE SET ...
> 
> Kan ikke redigere en post i Forsendelser (WHSShipmentTable). Forsendelses-ID: ...

Her er et faktisk eksempel som inneholder eksempeldata:

> Det ble registrert et unntak ved postering av belastning USMF-000033. Belastningen kan ikke frigis.
økt 5133 (Admin)
>
> OPPDATER WHSSHIPMENTTABLE SET ORDERNUM=?,RECVERSION=?,MODIFIEDDATETIME=?,MODIFIEDBY=? DER ((RECID=?) OG (RECVERSION=?))  
> [Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Storskalaenhet @@ forsøkte å oppdatere poster som eies av storskalaenhet @A.  
> Object Server Azure:
>
> Kan ikke redigere en post i Forsendelser (WHSShipmentTable). Forsendelses-ID: USMF-000031, USMF-000033. SQL-databasen har utstedt en feil.

### <a name="cause-of-issue-1"></a>Årsak til problem 1

Dette problemet kan oppstå hvis følgende kombinasjon av betingelser finnes når du installerer lagerarbeidsbelastningen for storskalaenheten:

- Systemet omfatter en ikke-frigitt belastning der flere linjer er knyttet til ulike ordrer, og enkelte belastningslinjer som ikke er tilknyttet en forsendelse.
- Systemet er satt opp for å bruke forsendelseskonsolidering.

I en distribuert hybridtopologidistribusjon merkes hver belastnings- og forsendelsespost som eid av en bestemt storskalaenhet eller et senter. Når du frigir en belastning fra siden **Arbeidsområde for lastplanlegging**, endrer systemet det tilordnede eierskapet. På grunn av de tidligere oppførte vilkårene kan det imidlertid hende at systemet ikke kan løse dataeierskapet. Derfor mislykkes det å frigi belastningen til lageret.

### <a name="resolution-of-issue-1"></a>Løsning på problem 1

Del belastningen i to mindre belastninger før du frigir den til lageret.

## <a name="issue-2-error-while-a-wave-is-processed-on-a-scale-unit"></a>Problem 2: Feil under behandling av en bølge på en storskalaenhet

### <a name="symptoms-of-issue-2"></a>Symptomer på problem 2

Når du behandler en bølge på en storskalaenhet, får du en feilmelding i følgende format:

> Du kan ikke endre belastningslinjen med RecId = %1, load id= %2, siden den fortsatt eies av bedriftssenteret. Kontroller at tilsvarende utgående belastning er frigitt til storskalaenhet, og dermed har opprettet lagerordrelinjer.

Her er et faktisk eksempel som inneholder eksempeldata:

> Infologg for jobben Kjør bølge USMF-000000012 (9223377668365210)  
> Infologg for oppgaven Kjør bølge USMF-000000012 (9223377668370462)  
> Du kan ikke endre belastningslinjen med RecId = 68719478242, load id= USMF-000034, siden den fortsatt eies av bedriftssenteret. Kontroller at tilsvarende utgående belastning er frigitt til storskalaenhet, og dermed har opprettet lagerordrelinjer.

### <a name="cause-of-issue-2"></a>Årsak til problem 2

I en distribuert hybridtopologidistribusjon er eierskapet av belastnings- og forsendelsesdataene tilordnet til en bestemt storskalaenhet eller et senter. Som en del av bølgebehandlingen forventes det at eierskapet av dataene blir tilordnet til en storskalaenhet.

Når du installerer en lagerarbeidsbelastning for en storskalaenhet, og hvis en åpen forsendelse er knyttet til en belastning og en bølge, kan ikke systemet kontrollere dataeierskapet. Derfor mislykkes bølgebehandlingen på storskalaenheten.

### <a name="resolution-of-issue-2"></a>Løsning på problem 2

Frigi belastningen til lageret fra senteret.

## <a name="troubleshoot-issues-by-viewing-a-records-ownership-and-destination"></a>Feilsøke problemer ved å vise en posts eierskap og mål

I en distribuert hybridtopologidistribusjon merkes mange typer poster som eid av en bestemt storskalaenhet eller et senter. Når du har byttet til en distribuert hybridtopologi og/eller konfigurert en ny lagerarbeidsbelastning for en storskalaenhet, tilordner systemet eierskap til hver relevante post. Denne prosessen kan noen ganger forårsake feil eller gi uventede resultater. Derfor kan informasjonen om en posts eierskap og overføringsmålet hjelpe deg med å feilsøke problemer som oppstår etter at du har gjort disse typene endringer.

Følg disse trinnene for å vise eierskap og overføringsmål for en post.

1. Åpne den relevante posten.
1. Velg **Vis alle felter** i gruppen **Postinformasjon** på fanen **Alternativer** i handlingsruten.
1. Siden som vises, viser verdier for alle feltene som er tilgjengelige for den valgte posten. Gå gjennom følgende felt:

    - **SYSSCALEUNITID** – Dette feltet viser den gjeldende eieren av posten.
    - **SYSTARGETSCALEUNITID** – Dette feltet viser storskalaenhets-ID-en til senteret eller storskalaenheten som posten blir overført til, når den gjeldende eieren er ferdig med arbeidet med den. Verdien i dette feltet brukes av satsvise jobber som administrerer denne typen prosess. Selv om dette feltet ikke er direkte knyttet til eierskap, kan eierskapet endres når posten overføres. I noen tilfeller er dette feltet tomt.
