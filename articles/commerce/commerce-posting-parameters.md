---
title: Commerce-posteringsparametere
description: Denne artikkelen beskriver parameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 56a2d1d2bcafdcdd9d88c132986e8ef485bf6b24
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027234"
---
# <a name="commerce-posting-parameters"></a>Commerce-posteringsparametere

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver parameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner i Microsoft Dynamics 365 Commerce. Du finner handelsposteringsparametere i Commerce headquarters under **Retail og Commerce \> Headquarters-oppsett \> Parametere \> Commerce-parametere \> Postering**.

## <a name="periodic-discount-parameters"></a>Parametere for tidsbestemt rabatt

Følgende tabell oppfører parameterne for tidsbestemt rabatt som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Poster tidsbestemt rabatt | Dette alternativet styrer om tidsbestemte tilbud posteres til finanskontoer. Tidsbestemte rabatter omfatter samlerabatter, kvantumsrabatter og rabattilbud. Når denne parameteren er aktivert, kan tilleggsfelter angis i delen **Tidsbestemte rabatter**. |
| Finanskontotype | <p>Velg typen konto som brukes til å postere tidsbestemte rabatter:</p><ul><li>**Standard** – Systemet bruker ikke rabattrelaterte felter på denne siden. I stedet brukes kontoene som er definert på siden **Postering** i Commerce headquarters (**Lagerstyring \> Oppsett \> Postering \> Posteringsskjemaer**).</li><li>**Tidsbestemt** – Systemet bruker handelsrabattkontoene som er angitt av de rabattrelaterte feltene på denne siden. Hvis du velger dette alternativet, må du angi finanskontoen for hver type tilbud (rabatt, samlerabatt, kvantumsrabatt og terskelrabatt). Du kan definere en konto når du definerer rabatten. Når posteringsfunksjonen for rabattkonto brukes på rabattoppsettsiden, opprettes det en ekstra debet- og kreditoppføring for å omklassifisere rabattposteringen fra finanskontoen for handelsrabatt til rabattfinanskontoen. Hvis du vil ha mer informasjon, kan du se [Handelsrabatter](retail-discounts-overview.md).</li></ul> |
| Poster infokoderabatt | Dette alternativet brukes ikke lenger i standard handelsløsning og blir avskrevet. |
| Poster tidsbestemt rabatt for ordrer | Dette alternativet kontrollerer om tidsbestemte rabatter for detaljhandel blir postert for kundeordre og telefonsenterordrer. |

## <a name="inventory-update-parameters"></a>Lageroppdateringsparametere

Følgende tabell oppfører lageroppdateringsparameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Bruk standard parti-ID når partinumre ikke finnes | Dette alternativet kontrollerer om standard parti-ID brukes for partiaktiverte varer hvis partinumre ikke blir funnet, og når negativ beholdning er tillatt. |
| Standard parti-ID | Partinummeret som skal brukes hvis det ikke finnes partinumre for varer, og når parameteren **Bruk av standard parti-ID når partinumre ikke finnes** er aktivert. |

## <a name="aggregation-parameters"></a>Aggregeringsparametere

Følgende tabell oppfører aggregeringsparameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Deponer til safe | Aktiver denne parameteren til å samle alle transaksjonene under utdragspostering, og opprett en enkeltlinje i journalen for postering i stedet for en egen linje for hver deponering. |
| Deponer til bank | Aktiver denne parameteren til å samle alle transaksjonene under utdragspostering, og opprett en enkeltlinje i journalen for postering i stedet for en egen linje for hver deponering. |
| Salgstransaksjoner | Aktiver denne parameteren til å konsolidere transaksjonene som en del av posteringsprosessen for transaksjonsutdraget. Vi anbefaler at du aktiverer denne parameteren. Det ble tidligere kalt **Bilagstransaksjoner**. |
| Ikke aggreger returer | Hvis dette alternativet er valgt, blir hver returtransaksjon bli postert som en egen salgsordre når et detaljhandelsutdrag posteres. |

## <a name="batch-processing-parameters"></a>Partibehandlingsparametere

Følgende tabell oppfører partibehandlingsparameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Maksimalt antall parallelle kontoutdrag | Dette feltet definerer antall partioppgaver som brukes til å postere flere utdrag. |
| Maksimal tråd for ordrebehandling per utdrag | Dette feltet viser det maksimale antallet tråder som brukes for den satsvise jobben for utdragspostering for å opprette og fakturere salgsordrer for ett enkelt utdrag. Det totale antallet tråder som utdragsposteringsprosessen bruker, beregnes ved å gange verdien til denne parameteren multiplisert med verdien i parameteren **Maksimalt antall parallell kontoutdragspostering**. Hvis du angir verdien for denne parameteren for høyt, kan det ha negativ innvirkning på ytelsen til utdragsposteringsprosessen. |
| Maksimalt antall transaksjonslinjer som er inkludert i aggregering | Dette feltet definerer antall transaksjonslinjer som skal inkluderes i en enkelt aggregert transaksjon før det opprettes en ny transaksjon. Aggregerte transaksjoner opprettes basert på forskjellige aggregeringskriterier, for eksempel kunde, forretningsdato eller finansdimensjoner. Merk deg at linjene fra en enkelt transaksjon ikke blir delt på tvers av forskjellige aggregerte transaksjoner. Derfor kan antall linjer i en aggregert transaksjon være litt høyere eller lavere, basert på faktorer som antall forskjellige produkter. |
| Maksimalt antall tråder for å validere butikktransaksjoner | Dette feltet definerer maksimalt antall tråder som brukes til å validere transaksjoner. Validering av transaksjoner er et obligatorisk trinn som må inntreffe før transaksjonene kan overføres til utdragene. Du må også definere et gavekortprodukt i hurtigfanen **Gavekort** i fanen **Postering** på siden **Parametere for Commerce**, selv om organisasjonen ikke bruker gavekort. |

Følgende tabell viser de anbefalte verdiene for parameterne i den foregående tabellen. Disse verdiene bør testes og tilpasses distribusjonskonfigurasjonen og tilgjengelig infrastruktur. Verdier som overskrider de anbefalte verdiene kan gå ut over annen satsvis behandling og bør valideres.

| Parameter | Anbefalt verdi | Detaljer |
|-----------|-------------------|---------|
| Maksimalt antall parallell kontoutdragspostering | <p>Sett denne parameteren til antallet satsvise oppgaver som er tilgjengelige for den satsvise gruppen som kjører **Utdrag**-jobben.</p><p>**Generell regel:** Multipliser antallet virtuelle AOS-servere (Application Object Server) med antallet satsvise oppgaver som er tilgjengelige per virtuelle AOS-server.</p> | Denne parameteren er ikke aktuell når funksjonen **Detaljhandelsutdrag – feedbasert** er aktivert. |
| Maksimal tråd for ordrebehandling per utdrag | Start testing av verdier fra **4**. Verdien bør vanligvis ikke overskride **8**. | Denne parameteren definerer antallet tråder som brukes til å opprette og postere salgsordrer. Den representerer antallet tråder som er tilgjengelige for postering per utdrag. |
| Maksimalt antall transaksjonslinjer som er inkludert i aggregering | Start testing av verdier fra **1000**. Mindre ordrer kan gi bedre ytelse, avhengig av konfigurasjonen av Commerce headquarters. | Denne parameteren definerer antall linjer som inkluderes i hver salgsordre under utdragspostering. Når dette nummeret nås, blir linjer delt inn i en ny ordre. Antall salgslinjer vil ikke være nøyaktig likt antallet du har angitt, fordi delingen skjer på salgsordrenivå, vil den være nær nummeret som er angitt. Likevel vil nummeret være nær nummeret som er angitt. Denne parameteren brukes til å generere salgsordrer for handelstransaksjoner som ikke har en navngitt kunde. |
| Maksimalt antall tråder for å validere butikktransaksjoner | Vi anbefaler at du angir denne parameteren til **4**, og at du bare øker den hvis du ikke oppnår akseptabel ytelse. Antallet tråder som denne prosessen bruker, kan ikke overskride antall prosessorer som er tilgjengelige for den satsvise serveren. Hvis antallet tråder er for høyt, kan annen satsvis behandling påvirkes. | Denne parameteren styrer antall transaksjoner som kan valideres samtidig for en angitt butikk. |

> [!NOTE]
> Alle innstillingene og parameterne som er knyttet til utdragsposteringer, og som er definert for butikker og på siden **Parametere for Commerce**, gjelder for den forbedrede funksjonen for utdragspostering.

## <a name="invoice-parameters"></a>Fakturaparametere

Følgende tabell oppfører fakturaparameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Journalnavn | Navnet på betalingsjournalen som brukes når det opprettes kundebetalingsjournaler for salgsordrebetalinger. Denne innstillingen gjelder alle ordrebetalinger som posteres for salgsstedet, telefonsenteret og bestillinger for netthandelskanalen. |
| Kontonavn | Navnet på betalingsbankkontoen. |
| Prioriter dimensjoner fra betalingsmåte | Når dette flagget er aktivert, prioriterer betalingsjournaler dimensjoner fra betalingsmåten i stedet for butikken. |
| Atferd for avgiftsberegning | Denne parameteren angir virkemåten når salgsordrer som opprettes under utdragspostering, faktureres:<ul><li>**Omberegn –** Beregn avgifter på nytt.</li><li> **Ikke omberegn** – Bruk avgiftsbeløpene som beregnes i salgssted.</li></ul> |
| Journalnavn | Journalnavnet som brukes når det opprettes en kundebetalingsjournal for refusjoner. Denne innstillingen gjelder alle ordrebetalinger som posteres for salgsstedet, telefonsenteret og bestillinger for netthandelskanalen. |

## <a name="statement-parameters"></a>Utdragsparametere

Følgende tabell oppfører utdragsparameterne som er spesifikke for postering av økonomiske og fysiske transaksjoner.

| Parameter | Beskrivelse |
|-----------|-------------|
| Reserver beholdning under beregning | Når denne parameteren er aktivert, reserverer utdragsberegning lager midlertidig til utdraget er postert. Denne parameteren er deaktivert som standard for å forbedre ytelsen til utdragsberegningen. Oppdatert lagerinformasjon kan beregnes ved å bruke den satsvise jobben **Poster lager**. Legg merke til at den satsvise jobben **Poster** lager ikke lenger brukes når ordeopprettelse basert på [fordelingsfeed](trickle-feed.md) på ordreoppretting for detaljhandelstransaksjoner er aktivert. |
| Deaktivering av opptelling kreves | Dette flagget deaktiverer opptellingen under postering i Commerce headquarters. |
| Omberegn finansdimensjoner ved feil | Når denne parameteren er aktivert, kan finansdimensjoner vurderes på nytt på etterfølgende utdragsposteringer hvis når utdragspostering mislykkes. |
| Bruke finansdimensjonene fra returbutikken | Når denne parameteren er aktivert, kan det opprettes koblede retursalgsordrer som bruker finansdimensjonene for butikken, i stedet for finansdimensjonene fra den opprinnelige transaksjonen. |
| Koble fra returer | Når denne parameteren er aktivert, kan setningen opprette returer av uposterte salg som blindereturer. Denne parameteren er deaktivert som standard, og vi anbefaler at du holder den deaktivert. |
| Deaktiver postering av avrundingsdifferanse | Denne parameteren deaktiverer postering av avrundingsdifferansen mellom en transaksjonsbetaling og bruttobeløpet ved behandling av betalinger. |
| Utligning av kundeinnskudd automatisk | Når denne parameteren er aktivert, utlignes kundeinnbetalinger som er postert under posterings av detaljhandelsutdrag, mot kundeåpne transaksjoner. |
| Aktiver og bruk kassastyringsavstemming fra salgssted | Når denne parameteren er aktivert, utføres avstemming av kontantstyring i salgsstedet, og verdiene sendes videre til postering av detaljhandelspostering for å opprette utdragslinjer. |
| Detaljnivå for finansbilag | Denne parameteren definerer detaljnivået som er inkludert i finansbilaget for valgte transaksjoner som stammer fra salgssted. Transaksjonstyper omfatter inntekt, utgifter og rabatter. For rabatter vurderes denne parameteren bare når kontonummeret for en tidsbestemt rabatt og kontonummeret for vanlig rabattilbud ikke er det samme. Med mindre det kreves detaljer, er **Sammendrag** den anbefalte verdien for disse posteringene. Når postering på samlenivå er definert, kan ikke **TransactionDiscountTrans.RecID** fylles ut. I Commerce-versjonen 10.0.27 ble dette flagget gitt nytt navn og ble flyttet. Det ble tidligere kalt **Detaljnivå** og var i **Lageroppdatering**-delen. |
