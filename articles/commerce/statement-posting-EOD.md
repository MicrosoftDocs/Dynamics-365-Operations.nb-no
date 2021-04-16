---
title: Forbedringer for utdragsposteringsfunksjonalitet
description: Dette emnet beskriver forbedringene som er gjort i funksjonen for utdragspostering.
author: josaw1
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7e9f41a65ca092606e79d5aaa4e3af0ec444604f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795315"
---
# <a name="improvements-to-statement-posting-functionality"></a>Forbedringer for utdragsposteringsfunksjonalitet

[!include [banner](includes/banner.md)]

Dette emnet beskriver det første settet med forbedringer som er gjort i funksjonen for utdragspostering. Disse forbedringene er tilgjengelige i Microsoft Dynamics 365 for Finance and Operations 7.3.2.

## <a name="activation"></a>Aktivering

Som standard, under distribusjon av Finance and Operations 7.3.2, konfigureres programmet til å bruke den eldre funksjonen for utdragspostering. Hvis du vil aktivere den forbedrede utdragsposteringen, må du aktivere konfigurasjonsnøkkelen for den.

- Gå til **Systemadministrasjon** \> **Oppsett** \> **Lisenskonfigurasjon** og deretter, under **Retail og Commerce**-noden fjerner du merket for **Utdrag (eldre)** og merker av for **Utdrag**.

Når den nye konfigurasjonsnøkkelen for **Utdrag** er aktivert, er et nytt menyelement som heter **Utdrag** tilgjengelig. Med dette alternativet kan du manuelt opprette, beregne og postere utdrag. Alle utdrag som forårsaker en feil når den satsvise posteringsprosessen brukes, vil også være tilgjengelig via dette menyelementet. (Når konfigurasjonsnøkkelen for **Utdrag (eldre)** er aktivert, heter menyelementet **Åpne utdrag**.)

Commerce omfatter følgende valideringer som er knyttet til disse konfigurasjonsnøkler:

- Begge konfigurasjonsnøkler kan ikke være aktivert samtidig.
- Samme konfigurasjonsnøklene som skal brukes for alle operasjoner som utføres på en angitt setning under livssyklusen (Opprett, Beregn, Slett, Poster og så videre). For eksempel du kan ikke opprette og beregne et utdrag når **Utdrag (eldre)**-konfigurasjonsnøkkelen er aktivert, og deretter prøve å postere det samme utdraget når **Utdrag**-konfigurasjonsnøkkelen er aktivert.

> [!NOTE]
> Vi anbefaler at du bruker **Utdrag**-konfigurasjonsnøkkelen for forbedret utdragspostering, med mindre du har gode grunner til å bruke **Utdrag (eldre)**-konfigurasjonsnøkkelen i stedet for. Microsoft vil fortsette å investere i nye og forbedrede utdragspostering, og det er viktig at du bytter til den ved å dra nytte av den første anledning. Den eldre funksjonen for utdragspostering vil avvikles fra og med versjon 8.0.

## <a name="setup"></a>Oppsett

Som en del av forbedringene for funksjonen for utdragspostering har tre nye parametere blitt lagt til på hurtigfanen **Utdrag** på **Postering**-fanen på siden **Parametere for Commerce**:

- **Deaktiver tømming av kontoutdrag** – dette alternativet gjelder bare for den eldre funksjonen for utdragspostering. Vi anbefaler at du setter dette alternativet til **Ingen** for å hindre brukere fra å fjerne utdrag som befinner seg i en delvis postert tilstand. Hvis utdrag som befinner seg i en delvis postert tilstand, fjernes, vil data bli skadet. Du bør sette dette alternativet til **Ja** bare i spesielle tilfeller.
- **Reserver beholdning under beregning** – vi anbefaler at du bruker den satsvise jobben **Poster lager** for lagerreserveringen, og at du setter dette alternativet til **Nei**. Når dette alternativet er satt til **Nei**, forbedret setningen postering funksjonen ikke prøver å opprette lager Reservasjonsposter ved beregning (Hvis oppføringene ikke allerede har opprettet ved hjelp av **Poster lager** satsvis jobb). Oppretter i stedet funksjonen lager Reservasjonsposter bare ved postering. Denne implementeringen er et valg for utforming og er basert på det faktum at tidsvinduet mellom beregningsprosessen og posteringsprosessen er vanligvis liten. Men hvis du vil reservere lager på tidspunktet for beregningen, kan du angi dette alternativet **Ja**.

    Funksjonen eldre setningen postering reserverer alltid lager i løpet av beregningsprosessen setning (hvis reserveringen ikke ble allerede har gjort ved hjelp av **poster lager** satsvis jobb), uavhengig av innstillingen for dette alternativet.

- **Deaktivering av opptelling kreves** – når dette alternativet er satt til **Ja**, fortsetter posteringsprosessen for et utdrag, selv om forskjellen mellom det talte beløpet og transaksjonsbeløpet på utdraget er utenfor terskelen som er definert i den **Utdrag** hurtigfane for butikker.

I tillegg er følgende parametere introdusert i hurtigfanen **Satsvis behandling** i kategorien **Postering** på siden **Parametere for Commerce**: 

- **Maksimalt antall parallell kontoutdragspostering** – Dette feltet definerer antall satsvise oppgaver som skal brukes til å postere flere utdrag. 
- **Maks. tråd for ordrebehandling per utdrag** – Dette feltet viser det maksimale antallet tråder som brukes av den satsvise jobben for utdragspostering for å opprette og fakturere salgsordrer for ett enkelt utdrag. Det totale antallet tråder som vil bli brukt av utdragsposteringsprosessen, beregnes basert på verdien i denne parameteren multiplisert med verdien i parameteren **Maksimalt antall parallell kontoutdragspostering**. Hvis du angir verdien for denne parameteren for høyt, kan det ha negativ innvirkning på ytelsen til utdragsposteringsprosessen.
- **Maks. transaksjonslinjer inkludert i aggregering** – Dette feltet definerer antall transaksjonslinjer som skal inkluderes i en enkelt aggregert transaksjon før det opprettes en ny. Aggregerte transaksjoner opprettes basert på forskjellige aggregeringskriterier, for eksempel kunde, forretningsdato eller finansdimensjoner. Det er viktig å merke seg at linjene fra en enkelt transaksjon ikke vil bli delt på tvers av forskjellige aggregerte transaksjoner. Dette betyr at det er en mulighet for at antall linjer i en aggregert transaksjon er litt høyere eller lavere, basert på faktorer som antall forskjellige produkter.
- **Maksimalt antall tråder for å validere butikktransaksjoner** – Dette feltet definerer antall tråder som skal brukes til å validere transaksjoner. Validering av transaksjoner er et obligatorisk trinn som må inntreffe før transaksjonene kan overføres til utdragene. Du må også definere et **Gavekortprodukt** i hurtigfanen **Gavekort** i kategorien **Postering** på siden **Parametere for Commerce**. Dette må defineres selv om gavekort ikke brukes av organisasjonen.

> [!NOTE]
> Alle innstillingene og parameterne som er knyttet til utdragsposteringer, og som er definert for butikker og på siden **Parametere for Commerce**, gjelder for den forbedrede funksjonen for utdragspostering.

## <a name="processing"></a>Behandling

Utdrag kan beregnes og posteres satsvis ved hjelp av menyelementene **Beregn utdrag satsvis** og **Poster utdrag satsvis**. Eventuelt utdrag kan manuelt beregnes og posteres ved hjelp av **Utdrag**, som er tilgjengelig via den forbedrede funksjonen for utdragspostering.

Prosessen og fremgangsmåten for beregning og postering av utdrag satsvis er de samme som de var i den eldre funksjonen for utdragspostering. Imidlertid er betydelige forbedringer gjort i kjernebakgrunnsbehandlingen av utdragene. Disse forbedringene gjør prosessen mer fleksibel og gir bedre oversikt over tilstander og feilinformasjon. Brukere kan derfor løse den opprinnelige årsaken til feil og deretter fortsette posteringsprosessen uten å forårsake datafeil og uten at det er nødvendig med datareparasjoner.

Delene nedenfor beskriver noen av de store forbedringene for utdragspostering som vises i brukergrensesnittet for utdrag og posterte utdrag.

### <a name="status-details"></a>Statusdetaljer

En ny statusmodell er introdusert i utdragsposteringsrutinen over beregnings- og posteringsprosessene.

Tabellen nedenfor beskriver de forskjellige statusene og rekkefølgen deres i løpet av beregningsprosessen.

| Tilstandsrekkefølge | Delstat      | beskrivelse |
|-------------|------------|-------------|
| 1           | Startet    | Utdraget ble opprettet og er klar til å bli beregnet. |
| 2           | Merket     | Transaksjonene som er i området for utdraget, identifiseres basert på utdragsparameterne, og de er merket med utdrags-ID-en. |
| 3           | Beregnet | Utdragslinjene er beregnet og vist. |

Tabellen nedenfor beskriver de forskjellige statusene og rekkefølgen deres i løpet av posteringsprosessen.

| Tilstandsrekkefølge | Delstat                   | beskrivelse |
|-------------|-------------------------|-------------|
| 1           | Kontrollert                 | Det gjøres flere valideringer som er knyttet til parametere (for eksempel disposisjonstillegget), og til utdrag og utdragslinjer (for eksempel differansen mellom det talte beløpet og transaksjonsbeløpet). |
| 2           | Aggregert              | Salgstransaksjoner for kunder med og uten navn samles basert på konfigurasjonen. Hver aggregerte transaksjon blir til slutt konvertert til en salgsordre. |
| 3           | Kundeordre opprettet  | Basert på den samlede transaksjonen, opprettes salgsordrer i systemet. |
| 4           | Kundeordre fakturert | Salgsordrer faktureres. |
| 5           | Posterte rabatter        | Periodiske rabattjournaler posteres basert på konfigurasjonen. |
| 6           | Postert inntekt/utgift   | Inntekts-/ utgiftstransaksjoner posteres som bilag. |
| 7           | Tilknyttede bilag         | Betalingsjournaler opprettes og kobles til den tilsvarende fakturaen. |
| 8           | Posterte betalinger         | Betalingsjournaler posteres. |
| 9           | Posterte gavekort       | Gavekorttransaksjoner posteres som bilag. |
| 10          | Postert                  | Utdraget er merket som bokført. |

Hver tilstand i tabellene ovenfor er uavhengig av natur, og en hierarkisk avhengighet bygges mellom statusene. Denne avhengigheten flyter fra topp til bunn. Hvis det oppstår feil i systemet mens det behandler en tilstand, er statusen for utdraget tilbake til den opprinnelige tilstanden. Eventuelle etterfølgende nye forsøk for prosessen går ut av hvilken tilstand som mislyktes, og fortsetter å gå fremover. Denne metoden har følgende fordeler:

- Brukeren har fullstendig synlighet i tilstanden der feilen inntraff.
- Ødelagte data unngås. I den eldre funksjonen for utdragspostering fantes det for eksempel forekomster der noen salgsordrer ble fakturert, men andre ble værende åpne. Det fantes også forekomster der noen betalingsjournaler ikke hadde en tilsvarende faktura å utligne, fordi det oppstod en feil i fakturaposteringen.
- Brukere kan se gjeldende tilstand for et utdrag ved hjelp av **Statusdetaljer**-knappen i gruppen **Utførelsesdetaljer** av utdraget. Statusdetaljersiden består av tre deler:

    - Den første delen viser gjeldende status for utdraget, sammen med feilkoden og en detaljert feilmelding hvis det oppstod en feil.
    - Den andre delen viser de forskjellige tilstandene i beregningsprosessen. Visuelle indikatorer viser tilstandene som er kjørt, tilstander som ikke kan kjøre på grunn av feil, og tilstander som ennå ikke har kjørt.
    - Den tredje delen viser de forskjellige tilstandene i posteringsprosessen. Visuelle indikatorer viser tilstandene som er kjørt, tilstander som ikke kan kjøre på grunn av feil, og tilstander som ennå ikke har kjørt.

Hodet i den andre og tredje delen viser også den overordnede statusen for den aktuelle prosessen.

### <a name="event-logs"></a>Hendelseslogger

Et utdrag går gjennom ulike operasjoner (for eksempel, Opprett, Beregn, Slett og Poster), og flere forekomster av den samme operasjonen kan kalles under livssyklusen for utdraget. Når et utdrag opprettes og beregnes, kan en bruker for eksempel fjerne utdraget og beregne det på nytt. **Hendelseslogger**-knappen i gruppen **Utførelsesdetaljer** av utdraget gir en fullstendig revisjonssporing for de ulike operasjonene som ble kalt på et utdrag, sammen med informasjon om når disse operasjonene ble kalt.

### <a name="aggregated-transactions"></a>Aggregerte transaksjoner

Under posteringsprosessen samles salgstransaksjonene basert på konfigurasjonen. Disse samlede transaksjonene lagres i systemet og brukes til å opprette salgsordrer. Hver samlet transaksjon oppretter én tilsvarende salgsordre i systemet. Du kan vise de samlede transaksjonene ved hjelp av **Aggregerte transaksjoner**-knappen i gruppen **Utførelsesdetaljer** av utdraget.

Kategorien **Salgsordredetaljer** for en aggregert transaksjon viser følgende informasjon:

- **Post-ID** – ID-en for den aggregerte transaksjonen.
- **Utdragsnummer** – utdraget som den aggregerte transaksjonen tilhører.
- **Dato** – datoen da den aggregerte transaksjonen ble opprettet.
- **Salgs-ID** – når en ordre opprettes fra den samlede transaksjonen, er dette ID-en for salgsordren. Hvis dette feltet er tomt, er den tilsvarende salgsordren ikke opprettet.
- **Antall aggregerte linjer** – totalt antall linjer for den aggregerte transaksjonen og salgsordren.
- **Statusr** – forrige status for den aggregerte transaksjonen.
- **Faktura-ID** – når salgsordren for den aggregerte transaksjonen er fakturert, er dette ID-en for salgsfakturaen. Hvis dette feltet er tomt, er fakturaen for salgsordren ikke postert.

Kategorien **Transaksjonsdetaljer** for en aggregert transaksjon viser alle transaksjoner som har blitt hentet til den aggregerte transaksjonen. De aggregerte linjene på den aggregerte transaksjonen viser alle de aggregerte postene fra transaksjoner. De aggregerte linjene viser også detaljer, for eksempel vare, variant, antall, pris, nettobeløp, enhet og lager. I utgangspunktet tilsvarer hver aggregerte linje én salgsordrelinje.

Fra siden **Aggregerte transaksjoner** kan du laste ned XML for en bestemt aggregert transaksjon ved hjelp av knappen **Eksporter XML for salgsordre**. Du kan bruke XML-filen til å feilsøke problemer som involverer oppretting av salgsordre og postering. Bare last ned XML-filen, last den opp til et testmiljø og feilsøk problemet i testmiljøet. Funksjonen for å laste ned XML for aggregerte transaksjoner er ikke tilgjengelig for utdrag som er postert.

Visningen av aggregerte transaksjoner gir følgende fordeler:

- Brukeren har oversikt over de aggregerte transaksjonene som mislyktes under oppretting av salgsordren, og salgsordrene som mislyktes under fakturering.
- Brukeren har oversikt over hvordan transaksjoner aggregeres.
- Brukeren har en fullstendig revisjonssporing, fra transaksjoner, til salgsordrer til salgsfakturaer. Denne revisjonssporingen var ikke tilgjengelige i den eldre funksjonen for utdragspostering.
- Den aggregerte XML-filen gjør det enklere å identifisere problemer under oppretting av salgsordre og fakturering.

### <a name="journal-vouchers"></a>Journalbilag

**Journalbilag**-knappen i gruppen **Utførelsesdetaljer** i utdraget viser alle de ulike bilagstransaksjonene som er opprettet for et utdrag, og som er knyttet til rabatter, inntekts-/ utgiftskontoer, gavekort og så videre.

For øyeblikket vises disse dataene bare for posterte utdrag.

### <a name="payment-journals"></a>Betalingsjournaler

**Betalingsjournaler**-knappen i gruppen **Utførelsesdetaljer** i utdraget viser alle de ulike betalingsjournalene som er opprettet for et utdrag.

For øyeblikket vises disse dataene bare for posterte utdrag.

## <a name="other-improvements"></a>Andre forbedringer

Andre forbedringer i bakgrunnen som brukerne kan se er gjort i funksjonen for utdragspostering. Her er noen eksempler:

- Aggregeringen vurderer ikke ansatte, terminal, og skiftenheter. Fordi det er færre aggregeringsparametere, må færre salgsordrelinjer behandles.
- Forekomsten av vranglås i transaksjonstabeller reduseres ved å introdusere flere utvidelsestabeller og ved å gjøre innsettingsoperasjoner i stedet for oppdateringsoperasjoner i transaksjonstabellene.
- Antallet kjørende satsvise oppgaver er parametriserte og begrenset. Dette antallet kan derfor være spesielt innstilt for kundens miljø. I den eldre funksjonen for utdragspostering ble det opprettet et ubegrenset antall satsvise oppgaver samtidig. Resultatet var uhåndterlige belastninger, administrasjon og flaskehalser på den satsvise serveren.
- Utdragene er effektivt lagt i kø for behandling ved å prioritere utdragene som har det maksimale antallet transaksjoner.
- Satsvise prosesser som **Beregn utdrag satsvis** og **Poster utdrag satsvis** kjøres bare i satsvis modus. I den eldre funksjonen for postering av utdrag kunne brukerne velge å kjøre disse satsvise prosessene i en interaktiv modus, som er en enkelttrådet operasjon, i motsetning til satsvise prosesser, som er flertrådige.
- I den eldre funksjonen for utdragspostering ville eventuelle feil i en satsvis oppgave sette hele jobben i feiltilstand. I den forbedrede funksjonen setter ikke mislykkede satsvise oppgaver hele den satsvise jobben i feiltilstand hvis andre satsvise oppgaver er vellykket fullført. Du bør undersøke posteringsstatusen for en satsvis utføring som er kjørt ved hjelp av siden **Utdrag**, der du kan se alle utdrag som ikke er postert på grunn av feil.
- I den eldre funksjonen for utdragspostering-får den første forekomsten av en utdragsfeil hele den satsvise jobben til å mislykkes. De gjenværende utdragene blir ikke behandlet. I den forbedrede funksjonen fortsetter den satsvise prosessen å behandle alle utdrag, selv om noen av utdragene mislykkes. Én fordel er at brukernefår innsikt i det nøyaktige antallet utdrag som inneholder feil. Brukerne trenger derfor ikke bli låst fast i en kontinuerlig løkke for å rette feilene og kjøre prosessen for postering av utdrag til alle utdrag er postert.

## <a name="general-guidance-about-the-statement-posting-process"></a>Generell informasjon om utdragsposteringsprosessen

- Vi anbefaler at du kjører utdragsposteringsprosessen satsvist, fordi satsvise kjøringer utnytter kraften i det satsvise rammeverket i form av flertrådskjøring. Flertråding kreves for å håndtere store mengder transaksjoner som vanligvis vises i utdragsposteringer.
- Vi anbefaler at du aktiverer fysisk negativt lager i varemodellgruppen, slik at du har erfaring med en sømløs postering. I enkelte tilfeller kan kanskje ikke negative utdrag posteres, hvis det ikke finnes et fysisk negativt lager. Hvis det for eksempel i teorien bare finnes én enhet av en vare på lager, og det har vært en salgstransaksjon og en returtransaksjon for varen, skal transaksjonen kunne posteres, selv om lagerbeholdningen ikke er aktivert. Siden utdragsposteringsprosessen henter både salgstransaksjonen og returner transaksjonen i en enkelt kundeordre, er det ingen garanti for at salgslinjen posteres først, etterfulgt av returlinjen. Derfor kan det oppstå feil. Hvis negativ beholdning er aktivert i denne situasjonen, transaksjonsposteringen påvirkes ikke negativt og systemet viser riktig beholdning.
- Vi anbefaler at du bruker aggregering mens du beregner og posterer utdrag. Derfor anbefales følgende innstillinger for noen av aggregeringsparameterne:

    - Gå til **Retail og Commerce** \> **Hovedkvarteroppsett** \> **Parametere** \> **Parametere for Commerce**. Deretter, på **Postering**-fanen på hurtigfanen **Lageroppdatering** i feltet **Detaljnivå**, velger du **Sammendrag**.
    - Gå til **Retail og Commerce** \> **Hovedkvarteroppsett** \> **Parametere** \> **Parametere for Commerce**. Deretter, på **Postering**-fanen på hurtigfanen **Aggregering**, angir du **Bilagstransaksjoner** til **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]