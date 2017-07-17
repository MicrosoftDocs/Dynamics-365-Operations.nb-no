---
title: Gantt-diagram til finplanlegging
description: "Gantt-diagrammet er utformet for å gi produksjonsplanleggere muligheten til å kontrollere og optimalisere produksjonsplanen. Gantt-diagrammet gjør flyten av operasjoner gjennomsiktig og gjør det enkelt å justere produksjonsplanen mens det tas hensyn til material- eller ressursmangler. På denne måten kan planleggere gjøre best bruk av ressurser, minimere varer i arbeid og optimalisere produksjonstider for produksjonsordrer."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 55631c4d588c699b9e47f73190d5b01d6da3b9ec
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017

---

# Gantt-diagram til finplanlegging
<a id="gantt-chart-for-job-scheduling" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Gantt-diagrammet er utformet for å gi produksjonsplanleggere muligheten til å kontrollere og optimalisere produksjonsplanen. Gantt-diagrammet gjør flyten av operasjoner gjennomsiktig og gjør det enkelt å justere produksjonsplanen mens det tas hensyn til material- eller ressursmangler. På denne måten kan planleggere gjøre best bruk av ressurser, minimere varer i arbeid og optimalisere produksjonstider for produksjonsordrer.

Gantt-diagrammet er utformet for å gi produksjonsplanleggere muligheten til å kontrollere og optimalisere produksjonsplanen. Gantt-diagrammet gjør flyten av operasjoner gjennomsiktig og gjør det enkelt å justere produksjonsplanen mens det tas hensyn til material- eller ressursmangler. På denne måten kan planleggere gjøre best bruk av ressurser, minimere varer i arbeid og optimalisere produksjonstider for produksjonsordrer.

Et Gantt-diagram er en visuell fremstilling av planlagte aktiviteter innenfor et definert tidsintervall. Aktivitetene planlegges med ressurser som har kapasitet definert av en kapasitetskalender. Følgende typer aktiviteter kan vises i Gantt-diagrammet.

-   Jobber fra produksjonsordrer som er finplanlagt.
-   Jobber fra planlagte produksjonsordrer.
-   Finplanlagte prosjektaktiviteter av typen Timeprognoser.

Gantt-diagrammet kan åpnes på to ulike måter, **Ordrevisning** og **Ressursvisning**[.](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true)I **Ordrevisning** grupperes aktiviteter under produksjonsordrer. Dette kan for eksempel være nyttig hvis du vil holde oversikt over alle jobbene som er knyttet til de samme bestillingene. I **Ressursvisning** grupperes alle jobber under enkeltressurser. Denne visningen kan være nyttig når du optimaliserer planen på et ressursnivå, for eksempel en maskin eller en gruppe maskiner. Gantt-diagrammene som er vist i illustrasjonene nedenfor, viser **Ordrevisning** og **Ressursvisning** med disse viktige elementer:

1.  Aktivitet i Gantt-diagram
2.  Materialmangel ikonet
3.  Materialtilgjengelighetsikon
4.  Ikon for dato for levering av bestillingen
5.  Kapasitetslinje

## Ordrevisning
<a id="order-view" class="xliff"></a>

[![ordrevisning](./media/orderview.png)](./media/orderview.png)

## Ressursvisning
<a id="resource-view" class="xliff"></a>
[![ressursvisning](./media/resview.png)](./media/resview.png)

## Aktiviteter
<a id="activities" class="xliff"></a>
Aktivitetene vises som stolper og er organisert i et tidsskalarutenett med et planlagt start- og sluttidspunkt, slik at lengden på stolpene blir proporsjonal med tiden som er nødvendig for å fullføre aktiviteten. Aktivitetene vises i henhold til en tidsskala. Du kan justere tidsskalaen på menyen der du velger en startdato og sluttdato og en tidsenhet, for eksempel timer eller dager. Du kan sette fokus på et tidsintervall der du vil behandle aktiviteter ved å justere tidsskalaen. 

Hvis du vil ha en bedre oversikt, finner du ulike alternativer for å kontrollere fargen på aktivitetene. Du kan konfigurere en enkelt farge for aktiviteter, bruke temafargen som er det generelle fargetemaet som brukes for programmet, eller angi fargen som skal kontrolleres av fargekoden for produksjonsordrer. 

Tidsintervallet for aktiviteter har en sjattering i bakgrunnen. Perioder med en hvit sjattering angir et tidsintervall med definert kapasitet på ressursen for aktiviteten, mens perioder med en grå sjattering angir tidsintervaller med ingen kapasitet definert. 

På venstre side av diagrammet finner du mer informasjon om aktiviteten, for eksempel ressursen som aktiviteten er planlagt på, og produksjonsordrenummeret. Forbindelsen mellom jobber som tilhører den samme ordren, vises med en pil. 

Du kan få mer informasjon om en aktivitet i dialogboksen for aktiviteten. Dobbeltklikk aktiviteten for å åpne dialogboksen, eller velg menyen **Informasjon**. I dialogboksen for aktiviteten kan du se den planlagte start- og sluttdatooen og tidsinformasjon om hvilke materialer det er planlagt å bruke for aktiviteten. 

Aktivitetene kan grupperes i grupperingsnivåer. Grupperingsnivåene er hierarkiske og kan brukes til å lage en logisk gruppering av aktiviteter. Hvis du for eksempel har et oppsett der produksjonsaktiviteter grupperes etter område, produksjonsenheter, ressursgrupper og ressurser, kan du bruke grupperingsnivåene til å gruppere aktivitetene i henhold til dette oppsettet. Grupperingsnivåene kan vises og skjules på de individuelle grupperingsnivåene eller for alle nivåer i diagrammet ved hjelp av knappene **Vis alle** og **Skjul alle** på menyen. Du kan også konfigurere grupperingsnivåer for å vises eller skjules når diagrammet åpnes.

### Materialtilgjengelighet
<a id="material-availability" class="xliff"></a>

Gantt-diagrammet kan defineres for å gi planleggeren detaljert informasjon om materialstatusen for de individuelle aktivitetene. Dette kan for eksempel være nyttig hvis material er forsinket og påvirker produksjonsplanen. I så fall blir materialavgangene merket i Gantt-diagrammet for å hjelpe planleggeren med å forstå konsekvenser og foreta justeringer. 

En jobb vises med et ikon for materialmangel hvis startdatoen for planen for jobben er senere enn datoen for materialtilgjengelighet for materialene som forbrukes av jobben. Materialtilgjengelighetsdatoen beregnes basert på utligningsinformasjonen i den dynamiske hovedplanen. Ikonet for materialmangel vises for eksempel på en jobb som bruker et materiale som er utlignet mot en bestilling som har et mottak som er senere enn planlagt startdato for jobben.

### Indikator for dato for materialtilgjengelighet
<a id="indicator-of-material-availability-date" class="xliff"></a>

Når du definerer diagrammet for å vise jobber med materialmangler, kan det også vises et ikon for å vise datoen for materialtilgjengelighet for jobben. Ikonet vises kun hvis datoen for materialtilgjengelighet er innenfor det definerte tidsintervallet i diagrammet. Hvis materialtilgjengelighetsdatoen ligger utenfor det definerte tidsintervallet, kan mer detaljert informasjon for materialtilgjengelighet hentes fra materiallisten i dialogboksen for jobben. I listen er det også et ikon som viser sene materialer for jobben. Du kan planlegge en jobb med materialtilgjengelighetsdatoen som startdato.

### Indikator for dato for levering av ordren
<a id="indicator-of-order-delivery-date" class="xliff"></a>

Dette ikonet angir leveringsdatoen for en produksjonsordre. Ikonet vises bare i ordrevisning.

### Kapasitetslinje
<a id="capacity-bar" class="xliff"></a>

Du kan konfigurere diagrammet for å vise en ressurskapasitetslinje. Denne linjen inneholder en oversikt over ressurskapasiteten for en aktivitet i det definerte tidsintervallet i diagrammet. Kapasitetslinjen vises ikke for perioder der ressursen ikke er reservert. I perioder der ressursen er reservert til full kapasitet, vises kapasitetslinjen som en heltrukket linje. I perioder der ressursen er overbestilt, vises linjen tykkere og i rødt. Hvis for eksempel to jobber overlapper, angir kapasitetslinjen en overbooking i tidsintervallet der det er en overlapping. Kapasitetslinjen oppdateres dynamisk når du planlegger en jobb. Du aktiverer kapasitetslinjen på menyen **Vis kapasitetslinje**. Den kan bare vises i **ressursvisning**. Hvis du vil ha en mer detaljert visning av kapasitetsbelastningen for en ressurs, kan du bruke **Kapasitetsbelastning**-diagrammet, som kan åpnes fra menyen eller hurtigmenyen for en valgt aktivitet.

## Finplanlegging i Gantt-diagrammet
<a id="job-scheduling-in-the-gantt-chart" class="xliff"></a>
Gantt-diagrammet inneholder ulike alternativer for å foreta justeringer i produksjonsplanen. I Gantt-diagrammet, kan du planlegge aktiviteter på nytt som en samhandling med dra og slipp eller fra en tidsplanmeny. I planleggingsprosessen kan du ta ressurskapasitet, ressursfunksjoner og materialbegrensninger i betraktning.

### Planlegge en jobb som en samhandling med dra og slipp
<a id="schedule-a-job-as-a-drag-and-drop-interaction" class="xliff"></a>

Du kan planlegge jobben på nytt i det definerte tidsintervallet som en samhandling med dra og slipp. Du kan bare planlegge jobben på nytt på den samme ressursen, og du kan bare planlegge én jobb om gangen.

### Planlegge en jobb fra menyen
<a id="schedule-a-job-from-the-menu" class="xliff"></a>

På **Planlegg jobber**-menyen kan du planlegge én eller flere valgte jobber i diagrammet basert på en planleggingsretning og en dato og et klokkeslett for planlegging. Det finnes tre tilgjengelige planleggingsretninger.

-   Fremover fra planleggingsdato
-   Bakover fra planleggingsdato
-   Fremover fra dato for materialtilgjengelighet

Det er ikke mulig å planlegge en jobb utenfor det definerte tidsintervallet i Gantt-diagrammet. Hvis du gjør dette, blir jobben værende uplanlagt, og du får feilmeldingen "Kan ikke planlegge jobb i den innlastede tidsperioden."

### Planlegg forrige jobber
<a id="schedule-previous-jobs" class="xliff"></a>

I et nettverk av aktiviteter, for eksempel jobber som tilhører samme produksjonsordre, kan du bruke funksjonen **Planlegg forrige jobber** -til å planlegge de forrige jobbene i forhold til en valgt jobb i nettverket. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben.

<table>
<tr>
<td>
Før
</td>
<td rowspan=2>
<img src='./media/schprevjob3.png'/>
</td>
</tr>
<tr>
<td>
Etter
</td>
</tr>
</table>

### Planlegg neste jobber
<a id="schedule-next-jobs" class="xliff"></a>

Du kan bruke funksjonen **Planlegg neste jobber** til å planlegge de neste jobbene i forhold til en valgt jobb i et nettverk av aktiviteter. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben.

<table>
<tr>
<td>
Før
</td>
<td rowspan=2>
<img src='./media/schnxtjob.png'/>
</td>
</tr>
<tr>
<td>
Etter
</td>
</tr>
</table>

### Planlegg rundt jobb
<a id="schedule-around-job" class="xliff"></a>

Du kan bruke funksjonen **Planlegg rundt jobb** til å planlegge den neste jobben og den forrige jobben i forhold til en valgt jobb i et nettverk av aktiviteter. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben.

<table>
<tr>
<td>
Før
</td>
<td rowspan=2>
<img src='./media/scharoundjob1.png'/>
</td>
</tr>
<tr>
<td>
Etter
</td>
</tr>
</table>

### Ordne jobber
<a id="arrange-jobs" class="xliff"></a>

Du kan bruke den **Ordne**-funksjonen til å ordne merkede aktiviteter på den samme ressursen. Disse aktivitetene kan være i samme nettverk av aktiviteter, men kan også tilhøre forskjellige nettverk. Når du bruker funksjonen Ordne, elimineres tidsmellomrommene mellom de valgte aktivitetene. Du kan bruke denne funksjonen til å optimere kapasitetsutnyttelsen for ressursene.

<table>
<tr>
<td>
Før
</td>
<td rowspan=2>
<img src='./media/arrangejobs1.png'/>
</td>
</tr>
<tr>
<td>
Etter
</td>
</tr>
</table>

### Tilordne aktiviteter på nytt fra en ressurs til en annen
<a id="reassign-activities-from-one-resource-to-another" class="xliff"></a>

Du kan tilordne en jobb på nytt fra en ressurs til en annen. Dette kan være nyttig i situasjoner der en maskin er i ustand eller overbestilt, og du vil finne en annen tilgjengelig ressurs som kan gjøre jobben.

### Tilordne en aktivitet på nytt som en samhandling med dra og slipp
<a id="reassigning-an-activity-as-a-drag-and-drop-interaction" class="xliff"></a>

I **Ressurs**-visningen kan du tilordne en aktivitet på nytt til en annen ressurs i Gantt-diagrammet som en samhandling med dra og slipp. Du kan gjøre dette ved å merke raden som aktiviteten er planlagt i. Når raden er valgt, kan du dra raden til ressursen i diagrammet gruppert under et annet ressursgrupperingsnivå.

### Tilordne en aktivitet på nytt fra menyen Planlegg jobber
<a id="reassigning-an-activity-from-the-schedule-jobs-menu" class="xliff"></a>

Du kan tilordne en jobb på nytt fra dialogboksen **Planlegg jobb** som åpnes fra menyen **Planlegg jobb**. På denne menyen kan du bare tilordne en jobb på nytt til en ressurs som allerede er lastet inn i Gantt-diagrammet. Hvis du bare velger én jobb, sorteres rullegardinlisten for ressursen etter gjeldende ressurser. Hvis du velger flere jobber, vil det ikke være noen informasjon om gjeldende ressurser fra ressurslisten.

## Laste inn flere ressurser i Gantt-diagrammet
<a id="load-additional-resources-to-the-gantt-chart" class="xliff"></a>
I **Ressursvisning** har du muligheten til å laste inn flere ressurser i Gantt-diagrammet. Dette kan være nyttig hvis du vil finne en alternativ ressurs for en jobb som er planlagt på en maskin som er overbestilt eller i ustand. På siden **Last inn tilleggsressurser** får du en liste over ressurser som er datogyldige per datoen som listen åpnes på. Gjeldende ressurser, i forhold til en valgt jobb i Gantt-diagrammet, vises først. Hvis du har flere jobber som er valgt, før du åpnet listen, vises ikke informasjon om gjeldende ressurser. På siden **Last inn tilleggsressurser** kan du velge én eller flere ressurser, som vil bli lastet inn i Gantt-diagrammet når du bekrefter valget. Hvis det ikke finnes noen jobber planlagt på den merkede ressursen i tidsintervallet i Gantt-diagrammet, plasseres ressursen under et ressursgrupperingsnivå nederst i listen over aktiviteter i Gantt-diagrammet.

### Få tilgang til Gantt-diagrammet
<a id="access-the-gantt-chart" class="xliff"></a>

Gantt-diagrammet kan åpnes fra følgende sider.

| **Side**                                                                                     | **Beskrivelse**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Produksjonsordreoversikt og -detaljer**                                                         | På siden **Produksjonsordreoversikt og -detaljer** kan du åpne Gantt-diagrammet fra én eller flere av de valgte ordrene. Når du åpner diagrammet fra menyelementet **Gantt-diagram**, lastes alle jobber som er knyttet til de valgte produksjonsordrene, men også jobber fra andre produksjonsordrer som er planlagt på de samme ressursene. Når du åpner diagrammet fra menyelementet **Gantt-diagram – hurtigvisning**, lastes bare jobber som er knyttet til de valgte produksjonsordrene. I denne visningen er det ikke mulig å planlegge jobber. |
| **Ressurs**                                                                                 | På **Ressurs**-siden du kan åpne Gantt-diagrammet fra menyelementet **Gantt-diagram**. Når valgt, lastes alle jobbene som er planlagt på ressursen i en valgt tidsintervall, i diagrammet.                                                                                                                                                                                                                                                                                                   |
| **Ressursgruppe**                                                                           | På **Ressursgruppe**-siden du kan åpne Gantt-diagrammet fra menyelementet **Gantt-diagram**. Når valgt, vises alle jobbene som er planlagt på ressursene i ressursgruppen, i det valgte tidsintervallet.                                                                                                                                                                                                                                                                                    |
| **Gantt-diagrammer**                                                                             | På **Gantt-diagrammer**-siden kan du konfigurere Gantt-diagrammer etter ressurser og ressursgrupper. Hvis du for eksempel vil kontrollere produksjonsaktiviteter for bestemte sett med ressurser eller ressursgrupper, kan du deretter gjøre enkeltkonfigurasjoner av disse på **Gantt-diagrammer**-siden. Du kan deretter åpne Gantt-diagrammet fra hver konfigurasjon.                                                                                                                                                    |
| **Timeprognoser** (prosjekt)                                                                 | Prosjektaktiviteter av typen **Timeprognoser** kan finplanlegges på ressurser. På **Timeprognose**-siden på menyen **Planlegging** kan du åpne Gantt-diagrammet i en bestilling for å se finplanlagte prosjektaktiviteter av typen Timeprognose.                                                                                                                                                                                                                                                             |
| **Jobber som skal fullføres** (liste i **Produksjonsstyring**-arbeidsområdet)                      | Listen **Jobber som skal fullføres i arbeidsområdet Produksjonsstyring** viser jobber fra produksjons- og partiordrer som pågår på de merkede ressursene for arbeidsområdet. På menyelementet **Gantt-diagram** kan du åpne Gantt-diagrammet, der alle jobber som er valgt i listen vil bli lastet inn i diagrammet.                                                                                                                                                                                |
| **Produksjonsordrer som skal frigis** (åpnes fra **Produksjonsstyring**-arbeidsområdet) | Siden Produksjonsordrer som skal frigis åpnes fra **Produksjonsstyring**-arbeidsområdet. Denne siden viser planlagte produksjons- og partiordrer som venter på frigivelse. Du kan åpne Gantt-diagrammet for valgte produksjonsordrer på denne siden.                                                                                                                                                                                                                                                        |




