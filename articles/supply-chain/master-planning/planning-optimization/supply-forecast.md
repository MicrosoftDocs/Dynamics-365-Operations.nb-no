---
title: Hovedplanlegging med forsyningsprognoser
description: Denne artikkelen beskriver hvordan forsyningsprognoser vurderes under hovedplanlegging.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: dc83d10851958ec67166cb7e40cfd84dceae6651
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690087"
---
# <a name="master-planning-with-supply-forecasts"></a>Hovedplanlegging med forsyningsprognoser

[!include [banner](../../includes/banner.md)]

Ved hjelp av forsyningsprognoser kan du angi forsyningen du forventer i en fremtidig periode. Vanligvis baserer du estimatet på forrige års salgshistorikk, og deretter bruker du prognosen til budsjetteringsformål. Du kan også konfigurere hovedplanene for å vurdere prognoser under planlegging.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Definer en hovedplan for å vurdere forsyningsprognoser

Du kan angi om hver hovedplan skal vurdere prognoser når den kjøres. Bruk fremgangsmåten nedenfor til å angi prognosealternativer for hver plan.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende hovedplan i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny en.
1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Prognosemodell** – Velg modellen som inneholder forsynings- og/eller behovsprognosene som skal vurderes av hovedplanen.
    - **Inkluder forsyningsprognose** – Sett dette alternativet til *Ja* hvis hovedplanen skal vurdere forsyningsprognoser.
    - **Inkluder behovsprognose** – Sett dette alternativet til *Ja* hvis hovedplanen skal vurdere behovsprognoser. Selv om denne innstillingen er uavhengig av innstillingen **Ta med forsyningsprognose**, kan noen av de andre innstillingene på siden gjelde for både forsyningsprognoser og behovsprognoser. Hvis du vil ha mer informasjon om planlegging som tar hensyn til etterspørselsprognoser, kan du se [Hovedplanlegging med behovsprognoser](demand-forecast.md).
    - **Metode som brukes til å redusere behovskrav** – Velg metoden som skal brukes til å redusere prognosebehovene under hovedplanlegging.

        - *Ingen* – Prognosekravene reduseres ikke under hovedplanlegging.
        - *Percent - reduction key* – Forecast requirements will be reduced according to the percentages and time periods that are defined in the reduction key.
        - *Transaksjoner - reduksjonsnøkkel* – Prognosebehovene reduseres av transaksjonene som skjer i periodene som er definert av reduksjonsnøkkelen.
        - *Transaksjoner – dynamisk periode* – Prognosekravene reduseres av ordretransaksjonene som forekommer i løpet av perioden som er dynamisk. Den dynamiske perioden dekker gjeldende prognosedatoer og slutter når neste prognose starter. Metoden *Transaksjoner – dynamisk periode* bruker eller krever ikke en reduksjonsnøkkel, og når du bruker den, gjelder følgende betingelser:

            - Hvis prognosen reduseres fullstendig, blir behovene i prognosen for nåværende prognose 0 (null).
            - Hvis det ikke er noen fremtidig prognose, reduseres behovene i prognosen fra den siste prognosen som ble angitt.
            - Horisonter er inkludert i beregningen av prognosereduksjon.
            - Positive dager er inkludert i beregningen av prognosereduksjon.
            - Hvis faktiske ordretransaksjoner overskrider de prognoseberegnede kravene, videresendes ikke de gjenværende transaksjonene til neste prognoseperiode.

        > [!NOTE]
        > Innstillingen **Metode som brukes til å redusere prognosebehov** gjelder også for behovsprognoser hvis du har aktivert dem for hovedplanen, og påvirker dem på lignende måte. Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging med behovsprognoser](demand-forecast.md).

## <a name="set-reduction-options-for-coverage-groups"></a>Angi reduksjonsalternativer for dekningsgrupper

Følg denne fremgangsmåten for å definere alternativer som styrer hvordan en dekningsgruppe vil redusere prognosekravene for hovedplaner som bruker transaksjonsbasert reduksjon.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Dekningsgrupper**.
1. Velg enten en eksisterende dekningsgruppe i listen, eller velg **Ny** i handlingsruten for å opprette en ny.
1. På hurtigfanen **Annet** i feltet **Reduser prognose etter** angir du hvordan forsyningsprognosekrav må reduseres for elementer i dekningsgruppen, for hovedplaner der feltet **Metode som brukes til å redusere prognosebehov** er satt til *Transaksjoner – reduksjonsnøkkel* eller *Transaksjoner – dynamisk periode*. Velg én av følgende verdier:

    - *Alle transaksjoner* – Alle transaksjoner skal redusere prognosen.
    - *Ordrer* – Bare ordrer av samme type skal redusere prognosen.

    Standardinnstillingene for en vare angir for eksempel at den skal produseres. Det finnes en forsyningsprognoselinje for et antall på 50, og det finnes en eksisterende bestilling av et antall på 20. Hvis feltet **Reduser prognose etter** er satt til *Bestillinger*, opprettes et produksjonsforslag for et antall på 50. Hvis den er satt til *Alle transaksjoner*, reduseres den planlagte produksjonsordren til et antall på 30.

    Denne innstillingen gjelder også for reduksjon i etterspørselsprognose. Hvis du vil ha mer informasjon, kan du se [Hovedplanlegging med behovsprognoser](demand-forecast.md).

## <a name="enter-a-supply-forecast-for-a-product"></a>Angi en forsyningsprognose for et produkt

Følg denne fremgangsmåten for å angi en forsyningsprognose.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet du vil angi en prognose for.
1. Gå til **Plan**-fanen i handlingsruten, og velg deretter **Forsyningsprognose**.
1. I handlingsruten velger du **Ny** for å legge til en prognose i rutenettet på siden **Forsyningsprognose**.
1. Angi informasjon på den nye linjen etter behov for å spesifisere prognosen.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Planlegge for en vare med forsyningsprognoselinjer

Når du kjører en hovedplan som omfatter en vare som det finnes en forsyningsprognose for, oppretter systemet en bestilling for forsyningslinjene som er angitt. Standard ordreinnstillinger for varen overholdes. Hvis disse standard ordreinnstillingene angir **Standard ordretype** for *Bestilling*, og det ikke er angitt en leverandørkonto på forsyningsprognoselinjen, vil systemet bruke standardleverandøren for varen.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Kontrollere om en planlagt bestilling er en forsyningsprognoseordre

Bruk fremgangsmåten nedenfor for å finne ut om en planlagt bestilling ble opprettet som et resultat av en forsyningsprognose.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**.
1. Åpne den planlagte bestillingen du vil inspisere.
1. I hurtigkategorien **Generelt** se på verdien av feltet **Forsyningsprognose**. Hvis ordren ble opprettet for å dekke en forsyningsprognose, blir dette feltet satt til *Ja*.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Eksempler på hovedplanlegging med forsyningsprognoser

Denne delen inneholder flere eksempler som viser hvordan forsyningsprognoser påvirker hovedplanlegging.

### <a name="example-1-supply-forecast-for-an-item"></a>Eksempel 1: Forsyningsprognose for en vare

Du har en vare der standard ordretype er *Bestilling,* og standardleverandøren er *US-002*. Den har følgende forsyningsprognoselinje.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |

Når du kjører hovedplanlegging, blir det opprettet en bestillingsforslag for *35* forskjellige leverandører fra *USA-002*.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Eksempel 2: Flere forsyningsprognoselinjer, med og uten en leverandør

Du har en vare der standard ordretype er *Bestilling,* og standardleverandøren er *US-002*. Den har følgende forsyningsprognoselinjer.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | hver   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

I dette tilfellet behandler systemet linjen som ikke angir en leverandør, som en generisk prognose, og det forutsetter at linjen som angir en leverandør, skal trekkes fra den generiske prognosen. Hovedplanleggingen vil derfor opprette følgende bestillingsforslag for varen:

- Bestillingsforslag for et antall på *25 ea* fra leverandør *US-101* (Leverandøren og antallet som er angitt i prognoselinjen brukes.)
- Et bestillingsforslag på et antall på *10 ea* fra leverandøren *US-002* (Siden ingen leverandør er angitt på den andre prognoselinjen, brukes standardleverandøren, og antall på denne prognoselinjen reduseres med antallet på den leverandørspesifikke prognoselinjen.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Eksempel 3: Planer som bruker reduksjonsmetoden Transaksjoner – dynamisk periode i en enkelt prognoseperiode

For hovedplaner som bruker *Transaksjoner – dynamisk periode* som prognosereduksjonsmetode, vil hovedplanlegging redusere prognoseantall hvis det finnes eksisterende transaksjoner som samsvarer med disse forsyningsegenskapene.

Du har for eksempel en vare der standard ordretype er *Bestilling*. Den har følgende forsyningsprognoselinje.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Fordi det bare er én forsyningsprognoselinje, er det bare én prognoseperiode.

Når du kjører en hovedplan som er definert til å bruke *Transaksjoner – dynamisk periode* som reduksjonsmetode, kan ett av følgende resultater forekomme:

- Hvis det finnes en bestilling for leverandør *US-101* og et antall på *10 ea*, og **forsyningsprognose**-feltet er satt til *Ja*, oppretter hovedplanleggingen en ny planlagt bestilling for gjenværende antall på *10*. Prognoselinjen reduseres, fordi leverandøren samsvarer med den eksisterende bestillingen.
- Hvis det finnes en bestilling for leverandør *US-102*, område *1*, lager *11* og et antall på *10 ea*, og **Forsyningsprognose**-feltet er satt til *Ja*, oppretter hovedplanleggingen en ny planlagt bestilling for fullt antall på *25 ea*. Prognoselinjen kan ikke reduseres, fordi den har en annen leverandør enn den eksisterende bestillingen.

> [!NOTE]
> Denne situasjonen kan oppstå for planlagte bestillinger, fordi en leverandør er knyttet til dem. For overføringsordrer og produksjonsordrer vil imidlertid forsyningsprognosebeløpene alltid reduseres med eksisterende ordrer, fordi det ikke er angitt en leverandør for disse typene ordrer.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Eksempel 4: Planer som bruker reduksjonsmetoden Transaksjoner – dynamisk periode over flere prognoseperiode

Du har en vare der standard ordretype er *Bestilling*. Den har følgende forsyningsprognoselinjer.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |
| CurrentF | 15/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

I dette eksemplet er det to prognoselinjer der hver har en forskjellig dato. Datoene fastsetter derfor hvor viktig prognoseperiodene skal være. Den første perioden er fra 10. oktober til 14. oktober 2022 (10/10/22–14/10/22). Den andre er fra 15. oktober 2022 (15/10/22) og videre.

Det finnes en eksisterende bestilling for leverandøren *US-101*, et antall på *10 ea* og datoen *12/10/22* (12. oktober 2022). Når du kjører en hovedplan som er definert til å bruke *Transaksjoner – dynamisk periode* som reduksjonsmetode, opprettes følgende bestillinger:

- Planlagt bestilling av et antall på *15 ea* og datoen *10/10/22* (Antallet reduseres med den eksisterende bestillingen som er datert i løpet av den samme prognoseperioden.)
- Planlagt bestilling av et antall på *25 ea* og datoen *15/10/22* (Antallet er hele antallet i prognosen.)

### <a name="example-5-plans-that-use-no-reduction"></a>Eksempel 5: Planer som ikke bruker reduksjon

Når du kjører en plan der prognosereduksjonsmetoden er *Ingen*, vil hovedplanlegging alltid opprette planlagt forsyning for alle forsyningsprognoselinjer. Når den planlagte forsyningen er godkjent, vil det redusere fremtidige planlagte bestillinger. Bestillinger vil imidlertid ikke redusere forsyningsprognoselinjene.

Du har for eksempel en vare der standard ordretype er *Bestilling*. Den har følgende forsyningsprognoselinje.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | hver   | 1    | 11        |

Det finnes en eksisterende bestilling for leverandøren *US-101*, område *1*, lager *11*, et antall på *25 ea* og datoen *10/10/22*. 

Når du kjører en hovedplan som er definert til å bruke *Ingen* som reduksjonsmetode, opprettes det en planlagt bestilling for leverandør *US-101*, område *1*, lager *11*, et antall på *25* og datoen *10/10/22*. Den eksisterende bestillingen vil med andre ord ikke reduseres, fordi prognosereduksjonsmetoden *Ingen*.

Nå redigerer du den planlagte bestillingen som ble opprettet etter siste planleggingsutkjøring, og endre antallet til *15*. Deretter godkjenner du bestillingen. Neste gang du kjører hovedplanen, opprettes det en planlagt bestilling for leverandør *US-101*, område *1*, lager *11*, et antall på *10 ea* og datoen *10/10/22*. Denne tiden reduseres antallet for å gjenspeile antallet i den eksisterende godkjente ordren fra den forrige planleggingskjøringen.

## <a name="differences-between-planning-optimization-and-the-built-in-planning-engine"></a>Forskjeller mellom planleggingsoptimalisering og den innebygde planleggingsmotoren

Forsyningsprognose fungerer litt annerledes, avhengig av planleggingsmotoren du bruker (innebygde hovedplanlegging eller planleggingsoptimalisering). Denne delen beskriver forskjellene.

### <a name="vendor-groups"></a>Leverandørgrupper

Når du legger til en prognoselinje, kan du angi en leverandør og en leverandørgruppe. I den innebygde planleggingsmotoren grupperes planlagte bestillinger som opprettes av kombinasjonen av verdiene for leverandør- og leverandørgruppen. I planleggingsoptimalisering grupperes planlagte bestillinger etter leverandør.

Følgende tabell gir noen eksempler på forsyningsprognoselinjer for en vare.

| Modell    | Dato     | Leverandørnummer | Leverandørgruppe | Antall | Enhet | Nettsted | Lager |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | LeverandørGruppeA | 5        | hver   | 1    | 11        |
| CurrentF | 10/10/22 |                | LeverandørGruppeA | 6        | hver   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | hver   | 1    | 11        |

Leverandør *LeverandørA* er standardleverandøren for leverandørgruppen *LeverandørgruppeA*. Det er også standardleverandøren for varen.

Den innebygde planleggingsmotoren vil opprette følgende ordrer:

- Planlagt bestilling for leverandør *LeverandørA*, leverandørgruppe *LeverandørGruppe* og et antall på *11*
- Planlagt bestilling for leverandør *LeverandørA*, og et antall på *7*

Planleggingsoptimalisering oppretter bare én ordre:

- Planlagt bestilling for leverandør *LeverandørA*, leverandørgruppe *LeverandørGruppe* og et antall på *18*

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Reduksjon av generelle prognoser etter mer spesifikke prognoser

I den innebygde hovedplanleggingsmotoren er resultatet uforutsigbar hvis noen prognoser har en leverandør, men andre gjør det ikke.

I Planleggingsoptimalisering reduseres alltid generelle prognoser med mer spesifikke prognoser, slik eksemplet nedenfor viser.

Følgende tabell gir noen eksempler på forsyningsprognoselinjer for en vare.

| Dato       | Antall | Leverandør   | Leverandørgruppe  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Leverandør-A | LeverandørGruppe-A |
| 02/11/2022 | 6,00     | Leverandør-A | LeverandørGruppe-A |
| 02/11/2022 | 15.00    |          |               |

Den generelle prognosen (for 15,00 stykker) reduseres med de mer spesifikke prognosene (for 5,00 + 6,00 = 11,00 stykker). Resten tilordnes standardleverandøren. Tabellen nedenfor viser planlagte ordrer.

| Dato       | Antall | Leverandør   | Leverandørgruppe  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Leverandør-A | LeverandørGruppe-A |
| 02/11/2022 | 4.00     | Leverandør-A | LeverandørGruppe-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Overholde standardordreinnstillinger når planlagte bestillinger genereres

Hver vare kan ha standard bestillingsinnstillinger, for eksempel minimum bestillingsantall. Den innebygde planleggingsmotoren ignorerer disse innstillingene, og oversetter derfor prognoser til planlagte ordrer som har samme antall. Planleggingsoptimalisering overholder disse innstillingene når planlagte bestillinger genereres fra forsyningsprognoser. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Samling av planlagte bestillinger som resultat av reduksjon av godkjente bestillinger

Den innebygde hovedplanleggingsmotoren antar at bare én ordre vil redusere den eksisterende forsyningsprognosen. Hvis flere ordrer samsvarer med en forsyningsprognoselinje, vil derfor bare den første ordren redusere den. I Planleggingsoptimalisering vil alle ordrer som samsvarer med forsyningsprognoselinjene, redusere den.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Reduksjon av prognoser bare ved å samsvare leverandører

Når den innebygde hovedplanleggingsmotoren reduserer en prognose ved eksisterende frigitte bestillinger, sikrer den ikke at leverandøren i bestillingen samsvarer med leverandøren fra prognosen. Planleggingsoptimalisering reduserer prognoser bare etter bestillinger som har en samsvarende verdi i leverandørfeltet.

For overførings- og produksjonsordrer blir leverandørfeltet alltid ignorert, fordi det ikke er relevant for disse ordretypene.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Reduksjon av prognoser etter overføringsordrer

Hvis standard ordretype for en vare er *Overføring*, kan prognoser bare reduseres ved hjelp av eksisterende overføringsforslag. For produksjonsordrer og bestillinger vil imidlertid bare frigitte ordrer redusere forsyningsprognosen.

Den innebygde planleggingsmotoren reduserer for alle overføringsordrestatuser, mens planleggingsoptimalisering reduserer prognoser bare ved hjelp av overføringsordrer som er i *Frigitt* tilstand.
