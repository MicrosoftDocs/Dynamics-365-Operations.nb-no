---
title: Vanlige spørsmål om årssluttaktiviteter
description: Denne artikkelen viser spørsmål som kan oppstå ved avslutning av et år, og svarene som kan hjelpe til med aktiviteter for årsavslutning.
author: moaamer
ms.date: 11/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2a75d1e3e68837a437b2369ba369b0063e015b12
ms.sourcegitcommit: 78cbb125f20a33df38bda0546203b8f837cbcd93
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/09/2022
ms.locfileid: "9751965"
---
# <a name="year-end-activities-faq"></a>Vanlige spørsmål om årssluttaktiviteter 

[!include [banner](../includes/banner.md)]

Denne artikkelen viser spørsmål som kan oppstå ved avslutning av et år, og svarene som kan hjelpe til med aktiviteter for årsavslutning. Informasjonen i denne artikkelen fokuserer først og fremst på spørsmål som gjelder lukkeaktiviteter ved årsavslutning for økonomi- og leverandørmodulen.

## <a name="general-ledger-year-end-enhancements"></a>Forbedringer ved årsavslutning for økonomimodul 
Versjon 10.0.20 innførte en forbedring av årsavslutning, som er aktivert som standard fra og med versjon 10.0.25. Hvis organisasjonen bruker en versjon som er tidligere enn 10.0.25, anbefaler vi at du aktiverer denne funksjonen før du starter årsavslutningsprosessen. Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet Funksjonsbehandling til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

 - Modul: Økonomimodul
 - Funksjonsnavn: Forbedringer ved årsavslutning for økonomimodul

Oppsettet av årsavslutningsmalene er flyttet til den nye oppsettsiden **Konfigurasjon av årsavslutningsmal**. Den eksisterende siden for årsavslutning endres på en måte som ligner på revaluering av utenlandsk valuta i økonomimodulen, der en liste vises hver gang årsavslutningen kjøres eller tilbakeføres. En regnskapsansvarlig kan starte årsavslutningen fra den nye siden. 

Hvis du vil tilbakeføre årsavslutningen, velger du det nyeste regnskapsåret for den aktuelle juridiske enheten og velger knappen **Tilbakefør årsavslutning**. Tilbakeføringen sletter regnskapsoppføringene for forrige årsavslutning og kjører ikke årsavslutningen på nytt automatisk. 

Du kan kjøre årsavslutningen på nytt ved å starte prosessen for regnskapsåret og den juridiske enheten på nytt. Prosessen fortsetter å bruke parameterinnstillingen for økonomimodulen til å finne ut om årsavslutningen skal ta hensyn til bare de nye eller endrede transaksjonene, eller om den skal fullstendig tilbakeføre den forrige avslutningen og kjøre prosessen på nytt for alle transaksjoner.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Økonomimodul: Hvordan vet jeg at vi kjører årsavslutning og ikke angrer årsavslutning?
Vi har sett at organisasjoner prøver å kjøre årsavslutningen, men i stedet utførte vi opphevet årsavslutning. Hvis årsavslutningen avsluttes ganske raskt, eller årsavslutningen ikke genererer åpningssaldoer, validerer du innstillingen **Angre forrige avslutning** i **Årsavslutning** (**Økonomimodul > Periodeslutt > Årsavslutning > Kjør årsavslutning**). 

[![Kjøring av årsavslutning i forhold til å angre årsavslutning.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Hvis valget **Angre forrige avslutning** er satt til **Ja**, blir den forrige årsavslutningen reversert. Når du kjører en angring, blir alle sluttsaldo- og åpningssaldooppføringer slettet, som om årsavslutningen aldri var blitt kjørt. Bilagene blir slettet. Årsavslutningen kjøres ikke automatisk på nytt. Du må starte prosessen på nytt, og denne gangen må du endre verdien for **Angre forrige avslutning** til **Nei**. 

> [!NOTE]
> Avslutningssaldooppføringen blir eventuelt opprettet i året som avsluttes. Dette skjer bare hvis økonomimodulparameteren **Opprett avslutningstransaksjoner under overføring** er satt til **Ja**. Startsaldooppføringen opprettes alltid, ettersom dette er startsaldoen for det neste året.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Økonomi: Hva er forskjellen mellom angring og sletting av GL-parameter for årsavslutning?
Det kan hende det er forvirring rundt forskjellen mellom parameteren **Angre forrige avslutning**, som er i dialogboksen **Årsavslutning**, og parameteren **Slett årsavslutningstransaksjoner under overføring** i økonomimodulen (**Økonomimodul > Periodeslutt > Årsavslutning > Kjør årsavslutning**).  

[![Forskjellen mellom angring og sletting av GL-parameter for årsavslutning.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Velg **Angre forrige avslutning** i rullegardinmenyen når du kjører årsavslutningsprosessen for å slette alle sluttsaldo- og åpningssaldooppføringer, som om årsavslutningen aldri var kjørt. Bilagene vil bli slettet. Årsavslutningen kjøres ikke automatisk på nytt. Hvis du vil kjøre årsavslutningen, må du starte denne prosessen på nytt, denne gangen med å endre verdien for **Angre forrige avslutning** til **Nei** (**Økonomimodul > Finansoppsett > Parametere for økonomimodul**). 

[![Innstillingen Parameter for økonomimodul.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parameteren **Slett årsavslutningstransaksjoner under overføring** i økonomimodulen brukes bare under kjøring (ikke angring) av årsavslutningen (valget **Angre forrige avslutning** er satt til **Nei**). Hvis parameteren er satt til **Ja**, slettes alle sluttsaldo- og åpningssaldooppføringer, og årsavslutningen kjøres på nytt. Denne prosessen brukes når organisasjonen vil at alle transaksjoner, inkludert justeringer siden forrige årsavslutning, skal posteres i én enkelt regnskapsoppføring for sluttsaldoen og åpningssaldooppføringer. 

Hvis du setter dette alternativet til **Nei**, blir alle sluttsaldo- og åpningssaldooppføringer stående. De blir ikke slettet. I stedet blir det opprettet en ny sluttsaldo- og åpningssaldooppføring for bare deltaet eller nye transaksjoner som er postert siden forrige års avslutning for regnskapsåret.  

> [!NOTE]
> Avslutningssaldooppføringen blir opprettet i året som avsluttes. Dette skjer bare hvis parameteren **Opprett avslutningstransaksjoner under overføring** i økonomimodulen er satt til **Ja**. Startsaldooppføringen opprettes alltid, ettersom dette er startsaldoen for det neste året. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Økonomi: Hva kan endres for å forbedre ytelsen ved årsavslutningsbehandling? 
Du kan foreta en rekke endringer for å forbedre ytelsen ved årsavslutningen. Det anbefales at du evaluerer disse foreslåtte endringene for å vurdere om endringen passer for organisasjonen din.  

### <a name="dimension-sets"></a>Dimensjonssett
Når du kjører årsavslutningen, bygges hver dimensjonssettsaldo på nytt, noe som påvirker ytelsen direkte. Noen organisasjoner oppretter dimensjonssett unødvendig fordi de ble brukt på et tidspunkt, eller kan bli brukt på et tidspunkt.  Disse unødvendige dimensjonssettene bygges fremdeles opp på nytt i løpet av årsavslutningen, noe som legger tid til prosessen. Ta deg tid til å evaluere dimensjonssettene og slette alle unødvendige dimensjonssett.

Unødvendige dimensjonssett påvirker også den satsvise jobben **BudgetDimensionFocusInitializeBalance** (**Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjonssett**).

[![Finansdimensjonssett.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfigurasjon av årsavslutningsmal
Ved hjelp av årsavslutningsmalen kan organisasjonene velge finansdimensjonsnivået som skal vedlikeholdes ved overføring av resultatsaldoer til opptjente inntekter. Innstillingene gjør at en organisasjon kan vedlikeholde de detaljerte finansdimensjonene (**Avslutt alle**) når saldoene flyttes til opptjente inntekter eller velger å summere beløpene til én dimensjonsverdi (**Avslutt én**). Dette kan defineres for hver finansdimensjon. Hvis du vil ha mer informasjon om disse innstillingene, kan du se artikkelen [Årsavslutning](year-end-close.md).

Det anbefales at du evaluerer organisasjonens krav, og lukker så mange dimensjoner som mulig ved hjelp av årsavslutningsalternativet **Avslutt én** for å forbedre ytelsen. Ved å avslutte til én dimensjonsverdi (som også kan være en tom verdi) beregner systemet mindre detaljer når det skal fastsettes saldoer for kontooppføringer for opptjent egenkapital.

## <a name="degenerate-dimensions"></a>Degenerer dimensjoner

En degenert dimensjon gir liten eller ingen mulighet til å gjenbruke den i seg selv og i kombinasjon med andre dimensjoner. Det finnes to typer degenererte dimensjoner. Den første typen er en dimensjon som degenereres individuelt. Denne typen degenerert dimensjon vises vanligvis bare på en enkelt transaksjon eller på små sett med transaksjoner. Den andre typen er en dimensjon som blir degenerert i kombinasjon med en eller flere tilleggsdimensjoner som har det samme potensialet, basert på mulige unntak som kan genereres. En degenerert dimensjon kan ha en betydelig innvirkning på ytelsen til årsavslutningsprosessen. Hvis du vil redusere ytelsesproblemer, kan du definere alle degenererte dimensjoner som **Avslutt én** i årsavslutningsoppsettet, som beskrevet i den forrige delen.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Økonomimodul: Hva gjør periodeavslutning, årsavslutning?
 
[![Periodeavslutning, årsavslutning.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Ytelsesforbedringer for å gjenoppbygge finansdimensjonssett
En ny funksjon som ble lagt til i versjon 10.0.16, forbedrer ytelsen til årsavslutnings- og konsolideringsprosessene. Funksjonen får navnet Ytelsesforbedringer for gjenoppbygging av finansdimensjonssett. Denne funksjonen endrer hvordan dimensjonssett bygges opp på nytt, slik at de bare bygges opp på nytt for et relevant tidsrom. I de tidligere versjonene ble dimensjonssettene bygget opp på nytt for alle datoer. Hvis du for eksempel avslutter 2020, vil systemet bare bygge opp saldoene på nytt for transaksjoner i regnskapsåret 2020. Hvis du kjører konsolidering for et datointervall på 1. november 2020 til 30. november 2020, bygger systemet bare opp saldoene på nytt for dette datoområdet.

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet Funksjonsbehandling til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:
 
- Modul: Økonomimodul
- Funksjonsnavn: Ytelsesforbedringer for gjenoppbygging av finansdimensjonssett

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Leverandør: Hvilke endringer er gjort for å støtte 1099-årsavslutningsrapportering for 2021?

I 2021 er skjemaene DIV, NEC og MISC endret litt og noen ekstra felter er lagt til.

#### <a name="div-new-box2e-2f"></a>DIV: nytt felt 2e, 2f
 
- Felt 2e. Viser delen av beløpet i felt 1a som er del 897 for gevinst som kan tilskrives disposisjon av interesser i amerikanske reelle eiendommer (USRPI).  
- Felt 2f. Viser delen av beløpet i felt 2a som er del 897 for gevinst som kan tilskrives disposisjon av USRPI. Legg merke til at feltene 2e og 2f bare gjelder utenlandske personer og enheter med inntekt som opprettholder sin karakter når de går gjennom eller distribueres til sine direkte eller indirekte utenlandske eiere eller mottakere. Den behandles generelt som direkte koblet til en virksomhet eller et foretak i USA. Se instruksjonene for selvangivelsen. 
 
#### <a name="nec-new-box-2"></a>NEC: nytt felt 2 
 
Hvis felt 2 er merket, rapporterer du forbruksprodukter på totalt $ 5 000 eller mer som ble solgt til deg for videresalg, på grunnlag av kjøp–salg, innbetalingsprovisjon eller et annet grunnlag. Som regel rapporterer du inntekter fra salget av disse produktene i Plan C (skjema 1040). 
 
Skjemastørrelsen til NEC er også endret. Det finnes tre skjemaer per side under utskrift. 
 
#### <a name="misc-new-box-11"></a>MISC: nytt felt 11 
 
Felt 11 viser beløpet som er betalt for kjøp av fisk for videresalg fra en hvilken som helst person som er involvert i en virksomhet eller et foretak som fanger fisk. Se instruksjonene for selvangivelsen for å rapportere denne inntekten. 
 
#### <a name="electronic-filing"></a>Elektronisk innsending 
Hvis du vil ha informasjon om elektronisk innsending, kan du se [Publikasjon for krav til elektronisk innsending](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

Oppdater formatspesifikasjoner og postoppsett for 2021-e-rapport 
- Del 2 A-post for utsteder. 
- Beløpskoder – økte lengden til 18 for feltposisjon 28–45. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Del 2 A-post for utsteder, for rapportering av betalinger på skjema 1099-DIV: 
- Beløpstype – la til del 897 Ordinært utbytte og la til beløpskode H. 
- Beløpstype – la til del 897 Kapitalgevinst og la til beløpskode J. 
 
#### <a name="sec-3-payee-b-record"></a>Del 3 B-post for betalingsmottaker 
- Generelle informasjonsposter – oppdaterte tredje punkt fra 16 til 18 felter for betalingsbeløp. 
- Felttittel for betaling H – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 247–258. 
- Felttittel for betaling J – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 259–270. 
- Oppdaterte tomt felt til feltposisjon 271–286. 
- Oppdaterte indikator for utenlandsk land til feltposisjon 287. 
- Oppdaterte linjefeltet for navn på første betalingsmottaker til feltposisjon 288–327. 
- Oppdaterte linjefeltet for navnet på andre betalingsmottaker til feltposisjon 328–367. 
- Oppsettposisjoner for post, skjema 1099-MISC – slettet feltposisjon 548 og felttittelen Kravindikator for FATCA-innsending. 
- Oppsettposisjoner for post, skjema 1099-NEC – oppdaterte 545–546 til tomt, oppdaterte feltet 547 til direktesalgsindikator, lengde, beskrivelse og merknader, oppdaterte feltet 548–722 til tomt. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Del 4 Slutt på C-post for utsteder 
- Felttittel for betaling H – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 304–321. 
- Felttittel for betaling J – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 322–339. 
- Felttittel 340–499 – oppdaterte lengden til 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Del 5 K-post for delstatstotaler 
- Felttittel for betaling H – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 304–321. 
- Felttittel for betaling J – oppdaterte felttittel, lengde og generell feltbeskrivelse for feltposisjon 322–339. 
- Felttittel 340–499 – oppdaterte lengden til 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leverandører: 1099 – Hvordan endrer jeg 1099-boksen og -verdiene for en leverandør som ikke sporer 1099-informasjon hele året?
Bruk funksjonaliteten Oppdater 1099 (**Leverandør > Leverandører >Alle leverandører > Velg en leverandør > Leverandør-fane på båndet > Update 1099**) for å gå gjennom tidligere betalte fakturatransaksjoner for å tilordne 1099-dataene på nytt på riktig måte i henhold til innstillingene i fanen **1099-avgift** på siden **Leverandør**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan jeg kjøre Update 1099 for alle leverandørene samtidig?
Nei. Update 1099-rutinen utføres mot én leverandør om gangen. Hvis dette kravet kreves av organisasjonen, kan du stemme på forslaget kalt [Partiprosess for oppdatering av leverandørens 1099-data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Leverandør: 1099 – Omberegn eksisterende 1099-beløp i forhold til Oppdater alle i verktøyet for Update 1099
Hvis du merker av for **Beregn eksisterende 1099-beløp å nytt** tilbakestilles 1099-beløpet til det totale antallet betalte verdier, når dette antallet brukes sammen med avmerkingsboksen **Oppdater alle**. 

[![1099-avgiftstransaksjoner: Før kjøring av oppdateringsrutine.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Avmerkingsboksen **Omberegn eksisterende 1099-beløp** trer bare i kraft når det er delvise 1099-verdier i fakturaen, eller hvis den ble endret i 1099-avgiftsskjemaet. La oss for eksempel anta at du har en faktura som er USD 1000,00, men brukeren skriver inn et 1099-beløp manuelt på fakturaen på USD 500,00.

[![1099-avgiftstransaksjoner: Merking av både Oppdater alle og Beregning av eksisterende 1099-beløp på nytt.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Når denne betales, vil USD 500,00 bli 1099-beløpet som betales. Hvis du utfører omberegningsrutinen, vil systemet endre 1099-beløpet til USD 1000,00, som er totalsummen som ble betalt.

[![1099-avgiftstransaksjoner: Etter at 1099-rutinen er kjørt.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leverandør: 1099 – Manuell oppretting av 1099-transaksjoner
Det kan hende at en organisasjon manuelt må opprette 1099-transaksjoner som ikke er knyttet til fakturaen. Du kan legge til manuelle 1099-transaksjoner ved å gå til **Leverandører > Periodiske oppgaver > 1099-avgift > Leverandørutligning for 1099**. Velg knappen **Manuelle 1099-transaksjoner**. 

Manuelt opprettede 1099-transaksjoner oppdateres ikke med prosessen **Oppdater alle** eller prosessen **Omberegn eksisterende 1099-beløp** i verktøyet **Update 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leverandør: 1099 – Støtter Dynamics 365 Finance 1096-skjemaet? 

Dynamics 365 Finance skriver ikke ut det årlige 1096-sammendraget og skjemaet for overføring av amerikanske informasjonsreturer.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leverandør: 1099 – Er det noen nye funksjoner som støtter 1099-rapportering for offentlig sektor? 
En ny funksjon for offentlig sektor, **Oppdater 1099-informasjon etter hovedkonto**, er lagt til, og du kan aktivere den i arbeidsområdet **Funksjonsbehandling**. Ved hjelp av denne funksjonen kan du knytte 1099-verdiene for en leverandør til hovedkontoen i regnskapsdistribusjonen, i stedet for standardkontoen i leverandørposten.

Hvis du vil ha mer informasjon, kan du se [Definere leverandører for 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
