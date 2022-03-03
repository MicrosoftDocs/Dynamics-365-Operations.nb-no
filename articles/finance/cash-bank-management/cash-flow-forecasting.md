---
title: Kontantstrømprognose
description: Dette emnet gir en oversikt over prosessen for kontantstrømprognose. Det forklarer også hvordan kontantstrømprognose er integrert med andre moduler i systemet.
author: panolte
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5a46946ff2c3569dab0ce8b53b3cddcf18318cbf
ms.sourcegitcommit: 465c84eb5cdc211692e2ae09b45d1400f9a315ee
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2022
ms.locfileid: "8314729"
---
# <a name="cash-flow-forecasting"></a>Kontantstrømprognose

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Du kan bruke verktøy for kontantstrømprognose til å analysere kommende kontantstrøm- og valutabehov, slik at kan du estimere firmaets fremtidige behov for kontanter. Hvis du vil ha en prognose over kontantstrømmen, må du utføre følgende oppgaver:

- Identifiser og vis alle likviditetskontoer. Likviditetskontoer er firmaets kontoer for kontanter eller likvide midler.
- Konfigurer virkemåten til prognoser for transaksjoner som påvirker likviditetskontoene i firmaet.

Når du har fullført disse oppgavene, kan du beregne og analysere prognoser for kontantstrømmen og kommende valutabehov.

## <a name="cash-flow-forecasting-integration"></a>Integrasjon av kontantstrømprognose

Kontantstrømprognose kan integreres med økonomi, leverandører, kunder, budsjettering og lagerstyring. Prognoseprosessen bruker transaksjonsinformasjon som er registrert i systemet, og beregningsprosessen lager prognose for forventet kontantinnvirkning for hver transaksjon. Følgende transaksjonstyper vurderes når kontantstrømmen beregnes:

- **Salgsordrer** – salgsordrer som ikke er fakturert ennå, og som resulterer i et fysisk eller økonomisk salg.
- **Fritekstfakturaer** – Fritekstfakturaer som ikke er postert ennå, og som resulterer i økonomisk salg. 
- **Bestillinger** – bestillinger som ikke er fakturert ennå, og som resulterer i et fysisk eller økonomisk innkjøp.
- **Kunder** – åpne kundetransaksjoner (fakturaer som ennå ikke er betalt).
- **Leverandører** – åpne leverandørtransaksjoner (fakturaer som ennå ikke er betalt).
- **Finanstransaksjoner** – transaksjoner der det er angitt at en fremtidig postering kommer til å finne sted.
- **Budsjettregisteroppføringer** – budsjettregisteroppføringer som er valgt for kontantstrømprognoser.
- **Behovsprognoser** – linjer for lagerprognosemodell som er valgt for kontantstrømprognoser.
- **Forsyningsprognoser** – linjer for lagerprognosemodell som er valgt for kontantstrømprognoser.
- **Ekstern datakilde** – Eksterne data som er angitt eller importert til kontantstrømprognoser ved hjelp av regnearkmaler.
- **Prosjektprognoser** – Prosjektstyring og regnskapsprognoser ved hjelp av prognosemodell.
- **Betalinger til skattemyndighetene i kontantstrøm** – Forutsette betalingsbeløp for skattemyndighetene og tidsmåling som resulterer i økonomiske betalinger. Aktiver funksjonen Betalinger til skattemyndighetene i kontantstrøm.

## <a name="configuration"></a>Konfigurasjon

Hvis du vil konfigurere prosessen for kontantstrømprognose, bruker du siden **Oppsett for kontantstrømprognose**. På denne siden kan du angi likviditetskontoene som skal spores, og standard prognosevirkemåte for hvert område.

### <a name="general-ledger"></a>Økonomimodul

Du må først definere likviditetskontoene som skal spores gjennom kontantstrømprognose. Disse likviditetskontoene er vanligvis hovedkontoer som er knyttet til bankkontoene som skal motta og utbetale kontanter. Velg hovedkontoene som skal tas med for prognose, i **Økonomimodul**-fanen på siden **Oppsett for kontantstrømprognose**. Hvis en bankkonto er knyttet til hovedkontoen på **Bankkonto**-siden, vises den i **Bankkonto**-feltet.

Du kan definere en avhengig kontantstrømprognose for en hovedkonto som inneholder transaksjoner som er direkte relatert til transaksjoner på en annen hovedkonto. Hver linje du legger til i delen **Avhengige kontoer**, oppretter et beløp for kontantstrømprognose på en avhengig hovedkonto. Dette beløpet er en prosentdel av kontantstrømbeløpene til den primære hovedkontoen du valgte.

Først setter du **Hovedkonto**-feltet til den primære hovedkontoen der transaksjoner forventes å finne sted først. Sett feltet **Avhengig hovedkonto** til kontoen som kommer til å bli påvirket av den første transaksjonen mot den primære hovedkontoen. Angi aktuelle verdier for de andre feltene på linjen. Du kan endre verdien i **Prosent**-feltet for å gjenspeile virkningen av den primære hovedkontoen på den avhengige hovedkontoen. Når det gjelder en salgs- eller innkjøpsprognose, velger du en **Betalingsbetingelser**-verdi som er vanlig for de fleste kunder eller leverandører. Sett **Posteringstype**-feltet til forventet posteringstype som er knyttet til kontantstrømprognosen.

### <a name="accounts-payable"></a>Leverandører

Du kan beregne prognosen for innkjøp ved hjelp av oppsettalternativene i **Leverandører**-fanen på siden **Oppsett for kontantstrømprognose**. Før du kan konfigurere kontantstrømprognose for leverandører, må du konfigurere betalingsbetingelser, leverandørgrupper og leverandørposteringsprofiler.

Du kan velge standard innkjøpsvirkemåte for kontantstrømprognose i delen **Standardverdier for innkjøpsprognose**. Tre felt avgjør tidspunktet for kontantinnvirkningen: **Tid mellom leveringsdato og fakturadato**, **Betalingsbetingelser** og **Tid mellom fakturaens forfallsdato og betalingsdato**. Prognosen bruker bare standardinnstillingen for **Betalingsbetingelser**-feltet hvis det ikke er angitt en verdi for transaksjonen. Bruk en betalingsbetingelse til å beskrive det vanligste antallet dager for hver del av prosessen.

Feltet **Likviditetskonto for betalinger** angir likviditetskontoen som brukes oftest for betalinger. Bruk feltet **Prosent av beløp som skal tildeles til kontantstrømprognose** til å angi om en prosentdel av beløp skal brukes i prognoser. La dette feltet stå tomt hvis hele transaksjonsbeløpene skal brukes i prognoser.

Du kan overstyre standardinnstillingen for feltet **Tid mellom fakturaens forfallsdato og betalingsdato** for bestemte leverandørgrupper. Prognosen bruker standardverdien fra delen **Standardverdier for innkjøpsprognose** med mindre en annen verdi er angitt for leverandørgruppen som er knyttet til leverandøren i transaksjonen. Hvis du vil overstyre standardverdien, velger du en leverandørgruppe og angir deretter den nye verdien for **Innkjøpstid**-feltet.

Du kan overstyre standardinnstillingen for **Likviditetskonto**-feltet for bestemte leverandørposteringsprofiler. Prognosen bruker standardverdien fra delen **Standardverdier for innkjøpsprognose** med mindre en annen likviditetskonto er angitt for posteringsprofilen som er knyttet til leverandøren i transaksjonen. Hvis du vil overstyre standardverdien, velger du en posteringsprofil og angir deretter likviditetskontoen som forventes å bli påvirket.

### <a name="accounts-receivable"></a>Kunder

Du kan beregne prognosen for salg ved hjelp av oppsettalternativene i **Kunder**-fanen på siden **Oppsett for kontantstrømprognose**. Før du kan konfigurere kontantstrømprognose for kunder, må du konfigurere betalingsbetingelser, kundegrupper og kundeposteringsprofiler.

Du kan velge standard salgsvirkemåte for kontantstrømprognose i delen **Standardverdier for salgsprognose**. Tre felt avgjør tidspunktet for kontantinnvirkningen: **Tid mellom forsendelsesdato og fakturadato**, **Betalingsbetingelser** og **Tid mellom fakturaens forfallsdato og betalingsdato**. Prognosen bruker bare standardinnstillingen for **Betalingsbetingelser**-feltet hvis det ikke er angitt en verdi for transaksjonen. Bruk en betalingsbetingelse til å beskrive det vanligste antallet dager for hver del av prosessen. 

Feltet **Likviditetskonto for betalinger** angir likviditetskontoen som brukes oftest for betalinger. Bruk feltet **Prosent av beløp som skal tildeles til kontantstrømprognose** til å angi om en prosentdel av beløp skal brukes i prognoser. La dette feltet stå tomt hvis hele transaksjonsbeløpene skal brukes i prognoser.

Du kan overstyre standardinnstillingen for feltet **Tid mellom fakturaens forfallsdato og betalingsdato** for bestemte kundegrupper. Prognosen bruker standardverdien fra delen **Standardverdier for salgsprognose** med mindre en annen verdi er angitt for kundegruppen som er knyttet til kunden i transaksjonen. Hvis du vil overstyre standardverdien, velger du en kundegruppe og angir deretter den nye verdien for **Salgstid**-feltet.

Du kan overstyre standardinnstillingen for **Likviditetskonto**-feltet for bestemte kundeposteringsprofiler. Prognosen bruker standardverdien fra delen **Standardverdier for salgsprognose** med mindre en annen likviditetskonto er angitt for posteringsprofilen som er knyttet til kunden i transaksjonen. Hvis du vil overstyre standardverdien, velger du en posteringsprofil og angir deretter likviditetskontoen som forventes å bli påvirket.

### <a name="budgeting"></a>Budsjettering

Budsjetter som opprettes fra budsjettmodeller, kan tas med i kontantstrømprognoser. Velg budsjettmodellene som skal tas med i prognosen, i **Budsjettering**-fanen på siden **Oppsett for kontantstrømprognose**. Nye budsjettregisteroppføringer tas som standard med i prognoser etter at budsjettmodellen er aktivert for kontantstrømprognose.

Budsjettregisteroppføringer kan inkluderes i kontantstrømprognosen enkeltvis ved tilpasning. Når du legger til kolonnen "Ta med i kontantstrømprognoser" på siden **Budsjettregisteroppføring**, overskrives innstillingene på siden **Oppsett for kontantstrømprognose** slik at den inkluderer en individuell budsjettregisteroppføring i prognosen.


### <a name="inventory-management"></a>Beholdningsstyring

Prognoser for lagerforsyning og -behov kan tas med i kontantstrømprognoser. Velg prognosemodellen som skal tas med i kontantstrømprognosen, i **Lagerstyring**-fanen på siden **Oppsett for kontantstrømprognose**. Inkludering i kontantstrømprognoser kan overskrives på individuelle forsynings- og behovsprognoselinjer.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Definere dimensjoner for kontantstrømprognoser
En ny fane på siden  **Oppsett for kontantstrømprognose**  lar deg styre hvilke finansdimensjoner som skal brukes i arbeidsområdet  **Kontantstrømprognose** . Denne fanen vises bare når funksjonen for kontantstrømprognose er aktivert.

I fanen **Dimensjoner** velger du dimensjoner som skal brukes til filtrering, fra listen over dimensjoner, og bruker piltastene til å flytte dem til høyre kolonne. Du kan bare velge to dimensjoner til filtrering av data for kontantstrømprognose. 

### <a name="setting-up-external-source"></a>Definering av ekstern kilde
Eksterne data kan angis i eller importeres til kontantstrømprognoser når Finance Insights er konfigurert. Før eksterne data legges inn eller importeres, må eksterne kilder defineres. Definer eksterne kontantstrømkategorier i kategorien **Ekstern kilde**. En kategori kan være **Utgående** eller **Innkommende**. **Likviditet** må velges som posteringstype. I rutenettet **Innstillinger for juridisk enhet** velger du de juridiske enhetene og de tilsvarende hovedkontoene som de eksterne kontantstrømkategoriene gjelder for.

Hvis du vil ha mer informasjon, kan du se [Eksterne data i kontantstrømprognoser](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Prosjektstyring og regnskap

I versjon 10.0.17 aktiverer en ny funksjon integrering med prosjektstyring og regnskap og kontantstrømprognoser. I arbeidsområdet **Funksjonsstyring** slår du på funksjonen **Prosjektprognose for kontantstrøm** for å inkludere prognoser for kostnader og inntekter i kontantstrømprognosen. I kategorien **Prosjektstyring og regnskap** på siden **Oppsett for kontantstrømprognose** velger du prosjekttypene og transaksjonstypene som skal tas med i kontantstrømprognosen. Deretter velger du prosjektprognosemodellen. En reduksjonstypeundermodell fungerer best. Likviditetskontoene som ble angitt i kundeoppsettet, brukes som standard likviditetskontoer. Derfor trenger du ikke angi standard likviditetskontoer når du definerer kontantstrømprognosen. En budsjettmodell kan også brukes, men bare én type kan velges på siden **Oppsett for kontantstrømprognose** for prosjektstyring og regnskap. En prognosemodell gir mest fleksibilitet når prosjektstyring, regnskap eller Project Operations brukes.

Når funksjonen for kontantstrømprosjektprognose er aktivert, kan kontantstrømprognosen vises for hvert prosjekt på **Alle prosjekter**-siden. Velg **Kontantstrømprognose** i **Prognose**-gruppen i **Plan**-fanen i handlingsruten. I arbeidsområdene for **Kontantstrømoversikt** (se delen [Rapportering](#reporting) senere i dette emnet) viser transaksjonstypen for prosjektprognose innflytene (prognoseinntekt for prosjekt) og utflytene (prognosekostnader for prosjekt). Beløpene kan bare inkluderes hvis feltet **Prosjektfase** i arbeidsområdene **Kontantstrømoversikt** er angitt til **Pågår**.

Prosjekttransaksjoner er fremdeles inkludert i kontantstrømprognosen på flere måter, uansett om funksjonen **Prosjektprognose for kontantstrøm** er aktivert. Posterte prosjektfakturaer tas med i prognosen som en del av åpne kundetransaksjoner. Prosjektstartede salgsordrer og bestillinger tas med i prognosen som åpne ordrer etter at de er registrert i systemet. Du kan også overføre prosjektprognoser til en finansbudsjettmodell. Denne finansbudsjettmodellen tas deretter med i kontantstrømprognosen som en del av budsjettregisteroppføringene. Hvis du har aktivert funksjonen **Prosjektprognose for kontantstrøm**, må du ikke overføre prosjektprognoser til en budsjettmodell i finans, fordi denne handlingen vil føre til at prosjektprognosene telles to ganger.

### <a name="sales-tax-authority-payments"></a>Betalinger til skattemyndighet 

Funksjonen for kontantstrøm for betalinger til skattemyndighet forutser kontantstrømeffekten av mva-betalinger. Den bruker ubetalte mva-transaksjoner, utligningsperioder for mva og betalingsbetingelsene for avgiftsperioden for å forutse datoen og beløpet for kontantstrømbetalinger. 

### <a name="calculation"></a>Beregning

Før du kan vise analyse for kontantstrømprognose, må du kjøre kontantstrømberegningen. Beregningsprosessen prosjekterer fremtidige kontantinnvirkninger for transaksjoner som er angitt.

Beregne kontantstrømprognosen ved hjelp av siden **Beregn kontantstrømprognoser**. Du kan beregne hele kontantstrømprognosen eller en trinnvis kontantstrømprognose. 

- Hvis du vil fjerne alle kontantstrømprognosetransaksjoner og beregne på nytt, setter du feltet **Beregningsmetode for kontantstrømprognose** til **Total**. Vi anbefaler at du bruker denne fremgangsmåten hvis du ikke har oppdatert kontantstrømprognosene på lenge. 
- Hvis du vil oppdatere eksisterende kontantstrøminformasjon for bare nye transaksjoner, setter du feltet **Beregningsmetode for kontantstrømprognose** til **Ny**. Siden viser datoen kontantstrømberegningen sist ble kjørt.

Du kan også bruke satsvis behandling for kontantstrømprognosen. For å bidra til å sørge for at prognoseanalysen oppdateres jevnlig, konfigurerer du en gjentakende partiprosess for beregning av kontantstrømprognose.

I versjon 10.0.13 ble det utgitt en forbedring av beregningsprosessen som bruker rammeverket for prosessautomatisering til å planlegge beregningsjobben for kontantstrøm. Dette muliggjøres ved hjelp av funksjonen **Automatisering av kontantstrømprognose** i arbeidsområdet **Funksjonsbehandling**. Når den er aktivert, velger du koblingen **Automatisering av kontantstrømprognose** for å vise den nye automatiseringssiden, der du kan planlegge beregningsprosessen for kontantstrøm. Hvis du vil opprette en ny tidsplan for kontantstrømprognose, velger du **Opprett ny prosessautomatisering** og velger **Automatisering av kontantstrømprognose** på rullegardinmenyen **Planltype**. Du må definere en tidsplan for hvert firma du oppdaterer kontantstrømprognosedata for.  Denne siden viser også hvilke automatiseringsjobber for kontantstrømprognose som venter, og når den siste jobben ble fullført.  

> [!NOTE] 
> Hvis eksisterende satsvise jobber allerede er planlagt for kontantstrømprognoser, vil du få en feilmelding, og du vil ikke kunne aktivere denne funksjonen. Eksisterende satsvise jobber må fjernes før du kan aktivere denne funksjonen. 

Hvis du vil ha mer informasjon, se [Prosessautomatisering](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

### <a name="reporting"></a>Rapportering

Etter at kontantstrømprognosen er beregnet, må du oppdatere den tilknyttede enhetsinformasjonen for analytisk rapportering. Velg målingen **LedgerCovLiquidityMeasurement-aggregat** på **Enhetslager**-siden, og klikk deretter på **Oppdater**.

Det er to arbeidsområder som inneholder kontantstrømprognosedata. Det ene arbeidsområdet har data for alle firmaer, og det andre arbeidsområdet har bare data for gjeldende firma.

Tilgang til arbeidsområdet for alle firmaer styres via plikten **Vis kontantstrøm for alle firmaarbeidsområder**. Arbeidsområdet **Kontantstrømoversikt – alle firmaer** er tilgjengelig for følgende roller:

- Administrerende direktør
- Økonomidirektør
- Økonomikontrollør

Tilgang til arbeidsområdet for gjeldende firma styres via plikten **Vis kontantstrøm for gjeldende firmaarbeidsområde**. Arbeidsområdet **Kontantstrømoversikt – gjeldende firma** er tilgjengelig for følgende roller:

- Regnskapsfører
- Regnskapssjef
- Regnskapsansvarlig
- Regnskapssjef leverandørreskontro
- Regnskapssjef kundereskontro

Arbeidsområdet **Kontantstrømoversikt – alle firmaer** viser analyse for kontantstrømprognose i systemvalutaen. Systemvalutaen og valutakurstypen for systemet som brukes for analysen, er definert på siden **Systemparametere**. Arbeidsområdet viser en oversikt over kontantstrømprognose og bankkontosaldoer for alle firmaer. Et diagram over kontant innflyt og utflyt gir en oversikt over fremtidige kontantbevegelser og -saldoer i systemvalutaen, sammen med detaljert informasjon om de anslåtte transaksjonene. De anslåtte valutasaldoene vises også.

Arbeidsområdet **Kontantstrømoversikt – gjeldende firma** viser analyse for kontantstrømprognose i firmaets definerte regnskapsvaluta. Regnskapsvalutaen som brukes for analysen, er definert på **Finans**-siden. Arbeidsområdet viser en oversikt over kontantstrømprognose og bankkontosaldoer for gjeldende firma. Et diagram over kontant innflyt og utflyt gir en oversikt over fremtidige kontantbevegelser og -saldoer i regnskapsvalutaen, sammen med detaljert informasjon om de anslåtte transaksjonene. De anslåtte valutasaldoene vises også.

Hvis du vil ha mer informasjon om analyse for kontantstrømprognose, kan du se [Power BI-innholdet Kontantstrømoversikt](Cash-Overview-Power-BI-content.md).

Du kan også vise kontantstrømprognosedata for bestemte kontoer, ordrer og varer på følgende sider:

- **Råbalanse**: Velg **Kontantstrømprognoser** for å vise fremtidige kontantstrømmer for den valgte hovedkontoen.
- **Alle salgsordrer**: Velg **Kontantstrømprognoser** i **Faktura**-fanen for å vise den anslåtte kontantinnvirkningen for den valgte salgsordren.
- **Alle bestillinger**: Velg **Kontantstrømprognoser** i **Faktura**-fanen for å vise den anslåtte kontantinnvirkningen for den valgte bestillingen.
- **Forsyningsprognose**: Velg **Kontantstrømprognoser** for å vise fremtidige kontantstrømmer som er knyttet til den valgte vareforsyningsprognosen.
- **Behovsprognose**: Velg **Kontantstrømprognoser** for å vise fremtidige kontantstrømmer som er knyttet til den valgte varebehovsprognosen.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
