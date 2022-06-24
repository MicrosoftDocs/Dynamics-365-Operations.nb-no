---
title: Forbedringer for utdragsposteringsfunksjonalitet
description: Denne artikkelen beskriver forbedringene som er gjort i funksjonen for utdragspostering.
author: analpert
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: a7f25a7cc1e214b5c08013055126728b2ad10f3f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886912"
---
# <a name="improvements-to-statement-posting-functionality"></a>Forbedringer for utdragsposteringsfunksjonalitet

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver det første settet med forbedringer som er gjort i funksjonen for utdragspostering. Disse forbedringene er tilgjengelige i Microsoft Dynamics 365 for Finance and Operations 7.3.2.

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

> [!NOTE]
> Fra og med utgivelsen av Commerce versjon 10.0.14, når funksjonen **Detaljhandelsutdrag – feedbasert** er aktivert, er den satvise jobben **Poster beholdning** ikke lenger aktuell og kan ikke kjøres.

## <a name="processing"></a>Behandles

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

I løpet av posteringsprosessen samles hentesalgstransaksjoner etter kunde og produkt. Derfor reduseres antall salgsordrer og linjer som opprettes. De samlede transaksjonene lagres i systemet og brukes til å opprette salgsordrer. Hver samlet transaksjon oppretter én tilsvarende salgsordre i systemet. 

Hvis et utdrag ikke er postert fullt ut, kan du vise oppsamlete transaksjoner i utdraget. Velg **Aggregerte transaksjoner** i gruppen **Utførelsesdetaljer** i fanen **Utdrag** i handlingsruten.

![Akkumulerte transaksjoner-knappen for et utdrag som ikke er postert helt.](media/aggregated-transactions.png)

For posterte utdrag kan du vise aggregerte transaksjoner på siden **Posterte utdrag**. I handlingsruten velger du **Forespørsler** og deretter **Aggregerte transaksjoner**.

![Aggregerte transaksjoner-kommando for posterte utdrag.](media/aggregated-transactions-posted-statements.png)

Hurtigfanen **Salgsordredetaljer** for en aggregert transaksjon viser følgende informasjon:

- **Post-ID** – ID-en for den aggregerte transaksjonen.
- **Utdragsnummer** – utdraget som den aggregerte transaksjonen tilhører.
- **Dato** – datoen da den aggregerte transaksjonen ble opprettet.
- **Salgs-ID** – når en ordre opprettes fra den samlede transaksjonen, er dette ID-en for salgsordren. Hvis dette feltet er tomt, er den tilsvarende salgsordren ikke opprettet.
- **Antall aggregerte linjer** – totalt antall linjer for den aggregerte transaksjonen og salgsordren.
- **Statusr** – forrige status for den aggregerte transaksjonen.
- **Faktura-ID** – når salgsordren for den aggregerte transaksjonen er fakturert, er dette ID-en for salgsfakturaen. Hvis dette feltet er tomt, er fakturaen for salgsordren ikke postert.
- **Feilkode** – Dette feltet er angitt hvis aggregeringen har en feilstatus.
- **Feilmelding** – Dette feltet er angitt hvis aggregeringen har en feilstatus. Den viser detaljer om hva som forårsaket at prosessen mislyktes. Du kan bruke informasjonen i feilkoden til å løse problemet, og deretter starte prosessen på nytt manuelt. Alt etter løsningstypen kan det hende at akkumulert salg må slettes og behandles på et nytt utdrag.

![Felt i hurtigfanen Salgsordredetaljer for en akkumulert transaksjon.](media/aggregated-transactions-error-message-view.png)

Hurtigfanen **Transaksjonsdetaljer** for en aggregert transaksjon viser alle transaksjoner som har blitt hentet til den aggregerte transaksjonen. De aggregerte linjene på den aggregerte transaksjonen viser alle de aggregerte postene fra transaksjoner. De aggregerte linjene viser også detaljer, for eksempel vare, variant, antall, pris, nettobeløp, enhet og lager. I utgangspunktet tilsvarer hver aggregerte linje én salgsordrelinje.

![Hurtigfanen Transaksjonsdetaljer for en akkumulert transaksjon.](media/aggregated-transactions-sales-details.png)

I noen situasjoner kan aggregerte transaksjoner ikke postere den konsoliderte salgsordren. I disse situasjonene vil en feilkode bli knyttet til utdragsstatusen. Hvis du bare vil vise aggregerte transaksjoner som har feil, kan du aktivere filteret **Vis bare feil** i visningen for aggregerte transaksjoner ved å merke av for boksen. Ved å aktivere dette filteret begrenser du resultatene til aggregerte transaksjoner som har feil som krever løsning. Hvis du vil ha informasjon om hvordan du løser disse feilene, kan du se [Redigere og overvåke nettordretransaksjoner og asynkrone kundeordretransaksjoner](edit-order-trans.md).

![Merk av for filteret Vis bare feil i visningen for akkumulerte transaksjoner.](media/aggregated-transactions-failure-view.png)

På siden **Aggregerte transaksjoner** kan du laste ned XML for en bestemt aggregert transaksjon ved å velge **Eksporter aggregerte data**. Du kan se gjennom XMLen i et hvilket som helst XML-format for å se de faktiske dataene som omfatter oppretting og postering av salgsordrer. Funksjonen for å laste ned XML for aggregerte transaksjoner er ikke tilgjengelig for utdrag som er postert.

![Eksporter aggregerte data-knappen på siden Aggregerte transaksjoner.](media/aggregated-transactions-export.png)

Hvis du ikke kan reparere feilen ved å rette data i salgsordren eller dataene som støtter salgsordren, er knappen **Slett kundeordre** tilgjengelig. Hvis du vil slette en ordre, velger du den oppsamlede transaksjonen som mislyktes, og deretter velger du **Slett kundeordre**. Både dem aggregerte transaksjonen og den tilsvarende salgsordren slettes. Nå kan du se gjennom transaksjonene ved hjelp av redigerings- og revisjonsfunksjonen. Et alternativ er å behandling på nytt via et nytt utdrag. Når alle feil er løst, kan du fortsette utdragsposteringen ved å kjøre funksjonen for postering av utdrag for det relevante utdraget.

![Slett kundeordre-knappen i den akkumulerte transaksjonsvisningen.](media/aggregated-transactions-delete-cust-order.png)

Visningen av aggregerte transaksjoner gir følgende fordeler:

- Brukeren har oversikt over de aggregerte transaksjonene som mislyktes under oppretting av salgsordren, og salgsordrene som mislyktes under fakturering.
- Brukeren har oversikt over hvordan transaksjoner aggregeres.
- Brukeren har en fullstendig revisjonssporing, fra transaksjoner, til salgsordrer til salgsfakturaer. Denne revisjonssporingen var ikke tilgjengelige i den eldre funksjonen for utdragspostering.
- Den aggregerte XML-filen gjør det enklere å identifisere problemer under oppretting av salgsordre og fakturering.

> [!NOTE]
> Når transaksjonene samles opp, er ikke stabsmedlemmet som er tilordnet transaksjonen, lenger tilgjengelig for **Rapport om salg etter beste stab**, som betyr at **Rapport om salg etter beste stab** ikke vil vise alle transaksjonene. Vi anbefaler at du ikke bruker **Rapport om salg etter beste stab** akkumulerte transaksjoner.

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
