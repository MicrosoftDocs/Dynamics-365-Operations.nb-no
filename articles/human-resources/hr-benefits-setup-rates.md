---
title: Konfigurere satser
description: Satser i Microsoft Dynamics 365 Human Resources definerer hvor mye arbeidsgivere og ansatte bidrar til en fordel.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039b4aa3f044cda29944bcd4f5c42fc35818c58b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868166"
---
# <a name="configure-rates"></a>Konfigurere satser


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Satser definerer hvor mye arbeidsgivere og ansatte bidrar til en fordel. Verdien kan være et beløp eller flere fleksible kreditter, avhengig av konfigurasjonen.

Bruk satser til å bestemme hvor mye ansatte og arbeidsgivere skal betale for hver fordel, basert på flere faktorer. Dekningssatser gjelder for dato, slik at du kan holde en historisk oversikt over satser. 

## <a name="set-up-rates"></a>Definere satser

1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Satser**.

2. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | Beskrivelse |
   | --- | --- |
   | **Sats** | Et unikt navn som identifiserer fordelssatsen. |
   | **Beskrivelse** | En beskrivelse av fordelssatsen. |
   | **Effektiv** | Datoen satsen blir aktiv. Standardverdien er gjeldende systemdato. Denne datoen bør være på eller før fordelsperioden. En god praksis er å sette denne datoen til datoen for fordelsplanen. |
   | **Utløp** | Sluttdatoen for satsen. 12/31/2154 (som betyr aldri) er standardverdien. |
   | **Bruk lag** |  Bruk dette feltet hvis du har logikk som må brukes til å bestemme en sats. Hvis for eksempel en sats må øke basert på alder, velger du en verdi her. Velg **Enkelt lag** for en fordelssats på ett lag, eller et **dobbelt nivå** for en fordelssats på to lag. Et eksempel på et dobbelt lag er et lag basert på kjønn og alder. Når du har valgt en verdi, velger du **Handlinger** og deretter **Lagsatser**. Hvis du har en flat sats som ikke endres, lar du dette feltet stå tomt. |
   | **Betalingsfrekvens** | Angi hvor ofte fordelspremieprisen skal betales til fordelsleverandøren. Satsene du angir på siden som er beskrevet senere i denne artikkelen, er basert på betalingsfrekvensen du angir her. Hvis du for eksempel angir **Månedlig** i dette feltet, og du angir en ansattsats på **USD 100**, antas det at fordelen vil koste den ansatte USD 100 per måned. En ansatt kan imidlertid bli betalt to ganger i måneden, basert på fordelsbetalingsfrekvensen som er angitt på ansattposten. Når den ansatte logger seg på **selvbetjening for ansatte**, vil beløpet som de betaler, i dette tilfelle være USD 50 fordi satsen som **ansattselvbetjeningen** viser, er basert på den ansattes betalingsfrekvens. |
   | **Avrunding av sats for lønnsfrekvens** | Metodene for avrunding av satsen er: Standard, Avrunding, Normal, Nedover og Avrunding opp. </br></br><ul><li>**Standard** – Avrundes alltid oppover. 10,611 avrunder for eksempel til 10,62. -10,231 avrunder til -10,23. </li><li>**Avrunding** – Avrundes alltid nedover. 10,619 avrunder for eksempel til 10,61. -10,231 avrundes til -10,24. </li><li>**Normal** – Desimalverdier som slutter på eller er større enn 5, rundes fra null. Desimalverdier som slutter på eller mindre enn 4, avrundes mot null. 10,615 avrundes for eksempel til 10,62. -10,235 avrundes til -10,24. 10,614 avrundes til 10,61. -10,234 avrundes til -10,23. </li><li>**Nedover** – Avrund mot null. 10,619 avrunder for eksempel til 10,61. -10,231 avrunder til -10,23. </li><li>**Avrundes opp** – Rund av fra null. 10,619 avrunder for eksempel til 10,62. -10,231 avrundes til -10,24. |
   | **Beløp for ikke-røykende ansatt** | Beløpet som fordelsleverandøren tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for ikke-røykende arbeidsgiver** | Beløpet som fordelsleverandøren tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for røykende ansatt** | Beløpet som fordelsleverandøren tar betalt for en ansatt som røyker. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for røykende arbeidsgiver** | Beløpet som fordelsleverandøren tar betalt for en ansatt som røyker. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Administrativt beløp** | Det administrative beløpet som belastes av en tredjeparts administrator. Dette er beløpet som arbeidsgiveren betaler til den tredjeparts administratoren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Fleksikredittsats** | Antall fleksible kreditter som fordelen koster. Dette gjelder bare satser som er for fordelsplaner som er tilknyttet fleksible kredittprogrammer. Hvis du bruker lagsatser, blir satsen for den fleksible kreditten definert i Handlinger > Lagsatser. |
   | **Ikrafttredelsesdato for endring** | Datoen når endringen av fordelssatsen trer i kraft. Systemet endrer automatisk fordelssatsen og oppdaterer alle fordelsplanene som er knyttet til denne satsen, så lenge du kjører behandling av oppdatering av satsendring. Du bør ikke angi denne datoen med mindre du vil at systemet automatisk skal oppdatere de ansattes fordelsplaner basert på denne satsen. Dette er vanligvis reservert til automatisk behandling av fremtidige satsendringer. **Ikrafttredelsesdatoen** for endringen må være innenfor datoen for fordelssatsen og utløpsdatoen. |
   | **Satsendring fullført** | Avmerkingsboksen for **Satsendring fullført** blir valgt automatisk etter at fordelssatsendringene er fullført av oppdateringsbehandlingen av satsendring. |

4. Hvis du vil spore og vedlikeholde endringer i fordelssatsoppsettet, velger du **Handlinger** og deretter **Vedlikehold versjoner**.

5. Velg **Lagre**. 

## <a name="set-up-tier-rates"></a>Definere lagsatser

Du kan bruke lagsatser i satsoppsettet hvis satsen varierer avhengig av ulike faktorer. Du kan for eksempel konfigurere lagsatser for å si at hvis alderen er opptil 34,99, er beløpet for ikke-røyker lik 2. Hvis alderen er opptil 39,99, er beløpet for ikke-røyker lik 3.

Du kan også bruke doble lag. Hvis du velger **Dobbelt lag** for verdien **Bruk lag** i skjemaet **Satsoppsett**, kan du definere satser basert på to dimensjoner. Du kan for eksempel konfigurere et system med dobbelt lag for å si at hvis du er en mann og alderen er opptil 34,99, er beløpet for ikke-røyker lik 2. Hvis du er mann og alderen er opptil 39,99, er beløpet for ikke-røyker lik 3. Hvis du er kvinne og alderen er opptil 34,99, er beløpet for ikke-røyker lik 1,8. Hvis du er kvinne og alderen er opptil 39,99, er beløpet for ikke-røyker lik 2,8.

> [!IMPORTANT]
> Et alternativ under **Personlige opplysninger** i arbeiderposten brukes til å angi om den ansatte er en røyker. Hvis den ansatte registreres som en røyker, brukes satsen for røyker. (Røykerindikasjonen vises aldri for den ansatte.)
   
1. I arbeidsområdet **Fordelsbehandling**, under **Oppsett**, velger du **Satser**.

2. Velg en eller flere satser fra listen, velg **Handlinger**, og velg deretter **Lagsatser**.

3. Velg **Ny**.

3. Angi verdier for de følgende feltene:

   | Felt | beskrivelse |
   | --- | --- | 
   | **Beskrivelse** | Verdien i **Beskrivelse**-feltet vil bli brukt fra beskrivelsen av prisoppsettposten. Dermed kan du identifisere hvilket satsoppsett lagsatsene er knyttet til. |
   | **Lagkode** | Velg en lagkode. Lagkoder defineres på **Lagkoder**-siden. Systemet vil automatisk vise beskrivelsen av lagkoden i rutenettet til venstre. |
   | **Lagtype** | Angir hvilket felt som skal brukes som et utvalgskriterium for beregningsprosessen for lagsatsen. For eksempel:</br></br><ul><li>Hvis **alder** brukes, vil systemet bruke den ansattes fødselsdato i beregningsprosessen for fordelssatsen.</li><li>Hvis **lønn** brukes, vil systemet bruke den ansattes årlige fordelslønn i beregningsprosessen for fordelssatsen.</li><li>Hvis **Jobbtype** brukes, vil systemet bruke den ansattes gjeldende aktive stillingspost til å bestemme jobbtypen etter jobbposten som er knyttet til stillingen.</li></ul></br></br>Lagtypene er **alder**, **lønn**, **fysisk**, **kjønn**, **fulltidsekvivalent**, **jobbtype**, **kompensasjonsområde** og **nivå**. | 
   | **Nivå** | Verdien som skal brukes med lagtypen under beregningsprosessen for fordelssatsen. For eksempel:</br></br><ul><li>Hvis lagtypen er **alder**, vil dette være aldersverdien.</li><li>Hvis lagtypen er **lønn**, vil dette være lønnsbeløpet.</li><li> Hvis lagtypen er **jobbtype**, vil dette være jobbtypen.</li></ul></br></br>Når en lagtype er av typen **alder** eller **lønn**, representerer verdien i **Nivå**-feltet øvre grense for laget. Når en lagtype er **jobbtype**, brukes en nøyaktig samsvarsmetode under valg av lagsats. |
   | **Beregningstype** | Angir hvordan beløpet i Beregningsbeløp-feltet skal brukes, og hvilken matematisk beregning som skal utføres hvis det er nødvendig. Hvis beregningstypen er et flatt beløp, brukes beløpsfeltene som de er. Hvis beregningstypen er per beløp for lønn eller dekning, brukes beregningsbeløpet og beregningsretningen i den matematiske beregningen.</br></br>Hvis beregningstypen er per lønnsbeløp, brukes følgende matematiske formel:</br></br>Årlig fordelslønn dividert med beregningsbeløp (avrundet opp eller ned) ganger beløpene for røykende eller ikke-røykende ansatt eller arbeidsgiver.</br></br>Hvis beregningstypen er per dekningsbeløp, brukes følgende matematiske formel:</br></br>Dekningsbeløp dividert med beregningsbeløp (avrundet opp eller ned) ganger beløpene for røykende eller ikke-røykende ansatt eller arbeidsgiver.</br></br>I begge beregningene brukes beregningsretningen til å avgjøre om årlig fordelslønn eller dekningsbeløp dividert på beregningsbeløp skal rundes opp eller ned. |
   | **Beregningsbeløp** | Beløpet som skal brukes under beregning av fordelssatsen. Dette beløpet vil være divisoren under den matematiske beregningen av lagsatsen. |
   | **Beregningsretning** | Retningen som skal brukes for avrunding av det beregnede resultatbeløpet. Systemet støtter tre beregningsretninger: tom (eksakt metode), **økning** og **reduksjon**.</br></br><ul><li>Hvis tom vil systemet bruke den nøyaktige beregningen av lønns-/dekningsbeløpet dividert på beregningsbeløpet. Hvis denne verdien har en brøk, vil systemet bruke denne i beregningen.</li><li>Hvis **økning** vil systemet øke den matematiske beregningen av lønns-/dekningsbeløpet dividert på beregningsbeløpet til det neste heltallet, som betyr at 12,25 vil øke til 13.</li><li>Hvis **reduksjon** vil systemet redusere den matematiske beregningen av lønns-/dekningsbeløpet dividert på beregningsbeløpet til det gjeldende heltallet, som betyr at 12,25 vil reduseres til 12.</li></ul> |
   | **Beløp for ikke-røykende ansatt** | Beløpet som en fordelsleverandør tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for ikke-røykende arbeidsgiver** | Beløpet som en fordelsleverandør tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for røykende ansatt** | Beløpet som en fordelsleverandør tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Beløp for røykende arbeidsgiver** | Beløpet som en fordelsleverandør tar betalt for en ikke-røykende ansatt. Dette er beløpet arbeidsgiveren betaler til fordelsleverandøren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Administrativt beløp** | Det administrative beløpet som belastes av en tredjeparts administrator. Dette er beløpet som arbeidsgiveren betaler til den tredjeparts administratoren, og det bør være basert på betalingsfrekvensen for satsoppsettet. |
   | **Ikke-røykersats for fleksikreditt** | Antall fleksikreditter fordelen koster, basert på beregningen som er definert for lagnivået for ikke-røykere. Hvis for eksempel beregningstypen er **per dekningsbeløp**, er beregnings beløpet 10 000, og fleksikreditten for ikke-røykende sats er 6, noe som betyr at hvis en ikke-røykende ansatt velger 10 000 i dekning, vil det koste 6 fleksikreditter. Hvis de velger 20 000 i dekning, vil det koste 12 fleksikreditter og så videre. |
   | **Røykersats for fleksikreditt** | Antall fleksikreditter fordelen koster, basert på beregningen som er definert for lagnivået for røykere. |

5. Velg **Lagre**. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
