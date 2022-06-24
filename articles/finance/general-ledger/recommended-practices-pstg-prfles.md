---
title: Anbefalte fremgangsmåter for posteringsprofiler
description: Denne artikkelen beskriver anbefalte fremgangsmåter for å konfigurere posteringsprofiler.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849909"
---
# <a name="recommended-practices-for-posting-profiles"></a>Anbefalte fremgangsmåter for posteringsprofiler

Det er flere anbefalte fremgangsmåter du bør følge når du konfigurerer posteringsprofiler i hele systemet. Denne artikkelen beskriver ulike scenarier og tilsvarende anbefalte fremgangsmåter.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Angi flagget Ikke tillat manuell registrering

På siden **Hovedkontoer** bør det være merket av for **Ikke tillat manuell registrering** for enhver hovedkonto som brukes i en posteringsprofil. Denne innstillingen hindrer brukere i å postere en journaloppføring manuelt til hovedkontoen. Derfor er det med på å sikre at underfinansen forblir i balanse med økonomimodulen, og bidrar til å gjøre avstemmingsprosessen enklere.

Hvis det kreves justeringer for en konto som kontrolleres av systemet og posteres automatisk, kan du bruke én av disse metodene:

- Opprett en sekundær hovedkonto der justeringene kan posteres. Deretter kan du bruke en totalkonto eller en spesialrad i finansrapportene til å gruppere og summere kontoene sammen.
- Tilbakefør de opprinnelige transaksjonene i den aktuelle underledgeren, gjør eventuelle nødvendige korrigeringer og poster transaksjonen på nytt via samme underkonto.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Endre posteringsprofiler etter at det finnes transaksjoner

Hvis du endrer en posteringsprofil når det finnes transaksjoner, kan avstemmingen mislykkes, og underfinansmodulen og finans kan bli ut av balanse. Generelt anbefaler vi at du **ikke** endrer posteringsprofilen når det finnes transaksjoner.

Hvis det kreves endringer, bruker du følgende retningslinjer for å sikre integriteten for systemet:

- Gjør endringene i en periodeavslutning.
- Foreta endringene når det ikke forekommer noen andre transaksjoner i systemet.
- Valider hovedboken og avstem den til underfinans før og etter at du har gjort endringene.
- Posterte transaksjoner oppdateres ikke hvis du endrer posteringsprofilen. Vurder nøye om du må vurdere eventuelle justeringsoppføringer for endringen.
- Hvis du endrer lagerposteringsprofilene, må du vurdere hvordan endringene vil påvirke lagerbeholdningen og finanssaldoene. Enkelte endringer kan kreve at du bringer lageret til 0 (null), lukker lageret og henter deretter lageret tilbake etter at endringene er gjort.
- Test alltid endringene i et ikke-produksjonsmiljø før du lager dem i produksjon.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Bruk databaselogging til å revidere endringer i posteringsprofiler

Vurder å definere databaselogging for hver posteringsprofil og for parametertabeller som kontrollerer postering. Hvis en parameter eller profil endres, vil du få en full revisjonspost med hvilken verdi som ble endret, hvem som endret den, når den ble endret og hva den forrige verdien var. Denne informasjonen kan være kritisk under avstemmingsprosessen, og revisoren kan kreve støttedokumentasjonen.

Hvis du vil ha mer informasjon, kan du se [Konfigurer databaselogging](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Bruk tabellen nedenfor som en referanse for vanlige tabellnavn som er relatert til posteringsprofiler og relaterte posteringsparametere.

| Sidenavn | Navigasjonsrute | Tabellnavn |
|-----------|-----------------|------------|
| Leverandørparametere | Leverandører &gt; Oppsett &gt; Leverandørparametere | VendParm |
| Leverandørposteringsprofil | Leverandører &gt; Oppsett &gt; Leverandørposteringsprofil | VendPosting |
| Tilleggskode | Leverandører &gt; Oppsett for tillegg &gt; Tilleggskode eller Kunder &gt; Oppsett for tillegg &gt; Tilleggskode | MarkupTable |
| Betalingsmåter | Leverandører &gt; Betalingsoppsett &gt; Betalingsmåter | VendPaymMode |
| Kontantrabatt | Leverandører &gt; Betalingsoppsett &gt; Kontantrabatt eller Kunder &gt; Betalingsoppsett &gt; Kontantrabatt | CashDisc |
| Betalingsgebyr (leverandør) | Leverandører &gt; Betalingsoppsett &gt; Betalingsgebyr | VendPaymFee |
| Parametere for kundereskontro | Kunder &gt; Oppsett &gt; Kundeparametere | CustParm |
| Kundeposteringsprofiler | Kunder &gt; Oppsett &gt; Kundeposteringsprofil | CustPosting |
| Betalingsmåter | Kunder &gt; Betalingsoppsett &gt; Betalingsmåter | CustPaymMode |
| Betalingsgebyr (kunde) | Kunder &gt; Betalingsoppsett &gt; Betalingsmåter | CustPaymFee |
| Parametere for aktivaleie | Aktivaleie &gt; Oppsett &gt; Parametere for aktivaleie | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankkontoer | Kontant- og bankbehandling &gt; Bankkontoer &gt; Bankkontoer | BankAccountsTable |
| Banktransaksjonstyper | Kontant- og bankbehandling &gt; Oppsett &gt; Banktransaksjonstyper | BankTransType |
| Elimineringsregler | Konsolideringer &gt; Oppsett &gt; Elimineringsregel | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Utgiftskategorier | Reiseregning &gt; Oppsett &gt; Generelt &gt; Utgiftskategorier | ProjCategories |
| Parametere for anleggsmidler | Anleggsmidler &gt; Oppsett &gt; Parametere for anleggsmidler | AssetParameters |
| Posteringsprofiler for anleggsmidler | Anleggsmidler &gt; Oppsett &gt; Posteringsprofiler for anleggsmidler | AssetLedgerAccounts<br>AssetDisposalParameters |
| Valutarevalueringskontoer | Økonomimodul &gt; Valutaer &gt; Kontoer for revaluering av valuta | CurrencyLedgerGainLossAccount |
| Kontoer for automatiske transaksjoner | Økonomimodul &gt; Posteringsoppsett &gt; Kontoer for automatiske transaksjoner | LedgerSystemAccounts |
| Konserninternt regnskap | Økonomimodul &gt; Posteringsoppsett &gt; Konserninterne kontoer | LedgerIntercompany |
| Definisjoner for transaksjonspostering | Økonomimodul &gt; Posteringsoppsett &gt; Definisjoner for transaksjonspostering | JournalizingDefinitionTrans |
| Posteringsdefinisjoner | Økonomimodul &gt; Posteringsoppsett &gt; Posteringsdefinisjoner | JournalizingDefintion |
| Postering (lager) | Lagerstyring &gt; Oppsett &gt; Postering &gt; Postering | InventPosting |
| Kostnadstypekoder | Netto innkjøpspris &gt; Kostnadsoppsett &gt; Kosttypekoder | ITMCostTypeTable |
| Ressurser | Produksjonskontroll &gt; Oppsett &gt; Ressurser &gt; Ressursfunksjoner | WrkCtrTable |
| Ressursgrupper | Produksjonskontroll &gt; Oppsett &gt; Ressurser &gt; Ressursgrupper | WrkCtrResourceGroup |
| Produksjonsgrupper | Produksjonskontroll &gt; Oppsett &gt; Produksjon &gt; Produksjonsgruppe | ProdGroup |
| Kostnadskategorier | Produksjonskontroll &gt; Oppsett &gt; Ruter &gt; Kostnadskategorier | ProjCategory |
| Prosjektgrupper | Prosjektstyring og regnskap &gt; Oppsett &gt; Postering &gt; Prosjektgrupper | ProjGroup |
| Finansposteringsoppsett (prosjekter) | Prosjektstyring og regnskap &gt; Oppsett &gt; Postering &gt; Finansposteringsoppsett | ProjPosting |
| Standard motkonto for utgifter | Prosjektstyring og regnskap &gt; Oppsett &gt; Postering &gt; Standard motkontoer for utgifter | ProjDefaultOffsetSetup |
| Posteringsprofiler i Rabattbehandling | Rabattbehandling &gt; Posteringsoppsett for rabattbehandling &gt; Posteringsprofiler i Rabattbehandling | TAMRebatePosting |
| Finansposteringsgruppe (avgift) | Avgift &gt; Oppsett &gt; Merverdiavgift &gt; Finansposteringsgruppe | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Endre grupper etter at det finnes transaksjoner

Vær forsiktig når du endrer grupper i hoveddata. Hvis du bruker grupper til å definere posteringsprofilene, kan alle endringer i en gruppe i en hovedpost ha negativ virkning på evnen til å avstemme finans til underfinansen. Du kan for eksempel konfigurere lagerposteringsprofilen for salgsordreinntekter, slik at en annen inntektskonto brukes for hver varegruppe. Hvis du endrer varegruppen som er tilordnet til en vare etter at det finnes transaksjoner, blir omsetningen på nye transaksjoner postert til den oppdaterte kontoen. Inntekter som ble postert før endringen, vil imidlertid bli værende på den opprinnelige kontoen.

## <a name="testing-posting-profiles"></a>Testing av posteringsprofiler

Før du går live, og etter at du har gjort endringer eller tillegg i posteringsprofilene eller de tilknyttede parameterne, bør du teste hvert scenario. Du bør som et minimum teste hver posteringstype for å validere at posteringen fungerer som den skal. Den anbefalte tilnærmingen er imidlertid å teste hver posteringsprofiltransaksjon og -kombinasjon.

Du har for eksempel to kundeposteringsprofiler, der hver har tre poster som er spesifikke for kundegrupper. I dette tilfellet bør du teste hver transaksjonstype.

**Posteringsprofiler:**

- **GEN** – Den generelle posteringsprofilen som har én gruppe for ansatte, én for kunder og én for konsernintern. Hver gruppe peker på en annen handelskonto for kunder.
- **PRE** – Posteringsprofilen for forskuddsbetaling som har én post for alle forskuddsbetalinger som peker til kundens forskuddsbetalingskontoer.

### <a name="testing-scenarios"></a>Testing av scenarioer

- Fritekstfaktura for en kunde i **Ansatt**-gruppen som bruker **GEN**-posteringsprofilen
- Fritekstfaktura for en kunde i **Ansatt**-gruppen som bruker **PRE**-posteringsprofilen
- Salgsordrefaktura for en kunde i **Ansatt**-gruppen som bruker **GEN**-posteringsprofilen
- Salgsordrefaktura for en kunde i **Ansatt**-gruppen som bruker **PRE**-posteringsprofilen
- Kundebetalingsjournal for en kunde i **Ansatt**-gruppen som bruker **GEN**-posteringsprofilen
- Kundebetalingsjournal for en kunde i **Ansatt**-gruppen som bruker **PRE**-posteringsprofilen

Gjenta ett testscenario for hver kundegruppe i det forrige eksemplet, og gjenta hver gruppe med testscenarioer for hver ekstra transaksjonstype (for eksempel prosjektfakturaer og tjenestebehandling).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Avstemming av hovedbok mot underfinans

Hovedboken bør avstemmes mot underfinans hver periode. Mange moduler inneholder bruksklare rapporter som kan brukes til denne avstemmingen. Avhengig av dine lokale krav kan det imidlertid hende at du må utvikle egendefinerte rapporter eller utvide de eksisterende rapportene for å oppfylle rapporteringskravene.

Vi anbefaler at du simulerer en periodeavslutning og avstemmer hver av underhovedbøkene mot hovedboken før du går live. Vi anbefaler også at du simulerer en overgang av alle åpne saldoer og åpne transaksjoner før du går live innledningsvis. Som en del av denne prosessen bør du kjøre en fullstendig avstemming for å sikre at migrering av saldoer og åpne transaksjoner er i balanse med de eldre systemene, og at alle underhovedbøker er i balanse med hovedboken, før nye transaksjoner opprettes.
