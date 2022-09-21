---
title: Arbeiderhodekontroll
description: Denne artikkelen inneholder informasjon om den tilpassbare hodekontrollen i Ansattselvbetjening, i Personhub og på Arbeider-siden i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445951"
---
# <a name="worker-header-control"></a>Arbeiderhodekontroll

Microsoft Dynamics 365 Human Resources har en tilpassbar hodekontroll i **Ansattselvbetjening**, i **Personhub** og på den strømlinjeformede **Arbeider**-siden. Hodet inneholder viktig informasjon om arbeideren, og også enkeltklikkshandlinger som e-post, anrop eller meldinger. Hodet kan endres ved å fjerne felter eller legge til felter, inkludert egendefinerte felter, for å vise tilleggsinformasjon. Hvis du vil bruke den nye hodekontrollen, kan du gå til **Funksjonsbehandling** og aktivere funksjonen **Arbeiderhodekontroll**.

## <a name="personalization"></a>Tilpasning

En av hovedfordelene med kontroll av arbeiderhodet er muligheten til å tilpasse informasjonen som vises på hodet.

Øverst til høyre i hodet er det en gruppe på tre felter som viser ulike data, avhengig av statusen til den ansatte. Denne gruppen med felter kalles for søkelysdelen av hodet. Du kan tilpasse søkelysdelen av hodet ved å fjerne gjeldende felter eller legge til felter. Feltene som kan legges til i søkelysdelen i hodekontrollen, er forskjellige for **Ansattselvbetjening**, **Personer**-huben og **Arbeider**-siden.

## <a name="employee-self-service"></a>Ansattselvbetjening

Arbeiderhodet på siden **Ansattselvbetjening** inneholder følgende informasjon:

- Navn på arbeider
- Personalnummer
- Stillingstittel
- Avdelinger
- Arbeidertype
- Juridisk enhet for ansettelse
- Arbeidserfaring
- Rapporterer til (leder)
- Stillingstype

Hodet inneholder også en enkeltklikkhandling for å redigere personens personlige opplysninger. Velg **Rediger personopplysninger** for å åpne siden **Personlige opplysninger** i **Ansattselvbetjening**.

## <a name="people-hub"></a>Personhub

Arbeiderhodet i **Personer**-huben (siden med **Personer-arbeidsområdet**) inneholder følgende informasjon:

- Navn på arbeider
- Personalnummer
- Stillingstittel
- Avdelinger
- Arbeidertype
- Juridisk enhet for ansettelse
- Arbeidserfaring
- Rapporterer til (leder)
- Stillingstype

Hodet inneholder også enkeltklikkhandlinger, for eksempel e-post, anrop eller meldinger. Hvis en bruker viser sin egen informasjon på siden med **Persone-arbeidsområdet**, inneholder delen med enkeltklikkhandlinger knappen **Rediger personopplysninger**. Brukeren kan velge denne knappen for å åpne siden **Personlige opplysninger** i **Ansattselvbetjening**.

## <a name="streamlined-worker-page"></a>Strømlinjeformet Arbeider-side

Arbeiderhodet på den strømlinjeformede **Arbeider**-siden inneholder følgende informasjon:

- Navn på arbeider
- Personalnummer
- Stillingstittel
- Avdelinger
- Arbeidertype
- Juridisk enhet for ansettelse

Dataene i hodet kan endres, avhengig av statusen til den ansatte. Hvis den ansatte for eksempel har sluttet i firmaet, inneholder hodekontrollen et **Sluttet**-merke, sluttdatoen for ansettelsen og årsaken til avslutningen.

Tabellen nedenfor viser dataene som vises i hodet for ulike ansattstatuser.

| Medarbeiderstatus | Data som vises | Notat |
|-----------------|--------------------|------|
| Venter | <ul><li>Navn</li><li>Personalnummer</li><li>Stillingstittel</li><li>Avdeling</li><li>Arbeidertype</li><li>Juridisk enhet</li><li>Uavsluttet-merke</li><li>Startdato</li><li>Rapporter til</li><li>Stillingstype</li></ul> | |
| Nyansettelse | <ul><li>Navn</li><li>Personalnummer</li><li>Stillingstittel</li><li>Avdeling</li><li>Arbeidertype</li><li>Juridisk enhet</li><li>Nyansettelse-merke</li><li>Arbeidserfaring</li><li>Rapporter til</li><li>Stillingstype</li></ul> | Som standard vises **Nyansettelse**-merket for ansatte som har blitt ansatt i løpet av de siste sju dagene. Hvis du vil endre denne innstillingen, går du til siden **Personalparametere** i kategorien **Generelt** i delen **Datointervall for nyansettelser** og angir en tidsramme. Hvis du for eksempel vil vise **Nyansettelse**-merket over ansatte som ble ansatt i løpet av de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**. |
| Aktiv ansatt | <ul><li>Navn</li><li>Personalnummer</li><li>Stillingstittel</li><li>Avdeling</li><li>Arbeidertype</li><li>Juridisk enhet</li><li>Startdato</li><li>Rapporter til</li><li>Stillingstype</li></ul> | |
| Avslutter | <ul><li>Navn</li><li>Personalnummer</li><li>Stillingstittel</li><li>Avdeling</li><li>Arbeidertype</li><li>Juridisk enhet</li><li>Avslutter-merke</li><li>Arbeidserfaring</li><li>Rapporter til</li><li>Stillingstype</li></ul> | Som standard vises **Avslutter**-merket for ansatte som kommer til å slutte i løpet av de neste sju dagene. Hvis du vil endre denne innstillingen, går du til siden **Personalparametere** i kategorien **Generelt** i delen **Datointervall for avsluttende arbeidere** og angir en tidsramme. Hvis du for eksempel vil vise **Avslutter**-merket over ansatte som skal slutte i løpet av de neste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**. |
| Avsluttet | <ul><li>Avsluttet-merke</li><li>Personalnummer</li><li>Sluttdato for ansettelse</li><li>Årsakskode</li></ul> | Som standard vises **Avsluttet**-merket for ansatte som har slutter i løpet av de siste sju dagene. Hvis du vil endre denne innstillingen, går du til siden **Personalparametere** i kategorien **Generelt** i delen **Datointervall for tidligere arbeidere** og angir en tidsramme. Hvis du for eksempel vil vise **Avsluttet**-merket over ansatte som har sluttet i løpet av de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**. |
