---
title: Vedlikeholdsplaner
description: Dette emnet beskriver vedlikeholdsplaner i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 28c00b5a2485ffcc01a316d2a39e7259fb563d1d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889055"
---
# <a name="maintenance-plans"></a>Vedlikeholdsplaner

[!include [banner](../../includes/banner.md)]

 

En vedlikeholdsplan definerer når en forhåndsplanlagt forebyggende vedlikeholdsjobb skal utføres på et aktivum. Vedlikeholdsplaner kan knyttes til aktiva, aktivatyper, arbeidssteder eller arbeidsstedstyper, men først må du opprette vedlikeholdsplanene som skal brukes i selskapet ditt.

En vedlikeholdsplan kan ha flere linjer for vedlikeholdsplanen. Vedlikeholdsjobbtype og intervall angis på vedlikeholdsplanlinjen. Det finnes to typer av vedlikeholdsplanlinjer:

- Tidspunkt  
- Teller  

Vedlikeholdsplanlinjer av typen Tidspunkt brukes for regelmessig planlagt vedlikehold basert på et fast tidsintervall. Vedlikeholdsplanlinjer av typen Teller brukes for planlagt vedlikehold eller reaktivt vedlikehold basert på aktivatellerregistreringer. En vedlikeholdsplan kan inneholde flere vedlikeholdsplanlinjer av begge typer.

>[!NOTE]
>Hvis ingen tellerverdier er registrert for en tellertype på et aktiva, utelates vedlikeholdsplanlinjene.

Først oppretter du vedlikeholdsplanene du trenger for de forebyggende vedlikeholdsjobbene, og velger aktivatyper, aktiva, arbeidsstedstyper og arbeidssteder som skal knyttes til hver vedlikeholdsplan. Etterpå kan du om nødvendig også legge til vedlikeholdsplaner for et aktivum eller et arbeidssted, som gjøres i **Alle aktiva** > velg aktivum > **Vedlikeholdsplaner for aktivum**-hurtigfanen eller **Alle arbeidssteder** > velg arbeidssted > **Vedlikeholdsplaner**-hurtigfanen.

Hvis du legger til en vedlikeholdsplan for aktivatyper eller arbeidsstedstyper, betyr det at når du oppretter nye aktiva eller arbeidssteder med disse aktivatypene eller arbeidsstedstypene, legges aktivaet eller arbeidsstedet til vedlikeholdsplanen automatisk. Startdatoen for relasjonen til en vedlikeholdsplan vil være gjeldende dato, som kanskje må justeres.

## <a name="set-up-maintenance-plans"></a>Definer vedlikeholdsplaner

Denne delen beskriver hvordan du definerer linjer for vedlikeholdsplaner, og gir eksempler på hvordan de kan brukes.

1. Klikk på **Aktivastyring** > **Oppsett** > **Forebyggende vedlikehold** > **Vedlikeholdsplaner**.

2. Klikk på **Ny** for å opprette en ny sekvens.

3. Sett inn en ID i **Vedlikeholdssekvens**-feltet og et navn i **Navn**-feltet.

4. I **Plandato**-feltet setter du inn startdatoen som planleggingen kan utføres fra, i vedlikeholdsplanen. Vær oppmerksom på at tidsbaserte vedlikeholdsplanlinjer kan ha andre plandatoer.

5. Velg Ja på **Aktiver**-veksleknappen for å aktivere vedlikeholdsplanen.

>[!NOTE]
>Hvis du deaktiverer en vedlikeholdsplan, vil ingen planlagte poster bli opprettet i vedlikeholdsplanen når du kjører en planlagt vedlikeholdsplanjobb.

6. Feltene **Toleransedager før** og **Toleransedager etter** er relatert til vedlikeholdsplanlinjer der **Utelat overlappende vedlikeholdsjobber** er avmerket (se trinn 17). Toleranse-feltene brukes til å utvide intervallet i dager der, hvis flere vedlikeholdsplaner overlapper, den mest omfattende/største jobben opprettes som en vedlikeholdsplanlinje under vedlikeholdsplanplanleggingen, men oftere, utelates overlappende jobber under vedlikeholdsplanplanleggingen. Sett inn antall dager i **Toleransedager før**-feltet, for eksempel 2.

7. Hvis du har satt inn en verdi i **Toleransedager før**, kan du også sette inn antall dager i **Toleransedager etter**-feltet, for eksempel 2.

>[!NOTE]
>Eksemplet som beskrives i dette og det forrige trinnet, betyr at hvis flere vedlikeholdsplanlinjer overlapper og **Utelat overlappende vedlikeholdsjobber** er valgt for én eller flere linjer, forlenges perioden for å utelate vedlikeholdsplanlinjer til totalt fem dager (forventet startdato på vedlikeholdsplanlinjen *og* to dager før *og* to dager etter denne datoen).

8. Feltene i **Detaljer**-gruppen i hurtigfanen **Detaljer** viser antall vedlikeholdsplanlinjer som er definert i vedlikeholdsplanen, og antall aktiva og arbeidssteder som er knyttet til vedlikeholdsplanen.

9. I hurtigfanen **Linjer** klikker du på **Legg til tidslinje** eller **Legg til aktivatellerlinje** for å opprette en ny vedlikeholdsplanlinje.

10. Sett inn en beskrivelse for linjen i feltet **Beskrivelse av arbeidsordre**. Beskrivelsen overføres til tilknyttede arbeidsordrer.

11. I feltet **Vedlikeholdsjobbtype** velger du jobbtypen som vedlikeholdsplanlinjen er knyttet til.

12. I feltene **Variant av vedlikeholdsjobbtype** og **Handel** velger du varianten og handel for vedlikeholdsjobbtypen.

13. I feltene **Fullfør innen dager** og **Fullfør innen timer** kan du sette inn forventet sluttdato i dager eller timer. Den forventede sluttdatoen settes inn i forhold til forventet startdato, som beregnes når linjer for vedlikeholdsplan opprettes. Du kan for eksempel sette inn 7 i feltet **Fullfør innen dager** for å angi at den tilknyttede jobben skal fullføres innen en uke fra forventet startdato.

14. I **Intervalltype**-feltet velger du intervalltypen som skal brukes på vedlikeholdsplanlinjen, for eksempel Gjentatt... eller Én gang... Se tabellen [Oversikt over intervalltyper](## Interval types overview) hvis du vil ha en beskrivelse av relasjonen mellom intervalltyper og linjetyper.

15. **Periode**-feltet er bare knyttet til tidsbaserte linjetyper. Velg periodetypen som er knyttet til periodefrekvensen.

16. I **Periodefrekvens**-feltet setter du inn antall ganger linjen skal brukes til planlegging av forebyggende vedlikeholdsjobber. Eksempel: Hvis du har opprettet en linje av typen Teller, og telleren er produksjonsantall, og du setter inn tallet 20 000 i dette feltet, opprettes nye vedlikeholdssekvenslinjer under forebyggende vedlikeholdsplanlegging hver gang du forventes å produsere 20 000 flere varer.

17. Avmerkingsboksen **Utelat overlappende vedlikeholdsjobber** er knyttet til tidsbaserte og tellerbaserte linjetyper. Merk av i avmerkingsboksen for å slette vedlikeholdsplanoppføringer som er opprettet på samme dato. Dette er relevant hvis du for eksempel har opprettet en 1-måneds inspeksjonslinje, en 6-måneders inspeksjonslinje og en 1-års inspeksjonslinje. For 1-årsinspeksjonen vil du bare at denne inspeksjonen skal utføres, ikke de andre to inspeksjonene, som også passer i tidsrammen. Hvis du vil definere dette eksemplet riktig, angir du 1-års inspeksjonslinjen som den første linjen, 6-månederslinjen som andre linje og 1-månedslinjen som tredje linje, og du merker av for **Utelat overlappende vedlikeholdsjobber** for 1-måneds- og 6-månederslinjene. På den måten sikrer du at når du kommer til 1-årsmerket, utelates inspeksjonene for én måned og seks måneder, og det opprettes bare en vedlikeholdsplanlinje for 1-års inspeksjonslinjen.

>[!NOTE]
>Eksemplet som beskrives i dette trinnet, viser at den mest omfattende jobben, som inneholder det største antallet oppgaver, og som ikke gjøres så ofte, alltid skal settes inn som første linje. De mer hyppige jobbene settes deretter inn som separate linjer etter frekvens, noe som plasserer den hyppigste jobben nederst på listen.

18. **Teller**-feltet er bare knyttet til tellerbaserte linjetyper. Velg tellertypen som skal brukes på linjen. Hvis en tellertype ikke er aktiv for et tilknyttet aktivum, utelates vedlikeholdsplanlinjen.

19. Feltet **Aktivatellerhorisont i dager** gjelder bare for tellerbaserte linjetyper. Sett inn et tall som definerer hvor mange dager tilbake tellerregistreringer kontrolleres når vedlikeholdsplanplanlegging utføres. Dette betyr hvor langt tilbake data (eksisterende tellerregistreringer) brukes som grunnlag for å beregne trenden som bestemmer hvor mange vedlikeholdsplanlinjer som skal opprettes.

>*Eksempel:* Hvis det forventes at tellerregistreringer foretas én gang i måneden, kan du sette inn tallet 365 i dette feltet fordi planlegging av vedlikeholdsplan alltid baserer seg på de siste 12 månedene og dermed oppretter vedlikeholdsplanlinjer basert på trenden i det siste året. Hvis du derimot setter inn tallet 10 i dette feltet, forventer du at tellerregistreringer skal gjøres oftere, for eksempel daglig. Dette betyr at når du planlegger vedlikeholdsplan, brukes tellerregistreringer for de 10 siste dagene som grunnlag for planleggingen av vedlikeholdsplanlinjer.

20. **Plandato**-feltet er bare knyttet til tidsbaserte linjetyper. Hvis vedlikeholdsplanlinjen har en annen planleggingsdato enn hele vedlikeholdsplanen, velger du en dato i **Plandato**-feltet på linjen.

21. I **Servicenivå**-feltet kan du velge et servicenivå for arbeidsordren som en ytterligere avgrensning på vedlikeholdsplanlinjen – som skal brukes som et servicenivå i arbeidsordrer.

22. Merk av for **Opprett automatisk** hvis du vil at en arbeidsordre skal opprettes automatisk i henhold til den valgte vedlikeholdsplanlinjen når vedlikeholdsplaner planlegges.

23. Hvis du har merket av for **Opprett automatisk**, kan du velge en arbeidsordretype for den automatisk opprettede arbeidsordren i feltet **Arbeidsordretype**. Hvis du har merket av for **Opprett automatisk**, og du ikke velger en arbeidsordretype i dette feltet, vil arbeidsordretypen som er valgt i **Aktivastyring** > **Oppsett** > **Aktivabehandlingsparametere** > **Arbeidsordrer**-koblingen > **Preventiv arbeidsordretype**-feltet, brukes.

24. Bruk feltene **Sesong fra** og **Sesong til** for å opprette en gjentatt tidsbasert vedlikeholdsplanlinje innenfor en 12-måneders periode. *Eksempel:* Utstyr som brukes til å vedlikeholde grøntområder, krever service hver vår i en forhåndsdefinert periode. Sett inn startdatoen for perioden som skal gjentas, i **Sesong fra**-feltet.

25. Sett inn sluttdatoen for perioden som skal gjentas, i **Sesong til**-feltet.

26. I feltet **Resulterende periode** vises den gjeldende perioden som skal gjentas. Når gjeldende periode er passert, og du starter et nytt år, oppdateres perioden som vises i dette feltet, for å gjenspeile neste periode i gjentakelsessekvensen.

27. I hurtigfanen **Aktiva** velger du aktivaene som skal relateres til vedlikeholdsplanen.

28. I hurtigfanen **Aktivatyper** velger du aktivatypene som skal relateres til vedlikeholdsplanen.

29. I hurtigfanen **Arbeidssteder** velger du arbeidsstedene som skal relateres til vedlikeholdsplanen. Hvis det er nødvendig, kan du gjøre oppsettet mer spesifikt ved å velge en relatert aktivatype, produsent og modell.

30. I hurtigfanen **Arbeidsstedstyper** velger du arbeidsstedstypene som skal relateres til vedlikeholdsplanen.

>[!NOTE]
>Når arbeidsordrer opprettes manuelt for aktiva som dekkes av en leverandørgaranti, vises en dialogboks for å gjøre brukeren oppmerksom på garantien. Opprettingen av arbeidsordren kan deretter avbrytes. Kontrollen av en garantirelasjon utelates for arbeidsordrer som opprettes automatisk.

## <a name="interval-types-overview"></a>Oversikt over intervalltyper

| Intervalltype og beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                       | Linjetype: Tidspunkt                                                                                                                                                                                                                                                                                                                                                           | Linjetype: Teller                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Intervalltype: Gjentas fra plandato** Opptellingen starter fra plandatoen som brukes. Når du planlegger vedlikeholdsplaner, opprettes det vedlikeholdsplanlinjer når intervallet nås.                                                                                                                                                                                                                | **Plandato** på vedlikeholdsplanlinjen brukes. Hvis ingen plandato er valgt på linjen, brukes **Plandato** for vedlikeholdsplanen. Eksempel: Hvis tallet 3 settes inn i feltet **Periodefrekvens** og År velges i feltet **Periode**, vil det opprettes en ny vedlikeholdsplanlinje én gang hvert 3. år.                             | **Plandato** for vedlikeholdsplanen brukes. Hvis telleren er erstattet, brukes den siste erstatningsdatoen som plandato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Intervalltype: Gjentatt fra startdato** Tellingen starter fra startdatoen for aktivarelasjonen. Datoen velges i **Alle aktiva**-detaljvisningen > **Vedlikeholdsplaner for aktivum**-hurtigfanen > **Startdato**-feltet, eller i detaljvisningen **Alle arbeidssteder** > **Vedlikeholdsplaner**-hurtigfanen > **Startdato**-feltet. Når du planlegger vedlikeholdsplaner, opprettes det en vedlikeholdsplanlinje når intervallet nås. | Startdatoen på vedlikeholdsplanlinjen for aktivum eller arbeidssted brukes. Hvis dette feltet er tomt, brukes **Plandato** for vedlikeholdsplanen.                                                                                                                                                                                                 | Startdatoen på vedlikeholdsplanlinjen for aktivum eller arbeidssted brukes. Hvis dette feltet er tomt, brukes **Plandato** for vedlikeholdsplanen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Intervalltype: Gjentatt fra siste arbeidsordre** Tellingen starter fra den faktiske sluttdatoen og tidspunktet for den siste arbeidsordren som ble fullført for aktivumet med den spesifikke kombinasjonen av vedlikeholdsjobbtypen / variant av vedlikeholdsjobbtype / handel. Datoen og klokkeslettet vises i feltet **Faktisk slutt** i detaljvisningen **Alle arbeidsordrer**.                                                                                                                                 | Den faktiske sluttdatoen og tidspunktet for den fullførte arbeidsordren for aktivumet med den spesifikke kombinasjonen av vedlikeholdsjobbtype / variant av vedlikeholdsjobbtype / handel. Hvis det ikke blir funnet noen fullførte arbeidsordrer, brukes i stedet en av datoene som er brukt i intervalltypen Gjentatt fra startdato som er beskrevet ovenfor.                                                                                             | Den faktiske sluttdatoen og tidspunktet for den fullførte arbeidsordren for aktivaet *og* kombinasjonen av vedlikeholdsjobbtype / variant av vedlikeholdsjobbtype / handel. er brukt. Hvis sluttdatoen og tidspunket står tomme i arbeidsordren, brukes i stedet en av datoene som er brukt i intervalltypen Gjentatt fra startdato som er beskrevet ovenfor.                                                                                                                                                                                                                                                                                                                                                                           |
| **Intervalltype: Én gang fra plandato** Se beskrivelse for intervalltypen Gjentatt fra plandato ovenfor. Den eneste forskjellen er at denne intervalltypen bare kan brukes én gang.                                                                                                                                                                                                                                                   | Se beskrivelse for intervalltypen Gjentatt fra plandato ovenfor. Dette intervallet brukes vanligvis for en engangs vedlikeholds- eller servicejobb.                                                                                                                                                                                                                             | Se beskrivelse for intervalltypen Gjentatt fra plandato ovenfor. Dette intervallet brukes vanligvis for en engangs vedlikeholds- eller servicejobb. **Merknad 1:** Denne intervalltypen er bare relevant hvis telleren erstattes hver gang du utfører en vedlikeholds- eller servicejobb. Hvis en teller av en eller annen grunn er blitt erstattet før slutten på det planlagte intervallet, blir det beregnet et nytt tidspunkt for jobben fra tidspunktet for tellererstatningen. **Merknad 2:** Hvis telleren erstattes når vedlikeholds- eller servicejobben fullføres, fungerer denne intervalltypen som intervalltypen Gjentatt fra plandato ovenfor.                                             |
| **Intervalltype: Én gang fra startdato** Se beskrivelse for intervalltypen Gjentatt fra startdato ovenfor. Den eneste forskjellen er at denne intervalltypen bare kan brukes én gang.                                                                                                                                                                                                                                                 | Se beskrivelse for intervalltypen Gjentatt fra startdato ovenfor. Dette intervallet brukes vanligvis for en engangs vedlikeholds- eller servicejobb.                                                                                                                                                                                                                            | Se beskrivelse for intervalltypen Gjentatt fra startdato ovenfor. Dette intervallet brukes vanligvis for en engangs vedlikeholds- eller servicejobb. **Merknad 1** ovenfor gjelder også for denne intervalltypen. **Merknad 3:** Hvis telleren erstattes når vedlikeholds- eller servicejobben fullføres, fungerer denne intervalltypen som intervalltypen Gjentatt fra startdato ovenfor.                                                                                                                                                                                                                                                                                                |
| **Intervalltype: Når nådd over** Denne intervalltypen gjelder bare for tellere, og brukes for å angi en øvre grense som er definert på vedlikeholdsplanlinjen. Vedlikeholdsplanoppføringer vil ha forventet startdato og -klokkeslett for tellerregistreringen, noe som betyr at disse oppføringene vil bli opprettet med en forventet startdato som er lik eller før systemdatoen.                                                | Ikke tilgjengelig                                                                                                                                                                                                                                                                                                                                                                       | Tellerintervallet angir en øvre grense. Hvis denne grensen overskrides når du oppretter en tellerregistrering, opprettes en vedlikeholdsplanlinje når du planlegger forebyggende vedlikehold.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Intervalltype: Når nådd under** Denne intervalltypen gjelder bare for tellere, og brukes for å angi en nedre grense som er definert på vedlikeholdsplanlinjen. Vedlikeholdsplanoppføringer vil ha forventet startdato og -klokkeslett for tellerregistreringen, noe som betyr at disse oppføringene vil bli opprettet med en forventet startdato som er lik eller før systemdatoen.                                                 | Ikke tilgjengelig                                                                                                                                                                                                                                                                                                                                                                       | Tellerintervallet angir en nedre grense. Hvis denne grensen passeres når du oppretter en tellerregistrering, opprettes en vedlikeholdsplanlinje når du planlegger forebyggende vedlikehold.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Intervalltype: Koblet fra startdato** Denne intervalltypen oppretter bare en vedlikeholdsplanlinje én gang. En vedlikeholdsplan kan inneholde flere vedlikeholdsplanlinjer som bruker denne intervalltypen, og disse linjene er koblet. Vanligvis vil du opprette en vedlikeholdsplan som bare inneholder linjer av denne intervalltypen. Vedlikeholdsplanlinjer opprettes ved å identifisere vedlikeholdsplanlinjen som har den første forventede startdatoen og -klokkeslettet.                                                                                                                                                                                                                                                                                                                                                                                           | Se beskrivelse for Én gang fra startdato ovenfor. Eksempel: Du oppretter to linjer i en vedlikeholdsplan for en servicejobb på en bil: én tidsbasert linje med en 1-årsperiode, og én tellerbasert linje med en 25 000 km-grense. Det opprettes en vedlikeholdsplanlinje for grensen som nås først. For denne linjetypen oppretter du linjen med 1-årsperioden.                                                                                                                                                                                   | Se beskrivelse for Én gang fra startdato ovenfor. Eksempel: Du oppretter to linjer i en vedlikeholdsplan for en servicejobb på en bil: én tidsbasert linje med en 1-årsperiode, og én tellerbasert linje med en 25 000 km-grense. Det opprettes en vedlikeholdsplanlinje for grensen som nås først. For denne linjetypen oppretter du linjen med 25 000 km-grensen. Eksempel der to tellerlinjer opprettes: Du kan også definere en vedlikeholdsplan med to koblede, tellerbaserte linjer der den første linjen har en grense på 10 000 produserte varer, og den andre linjen er knyttet til maskinen eller arbeidssenteret som trenger service etter 3 000 timers drift.                                                                                                                                                           |
| **Intervalltype: Koblet fra siste arbeidsordre** Denne intervalltypen oppretter nye vedlikeholdsplanlinjer etter hver fullførte arbeidsordre. En vedlikeholdsplan kan inneholde flere linjer som bruker denne intervalltypen, og disse linjene er koblet. Vanligvis vil du opprette en vedlikeholdsplan som bare inneholder vedlikeholdsplanlinjer av denne intervalltypen. Vedlikeholdsplanlinjer opprettes ved å identifisere vedlikeholdsplanlinjen som har den første forventede startdatoen og -klokkeslettet.                                                                                                                                                                                                                                                                        | Denne intervalltypen fungerer hovedsakelig som Koblet fra startdato, som er beskrevet ovenfor. Den eneste forskjellen er datoen som intervalltypen er basert på. Datoen som brukes, er den faktiske datoen og tidspunktet for den siste fullførte arbeidsordren for aktivaet *og* kombinasjonen av vedlikeholdsjobbtype / variant av vedlikeholdsjobbtype / handel.                                                                                                                                                                                                                                                           | Denne intervalltypen fungerer hovedsakelig som Koblet fra startdato, som er beskrevet ovenfor. Den eneste forskjellen er datoen som intervalltypen er basert på. Datoen som brukes, er den faktiske datoen og tidspunktet for den siste fullførte arbeidsordren for aktivaet *og* kombinasjonen av vedlikeholdsjobbtype / variant av vedlikeholdsjobbtype / handel.                                                                                                                   |


>[!NOTE]
>Når vedlikeholdsplanlinjer opprettes for tidsbaserte vedlikeholdsplanlinjer, er forventet tidspunkt alltid på begynnelsen av dagen. For tellerbaserte vedlikeholdsplanlinjer kan forventet tidspunkt være når som helst på dagen.

Nedenfor finner du eksempler på oppsett av tidsbaserte og tellerbaserte vedlikeholdsplanlinjer:

**Eksempel 1 – tidsbasert vedlikeholdsplanlinje**: En smørejobb kan settes opp med et fast intervall, og skjer én gang i uken. For dette formålet kan du velge Gjentatt fra plandato i **Intervall type**-feltet. Se et eksempel i illustrasjonen nedenfor.

![Figur 1](media/02-preventive-maintenance.png)

**Eksempel 2 – tidsbasert vedlikeholdsplanlinje** : En inspeksjonsjobb kan defineres til å utføres omtrent én gang i uken. For dette formålet kan du velge Gjentatt fra siste arbeidsordre i **Intervall type**-feltet. Se et eksempel i illustrasjonen nedenfor.

![Figur 2](media/03-preventive-maintenance.png)

**Eksempel 3 – tellerbasert vedlikeholdsplanlinje**: Den grafiske illustrasjonen nedenfor viser en timeteller som det opprettes en ny vedlikeholdsplanlinje for hver gang det har gått 250 timer. Intervalltypen for denne tellerbaserte linjen er Gjentatt fra startdato. Startdatoen er startdatoen for de tilknyttede aktivaene i **Alle aktiva**-detaljvisningen > **Vedlikeholdsplaner for aktivum**-hurtigfanen > **Startdato**-feltet, eller i detaljvisningen **Arbeidssted** > **Vedlikeholdsplaner**-hurtigfanen > **Startdato**-feltet. Dette er et eksempel på en *forebyggende* vedlikeholdsplan fordi vedlikeholdsplanlinjen opprettes automatisk hver gang terskelen (+ 250) nås.

![Figur 3](media/04-preventive-maintenance.png)


**Eksempel 4 – tellerbasert vedlikeholdsplanlinje**: Den grafiske illustrasjonen nedenfor viser en reduksjon i tellerverdi, som måler bremseklosslitasje. En vedlikeholdsplanlinje opprettes når en tellerregistrering under 20 mm opprettes for bremseklossen. Intervalltypen for denne tellerbaserte linjen er "Når nådd under" eller "Én gang fra siste startdato". Dette er et eksempel på en *reaktiv* vedlikeholdsplan fordi vedlikeholdsplanlinjen opprettes ikke før en måling under 20 mm registreres.

![Figur 4](media/05-preventive-maintenance.png)


**Eksempel 5 – tellerbasert vedlikeholdsplanlinje**: Den grafiske illustrasjonen nedenfor viser en teller med en terskel på -18 ° Celsius. En vedlikeholdsplanlinje opprettes når det gjøres en tellerregistrering over -18 ° Celsius. Intervalltypen for denne tellerbaserte linjen er Når nådd over. Dette er et eksempel på en *reaktiv* vedlikeholdsplan fordi vedlikeholdsplanlinjen opprettes ikke før en måling høyere enn -18 ° Celsius registreres.

![Figur 5](media/06-preventive-maintenance.png)

- Når du oppretter et nytt aktivum og dette aktivaet bruker en aktivatype som er knyttet til en vedlikeholdsplan, settes vedlikeholdsplanen automatisk inn i **Alle objekter** > **Vedlikeholdsplaner for aktivum**-hurtigfanen. I **Standarder for aktivatype** på hurtigfanen **Vedlikeholdsplaner** settes også de tilknyttede vedlikeholdsplanene automatisk inn.  
- Hvis du legger til eller fjerner aktivatyper eller arbeidsstedstyper i **Vedlikeholdsplaner**, vil denne endringen bare reflekteres i nye aktiva som opprettes etter du gjorde endringen.  
- Hvis du legger til eller fjerner aktiva eller arbeidssteder i **Vedlikeholdsplaner**, blir denne endringen automatiske oppdatert i **Alle aktiva** > **Vedlikeholdsplaner for aktivum**-hurtigfanen eller i **Alle arbeidssteder** > **Vedlikeholdsplaner**-hurtigfanen.  

Illustrasjonen nedenfor viser et eksempel på en vedlikeholdsplan for lastebilservice på siden **Vedlikeholdsplaner**.

![Figur 6](media/07-preventive-maintenance.png)


## <a name="add-a-maintenance-plan-to-an-asset"></a>Legge til en vedlikeholdsplan for et aktivum

1. Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva** eller **Aktive aktiva**.

2. Velg aktivaet du vil definere en vedlikeholdsplan for, og klikk på **Rediger.**

3. I hurtigfanen **Vedlikeholdsplaner for aktivum** klikker du på **Legg til linje** for å legge til en vedlikeholdsplan for aktivaet.

4. I feltet **Vedlikeholdsplan** velger du den aktuelle vedlikeholdsplanen.

5. I **Startdato**-feltet velger du datoen som planleggingen av forebyggende vedlikeholdsjobber kan utføres fra. 

6. Klikk **Lagre**. **Aktiv**-feltet oppdateres automatisk.

Illustrasjonen nedenfor viser et eksempel på vedlikeholdsplaner for et aktivum på siden **Alle aktiva**.

![Figur 7](media/08-preventive-maintenance.png)

