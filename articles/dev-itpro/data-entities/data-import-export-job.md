---
title: Dataimport- og -eksportjobber
description: "Bruk arbeidsområdet Datahåndtering for å opprette og administrere dataimport- og -eksportjobber."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e79fcaa634c4b4eb601241d75da2f36f2455db4e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="data-import-and-export-jobs"></a>Dataimport- og -eksportjobber

[!include[banner](../includes/banner.md)]

For å opprette og administrere dataimport- og -eksportjobber i Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, kan du bruke arbeidsområdet **Dataadministrasjon**. Som standard oppretter dataimporterings- og eksportprosessen et oppstartstabell for hver enhet i måldatabasen. Staging-tabeller lar deg verifisere, rydde opp eller konvertere data før du flytter den.

## <a name="data-importexport-process"></a>Prosess for dataimport/-eksport
Her er fremgangsmåten for å importere eller eksportere data.

1. Opprett en import- eller eksportjobb der du fullfører følgende oppgaver:

    - Definer prosjektkategori.
    - Identifiser enhetene som skal importeres eller eksporteres.
    - Sett dataformatet for jobben.
    - Sekvenser enhetene, slik at de blir behandlet i logiske grupper og i en rekkefølge som gir mening.
    - Bestem deg for om du skal bruke staging-tabeller.

2. Bekreft at kildedataene og måldataene er tilordnet riktig.
3. Bekreft sikkerheten for import- eller eksportjobben.
4. Kjør import- eller eksportjobben.
5. Bekreft at jobben løp som forventet ved å se gjennom jobbhistorikken.
6. Rydd opp i staging-tabellene.

De gjenværende delene av dette emnet gir mer informasjon om hvert trinn i prosessen.

## <a name="create-an-import-or-export-job"></a>Opprett en import- eller eksportjobb
En import- eller eksportjobb kan kjøres én eller flere ganger.

### <a name="define-the-project-category"></a>Definer prosjektkategori
Vi anbefaler at du tar deg tid til å velge en passende prosjektkategori for import- eller eksportjobben. Prosjektkategorier kan hjelpe deg å håndtere tilknyttede jobber.

### <a name="identify-the-entities-to-import-or-export"></a>Identifiser enhetene som skal importeres eller eksporteres
Du kan legge til spesifikke enheter for en import- eller eksportjobb eller velge en mal å bruke. Maler fyller en jobb med en liste over enheter. Alternativet **Bruk mal** er tilgjengelig etter at du har gitt jobben et navn og lagret jobben.

### <a name="set-the-data-format-for-the-job"></a>Sett dataformatet for jobben
Når du velger et foretak, må du velge formatet for dataene som skal eksporteres eller importeres. Du kan definere formatet ved å bruke **Oppsett for datakilder**-flisen. Mange organisasjoner starter fra det formatet som er inkludert som standard i demo-datasettet. Her er en liste over noen av disse formatene:

- AX (for data som må importeres eller eksporteres i samme format som brukes til Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition)
- ColonSeparated
- CSV
- Excel
- Pakke

### <a name="sequence-the-entities"></a>Sekvenser enhetene
Enheter kan sekvenseres i et dataskjema, eller i import- og eksportjobber. Når du kjører en jobb som inneholder mer enn én dataenhet, må du sørge for at dataenhetene er riktig sekvensert. Du sekvenserer enhetene primært for å adressere noen funksjonelle avhengigheter mellom enheter. Hvis enheter ikke har noen funksjonelle avhengigheter, kan de planlegges for parallell import eller eksport.

#### <a name="execution-units-levels-and-sequences"></a>Utføringsenheter, nivåer og sekvenser
Utføringsenheten, nivået i kjøringsenheten og sekvensen av en enhet, hjelper til med å kontrollere rekkefølgen dataene blir eksportert eller importert i.

- Enheter i forskjellige utførelsesenheter behandles parallelt.
- I hver utførelsesenhet behandles enheter parallelt, hvis de har samme nivå.
- I hvert nivå behandles enheter i henhold til deres sekvensnummer i det nivået.
- Etter at ett nivå er behandles, behandles det neste nivået.

#### <a name="resequencing"></a>Endre sekvens
Du vil kanskje endre sekvensen for dine enheter i følgende situasjoner:

- Hvis bare én datajobb brukes for alle endringene dine, kan du bruke alternativet for å endre sekvens for å optimalisere utføringstiden for hele jobben. I disse tilfellene kan du bruke utføringsenheten til å representere modulen, nivået som representerer funksjonsområdet i modulen, og sekvensen som representerer enheten. Ved å bruke denne tilnærmingen, kan du jobbe på tvers av moduler parallelt, men du kan fortsatt jobbe i sekvens i en modul. For å sikre at parallelle operasjoner lykkes, må du vurdere alle avhengigheter.
- Hvis flere dataposter brukes (for eksempel en jobb for hver modul), kan du bruke sekvensering for å påvirke nivået og rekkefølgen av enheter for optimal utførelse.
- Hvis det ikke er noen avhengighet i det hele tatt, kan du sekvensere enheter ved forskjellige utførelsesenheter for optimal optimalisering.

Menyen **Endre sekvens** er tilgjengelig når flere enheter er valgt. Du kan endre sekvens basert på eksekveringsenhet, nivå eller sekvensalternativer. Du kan angi en økning for å endre sekvens for enhetene som er valgt. Enhets-, nivå- og/eller sekvensnummeret som er valgt for hver enhet oppdateres av angitt økning.

#### <a name="sorting"></a>Sortering
Du kan bruke alternativet **Sorter etter** for å vise enhetslisten i sekvensiell rekkefølge.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Bekreft at kildedataene og måldataene er kartlagt riktig
Tilordning er en funksjon som gjelder for både import- og eksportjobber.

- I sammenheng med en importjobb beskriver tilordning hvilke kolonner i kildefilen som blir kolonnene i staging-tabellen. Derfor kan systemet bestemme hvilke kolonnedata i kildefilen som skal kopieres inn i hvilken kolonne på staging-tabellen.
- I sammenheng med en eksportjobb beskriver tilordning hvilke kolonner av staging-tabellen (det vil si kilden) som blir kolonnene i målfilen.

Hvis kolonnene i staging-tabellen og filen matcher, etablerer systemet automatisk tilordningen, basert på navnene. Men hvis navnene er forskjellige, tilordnes ikke kolonner automatisk. I disse tilfellene må du fullføre tilordningen ved å velge **Vis tilordning**-alternativet for enheten i datajobben.

Det er to tilordningsvisninger: **Tilordningsvisualisering**, som er standard visning, og **Tilordningsdetaljer**. En rød stjerne (\*) identifiserer eventuelle obligatoriske felt i enheten. Disse feltene må tilordnes før du kan jobbe med enheten. Du kan frakoble andre felt som du trenger når du jobber med enheten. For å frakoble et felt, velg feltet i enten kolonnen **Enhet** eller kolonnen **Kilde**, og velg deretter **Slett utvalg**. Velg **Lagre** for å lagre endringene dine, og lukk deretter siden for å gå tilbake til prosjektet. Du kan bruke samme prosess for å redigere tilordning av felt fra kilde til oppstart etter at du har importert.

Du kan generere en tilordning på siden ved å velge **Generer kildetilordning**. En generert tilordning oppfører seg som en automatisk tilordning. Derfor må du manuelt tilordne alle felt som ikke er tilordnet.

![Datatilordning](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Bekreft sikkerheten for import- eller eksportjobben
Tilgang til arbeidsområdet **Databehandling** kan være begrenset, så ikke-administratorbrukere kan kun ha tilgang til spesifikke datajobber. Tilgang til et datajobb innebærer full tilgang til utførelsesloggen for den jobben og tilgang til staging-tabellene. Derfor må du sørge for at det er riktig tilgangskontroll på plass når du oppretter en datajobb.

### <a name="secure-a-job-by-roles-and-users"></a>Sikre en jobb med regler og brukere
Bruk menyen **Tilgangsroller** for å begrense jobben til en eller flere sikkerhetsroller. Kun brukere i disse rollene vil ha tilgang til jobben.

Du kan også begrense en jobb til spesifikke brukere. Når du sikrer en jobb ved brukere i stedet for med roller har du mer kontroll hvis flere brukere er tildelt en rolle.

### <a name="secure-a-job-by-legal-entity"></a>Sikre en jobb av juridisk enhet
Datajobber er globale av natur. Derfor, hvis en datajobb ble opprettet og brukt i en juridisk enhet, vil jobben bli synlig i andre juridiske enheter i systemet. Denne standardoppførelsen kan foretrekkes i enkelte applikasjonsscenarier. For eksempel kan en organisasjon som importerer fakturaer ved hjelp av dataenheter gi et sentralisert fakturabehandlingslag som har ansvaret for å håndtere fakturafeil for alle divisjoner i organisasjonen. I dette scenariet er det nyttig for det sentraliserte fakturabehandlingsteam å få tilgang til fakturaimport av jobber fra alle juridiske enheter. Derfor oppfyller standardoppførselen kravet fra et juridisk enhetsperspektiv.

En organisasjon vil imidlertid kanskje ha fakturabehandlingsteam per juridisk enhet. I dette tilfellet bør et team i en juridisk enhet kun ha tilgang til fakturaimportjobben i sin egen juridiske enhet. For å oppfylle dette kravet kan du konfigurere juridisk enhetsbasert tilgangskontroll på datajobbene ved å bruke menyen **Tilgang for juridiske enheter** i jobben. Etter at konfigurasjonen er ferdig, kan brukerne bare se jobber som er tilgjengelige i den juridiske enheten som de er logget på. For å se jobber fra en annen juridisk enhet, må brukerne bytte til den juridiske enheten.

En jobb kan sikres av roller, brukere og juridiske enheter samtidig.

## <a name="run-the-import-or-export-job"></a>Kjør import- eller eksportjobben
Du kan kjøre en jobb én gang ved å velge **Import** eller **Eksport**-knappen etter at du har definert jobben. For å sette opp gjentakende jobber, velg **Opprett gjentakende datajobb**.

## <a name="validate-that-the-job-ran-as-expected"></a>Bekreft at jobben kjørte som forventet.
Jobbhistorikken er tilgjengelig for feilsøking og etterforskning på både import- og eksportjobber. Historiske jobber er organisert av tidsintervall.

![Jobbhistorikkperioder](./media/dixf-job-history.md.png)

Hver jobbkjøring gir følgende detaljer:

- Utførelsesdetaljer
- Utførelseslogg

Utførelsesdetaljer viser status for hver dataenheter som jobben behandlet. Derfor kan du raskt finne følgende informasjon:

- Hvilke enheter ble behandlet
- Hvor mange oppføringer som ble behandlet og hvor mange som mislyktes for en enhet.
- Staging-oppføringer for hver enhet

Du kan laste ned staging-dataene i en fil for eksportjobber, eller du kan laste den ned som en pakke for import- og eksportjobber.

Fra utførelsesdetaljene kan du også åpne utførelsesloggen.

## <a name="clean-up-the-staging-tables"></a>Rydd opp i staging-tabellene
Du kan rydde opp i staging-tabellene ved å bruke **Rydd opp i staging**-funksjonen i **Databehandling**-arbeidsområdet. Du kan bruke følgende alternativer for å velge hvilke oppføringer som skal slettes fra hvilke staging-tabeller:

- **Enhet** – Kun hvis en enhet er gitt, vil alle oppføringer fra den enhetens staging-tabeller slettes. Velg dette alternativet for å rydde opp i alle data for enheten på tvers av alle dataprosjekter og alle jobber.
- **Jobb-ID** – Kun hvis en Jobb-ID er gitt, vil alle oppføringer for alle enheter i den valgte jobben slettes fra de passende staging-tabellene.
- **Dataprosjekter** – Hvis kun ett dataprosjekt er valgt, vil alle oppføringer for alle enheter på tvers av jobber for valgte dataprosjekter slettes.

Du kan også kombinere alternativene for å ytterligere begrense oppføringssettet som er slettet.

