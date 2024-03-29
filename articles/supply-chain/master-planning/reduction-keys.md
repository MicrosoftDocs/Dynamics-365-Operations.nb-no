---
title: Prognosereduksjonsnøkler
description: Denne artikkelen inneholder eksempler som viser hvordan du definerer en reduksjonsnøkkel. Den inneholder informasjon om de ulike innstillingene for reduksjonsnøkler for og resultatene av hver. Du kan bruke en reduksjonsnøkkel til å definere hvordan du kan redusere prognosebehov.
author: t-benebo
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0efd7245d100730622e9862554f484ed6b17d1ed
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739931"
---
# <a name="forecast-reduction-keys"></a>Prognosereduksjonsnøkler

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om de ulike metodene som brukes til å redusere behovene for prognose. Det inneholder eksempler på resultatene av hver metode. Det forklarer også hvordan du oppretter, definerer og bruker en prognosereduksjonsnøkkel. Noen metoder bruker en prognosereduksjonsnøkkel til å redusere prognosebehov.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Metoder som brukes til å redusere prognosebehov

Når du inkluderer en prognose i en hovedplan, kan du velge hvordan prognosekravene reduseres når faktisk etterspørsel er inkludert. Legg merke til at hovedplanleggingen ekskluderer tidligere prognosekrav, noe som betyr alle prognosekrav før dagens dato.

For å inkludere en prognose i en hovedplan og velge metoden som brukes til å redusere prognosebehove, går du til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**. I feltet **Prognosemodell** velger du en prognisemodell. I feltet **Metode som brukes til å redusere prognosebehov** velger du en metode. Følgende alternativer er tilgjengelige:

- Ingen
- Prosent – reduksjonsnøkkel
- Transaksjoner – reduksjonsnøkkel
- Transaksjoner – dynamisk periode

De følgende delene gir mer informasjon om hvert alternativ.

### <a name="none"></a>Ingen

Hvis du velger **Ingen**, reduseres ikke prognosebehovet under hovedplanlegging. I så fall oppretter hovedplanleggingen planlagte ordrer for å angi prognosebehovet (prognosekrav). Disse planlagte ordrene vedlikeholder det foreslåtte antallet, uavhengig av andre typer behov. Hvis det for eksempel plasseres salgsordrer, vil hovedplanlegging opprette flere planlagte ordrer for å forsyne salgsordrene. Antallet for prognosebehovene reduseres ikke.

### <a name="percent--reduction-key"></a>Prosent – reduksjonsnøkkel

Hvis du velger **Prosent - reduksjonsnøkkel**, reduseres prognosebehov i henhold til prosentene og periodene som er definert av reduksjonsnøkkelen. I dette tilfellet oppretter hovedplanleggingen planlagte ordrer der antallet beregnes som prognoseberegnet antall × reduksjonsnøkkel i hver periode. Hvis det finnes andre typer behov, oppretter hovedplanleggingen også planlagte ordrer for å levere dette behovet.

#### <a name="example-percent--reduction-key"></a>Eksempel: Prosent – reduksjonsnøkkel

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

### <a name="transactions--reduction-key"></a>Transaksjoner – reduksjonsnøkkel

Hvis du angir **metoden som brukes til å redusere prognosebehov**-feltet til *Transaksjoner - reduksjonsnøkkel*, reduseres prognosekravene av kvalifiserte behovstransaksjoner som oppstår i periodene som er definert reduksjonsnøkkelen.

Det kvalifiserte behovet defineres av feltet **Reduser prognose etter**-feltet på **Dekningsgrupper**-siden. Hvis du setter feltet **Reduser prognose etter** til *Ordrer*, betraktes bare salgsordretransaksjoner som kvalifisert behov. Hvis du setter den til *Alle transaksjoner*, betraktes alle ikke-konserninterne avgangslagertransaksjoner som kvalifisert behov. Hvis konserninterne salgsordrer også skal vurderes som kvalifisert behov, angir du alternativet **Ta med konserninterne ordrer** til *Ja*.

Prognosereduksjon starter med den første (tidligste) behovsprognoseposten i reduksjonsnøkkelperioden. Hvis antallet kvalifiserte lagertransaksjoner er mer enn antallet behovsprognoselinjer i samme reduksjonsnøkkelperiode, vil saldoen i lagertransaksjonsantallet brukes til å redusere behovsprognoseantallet i forrige periode (hvis det er en prognose som ikke er brukt).

Hvis det ikke gjenstår en prognose som ikke er forbrukt, i den forrige reduksjonsnøkkelperioden, blir saldoen for lagertransaksjonsantall brukt til å redusere prognoseantallet i neste måned (hvis det finnes en ikke-brukt prognose).

Verdien til **Prosent**-feltet på reduksjonsnøkkellinjene vil ikke brukes når **Metode som brukes til å redusere prognosebehov**-feltet er satt til *Transaksjoner – reduksjonsnøkkel*. Bare datoene brukes til å definere reduksjonsnøkkelperioden.

> [!NOTE]
> Alle prognoser som posteres på eller før dagens dato, blir ignorert og vil ikke bli brukt til å opprette planlagte bestillinger. Hvis for eksempel behovsprognosen for måneden genereres 1. januar, og du kjører hovedplanlegging som omfatter behovsprognoser 2. januar, vil beregningen ignorere behovsprognoselinjen som er datert 1. januar.

#### <a name="example-transactions--reduction-key"></a>Eksempel: Transaksjoner – reduksjonsnøkkel

Dette eksemplet viser hvordan faktiske ordrer som skjer i periodene som er definert av reduksjonsnøkkelen, reduserer behovene i behovsprognosen.

Du velger for eksempel **Transaksjoner – reduksjonsnøkkel** i feltet **Metode som brukes til å redusere prognosebehov** -feltet på siden **Hovedplaner**.

Følgende salgsordrer finnes den 1. januar.

| Måned    | Antall stykker som er bestilt |
|----------|--------------------------|
| Januar  | 956                      |
| Februar | 1,176                    |
| Mars    | 451                      |
| April    | 119                      |

Hvis du bruker den samme behovsprognosen på 1 000 stykker per måned som ble brukt i forrige eksempel, overføres følgende behovsantall til hovedplanen:

| Måned                | Antall stykker som kreves |
|----------------------|---------------------------|
| Januar              | 44                        |
| Februar             | 0                         |
| Mars                | 549                       |
| April                | 881                       |
| Mai til desember | 1 000                     |

### <a name="transactions--dynamic-period"></a>Transaksjoner – dynamisk periode

Hvis du velger **Transaksjoner – dynamisk periode**, reduseres prognosekravene med de faktiske ordretransaksjonene som forekommer i løpet av perioden som er dynamisk. Den dynamiske perioden dekker gjeldende prognosedatoer og slutter ved starten av neste prognose. I så fall oppretter hovedplanleggingen planlagte ordrer for å angi prognosebehovet (prognosekrav). Men når faktiske ordretransaksjoner plasseres, reduseres prognosebehovene. De faktiske transaksjonene forbruker deler av de prognoseberegnede behovene.

Når dette alternativet brukes, skjer følgende:

- Reduksjonsnøkler kreves eller brukes ikke. 
- Hvis prognosen reduseres fullstendig, blir behovene i prognosen for nåværende prognose 0 (null).
- Hvis det ikke er noen fremtidig prognose, reduseres behovene i prognosen fra den siste prognosen som ble angitt.
- Horisonten for behovsprognosereduksjon er ikke inkludert i beregningen av prognosereduksjon. I stedet brukes dekningsgruppehorisonten for prognosereduksjon.
- Positive dager er inkludert i beregningen av prognosereduksjon.
- Hvis faktiske ordretransaksjoner overskrider de prognoseberegnede kravene, videresendes ikke de gjenværende transaksjonene til neste prognoseperiode.

#### <a name="example-1-transactions--dynamic-period"></a>Eksempel 1: Transaksjoner – dynamisk periode

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

#### <a name="example-2-transactions--dynamic-period"></a>Eksempel 2: Transaksjoner – dynamisk periode

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

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Opprette og definere en prognosereduksjonsnøkkel

En prognosereduksjonsnøkkel brukes i metodene **Transaksjoner – reduksjonsnøkkel** og **Prosent – reduksjonsnøkkel** for å redusere prognosebehovene. Følg denne fremgangsmåten for å opprette og definere en reduksjonsnøkkel.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Reduksjonsnøkler**.
2. Velg **Ny** for å opprette en reduksjonsnøkkel.
3. I **Reduksjonsnøkkel**-feltet skriver du inn en unik identifikator for prognosereduksjonsnøkkelen. Angi deretter et navn i **Navn**-feltet. 
4. Definer periodene og reduksjonsnøkkelprosenten i hver periode:

    - **Gyldighetsdato**-feltet angir datoen når opprettelse av periodene starter. Når **Bruk gyldig dato**-alternativet er satt til **Ja**, starter periodene på gyldighetsdatoen. Når det er satt til **Nei**, starter periodene på datoen hovedplanlegging kjøres.
    - Definer periodene prognosereduksjonen skal utføres.
    - For en bestemt periode angir du prosentene som prognosebehovene skal reduseres med. Du kan angi positive verdier for å redusere krav eller negative verdier for å øke krav.

## <a name="use-a-reduction-key"></a>Bruke en reduksjonsnøkkel

En prognosereduksjonsnøkkel må tilordnes til en dekningsgruppe for varen. Følg denne fremgangsmåten hvis du vil tilordne en reduksjonsnøkkel til varens dekningsgruppe.

1. Gå til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**.
2. På **Andre**-hurtigfanen i feltet **Reduksjonsnøkkel** velger reduksjonsnøkkelen som skal tilordnes dekningsgruppen. Reduksjonsnøkkelen gjelder deretter for alle varer som tilhører en dekningsgruppe.
3. Hvis du vil bruke en reduksjonsnøkkel for å beregne prognosereduksjon under hovedplanlegging, må du definere denne innstillingen i oppsettet av prognoseplanen eller hovedplanen. Gå til ett av følgende steder:

    - Hovedplanlegging \> Oppsett \> Planer \> Prognoseplaner
    - Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner

4. På siden **Prognoseplaner** eller **Hovedplaner**, i **Generelt**-hurtigfanen i feltet **Metode som brukes til å redusere prognosebehov**, velger du enten **Prosent – reduksjonsnøkkel** eller **Transaksjoner – reduksjonsnøkkel**.

## <a name="reduce-a-forecast-by-transactions"></a>Redusere en prognose etter transaksjoner

Når du velger **Transaksjoner – reduksjonsnøkkel** eller **Transaksjoner – dynamisk periode** som metode for å redusere prognosebehov, kan du angi hvilke transaksjoner som reduserer prognosen. På siden **Dekningsgrupper**, i **Andre**-hurtigfanen i feltet **Reduser prognose etter**, velger du **Alle transaksjoner** hvis alle transaksjoner skal redusere prognosen, eller **Ordrer** hvis bare salgsordrer skal redusere prognosen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over hovedplaner](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
