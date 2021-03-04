---
title: Gantt-diagram til finplanlegging
description: Produksjonsplanleggere kan kontrollere og optimalisere produksjonsplaner ved å bruke Gantt-diagrammer.
author: johanhoffmann
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e194f379d118ee174095229d38ba5b0a679f49ac
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434508"
---
# <a name="gantt-chart-for-job-scheduling"></a>Gantt-diagram til finplanlegging

[!include [banner](../includes/banner.md)]

Gantt-diagrammet er utformet for å gi produksjonsplanleggere muligheten til å kontrollere og optimalisere produksjonsplanen. Gantt-diagrammet gjør flyten av operasjoner gjennomsiktig og gjør det enkelt å justere produksjonsplanen mens det tas hensyn til material- eller ressursmangler. På denne måten kan planleggere gjøre best bruk av ressurser, minimere varer i arbeid og optimalisere produksjonstider for produksjonsordrer.

Et Gantt-diagram er en visuell fremstilling av planlagte aktiviteter innenfor et definert tidsintervall. Aktivitetene planlegges med ressurser som har kapasitet definert av en kapasitetskalender. Følgende typer aktiviteter kan vises i Gantt-diagrammet.

-   Jobber fra produksjonsordrer som er finplanlagt.
-   Jobber fra planlagte produksjonsordrer.
-   Finplanlagte prosjektaktiviteter av typen Timeprognoser.

Gantt-diagrammet kan åpnes i to forskjellige visninger, **Ordrevisning** og **Ressursvisning**. I **Vis** grupperes aktiviteter under produksjonsordrer. Dette kan for eksempel være nyttig hvis du vil holde oversikt over alle jobbene som er knyttet til de samme bestillingene. I **Ressursvisning** grupperes alle jobber under enkeltressurser. Denne visningen kan være nyttig når du optimaliserer planen på et ressursnivå, for eksempel en maskin eller en gruppe maskiner. Gantt-diagrammene som er vist i illustrasjonene nedenfor, viser **Ordrevisning** og **Ressursvisning** med disse viktige elementer:

1.  Aktivitet i Gantt-diagram
2.  Materialmangel ikonet
3.  Materialtilgjengelighetsikon
4.  Ikon for dato for levering av bestillingen
5.  Kapasitetslinje

## <a name="order-view"></a>Ordrevisning

[![Ordrevisning](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Ressursvisning
[![Ressursvisning](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Aktiviteter
Aktivitetene vises som stolper og er organisert i et tidsskalarutenett med et planlagt start- og sluttidspunkt, slik at lengden på stolpene blir proporsjonal med tiden som er nødvendig for å fullføre aktiviteten. Aktivitetene vises i henhold til en tidsskala. Du kan justere tidsskalaen på menyen der du velger en startdato og sluttdato og en tidsenhet, for eksempel timer eller dager. Du kan sette fokus på et tidsintervall der du vil behandle aktiviteter ved å justere tidsskalaen. 

Hvis du vil ha en bedre oversikt, finner du ulike alternativer for å kontrollere fargen på aktivitetene. Du kan konfigurere en enkelt farge for aktiviteter, bruke temafargen som er det generelle fargetemaet som brukes for programmet, eller angi fargen som skal kontrolleres av fargekoden for produksjonsordrer. 

Tidsintervallet for aktiviteter har en sjattering i bakgrunnen. Perioder med en hvit sjattering angir et tidsintervall med definert kapasitet på ressursen for aktiviteten, mens perioder med en grå sjattering angir tidsintervaller med ingen kapasitet definert. 

På venstre side av diagrammet finner du mer informasjon om aktiviteten, for eksempel ressursen som aktiviteten er planlagt på, og produksjonsordrenummeret. Forbindelsen mellom jobber som tilhører den samme ordren, vises med en pil. 

Du kan få mer informasjon om en aktivitet i dialogboksen for aktiviteten. Dobbeltklikk aktiviteten for å åpne dialogboksen, eller velg menyen **Informasjon**. I dialogboksen for aktiviteten kan du se den planlagte start- og sluttdatooen og tidsinformasjon om hvilke materialer det er planlagt å bruke for aktiviteten. 

Aktivitetene kan grupperes i grupperingsnivåer. Grupperingsnivåene er hierarkiske og kan brukes til å lage en logisk gruppering av aktiviteter. Hvis du for eksempel har et oppsett der produksjonsaktiviteter grupperes etter område, produksjonsenheter, ressursgrupper og ressurser, kan du bruke grupperingsnivåene til å gruppere aktivitetene i henhold til dette oppsettet. Grupperingsnivåene kan vises og skjules på de individuelle grupperingsnivåene eller for alle nivåer i diagrammet ved hjelp av knappene **Vis alle** og **Skjul alle** på menyen. Du kan også konfigurere grupperingsnivåer for å vises eller skjules når diagrammet åpnes.

### <a name="material-availability"></a>Materialtilgjengelighet

Gantt-diagrammet kan defineres for å gi planleggeren detaljert informasjon om materialstatusen for de individuelle aktivitetene. Dette kan for eksempel være nyttig hvis material er forsinket og påvirker produksjonsplanen. I så fall blir materialavgangene merket i Gantt-diagrammet for å hjelpe planleggeren med å forstå konsekvenser og foreta justeringer. 

En jobb vises med et ikon for materialmangel hvis startdatoen for planen for jobben er senere enn datoen for materialtilgjengelighet for materialene som forbrukes av jobben. Materialtilgjengelighetsdatoen beregnes basert på utligningsinformasjonen i den dynamiske hovedplanen. Ikonet for materialmangel vises for eksempel på en jobb som bruker et materiale som er utlignet mot en bestilling som har et mottak som er senere enn planlagt startdato for jobben.

### <a name="indicator-of-material-availability-date"></a>Indikator for dato for materialtilgjengelighet

Når du definerer diagrammet for å vise jobber med materialmangler, kan det også vises et ikon for å vise datoen for materialtilgjengelighet for jobben. Ikonet vises kun hvis datoen for materialtilgjengelighet er innenfor det definerte tidsintervallet i diagrammet. Hvis materialtilgjengelighetsdatoen ligger utenfor det definerte tidsintervallet, kan mer detaljert informasjon for materialtilgjengelighet hentes fra materiallisten i dialogboksen for jobben. I listen er det også et ikon som viser sene materialer for jobben. Du kan planlegge en jobb med materialtilgjengelighetsdatoen som startdato.

### <a name="indicator-of-order-delivery-date"></a>Indikator for dato for levering av ordren

Dette ikonet angir leveringsdatoen for en produksjonsordre. Ikonet vises bare i ordrevisning.

### <a name="capacity-bar"></a>Kapasitetslinje

Du kan konfigurere diagrammet for å vise en ressurskapasitetslinje. Denne linjen inneholder en oversikt over ressurskapasiteten for en aktivitet i det definerte tidsintervallet i diagrammet. Kapasitetslinjen vises ikke for perioder der ressursen ikke er reservert. I perioder der ressursen er reservert til full kapasitet, vises kapasitetslinjen som en heltrukket linje. I perioder der ressursen er overbestilt, vises linjen tykkere og i rødt. Hvis for eksempel to jobber overlapper, angir kapasitetslinjen en overbooking i tidsintervallet der det er en overlapping. Kapasitetslinjen oppdateres dynamisk når du planlegger en jobb. Du aktiverer kapasitetslinjen på menyen **Vis kapasitetslinje**. Den kan bare vises i **ressursvisning**. Hvis du vil ha en mer detaljert visning av kapasitetsbelastningen for en ressurs, kan du bruke **Kapasitetsbelastning**-diagrammet, som kan åpnes fra menyen eller hurtigmenyen for en valgt aktivitet.

## <a name="job-scheduling-in-the-gantt-chart"></a>Finplanlegging i Gantt-diagrammet
Gantt-diagrammet inneholder ulike alternativer for å foreta justeringer i produksjonsplanen. I Gantt-diagrammet, kan du planlegge aktiviteter på nytt som en samhandling med dra og slipp eller fra en tidsplanmeny. I planleggingsprosessen kan du ta ressurskapasitet, ressursfunksjoner og materialbegrensninger i betraktning.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Planlegge en jobb som en samhandling med dra og slipp

Du kan planlegge jobben på nytt i det definerte tidsintervallet som en samhandling med dra og slipp. Du kan bare planlegge jobben på nytt på den samme ressursen, og du kan bare planlegge én jobb om gangen.

### <a name="schedule-a-job-from-the-menu"></a>Planlegge en jobb fra menyen

På **Planlegg jobber**-menyen kan du planlegge én eller flere valgte jobber i diagrammet basert på en planleggingsretning og en dato og et klokkeslett for planlegging. Det finnes tre tilgjengelige planleggingsretninger.

-   Fremover fra planleggingsdato
-   Bakover fra planleggingsdato
-   Fremover fra dato for materialtilgjengelighet

Det er ikke mulig å planlegge en jobb utenfor det definerte tidsintervallet i Gantt-diagrammet. Hvis du gjør dette, blir jobben værende uplanlagt, og du får feilmeldingen "Kan ikke planlegge jobb i den innlastede tidsperioden."

### <a name="schedule-previous-jobs"></a>Planlegg forrige jobber

I et nettverk av aktiviteter, for eksempel jobber som tilhører samme produksjonsordre, kan du bruke funksjonen **Planlegg forrige jobber** -til å planlegge de forrige jobbene i forhold til en valgt jobb i nettverket. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben. Diagrammet vises før en tidligere jobb er planlagt og etter den tidligere jobben er planlagt. 

[![Planlegge tidligere jobb](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Planlegg neste jobber

Du kan bruke funksjonen **Planlegg neste jobber** til å planlegge de neste jobbene i forhold til en valgt jobb i et nettverk av aktiviteter. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben. Diagrammet vises før neste jobb er planlagt og etter den neste jobben er planlagt. 

[![Tidsplan next job](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Planlegg rundt jobb

Du kan bruke funksjonen **Planlegg rundt jobb** til å planlegge den neste jobben og den forrige jobben i forhold til en valgt jobb i et nettverk av aktiviteter. I eksemplet nedenfor er den merkede aktiviteten den valgte jobben. Diagrammet vises før en jobb er planlagt, og etter at jobben er planlagt. 

[![Planlegg rundt jobb](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Ordne jobber

Du kan bruke den **Ordne**-funksjonen til å ordne merkede aktiviteter på den samme ressursen. Disse aktivitetene kan være i samme nettverk av aktiviteter, men kan også tilhøre forskjellige nettverk. Når du bruker funksjonen Ordne, elimineres tidsmellomrommene mellom de valgte aktivitetene. Du kan bruke denne funksjonen til å optimere kapasitetsutnyttelsen for ressursene. Diagrammet vises før en jobb er planlagt, og etter at jobben er planlagt. 

[![Ordne jobb](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Tilordne aktiviteter på nytt fra en ressurs til en annen

Du kan tilordne en jobb på nytt fra en ressurs til en annen. Dette kan være nyttig i situasjoner der en maskin er i ustand eller overbestilt, og du vil finne en annen tilgjengelig ressurs som kan gjøre jobben.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Tilordne en aktivitet på nytt som en samhandling med dra og slipp

I **Ressurs**-visningen kan du tilordne en aktivitet på nytt til en annen ressurs i Gantt-diagrammet som en samhandling med dra og slipp. Du kan gjøre dette ved å merke raden som aktiviteten er planlagt i. Når raden er valgt, kan du dra raden til ressursen i diagrammet gruppert under et annet ressursgrupperingsnivå.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Tilordne en aktivitet på nytt fra menyen Planlegg jobber

Du kan tilordne en jobb på nytt fra dialogboksen **Planlegg jobb** som åpnes fra menyen **Planlegg jobb**. På denne menyen kan du bare tilordne en jobb på nytt til en ressurs som allerede er lastet inn i Gantt-diagrammet. Hvis du bare velger én jobb, sorteres rullegardinlisten for ressursen etter gjeldende ressurser. Hvis du velger flere jobber, vil det ikke være noen informasjon om gjeldende ressurser fra ressurslisten.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Laste inn flere ressurser i Gantt-diagrammet
I **Ressursvisning** har du muligheten til å laste inn flere ressurser i Gantt-diagrammet. Dette kan være nyttig hvis du vil finne en alternativ ressurs for en jobb som er planlagt på en maskin som er overbestilt eller i ustand. På siden **Last inn tilleggsressurser** får du en liste over ressurser som er datogyldige per datoen som listen åpnes på. Gjeldende ressurser, i forhold til en valgt jobb i Gantt-diagrammet, vises først. Hvis du har flere jobber som er valgt, før du åpnet listen, vises ikke informasjon om gjeldende ressurser. På siden **Last inn tilleggsressurser** kan du velge én eller flere ressurser, som vil bli lastet inn i Gantt-diagrammet når du bekrefter valget. Hvis det ikke finnes noen jobber planlagt på den merkede ressursen i tidsintervallet i Gantt-diagrammet, plasseres ressursen under et ressursgrupperingsnivå nederst i listen over aktiviteter i Gantt-diagrammet.

### <a name="access-the-gantt-chart"></a>Få tilgang til Gantt-diagrammet

Gantt-diagrammet kan åpnes fra følgende sider.


|                                                 <strong>Side</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Beskrivelse</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Produksjonsordreoversikt og -detaljer</strong>                                    | På siden <strong>Produksjonsordreoversikt og -detaljer</strong> kan du åpne Gantt-diagrammet fra én eller flere av de valgte ordrene. Når du åpner diagrammet fra menyelementet <strong>Gantt-diagram</strong>, lastes alle jobber som er knyttet til de valgte produksjonsordrene, men også jobber fra andre produksjonsordrer som er planlagt på de samme ressursene. Når du åpner diagrammet fra menyelementet <strong>Gantt-diagram – hurtigvisning</strong>, lastes bare jobber som er knyttet til de valgte produksjonsordrene. I denne visningen er det ikke mulig å planlegge jobber. |
|                                               <strong>Ressurs</strong>                                                |                                                                                                                                                        På <strong>Ressurs</strong>-siden du kan åpne Gantt-diagrammet fra menyelementet <strong>Gantt-diagram</strong>. Når valgt, lastes alle jobbene som er planlagt på ressursen i en valgt tidsintervall, i diagrammet.                                                                                                                                                         |
|                                            <strong>Ressursgruppe</strong>                                             |                                                                                                                                                 På <strong>Ressursgruppe</strong>-siden du kan åpne Gantt-diagrammet fra menyelementet <strong>Gantt-diagram</strong>. Når valgt, vises alle jobbene som er planlagt på ressursene i ressursgruppen, i det valgte tidsintervallet.                                                                                                                                                 |
|                                             <strong>Gantt-diagrammer</strong>                                              |                                                                                 På <strong>Gantt-diagrammer</strong>-siden kan du konfigurere Gantt-diagrammer etter ressurser og ressursgrupper. Hvis du for eksempel vil kontrollere produksjonsaktiviteter for bestemte sett med ressurser eller ressursgrupper, kan du deretter gjøre enkeltkonfigurasjoner av disse på <strong>Gantt-diagrammer</strong>-siden. Du kan deretter åpne Gantt-diagrammet fra hver konfigurasjon.                                                                                 |
|                                       <strong>Timeprognoser</strong> (prosjekt)                                        |                                                                                                                              Prosjektaktiviteter av typen <strong>Timeprognoser</strong> kan finplanlegges på ressurser. På <strong>Timeprognose</strong>-siden på menyen <strong>Planlegging</strong> kan du åpne Gantt-diagrammet i en bestilling for å se finplanlagte prosjektaktiviteter av typen Timeprognose.                                                                                                                               |
|           <strong>Jobber som skal fullføres</strong> (liste i <strong>Produksjonsstyring</strong>-arbeidsområdet)            |                                                                                               Listen <strong>Jobber som skal fullføres i arbeidsområdet Produksjonsstyring</strong> viser jobber fra produksjons- og partiordrer som pågår på de merkede ressursene for arbeidsområdet. På menyelementet <strong>Gantt-diagram</strong> kan du åpne Gantt-diagrammet, der alle jobber som er valgt i listen vil bli lastet inn i diagrammet.                                                                                               |
| <strong>Produksjonsordrer som skal frigis</strong> (åpnes fra <strong>Produksjonsstyring</strong>-arbeidsområdet) |                                                                                                                                         Siden Produksjonsordrer som skal frigis åpnes fra <strong>Produksjonsstyring</strong>-arbeidsområdet. Denne siden viser planlagte produksjons- og partiordrer som venter på frigivelse. Du kan åpne Gantt-diagrammet for valgte produksjonsordrer på denne siden.                                                                                                                                          |

## <a name="additional-resources"></a>Tilleggsressurser  
[Visuell planlegging med Gantt-diagram for produksjon og batchordrer (video)](https://youtu.be/BtbuShkGj4I)

[Visuell planlegging for produksjon (demonstrasjonsskript)](https://mbs.microsoft.com/customersource/northamerica/365Enterprise/learning/documentation/how-to-articles/365finoptvisschep)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]