---
title: Feilanalyse av aktivum
description: Dette emnet beskriver feilanalyse for aktiva i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 67ccbb742bb4e2283c30b4dec055d137b4a51e40
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216419"
---
# <a name="asset-fault-analysis"></a>Feilanalyse av aktivum

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du analysere feilregistreringer for anleggsmidler for å få en oversikt over det totale antallet feil som er registrert i en bestemt periode. Feilregistreringer kan analyseres fra ulike perspektiver, for eksempel fokus på aktiva, anleggsmiddeltyper, arbeidssteder, feilsymptomer eller feiltyper.

1. Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Feilanalyse av aktivum**.

2. I dialogboksen **Beregning av feilanalyse av aktivum** kan du bruke **Nivå**-feltet til å angi hvor detaljert du vil at anleggsmiddellinjene skal være angående arbeidssteder. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle anleggsmiddellinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
        
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle anleggsmiddellinjer på alle arbeidsstedsnivået de er relatert til.

3. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer, feilårsaker og feilløsninger i hurtigfanen **Poster som skal inkluderes**.

4. Klikk på **OK** for å starte beregningen.

5. I kategorien **Feilanalyse av aktivum** klikker du én eller flere **Grupper etter**-knapper for å vise detaljnivået du vil se. Aktiverte knapper er uthevet. Aktiver eller deaktiver en knapp ved å klikke på den.

6. Klikk **Oppdater beregninger** for å vise valgene dine på skjermen. 

>[!NOTE]
>Hver gang du aktiverer eller deaktiverer en **Grupper etter** -knapp, må du huske å klikke på **Oppdater beregninger**-knappen. Dette er obligatorisk fordi en stor mengde data behandles når du beregner feilsannsynlighet på nytt.

## <a name="examples"></a>Eksempler

Det er mange måter å analysere feilregistreringer på. Denne delen inneholder fem eksempler som viser hvordan ulike datavalg kan gi mer innsikt og detaljer når du analyserer feilregistreringer for anleggsmidler.

### <a name="group-by-symptoms"></a>Gruppere etter symptomer

I skjermbildet nedenfor er det bare merket av for **Symptom**-knappen.

- Feilregistreringer er gjort på tre feilsymptomer: "Luftlekkasje", "Sikring er gått" og "Fastkjørt utstyr".  
- I kolonnen **Sannsynlighets-%** utgjør alle prosentdeler samlet 100 %. Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen.

![Figur 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a>Gruppere etter symptomer og tidsperiode

I skjermbildet nedenfor er **År** og **Måned** lagt til for å vise hvordan du kan vise feilregistreringer i en valgt periode.

- Feilsymptomene vises nå som registreringer per år/måned.  
- Hvis du legger til alle prosentdeler for hver måned i kolonnen **Sannsynlighets-%**, blir det 100 % til sammen. Sannsynlighet er basert på alle **Symptom**-registreringene i denne feilanalysen. Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.

![Figur 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a>Gruppere etter flere symptomer og aktiva

Kombinasjonen av aktiva og en aktivatype brukes som grunnlag for beregningene som vises i de tre skjermbildene nedenfor, som øker i detaljnivå.  

Knappene i handlingsrutegruppene **Grupper etter dato**, **Grupper etter aktiva**, **Grupper etter arbeidssted** samt **Feil**-knappen (feil-ID) inneholder vanligvis perioder eller aktivarelasjoner. Knappene **Symptom**, **Område**, **Type**, **Årsak** og **Løsning** er kategoriseringer som brukes i feilbehandling til å analysere registreringer av aktivafeil og finne problemområder.  

**Grupper etter symptom, aktiva og aktivatype**

I skjermbildet nedenfor ble **Aktiva** og **Aktivatype** lagt til for å gi mer informasjon om feilregistreringer.

- Feilsymptomene er nå delt opp i kombinasjoner av **Aktiva** / **Aktivatype** / **Symptom**.  
- Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom**, utgjør de 100 % til sammen. Sannsynlighet er basert på alle **Symptom**-registreringer i denne feilanalysen. Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilsymptom som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilsymptomet på.

![Figur 3](media/08-controlling-and-reporting.png)

**Grupper etter to symptomer, aktiva og aktivatype**

I skjermbildet nedenfor ble **Område** lagt til i **Symptom**, **Aktiva** og **Aktivatype** for å gi mer informasjon om feilregistreringer.

- Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen. Sannsynlighet er basert på kombinasjonen av **Symptom** og **Område** i denne feilanalysen. Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på et feilområde som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for dette feilområdet på.  

![Figur 4](media/09-controlling-and-reporting.png)

**Grupper etter tre symptomer, aktiva og aktivatyper**

I skjermbildet nedenfor ble **Type** lagt til, og den mest detaljerte beregningen i dette eksemplet vises.
 
- Hvis du i kolonnen **Sannsynlighets-%** legger til alle prosentdeler for kombinasjonen av **Aktiva** / **Aktivatype** / **Symptom** for et aktivum, utgjør de 100 % til sammen. Sannsynlighet er basert på kombinasjonen av **Symptom**, **Område** og **Type** i denne feilanalysen. Hvis du har et stort antall linjer i et anleggsmiddel, men en stor prosentdel vises på en linje, vil dette være en indikasjon på en feiltype som bør undersøkes nøyere for å finne en måte å begrense antall registreringer for denne feiltypen på.

![Figur 5](media/10-controlling-and-reporting.png)


>[!NOTE]
>Hvis du vil ha en oversikt over alle feilregistreringer som er opprettet på arbeidsordrer og vedlikeholdsanmodninger, klikker du **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Aktivafeil**. På siden **Aktivafeil** velger du en registrering av aktivafeil og utvider ruten **Beslektet informasjon** for å se informasjon om den beslektede arbeidsordren eller vedlikeholdsanmodningen.

