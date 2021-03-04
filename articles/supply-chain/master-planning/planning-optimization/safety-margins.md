---
title: Sikkerhetsmarginer
description: Dette emnet beskriver hvordan sikkerhetsmarginer kan brukes med tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8ab5f1c3cdfa990a73951ddc5a7469644954d5c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434281"
---
# <a name="safety-margins"></a>Sikkerhetsmarginer

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver hvordan sikkerhetsmarginer kan brukes med tillegget for planleggingsoptimalisering for Microsoft Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Oversikt over sikkerhetsmarginer

Formålet med sikkerhetsmarginer er å aktivere et oppsett som gir litt ekstra tid i tillegg til den normale leveringstiden. Når materialer for eksempel må pakkes ut eller kontrolleres etter at de kommer fra leverandøren, kan du ikke legge til den ekstra tiden i leveringstiden, fordi denne fremgangsmåten vil gi leverandøren en ekstra buffertid. I dette eksemplet kan mottaksmarginen brukes til å sikre at leverandøren leverer tidligere. Denne fremgangsmåten gir buffertid slik at varene kan håndteres internt.

Det finnes tre typer sikkerhetsmarginer:

- **Gjenbestillingsmargin** – buffertiden for å plassere forsyningsordren
- **Mottaksmargin** – buffertiden for håndtering av innkommende forsyninger
- **Avgangsmargin** – buffertiden for håndtering av forsendelser

Illustrasjonen nedenfor viser hvordan disse sikkerhetsmarginene gjelder over tid.

![Sikkerhetsmarginer](media/safety-margins-1.png)

Alle marginer er definert i dager. Standardverdien, *0* (null), angir at ingen margin er i bruk. Hvis du definerer flere marginer, legger de alle til den totale tiden fra forsyningens *ordredato* til etterspørselens *behovsdato*. Et oppsett har for eksempel ingen leveringstid, og alle tre margintypene er satt til én dag. I dette tilfellet vil det være tre dager mellom forsyningsordredatoen og etterspørselsbehovsdatoen, så hvis ordredatoen er 1. juli, vil behovsdatoen være 4. juli.

### <a name="receipt-margin"></a>Mottaksmargin

Mottaksmarginen er sannsynligvis den mest brukte av de tre sikkerhetsmarginene. Den brukes på *leveringsdatoen* og bakover fra *behovsdatoen*. Med andre ord bør produktene motta det angitte antallet mottaksmargindager før de er påkrevd.

Illustrasjonen nedenfor uthever mottaksmargin.

![Mottaksmargin](media/safety-margins-2.png)

Mottaksmarginen brukes vanligvis som en buffer for å sikre tiden for lagerregistrering eller andre tidkrevende prosesser som ikke blir registrert som en del av den generelle leveringstiden i systemet. For innkjøp er én fordel at *leveringsdatoen* for bestillingen flyttes videre fremover i henhold til dette. Hvis du øker leveringstiden i stedet for å bruke en sikkerhetsmargin, vil leverandøren likevel bli bedt om å levere i siste liten.

Legg merke til at mottaksmarginen ikke endrer *behovsdatoen* til forsyningen. Derfor vil ikke mottaksmarginen være direkte synlig når behovsdatoer for etterspørsel og forsyning sammenlignes (for eksempel på siden **Nettobehov**). Hvis mottaksmarginen for eksempel er satt til fire dager, og en bestillingslinje er planlagt for mottak den 15. i måneden, beregner hovedplanleggingen den justerte mottaksdatoen som den 19. i måneden.

Legg merke til at en mottaksmargin ikke brukes når lagerbeholdningen brukes som forsyningen. Alle lagerbeholdninger antas å være tilgjengelige umiddelbart, uansett når de faktisk er mottatt.

### <a name="reorder-margin"></a>Gjenbestillingsmargin

> [!NOTE]
> **Kommer snart:** Denne funksjonen støttes ennå ikke for planleggingsoptimalisering. Før den støttes, vil alle verdier som angis for **Gjenbestillingsmargin lagt til vareleveringstiden**, behandles som *0* (null).

Illustrasjonen nedenfor uthever gjenbestillingsmarginen.

![Gjenbestillingsmargin](media/safety-margins-3.png)

Gjenbestillingsmarginen legges til før varens leveringstid for alle planlagte ordrer under hovedplanlegging. Derfor sikres tilleggstiden for en forsyningsordre. Denne marginen brukes vanligvis som en buffer for å sikre tiden for godkjenningsprosesser eller andre interne prosesser som kreves ved opprettingen av forsyningsordrer. Gjenbestillingsmarginen plasseres mellom forsyningens *ordredato* og *startdato*.

### <a name="issue-margin"></a>Avgangsmargin

> [!NOTE]
> **Kommer snart:** Denne funksjonen støttes ennå ikke for planleggingsoptimalisering. Før den støttes, vil alle verdier som angis for **Avgangsmargin trukket fra behovsdato**, behandles som *0* (null).

Illustrasjonen nedenfor uthever avgangsmarginen.

![Avgangsmargin](media/safety-margins-4.png)

Avgangsmarginen trekkes fra etterspørselens behovsdato under hovedplanleggingen. Den bildrar til å sikre at du har tid til å respondere på og sende innkommende ordrer. Denne marginen brukes vanligvis som en buffer for å sikre tid for forsendelse og tilknyttede utgående lagerprosesser.

Legg merke til at når det gjelder en avgangsmargin, samsvarer ikke relaterte forsyninger og etterspørselens behovsdatoer. De avviker i stedet etter avgangsmarginen, fordi avgangsmarginen legges til mellom forsyningens *behovsdato* og etterspørselens *behovsdato*.

## <a name="set-up-safety-margins"></a>Definere sikkerhetsmarginer

### <a name="turn-on-safety-margins-in-feature-management"></a>Aktiver sikkerhetsmarginer i Funksjonsbehandling

Før du kan bruke denne funksjonen med planleggingsoptimalisering, må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** _Hovedplanlegging_
- **Funksjonsnavn:** _Marginer for planleggingsoptimalisering_

### <a name="define-safety-margins"></a>Definere sikkerhetsmarginer

Sikkerhetsmarginer har et fleksibelt oppsett. De kan angis både for *dekningsgruppen* og *hovedplanen*. Det er viktig at du forstår at marginene legges oppå hverandre. En mottaksmargin på to dager i dekningsgruppen og tre dager i hovedplanen vil for eksempel produsere en effektiv mottaksmargin på fem dager.

Muligheten til å angi marginen på hovedplanen kan være nyttig når du vil simulere lengre leveringstider eller -opplegg for en bestemt plan, men uten å påvirke den daglige planleggingen.

#### <a name="coverage-group-safety-margins"></a>Sikkerhetsmarginer for dekningsgruppe

Hvis du vil bruke en sikkerhetsmargin for en dekningsgruppe, følger du disse trinnene.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekningsgrupper**.
1. I listeruten velger du ønsket dekningsgruppe.
1. I delen **Sikkerhetsmarginer i dager** i hurtigkategorien **Annet** bruker du følgende felt til å angi påkrevde sikkerhetsmarginer (i dager):

    - Påslag dager lagt til i behovsdato
    - Sikkerhetsdager trukket fra behovsdato
    - Respittid, gjenbestilling lagt til vareleveringstiden

#### <a name="master-plan-safety-margins"></a>Sikkerhetsmarginer for hovedplan

Hvis du vil bruke en sikkerhetsmargin for en hovedplan, følger du disse trinnene.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. I listeruten velger du den ønskede hovedplanen.
1. I hurtigkategorien **Sikkerhetsmarginer i dager** bruker du følgende felt til å angi påkrevde sikkerhetsmarginer (i dager):

    - Påslag dager lagt til i behovsdato
    - Sikkerhetsdager trukket fra behovsdato
    - Respittid, gjenbestilling lagt til vareleveringstiden

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Definere om beregninger skal baseres på kalenderdager eller virkedager

Du kan angi alle sikkerhetsmarginer slik at de beregnes på grunnlag av enten kalenderdager eller virkedager.

1. Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**.
1. I kategorien **Generelt** i delen **Sikkerhetsmarginer i dager** setter du alternativet **virkedager** til *Ja* for å beregne marginer basert på virkedager. Sett alternativet til *Nei* for å beregne marginer basert på kalenderdager.

En kalender kan for eksempel være åpen fra mandag til fredag og avsluttes fra lørdag til og med søndag. Hvis det er en mottaksmargin på én dag, vil en behovsdato på en mandag generere en leveringsdato på forrige fredag, ettersom lørdag og søndag ikke er virkedager.

Kalenderen som brukes til å fastslå virkedagene, avhenger av oppsettet og forsyningstypen. Den kan styres av kalenderne til dekningsgruppen, lageret og leverandøren.

> [!NOTE]
> Hvis *lageret* ikke er en del av dekningsdimensjonen (med andre ord er planlegging bare basert på *område*), brukes ikke lagerkalenderen.

Systemet kan håndtere et oppsett der én eller flere kalendere er definert. Underdelene nedenfor beskriver de mulige kombinasjonene som kan brukes til å kontrollere resultatet.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalender som brukes for varigheten

De definerte kalenderne styrer den faktiske totale leveringstiden i kalenderdager, fra forsyningens ordredato til etterspørselens behovsdato. Følgende kalenderprioritering brukes:

- **Leveringstid for innkjøp** – bare dekningsgruppekalenderen vurderes.
- **Mottaksmargin** – dekningsgruppekalenderen brukes hvis den er definert. Ellers brukes lagerkalenderen.
- **Avgangsmargin** – dekningsgruppekalenderen brukes hvis den er definert. Ellers brukes lagerkalenderen.
- **Ordremargin** – bare dekningsgruppekalenderen vurderes.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalender som brukes for sluttdatoen

Følgende regler brukes for å fastslå om planleggingsmotoren kan bruke en angitt dato for en bestemt datotype:

- **Mottaksdato for innkjøp** – leverandørkalenderen brukes hvis den er definert. Ellers brukes dekningsgruppekalenderen hvis den er definert. Hvis ingen av disse kalenderne er definert, brukes lagerkalenderen.
- **Mottaksdato for overføring** – dekningsgruppekalenderen brukes hvis den er definert. Ellers brukes lagerkalenderen.
- **Mottaksdato for produksjon** – dekningsgruppekalenderen brukes hvis den er definert. Ellers brukes lagerkalenderen.
- **Åpen dag for etterspørselsbehov** – lagerkalenderen brukes hvis den er definert. Ellers brukes dekningsgruppekalenderen.
- **Åpen dag for ordre** – en kombinasjon (skjæringspunkt) av dekningsgruppekalenderen og leverandørkalenderen brukes. Begge kalenderne må være åpne for å bruke datoen. Hvis bare én av kalendrne er definert, brukes kun den kalenderen.

#### <a name="calendar-setup-overview-matrix"></a>Matrise for oversikt over kalenderoppsett

Illustrasjonen nedenfor viser en matrise som oppsummerer hvilke kalendere som gjelder når det beregnes sikkerhetsmarginer. (Velg bildet for å åpne en høyoppløsningsversjon av det.) Følgende forkortelser og farger brukes til å angi hvor hver type kalender er angitt:

- **Dekningsgruppe (CG):** Grønn
- **Lager (WH):** Gul
- **Leverandør (V):** Blå

[![Matrise for oversikt over kalenderoppsett](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Beregne forsinkelser

Alle tre typer sikkerhetsmarginer tas med når systemet fastslår om en ordre er forsinket.

En vare har for eksempel innledende tid på én dag og en mottaksmargin på tre dager. En salgsordre for denne varen er angitt som nødvendig i dag. I dette tilfellet blir forsinkelsen beregnet som *leveringstid* + *mottaksmargin* = fire dager. Hvis i dag er 14. august, fører de fire dagene med forsinkelse til at leveringen blir 18. august. Illustrasjonen nedenfor viser dette eksemplet.

![Eksempel på forsinkelsesberegning](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Komme i gang med planleggingsoptimalisering](get-started.md)

[Analyse for tilpassing av planleggingsoptimalisering](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]