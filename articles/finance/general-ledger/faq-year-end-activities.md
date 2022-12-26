---
title: Vanlige spørsmål om årssluttaktiviteter
description: Denne artikkelen viser spørsmål som kan oppstå ved avslutning av et år, og svarene som kan hjelpe til med aktiviteter for årsavslutning.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853048"
---
# <a name="year-end-activities-faq"></a>Vanlige spørsmål om årssluttaktiviteter 

[!include [banner](../includes/banner.md)]

Denne artikkelen viser spørsmål som kan oppstå ved avslutning av et år, og svarene som kan hjelpe til med aktiviteter for årsavslutning. Informasjonen i denne artikkelen fokuserer først og fremst på spørsmål som gjelder årsavslutningsaktiviteter for økonomi- og leverandørgjeldmodulen.

## <a name="general-ledger-year-end-enhancements"></a>Forbedringer ved årsavslutning for økonomimodul

Microsoft Dynamics 365 Finance, versjon 10.0.20 innførte en forbedring av årsavslutning. Denne forbedringen er aktivert som standard fra og med versjon 10.0.25 og er obligatorisk fra og med versjon 10.0.29. Hvis organisasjonen bruker en versjon som er tidligere enn 10.0.25, anbefaler vi at du aktiverer denne funksjonen før du starter årsavslutningsprosessen. Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke arbeidsområdet **Funksjonsbehandling** til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** Økonomimodul
- **Funksjonsnavn:** Forbedringer ved årsavslutning for økonomimodul

Oppsettet av årsavslutningsmalene er flyttet til den nye oppsettsiden **Konfigurasjon av årsavslutningsmal**. Den eksisterende siden for årsavslutning blir lik siden for **revaluering av utenlandsk valuta i økonomimodulen**, der en liste vises hver gang årsavslutningen kjøres eller tilbakeføres. Siden viser ikke historisk informasjon om årsavslutninger som ble utført før funksjonen ble aktivert. En regnskapsansvarlig kan starte årsavslutningen fra den nye siden.

Hvis du vil tilbakeføre årsavslutningen, velger du det nyeste regnskapsåret for den aktuelle juridiske enheten, og deretter velger du **Tilbakefør årsavslutning**. Tilbakeføringen sletter regnskapsoppføringene for forrige årsavslutning og kjører ikke årsavslutningen på nytt automatisk. Hvis du aktiverer funksjonen **Forbedringer ved årsavslutning for økonomimodul** etter at du har fullført en årsavslutning, og du vil tilbakeføre de historiske årsavslutningsresultatene, kjører du den historiske årsavslutningen på nytt når du aktiverer økonomimodulparameteren **Slett eksisterende årsavslutningsoppføringer ved lukking av året på nytt**.

Du kan kjøre årsavslutningen på nytt ved å starte prosessen for regnskapsåret og den juridiske enheten på nytt. Prosessen fortsetter å bruke parameterinnstillingen for økonomimodulen til å finne ut om årsavslutningen skal ta hensyn til bare de nye eller endrede transaksjonene, eller om den skal kjøre prosessen på nytt for alle transaksjoner og fullstendig tilbakeføre den forrige avslutningen.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Økonomimodul: Funksjonen Forbedringer ved årsavslutning for økonomimodul er aktivert. Hvorfor kan jeg ikke se de forrige årsavslutningene i delen Logg på årsavslutningssiden?

Før aktivering av funksjonen **Forbedringer ved årsavslutning for økonomimodul**, spores datoen og klokkeslettet da forrige årsavslutningsprosess ble kjørt. Den sporer ikke loggen for hver gang årsavslutningen ble utført. Detaljene for årsavslutningskjøringen er derfor ikke tilgjengelige for visning. Når funksjonen er aktivert, opprettholdes informasjon om påfølgende årsavslutningsprosess. Bilag fra alle årsavslutningsprosesser, også de som kjøres før aktivering av funksjonen, kan vises på siden **Bilagstransaksjoner**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Økonomimodul: Årsavslutningsprosessen mislykkes på grunn av følgende feil: Årsavslutningen kan ikke kjøres fordi en eller flere finanstransaksjoner som er postert til regnskapsåret du avslutter, ble utlignet til en finanstransaksjon i et annet regnskapsår. Hva betyr denne feilen?

Ettersom funksjonen **Forståelse av utligning og årsavslutning** er aktivert, utelates bare utlignede finanstransaksjoner fra regnskapsåret som avsluttes, fra åpningssaldoen. Denne virkemåten fører til at debet og kredit kommer i ubalanse. Hvis du vil ha mer informasjon, kan du se [Forståelse av utligning og årsavslutning](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Økonomimodul: Tilbakeføring av årsavslutningsprosessen mislykkes på grunn av følgende feil: Årsavslutningen for 01.01.2022 kan ikke tilbakeføres fordi åpningssaldotransaksjoner er utlignet av finans i regnskapsåret 01.01.2023. Hva betyr denne feilen?

Ettersom funksjonen **Forståelse av utligning og årsavslutning** er aktivert, er tilbakeføringer av årsavslutningsbehandlingen ikke tillatt hvis åpningstransaksjonene er utlignet i det nye regnskapsåret. Tilbakefør utligningen i det nye regnskapsåret 2023 før du tilbakefører årsavslutningen for 1. januar 2022. Du kan eventuelt avslutte året for 1. januar 2022 på nytt, men bare for nye justeringsoppføringer. Hvis du vil avslutte året på nytt bare for justeringer, deaktiverer du økonomimodulparameteren **Slett eksisterende årsavslutningsoppføringer ved lukking av året på nytt**.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Økonomimodul: Hvorfor behandler ikke utligningsautomatiseringen utligningstransaksjoner for desember?

Funksjonen **Automatiser utligninger** kjører automatiseringen for transaksjoner som er datert fra den første dagen i regnskapsåret til gjeldende dato når forekomsten kjøres. For regnskapsår som slutter 31. desember må du kanskje justere utføringsdatoen for forekomsten for å sørge for at den kjøres i desember. Automatisering er for eksempel konfigurert til å kjøres på den første dagen i hver måned. Denne automatiseringen blir kjørt 1. desember 2022, og den er planlagt å kjøre 1. januar 2023. Vi anbefaler at du endrer forekomsten for 1. januar 2023 slik at den i stedet kjøres 31. desember 2022. Denne endringen sørger for at transaksjonene som er datert 2. desember til og med 31. desember blir tatt med for automatisk utligning.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Økonomimodul: Hva er forskjellen mellom handlingen Tilbakefør årsavslutning og parameteren Slett eksisterende årsavslutningsoppføringer når året avsluttes på nytt?

Det kan være forvirring rundt forskjellen mellom handlingen **Tilbakefør årsavslutning** og parameteren **Slett eksisterende årsavslutningsoppføringer når året avsluttes på nytt** i økonomimodulen (**Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**).

Velg handlingen **Tilbakefør årsavslutning** når du kjører årsavslutningsprosessen for å slette alle sluttsaldo- og åpningssaldooppføringer, som om årsavslutningen aldri var kjørt. I dette tilfellet blir bilagene slettet. Årsavslutningen kjøres ikke automatisk på nytt. Hvis du vil kjøre årsavslutningen, velger du handlingen **Kjør årsavslutning**.

Parameteren **Slett eksisterende årsavslutningsoppføringer ved lukking av året på nytt** i økonomimodulen brukes bare når du kjører (ikke tilbakefører) årsavslutningen. Hvis du velger **Ja** for parameteren, slettes alle sluttsaldo- og åpningssaldooppføringer, og årsavslutningen kjøres på nytt. Dette alternativet brukes når en organisasjon vil at alle transaksjoner, inkludert justeringer siden forrige årsavslutning, skal posteres i én enkelt regnskapsoppføring for sluttsaldoen og åpningssaldooppføringer. Hvis du velger **Nei** for parameteren, blir alle sluttsaldo- og åpningssaldooppføringer stående. De slettes ikke. I stedet blir det opprettet en ny sluttsaldo- og åpningssaldooppføring for bare deltaet eller nye transaksjoner som er postert siden forrige års avslutning for regnskapsåret.

> [!NOTE]
> Avslutningssaldooppføringen blir opprettet i året som avsluttes. Dette skjer bare hvis parameteren **Opprett avslutningstransaksjoner under overføring** i økonomimodulen er satt til **Ja**. Åpningssaldooppføringen opprettes alltid, ettersom dette er startsaldoen for det neste året.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Økonomimodul: Hva er forskjellen mellom alternativene Lukk alle og Lukk én i delen Overfør resultatdimensjoner i årsavslutningsprosessen?

**Lukk alle** beholder de opprinnelige finansdimensjonsverdiene fra posterte transaksjoner og bruker dem til å lage åpningssaldoer for kontoen for opptjent egenkapital. Separate startsaldoer for opptjent egenkapital opprettes for hver unike kombinasjon av finansdimensjonsverdier. Hvis **Lukk én** er valgt, blir alle transaksjoner som er postert med denne finansdimensjonen, summert i en startsaldo for opptjent egenkapital for dimensjonsverdien som er angitt i feltet som vises etter **Lukk én**. 

Alle transaksjonene for regnskapsåret ble for eksempel postert med kontostrukturen Hovedkonto – Avdeling. For finansdimensjonen Avdeling i malen er **Lukk én** valgt, og 100 angis som dimensjonsverdien. Hvis totalinntekt for alle transaksjoner som er postert til avdeling 200, 300 og 400 er USD 100 000, opprettes det én åpningssaldo for Tilbakeholdt overskudd – 100. Hvis du velger **Lukk én**, men lar finansdimensjonsverdien være tom, posteres alle transaksjoner til tilbakeholdt overskudd med denne dimensjonsverdien tom.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Økonomimodul: Vil den detaljerte transaksjonsinformasjonen min gå tapt når jeg velger alternativet Lukk én i delen Overfør resultatdimensjon i årsavslutningsprosessen?

Alternativene **Lukk alle** og **Lukk én** brukes til å angi hvilke finansdimensjoner på transaksjoner som blir postert til resultatkontoene, som skal overføres til hovedkontoen for tilbakeholdt inntekt. Den historiske, detaljerte posteringen til resultatkontoene påvirkes ikke og forblir i detaljer. Alternativet påvirker detaljnivået som overføres til kontoene for tilbakeholdt inntekt, som en åpningssaldo i det nye året. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Økonomimodul: Årsavslutningsprosessen mislykkes fordi rapporteringsvalutaen for året ikke er i balanse. Hva betyr det?

Du kan få denne feilen etter at du har aktivert funksjonen **Forståelse av utligning og årsavslutning** (funksjonen Forståelse). Når funksjonen er aktivert, inkluderes ikke finanstransaksjoner som er utlignet, lenger i åpningssaldoen for det neste regnskapsåret når årsavslutningen for økonomimodulen kjøres. Hvis du utelukker finanstransaksjoner som er utlignet, kan det by på en utfordring for kunder ved årsavslutning hvis finans er definert med en rapporteringsvaluta.   
Utligning utføres bare for regnskapsvalutaen.  Når finanstransaksjonene utlignes, sikrer validering bare at regnskapsvalutadebetene er lik regnskapsvalutakredittene. Rapporteringsvalutabeløpene for disse finanstransaksjonene er ikke validert og har kanskje ikke debet = kredit.  I tillegg beregner og posterer ikke utligningen automatisk et resultat i rapporteringsvalutaen.  På grunn av disse begrensningene må det finnes en resultattransaksjon i rapporteringsvalutaen ved utføring av utligning.  Hvis resultatet ikke er inkludert i utligningen, fører årsavslutningen til en melding om ubalanse.  Hvis du vil ha mer informasjon, kan du se [Forståelse av melding om at utligningsfunksjon og rapporteringsvaluta er i ubalanse](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Økonomimodul: Hva kan endres for å bidra til å forbedre ytelsen ved årsavslutningsbehandling?

Du kan foreta flere endringer for å bidra til å forbedre ytelsen ved årsavslutningen. Det anbefales at du evaluerer disse foreslåtte endringene for å bestemme om de er riktige for organisasjonen din.

### <a name="optimize-year-end-close-service"></a>Tjenesten Optimaliser årsavslutning

Med tjenesten **Optimaliser årsavslutning** kan Microsoft Dynamics 365 Finance-kunder få raskere årsavslutning ved å flytte den tunge årsavslutningsprosessen til en mikrotjeneste. Tiden som spares gjennom en effektiv årsavslutning, gjør at hver Finance-gruppe kan respondere raskt på nødvendige justeringer, noe som ender opp med genereringen av finansrapportene. Ved å behandle årsavslutningen på en mikrotjeneste frigjøres verdifulle ressurser. Behandlingshøyden minimerer belastningen på SQL Server og gir kundene en mulighet til å fremskynde årsavslutningsbehandlingen.

Tjenesten **Optimaliser årsavslutning** er tilgjengelig i versjon 10.0.31, slik at flere kunder kan bruke den nye tjenesten for årsavslutningssesongen 2022. I tillegg har tjenesten blitt tilbakeportert til versjon 10.0.30 og 10.0.29. Hvis du vil ha mer informasjon, kan du se [Optimaliser årsavslutning](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensjonssett

Når du kjører årsavslutningen, bygges hver dimensjonssettsaldo på nytt. Denne virkemåten påvirker ytelsen direkte. Noen organisasjoner oppretter dimensjonssett unødvendig fordi de ble brukt på et tidspunkt, eller kan bli brukt på et tidspunkt. Siden disse unødvendige dimensjonssettene bygges opp på nytt i løpet av årsavslutningen, legges det til tid til prosessen. Ta deg tid til å evaluere dimensjonssettene og slette alle som er unødvendige.

Unødvendige dimensjonssett påvirker også den satsvise jobben **BudgetDimensionFocusInitializeBalance** (**Økonomimodul \> Kontoplan \> Dimensjoner \> Finansdimensjonssett**).

[![Finansdimensjonssett.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Konfigurasjon av årsavslutningsmal

Ved hjelp av årsavslutningsmalen kan organisasjonene velge finansdimensjonsnivået som skal vedlikeholdes ved overføring av resultatsaldoer til opptjente inntekter. Innstillingene gjør at en organisasjon kan vedlikeholde de detaljerte finansdimensjonene (**Avslutt alle**) når saldoene flyttes til opptjente inntekter eller velger å summere beløpene til én dimensjonsverdi (**Avslutt én**). Dette kan defineres for hver finansdimensjon. Hvis du vil ha mer informasjon om disse innstillingene, kan du se artikkelen [Årsavslutning](year-end-close.md).

Det anbefales at du evaluerer organisasjonens krav, og lukker så mange dimensjoner som mulig ved hjelp av årsavslutningsalternativet **Avslutt én** for å forbedre ytelsen. Ved å avslutte til én dimensjonsverdi (som også kan være en tom verdi) beregner systemet mindre detaljer når det skal fastsettes saldoer for kontooppføringer for opptjent egenkapital.

### <a name="degenerate-dimensions"></a>Degenerer dimensjoner

En degenert dimensjon gir liten eller ingen mulighet til å gjenbruke den i seg selv og i kombinasjon med andre dimensjoner. Det finnes to typer degenererte dimensjoner. Den første typen er en dimensjon som degenereres individuelt. Denne typen degenerert dimensjon vises vanligvis bare på én enkelt transaksjon eller på små sett med transaksjoner. Den andre typen er en dimensjon som blir degenerert i kombinasjon med en eller flere tilleggsdimensjoner som har det samme potensialet, basert på mulige unntak som kan genereres. En degenerert dimensjon kan ha en betydelig innvirkning på ytelsen til årsavslutningsprosessen. Hvis du vil redusere ytelsesproblemer, kan du definere alle degenererte dimensjoner som **Avslutt én** i årsavslutningsoppsettet, som beskrevet i den forrige delen.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Leverandørgjeld: Hvilke endringer er gjort for å støtte 1099-årsavslutningsrapportering for 2022?

#### <a name="update-to-all-1099-forms"></a>Oppdatering i alle 1099-skjemaer

Følgende endringer er gjort i alle 1099-skjemaer for avgiftsåret 2022:

- I 2021 var året fast på 1099-skjemaer. Fra og med 2022 fylles året ut av rapporten.

#### <a name="1099-misc"></a>1099-MISC

Følgende oppdateringer er gjort i skjema 1099-MISC for avgiftsåret 2022:

- Boks 13: Angir nå FATCA-innsendingskravet (Foreign Account Tax Compliance Act).
- Boks 14: Brukes nå til å rapportere overflødige betalinger for gyllen fallskjerm.
- Boks 15: Brukes nå til å rapportere betalingen under ikke-kvalifiserte planer for utsatt kompensasjon (NQDC).
- Boks 16: Brukes nå til å rapportere statlig tilbakeholdte avgifter.
- Boks 17: Brukes nå til å rapportere betalerens delstatsnummer.
- Boks 18: Brukes nå til å rapportere delstatlig inntekt.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leverandørgjeld: 1099 – Hvordan endrer jeg 1099-boksen og -verdiene for en leverandør som ikke sporer 1099-informasjon hele året?

Bruk funksjonaliteten **Oppdater 1099** for å gå gjennom fakturatransaksjoner som allerede er betalt, og tildel 1099-dataene på nytt på riktig måte, i henhold til innstillingene i fanen **Avgift 1099** på siden **Leverandør**. Hvis du vil bruke funksjonaliteten **Oppdater 1099**, går du til **Leverandørgjeld \> Leverandører \> Alle leverandører** og velger en leverandør. I handlingsruten velger du **Oppdater 1099** i fanen **Leverandører**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Kan jeg kjøre funksjonaliteten Oppdater 1099 for alle leverandørene samtidig?

Du kan bruke siden **Oppdater 1099-informasjon for flere leverandører** til å oppdatere 1099-boksen på en leverandørpost, og til å oppdatere transaksjoner med informasjonen fra 1099-boksen. Du åpner denne siden ved å gå til **Leverandørgjeld \> Periodisk oppgave, \> Avgift 1099**. For å få tilgang til siden må du være delt sikkerhetsrettigheten **Oppdater 1099-boksen og -transaksjoner for flere leverandører**.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Leverandørgjeld: 1099 – Omberegn eksisterende 1099-beløp i forhold til Oppdater alle i verktøyet for Oppdater 1099

Hvis du merker av for **Beregn eksisterende 1099-beløp å nytt**, tilbakestilles 1099-beløpet til det totale antallet betalte verdier når det brukes sammen med avmerkingsboksen **Oppdater alle**.

[![1099-avgiftstransaksjoner: Før kjøring av oppdateringsrutine.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Avmerkingsboksen **Omberegn eksisterende 1099-beløp** trer bare i kraft hvis det er delvise 1099-verdier i fakturaen, eller hvis fakturaen ble endret i 1099-avgiftsskjemaet. La oss for eksempel anta at du har en faktura som er USD 1000,00, men brukeren angir et 1099-beløp på USD 500,00 manuelt på fakturaen.

[![1099-avgiftstransaksjoner: Merking av både Oppdater alle og Beregning av eksisterende 1099-beløp på nytt.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Når denne fakturaen betales, blir USD 500,00 1099-beløpet som betales. Hvis du utfører omberegningsrutinen, blir 1099-beløpet endret til USD 1000,00, som er totalsummen som ble betalt.

[![1099-avgiftstransaksjoner: Etter at 1099-rutinen er kjørt.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leverandør: 1099 – Manuell oppretting av 1099-transaksjoner

Det kan hende at en organisasjon manuelt må opprette 1099-transaksjoner som ikke er knyttet til fakturaen. Du kan legge til manuelle 1099-transaksjoner ved å gå til **Leverandører \> Periodiske oppgaver \> 1099-avgift \> Leverandørutligning for 1099**. Velg knappen **Manuelle 1099-transaksjoner**.

Manuelt opprettede 1099-transaksjoner oppdateres ikke med prosessen **Oppdater alle** eller prosessen **Omberegn eksisterende 1099-beløp** i verktøyet **Update 1099**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leverandørgjeld: 1099 – Støtter Dynamics 365 Finance 1096-skjemaet?

Dynamics 365 Finance skriver ikke ut det årlige 1096-sammendraget og skjemaet for overføring av amerikanske informasjonsreturer.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leverandør: 1099 – Er det noen nye funksjoner som støtter 1099-rapportering for offentlig sektor?

En ny funksjon for offentlig sektor, **Oppdater 1099-informasjon etter hovedkonto**, er lagt til, og du kan aktivere den i arbeidsområdet **Funksjonsbehandling**. Ved hjelp av denne funksjonen kan du knytte 1099-verdiene for en leverandør til hovedkontoen i regnskapsdistribusjonen, i stedet for standardkontoen i leverandørposten.

Hvis du vil ha mer informasjon, kan du se [Definere leverandører for 1099-rapportering](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
