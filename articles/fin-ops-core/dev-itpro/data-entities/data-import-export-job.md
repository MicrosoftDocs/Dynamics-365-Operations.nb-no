---
title: Oversikt over dataimport- og -eksportjobber
description: Bruk arbeidsområdet Datahåndtering for å opprette og administrere dataimport- og -eksportjobber.
author: Sunil-Garg
manager: AnnBe
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a4b5396d2bb3fbb98b3f0f8a1bf59d62f673a3d
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124618"
---
# <a name="data-import-and-export-jobs-overview"></a>Oversikt over dataimport- og -eksportjobber

[!include [banner](../includes/banner.md)]

For å opprette og administrere dataimport- og -eksportjobber bruker du arbeidsområdet **Dataadministrasjon**. Som standard oppretter dataimporterings- og eksportprosessen et oppstartstabell for hver enhet i måldatabasen. Staging-tabeller lar deg verifisere, rydde opp eller konvertere data før du flytter den.

> [!NOTE]
> Dette emnet forutsetter at du er kjent med [dataenheter](data-entities.md).

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

> [!NOTE]
> Hvis du vil oppdatere dataimport/-eksportskjemaet for å se siste fremdrift, kan du bruke ikonet for skjemaoppdatering. Oppdatering på lesernivå anbefales ikke fordi det vil forstyrre import- og eksportjobber som ikke kjøres satsvis.

## <a name="create-an-import-or-export-job"></a>Opprett en import- eller eksportjobb
En import- eller eksportjobb kan kjøres én eller flere ganger.

### <a name="define-the-project-category"></a>Definer prosjektkategori
Vi anbefaler at du tar deg tid til å velge en passende prosjektkategori for import- eller eksportjobben. Prosjektkategorier kan hjelpe deg å håndtere tilknyttede jobber.

### <a name="identify-the-entities-to-import-or-export"></a>Identifiser enhetene som skal importeres eller eksporteres
Du kan legge til spesifikke enheter for en import- eller eksportjobb eller velge en mal å bruke. Maler fyller en jobb med en liste over enheter. Alternativet **Bruk mal** er tilgjengelig etter at du har gitt jobben et navn og lagret jobben.

### <a name="set-the-data-format-for-the-job"></a>Sett dataformatet for jobben
Når du velger et foretak, må du velge formatet for dataene som skal eksporteres eller importeres. Du kan definere formatet ved å bruke **Oppsett for datakilder**-flisen. Et kildedataformat er en kombinasjon av **type**, **filformat**, **radskilletegn** og **kolonneskilletegn**. Det finnes også andre attributter, men dette er de viktigste å forstå. I tabellen nedenfor finner du en oversikt over gyldige kombinasjoner.

| Filformat            | Rad-/kolonneskilletegn                       | XML-stil                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-I/T-                     |
| XML                    | \-I/T-                                      | XML-attributt for XML-element |
| Skilletegn, fastsatt bredde | Komma, semikolon, tab, loddrett strek, kolon | \-I/T                     |

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

### <a name="truncating"></a>Avkorting
Du kan velge å avkorte poster i enheter før import for importprosjekter. Dette er nyttig hvis postene må importeres til et rent sett med tabeller. Denne innstillingen er av som standard.

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

> [!NOTE]
> En import- eller eksportjobb kan kjøres asynkront ved å velge **Import**- eller **Eksport**-knappen. Kjøring i asynkron bruker asynkront rammeverk, som er forskjellig fra det satsvise rammeverket. Men, som i det satsvise rammeverket, kan asynkront rammeverk også gjennomgå begrensning som et resultat, og jobben kjøres kanskje ikke umiddelbart. Jobbene kan også kjøres synkront ved å velge **Importer nå** eller **Eksporter nå**. Dette starter jobben umiddelbart og er nyttig hvis asynkront eller et parti ikke starter på grunn av begrensning. Jobbene kan også utføres i et parti ved å velge **Kjør satsvis**-alternativet. Satsvise ressurser er underlagt begrensning, slik at den satsvise jobben kanskje ikke starter umiddelbart. Asynkron-alternativet er nyttig når brukerne samhandler direkte med brukergrensesnittet, og ikke er privilegerte brukere for å forstå satsvis planlegging. Bruk av et parti er et annet alternativ hvis store volumer må bli importert eller eksportert. Satsvise jobber kan planlegges til å kjøre på en bestemt satsvis gruppe, som gir mer kontroll fra et perspektiv for belastningsfordeling. Hvis både asynkront og parti gjennomgår begrensning på grunn av høy ressursutnyttelse på systemet, kan det som en øyeblikkelig løsning brukes synkron versjon for import/eksport. Synkron-alternativet starter umiddelbart og blokkerer brukergrensesnittet, fordi den kjører synkront. Leservinduet må være åpent når synkron operasjon pågår.

## <a name="validate-that-the-job-ran-as-expected"></a>Bekreft at jobben kjørte som forventet.
Jobbhistorikken er tilgjengelig for feilsøking og etterforskning på både import- og eksportjobber. Historiske jobber er organisert av tidsintervall.

![Jobbhistorikkperioder](./media/dixf-job-history.md.png)

Hver jobbkjøring gir følgende detaljer:

- Utførelsesdetaljer
- Utførelseslogg

Utførelsesdetaljer viser status for hver dataenheter som jobben behandlet. Derfor kan du raskt finne følgende informasjon:

- Hvilke enheter ble behandlet.
- Hvor mange oppføringer som ble behandlet og hvor mange som mislyktes for en enhet.
- Staging-oppføringer for hver enhet.

Du kan laste ned staging-dataene i en fil for eksportjobber, eller du kan laste den ned som en pakke for import- og eksportjobber.

Fra utførelsesdetaljene kan du også åpne utførelsesloggen.

## <a name="clean-up-the-staging-tables"></a>Rydd opp i staging-tabellene
Starter i Platform-oppdatering 29, denne funksjonaliteten er avverget. Dette er erstattet av en ny versjon av jobbhistorie oppryddingsfunksjonalitet forklart nedenfor.

Du kan rydde opp i staging-tabellene ved å bruke **Rydd opp i staging**-funksjonen i **Databehandling**-arbeidsområdet. Du kan bruke følgende alternativer for å velge hvilke oppføringer som skal slettes fra hvilke staging-tabeller:

- **Enhet** – Kun hvis en enhet er gitt, vil alle oppføringer fra den enhetens staging-tabeller slettes. Velg dette alternativet for å rydde opp i alle data for enheten på tvers av alle dataprosjekter og alle jobber.
- **Jobb-ID** – Kun hvis en Jobb-ID er gitt, vil alle oppføringer for alle enheter i den valgte jobben slettes fra de passende staging-tabellene.
- **Dataprosjekter** – Hvis kun ett dataprosjekt er valgt, vil alle oppføringer for alle enheter på tvers av jobber for valgte dataprosjekter slettes.

Du kan også kombinere alternativene for å ytterligere begrense oppføringssettet som er slettet.

## <a name="job-history-clean-up-available-in-platform-update-29-and-later"></a>Opprydding i jobbhistorie (tilgjengelig i plattformoppdatering 29 og senere)

Oppryddingsfunksjonen for jobblogg i databehandling må brukes til å planlegge en periodisk opprydding av kjøringsloggen. Denne funksjonaliteten erstatter den tidligere oppryddingsfunksjonaliteten for oppsamlingstabellen, som nå er foreldet. De følgende tabellene vil bli fjernet av oppryddingsprosessen.

-   Alle oppsamlingstabeller

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   DMFSTAGINGLOG

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Funksjonaliteten må aktiveres i funksjonsbehandling, og kan deretter åpnes fra **Databehandling \> Opprydding i jobblogg**.

### <a name="scheduling-parameters"></a>Planleggingsparametere

Når du planlegger oppryddingsprosessen, må du angi følgende parametere for å definere oppryddingsskriteriene.

-   **Antall dager for å beholde loggen** – denne innstillingen brukes til å kontrollere hvor mye av kjøringsloggen som skal beholdes. Dette angis i antall dager. Når oppryddingsjobben er planlagt som en gjentakende satsvis jobb, vil denne innstillingen fungere som et kontinuerlig bevegelig vindu og dermed blir loggen for det angitte antallet dager intakt mens du sletter resten. Standardverdien er 7 dager.

-   **Antall timer for å utføre jobben** – avhengig av hvor mye av historikken som skal ryddes opp, kan den totale utførelsestiden for oppryddingsjobben variere fra noen få minutter til noen timer. Denne parameteren må settes til antall timer som jobben vil bli utført. Når oppryddingsjobben er utført for det angitte antallet timer, avsluttes jobben, og oppryddingen vil fortsette neste gang den kjøres basert på tidsplanen for regelmessighet.

    Du kan angi maksimal utførelsestid ved å angi en maksimumsgrense for antall timer jobben må kjøres med denne innstillingen. Oppryddingslogikken går gjennom én jobbutførelses-ID om gangen i en kronologisk ordnet rekkefølge, med eldste først for opprydding av relatert kjøreloggen. Den slutter å hente nye kjøre-ID-er for opprydding når den resterende kjørevarigheten er innen de siste 10 % av den spesifiserte varigheten. I noen tilfeller vil det forventes at oppryddingsjobben vil fortsette utover den angitte maksimumstiden. Dette vil i stor grad avhenge av antall poster som skal slettes for gjeldende utførelses-ID som ble startet før grensen på 10 % ble nådd. Oppryddingen som ble startet, må fullføres for å sikre dataintegritet, noe som betyr at opprydding vil fortsette til tross for overskridelse av den angitte grensen. Når dette er fullført, hentes ikke nye utførelses-ID-er, og oppryddingsjobben fullføres. Den gjenstående utførelsesloggen som ikke ble ryddet opp på grunn av mangel på nok utførelsestid, vil bli plukket opp neste gang oppryddingsjobben er planlagt. Standard- og minimumsverdien for denne innstillingen er satt til 2 timer.

-   **Gjentakende parti** – oppryddingsjobben kan kjøres som en éngangs, manuell kjøring, eller den kan også planlegges for gjentakende kjøring satsvis. Den satsvise jobben kan planlegges ved hjelp innstillingene for **kjøring i bakgrunnen**, som er standardpartiet som er satt opp.

> [!NOTE]
> Hvis poster i oppsamlingstabellene ikke ryddes opp fullstendig, kontrollerer du at oppryddingsjobben er planlagt å kjøres i regelmessighet. Som forklart ovenfor, vil jobben bare rydde opp så mange utførelses-ID-er som mulig i løpet av de angitte maksimale timene, i alle oppryddingskjøringer. Hvis du vil fortsette oppryddingen av alle gjenværende oppsamlingsposter, må jobben planlegges å kjøre med jevne mellomrom.
