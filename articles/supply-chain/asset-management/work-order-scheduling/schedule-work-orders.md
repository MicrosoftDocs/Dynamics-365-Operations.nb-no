---
title: Planlegg arbeidsordrer
description: Dette emnet forklarer hvordan du planlegger arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 953c4bb17329205c5d8d14b6570a6bac152e9320
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652155"
---
# <a name="schedule-work-orders"></a>Planlegg arbeidsordrer

[!include [banner](../../includes/banner.md)]

 

Dette emnet forklarer hvordan du planlegger arbeidsordrer i Aktivastyring. 

Det nødvendige antallet timer for en arbeidsordre defineres av summen av prognosetimer minus posterte timer. Hvis det kreves mer tid, må prognosen justeres tilsvarende. I **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer** kan du vise eller redigere prognoser i en arbeidsordre ved å velge arbeidsordren og klikke på **Prognose** i kategorien **Arbeidsordre**. Når arbeidsordrer er opprettet og estimert, er neste trinn å tildele nødvendige vedlikeholdspersoner og verktøy.

Bare arbeidsordrer med en arbeidsordrelivssyklustilstand som tillater planlegging, kan planlegges. Tillat planlegging defineres i **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Livssyklustilstander** > **Generelt**-hurtigfanen > **Tillat planlegging**-veksleknappen.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer**.

2. Velg arbeidsordrene du vil planlegge, i listen. Du kan for eksempel sortere listen etter **Gjeldende livssyklustilstand**.

3. Gå til kategorien **Generelt**, og klikk på **Planlegg**.

4. I dialogboksen **Planlegg arbeidsordrer** kan du legge til valg som gjelder forventet startdato og servicenivå, om nødvendig. Hvis planleggingsprosessen skal observere kapasitetsbegrensninger for ressurser som allerede er planlagt for andre jobber, må du kontrollere at veksleknappene for **Aktivum**, **Verktøy** og **Arbeider** er satt til Ja.

    [!NOTE]
    Hvis du setter veksleknappene for **Aktivum**, **Verktøy** og **Arbeider** til Nei, vil eksisterende reservasjoner bli ignorert. I infologgen vises en liste over overlappende arbeidsordreplaner, og du kan klikke på meldingene for å åpne en arbeidsordre og planlegge på nytt om nødvendig.

5. Hvis du vil ha detaljert informasjon om planleggingsprosessen, velger du Ja på **Detaljert**-veksleknappen. Dette betyr at detaljert informasjon om de beregnede resultatene for arbeidsordrene og vedlikeholdspersonene vil vises i informasjonsloggen.

6. Klikk på **OK** for starte planleggingsprosessen.

7. Når planleggingen er fullført, viser en infologg antall arbeidsordrer som er planlagt, og også mer detaljert informasjon hvis **Detaljert**-veksleknappen var satt til Ja.

>[!NOTE]
>Arbeidsordrer planlegges i én syklus per arbeidsordre, ikke per arbeidsordrejobb. Du kan også åpne dialogboksen **Planlegg arbeidsordrer** direkte i **Aktivastyring** > **Periodisk** > **Arbeidsordrer** > **Planlegg arbeidsordrer**. Gjør valg, og klikk på **OK** for å starte arbeidsordreplanleggingen. Det er mulig å definere arbeidsordreplanlegging som en satsvis jobb i dialogboksen **Planlegg arbeidsordrer** > **Kjør i bakgrunnen**-hurtigfanen.

*Eksempel:* I figuren nedenfor vil formelen som er satt inn i **Forventet start**-feltet, generere arbeidsordreplanlegging for alle arbeidsordrer med forventet startdato en uke fra nå og senere. Denne formelen kan være nyttig når du kjører arbeidsordreplanlegging fortløpende, men vil sikre at arbeidsordrene som er planlagt for de neste 5-6 dagene, ikke planlegges på nytt.

![Figur 1](media/03-work-order-scheduling.png)

Arbeidsordretypen som er knyttet til arbeidsordrer, kan definere planlegging for én vedlikeholdsperson (**Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Arbeidsordretyper** > **Én vedlikeholdsperson**-veksleknappen satt til Ja). Dette betyr at hvis arbeidsordretypen brukes i en arbeidsordre, settes veksleknappen **Én vedlikeholdsperson** automatisk til Ja på detaljsiden **Alle arbeidsordrer** > **Hode**-visningen > **Tidsplan**-hurtigfanen. Under arbeidsordreplanleggingen vil alle arbeidsordrejobber som opprettes i arbeidsordren, bli planlagt til samme vedlikeholdsarbeider. Hvis det er nødvendig, kan du redigere valget på **Én vedlikeholdsperson**-veksleknappen i **Alle arbeidsordrer** slik at du kan planlegge flere arbeidere eller én arbeider for arbeidsordrejobbene.

Planleggingsprosessen i Aktivastyring omfatter flere faktorer i planleggingsberegningen:

- Beregne poeng for både arbeidsordrer og vedlikeholdsarbeidere. Poengene for arbeidsordrer og vedlikeholdsarbeidere defineres i **Parametere for aktivastyring**. 
- Se etter samsvarende kompetanser, dvs. ferdigheter og sertifikater som kreves for å utføre jobben. Kompetanser og sertifikater defineres under vedlikeholdspersoner i **Personale**-modulen (**Personale** > **Arbeidere** > **Arbeidere** > velg arbeider i listen > kategorien **Arbeider** > **Kompetanser**-delen > **Kompetanse**- og **Sertifikater**-knappene). Kompetanser og sertifikater kan også legges til vedlikeholdsjobbtyper og vedlikeholdsjobbfag. Les mer om kompetanser og vedlikeholdsjobbtyper i [Kategorier for vedlikeholdsjobbtyper og vedlikeholdsjobbtyper, varianter av vedlikeholdsjobbtyper, vedlikeholdsjobbfag og sjekklister for vedlikehold](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Poeng som brukes i arbeidsordreplanlegging

Beregning av poeng for en arbeidsordrejobb er basert på forventet startdato og servicenivå for arbeidsordren.

Beregning av **startdato**: For hver fremtidig dato som beregnes fra forventet startdato, trekkes startdatoen fra og multipliseres med poengsummen, som er 10 i eksemplene nedenfor.

Beregning av **kritikalitet**: Poeng for kritikalitet multiplisert med kritikaliteten for arbeidsordren.

Beregning av **servicenivå**: Servicenivåpoeng delt på servicenivået i arbeidsordren.

I eksemplene nedenfor er kritikalitetspoengene 2 og servicenivåpoengene er 5 og 100.

**Eksempel 1:**

| Arbeidsordre-ID | Forventet startdato | Kritikalitet for arbeidsordre | Servicenivå for arbeidsordre | Beregning               | Poengsum      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | I morgen            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | To dager fra nå   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | To dager fra nå   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Arbeidsordrene blir planlagt i følgende rekkefølge: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Eksempel 2:**

| Arbeidsordre-ID | Forventet startdato | Kritikalitet for arbeidsordre | Servicenivå for arbeidsordre | Beregning                 | Poengsum    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | I morgen            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | To dager fra nå   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | To dager fra nå   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Hvis servicenivåpoengene økes til 100 i stedet for 5, vil planleggingsrekkefølgen være: WO-000108**18**, WO-000108**16**, WO-000108**17**.

Vurderingsresultatene relatert til beregning av hvilke vedlikeholdsarbeidere som skal arbeide med arbeidsordrene, defineres som tall, som legges til hver vedlikeholdsarbeiderberegning under arbeidsordreplanleggingen. Vedlikeholdsarbeideren med høyest poengsum velges i arbeidsordren. Her er en kort beskrivelse av poengene for vedlikeholdsarbeideren:

| Poengsum for vedlikeholdsperson       | Beskrivelse                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ansvarlig arbeider | Hvis vedlikeholdspersonen er valgt som ansvarlig arbeider i arbeidsordren, legges poengene til.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ansvarlig vedlikeholdspersongruppe | Hvis vedlikeholdspersonen er del av den ansvarlige vedlikeholdsarbeidegruppen i arbeidsordren, legges poengene til.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Foretrukket vedlikeholdsperson         | Hvis arbeideren er valgt som foretrukket vedlikeholdsperson for aktivaet, legges poengene til.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Foretrukket vedlikeholdspersongruppe   | Hvis arbeideren er del av den foretrukne vedlikeholdspersongruppen for aktivaet, legges poengene til.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Lokasjon                 | Hvis firmaet bruker arbeidssteder, får vedlikeholdsarbeiderne full poengsum hvis de befinner seg på arbeidsstedet som er knyttet til anleggsmidlet. Hvis arbeidsstedet til anleggsmidlet har et overordnet sted, får vedlikeholdsarbeidere på dette arbeidsstedet 1/2 poeng. Hvis dette stedet også har et overordnet sted, får vedlikeholdsarbeidere på dette stedet 1/3 poeng. Hvis dette stedet også har et overordnet sted, får vedlikeholdsarbeidere på dette stedet 1/4 poeng osv. Hvis firmaet ditt bruker aktivasted, som vi ikke anbefaler, brukes sted, område og sone til å beregne stedspoengsummer. Arbeiderne får full poengsum hvis de befinner seg på stedet og i området og sonen som er knyttet til eiendelen. Hvis arbeiderstedet bare samsvarer med sted og område, er rangeringspoengsummen for vedlikeholdsarbeideren 2/3 for hele poengsummen. Hvis vedlikeholdsarbeiderstedet bare samsvarer med sted, er rangeringspoengsummen for vedlikeholdsarbeideren 1/3 for hele poengsummen. |
| Arbeiderens startdato               | For hver dato som den planlagte startdatoen er senere enn forventet startdato, trekkes poengsummen fra.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

>[!NOTE]
>Hvis en poengsum settes til 0, beregnes ikke denne poengsummen. Dette er nyttig hvis du for eksempel ikke vil ta med en ansvarlig arbeider i planleggingen.

## <a name="competencies-used-in-work-order-scheduling"></a>Kompetanser som brukes i arbeidsordreplanlegging

Krav til kompetanse og sertifikater kan defineres i vedlikeholdsjobbtyper (**Aktivastyring** > **Oppsett** > **Jobber** > **Vedlikeholdsjobbtyper**) og vedlikeholdsjobbfag (**Aktivastyring** > **Oppsett** > **Jobber** > **Vedlikeholdsjobbfag**). 

Vedlikeholdsjobbtyper og vedlikeholdsjobbfag velges i arbeidsordrejobber. Hvis kompetanse eller sertifikater er valgt for en vedlikeholdsjobbtype eller et vedlikeholdsjobbfag, og vedlikeholdsjobbtypen eller vedlikeholdsjobbfaget brukes på en arbeidsordrejobb, er det bare vedlikeholdsarbeidere med samsvarende ferdigheter og sertifikater som tilordnes til å jobbe på arbeidsordren.

