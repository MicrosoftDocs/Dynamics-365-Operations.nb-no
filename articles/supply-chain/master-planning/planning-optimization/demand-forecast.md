---
title: Hovedplanlegging med behovsprognoser
description: Denne artikkelen forklarer hvordan du inkluderer behovsprognoser under hovedplanlegging.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 79a25d6fc5c809947b5b92a32cc00c9a3cc73202
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739790"
---
# <a name="master-planning-with-demand-forecasts"></a>Hovedplanlegging med behovsprognoser

[!include [banner](../../includes/banner.md)]

Du kan bruke en behovsprognose til å gjøre rede for forventet behov i hovedplanleggingen. Du kan opprette en behovsprognose manuelt, importere den eller generere den ved hjelp av funksjonen for behovsprognose i Microsoft Dynamics 365 Supply Chain Management. Hvis du vil ha mer informasjon om behovsprognose, kan du se [Oversikt over behovsprognose](../introduction-demand-forecasting.md).

> [!NOTE]
> Egen planlegging av prognoser støttes ikke med Planleggingsoptimalisering. Derfor har innstillingen **Gjeldende prognoseplan** på siden **Hovedplanleggingsparametere** ingen virkning når du bruker Planleggingsoptimalisering.

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a>Definer en hovedplan for å inkludere en behovsprognose

Følg denne fremgangsmåten for å konfigurere en hovedplan slik at den inneholder en behovsprognose.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende plan, eller opprett en ny plan.
1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Prognosemodell** – Velg prognosemodellen som skal brukes. Denne modellen blir tatt hensyn til når det genereres et forsyningsforslag for den gjeldende hovedplanen.
    - **Inkluder behovsprognose** – Sett dette alternativet til *Ja* for å inkludere behovsprognose i gjeldende hovedplan. Hvis du setter det til *Nei*, blir ikke transaksjoner for behovsprognose inkludert i hovedplanen.
    - **Metode som brukes til å redusere behovskrav** – Velg metoden som skal brukes til å redusere prognosebehovene. Hvis du vil ha mer informasjon, kan du se [Prognosereduksjonsnøkler](#reduction-keys) senere i denne artikkelen.

1. I **Tidshorisont i dager** kan du angi følgende felter for å angi perioden som behovsprognose skal tas med i:

    - **Prognoseplan** – Sett dette alternativet til *Ja* for å overstyre prognoseplanen som kommer fra de individuelle dekningsgruppene. Sett det til *Nei* for å bruke verdiene fra de individuelle dekningsgruppene for den gjeldende hovedplanen.
    - **Tidsperiode for prognose** – Hvis du angir **Prognoseplan** til *Ja*, angir du antall dager (fra dagens dato) som behovsprognose skal brukes på.

    > [!IMPORTANT]
    > Innstillingen **Prognoseplan** støttes ikke med Planleggingsoptimalisering.

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a>Definer en dekningsgruppe for å inkludere en behovsprognose

Følg denne fremgangsmåten for å konfigurere en hovedplan slik at den inneholder en dekningsgruppe.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Dekningsgrupper**.
1. Velg eksisterende dekningsgruppe, eller opprett en ny gruppe.
1. Angi følgende felter i hurtigfanen **Andre**:

    - **Tidshorisont for prognoseplan** – Angi antall dager (fra dagens dato) som behovsprognosen skal gjelde for. Denne verdien kan overstyres ved hjelp av **Prognoseplan**-alternativet i hovedplanen, som beskrevet i forrige del.
    - **Reduksjonsnøkkel** – Velg reduksjonsnøkkelen som skal brukes. Hvis du vil ha mer informasjon, kan du se delene [Opprett og definer en prognosereduksjonsnøkkel](#create-reduction-key) og [Bruk en reduksjonsnøkkel](#use-reduction-key) senere i denne artikkelen.
    - **Reduser prognose etter** – For hovedplaner der feltet **Metode som brukes til å redusere prognosebehov** er satt til *Transaksjoner – reduksjonsnøkkel* eller *Transaksjoner – dynamisk periode*, angir du hvilke transaksjoner som skal redusere prognosen. Velg én av følgende verdier:

        - **Alle transaksjoner** – Alle transaksjoner skal redusere prognosen.
        - **Ordrer** – Bare salgsordrer skal redusere prognosen.

        > [!NOTE]
        > Hvis du velger *Alle transaksjoner*, anses transaksjoner som har både etterspørsel og forsyning i de samme lagerdimensjonene, som nøytrale og ignoreres under prognosen. Hvis for eksempel planleggingsdimensjonen er satt til bare område, ikke lager, blir en overføringsordre mellom område 1, lager 11 og område 1, lager 13 ignorert og vil ikke redusere den gjenværende behovsprognose.

    - **Ta med konserninterne ordrer** – Sett dette alternativet til *Ja* hvis konserninterne ordrer skal inkluderes når prognosen reduseres. Hvis ikke setter du det til *Nei*.
    - **Ta med salgsprognose i behovsprognosen** – Angi om det skal tas med en prognose i den overordnede prognosen. Dette alternativet bestemmer hvordan faktisk etterspørsel reduserer det prognoseberegnede behovet. Du kan bruke den til å sikre at hovedplanleggingen dekker forsyningen av varene som kjøpes av bestemte kunder.

        - Sett dette alternativet til *Ja* for å inkludere en prognose i den overordnede prognosen. I dette tilfellet vil faktiske kundebehov redusere både kundeprognosen og den overordnede prognosen. Hovedplanlegging genererer planlagte ordrer for å dekke bare det totale prognoseantallet.
        - Sett dette alternativet til *Nei* hvis du ikke vil inkludere en prognose i den overordnede prognosen. I dette tilfellet vil faktisk kundebehov bare redusere kundeprognosen. Hovedplanlegging genererer planlagte ordrer for å dekke både det generelle prognoseantallet og prognosen for hver kundeantall.

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a>Prognosereduksjonsnøkler

Denne delen gir informasjon om de ulike metodene som brukes til å redusere behovene for prognose. Det inneholder eksempler på resultatene av hver metode. Det forklarer også hvordan du oppretter, definerer og bruker en prognosereduksjonsnøkkel. Noen metoder bruker en prognosereduksjonsnøkkel til å redusere prognosebehov.

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metoder som brukes til å redusere prognosebehov

Når du inkluderer en prognose i en hovedplan, kan du velge hvordan prognosekravene reduseres når faktisk etterspørsel er inkludert. Legg merke til at hovedplanleggingen ekskluderer tidligere prognosekrav, noe som betyr alle prognosekrav før dagens dato.

For å inkludere en prognose i en hovedplan og velge metoden som brukes til å redusere prognosebehove, går du til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**. I feltet **Prognosemodell** velger du en prognisemodell. I feltet **Metode som brukes til å redusere prognosebehov** velger du en metode. Følgende alternativer er tilgjengelige:

- Ingen
- Prosent – reduksjonsnøkkel
- Transaksjoner – reduksjonsnøkkel
- Transaksjoner – dynamisk periode

De følgende delene gir mer informasjon om hvert alternativ.

#### <a name="none"></a>Ingen

Hvis du velger **Ingen**, reduseres ikke prognosebehovet under hovedplanlegging. I så fall oppretter hovedplanleggingen planlagte ordrer for å angi prognosebehovet (prognosekrav). Disse planlagte ordrene vedlikeholder det foreslåtte antallet, uavhengig av andre typer behov. Hvis det for eksempel plasseres salgsordrer, vil hovedplanlegging opprette flere planlagte ordrer for å forsyne salgsordrene. Antallet for prognosebehovene reduseres ikke.

#### <a name="percent--reduction-key"></a>Prosent – reduksjonsnøkkel

Hvis du velger **Prosent - reduksjonsnøkkel**, reduseres prognosebehov i henhold til prosentene og periodene som er definert av reduksjonsnøkkelen. I dette tilfellet oppretter hovedplanleggingen planlagte ordrer der antallet beregnes som prognoseberegnet antall × reduksjonsnøkkel i hver periode. Hvis det finnes andre typer behov, oppretter hovedplanleggingen også planlagte ordrer for å levere dette behovet.

##### <a name="example-percent--reduction-key"></a>Eksempel: Prosent – reduksjonsnøkkel

Dette eksemplet viser hvordan en reduksjonsnøkkel reduserer behovene i behovsprognosen i henhold til prosentene og tidsperiodene som er definert av reduksjonsnøkkelen.

I dette eksemplet kan du inkludere følgende behovsprognose i en hovedplan.

| Måned    | Behovsprognose |
|----------|-----------------|
| Januar  | 1 000           |
| Februar | 1 000           |
| Mars    | 1 000           |
| April    | 1 000           |

På siden **Reduksjonsnøkler** definerer du følgende linjer.

| Vekslepenger | Enhet  | Prosent |
|--------|-------|---------|
| 1      | Måned | 100     |
| 2      | Måned | 75      |
| 3      | Måned | 50      |
| 4      | Måned | 25      |

Du tilordner reduksjonsnøkkelen til varens dekningsgruppe. På **Hovedplaner**-siden, i **Metode som brukes til å redusere prognosebehov** -feltet, velger du **Prosent - reduksjonsnøkkel**.

I dette tilfellet, hvis du kjører prognoseplanlegging 1. januar, forbrukes behovsprognosekravene i henhold til prosentene du definerer på **Reduksjonsnøkler**-siden. Følgende behovsantall overføres til hovedplanen.

| Måned                | Planlagt ordreantall | Beregning    |
|----------------------|------------------------|----------------|
| Januar              | 0                      | = 0 % × 1 000   |
| Februar             | 250                    | = 25 % × 1 000  |
| Mars                | 500                    | = 50 % × 1 000  |
| April                | 750                    | = 75 % × 1 000  |
| Mai til desember | 1 000                  | = 100 % × 1 000 |

#### <a name="transactions--reduction-key"></a>Transaksjoner – reduksjonsnøkkel

Hvis du angir **metoden som brukes til å redusere prognosebehov**-feltet til *Transaksjoner - reduksjonsnøkkel*, reduseres prognosekravene av kvalifiserte behovstransaksjoner som oppstår i periodene som er definert reduksjonsnøkkelen.

Det kvalifiserte behovet defineres av feltet **Reduser prognose etter**-feltet på **Dekningsgrupper**-siden. Hvis du setter feltet **Reduser prognose etter** til *Ordrer*, betraktes bare salgsordretransaksjoner som kvalifisert behov. Hvis du setter den til *Alle transaksjoner*, betraktes alle ikke-konserninterne avgangslagertransaksjoner som kvalifisert behov. Hvis konserninterne salgsordrer også skal vurderes som kvalifisert behov, angir du alternativet **Ta med konserninterne ordrer** til *Ja*.

Prognosereduksjon starter med den første (tidligste) behovsprognoseposten i reduksjonsnøkkelperioden. Hvis antallet kvalifiserte lagertransaksjoner er mer enn antallet behovsprognoselinjer i samme reduksjonsnøkkelperiode, vil saldoen i lagertransaksjonsantallet brukes til å redusere behovsprognoseantallet i forrige periode (hvis det er en prognose som ikke er brukt).

Hvis det ikke gjenstår en prognose som ikke er forbrukt, i den forrige reduksjonsnøkkelperioden, blir saldoen for lagertransaksjonsantall brukt til å redusere prognoseantallet i neste måned (hvis det finnes en ikke-brukt prognose).

Verdien til **Prosent**-feltet på reduksjonsnøkkellinjene vil ikke brukes når **Metode som brukes til å redusere prognosebehov**-feltet er satt til *Transaksjoner – reduksjonsnøkkel*. Bare datoene brukes til å definere reduksjonsnøkkelperioden.

> [!NOTE]
> Alle prognoser som posteres på eller før dagens dato, blir ignorert og vil ikke bli brukt til å opprette planlagte bestillinger. Hvis for eksempel behovsprognosen for måneden genereres 1. januar, og du kjører hovedplanlegging som omfatter behovsprognoser 2. januar, vil beregningen ignorere behovsprognoselinjen som er datert 1. januar.

##### <a name="example-transactions--reduction-key"></a>Eksempel: Transaksjoner – reduksjonsnøkkel

Dette eksemplet viser hvordan faktiske ordrer som skjer i periodene som er definert av reduksjonsnøkkelen, reduserer behovene i behovsprognosen.

[![Faktiske ordrer og prognose før hovedplanlegging kjøres.](media/forecast-reduction-keys-1-small.png)](media/forecast-reduction-keys-1.png)

Du velger for eksempel *Transaksjoner – reduksjonsnøkkel* i feltet **Metode som brukes til å redusere prognosebehov** -feltet på siden **Hovedplaner**.

Følgende behovsprognoselinjer finnes den 1. april.

| Dato     | Antall stykker som anslått |
|----------|-----------------------------|
| 5. april  | 100                         |
| 12. april | 100                         |
| 19. april | 100                         |
| 26. april | 100                         |
| 3. mai    | 100                         |
| 10. mai   | 100                         |
| 17. mai   | 100                         |

Følgende salgsordrelinjer finnes i april.

| Dato     | Antall stykker som er forespurt |
|----------|----------------------------|
| 27. april | 240                        |

[![Planlagt forsyning generert basert på aprilordrer.](media/forecast-reduction-keys-2-small.png)](media/forecast-reduction-keys-2.png)

Følgende behovsantall overføres til hovedplanen når hovedplanleggingen kjøres 1. april. Som du ser, ble prognosetransaksjonene for april redusert med behovsantallet på 240 i en serie, fra og med den første av disse transaksjonene.

| Dato     | Antall stykker som kreves |
|----------|---------------------------|
| 5. april  | 0                         |
| 12. april | 0                         |
| 19. april | 60                        |
| 26. april | 100                       |
| 27. april | 240                       |
| 3. mai    | 100                       |
| 10. mai   | 100                       |
| 17. mai   | 100                       |

Anta nå at nye ordrer ble importert for maiperioden.

Følgende salgsordrelinjer finnes i mai.

| Dato   | Antall stykker som er forespurt |
|--------|----------------------------|
| 4. mai  | 80                         |
| 11. mai | 130                        |

[![Planlagt forsyning generert basert på april- og mai-ordrer.](media/forecast-reduction-keys-3-small.png)](media/forecast-reduction-keys-3.png)

Følgende behovsantall overføres til hovedplanen når hovedplanleggingen kjøres 1. april. Som du ser, ble prognosetransaksjonene for april redusert med behovsantallet på 240 i en serie, fra og med den første av disse transaksjonene. I mai ble imidlertid prognosetransaksjonene redusert med totalt 210, fra og med den første behovsprognosetransaksjonen i mai. Totalene per periode beholdes imidlertid (400 i april og 300 i mai).

| Dato     | Antall stykker som kreves |
|----------|---------------------------|
| 5. april  | 0                         |
| 12. april | 0                         |
| 19. april | 60                        |
| 26. april | 100                       |
| 27. april | 240                       |
| 3. mai    | 0                         |
| 4. mai    | 80                        |
| 10. mai   | 0                         |
| 11. mai   | 130                       |
| 17. mai   | 90                        |

#### <a name="transactions--dynamic-period"></a>Transaksjoner – dynamisk periode

Hvis du velger **Transaksjoner – dynamisk periode**, reduseres prognosekravene med de faktiske ordretransaksjonene som forekommer i løpet av perioden som er dynamisk. Den dynamiske perioden dekker gjeldende prognosedatoer og slutter ved starten av neste prognose. I så fall oppretter hovedplanleggingen planlagte ordrer for å angi prognosebehovet (prognosekrav). Men når faktiske ordretransaksjoner plasseres, reduseres prognosebehovene. De faktiske transaksjonene forbruker deler av de prognoseberegnede behovene.

Når dette alternativet brukes, skjer følgende:

- Reduksjonsnøkler kreves eller brukes ikke. 
- Hvis prognosen reduseres fullstendig, blir behovene i prognosen for nåværende prognose 0 (null).
- Hvis det ikke er noen fremtidig prognose, reduseres behovene i prognosen fra den siste prognosen som ble angitt.
- Horisonter er inkludert i beregningen av prognosereduksjon.
- Positive dager er inkludert i beregningen av prognosereduksjon.
- Hvis faktiske ordretransaksjoner overskrider de prognoseberegnede kravene, videresendes ikke de gjenværende transaksjonene til neste prognoseperiode.

##### <a name="example-1-transactions--dynamic-period"></a>Eksempel 1: Transaksjoner – dynamisk periode

Her er et enkelt eksempel som viser hvordan **Transaksjoner – dynamisk periode**-metoden fungerer.

I dette eksemplet kan du inkludere følgende behovsprognose i en hovedplan.

| Dato       | Behovsprognose |
|------------|-----------------|
| 1. januar  | 1 000           |
| 1. februar | 1 000             |

Du kan også opprette følgende salgsordrer:

| Dato        | Salgsordreantall |
|-------------|----------------------|
| 15. januar  | 200                  |
| 15. februar | 400                  |

I dette tilfellet blir følgende planlagte ordrer opprettet:

| Behovsprognosedato | Antall | Forklaring                           |
|--------------------- |----------|---------------------------------------|
| 1. januar            | 800      | Prognosebehov (= 1 000 − 200) |
| 15. januar           | 200      | Salgsordrebehov             |
| 1. februar           | 600      | Prognosebehov (= 1 000 − 400) |
| 15. februar          | 400      | Salgsordrebehov             |

##### <a name="example-2-transactions--dynamic-period"></a>Eksempel 2: Transaksjoner – dynamisk periode

I de fleste tilfeller er systemer satt opp slik at transaksjoner reduserer behovsprognose i bestemte prognoseperioder: uker, måneder og så videre. Disse er definert i reduksjonsnøkkelen. Tiden mellom to behovsprognoselinjer kan imidlertid også *angi* en periode.

Du kan for eksempel opprette en behovsprognose for følgende datoer og antall:

| Dato       | Behovsprognose |
|------------|-----------------|
| 1. januar  | 1 000           |
| 5. januar  | 500             |
| 12. januar | 1 000           |

Legg merke til at i denne prognosen er det ikke en tydelig periode mellom prognosedatoene. Mellom første og andre dato er det et tidsintervall på 4 dager, og mellom andre og tredje dato er det et intervall på sju dager. Disse intervallene er dynamiske perioder.

Du kan også opprette følgende salgsordrelinjer:

| Dato                             | Salgsordreantall |
|----------------------------------|----------------------|
| 15. desember i fjor | 500                  |
| 3. januar                        | 100                  |
| 10. januar                       | 200                  |

I dette tilfellet reduseres prognosen på følgende måte:

- Fordi den første salgsordren ikke er innenfor noen periode, reduserer den ingen prognoser.
- Fordi den andre salgsordren er mellom 1. og 5. januar, reduserer den prognosen for 1. januar med 100.
- Fordi den tredje salgsordren er mellom 5. og 12. januar, reduserer den prognosen for 5. januar med 200.

Derfor opprettes følgende planlagte ordrer:

| Behovsprognosedato             | Antall | Forklaring                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| 15. desember i fjor | 500      | Salgsordrebehov                                            |
| 1. januar                        | 900      | Prognosebehovsperiode 1. januar til 5. januar (= 1 000 – 100) |
| 3. januar                        | 100      | Salgsordrebehov                                            |
| 5. januar                        | 300      | Prognosebehovsperiode 5. januar til 10. januar (= 500 – 200)  |
| 12. januar                       | 1 000    | Prognosebehovsperiode 12. januar til slutten                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a>Opprette og definere en prognosereduksjonsnøkkel

En prognosereduksjonsnøkkel brukes i metodene **Transaksjoner – reduksjonsnøkkel** og **Prosent – reduksjonsnøkkel** for å redusere prognosebehovene. Følg denne fremgangsmåten for å opprette og definere en reduksjonsnøkkel.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Reduksjonsnøkler**.
2. Velg **Ny** for å opprette en reduksjonsnøkkel.
3. I **Reduksjonsnøkkel**-feltet skriver du inn en unik identifikator for prognosereduksjonsnøkkelen. Angi deretter et navn i **Navn**-feltet. 
4. Definer periodene og reduksjonsnøkkelprosenten i hver periode:

    - **Gyldighetsdato**-feltet angir datoen når opprettelse av periodene starter. Når **Bruk gyldig dato**-alternativet er satt til **Ja**, starter periodene på gyldighetsdatoen. Når det er satt til **Nei**, starter periodene på datoen hovedplanlegging kjøres.
    - Definer periodene prognosereduksjonen skal utføres.
    - For en bestemt periode angir du prosentene som prognosebehovene skal reduseres med. Du kan angi positive verdier for å redusere krav eller negative verdier for å øke krav.

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a>Bruke en reduksjonsnøkkel

En prognosereduksjonsnøkkel må tilordnes til en dekningsgruppe for varen. Følg denne fremgangsmåten hvis du vil tilordne en reduksjonsnøkkel til varens dekningsgruppe.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**.
2. På **Andre**-hurtigfanen i feltet **Reduksjonsnøkkel** velger reduksjonsnøkkelen som skal tilordnes dekningsgruppen. Reduksjonsnøkkelen gjelder deretter for alle varer som tilhører en dekningsgruppe.
3. Hvis du vil bruke en reduksjonsnøkkel for å beregne prognosereduksjon under hovedplanlegging, må du definere denne innstillingen i oppsettet av prognoseplanen eller hovedplanen. Gå til ett av følgende steder:

    - **Hovedplanlegging \> Oppsett \> Planer \> Prognoseplaner**
    - **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**

4. På siden **Prognoseplaner** eller **Hovedplaner**, i **Generelt**-hurtigfanen i feltet **Metode som brukes til å redusere prognosebehov**, velger du enten **Prosent – reduksjonsnøkkel** eller **Transaksjoner – reduksjonsnøkkel**.

### <a name="reduce-a-forecast-by-transactions"></a>Redusere en prognose etter transaksjoner

Når du velger **Transaksjoner – reduksjonsnøkkel** eller **Transaksjoner – dynamisk periode** som metode for å redusere prognosebehov, kan du angi hvilke transaksjoner som reduserer prognosen. På siden **Dekningsgrupper**, i **Andre**-hurtigfanen i feltet **Reduser prognose etter**, velger du **Alle transaksjoner** hvis alle transaksjoner skal redusere prognosen, eller **Ordrer** hvis bare salgsordrer skal redusere prognosen.

## <a name="forecast-models-and-submodels"></a>Prognosemodeller og undermodeller

Denne delen beskriver hvordan du oppretter prognosemodeller og hvordan du kombinerer flere prognosemodeller ved å definere undermodeller.

En *prognosemodell* gir navn til og identifiserer en bestemt prognose. Når du har opprettet prognosemodellen, kan du legge til prognoselinjer i den. Hvis du vil legge til prognoselinjer for flere varer, bruker du siden **Behovsprognoselinjer**. Hvis du vil legge til prognoselinjer for en bestemt valgt vare, bruker du siden **Frigitte produkter**.

En prognosemodell kan omfatte prognoser fra andre prognosemodeller. Hvis du vil oppnå dette resultatet, legger du til andre prognosemodeller som *undermodeller* for en overordnet prognosemodell. Du må opprette hver relevante modell før du kan legge den til som undermodell for en overordnet prognosemodell.

Resultatstrukturen gir deg en kraftig måte å kontrollere prognoser på, fordi den lar deg kombinere (samle) inndataene fra flere individuelle prognoser. Derfor er det enkelt å kombinere prognoser for simuleringer fra et planleggingspunkt. Du kan for eksempel definere en simulering som er basert på kombinasjonen av en vanlig prognose med prognosen for en vårkampanje.

### <a name="submodel-levels"></a>Undermodellnivåer

Det er ingen begrensninger på antall undermodeller som kan legges til en overordnet prognosemodell. Strukturen kan imidlertid bare være ett nivå lavt. Med andre ord kan ikke en prognosemodell som er undermodell for en annen prognosemodell, ha sine egne undermodeller. Når du legger til undermodeller i en prognosemodell, kontrollerer systemet om prognosemodellen allerede er en undermodell av en annen prognosemodell.

Hvis hovedplanleggingen finner en undermodell som har sine egne undermodeller, får du en feilmelding.

#### <a name="submodel-levels-example"></a>Eksempel på undermodellnivåer

Prognosemodell A har prognosemodell B som undermodell. Derfor kan ikke prognosemodell B ha sine egne undermodeller. Hvis du prøver å legge til en undermodell i prognosemodell B, får du følgende feilmelding: Prognosemodell B er en undermodell for modell A.

### <a name="aggregating-forecasts-across-forecast-models"></a>Samling av prognoser på tvers av prognosemodeller

Prognoselinjer som forekommer på samme dag, vil bli aggregert over prognosemodellen og dens undermodeller.

#### <a name="aggregation-example"></a>Eksempel på samling

Prognosemodell A har prognosemodell B og C som undermodeller.

- Prognosemodell A omfatter en etterspørselsprognose for 2 stykker (stk) den 15. juni.
- Prognosemodell B omfatter en etterspørselsprognose for 3 stk den 15. juni.
- Prognosemodell C omfatter en etterspørselsprognose for 4 stk den 15. juni.

Den resulterende behovsprognosen vil være ett enkelt behov for 9 stk (2 + 3 + 4) den 15. juni.

> [!NOTE]
> Hver undermodell bruker egne parametere, og ikke parameterne for den overordnede prognosemodellen.

### <a name="create-a-forecast-model"></a>Opprette en prognosemodell

Hvis du vil opprette en prognosemodell, gjør du følgende.

1. Gå til **Hovedplanlegging \> Oppsett \> Behovsprognose \> Prognosemodeller**.
1. Velg **Ny** i handlingsruten.
1. Angi følgende felt for den nye prognosemodellen:

    - **Modell** – Angi en unik identifikator for modellen.
    - **Navn** – Angi et beskrivende navn for modellen.
    - **Stoppet** – Vanligvis bør du sette dette alternativet til *Nei*. Sett det til *Ja* bare hvis du vil hindre redigering av alle prognoselinjer som er tilordnet modellen.

    > [!NOTE]
    > Feltet **Ta med i kontantstrømprognoser** og feltene i hurtigfanen **Prosjekt** er ikke knyttet til hovedplanlegging. Derfor kan du ignorere dem i denne sammenhengen. Du må bare ta hensyn til dem når du arbeider med prognoser for modulen **Prosjektstyring og regnskap**.

### <a name="assign-submodels-to-a-forecast-model"></a>Tilordne undermodeller til en prognosemodell

Hvis du vil tilordne undermodeller til en prognosemodell, gjør du følgende.

1. Gå til **Lagerstyring \> Oppsett \> Prognose \> Prognosemodeller**.
1. I listen velger du prognosemodellen du vil definere en undermodell for.
1. I hurtigfanen **Undermodell** velger du **Legg til** for å legge til en rad i rutenettet.
1. I den nye raden angir du følgende felter:

    - **Undermodell** – Velg prognosemodellen som skal legges til som undermodell. Denne prognosemodellen må allerede finnes, og den må ikke ha noen egne undermodeller.
    - **Navn** – Angi et beskrivende navn for undermodellen. Dette navnet kan for eksempel angi undermodellens relasjon til den overordnede prognosemodellen.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

