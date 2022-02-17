---
title: Forståelse av finansutligning og årsavslutning
description: Dette emnet inneholder informasjon om forbedringer som påvirker finansutligninger og årsavslutting for økonomimodulen.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075575"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Forståelse av finansutligning og årsavslutning

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Finance versjon 10.0.25 er funksjonen **Forståelse av finansutligning og årsavslutning** tilgjengelig i arbeidsområdet **Funksjonsbehandling**. Denne funksjonen legger til to primære forbedringer som påvirker finansutligningen og årsavslutningen i økonomimodulen.

Ved årsavslutning i økonomimodulen blir ikke finanstransaksjoner som er utlignet, lenger tatt med i åpningssaldoen for det neste regnskapsåret. Denne forbedringen sikrer at bare ubetalte finanstransaksjoner blir inkludert i åpningssaldoen. Det er viktig at revaluering av utenlandsk valuta kjøres i økonomimodulen. Revaluering av utenlandsk valuta kjøres bare for finanstransaksjoner med statusen **Ikke utlignet**. Før funksjonen **Forståelse av finansutligning og årsavslutning** ble lansert, oppsummerte imidlertid åpningssaldoen både transaksjoner med statusen **Utlignet** og transaksjoner med statusen **Ikke utligninet**, og statusen for det summerte beløpet ble angitt til **Ikke utlignet**.

Den andre forbedringen lar deg postere detaljerte åpningssaldotransaksjoner ved årsavslutning i økonomimodulen. Hvis alternativet **Behold detaljer ved årsavslutning** er satt til **Ja**, opprettes det en egen åpningssaldo for hver finanstransaksjon som ikke er utlignet. Denne innstillingen er definert for hver hovedkonto i finansutligningsoppsettet. Ved å ha detaljerte transaksjoner for åpningssaldoen kan du betydelig forbedre muligheten til å utligne de ubetalte finanstransaksjonene i det neste regnskapsåret.

For å støtte de nye forbedringene ble det gjort endringer i finansutligning og årsavslutning.

### <a name="changes-to-ledger-settlement"></a>Endringer i finansutligning

- Finansutligningen må utføres innen et regnskapsår.
- Finansutligningen må utføres for transaksjoner i en enkelt hovedkonto. Hovedkontoen er nå et obligatorisk filter på siden **Utligning**.
- Finansutligning og tilbakeføring av finansutligning kan ikke utføres for transaksjoner som er postert i et avsluttet regnskapsår (med andre ord, årsavsluttingen er kjørt).

### <a name="changes-to-year-end-close"></a>Endringer i årsavslutning

- En årsavslutning kan ikke tilbakeføres hvis åpningssaldotransaksjoner er utlignet i det neste regnskapsåret. Denne endringen gjelder når en årsavslutning tilbakeføres, eller når en årsavslutning kjører på nytt og alternativet **Slett eksisterende årsavslutningsoppføringer når du avslutter året på nytt** er satt til **Ja** i parametrene for økonomimodulen.
- Hvis alternativet **Behold detaljer ved årsavslutning** er satt til **Ja** for en hvilken som helst balansekonto i finansutligning, blir det opprettet mer detaljerte åpningssaldotransaksjoner for denne hovedkontoen.

## <a name="before-you-enable-the-feature"></a>Før du aktiverer funksjonen

På grunn av endringene i funksjonalitet og datamodellen, er det viktig at du vurderer følgende punkter før du aktiverer funksjonen:

- Alle transaksjoner som er merket for utligning, men som ikke har blitt utlignet, vil automatisk få merket fjernet når funksjonen er aktivert. For å unngå tap av arbeid må du utligne alle merkede transaksjoner før du aktiverer funksjonen.
- Noen organisasjoner kjører årsavslutningen flere ganger for samme regnskapsår. Ikke aktiver funksjonen hvis årsavslutningen allerede er kjørt én gang og vil bli kjørt på nytt for det samme regnskapsåret. Funksjonen må aktiveres før du behandler den første årsavslutningen eller etter at du har behandlet den forrige årsavslutningen for regnskapsåret.

  Hvis du vil aktivere funksjonen, men årsavslutningen allerede er kjørt én gang, må du tilbakeføre årsavslutninen før du kan aktivere funksjonen.

- Fordi utligning på tvers av regnskapsår ikke lenger er tillatt, anbefaler vi at du aktiverer funksjonen før du starter årsavslutningsprosessen. For å sikre at neste regnskapsårs åpningssaldoer ikke berøres av tidligere utligninger på tvers av regnskapsår, bør deretter åpningssaldotransaksjonen utlignes for regnskapsåret som avsluttes.
- Fordi utligning på tvers av hovedkontoer ikke lenger er tillatt, kan du justere kontoplanen eller prosessene etter behov for å sikre at finansutligning kan utføres i den samme hovedkontoen.
- Funksjonen kan ikke aktiveres hvis årsavslutningsprosessen for offentlig sektor brukes.

## <a name="set-up-ledger-settlement"></a>Konfigurerer utligning i hovedbok

Når du har aktivert funksjonen, og før du kjører neste årsavslutning, må hver organisasjon fastslå om den vil beholde transaksjonsdetaljene ved årsavslutningen. Valget har ingen innvirkning på åpningssaldoposteringer fra årsavslutningsprosessene fra forrige år.

Alternativet **Behold detaljer ved årsavslutning** er angitt for hver hovedkonto på siden **Finansutligningsoppsett**.

1.  Gå til **Økonomimodul** > **Finansoppsett** > **Parametere for økonomimodul**.
2.  På fanen **Utligninger** velger du **Utligningskontoer**.

- eller -

1.  Gå til **Økonomimodul** > **Periodiske oppgaver** > **Utligninger**.
2.  Velg **Utligningskontoer**.

To kolonner er lagt til på siden **Utligninger**:
    
- **Hovedkontotype** – Denne kolonnen er bare til informasjonsformål. Den viser typen som er tilordnet til hovedkontoen.
- **Behold detaljer ved årsavslutning** – Som standard er alternativet angitt til **Nei**. Det kan bare angir til **Ja** hvis verdien i kolonnen **Hovedkontotype** er **Balanse**, **Aktiva** eller **Gjeld**. Når alternativet er angitt til **Nei**, posteres åpningssaldoer i sammendraget, slik det er vanlig ved årsavslutning. Hvis det er angitt til **Ja**, blir åpningssaldoer opprettet i detalj for hver finanstransaksjon som ikke er utlignet for hovedkontoen.

## <a name="year-end-close"></a>Årsavslutning

Når du kjører årsavslutningen ved å gå til **Økonomimodul** > **Periodeavslutnin** > **Årsavslutning**, oppretter prosessen åpningssaldoene for hovedkontoene som er definert for finansutligning. Åpningssaldoene opprettes enten i sammendrag eller detaljer, avhengig av utligningsoppsettet for finans. Prosessen utelater finanstransaksjoner som er utlignet, uansett om du posterer åpningssaldoen for hver hovedkonto i sammendrag eller detaljert.

For eksempel posteres flere transaksjoner til hovedkontoen 130100 i regnskapsåret 2021.

| Journalnummer | Bilag  | Dato       | Type      | Finanskonto | Kontonavn        | Beskrivelse       | Valuta | Beløp i transaksjonsvaluta | Beløp  | Beløp i rapporteringsvaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 03.12.2021  | I drift | 130100-001-    | Kundereskontro | Tjenestegebyr       | USD      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 05.12.2021  | I drift | 130100-002-    | Kundereskontro | Verktøy         | USD      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16.12.2021 | I drift | 130100-001-    | Kundereskontro | Refundering            | USD      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20.12.2021 | I drift | 130100-002-    | Kundereskontro |                   | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | I drift | 130100-002-    | Kundereskontro |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21.12.2021 | I drift | 130100-002-    | Kundereskontro | Kreditt på konto | USD      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28.12.2021 | I drift | 130100-001-    | Kundereskontro | Verktøy         | USD      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29.12.2021 | I drift | 130100-002-    | Kundereskontro | Tjeneste           | USD      | 300                            | 300     | 300                          |

Av disse transaksjonene utlignes tre under finansutligning.

Det er en faktura på 175 amerikanske dollar (USD 175). Denne fakturaen ble betalt i euro (EUR), og det ble gitt en kontantrabatt.

| Journalnummer | Bilag  | Dato       | Type      | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløp i transaksjonsvaluta | Beløp  | Beløp i rapporteringsvaluta |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 05.12.2021  | I drift | 130100-002-    | Kundereskontro | Verktøy   | USD      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20.12.2021 | I drift | 130100-002-    | Kundereskontro |             | USD      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | I drift | 130100-002-    | Kundereskontro |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Resultatene for hovedkontoen 130100 avhenger av om funksjonen er aktivert før årsavslutningen kjøres. Hvis funksjonen er aktivert, avhenger resultatet også av innstillingen for alternativet Behold detaljer ved årsavslutning.

### <a name="the-feature-isnt-enabled"></a>Funksjonen er ikke aktivert
Ved årsavslutningen opprettes det tre åpningssaldotransaksjoner for hovedkontoen 130100 i 2022. Summen av transaksjonene i regnskapsvalutaen er USD 525.

| Journalnummer | Bilag  | Dato     | Type    | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløp i transaksjonsvaluta | Beløp  | Beløp i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-002-    | Kundereskontro |             | USD      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-001-    | Kundereskontro |             | USD      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-002-    | Kundereskontro |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Selv om betalingens transaksjon på EUR -127,11 ble finansutlignet, videresendes transaksjonen fortsatt som en startsaldo.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funksjonen er aktivert og Behold detaljer ved årsavslutning = Nei

Ved årsavslutningen opprettes det to åpningssaldotransaksjoner for hovedkontoen 130100 i 2022. Summen av transaksjonene i regnskapsvalutaen er fremdeles USD 525, men de finansutlignede transaksjonene utelates fra åpningssaldoen. Totalbeløpet for kontoen 130100-002- er USD 125 i stedet for USD 299,12, og transaksjonen på EUR 127,11 / USD 174,12 utelates fullstendig.

| Journalnummer | Bilag  | Dato     | Type    | Finanskonto | Kontonavn        | Beskrivelse | Valuta | Beløp i transaksjonsvaluta | Beløp | Beløp i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-002-    | Kundereskontro |             | USD      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-001-    | Kundereskontro |             | USD      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funksjonen er aktivert og Behold detaljer ved årsavslutning = Ja

Ved årsavslutningen opprettes det fem åpningssaldotransaksjoner for hovedkontoen 130100 i 2022. En separat åpningssaldotransaksjon opprettes for hver av de fem transaksjonene som ikke ble utlignet. Summen av transaksjonene i regnskapsvalutaen er fortsatt USD 525.

| Journalnummer | Bilag  | Dato     | Type    | Finanskonto | Kontonavn        | Beskrivelse       | Valuta | Beløp i transaksjonsvaluta | Beløp | Beløp i rapporteringsvaluta |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-001-    | Kundereskontro | Tjenestegebyr       | USD      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-001-    | Kundereskontro | Refundering            | USD      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-002-    | Kundereskontro | Kreditt på konto | USD      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-001-    | Kundereskontro | Verktøy         | USD      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1/1/2022 | Åpning | 130100-002-    | Kundereskontro | Tjeneste           | USD      | 300                            | 300    | 300                          |

Når transaksjonsdetaljer beholdes, berøres ikke de opprinnelige detaljerte transaksjonene. De forblir postert og ikke utlignet i regnskapsåret som avsluttes. Det opprettes en kopi av disse transaksjonene for åpningssaldoen. Følgende verdier fra de opprinnelige transaksjonene kopieres til åpningssaldotransaksjonene.

- Finanskonto (hovedkontoen og alle finansdimensjoner)
- Beløp i transaksjons-, regnskap- og rapporteringsvalutaene
- Beskrivelse
- Posteringslag
- Posteringstype

   > [!NOTE]
   > Ingen andre åpningssaldotransaksjoner er tilordnet en posteringstype. Posteringstypen kan derfor brukes til å differensiere åpningstransaksjoner som er fremført i detalj.

Noen felter fra de opprinnelige transaksjonene må endres i de detaljerte transaksjonene for åpningssaldoen. Datoen for åpningssaldotransaksjoner er alltid den første dagen i det neste regnskapsåret. Journalnummeret må endres, og bilagsnummeret endres til verdien som ble angitt i dialogboksen for årsavslutning.

Du finner informasjon fra de opprinnelige transaksjonene på siden **Utligning**. Hver detaljerte åpningssaldotransaksjon viser kolonnen **Opprinnelig transaksjonsdato** i rutenettet. Denne kolonnen kan hjelpe deg med å samsvare transaksjoner i det nye regnskapsåret. Du kan velge **Vis opprinnelig bilag** for å drille tilbake til det fullstendige opprinnelige bilaget.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Utlign transaksjoner
Hvis du vil utligne finanstransaksjoner, følger du disse trinnene.

1. Gå til **Økonomimodul** > **Periodiske oppgaver** > **Utligninger**.
2.  Definer filtrene øverst på siden.

    1. Velg et datoområde. Du kan også velge en datointervallkode for å automatisk fylle ut datoområdet.

       - Datoområdet kan ikke gå over regnskapsår. Hvis datoområdet går over regnskapsår, vises ingen transaksjoner når du velger **Vis transaksjoner**.
       - Hvis datoområdet er i et åpent regnskapsår, kan transaksjoner utlignes, og utligningen kan tilbakeføres. Hvis datoområdet er i et avsluttet regnskapsår, eller hvis årsavslutningen er fullført, vises transaksjoner, men de kan ikke utlignes eller få opphevet utligningen. Du kan fjerne merket for transaksjoner bare i et avsluttet regnskapsår. Hvis datoområdet er i et avsluttet regnskapsår, er ikke knappene **Merk som valgt**, **Utligne merkede transaksjoner** og **Tilbakefør merkede transaksjoner** tilgjengelige.

    2. Velg hovedkontoen du vil vise transaksjoner for. Dette feltet er obligatorisk. Oppslaget viser bare hovedkontoene som er valgt på siden **Utligning** finans for firmaets kontoplan.
    3. Velg posteringslaget. Du kan ikke utligne transaksjoner som er i forskjellige posteringslag.
    4. Velg et finansdimensjonsett for å vise hovedkontoen og dimensjonene i separate kolonner.

3.  Velg **Vis transaksjoner** for å vise alle transaksjonene som samsvarer med filtrene du angir. Hvis du endrer noen av filtrene eller dimensjonssettene, må du velge **Vis transaksjoner** på nytt.
4.  Velg linjer for utligning. Verdien i feltet **Valgt beløp** øverst på siden økes eller reduseres for å gjenspeile det totale beløpet på de valgte linjene.
5.  Når du er ferdig med å velge transaksjoner, velger du **Merk som valgt**. For hver valgte transaksjon vises det en hake i **Merket**-kolonnen. I tillegg økes eller reduseres verdien i feltet **Merket beløp** over rutenettet for å gjenspeile det totale beløpet på de merkede linjene.
6.  Når verdien i feltet **Merket beløp** er **0** (null), velger du **Utligne merkede transaksjoner**.

    - Delvis utligning er ikke tillatt. Du kan for eksempel ikke utligne en debettransaksjon på USD 100 mot en kredittransaksjon på USD 90. Den gjenværende kredittransaksjonen på USD 10 må også merkes for inkludering i utligningen.
    - Angi en utligningsdato. Datoen må være på eller etter den siste datoen til transaksjonene som er merket for utligning.

Statusen for de merkede transaksjonene oppdateres til **Utlignet**.

> [!IMPORTANT]
> Alle transaksjoner som du har merket for utligning for den aktive juridiske enheten og den valgte hovedkontoen, blir utlignet. Transaksjonene må ikke vises på siden. De utlignes selv om de er skjult på grunn av et filter.

Noen prosesser, for eksempel tilbakeføring av en transaksjon, utligner automatisk finanstransaksjoner. En betaling og faktura utlignes for eksempel i Kunder, og utligningen genererer en realisert gevinst/tap. Utligningen av betalingen og fakturaen utligner ikke finanstransaksjoner, for eksempel transaksjoner for finanskontoen Kunde. Hvis betalingen og fakturaen ikke er avregnet i Kunder, vil imidlertid tilbakeføringsregnskapsoppføringen som ble postert under tilbakeføringen av kundeutligningen, føre til at de opprinnelige oppføringene og tilbakeføringsregnskapsoppføringene blir utlignet i økonomimodulen. Når funksjonen **Forståelse av finansutligning og årsavslutning** er aktivert, skjer ikke finansutligningen av en tilbakeføring automatisk hvis tilbakeføringsdatoen er i et annet regnskapsår.

## <a name="use-excel-for-ledger-settlement"></a>Bruke Excel til finansutligning

Transaksjoner som vises på siden **Utligning**, kan eksporteres til Excel. I Excel kan du ytterligere filtrere transaksjoner for å bestemme hvilke transaksjoner som skal merkes for utligning.
Begge finansutligningsenhetene eksporterer finanstransaksjoner bare for hovedkontoen som er valgt på siden **Utligning**. Selv om transaksjoner for lukkede regnskapsår fremdeles kan merkes eller ikke merkes ved hjelp av Excel, kan de ikke utlignes. I tillegg kan ikke utlignede transaksjoner tilbakeføres for det aktuelle regnskapsåret.

## <a name="make-transactions-easier-to-find"></a>Gjøre det enklere å finne transaksjoner

Siden **Utligninger** inkluderer funksjoner som gjør det enklere å vise transaksjoner som er nødvendige for utligning.

•   Bruk filteret **Merket** til å filtrere transaksjoner basert på om **Merket**-avmerkingsboksen for transaksjonene er merket av.
•   Bruk **Status**-filteret til å filtrere transaksjoner basert på statusen.
•   Velg **Sorter etter absolutt beløp** for å sortere beløpene etter absolutt verdi. På denne måten kan du gruppere debet- og kreditoppføringer som har samme beløp.

## <a name="reverse-a-settlement"></a>Tilbakeføre en utligning

Du kan tilbakeføre en utligning som ble gjort ved en feiltakelse.

1.  Følg trinn 1 til 3 i delen [Utligne transaksjoner](#settle-transactions) for å vise transaksjonene du er interessert i.
2.  Velg **Utlignet** i **Status**-filteret.
3.  Velg linjer for tilbakeføring.
4.  Velg **Tilbakefør merkede transaksjoner**. Statusen for alle transaksjoner som har samme utlignings-ID, oppdateres til **Ikke utlignet**.

> [!IMPORTANT]
> Alle transaksjoner som har samme utlignings-ID, blir tilbakeført, selv om de ikke er merket. Fire linjer ble for eksempel merket og utlignet. Alle de fire linjene har samme utlignings-ID. Hvis du merker én av disse fire linjene og deretter velger **Tilbakefør merkede transaksjoner**, tilbakeføres alle de fire linjene.






