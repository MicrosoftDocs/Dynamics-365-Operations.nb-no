---
title: Vanlige spørsmål om årssluttaktiviteter
description: Dette emnet er kompilert for å bidra med aktiviteter for årsavslutning.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a9feafcab5969e9ec8fcbb8a6903d7b59505f6ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249417"
---
# <a name="year-end-activities-faq"></a>Vanlige spørsmål om årssluttaktiviteter 

Dette emnet er kompilert for å bidra med aktiviteter for årsavslutning. Informasjonen i dette emnet fokuserer først og fremst på spørsmål som gjelder lukkeaktiviteter ved årsavslutning for økonomi- og leverandørmodulen.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Økonomi: Hvordan vet jeg at vi kjører årsavslutning og ikke angrer årsavslutning?
Vi har sett at organisasjoner prøver å kjøre årsavslutningen, men i stedet utførte vi opphevet årsavslutning. Hvis årsavslutningen avsluttes ganske raskt, eller årsavslutningen ikke genererer åpningssaldoer, validerer du innstillingen **Angre forrige avslutning** i **Årsavslutning** (**Økonomi > Periodeslutt > Årsavslutning > Kjør årsavslutning**). 

[![Kjøre årsavslutning i forhold til å angre årsavslutning](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Hvis valget **Angre forrige avslutning** er satt til **Ja**, blir den forrige årsavslutningen reversert. Når du kjører en angring, blir alle sluttsaldo- og åpningssaldooppføringer slettet, som om årsavslutningen aldri var blitt kjørt. Bilagene blir slettet. Årsavslutningen kjøres ikke automatisk på nytt. Du må starte prosessen på nytt, og denne gangen må du endre verdien for **Angre forrige avslutning** til **Nei**. 

> [!NOTE]
> Avslutningssaldooppføringen blir eventuelt opprettet i året som avsluttes. Dette skjer bare hvis økonomimodulparameteren **Opprett avslutningstransaksjoner under overføring** er satt til **Ja**. Startsaldooppføringen opprettes alltid, ettersom dette er startsaldoen for det neste året.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Økonomi: Hva er forskjellen mellom angring og sletting av GL-parameter for årsavslutning?
Det kan hende det er forvirring rundt forskjellen mellom parameteren **Angre forrige avslutning**, som er i dialogboksen **Årsavslutning**, og parameteren **Slett årsavslutningstransaksjoner under overføring** i økonomimodulen (**Økonomimodul > Periodeslutt > Årsavslutning > Kjør årsavslutning**).  

[![Forskjellen mellom angring og sletting av GL-parameter for årsavslutning](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Velg **Angre forrige avslutning** i rullegardinmenyen når du kjører årsavslutningsprosessen for å slette alle sluttsaldo- og åpningssaldooppføringer, som om årsavslutningen aldri var kjørt. Bilagene vil bli slettet. Årsavslutningen kjøres ikke automatisk på nytt. Hvis du vil kjøre årsavslutningen, må du starte denne prosessen på nytt, denne gangen med å endre verdien for **Angre forrige avslutning** til **Nei** (**Økonomimodul > Finansoppsett > Parametere for økonomimodul**). 

[![Innstillingen Parameter for økonomimodul](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Parameteren **Slett årsavslutningstransaksjoner under overføring** i økonomimodulen brukes bare under kjøring (ikke angring) av årsavslutningen (valget **Angre forrige avslutning** er satt til **Nei**). Hvis parameteren er satt til **Ja**, slettes alle sluttsaldo- og åpningssaldooppføringer, og årsavslutningen kjøres på nytt. Denne prosessen brukes når organisasjonen vil at alle transaksjoner, inkludert justeringer siden forrige årsavslutning, skal posteres i én enkelt regnskapsoppføring for sluttsaldoen og åpningssaldooppføringer. 

Hvis du setter dette alternativet til **Nei**, blir alle sluttsaldo- og åpningssaldooppføringer stående. De blir ikke slettet. I stedet blir det opprettet en ny sluttsaldo- og åpningssaldooppføring for bare deltaet eller nye transaksjoner som er postert siden forrige års avslutning for regnskapsåret.  

> [!NOTE]
> Avslutningssaldooppføringen blir opprettet i året som avsluttes. Dette skjer bare hvis parameteren **Opprett avslutningstransaksjoner under overføring** i økonomimodulen er satt til **Ja**. Startsaldooppføringen opprettes alltid, ettersom dette er startsaldoen for det neste året. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Økonomi: Hva kan endres for å forbedre ytelsen ved årsavslutningsbehandling? 
Du kan foreta en rekke endringer for å forbedre ytelsen ved årsavslutningen. Det anbefales at du evaluerer disse foreslåtte endringene for å vurdere om endringen passer for organisasjonen din.  

### <a name="dimension-sets"></a>Dimensjonssett
Når du kjører årsavslutningen, bygges hver dimensjonssettsaldo på nytt, noe som påvirker ytelsen direkte. Noen organisasjoner oppretter dimensjonssett unødvendig fordi de ble brukt på et tidspunkt, eller kan bli brukt på et tidspunkt.  Disse unødvendige dimensjonssettene bygges fremdeles opp på nytt i løpet av årsavslutningen, noe som legger tid til prosessen. Ta deg tid til å evaluere dimensjonssettene og slette alle unødvendige dimensjonssett.

Unødvendige dimensjonssett påvirker også den satsvise jobben **BudgetDimensionFocusOppgavetializeBalance** (**Økonomimodul > Kontoplan > Dimensjoner > Finansdimensjonssett**).

[![Finansdimensjonssett](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfigurasjon av årsavslutningsmal
Ved hjelp av årsavslutningsmalen kan organisasjonene velge finansdimensjonsnivået som skal vedlikeholdes ved overføring av resultatsaldoer til opptjente inntekter. Innstillingene gjør at en organisasjon kan vedlikeholde de detaljerte finansdimensjonene (**Avslutt alle**) når saldoene flyttes til opptjente inntekter eller velger å summere beløpene til én dimensjonsverdi (**Avslutt én**). Dette kan defineres for hver finansdimensjon. Hvis du vil ha mer informasjon om disse innstillingene, kan du se emnet [Årsavslutning](year-end-close.md).

Det anbefales at du evaluerer organisasjonens krav, og lukker så mange dimensjoner som mulig ved hjelp av årsavslutningsalternativet **Avslutt én** for å forbedre ytelsen. Ved å avslutte til én dimensjonsverdi (som også kan være en tom verdi), beregner systemet mindre detaljer når det skal fastsettes saldoer for kontooppføringer for opptjent egenkapital.

### <a name="10013-update-or-later"></a>10.0.13-oppdatering eller senere
Hvis du har oppdatert til versjon 10.0.13 eller senere siden forrige gang organisasjonen kjørte en årsavslutning, kan årsavslutningsprosessen ta lengre tid på grunn av [HashV2-funksjonsimplementeringen](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). (Begrepet *hash* refererer til et felt som beregnes fra andre strengfelter. API-en for å beregne GUID-verdien for hash ble oppdatert for å forbedre sikkerheten.) For at årsavslutningsprosessen skal gå raskere, anbefales det at du bygger opp saldoene på dimensjonssettene på nytt før du kjører årsavslutningen. Hvis du allerede har utført en gjenoppbygging av dimensjonssettsaldoene etter å ha utført 10.0.13-oppdateringen, er det ikke nødvendig å kjøre gjenoppbyggingsprosessen på nytt.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Økonomi – Hva gjør periodeavslutningen – årsavslutningen?
 
[![Periodeavslutning, årsavslutning](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Ytelsesforbedringer for gjenoppbygging av finansdimensjonssett (ny funksjon)
En ny funksjon som er lagt til i versjon 10.0.16, forbedrer ytelsen til årsavslutnings- og konsolideringsprosessene. Funksjonen får navnet Ytelsesforbedringer for gjenoppbygging av finansdimensjonssett. Denne funksjonen endrer hvordan dimensjonssett bygges opp på nytt, slik at de bare bygges opp på nytt for et relevant tidsrom. I de tidligere versjonene ble dimensjonssettene bygget opp på nytt for alle datoer. Hvis du for eksempel avslutter 2020, vil systemet bare bygge opp saldoene på nytt for transaksjoner i regnskapsåret 2020. Hvis du kjører konsolidering for et datointervall på 1. november 2020 til 30. november 2020, vil systemet bare bygge opp saldoene på nytt for dette datoområdet.

Ettersom denne funksjonen betraktes som en endring som brytes, må du aktivere den ved hjelp av arbeidsområdet for **Funksjonsbehandling**.
 
[![Årsavslutning](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Leverandør: Hvilke endringer er gjort for å støtte 1099-årsavslutningsrapportering for 2020?

To nye reguleringsfunksjoner er lagt til for 1099-årsavslutningsendringer i 2020. Den første funksjonen, **Bruk endringer i 1099-NEC- og 1099-MISC-skjemaer for 2020**, ble lansert halvveis i året som en obligatorisk funksjon. Formålet er å sikre at 1099-transaksjonsdata for året 2020 kan spores for det nye 1099-NEC-skjemaet. Denne funksjonen la til 1099-feltene som kreves for å støtte de nye 1099-NEC- og oppdaterte 1099-MISC-feltene. Denne oppdateringen oppgraderte også leverandørpostdata for 1099-boksinformasjonen. 

Den andre reguleringsfunksjonen, **1099-kontoutdrag som er oppdatert for 2020-avgiftslovgivningen**, inneholder følgende endringer.

- 1099-OID – IRS har konvertert skjemaet til sammenhengende bruk.
   - Rapporteringsårets 3. og 4. siffer må fylles ut ved utskrift. Bruk 3. og 4. siffer for feltet **Rapporteringsår** fra **Utskriftsalternativer for 1099-avgift**. 

- 1099-NEC – Et nytt skjema for 2020. Dette registrerer ingen kompensasjon. 

-   1099-MISC – På grunn av opprettingen av Skjema 1099-NEC har IRS endret skjema 1099-MISC og ordnet boksnumre for rapportering av bestemte inntekter.
Endringer i inntektsrapporteringen og skjemaets boksnumre vises nedenfor.
   - Betaler utførte direkte salg på USD 5 000 eller mer (avmerkingsboks) i boks 7.
   - Avlingsforsikringsprovenyen rapporteres i boks 9.
   - Bruttoproveny til en advokat rapporteres i boks 10.
   - Del 409A-periodiseringer rapporteres i boks 12.
   - Ikke-kvalifisert, periodisert kompensasjonsinntekt rapporteres i boks 14.
   - Boks 15, 16 og 17 rapporterer henholdsvis delstatlige avgifter, identifikasjonsnummer for delstat og inntektsbeløp som er inntekt for delstaten.

- Ingen endringer i 1099-DIV eller 1099-INT i 2020.

- Elektronisk arkivering – Formatet er endret for å legge til rette for det nye NEC-skjemaet og MISC-boksen som er beskrevet ovenfor. Hvis du vil ha bestemt informasjon om krav til elektronisk arkivering, kan du se [IRS-publikasjon 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leverandører: 1099 – Hvordan endrer jeg 1099-boksen og -verdiene for en leverandør som ikke sporer 1099-informasjon hele året?
Bruk funksjonaliteten Oppdater 1099 (**Leverandør > Leverandører >Alle leverandører > Velg en leverandør > Leverandør-fane på båndet > Update 1099**) for å gå gjennom tidligere betalte fakturatransaksjoner for å tilordne 1099-dataene på nytt på riktig måte i henhold til innstillingene i fanen **1099-avgift** på siden **Leverandør**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan jeg kjøre Update 1099 for alle leverandørene samtidig?
Nei. Update 1099-rutinen utføres mot én leverandør om gangen. Hvis dette kravet kreves av organisasjonen, kan du stemme på ideen kalt [Satsvis prosess for oppdatering av leverandørens 1099-data](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Leverandør: 1099 – Omberegn eksisterende 1099-beløp i forhold til Oppdater alle i verktøyet for Update 1099.
Hvis du merker av for **Beregn eksisterende 1099-beløp å nytt** tilbakestilles 1099-beløpet til det totale antallet betalte verdier, når dette antallet brukes sammen med avmerkingsboksen **Oppdater alle**. 

[![1099-avgiftstransaksjoner: Før kjøring av oppdateringsrutine](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Avmerkingsboksen **Omberegn eksisterende 1099-beløp** trer bare i kraft når det er delvise 1099-verdier i fakturaen, eller hvis den ble endret i 1099-avgiftsskjemaet. La oss for eksempel anta at du har en faktura som er USD 1000,00, men brukeren skriver inn et 1099-beløp manuelt på fakturaen på USD 500,00.

[![1099-avgiftstransaksjoner: Merking av både Oppdater alle og Beregning av eksisterende 1099-beløp på nytt](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Når denne betales, vil USD 500,00 bli 1099-beløpet som betales. Hvis du utfører omberegningsrutinen, vil systemet endre 1099-beløpet til USD 1000,00, som er totalsummen som ble betalt.

[![1099-avgiftstransaksjoner: Etter at 1099-rutinen er kjørt](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leverandør: 1099 – Manuell oppretting av 1099-transaksjoner
Det kan hende at en organisasjon manuelt må opprette 1099-transaksjoner som ikke er knyttet til fakturaen. Du kan legge til manuelle 1099-transaksjoner ved å gå til **Leverandører > Periodiske oppgaver > 1099-avgift > Leverandørutligning for 1099**. Velg knappen **Manuelle 1099-transaksjoner**. 

Manuelt opprettede 1099-transaksjoner oppdateres ikke med prosessen **Oppdater alle** eller prosessen **Omberegn eksisterende 1099-beløp** i verktøyet **Update 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leverandør: 1099 – Støtter Dynamics 365 Finance 1096-skjemaet? 

Dynamics 365 Finance skriver ikke ut det årlige 1096-sammendraget og skjemaet for overføring av amerikanske informasjonsreturer.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leverandør: 1099 – Er det noen nye funksjoner som støtter 1099-rapportering for offentlig sektor? 
En ny funksjon for offentlig sektor, **Oppdater 1099-informasjon etter hovedkonto**, er lagt til, og du kan aktivere den i arbeidsområdet **Funksjonsbehandling**. Ved hjelp av denne funksjonen kan du knytte 1099-verdiene for en leverandør til hovedkontoen i regnskapsdistribusjonen, i stedet for standardkontoen i leverandørposten.

Hvis du vil ha mer informasjon, kan du se [Definere leverandører for 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]