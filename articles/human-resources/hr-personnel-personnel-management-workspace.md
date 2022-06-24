---
title: Arbeidsområde for personaladministrasjon
description: Denne artikkelen beskriver de konseptuelle elementene i arbeidsområdet for personaladministrasjon.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fc424905bc9311662859b900636a68de2f7ee3cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888766"
---
# <a name="personnel-management-workspace"></a>Arbeidsområde for personaladministrasjon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeidsområdet **Personaladministrasjon** inneholder en omfattende mengde innhold. Det inneholder personalbevegelser, sporer ansattendringer, ledige stillinger, adresseendringer, utløpsposter og analyse og inneholder koblinger til bestemt informasjon. Denne artikkelen inneholder detaljert informasjon om hver del av arbeidsområdet.

## <a name="activity-tab"></a>Kategorien Aktivitet

Kategorien **Aktivitet** inneholder deler som grupperer arbeidere basert på stadiet deres i ansettelsesprosessen:

- **Kandidater som skal ansettes**
- **Starter snart**
- **Nyansettelser**
- **Avslutter**
- **Avsluttet**

Når en arbeider er i ett av disse stadiene, er bestemte handlinger tilgjengelige som en knapp på kortet, eller på menyen som vises når du velger (**...**) i øvre høyre hjørne. De følgende underdelene beskriver delene i kategorien **Aktivitet**, og viser hvilke handlinger som er tilgjengelige.

### <a name="candidates-to-hire"></a>Kandidater som skal ansettes

Delen **Kandidater som skal ansettes** i arbeidsområdet er fylt ut fra flere kilder:

- En OData-enhet (Open Data Protocol)
- LinkedIn-integrering
- Data som angis manuelt i produktet

Når kandidater vises i delen **Kandidater som skal ansettes**, kan du utføre følgende handlinger ved å velge ellipsen på kandidatkortet:

- **Forkast kandidat**
- **Ikke ansett**
- **Ansett**

> [!NOTE]
> Hvis kandidatlisten fylles ut fra Microsoft Dataverse, vises de samme kandidatene i alle juridiske enheter, fordi en juridisk enhet ikke er tilknyttet kandidaten.

### <a name="starting-soon"></a>Starter snart

Delen **Starter snart** viser arbeidere som har en startdato i fremtiden. Listen sorteres etter startdato. Startdatoen som er nærmest dagens dato, vises først.

Hvis lederen ikke vises på kortet, er det ikke tilordnet en stilling for arbeideren.

> [!NOTE] 
> Vi anbefaler at du tilordner en stilling til en arbeider før du bruker en sjekkliste. Enkelte ganger tilordnes de ansatte oppgaver som nyansattes overordnede. Hvis en stilling ikke er tilordnet en stilling, kan imidlertid ikke den nye ansattes overordnede bestemmes. I så fall blir de planlagte oppgavene som er beregnet på lederen, tilordnet kontrollistens eier i stedet.

Når arbeidere vises i **Starter snart**-delen, er følgende handlinger tilgjengelige for dem:

- Tilordne stilling
- Bekreft ansettelse
- Tilordne fast kompensasjon
- Tilordne variabel kompensasjon
- Vis i hierarki
- Bruk sjekkliste\*\*

\*\* Denne handlingen er standardhandlingen. Den vises som en knapp på kortet.

### <a name="recent-hires"></a>Nyansettelser

Delen **Nyansettelser** viser arbeidere som har en startdato i den nylige fortiden. Listen sorteres etter startdato. Startdatoen som er nærmest dagens dato, vises først.

Som standard viser listen arbeidere som ble ansatt de siste sju dagene. Hvis du vil endre denne innstillingen, angir du en tidsramme for **Nyansettelser** på fanen **Generelt** på siden **Parametere for Personal**. Dataene i delen **Nyansettelser** kan vises i et bestemt antall dager, måneder eller år. Hvis du for eksempel vil vise listen over arbeidere som ble ansatt i de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**.

> [!NOTE]
> Innstillingene på siden **Parametere for Personal** er firmaspesifikke. Derfor kan tidsrammen du viser nyansettelser for, variere fra firma til firma. I USMF-firmaet kan det for eksempel være at du vil vise alle nye ansettelser fra de siste sju dagene. Mens i USSI-firmaet kan det være at du vil vise alle nye ansettelser fra de siste 14 dagene. I dette tilfellet må du åpne siden **Parametere for Personal** i hvert firma, og angi parameterne etter behov.

Hvis lederen ikke vises på kortet, er det ikke tilordnet en stilling for arbeideren.

Når arbeidere vises i **Nyansettelser**-delen, er følgende handlinger tilgjengelige for dem:

- Tilordne stilling
- Bekreft ansettelse
- Fast kompensasjon
- Tilordne variabel kompensasjon
- Vis i hierarki
- Bruk sjekkliste\*\*

\*\* Denne handlingen er standardhandlingen. Den vises som en knapp på kortet.

### <a name="exiting"></a>Avslutter

Delen **Avslutning** viser arbeidere som har en avslutningsdato i fremtiden. Listen sorteres etter avslutningsdato. Avslutningsdatoen som er nærmest dagens dato, vises først. 

Som standard viser listen arbeidere som har en avslutningsdato de neste sju dagene. Hvis du vil endre denne innstillingen, angir du en tidsramme for **Nyansettelser** på fanen **Generelt** på siden **Vis avsluttende arbeidere**. Dataene i delen **Avslutning** kan vises i et bestemt antall dager, måneder eller år. Hvis du for eksempel vil vise listen over arbeidere som skal slutte i de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**.

Når arbeidere vises i **Avslutning**-delen, er følgende handlinger tilgjengelige for dem:

- Bruk sjekkliste\*\*
- Bekreft ansettelse
- Vis i hierarki

\*\* Denne handlingen er standardhandlingen. Den vises som en knapp på kortet.

### <a name="exited"></a>Avsluttet

Delen **Avsluttet** viser arbeidere som har en avslutningsdato i den nylige fortiden. Listen sorteres etter avslutningsdato. Avslutningsdatoen som er nærmest dagens dato, vises først.

Som standard viser listen arbeidere som har en avslutningsdato de siste sju dagene. Hvis du vil endre denne innstillingen, angir du en tidsramme for **Nyansettelser** på fanen **Generelt** på siden **Vis arbeidere som har sluttet**. Dataene i delen **Avsluttet** kan vises i et bestemt antall dager, måneder eller år. Hvis du for eksempel vil vise listen over arbeidere som har sluttet i de siste 14 dagene, setter du **Periode**-feltet til **14** og **Enhet**-feltet til **Dager**.

Når arbeiderne vises i **Avsluttet**-delen, er følgende handlinger tilgjengelige for dem:

- Bruk sjekkliste\*\*
- Bekreft ansettelse
- Vis i hierarki

\*\* Denne handlingen er standardhandlingen. Den vises som en knapp på kortet.

## <a name="employee-changes-tab"></a>Fanen Ansattendringer

Kategorien **Ansattendringer** viser en liste over alle ansattes handlinger. Denne listen er ikke tilgjengelig som standard. Hvis du vil aktivere funksjonaliteten, setter du alternativet **Aktiver ansatthandlinger** på siden **Delte parametere for personaladministrasjon** på fanen **personalhandlinger** til **Ja**.

## <a name="position-changes-tab"></a>Kategorien Stillingsendringer

Kategorien **Stillingsendringer** viser en liste over alle stillingspersonalhandlinger. Denne listen er ikke tilgjengelig som standard. Hvis du vil aktivere funksjonaliteten, setter du alternativet **Aktiver stillingshandlinger** på siden **Delte parametere for personaladministrasjon** på fanen **personalhandlinger** til **Ja**.

## <a name="open-positions-tab"></a>Fanen Åpne stillinger

Fanen **Åpne stillinger** viser alle åpne stillinger. Stillinger må ha en aktiveringsdato på nåværende eller tidligere tidspunkt for at de skal vises i listen, og de må ikke ha en gjeldende arbeidertilordning.

> [!NOTE]
> Listen vurderer arbeidertilordningen per i dag. Enhver stilling som har en fremtidig datert arbeidertilordning, vil fortsatt vises i listen. Etter at gyldighetsdatoen for arbeidertilordningen er nådd, fjernes imidlertid stillingen fra listen.

## <a name="expiring-records-tab"></a>Kategorien Utløpende poster

Kategorien **Utløpende poster** viser alle elementer som er utløpt eller vil utløpe for arbeiderne i firmaet som brukeren er logget på. Følgende elementer vises i listen:

- **Attester**
- **Identifikasjon**
- **Prøveperioder**
- **Screeninger**
- **Tester**

Hvis du vil angi om listen viser utløpte poster eller utløpende poster, definererer du en tidsramme på siden **Parametere for Personal** på **Generelt**-fanen for enten **Utløpende poster** eller **Utløpte poster**. Dataene i kategorien **Utløpende poster** kan vises i et bestemt antall dager. Hvis du for eksempel vil vise listen over poster som vil utløpe i de neste 14 dagene, setter du **Antall dager**-feltet til **14**.

> [!NOTE] 
> Hvis du angir tidsrammen for **Utløpte poster** eller **Utløpende poster** til **0** på siden **Parametere for Personal**, vil ikke listen vise noen av disse postene.

## <a name="employees-tile"></a>Ansatte-flis

**Ansatte**-flisen gir en telling av alle ansatte som er ansatt i firmaet som brukeren for øyeblikket er logget på. Når du velger **Ansatt**-flisen, viser en ny side detaljene til de ansatte.

## <a name="contractors-tile"></a>Oppdragstakere-flisen

**Oppdragstakere**-flisen gir en telling av alle oppdragstakere som er ansatt i firmaet som brukeren for øyeblikket er logget på. Når du velger **Oppdragstakere**-flisen, viser en ny side detaljene til oppdragstakerne.

## <a name="open-positions-tile"></a>Åpne stillinger-flisen

**Åpne stillinger**-flisen gir en telling av alle åpne stillinger. Når du velger **Åpne stillinger**-flisen, viser en ny side detaljene til de åpne stillingene. Stillinger må ha en aktiveringsdato på nåværende eller tidligere tidspunkt for at de skal inkluderes i tellingen, og de må ikke ha en gjeldende arbeidertilordning.

> [!NOTE]
> Flisen vurderer arbeidertilordningen per i dag. Enhver stilling som har en fremtidig datert arbeidertilordning, vil fortsatt skal inkluderes i tellingen. Etter at gyldighetsdatoen for arbeidertilordningen er nådd, utelates imidlertid stillingen fra tellingen.

## <a name="approvals-tile"></a>Godkjenninger-flisen

**Godkjenninger**-flisen inneholder en telling av alle arbeidsflytelementer som venter på gjeldende brukers godkjenning. Når du velger **Godkjenninger**-flisen, viser en ny side detaljene for arbeidsflytelementene som krever din godkjenning.

## <a name="address-changes-tile"></a>Adresseendringer-flisen

**Adresseendringer**-flisen gir en telling av alle adresseendringene som skjedde i løpet av antall dager som er angitt på siden **Parametere for Personal**. Når du velger **Adresseendringer**-flisen, viser en ny side detaljene for alle adresseendringer. Oppe til høyre på siden kan du velge **Inkluder fremtidige adresseendringer** for å vise adresseendringer med en fremtidig dato.

Hvis du vil ha mer informasjon om hvordan du viser og administrerer adresseendringer, kan du se [Vise og behandle adresseendringer](hr-personnel-view-address-changes.md).
