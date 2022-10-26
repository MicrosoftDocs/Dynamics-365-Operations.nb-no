---
title: Arbeidsområde for kostnadskontroll
description: Denne artikkelen gir informasjon om arbeidsområdet for kostnadskontroll. Dette arbeidsområdet er et sentralt punkt der ledere som har ansvaret for å kontrollere et kostnadsobjekt eller et sett med kostnadsobjekter i en dimensjon eller på tvers av dimensjoner, kan få tilgang til rapporter.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace, CAMCostControlWorkspaceConfigurationPerUser
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8d5ded4b08d562fff9ec5fd9a3de591f944e3ee0
ms.sourcegitcommit: dca54dd3afc7c94795d89c63050b105df2c48e3f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/15/2022
ms.locfileid: "9682905"
---
# <a name="cost-control-workspace"></a>Arbeidsområde for kostnadskontroll 

[!include [banner](../includes/banner.md)]

Arbeidsområdet **Kostnadskontroll** er et sentralt punkt der ledere som har ansvaret for å kontrollere et kostnadsobjekt eller et sett med kostnadsobjekter i en dimensjon eller på tvers av dimensjoner, kan få tilgang til rapporter. Rapportene i arbeidsområdet blir administrert i sin helhet av regnskapsførere, slik at oppsettet og dataene som brukes til rapportering, blir konsekvent på tvers av hele organisasjonen.

## <a name="cost-control-workspace-configuration"></a>Konfigurasjon av arbeidsområde for kostnadskontroll

Regnskapsførere kan definere så mange rapportkonfigurasjoner de trenger for ønsket datasammensetning eller oppsett. En rapportkonfigurasjon består av seks deler, der hver del bidrar til valget av datasammensetningen eller oppsettet.

Hvis du vil konfigurere et arbeidsområde for kostnadskontroll, klikker du på **Kostnadsregnskap** \> **Oppsett** \> **Konfigurasjon av arbeidsområde for kostnadskontroll**.

### <a name="general"></a>Generelt

Du kan opprette et unikt rapportoppsett i hurtigfanen **Generelt**. Navnet på rapporten er en unik identifikator som brukere kan gjenkjenne i arbeidsområdet **Kostnadskontroll**. Du kan også angi om rapporten skal deles eller holdes intern for regnskapsførere.

| Felt       | Beskrivelse |
|-------------|-------------|
| Navn        | Skriv inn et unikt navn for oppsettet. |
| Beskrivelse | Angi en detaljert beskrivelse. |
| Publisert   | Hvis du setter dette feltet til **Ja**, kan en bruker som er tilordnet en av følgende roller, se rapporten i arbeidsområdet **Kostnadskontroll**:<ul><li>Behandling av kostnadsregn</li><li>Regnskapsfører lager</li><li>Assisterende lagerregnskapsfører</li><li>Kontroller for kostnadsobjekt</li></ul>Hvis du setter dette feltet til **Nei**, kan bare brukere som er tilordnet en av følgende roller, se rapporten i arbeidsområdet **Kostnadskontroll**:<ul><li>Behandling av kostnadsregn</li><li>Regnskapsfører lager</li><li>Assisterende lagerregnskapsfører</li></ul> |

### <a name="data-filtering"></a>Datafiltrering

Du kan definere datagrunnlaget for rapporten i hurtigfanen **Datafiltrering**. Brukere av denne rapporten kan se verdiene i den etter at kildedataene er behandlet.

| Felt                                                             | Beskrivelse |
|-------------------------------------------------------------------|-------------|
| Kostnadsregnskapsfinans                                            | **Kostnadsregnskapsfinans** som rapporten er basert på. Verdien hentes fra feltet **Kostnadskontrollenhet**. |
| Kostnadskontrollenhet                                                 | Verdien du velger, fastsetter kostnadsregnskapsfinansen og kostnadsobjektene som denne rapporten skal baseres på. |
| Dimensjonshierarki for statistikk, Dimensjonshierarki for kostnadselement | En post for konfigurasjon av arbeidsområdet **Kostnadskontroll** kan rapportere ikke-monetære eller monetære verdier, men ikke i samme oppsett. Velg en verdi i feltet **Dimensjonshierarki for kostnadselement** for å rapportere monetære verdier. Velg en verdi i feltet **Dimensjonshierarki for statistikk** for å rapportere ikke-monetære verdier. Dimensjonshierarkiposten du velger, fastsetter strukturen for rapporteringen og aggregeringsnivåene.<blockquote>**Obs:**<br>Hvis du vil vise ikke-monetære og monetære verdier ved siden av hverandre, kan du eksportere data til Microsoft Excel for innholdspakken for Microsoft Power BI.</blockquote> |
| Dimensjonsobjekt for kostnadselement      | Velg dimensjonshierarkiet for kostnadsobjektdimensjonen som passer til formålet med rapportering du definerer. |
| Opprinnelig budsjettversjon                                           | Velg budsjettversjons-ID-en som fungerer som det opprinnelige budsjettet i forbindelse med denne rapporten. |
| Revidert budsjettversjon                                            | Velg budsjettversjons-ID-en som fungerer som det reviderte budsjettet i forbindelse med denne rapporten. |

### <a name="assign-calculation-records"></a>Tilordne beregningsposter

Beregningen av indirekte kostnader utfører beregning av kildedataene i flere trinn, for eksempel kostnadsdistribusjon, kostnadstildeling og klassifisering av kostnadsatferd. Du kan utføre flere beregninger av indirekte kostnader for samme regnskapsperiode, i tilfelle du oppdager manglende kildedata, eller hvis regler må oppdateres. Hver beregning av indirekte kostnader lagres med en unik ID. Regnskapsføreren kan velge en bestemt ID for beregning av indirekte kostnader. Brukere av rapporten, for eksempel ledere, kan se resultatet av beregningen av indirekte kostnader i arbeidsområdet **Kostnadskontroll**.

| Felt                  | Beskrivelse |
|------------------------|-------------|
| Økonomisk kalenderperiode | Velg regnskapskalenderperioden du vil tilordne en ID for beregning av indirekte kostnader til.<blockquote>**Obs:**<br>Regnskapsperiodene som er oppført i feltet, kommer fra regnskapskalenderen som er knyttet til kostnadsregnskapsfinansen.</blockquote> |
| Faktisk versjon         | Velg den aktuelle ID-en for beregning av indirekte kostnader. |
| Budsjettversjon         | Velg den aktuelle ID-en for beregning av indirekte kostnader. |
| Revidert budsjettversjon | Velg den aktuelle ID-en for beregning av indirekte kostnader. |

### <a name="fiscal-periods-per-column"></a>Regnskapsperioder per kolonne

I hurtigfanen **Regnskapsperioder per kolonne** bestemmer regnskapsføreren hvilken regnskapsperiode som skal vises i rapportoppsettet.

Verdiene i de merkede kolonnene multipliseres med de merkede verdiene i hurtigfanen **Regnskapsperioder per kolonne**.

| Felt                | Beskrivelse |
|----------------------|-------------|
| Nåværende periode       | Saldoen for gjeldende regnskapsperiode vises.<blockquote>**Obs:**<br>Gjeldende periode fastsettes som standard av øktdatoen. Du kan velge en bestemt regnskapsperiode i arbeidsområdet **Kostnadskontroll**. Den valgte verdien representerer deretter gjeldende periode.</blockquote> |
| Forrige periode      | Saldoen for forrige regnskapsperiode vises. Følgende formel brukes:<br>Gjeldende regnskapsperiode – 1<blockquote>**Obs:**<br>Forrige periode avledes som standard fra øktdatoen. Du kan velge en bestemt regnskapsperiode som gjeldende periode i arbeidsområdet **Kostnadskontroll**. **Forrige periode** blir deretter beregnet på nytt i samsvar med dette.</blockquote> |
| Hittil i år         | Saldoen hittil i år vises. Følgende formel brukes:<br>YearToDate (gjeldende regnskapsperiode)<blockquote>**Obs:**<br>Gjeldende periode fastsettes som standard av øktdatoen. Du kan velge en bestemt regnskapsperiode i arbeidsområdet **Kostnadskontroll**. Den valgte verdien representerer deretter gjeldende periode, og verdien for **Hittil i år** oppdateres i samsvar med dette.</blockquote> |
| Gjennomsnitt hittil i år | Gjennomsnittet hittil i år vises. Følgende formel brukes:<br>(YearToDate [gjeldende regnskapsperiode]) ÷ (antall [gjeldende regnskapsperiode])<p><strong>Eksempel</strong></p><ul><li>**Medlem av statistisk dimensjon:** heltidsansatte</li><li>**Gjeldende dato:** 21.03.2017</li><li>**Periode:** regnskapsperiode 1, regnskapsperiode 2, regnskapsperiode 3</li><li>**Størrelse:** 10, 10, 12</li></ul>I dette tilfellet er **Gjennomsnitt hittil i år** = (10 + 10 + 12) ÷ 3 = 10,67<p>Verdien for **Gjennomsnitt hittil i år** kan beregnes for medlemmer av dimensjon for kostnadselement og medlemmer av statistisk dimensjon.</p><blockquote>**Obs:**<br>Gjeldende periode fastsettes som standard av øktdatoen. Du kan velge en bestemt regnskapsperiode i arbeidsområdet **Kostnadskontroll**. Den valgte verdien representerer deretter gjeldende periode, og verdiene for **Hittil i år** og **Gjennomsnitt hittil i år** oppdateres i samsvar med dette.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Kolonner som skal vises for kostnader

I hurtigfanen **Kolonner som skal vises for kostnader** bestemmer regnskapsføreren hvilke kolonner rapportoppsettet skal inneholde. Det finnes tre kategorier: Fast kostnad, Variabel kostnad og Uklassifisert kostnad.

| Felt                 | Beskrivelse |
|-----------------------|-------------|
| Fast kostnad            | Denne kolonnetypen viser den faste kostnaden, basert på den valgte ID-en for beregning av indirekte kostnader.<blockquote>**Obs:**<br>Denne kolonnetypen viser en saldo bare når en ID for beregning av indirekte kostnader blir valgt for regnskapsperioden.</blockquote> |
| Variabel kostnad         | Denne kolonnetypen viser den variable kostnaden, basert på den valgte ID-en for beregning av indirekte kostnader.<blockquote>**Obs:**<br>Denne kolonnetypen viser en saldo bare når en ID for beregning av indirekte kostnader blir valgt for regnskapsperioden.</blockquote> |
| Fast + variabel kostnad | Denne kolonnetypen viser den faste kostnaden og variable kostnaden, basert på den valgte ID-en for beregning av indirekte kostnader.<blockquote>**Obs:**<br>Denne kolonnetypen viser en saldo bare når en ID for beregning av indirekte kostnader blir valgt for regnskapsperioden.</blockquote> |
| Total kostnad            | Denne kolonnetypen viser den totale kostnaden (uklassifisert kostnad, fast kostnad og variabel kostnad).<blockquote>**Obs:**<br>Kolonnetypen viser balansen til enhver tid.</blockquote> |
| Uklassifisert kostnad     | Denne kolonnetypen viser den uklassifiserte kostnaden.<blockquote>**Obs:**<br>Denne kolonnen kan brukes til å validere om alle kostnader er riktig klassifisert av beregningen av indirekte kostnader, eller om du må justere reglene for kostnadsatferd.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Kolonner som skal vises for budsjetterte kostnader

I hurtigfanen **Kolonner som skal vises for budsjetterte kostnader** bestemmer regnskapsføreren hvilke kolonner som skal vises for de valgte budsjettversjonene. Du kan gjøre enkeltvalg for det opprinnelige og reviderte budsjettet.

> [!NOTE]
> Siden følgende felt fungerer på samme måte for det opprinnelige budsjettet og reviderte budsjettet, blir de forklart bare én gang.

| Felt                     | Beskrivelse |
|---------------------------|-------------|
| Budsjett                    | Budsjettsaldoer blir vist per de merkede kolonnene.<blockquote>**Obs:**<br>Saldoene baseres på budsjettversjonene som er valgt i hurtigfanen **Datafiltrering**.</blockquote> |
| Budsjettavvik           | Beregne og vise forskjellene mellom budsjett og faktisk. Følgende formel brukes:<br>Budsjettsaldo – faktisk saldo |
| Budsjettavvik i %      | Beregne og vise forskjellene mellom budsjett og faktisk i prosent. Følgende formel brukes:<br>(Budsjettsaldo – faktisk saldo) ÷ budsjettsaldo |
| Terskel for avviksperiode | Angi en terskel for avviket i pengebeløp for gjeldende periode. Hvis terskelen overskrides, blir linjen uthevet i rødt i arbeidsområdet **Kostnadskontroll**.<blockquote>**Obs:**<br>Dette feltet gjelder bare for kostnadselementer som representerer utgifter.</blockquote> |
| Terskel for avviksår   | Angi en terskel for avviket i pengebeløp for året. Hvis terskelen overskrides, blir linjen uthevet i rødt i arbeidsområdet **Kostnadskontroll**. |
| Avviksterskel i %      | Angi en terskel for avviket i prosent. Hvis terskelen overskrides, blir linjen uthevet i rødt i arbeidsområdet **Kostnadskontroll**.<blockquote>**Obs:**<br>Den samme prosentterskelen gjelder for gjeldende periode og år.</blockquote> |

## <a name="cost-control-workspace"></a>Arbeidsområde for kostnadskontroll

Arbeidsområdet **Kostnadskontroll** er utformet som en webrapport. Derfor kan alle ledere som er ansvarlige for et kostnadsobjekt, få tilgang som beskrevet i [Definere tilgangsrettigheter til kontrollere for kostnadsobjekt](access-rights-cost-object-controller.md).

Listen over rapporter som er tilgjengelige for brukere, for eksempel ledere, styres av innstillingen for alternativet **Publisert** på siden **Konfigurasjoner av arbeidsområde for kostnadskontroll**.

![En rapport som brukere kan se i arbeidsområdet for kostnadskontroll.](./media/report-cost-control.png)

En leder kan velge regnskapskalenderperioden som skal vises. Øktdatoen brukes til å fastsette standard gjeldende periode.

Verdiene i regnskapskalenderperioden fastsettes av rapportnavnet og regnskapskalenderen som er valgt for kostnadsregnskapsfinansen som er knyttet til rapportnavnet på siden **Konfigurasjoner av arbeidsområde for kostnadskontroll**.

Brukere kan velge aggregeringsnivået som saldoer skal vises på, i dimensjonshierarkiet for kostnadsobjekt. Når du aktiverer tilgangsnivåsikkerhet, kontrollerer du tillatelsene slik at brukere bare kan velge hierarkinivåene de har fått tilgang til. Derfor kan de bare se de aggregerte saldoene de har fått tilgang til.

### <a name="add-or-remove-columns"></a>Legg til eller fjern kolonner

Brukere kan tilpasse kolonnene i en rapport til behovene deres.

### <a name="view-details"></a>Vis detaljer

Brukere kan drille ned i detaljene bak saldoene som vises i arbeidsområdet. Hvis brukere velger en dimensjonshierarkinode for kostnadselement og deretter klikker på **Vis detaljer**, viser dialogboksen **Kostnadselementdetaljer** detaljert informasjon for noden.

Et rutenett viser hvert kostnadselement som er knyttet til dimensjonshierarkinoden for kostnadselement, og verdiene for den. Kolonnene som vises i rutenettet, samsvarer med innstillingene for arbeidsområde.

To diagrammer viser et sammendrag av faktisk kontra budsjett og budsjettavvik etter periode.

![Diagrammer som viser et sammendrag av faktisk kontra budsjett og budsjettavvik etter periode.](./media/cost-element-details-operations.png)

Brukere kan klikke på **Kostnadsoppføringer** for å drille ned i oppføringsdetaljene etter behov.

![Kostnadsoppføringer.](./media/cost-entries.png)

Leie er for eksempel en utgift som distribueres til kostsentre. En bruker som vil ha klarhet i leiekostnaden som kostsenteret til vedkommende må betale, kan drille ned for å se hvordan leien beregnes.

Hvis du klikker på **Tildelingsgrunnlag** på **Kostnadsoppføringer**-siden, vises en dialogboks. Brukere kan deretter tilordne tildelingsgrunnlaget til regelen og vise de tilsvarende statistiske målingene som er registrert for perioden.

I eksemplet nedenfor er tildelingsgrunnlaget av typen **Formeltildelingsgrunnlag**, og formelen vises. Faktorene som definerer formelen, vises. I tillegg viser et rutenett beregningen som utføres per kostnadsobjekt.

![Beregninger per kostnadsobjekt.](./media/cost-entries-allocation-base.png)

Tilleggsressurser 

[Definere tilgangsrettigheter for kontrollere for kostnadsobjekt](access-rights-cost-object-controller.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
