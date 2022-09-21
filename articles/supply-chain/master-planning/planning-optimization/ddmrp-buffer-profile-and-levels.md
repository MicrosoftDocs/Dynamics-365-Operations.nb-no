---
title: Bufferprofil og -nivåer
description: Denne artikkelen inneholder informasjon om bufferprofiler og -nivåer, som fastsetter minimums- og maksimumsnivåene for lager som bør holdes for hvert utkoblingspunkt.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428151"
---
# <a name="buffer-profile-and-levels"></a>Bufferprofil og -nivåer

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Når du har identifisert utkoblingspunktene (nøkkelvarer som du vil beholde på lageret strategisk), må du bestemme hvor mye lager (buffer) du vil ha på hver av dem. Denne oppgaven er det andre trinnet i DDMRP (Demand Driven Materials Resource Planning – behovsdrevet planlegging av materialressurser).

## <a name="buffer-levels-and-zones"></a>Buffernivåer og -soner

I DDMRP defineres hver lagerbuffer ved hjelp av tre verdier: minimumsantallet, maksimumsantallet og gjenbestillingspunktet. Disse verdiene fastsetter tre differansesoner, som identifiseres av følgende fargekoder:

- **Rød sone** – Området under minimumsantallet. Minimumsantallet kalles også "toppen av rødt", og planleggingsstrategien bør være utformet for å sikre at beholdningsnivåene alltid er over dette punktet.
- **Gul sone** – Området mellom minimumsantallet og gjenbestillingspunktet. Gjenbestillingspunktet kalles også "toppen av gult". Når dette punktet nås, skal systemet bestille på nytt.
- **Grønn sone** – Området mellom gjenbestillingspunktet og det maksimale antallet. Det maksimale antallet også "toppen av grønt". Dette er det maksimale nivået som lageret vil bli etterfyllt til.

Illustrasjonen nedenfor viser de tre fargede sonene, og hvordan de står i forhold til minimumsantall, maksimumsantall og gjenbestillingspunkt.

![DDMRP-buffersoner og -nivåer.](media/ddmrp-buffer-levels.png "DDMRP-buffersoner og -nivåer")

## <a name="calculating-the-buffer-zones"></a>Beregning av buffersonene

Denne delen beskriver hvordan høyden til hver buffersone beregnes.

Den gule sonen beregnes vanligvis først. Denne sonen representerer antallet som du bruker i det øyeblikket du bestiller til ordren ankommer. Det er med andre ord det forventede forbruket under leveringstiden for etterfylling. Det beregnes ved hjelp av følgende ligning:

- **Gul sone** = *Gjennomsnittlig daglig bruk (ADU)* × *Utkoblet leveringstid*

Den *utkoblede leveringstiden* representerer tiden som kreves for å produsere eller motta en vare, hvis utkoblingspunktene alltid er på lager. Dette er vanligvis mye kortere enn den *samlede leveringstiden*, som tradisjonelt brukes i hovedplanlegging. Riktige bufferinnstillinger er nøkkelen til å sikre at utkoblingspunktene alltid er på lager, uten at lageret er overfylt.

Den røde sonen beregnes ved hjelp av følgende ligninger:

- **Rødt grunnlag** = *ADU* × *Utkoblet leveringstid* × *Leveringstidsfaktor*
- **Rød sikkerhet** = *Rødt grunnlag* × *Variasjonsfaktor*
- **Rød sone** = *Rødt grunnlag* + *Rød sikkerhet*

Den grønne sonen beregnes som det maksimale resultatet av de følgende tre ligningene:

- *Minste ordreantall*
- *ADU* × *Ordresyklus*
- *ADU* × *Utkoblet leveringstid* × *Leveringstidsfaktor*

## <a name="calculating-average-daily-usage"></a>Beregning av gjennomsnittlig daglig bruk

Systemet bruker én av tre metoder for å beregne mengden du bruker per dag:

- **Gjennomsnittlig daglig bruk (tidligere)** – Denne fremgangsmåten er basert på faktisk tidligere forbruk.
- **Gjennomsnittlig daglig bruk (senere)** – Denne fremgangsmåten er basert på de estimerte fremtidige forbruket.
- **Gjennomsnittlig daglig bruk (blandet)** – Denne fremgangsmåten er basert på en vektet blanding av tidligere og estimert forbruk.

### <a name="average-daily-usage-past"></a>Gjennomsnittlig daglig bruk (tidligere)

Tidligere ADU beregnes som et gjennomsnitt ved å legge sammen antallene som brukes hver dag i et angitt antall tidligere dager, og deretter dele totalen på antall dager. Illustrasjonen nedenfor viser hvordan denne fremgangsmåten fungerer når beregningen ser tre dager inn i fortiden.

![Diagram over gjennomsnittlig daglig bruk (tidligere).](media/ddmrp-adu-past.png "Diagram over gjennomsnittlig daglig bruk (tidligere)")

I den forrige illustrasjonen, hvis i dag er 11. juni om morgenen, er ADU for de forrige tre dagene (8. juni, 9 og 10) lik 21.

- **ADU (tidligere)** = (29 + 11 + 23) ÷ 3 = 21

Følgende transaksjoner tas i betraktning for beregning av gjennomsnittlig daglig bruk (fortid):

- Transaksjoner som reduserer antallet av varen (i `inventtrans`-tabellen der antallet er mindre enn null)
- Transaksjoner med statusen *I ordre/bestilling*, *Reservert av bestilt*, *Fysisk reservert*, *Plukket*, *Fratrukket* eller *Solgt*
- Transaksjoner datert i den valgte perioden bakover (gjennomsnittlig daglig bruk for forrige periode)
- Andre transaksjoner enn lagerarbeid, karantene, salgstilbud eller kontoutdrag (`WHSWork`, `WHSQuarantine`, `SalesQuotation` eller `Statement`)
- Andre transaksjoner enn overføringsjournaler som er innenfor samme dekningsdimensjon

### <a name="average-daily-usage-forward"></a>Gjennomsnittlig daglig bruk (senere)

Det kan hende at du ikke har noen tidligere bruksdata for et nytt produkt. Derfor kan du i stedet bruke prosjektert ADU fremover (for eksempel basert på estimert behov). Illustrasjonen nedenfor viser hvordan denne fremgangsmåten fungerer når beregningen ser tre dager inn i fremtiden (inkludert i dag).

![Diagram over gjennomsnittlig daglig bruk (senere).](media/ddmrp-adu-forward.png "Diagram over gjennomsnittlig daglig bruk (senere)")

I den forrige illustrasjonen, hvis i dag er 11. juni om morgenen, er ADU for de neste tre dagene (11. juni, 12 og 13) lik 21,66.

- **ADU (senere)** = (18 + 18 + 29) ÷ 3 = 21,66

Følgende transaksjoner tas i betraktning for beregning av gjennomsnittlig daglig bruk (fremtid):

- Prognosetransaksjoner for varen der prognosen er valgt i hovedplanen
- Transaksjoner datert i den valgte perioden fremover (gjennomsnittlig daglig bruk for neste periode)

### <a name="average-daily-usage-blended"></a>Gjennomsnittlig daglig bruk (blandet)

Blandet ADU kombinerer gjennomsnittlig tidligere bruk og gjennomsnittlig bruk fremover, som vist i illustrasjonen nedenfor.

![Diagram over gjennomsnittlig daglig bruk (blandet).](media/ddmrp-adu-blended.png "Diagram over gjennomsnittlig daglig bruk (blandet)")

I den forrige illustrasjonen, hvis i dag er 11. juni om morgenen, er blandet ADU for de forrige og neste tre dagene (8. juni til 13. juni) lik 21,33.

- **ADU blandet** = (*ADU tidligere* + *ADU senere*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Bufferberegningsfaktorer

For hver vare kan du definere to faktorer for å justere hvor store de røde og grønne sonene skal være. På denne måten kan du kompensere for forventet leveringstid og etterspørselsavvik.

![Leveringstid og avviksfaktorer.](media/ddmrp-zone-factors.png "Leveringstid og avviksfaktorer")

Den første faktoren er *leveringstidsfaktoren*. Verdien er en desimalverdi fra 0 til 1. Jo lenger leveringstiden er, jo lavere skal verdien være. Demand Driven Institute anbefaler følgende områder:

- **Lang leveringstid:** 0,20–0,40
- **Middels leveringstid:** 0,41–0,60
- **Kort leveringstid:** 0,61–1,00

Den andre faktoren er *avviksfaktoren*. Verdien er en desimalverdi fra 0 til 1. Jo høyere etterspørselsavviket er, jo lavere skal verdien være. Demand Driven Institute anbefaler følgende områder:

- **Lavt avvik:** 0,20–0,40
- **Middels avvik:** 0,41–0,60
- **Høyt avvik:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Eksempler på bufferberegning

Dette eksemplet er en fortsettelse av eksemplet på produksjon av puter i [Lagerplassering](ddmrp-inventory-positioning.md). I dette eksemplet valgte du utkoblingspunkter som reduserte leveringstiden fra 21 dager til 5 dager, slik illustrasjonen nedenfor viser.

![Eksempel på utkoblet leveringstid.](media/ddmrp-bom-decoupled-lead-time-example.png "Eksempel på utkoblet leveringstid")

For dette eksemplet kan du anta at ADU er beregnet som 23 stykker, og som vist i den forrige illustrasjonen, er den utkoblede leveringstiden 5 dager. Ved å bruke disse verdiene kan du beregne den gule sonen ved hjelp av følgende ligning:

- **Gul sone** = *ADU* × *Utkoblet leveringstid* = 115

![Eksempel på beregning av gul sone.](media/ddmrp-example-calc-yellow.png "Eksempel på beregning av gul sone")

Beregningen av den røde sonen ligner på beregningen av den gule sonen, men det dreier seg om avvik og leveringstid. La oss si at du har observert en middels leveringstid (faktor = 0,50) og et stort etterspørselsavvik (faktor = 0,8). Ved å bruke disse verdiene sammen med komponentene fra ligningen for den gule sonen kan du beregne den røde sonen ved hjelp av følgende ligninger:

- **Rødt grunnlag** = *ADU* × *Utkoblet leveringstid* × *Leveringstidsfaktor* = 57,5
- **Rød sikkerhet** = *Rødt grunnlag* × *Variasjonsfaktor* = 46
- **Rød sone** = *Rødt grunnlag* + *Rød sikkerhet* = 103,5

Systemet runder av den røde sonen til 104 stykker (stykkevis), fordi stykker telles i hele tall.

![Eksempel på beregning av rød sone.](media/ddmrp-example-calc-red.png "Eksempel på beregning av rød sone")

Beregningen av den grønne sonen omfatter også komponentene fra ligningen for den gule sonen, men tillater en minimum ordrestørrelse, ordresyklus og leveringstidsfaktor. For dette eksemplet kan vi anta at det ikke finnes noen ordresyklus (derfor har du ingen tidsbegrensninger på hvor ofte du bestiller), og minimum ordreantall er 10 stykker. Den grønne sonen beregnes deretter som det maksimale resultatet av de følgende tre ligningene:

- *Minste ordreantall* = 10
- *ADU* × *Ordresyklus* = 0
- *ADU* × *Utkoblet leveringstid* × *Leveringstidsfaktor* = 57,5

Systemet runder av den grønne sonen til 58 stykker (stykkevis), fordi stykker telles i hele tall.

![Eksempel på beregning av grønn sone.](media/ddmrp-example-calc-green.png "Eksempel på beregning av grønn sone")

Illustrasjonen nedenfor oppsummerer disse soneberegningsresultatene ved å bruke traktgrafikken som ofte brukes i DDMRP.

![Oppsummering av soneberegningsresultater.](media/ddmrp-example-calc-summary.png "Oppsummering av soneberegningsresultater")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynamiske justeringer

Med dynamiske justeringer kan du bruke en *etterspørselsjusteringsfaktor* i perioder med høy eller lav etterspørsel. Denne faktoren multipliserer ADU i alle beregninger for den valgte perioden. Buffersonene endres deretter i neste omgang. Du bruker vanligvis denne faktoren når du har generert de opprinnelige bufferverdiene, slik at du kan finjustere dem over tid og som svar på endring av betingelser. Denne oppgaven er det tredje trinnet av DDMRP.

Det kan for eksempel være mer etterspørsel etter et puteprodukt i august når folk tar ferie. Derfor forventes det at salget vil være høyere. I dette tilfellet kan du endre verdien for **etterspørselsjusteringsfaktoren** for produktet til *1,5* for alle ukene i august.

På denne måten kan du beregne bufferverdier over tid og deretter justere dem basert på mer enn bare informasjonen som systemet har. I en fullstendig DDMRP-implementering vil du beregne nye bufferverdier hver dag gjennom en satsvis jobb, og automatisk godta verdiene. Deretter vil du kjøre planleggingen som en satsvis jobb og gå gjennom de planlagte bestillingene hver dag for å fylle på bufferne.

## <a name="implement-buffers-in-supply-chain-management"></a>Implementer buffere i Supply Chain Management

Denne delen beskriver hvordan du implementerer buffersonestrategien i Microsoft Dynamics 365 Supply Chain Management. Det forutsettes at du allerede har utført analysene og beregningene som er beskrevet i første halvdel av denne artikkelen.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Definer buffere for en vare som har et utkoblingspunkt

Følg denne fremgangsmåten for å definere bufferverdier for et utkoblingspunkt.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg en frigitt vare som er definert som et utkoblingspunkt. (For mer informasjon, se [Lagerplassering](ddmrp-inventory-positioning.md).)
1. Gå til **Plan**-fanen i handlingsruten, og velg deretter **Varedekning**.
1. Velg en varedekningspost som oppretter et utkoblingspunkt, på **Varedekning**-siden. (Denne posten vil vise navnet på en dekningsgruppe som er konfigurert til å opprette utkoblingspunkter.)
1. Velg fanen **Generelt**.
1. Hvis du vil at systemet skal beregne bufferverdier på nytt hver dag eller hver uke, basert på innstillingene for salgshistorikk, prognoser og dekningsgruppe, følger du denne fremgangsmåten:

    1. Sett alternativet **Bufferverdier over tid** til *Ja*.
    1. En meldingsboks varsler deg om at de manuelle bufferinnstillingene (**Minimum**, **Gjenbestillingspunkt** og **Maksimum**) vil bli tilbakestilt hvis du fortsetter. Velg **Ja** for å beholde den nye innstillingen.

    Hvis du heller foretrekker å beregne eller angi bufferinnstillingene bare én gang, følger du denne fremgangsmåten:

    1. Sett alternativet **Bufferverdier over tid** til *Nei*.
    1. Sett feltene **Minimum**, **Gjenbestillingspunkt** og **Maksimum** til bufferverdiene du har beregnet for varen, som beskrevet tidligere i denne artikkelen.

1. Sett følgende felt for å fullføre konfigurasjon av DDMRP-beregningene for varen:

    - **Ordresyklus** – Angi antall dager som må gå mellom bestillingene for varen. Sett verdien til *0* (null) hvis det ikke finnes ordrebegrensninger. Dette feltet påvirker bufferen for maksimalt antall, som beskrevet tidligere i denne artikkelen.
    - **Gjennomsnittlig daglig bruk** – Du kan velge å angi en estimert ADU for varen. Dette feltet er bare beregnet til informasjon. Vanligvis beregnes verdien automatisk som en del av bufferberegningene.
    - **Ordreøkningsterskel** – Angi minste antall daglig salg av varen som kvalifiserer som en salgsøkning (vanligvis stor etterspørsel). Systemet bruker dette feltet til å øke gjenbestillingsantallet for planlagte bestillinger i perioder med høy etterspørsel. Hvis du vil ha mer informasjon, kan du se [Etterspørselsdrevet planlegging](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Beregn eller angi utkoblede leveringstider

Når det gjelder varer der du velger å tillate at systemet [beregner buffersonene automatisk](#set-up-buffers), følger du denne fremgangsmåten for å beregne eller angi utkoblede leveringstider for en vare som har et utkoblingspunkt.

1. Åpne **Varedekning**-siden for varen som har et utkoblingspunkt. (Hvis du vil ha mer informasjon, kan du se [Definer buffere for en vare som har et utkoblingspunkt](#set-up-buffers).)
1. Velg en varedekningspost som oppretter et utkoblingspunkt.
1. Velg **Bufferverdier**-fanen.
1. Hvis det ikke vises noen tidsperioder i rutenettet, går du til **Bufferverdier**-fanen i handlingsruten og velger **Legg til tidsperioder**. Systemet fyller ut rutenettet med rader for hver daglig eller ukentlige tidsperiode, avhengig av om feltet **Periode for min, maks og gjenbestillingspunkt** for [dekningsgruppen](ddmrp-inventory-positioning.md) er angitt til *Daglig* eller *Ukentlig*. Systemet legger til nok rader til å nå horisonten som er angitt for dekningsgruppen som er tilordnet varen.
1. Velg tidsperioden der du vil beregne den utkoblede leveringstiden. (Vanligvis er denne tidsperioden perioden som inkluderer dagens dato.)
1. På **Bufferverdier**-fanen i handlingsruten velger du **Beregn utkoblet leveringstid**.
1. I dialogboksen **Beregn utkoblet leveringstid** angir du verdier i følgende felter:

    - **Stykkliste** – Velg stykklisten som du vil kjøre beregningen på.
    - **Dato** – Velg datoen som du vil kjøre beregningen på. Settet med tilgjengelige stykklister blir filtrert slik at bare stykklister som er aktive for den valgte datoen, vises.
    - **Antall** – Angi antallet som du vil kjøre beregningen for. Settet med tilgjengelige stykklister blir filtrert slik at bare stykklister som gjelder for det angitte antallet, vises.

1. Velg **OK** for å kjøre beregningen og lukke dialogboksen **Beregn utkoblet leveringstid**. Kolonnen **Beregn utkoblet leveringstid** for den valgte tidsperioden viser nå den beregnede verdien.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Beregn eller angi gjennomsnittlig daglig bruk

Når det gjelder varer der du velger å tillate at systemet [beregner buffersonene automatisk](#set-up-buffers), følger du denne fremgangsmåten for å beregne eller angi ADU-en for en vare som har et utkoblingspunkt.

1. Åpne **Varedekning**-siden for varen som har et utkoblingspunkt. (Hvis du vil ha mer informasjon, kan du se [Definer buffere for en vare som har et utkoblingspunkt](#set-up-buffers).)
1. Velg en varedekningspost som oppretter et utkoblingspunkt.
1. Velg **Bufferverdier**-fanen.
1. Hvis det ikke vises noen tidsperioder i rutenettet, går du til **Bufferverdier**-fanen i handlingsruten og velger **Legg til tidsperioder**. Systemet fyller ut rutenettet med rader for hver daglig eller ukentlige tidsperiode, avhengig av om feltet **Periode for min, maks og gjenbestillingspunkt** for [dekningsgruppen](ddmrp-inventory-positioning.md) er angitt til *Daglig* eller *Ukentlig*. I tillegg hentes standardverdier for feltene **Leveringstidsfaktor** og **Variasjonsfaktor** fra dekningsgruppen. Du kan redigere disse verdiene for hver rad etter behov.
1. Velg en tidsperiode der du vil beregne ADU.
1. På **Bufferverdier**-fanen i handlingsruten velger du **Beregn gjennomsnittlig daglig bruk**. Systemet prøver å samle inn data som kreves for ADU-beregningen, som definert for [dekningsgruppen](ddmrp-inventory-positioning.md).
1. Følg ett av disse trinnene:

    - Hvis dataene som kreves, er tilgjengelige, legges beregningsresultatene til i kolonnen **Gjennomsnittlig daglig bruk**. I dette tilfellet kreves det ingen handling.
    - Hvis dataene som kreves, ikke er tilgjengelige, legges det ikke til noen verdier automatisk. I dette tilfellet må du angi estimerte verdier manuelt for hver rad du planlegger å beregne bufferverdier for.

### <a name="calculate-and-apply-buffer-values"></a>Beregn og bruk bufferverdier

For varer der du velger å tillate at systemet [beregner buffersonene automatisk](#set-up-buffers), kan du manuelt utløse beregningen av bufferverdier ved å følge disse trinnene.

1. For den relevante varen som har et avkoblingspunkt, må du [konfigurere bufferberegningen](#set-up-buffers), [beregne eller angi avkoblede leveringstider](#calc-lead-time) og [beregne eller angi gjennomsnittlig daglig bruk](#calc-adu) for alle relevante tidsperioder, som beskrevet tidligere i denne artikkelen.
1. Åpne **Varedekning**-siden for varen som har et utkoblingspunkt.
1. Velg **Bufferverdier**-fanen, som allerede skal vise en liste over tidsperioder.
1. Velg tidsperioden der du vil beregne bufferverdier. (Vanligvis vil denne tidsperioden være perioden som inkluderer i dag.) Raden du velger, må allerede ha verdier som ikke er null, i kolonnene **Gjennomsnittlig daglig bruk** og **Utkoblet leveringstid**.
1. Rediger feltet **Etterspørselsjusteringsfaktor** for én eller flere rader etter behov. Systemet vil bruke denne faktoren for verdien **Gjennomsnittlig daglig bruk** i alle bufferberegninger der denne verdien brukes. Ved hjelp av denne faktoren kan du justere etter dato (for eksempel til helligdager eller sesongvarer).
1. På **Bufferverdier**-fanen i handlingsruten velger du **Beregn antall for min, maks og gjenbestillingspunkt**. Systemet beregner og fyller ut kolonnene **Beregnet min**, **Beregnet gjenbestillingspunkt** og **Beregnet maks** på **Varedekning**-siden.
1. Når du er ferdig med å gå gjennom de beregnede verdiene, må du bruke dem. Ellers vil de ikke ha noen virkning. Når du bruker en beregning for én eller flere rader, kopieres verdier fra feltene **Beregnet min**, **Beregnet gjenbestilling** og **Beregnet maks** henholdsvis til kolonnene **Min**, **Gjenbestillingspunkt** og **Maks**. På **Bufferverdier**-fanen i handlingsruten, i gruppen **Utfør handling**, velger du en av følgende knapper:

    - **Godta alle beregninger** – Bruk alle beregnede verdier i rutenettet.
    - **Godta beregninger for valgte rader** – Bruk bare beregnede verdier for de valgte radene.
    - **Forkast alle beregninger** – Forkast alle beregnede verdier for minimumsantall, maksimalt antall og gjenbestillingspunkt i rutenettet.
    - **Forkast beregninger for valgte rader** – Forkast alle beregnede verdier for minimumsantall, maksimumsantall og gjenbestillingspunkt for de valgte radene.

### <a name="schedule-automatic-buffer-value-calculations"></a>Planlegg automatiske bufferverdiberegninger

Når du har konfigurert DDMRP-innstillingene fullstendig og bekreftet at de fungerer som forventet, vil du sannsynligvis sette opp en satsvis jobb for å omberegne ADU og relaterte bufferverdier regelmessig etter behov, basert på data om faktisk forbruk og/eller oppdaterte prognoser. Denne fremgangsmåten gjelder bare for varer der du velger å tillate at systemet [automatisk beregner buffersonene](#set-up-buffers).

Følg denne fremgangsmåten for å planlegge automatiske bufferverdiberegninger.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Beregn bufferverdier**.
1. I dialogboksen **Beregn bufferverdier** angir du verdier i følgende felter:

    - **Beregn gjennomsnittlig daglig bruk** – Sett dette alternativet til *Ja* for å beregne ADU for varer med utkoblingspunkt på nytt hver gang jobben kjøres. Sett det til *Nei* for å hoppe over denne beregningen. Vanligvis bør du sette dette alternativet til *Ja*.
    - **Beregn utkoblet leveringstid** – Sett dette alternativet til *Ja* for å beregne de utkoblede leveringstidene på nytt hver gang jobben kjøres. Sett det til *Nei* for å hoppe over denne beregningen. Vanligvis bør du sette dette alternativet til *Ja*.
    - **Beregn bufferverdier** – Sett dette alternativet til *Ja* for å beregne bufferverdier på nytt hver gang jobben kjøres. Sett det til *Nei* for å hoppe over denne beregningen. Vanligvis bør du sette dette alternativet til *Ja*.
    - **Godta beregning for min, maks og gjenbestillingspunkt** – Sett dette alternativet til *Ja* for automatisk å godkjenne og bruke de omberegnede bufferverdiene hver gang jobben kjøres. Sett det til *Nei* hvis du vil at de omberegnede verdiene ikke skal være i bruk. I så fall trer ikke de omberegnede verdiene i kraft hvis de ikke noen bruke dem manuelt senere fra hvert produkts **Varedekning**-side. Vanligvis bør du sette dette alternativet til *Ja*.
    - **Hovedplan** – Velg en hovedplan som inkluderer varene som vil bli påvirket av beregningen. Beregningen vil gjelde for alle varene i planfilteret, som vil bli ytterligere begrenset av **Filter**-innstillingene i denne dialogboksen.

1. Hvis du vil begrense settet med poster som denne satsvise jobben skal kjøres på, går du til hurtigfanen **Poster som skal inkluderes**, og velger **Filter** for å åpne dialogboksen **Forespørsel**. Denne dialogbosen fungerer på samme måte som den fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. På hurtigfanen **Kjør i bakgrunnen** angir du hvordan, når og hvor ofte de valgte beregningene skal utføres for de valgte varene. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å legge til den nye jobben i en satsvis kø for kjøring.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Gå gjennom og beregn utkoblede leveringstider på nytt for alle varer

Følg denne fremgangsmåten for å gå gjennom og beregne alle utkoblede leveringstider som er tilgjengelige i den juridiske enheten (firmaet), på nytt.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Utkoblet leveringstid**.
1. På siden **Utkoblet leveringstid** blar du gjennom og filtrerer listen etter behov for å finne informasjonen du leter etter. Hvis du vil vise enda mer informasjon for en vare, velger du koblingen i **Varenummer**-kolonnen.
1. Hvis du vil beregne den utkoblede leveringstiden på nytt for en hvilken som helst vare, velger du varen og velger deretter **Beregn utkoblet leveringstid** i handlingsruten. Dialogboksen **Beregn utkoblet leveringstid** vises. Denne dialogboksen fungerer på samme måte som den gjør når du [beregner utkoblede leveringstider](#calc-lead-time) for den samme varen på **Varedekning**-siden.
