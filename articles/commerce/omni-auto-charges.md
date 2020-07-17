---
title: Avanserte automatiske gebyrer for omnikanal
description: Dette emnet beskriver funksjoner for å håndtere flere ordregebyrer for handelskanalordrer ved hjelp av funksjoner for avanserte automatiske gebyrer.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: c397354ade1ac1d4f5f9bc0e6bb5d4be5a7ae9f3
ms.sourcegitcommit: f7294160d18f15cb762c24f2459b4f0887c37541
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/25/2020
ms.locfileid: "3505617"
---
# <a name="omni-channel-advanced-auto-charges"></a>Avanserte automatiske tillegg for omnikanal

[!include [banner](includes/banner.md)]

Dette emnet gir informasjon om konfigurasjon og distribusjon av funksjonene for avanserte automatiske gebyrer som er tilgjengelige i Dynamics 365 for Retail versjon 10.0.

Når funksjonene for avanserte automatiske gebyrer er aktivert, kan ordrer som opprettes i en støttet handelskanal (salgssted, telefonsenter og online), dra nytte av konfigurasjonene for [automatisk gebyrer](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) som er definert i ERP-programmet for både hode- og linjenivårelaterte gebyrer.

I versjoner før Retail versjon 10.0 er konfigurasjoner for [automatiske gebyrer](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services) bare tilgjengelige for ordrer som er opprettet i e-handels- og telefonsenterkanaler. I versjon 10.0 og senere kan ordrer opprettet på salgsstedet dra nytte av konfigurasjonene for automatiske gebyrer. På denne måten kan flere tillegg systematisk legges til salgstransaksjonene.

Ved bruk av versjoner før versjon 10.0 blir brukeren for salgsstedet bedt om å angi et fraktgebyr manuelt under opprettingen av en salgsstedstransaksjon av typen Send alle eller Valgt for forsendelse. Ettersom funksjonene for tilleggene i programmet brukes i forhold til hvordan gebyrene skrives til ordren, tilbys det ingen systematisk beregning. Beregningen er avhengig av brukerens inndata for å bestemme verdien på tillegget. Gebyrene kan bare legges til som en enkelt forsendelsesrelatert gebyrkode og kan ikke redigeres eller endres enkelt på salgsstedet etter at de er opprettet.

Bruken av manuelle ledetekster for å legge til forsendelseskostnader er fremdeles tilgjengelig i versjon 10.0 og nyere. Hvis en organisasjon ikke aktiverer parameteren **Avanserte automatiske gebyrer**, blir salgsstedsforespørslene om manuell registrering av gebyrer de samme.

Med funksjonen for avanserte automatiske gebyrer kan brukerne for salgsstedet ha systematiske beregninger for alle definerte tillegg basert på tabellene med oppsett for automatiske gebyrer. I tillegg vil brukere ha muligheten for å legge til eller redigere et ubegrenset antall tilleggskostnader og gebyrer i en salgstransaksjon for salgsstedet på hode- eller linjenivået (for hentesalg eller kundeordre).

## <a name="enabling-advanced-auto-charges"></a>Aktivere avanserte automatiske gebyrer

På siden **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Handelsparametere** går du til kategorien **Kundeordrer**. I hurtigfanen **Gebyrer** setter du **Bruk avanserte automatiske gebyrer** til **Ja**.

![Parameter for avanserte automatiske gebyrer](media/advancedchargesparameter.png)

Når avanserte automatiske gebyrer er aktivert, blir brukere ikke lenger bedt om å angi en forsendelseskostnad manuelt på salgsstedsterminalen når de oppretter en kundeordre av typen Send alle eller Valgt for forsendelse. Ordregebyrer for salgssted beregnes systematisk og legges til salgsstedstransaksjonen (hvis det finnes en tilsvarende tabell for automatiske gebyrer som samsvarer med kriteriet for ordren som opprettes). Brukere kan også legge til eller vedlikeholde hode- eller linjenivågebyrer manuelt via salgsstedsoperasjoner som nylig er lagt til, som kan legges til skjermoppsettene for salgsstedet.

Når avanserte automatiske gebyrer er aktivert, brukes ikke lenger eksisterende **Handelsparametere** for **Kode for forsendelseskostnader** og **Refundering av forsendelseskostnader**. Disse parameterne gjelder bare hvis parameteren **Bruk avanserte automatiske gebyrer** er satt til **Nei**.

Før du aktiverer denne funksjonen, må du passe på at du har testet og lært opp dine ansatte siden den aktiverte funksjonen tte vil endre forretningsprosessflyten for hvordan forsendelseskostnader eller andre gebyrer beregnes og legges til salgsordrer for salgsstedet. Pass på at du forstår virkningen prosessflyten har på opprettingen av transaksjoner fra salgssted. For telefonsenter- og e-handelsorder er virkningen av å aktivere avanserte automatiske gebyrer minimal. Telefonsenter- og e-handelsprogrammer vil fortsatt ha samme virkemåte som de har hatt tidligere knyttet til tabellene for automatiske gebyrer for å beregne ekstra ordregebyrer. Brukere av telefonsenterkanaler vil fortsatt ha muligheten til å redigere manuelt systemberegnede automatiske gebyrer på hode- eller linjenivå, eller legge til flere tillegg på hode- eller linjenivå manuelt.

## <a name="additional-pos-operations"></a>Flere salgsstedsoperasjoner

For at avanserte automatiske gebyrer skal fungere riktig i ditt salgsstedsprogrammiljø, er det lagt til nye salgsstedsoperasjoner. Disse operasjonene må legges til i [skjermoppsettene for salgssted](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) og distribueres til salgsstedsenhetene når du distribuerer avanserte automatiske gebyrer. Hvis disse operasjonene ikke legges til, kan ikke brukere behandle eller vedlikeholde tillegg i salgsstedstransaksjonene, og vil ikke ha noen måte å justere eller endre gebyrverdiene på som beregnes systematisk basert på konfigurasjoner for automatiske gebyrer. Som minimum anbefales det at du distribuerer **Behandle tillegg**-operasjonen til salgsstedsoppsettet.

De nye operasjonene er følgende:

- **142 - Administrer tillegg** – Bruk denne operasjonen for å la brukere på salgsstedet vise og redigere tillegg for salgsstedstransaksjonen som ble lagt til manuelt eller systematisk gjennom automatiske gebyrberegninger.
- **141 - Legg til hodegebyrer** – Bruk denne operasjonen for å gi brukeren mulighet til å manuelt legge til et tillegg på hodenivå i salgstransaksjoner på salgsstedet (og velge gebyrkoden som skal brukes).
- **140 - Legg til linjegebyrer** – Bruk denne operasjonen for å gi brukeren mulighet til å manuelt legge til et tillegg på linjenivå i salgstransaksjonslinjer på salgsstedet (og velge gebyrkoden som skal brukes).
- **143 - Beregn gebyrer på nytt** – Bruk denne operasjonen for å utføre en fullstendig ny beregning av gebyrene salgstransaksjonen. Tidligere automatiske gebyrer som er overskrevet av bruker, beregnes på nytt basert på den gjeldende handlekurvkonfigurasjonen.

Som med alle salgsstedsoperasjoner kan sikkerhet konfigureres slik at det kreves godkjenning fra leder før operasjonen kan utføres.

Det er viktig å være klar over at salgsstedsoperasjonene også kan legges til salgsstedoppsettet, selv om **Bruk avanserte automatiske gebyrer**-parameteren er deaktivert. I slike scenarioer vil organisasjoner likevel få fordeler med å kunne vise manuelt tillagte gebyrer og redigere dem ved hjelp av **Behandle gebyrer**-operasjonen. Brukere kan også bruke operasjonene **Legg til hodegebyrer** og **Legg til linjegebyrer** for salgsstedstransaksjoner, selv når **Bruk avanserte automatiske gebyrer**-parameteren er deaktivert. **Beregn gebyrer på nytt**-operasjonen har mindre funksjonalitet hvis den brukes når **Bruk avanserte automatiske gebyrer** er deaktivert. Ingenting vil bli beregnet på nytt i dette scenarioet, og gebyrer som legges til manuelt i transaksjonen, vil bare tilbakestilles til USD 0,00.

## <a name="use-case-examples"></a>Brukseksempler

I denne delen vises brukseksempler for å hjelpe deg med å forstå konfigurasjon og bruk av automatiske gebyrer og tillegg i forbindelse med kanalordrer. Disse eksemplene viser virkemåten til programmet når parameteren **Bruk avanserte automatiske gebyrer** er aktivert.

### <a name="auto-charges-header-charges-example"></a>Eksempel på automatiske gebyrer for hodetillegg

#### <a name="use-case-scenario"></a>Bruksscenario

En forhandler ønsker å legge til tillegg for frakt automatisk når transaksjoner opprettes i en handelskanal som krever forsendelse av varer til kunden. Forhandleren tilbyr to leveringsmåter: landtransport og fly. Hvis en kunde velger landtransportlevering og ordreverdien er mindre enn NOK 1000, vil forhandleren belaste kunden med et fraktgebyr på NOK 100. Hvis ordren er over NOK 1000 og kunden velger forsendelse på land, vil kunden ikke bli belastet med ekstra fraktgebyrer. Hvis kunden velger leveringsmåten for fly for alle ordrer, uavhengig av deres totale verdi, tilfaller det et fraktgebyr på NOK 200.

#### <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Dette scenariet krever konfigurasjon av to tabeller for automatiske gebyrer.

Gå til **Kunder \> Oppsett for tillegg \> Automatiske gebyrer**.

Konfigurer to ulike automatiske gebyrer på hodenivå. Konfigurer ett for «over land»-leveringsmåten og ett for «flyfrakt»-leveringsmåten. I dette scenariet konfigurerer du dem for bruk for «Alle kunder».

I linjedelen på siden **Automatiske gebyrer** for gebyrene for levering på land definerer du et gebyr som skal brukes for ordrer mellom NOK 0,10 og 1000, som NOK 100,00. Opprett en ny gebyrlinje for å angi at ordrer over NOK 1000,10 ikke har gebyrer.

![Eksempel på to tabeller for automatiske gebyrer](media/headerchargesexample.png)

I linjedelen i skjemaet for automatiske gebyrer for gebyrene for levering med fly definerer du et gebyr på NOK 200,00 som skal brukes for alle ordrer (mellom en verdi på NOK 0,10 og NOK 99 999 990).

Send endringene til Commerce Scale Unit / kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben **1040 distribusjonsplan**.

#### <a name="sales-processing-for-this-scenario"></a>Salgsbehandling for dette scenariet

Når konfigurasjonstrinnene ovenfor er fullført, og endringene er implementert i kanaldatabasen, vil kundeordrer eller salgstransaksjoner som er opprettet på salgsstedet, telefonsenteret eller e-handelskanalene som har angitt leveringsmåten land eller fly på hodenivå, bruke disse gebyrene og automatiske bruke dem på salget.

På dette tidspunktet vil gebyrene gjelde for alle salgstransaksjoner som opprettes i den juridiske enheten som bruker disse leveringsmåtene, siden det ikke finnes noen funksjon som kan angi at en konfigurasjon for automatiske gebyrer bare skal gjelde for en bestemt salgskanal.

For salgssteds- og e-handelsscenarier, fordi det er ikke noe klart definert «hode» i disse ordrene, gjelder bare hodenivågebyrer hvis alle salgslinjer i transaksjonen er satt til forsendelse med nøyaktig samme leveringsmåte. Hvis det er «blandede måter» for fullføring i transaksjonene som er opprettet på salgsstedet eller i e-handel, vurderes og brukes bare automatiske gebyrer på linjenivå.

I telefonsenterscenarier har brukeren kontroll over innstillingen for leveringsmåte i ordrehodet. Derfor brukes gebyrer på hodenivå for disse ordrene selv om noen av salgslinjene er konfigurert for å bruke en annen leveringsmåte. Gebyrer på hodenivå for telefonsenterordrer baseres alltid på leveringsmåten som er definert i ordrehodenivået for salgsordren.

### <a name="auto-charges-line-charges-example"></a>Eksempel på automatiske gebyrer for linjetillegg

#### <a name="use-case-scenario"></a>Bruksscenario 

En forhandler ønsker å legge til en tilleggsavgift for kunden for oppsettsgebyrer når kunden kjøper en bestemt modell av en datamaskin. Denne datamaskinen krever ekstra konfigurasjonshandlinger som ikke er valgfrie, og som forhandleren utfører for kunden. Forhandleren har informert kunder om at det er tilleggsgebyr for dette oppsettet. Forhandleren foretrekker å håndtere tilleggene som er knyttet til dette gebyret, separat fra produktsalgsprisen for regnskapsrapporteringsformål. Et oppsettsgebyr på NOK 199,90 skal belastes kunden når denne bestemte datamaskinen kjøpes i en handelskanal.

#### <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Dette scenariet krever konfigurasjon av én tabell for automatiske gebyrer på linjenivå.

Gå til **Kunder \> Oppsett for tillegg \> Automatiske gebyrer**.

Sett **Nivå**-rullegardinmenyen til **Linje**, og opprett en ny post for automatiske gebyrer for alle kunder og for det bestemte produktet eller produktgruppen der konfigurasjonsgebyret belastes.

![Eksempel på én tabell for automatiske gebyrer på linjenivå](media/linechargesexample.png)

Send prisene til Commerce Scale Unit / kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben **1040 distribusjonsplan**.

#### <a name="sales-processing-for-this-scenario"></a>Salgsbehandling for dette scenariet

Når konfigurasjonstrinnene ovenfor er fullført, og endringene er implementert i kanaldatabasen, vil kundeordrer eller salgstransaksjoner som er opprettet på salgsstedet, telefonsenteret eller e-handelskanalene som har denne varen i ordren, utløse et linjenivågebyr som legges til ordretotalen systematisk.

På dette tidspunktet vil gebyrene gjelde for alle salgslinjer som samsvarer med konfigurasjonen for automatiske gebyrer på linjenivå i den juridiske enheten, siden det ikke finnes noen funksjon for å konfigurere et automatisk gebyr på linjenivå som bare skal gjelde for en bestemt salgskanal.

### <a name="manual-header-charges-example"></a>Eksempel på manuelle hodetillegg

#### <a name="use-case-scenario-description"></a>Bruksscenariobeskrivelse

En forhandler gjør et unntak fra vanlige prosesser ved å tilby å en spesiell hjemmelevering av varer til kunder som bestiller varer i butikken. Forhandleren og kunden har blitt enige om at kunden skal betale et ekstra administrasjonsgebyr på NOK 250 for denne tjenesten. Ordremottakeren må legge til dette tilleggsgebyret i transaksjonen. Fordi gebyret er generelt og ikke knyttet til et enkelt produkt i ordren, benyttes et hodetillegg.

#### <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Kontroller at tilleggskoden som skal brukes i dette scenariet, er riktig konfigurert ved å gå til **Kunder \> Oppsett for tillegg \> Tillegg** for å definere en passende tilleggskode for scenariet.

![Eksempel på gebyrer](media/chargesexample.png)

Hvis tillegget skal betraktes som et forsendelsesrelatert tillegg for forsendelsesrelaterte rabatter og tilbud, setter du **Forsendelsesgebyr** for tilleggskoden til **Ja**. Hvis dette gebyret også kan refunderes systematisk under behandlingen av en returtransaksjon i salgsstedprogrammet, setter du **Refunderbar** til **Ja**. **Refunderbar**-flagget er bare tilgjengelig når **Bruk avanserte automatiske gebyrer**-parameteren er satt til **Ja**.

Send prisene til Commerce Scale Unit / kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben **1040 distribusjonsplan**.

**Legg til hodegebyrer**-operasjonen må konfigureres i [skjermoppsettet for salgssted](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) slik at en knapp som er tilgjengelig for brukeren fra salgsstedet, kan kalle denne operasjonen (operasjon 141). Endringene i skjermoppsettet må distribueres til handelsekanalen og via funksjonen for distribusjonsplan.

#### <a name="sales-processing-of-manual-header-charges"></a>Salgsbehandling av manuelle hodegebyrer

Hvis scenariet skal utføres i salgsstedsprogrammet, oppretter salgsstedsbrukeren salgstransaksjonen på vanlig måte, og legger til produktene og andre konfigurasjoner i salget. Før brukeren tar betaling, må brukeren utføre **Legg til hodetillegg**-operasjonen, som vil be brukeren om å velge en tilleggskode og angi tilleggsverdien. Når brukeren fullfører prosessen, vil tillegget legges til salgsordren som et hodenivåtillegg.

Denne prosessen kan brukes i telefonsenteret ved hjelp av den eksisterende **Tillegg**-funksjonen som finnes i **Selg**-kategorien på verktøylinjen. På siden **Vedlikehold tillegg** kan brukeren legge til en ny tilleggslinje i ordrehodet.

### <a name="manual-line-charges-example"></a>Eksempel på manuelle linjetillegg

#### <a name="use-case-scenario"></a>Bruksscenario

En kunde har bedt om at to av fem varer i salgsordren skal pakkes som gave. Forhandleren tilbyr denne tilleggstjenesten mot et gebyr på NOK 20 per vare. Ordremottakeren må legge til disse gebyrene for de bestemte varene som skal pakkes som gave.

#### <a name="setup-and-configuration"></a>Oppsett og konfigurasjon

Kontroller at tilleggskoden som skal brukes i dette scenariet, er riktig konfigurert ved å gå til **Kunder \> Oppsett for tillegg \> Tillegg** for å definere en passende tilleggskode for scenariet.

Hvis tillegget skal betraktes som et forsendelsesrelatert tillegg for forsendelsesrelaterte rabatter og tilbud, setter du **Forsendelsesgebyr** for tilleggskoden til **Ja**. Hvis gebyret også kan refunderes systematisk under behandlingen av en returtransaksjon i salgsstedprogrammet, setter du **Refunderbar** til **Ja**. **Refunderbar**-flagget er bare tilgjengelig når **Bruk avanserte automatiske gebyrer**-parameteren er satt til **Ja**.

Send prisene til Commerce Scale Unit / kanaldatabasen slik at salgsstedet kan bruke dem ved å kjøre jobben **1040 distribusjonsplan**.

**Legg til linjegebyrer**-operasjonen må konfigureres i [skjermoppsettet for salgssted](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) slik at en knapp som er tilgjengelig for brukeren fra salgsstedet, kan kalle denne operasjonen (operasjon 140). Endringene i skjermoppsettet må distribueres til handelsekanalen og via funksjonen for distribusjonsplan.

#### <a name="sales-processing-of-the-manual-line-charge"></a>Salgsbehandling av manuelle linjegebyrer

Hvis scenariet skal utføres i salgsstedsprogrammet, oppretter salgsstedsbrukeren salgstransaksjonen på vanlig måte, og legger til produktene og andre konfigurasjoner i salget. Før brukeren tar betaling, bør brukeren velge den bestemte linjen der gebyret skal gjelde, fra visningen for salgsstedsvareliste og utføre **Legg til linjegebyrer**-operasjonen. Brukeren blir bedt om å velge en tilleggskode og angi verdien for tillegget. Når brukeren fullfører prosessen, vil tillegget kobles til linjen og legges til ordretotalen som et linjenivåtillegg. Brukeren kan gjenta prosessen for å legge til flere linjegebyrer i andre varelinjer for transaksjonen hvis nødvendig.

Den samme fremgangsmåten kan brukes i telefonsenteret ved hjelp av funksjonen Vedlikehold tillegg under **Finans**-rullegardinmenyen i **Salgsordrelinjer**-delen på **Salgsordre**-siden. Når du velger dette alternativet, åpner **Vedlikehold tillegg**-siden der brukeren kan legge til en nytt linjebestemt tillegg for transaksjonen.

## <a name="additional-features"></a>Tilleggsfunksjoner

### <a name="editing-charges-on-a-pos-sales-transaction"></a>Redigere tillegg i en salgstransaksjon for salgssted

**Behandle tillegg**-operasjonen (142) skal legges til [skjermoppsettet for salgssted](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) slik at en bruker kan vise og redigere eller overstyre systemberegnede eller manuelt opprettede hode- eller linjenivåtillegg. Hvis operasjonen ikke legges til, vil ikke brukere kunne justere verdien på gebyrene i salgsstedstransaksjonen. De vil heller ikke kunne vise detaljene om tilleggene, for eksempel typen tilleggskode som er knyttet til tillegget.

På **Behandle tillegg**-siden i POS kan brukeren vise både hode- og linjenivåtilleggsdetaljer. Brukeren kan bruke funksjonen **Rediger** som er tilgjengelig på denne siden, for å endre beløpet som belastes på en bestemt gebyrlinje. Når en gebyrlinje blir overskrevet manuelt, blir den ikke systematisk beregnet på nytt med mindre brukeren starter operasjonen **Beregn gebyrer på nytt**.

Hvis **Overstyringsårsakskode for tillegg** er konfigurert på oppsettssiden for **Handelsparametere**, blir brukeren bedt om å oppgi en årsakskode når tilleggene er endret i salgsstedsprogrammet.

Hvis årsakskoder er registrert for overskrevne gebyrer, finnes det også en ny rapport hvor du kan se gjennom og revidere disse overstyringene. Rapporten finnes i **Retail og Commerce \> Forespørsler og rapporter \> Historikk for gebyroverstyring**.

### <a name="refunding-charges-on-a-pos-return-transaction"></a>Refundere tillegg i en returtransaksjon på salgsstedet

Hvis parameteren **Bruk avanserte automatiske gebyrer** er satt til **Ja**, er ikke den eksisterende handelsparameteren for **Refundering av forsendelseskostnader** lenger tilgjengelig. For å angi hvilke tillegg som skal refunderes systematisk til en kunde ved bruk av avanserte automatiske gebyrer, må du kontrollere at den tilknyttede gebyrkoden er konfigurert som **Refunderbar** på oppsettssiden for **Tilleggskode**. Kontroller at innstillingene er synkronisert til handelskanaldatabasene via distribusjonplanbehandlingen.

### <a name="refunding-charges-on-a-return-order-transaction"></a>Refundere tillegg i en returordretransaksjon

Tillegg blir ikke systematisk refundert til **Returordrer** som er opprettet i Commerce. Brukere må velge **Kopier gebyrer**-alternativet når de oppretter **returordren**. Hvis **Kopier gebyrer** ikke er merket av, blir ikke gebyrer fra den opprinnelige salgstransaksjonen automatisk refundert. Hvis **Kopier gebyrer** er valgt, blir alle gebyrer kopiert til returordren, og brukeren kan manuelt redigere eller fjerne tillegg som de ikke vil ha refundert. Returordreprosessen for telefonsentre godtar for øyeblikket ikke **Refunderbar**-flagget i **Tilleggskode**-oppsettet.

### <a name="configuring-pos-receipts-to-show-charges"></a>Konfigurere salgsstedskvitteringer for å vise tillegg

De følgende kvitteringselementene er lagt til på kvitteringslinjen og bunnteksten for å støtte funksjonen for avanserte automatiske gebyrer.

- **Forsendelseskostnader for linje** – Dette linjenivåelementet kan brukes til å oppsummere bestemt tilleggskoder som er brukt på salgslinjen. Bare tilleggskoder som er flagget som **Forsendelse**-tillegg på **Tilleggskode**-siden, vises her.
- **Andre tillegg for linje** – Dette linjenivåelementet kan brukes til å oppsummere ikke-forsendelsesbestemte tilleggskoder som er brukt på salgslinjen. Dette er tilleggskoder der **Forsendelse**-flagget på **Tilleggskode**-siden ikke er aktivert.
- **Detaljer for forsendelseskostnader for ordre** – Dette elementet på bunntekstnivå viser beskrivelsene av gebyrkodene som er brukt i ordren som er flagget som **Forsendelse**-tillegg på oppsettssiden for **Tilleggskode**.
- **Forsendelseskostnader for ordre** – Dette elementet på bunntekstnivå viser kroneverdien av kostnadene knyttet til forsendelsen.
- **Detaljer for andre kostnader for ordre** – Dette elementet på bunntekstnivå viser beskrivelsen av gebyrkodene som er brukt i ordren som ikke er flagget som forsendelsesrelaterte tillegg.
- **Andre kostnader for ordre** – Dette elementet på bunntekstnivå viser kroneverdien av andre kostnader som ikke er relatert til forsendelsen.

Det anbefales at organisasjonen også legger til fritekstfelt i kvitteringsbunnteksten, for å definere områdene der tillegg oppsummeres.

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>Hindre at tillegg blir beregnet før salgsstedsordren er fullført

Noen organisasjoner kan foretrekke å vente til brukeren er ferdig med å legge til alle salgslinjene i salgsstedstransaksjonen før tilleggene beregnes. Du kan unngå beregning av gebyrer etter hvert som varer legges til salgsstedstransaksjonen, ved å aktivere parameteren **Manuell tilleggsberegning** i **funksjonalitetsprofilen** som butikken bruker. Aktivering av denne parameteren krever at salgsstedsbrukeren bruker operasjonen **Beregne totaler** når de er ferdig med å legge til produktene i salgsstedstransaksjonen. **Beregne totaler**-operasjonen vil deretter utløse beregningen av automatiske gebyrer for ordrehodet eller -linjene etter behov.

### <a name="charges-override-reports"></a>Tillegg overstyrer rapporter

Hvis brukere overstyrer de beregnede kostnadene manuelt eller legger til et manuelt tillegg i transaksjonen, vil disse dataene være tilgjengelige for revisjon i rapporten **Historikk for gebyroverstyring**. Rapporten kan vises i **Retail og Commerce \> Forespørsler og rapporter \> Historikk for gebyroverstyring**. Det er viktig å være oppmerksom på at dataene som kreves for denne rapporten, importeres fra kanaldatabasen til HK via "P"-distribusjonsplanleggingsjobber. Informasjon om overstyringer som nettopp er utført på salgsstedet, er derfor kanskje ikke tilgjengelig umiddelbart i denne rapporten før denne jobben har lastet opp butikktransaksjonsdataene til HK.

## <a name="additional-resources"></a>Tilleggsressurser

[Aktivere og konfigurere automatiske avregninger etter kanal](auto-charges-by-channel.md)

[Fordele hodegebyrer til samsvarende salgslinjer](pro-rate-charges-matching-lines.md)

