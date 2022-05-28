---
title: Oversikt over budsjettkontroll
description: Dette emnet introduserer budsjettkontrollfunksjonen, og gir informasjon som hjelper deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.
author: panolte
ms.date: 03/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36ecacc621b4ecb8cc71e42b7a306c4494f625a
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711278"
---
# <a name="budget-control-overview"></a>Oversikt over budsjettkontroll

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dette emnet introduserer budsjettkontrollfunksjonen, og gir informasjon som hjelper deg med å konfigurere budsjettkontroll for å optimalisere administrasjon av organisasjonens finansressurser.

Budsjettkontroll støtter behandling av en organisasjons økonomiske ressurser ved hjelp av kontoplaner, arbeidsflyter, brukergrupper, kildedokumentene og journaler, konfigurerbar beregning av tilgjengelige midler, budsjettsykluser og terskelverdier. Når kontrollene er på plass, kan en organisasjon planlegge, måle, administrere og utarbeide prognoser for sine økonomiske ressursene i hele regnskapsåret. 

Når budsjetter er godkjent i systemet, kan du bruke budsjettplaner for å generere budsjettregisteroppføringer for å registrere utgiftsbudsjettet for en organisasjon. Du kan også opprette eller importere budsjettregisteroppføringer fra et tredjepartsprogram i stedet for å bruke funksjonaliteten for budsjettplanlegging. 

Utgifter kan registreres ved hjelp av hovedkontoer og finansdimensjoner. Du kan konfigurere kontroll over de totale utgiftsene for å oppfylle organisasjonens retningslinjer og krav, ved å gruppere kombinasjoner av finansdimensjoner og hovedkontoer. 

Diagrammet nedenfor viser budsjettkontrollenes plassering i fasene i en vanlig budsjettsyklus.

[![Vanlig budsjetteringsyklus.](./media/budgetingcycle-300x198.png)](./media/budgetingcycle.png) 

Du kan du konfigurere budsjettkontroll basert på flere faktorer:

- **Finansdimensjoner** – Hvilke finansdimensjoner trengs ved rapportering av budsjett og faktiske data, og hvilke finansdimensjoner trengs for å kontrollere budsjetter? Finnes det bestemte kombinasjoner av dimensjoner eller hovedkontoer som krever spesiell oppmerksomhet? Er det for eksempel krav om å spore budsjettet med faktiske data etter kostsenter og program? Krever reiseutgifter spesiell oppmerksomhet?
- **Tid** – Hvilke tidsrom (regnskapsperiode, regnskapsperioden hittil og så videre) må brukes til å evaluere tilgjengelige budsjettmidler?
- **Kildedokumenter** – Hvilke kildedokumenter må evalueres for budsjettkontroll? Skal dokumentene evalueres per linje eller per dokument?
- **Beregningen av tilgjengelige budsjettmidler** – Skal dokumenter som innkjøpsrekvisisjoner (forhåndsdisposisjoner) og bestillinger (disposisjoner) tas med i beregningen av tilgjengelige budsjettmidler? Skal dokumenter som er i utkaststatus tas med i beregningen?
- **Tillatelse for overstyring** – Hvem har tilgang til å overskrider det tilgjengelige budsjettet?

Budsjettkontroll er fullstendig integrert med programmet. Derfor kan du vurdere det tilgjengelige budsjettet for både innkjøp planlagte og faktiske innkjøp. Budsjettforespørsler og rapporter er tilgjengelig. Derfor kan brukere evaluere budsjettet i hele budsjettsyklusen og kan foreta nødvendige justeringer etter behov, i form av budsjettendringer eller overføringer. Budsjettansvarlig kan også eksportere budsjettet og faktiske data til Microsoft Excel for å analysere og beregne etter behov.

## <a name="configuring-budget-control"></a>Konfigurere budsjettkontroll

### <a name="budget-cycle-time-span"></a>Tidsrom for budsjettsyklus

Når grunnleggende budsjettering er konfigurert, kan du definere tidspunkt for start- og avslutningsperioder for budsjettering og budsjettkontroll på siden **Tidsrom for budsjettsyklus**. Budsjettsykluser tilsvarer ofte regnskapskalendere, men kan omfatte regnskapsår.

Neste trinn i konfigurasjonen utføres i de ulike kategoriene som åpnes fra siden **Budsjettkontrollkonfigurasjon**.

### <a name="define-parameters"></a>Definer parametere

Basert på finansdimensjonene som er aktivert for budsjettet, kan du bruke alle eller deler av finansdimensjonene til budsjettkontroll. 

Du kan også angi standard tidsintervall (for eksempel **Regnskapsår**, **Regnskapsår til dato**, **Regnskapsperiode** eller **Kvartalsvis**) for utførelse av budsjettkontroll i det tilknyttede tidsrommet for budsjettsyklus. Du kan også angi en standard budsjettetansvarlig og terskelen som brukes til å varsle brukere når terskelen er nådd. Verdiene i disse feltene brukes som standardverdier i alle nye budsjettkontrollregeler eller budsjettetgrupper som opprettes. Standardverdiene kan imidlertid endres for individuelle grupper eller regler. 

Hvordan budsjetter opprettes og registreres i budsjettregisteret bidrar til å fastsette tidsrommet som velges når du vurderer tilgjengelige budsjettmidler. Hvis det utvikler og brukes et årlige beregnet beløp for en dimensjonsverdikombinasjon, kan det være fornuftig å bruke et regnskapsår eller regnskapsår hittil i år. Hvis en organisasjon imidlertid oppretter budsjetter etter regnskapsperiode eller tilordner til regnskapsperioder og ønsker mer detaljert kontroll, bør det vurderes å bruke tidsperiodene regnskapsperiode hittil i år eller kvartalsvis. 

I tillegg spiller den en rolle i defineringen av konfigurasjonen hvordan organisasjonens kultur er knyttet til budsjettering og budsjettkontroll.

### <a name="over-budget-permissions"></a>Tillatelser for budsjettoverskridelse

I kategorien **Tillatelser for budsjettoverskridelse** kan du deretter angi brukergrupper. Du kan også angi om brukere som er medlemmer av en gruppe har tillatelse til å overskrider budsjettet. Du kan hindre brukere i å overskride budsjettet etter budsjetterskelen som ble angitt i den **Budsjettparametere** , eller du kan hindre dem i å overskride budsjettet etter en hvilken som helst beløp, uavhengig av terskelen. Disse tillatelsene bidra til å behandle de økonomiske ressursene avhengig av hvordan en organisasjon proaktivt styrer forbruket sitt. 

### <a name="budget-funds-available"></a>Budsjettmidler tilgjengelig

I kategorien **Tilgjengelige budsjettmidler** kan du deretter angi formelen som brukes til å beregne tilgjengelige budsjettmidler. Avhengig av hvor konservativt en organisasjon styrer de økonomiske ressursene sine eller bestemmelser eller bransjekrav, kan beregningen omfatte utkast eller dokumenter som ikke er bokførte. 

> [!NOTE]
> Hvis denne beregningen endres i løpet av en budsjettsyklus, vil ikke endringene ha innvirkning på dokumenter som allerede har bestått kontroller i budsjettkontrollen og er postert eller fullført. Ved hjelp av en funksjon med navnet **Bare spor beløp i beregning for tilgjengelige budsjettmidler** kan du endre hvilke data som spores i BudgetSourceTracking-tabellene. Når denne funksjonen er aktivert, lagres beløp bare hvis de er valgt for bruk i beregningen av tilgjengelige budsjettmidler. Hvis du vil ha mer informasjon, se [Budsjettmidler tilgjengelig](budget-funds-available.md).

### <a name="documents-and-journals"></a>Dokumenter og journaler

P fanen **Dokumenter og kladder** kan du deretter velge hvilke kildedokumenter og kladder som skal underlegges kontroller i budsjettkontrollen og om kontrollene utføres på linjeoppføringene eller på hele dokumentet. I tillegg inneholder den nye funksjonen **Forbedring av dokumentfiltrering for budsjettkontroll**, som er tilgjengelig fra Microsoft Dynamics 365 Finance, versjon 10.0.27, et spørringsbasert filteralternativ for hvert dokument som er inkludert i budsjettkontroll. Derfor kan du angi hvilke budsjettkontrolldokumenter som skal budsjetteres. På denne måten gjør funksjonen det bare mulig å kontrollere et delsett av en dokumenttype. Du kan for eksempel bare kontrollere bestillinger der **Pulje**-feltet er satt til **01**. En ny kolonne som legges til fanen **Dokumenter og journaler**, angir om det er definert en spørring for den valgte dokumenttypen. I tillegg kan du legge til, redigere eller slette filtrering ved hjelp av to nye knapper som legges til på verktøylinjen over dokumentrutenettet. 

Du bør samsvare de valgte kildedokumentene som er merket med avmerkingsboksene, for saldoer som er inkludert i beregningen av tilgjengelige budsjettmidler. Hvis du for eksempel har valgt **Budsjettreservasjoner for disposisjoner**, bør du velge alternativet **Bestillinger**. Når en budsjettkontroll utføres for beløpene og kontoene på en innkjøpslinje, blir budsjettkontrollkategorien som tilordnes reservasjonen, **Disposisjon**. Når en budsjettkontroll utføres for beløpene og kontoene på en innkjøpslinje, blir innkjøpsrekvisisjonen som tilordnes reservasjonen, **Forhåndsdisposisjon**. 

Hvis **Budsjettreservasjoner for disposisjoner** og/eller **Budsjettreservasjoner for forhåndsdisposisjon** er inkludert i beregningen av tilgjengelige budsjettmidler og må gjenspeiles via posteringer i økonomimodulen, må du aktivere disse valgene i **Prognoseregnskap**-gruppen på siden **Økonomiparametere**.

### <a name="assign-budget-models"></a>Tilordne budsjettmodeller

I kategorien **Tilordne budsjettmodeller** tilordner du deretter budsjettmodeller til budsjettsyklustidsrom som skal tas med i budsjettkontrollen.

### <a name="define-budget-control-rules"></a>Definer budsjettkontrollregler

I kategorien **Definer budsjettkontrollregler** må du deretter opprette spesifikke regler som er basert på finansdimensjoner som er aktivert for budsjettkontroll. Hvis det for eksempel er fokus basert på utgifter eller utvalg av utgifter for en avdeling, da kan du bruke innstillingene i denne kategorien til å definere og evaluere disse utgiftene. Du kan definere forskjellige terskler for hver budsjettkontrollregel. 

> [!Important]
> Budsjettkontroll aktiveres for alle hovedkontoer av typen **Resultat**, **Utgift**, **Inntekter, Balanse, Gjeld, Egenkapital** eller **Anleggsmiddel**. Hvis kategorien **Definer budsjettkontrollregler** inneholder en regel som har tomme kriterier, aktiveres budsjettkontroll for **alle** kombinasjonene av finansdimensjoner som omfatter hovedkontoer for disse typene. Pass derfor på at du oppretter budsjettkontrollregler som bare definerer områdene for kombinasjoner av finansdimensjoner der det er viktig å aktivere budsjettkontroll.

### <a name="select-main-accounts"></a>Velg hovedkontoer

Hvis **Hovedkonto** ikke er valgt som en budsjettkontrolldimensjon på siden **Definer parametere** , men spesifikke utgifter administreres, kan du velge disse utgiftene på kategorien **Velg hovedkontoer**. Hvis **Hovedkonto** er valgt som en budsjettkontrolldimensjon, er det ikke nødvendig med noen oppføringer.

### <a name="define-budget-groups"></a>Definer budsjettgrupper

I kategorien **Definer budsjettgrupper** kan du deretter også definere unike kombinasjoner av finansdimensjoner der budsjettressurser er gruppert for sekundære budsjettkontroll. Du kan opprette én enkelt post som inneholder hele organisasjonen, eller du kan definere flere grupper for å representere individuelle avdelinger eller kostsentre.

### <a name="define-message-levels"></a>Definer meldingsnivåer

Hvis budsjettkontrollvarsler skal undertrykkes for alle brukergrupper, kan du angi disse gruppene på siden **Definer meldingsnivåer**. Medlemmer av brukergrupper fortsetter å motta feilmeldinger når deoverskrider tilgjengelige budsjettmidler, basert på deres tillatelser for budsjettoverskridelse.

### <a name="activate-budget-control"></a>Aktiver budsjettkontroll

Etter at budsjettkontrollen er konfigurert, kan du slå den på og aktivere den i kategorien **Aktiver budsjettkontroll**. Utkastversjonen vil da bli effektiv.

> [!Important]
> Når budsjettkontrollen er aktivert og aktiv og etter at transaksjonene er postert, må den ikke deaktiveres midt i året. Aktiviteter registreres ikke for budsjettkontrollformål når budsjettkontroll er deaktivert, og budsjettkontroller blir ikke lenger utført. Dokumenter som allerede er bokført gjenspeiler derfor kanskje ikke riktig frigivende beløp eller saldoer i forespørsler og rapporter som er knyttet til budsjettkontroll. Disse omfatter statistikk for budsjettkontroll for en hvilken som helst nedstrømsflyt eller justering av dokumenter og journaler. 

Vær i tillegg oppmerksom på at transaksjoner, inkludert budsjettregisteroppføringer, som er postert før budsjettkontroll er aktivert, utføres det ikke budsjettkontroll for. Det er derfor lurt å aktivere budsjettkontroll i begynnelsen av den nye budsjettsyklusen. Pass på at budsjettregisteroppføringer som inneholder startsaldoer for budsjett for budsjettkontroll får budsjettsaldoene oppdatert etter at budsjettkontroll er aktivert. Et åpent dokument (for eksempel en bestilling) vil bli kontrollert for tilgjengelige budsjettmidler og får en budsjettreservasjon for budsjettkontroll når brukeren manuelt utløser budsjettkontroll i dokumentet.

## <a name="using-budget-control"></a>Bruke budsjettkontroll
Når budsjettkontroll er aktivert, får du budsjettkontrolladvarsel og feilmeldinger i dokumenter og journaler som er konfigurert for budsjettkontroll. Husk at du kan konfigurere budsjettkontroll slik at brukere blir varslet hvis de overskrider budsjettmidlene, men du kan fortsette å bekrefte eller posterer transaksjoner. Du kan vise detaljene for mislykkede budsjettkontroller på siden **Budsjettetkontrollfeil og advarsler**.

Fra denne siden kan brukere drille ned i siden **Statistikk for budsjettkontroll etter periode** for å vise budsjettdetaljer for tilgjengelighet og reserveringer for en valgt kombinasjon av budsjettkontrolldimensjon. Brukere kan også gå til siden **Statistikk for budsjettkontroll** for å vise budsjetttilgjengeligheten for alle kombinasjonene av finansdimensjoner som brukes i budsjettkontroll. 

Hvis budsjettkontroll er aktivert for bestillinger, kan budsjettansvarlig bruke arbeidsområdet **Finansbudsjetter og prognoser** for å gå gjennom køen av alle ubekreftede bestillinger som har advarsler og feil. Hvis det er konfigurert tillatelse for budsjettoverskridelse for budsjettansvarlig, kan bestillingene bekreftes direkte i arbeidsområdet.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
