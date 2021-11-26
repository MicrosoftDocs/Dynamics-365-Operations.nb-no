---
title: Bruk sikkerhetslagerjournalen til å oppdatere minste dekning for varer
description: Dette emnet beskriver hvordan du bruker sikkerhetslagerhournalen til å oppdatere sikkerhetslagerantall for varer ved å beregne minimumsdekningsforslag basert på historiske transaksjoner.
author: ChristianRytt
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 59e4959898cd961582e1ac1d2285c0c0867ee7af
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790987"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Bruk sikkerhetslagerjournalen til å oppdatere minste dekning for varer

[!include [banner](../../includes/banner.md)]

Sikkerhetslager angir en tilleggsmengde for en vare som er på lageret, for å redusere risikoen for at varen er utsolgt. Sikkerhetslager brukes som et reservelager i tilfelle salgsordrer kommer inn, men leverandøren kan oppfylle kundens ønskede leveringsdato.

Dette emnet beskriver hvordan du bruker sikkerhetslagerjournalen til å beregne minste dekningsforslag basert på historiske transaksjoner, og deretter oppdaterer varedekningen med forslagene.

## <a name="overview-of-minimum-coverage-usage"></a>Oversikt over minimum dekningsbruk

Sikkerhetslager defineres på siden **Varedekning** for hver vare. Forskjellige etterfyllingstyper representeres av forskjellige dekningskoder. (Hvis du vil ha mer informasjon, kan du se [Fullføring av sikkerhetslager for varer](safety-stock-replenishment.md).) Alle dekningskoder bruker imidlertid verdien som er angitt i **Minimum**-feltet på **Varedekning**-siden for hver vare. Det finnes to hovedtilnærminger for bruk av **Minimum**-feltet:

- **Minimumsantall for min/maks-formål** – Denne tilnærmingen bruker minimumsantallet sammen med min/maks-logikk. Dette gjelder når **Dekningskode**-feltet er satt til *Min/maks* for den relevante varen eller dekningsgruppen. **Minimum**-antallet representerer gjennomsnittlig daglig bruk multiplisert med varens leveringstid.
- **Minimumsantall for lagerplanformål** – Denne tilnærmingen bruker minimumsantallet til å representere en lagerplan i kombinasjon med behovsprognoser. Dette gjelder når **Dekningskode**-feltet er satt til *Periode* eller *Krav* for den relevante varen eller dekningsgruppen. **Minimum**-antallet representerer en lagerplan som gjenspeiler ønsket kundeservicenivå for å redusere lagerbeholdning, delvise forsendelser og leveringstider. Minimumsantallet gjenspeiler en prosent av prognosenøyaktigheten for en angitt vare. Det representerer ikke ønsket lagerposisjon.

**Minimum**-verdien kan angis på tre måter:

- Manuelt på siden **Varedekning**
- Via dataadministrasjonsrammeverket (*Varedekning*-dataenheter)
- Via beregningen av sikkerhetslager som utføres av journaler for sikkerhetslager

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Beregning av minimumsdekning basert på historisk bruk

Journaler for sikkerhetslager brukes til å beregne et foreslått minimumsantall basert på varens historiske bruk, enten for minimums-/maksimumsformål eller for lagerplanformål. Historisk bruk representerer alle avgangstransaksjoner i løpet av en bestemt periode. Disse avgangstransaksjonene omfatter salgsordretransaksjoner og lagerjusteringer. Beregningene identifiserer også virkningen av det foreslåtte minimumsantallet på lagerverdi og endring i lagerverdi sammenlignet med gjeldende minimumsantall.

Hver journallinje for sikkerhetslager representerer en vare og dens dekningsdimensjoner. Disse journallinjene opprettes og vises på siden **Journallinjer for sikkerhetslager** (**Hovedplanlegging \> Hovedplanlegging \> Kjør \> Beregning av sikkerhetslager**). Forretningsprosessen for bruk av journaler for sikkerhetslager til å beregne de foreslåtte minimumsantallene, beskrives senere i dette emnet.

Planleggeren bruker en sikkerhetslagerjournal til å beregne foreslåtte minimumsantall for valgte varer, basert på historisk bruk i valgte perioder. De foreslåtte minimumsverdiene kan overstyres manuelt etter behov, og du kan gå gjennom de potensielle virkningene av de foreslåtte minimumene på lagerverdi. Når journalen er postert, oppdateres de tilknyttede minimumsantallene i varedekningen automatisk.

### <a name="create-a-new-safety-stock-journal-name"></a>Opprette en nytt journalnavn for sikkerhetslager

Du må opprette minst ett journalnavn for sikkerhetslager før du kan generere denne typen journal. Det kan hende at du vanligvis bruker flere journalnavn som en hjelp til å skille beregningen av sikkerhetslager.

1. Gå til **Hovedplanlegging \> Oppsett \> Journalnavn for sikkerhetslager**.
1. Velg **Ny** i handlingsruten.
1. Angi følgende felter på den nye linjen:

    - **Navn** – Angi et kort navn for journalen.
    - **Beskrivelse** – Angi en beskrivelse av journalen.
    - **Privat for brukergruppe** – Velg en brukergruppe for å begrense målgruppen for gjeldende journalnavn.
    - **Slett linjer etter postering** – Merk av i denne avmerkingsboksen for å fjerne journallinjer som standard når du posterer dem. Fjern merket hvis du vil beholde alle posterte linjer.

    **Journaltype**-feltet er skrivebeskyttet og er forhåndsinnstilt til *Sikkerhetslager*.

1. Lukk siden.

### <a name="create-a-safety-stock-journal-and-lines"></a>Opprett en sikkerhetslagerjournal og -linjer

Dette trinnet oppretter en journal og legger til linjer automatisk i den. Hver linje identifiserer en vare, dekningsdimensjonene og diverse beregnede antall fra brukshistorikken. De beregnede antallene omfatter gjennomsnittlig avgang per leveringstid for vare, gjennomsnittlig avgang per måned og månedlig standardavvik.

#### <a name="automatically-generate-journal-lines"></a>Generer journallinjer automatisk

Journallinjer kan bare genereres automatisk hvis det ikke finnes linjer for journalen som vises for øyeblikket.

Følg denne fremgangsmåten for å generere journallinjer automatisk.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Beregning av sikkerhetslager**.
1. Velg **Ny** i handlingsruten. En ny sikkerhetslagerjournal er opprettet.
1. På hurtigfanen **Journalhodedetaljer** angir du følgende felter:

    - **Navn** – Velg navnet på sikkerhetslagerjournalen der du vil legge til linjen.
    - **Beskrivelse** – Standardverdien er beskrivelsen av journalnavnet du har valgt. Du kan imidlertid redigere verdien etter behov.
    - **Slett linjer etter postering** – Merk av i denne avmerkingsboksen for å fjerne journallinjer når du posterer dem. Fjern merket hvis du vil beholde alle posterte linjer. Innstillingen arves fra det valgte journalnavnet.

    **Journal**-feltet er skrivebeskyttet, og viser ID-nummeret til journalen som du oppretter og legger til linjer i.

1. På hurtigfanen **Journallinjer** velger du **Opprett linjer** på verktøylinjen.
1. I dialogboksen **Opprett journallinjer for foreslåtte minimumslagernivåer** definerer du følgende felter:

    - **Fra dato** – Velg startdatoen for perioden som avganger skal tas med i beregningen for.
    - **Til dato** – Velg sluttdatoen for perioden som avganger skal tas med i denne beregningen for. Det må være minst to måneder mellom start- og sluttdatoene.
    - **Beregn standardavvik** – Sett dette alternativet til *Ja* for å beregne standardavviket. Du må sette dette alternativet til *Ja* hvis du vil bruke alternativet **Bruk servicenivå** når du beregner forslaget (som beskrevet senere i dette emnet).

1. På hurtigfanen **Poster som skal inkluderes** kan du definere du filtre og betingelser for å definere hvilke varer som skal tas med. (Du kan for eksempel filtrere etter **Dekningsgruppe**-verdien.) Velg **Filter** for å åpne en standard dialogboks i redigeringsprogrammet for spørring, der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Microsoft Dynamics 365 Supply Chain Management.
1. På hurtigfanen **Kjør i bakgrunnen** velger du om jobben slik skal kjøres i satsvis modus, og/eller angir en gjentakende tidsplan. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK**. Linjer opprettes for dimensjonene som har lagertransaksjoner.

#### <a name="manually-add-or-remove-journal-lines"></a>Legg til eller fjern journallinjer manuelt

Du kan når som helst legge til og/eller fjerne journallinjer manuelt (enten etter eller i stedet for automatisk generering av linjer). Bruk følgende knapper på verktøylinjen på hurtigfanen **Journallinjer**:

- **Ny** – Legg til en ny linje. Angi deretter en verdi i hver kolonne for å definere produktet som skal beregnes, og som nye minimumsverdier skal brukes for. Fordi foreslåtte minimumsberegninger ikke er tilgjengelige for linjer som er lagt til manuelt, vises ingen nye verdier for **beregnet minimumsantall** for dem. Derfor må du manuelt angi **nye minimumsantallsverdier**. Du kan imidlertid fremdeles vise den potensielle virkningen av den **nye minimumsantallsverdien** på lagerverdien og den potensielle endringen i lageret sammenlignet med minimumsverdien som er angitt for øyeblikket.
- **Slett** – Slett den valgte linjen.
- **Slett journallinjer** – Slett alle linjene i journalen.

### <a name="calculate-a-proposal"></a>Beregn et forslag

Dette trinnet beregner et foreslått minimum for hver journallinje og linjens potensielle innvirkning på lagerverdien. (Den foreslåtte minimumsverdien vises som verdien **Beregnet minimumsantall**.) Du kan utføre beregningen flere ganger etter behov. Beregningen oppdaterer verdien for **Beregnet minimumsantall** som vises for alle journallinjer.

Beregningene som vises, vil ikke påvirke de faktiske verdiene for minimumsantall for hvert produkt før du velger **Poster** i handlingsruten. Da brukes verdiene under **Nytt minimumsantall** for hvert produkt.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Beregning av sikkerhetslager**.
1. Åpne journalen det skal beregnes et forslag for. Du kan også opprette en ny journal slik det er beskrevet tidligere i dette emnet.
1. På hurtigfanen **Journallinjer** velger du **Beregn forslag** på verktøylinjen. (Du trenger ikke merke noen linjer.)
1. I dialogboksen **Beregn forslag for minimumslagernivå** definerer du følgende felter:

    - **Bruk gjennomsnittlig avgang i leveringstid** – Velg dette alternativet hvis du vil generere verdier for **Beregn minimumsantall** basert på gjennomsnittlig avgang i den angitte perioden. Deretter angir du en verdi i feltet **Multiplikasjonsfaktor** for å justere resultatet etter behov. Du kan for eksempel angi *1,0* for å bruke nøyaktig beregnet gjennomsnitt, eller *1,1* for å legge til en ekstra buffer på 10 prosent.
    - **Bruk servicenivå** – Velg dette alternativet hvis du vil beregne et foreslått minimum basert på ønsket servicenivå. Velg deretter foretrukket servicenivå i **Servicenivå**-feltet.
    - **Leveringstidsmargin** – Angi en verdi som den normale leveringstiden skal forlenges med (for eksempel hvis du vil tillate administrasjon).
    - **Bruk det beregnede minimumsantallet som det nye minimumsantallet** – Sett dette alternativet til *Ja* for å automatisk kopiere verdier fra kolonnen **Beregnet minimumsantall** til kolonnen **Nytt minimumsantall** for alle liner etter at beregningen er fullført. Hvis du setter dette alternativet til *Nei*, blir verdien **Gjeldende minimumsantall** kopiert til kolonnen **Nytt minimumsantall** for alle linjer. Deretter må du manuelt redigere verdiene for **Nytt minimumsantall** etter behov.

1. På hurtigfanen **Kjør i bakgrunnen** velger du om jobben slik skal kjøres i satsvis modus, og/eller angir en gjentakende tidsplan. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK**. Resultatet av beregningen vises i kolonnen **Beregnet minimumsantall** på hurtigfanen **Journallinjer**. For øyeblikket er verdiene bare foreslåtte verdier som ennå ikke er brukt på produktene.

### <a name="update-minimum-quantity"></a>Oppdatere minimumsantall

Du kan velge en hvilken som helst linje i en sikkerhetslagerjournal og manuelt overstyre verdien i feltet **Nytt minimumsantall**.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Beregning av sikkerhetslager**.
1. Åpne journalen som skal redigeres. Du kan også opprette en ny journal slik det er beskrevet tidligere.
1. Finn linjen som skal justeres, på hurtigfanen **Journallinjer**, og rediger deretter verdien i kolonnen **Nytt minimumsantall**. Du kan for eksempel angi verdien for **Nytt minimumsantall**, slik at den samsvarer med verdien for **Beregnet minimumsantall**. Hvis verdien for **Beregnet minimumsantall** er *0* (null), kan du angi ønsket fremtidig verdi.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Postere det nye minimumsantallet og validere resultatet

Følg disse trinnene for å postere det nye minimumsantallet og validere resultatet.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Beregning av sikkerhetslager**.
1. Åpne journalen du vil postere nye minimumsantall for. Du kan også opprette en ny journal slik det er beskrevet tidligere.
1. Velg **Poster** i handlingsruten.
1. I dialogboksen **Poster journal** angir du feltet **Overfør alle posteringsfeil til en ny journal** etter behov. Velg deretter **OK** for å postere journalen.
1. Hvis du endret verdien for **Nytt minimumsantall** for en linje på hurtigfanen **Journallinjer**, kan du bekrefte endringen ved å følge disse trinnene:

    1. For linjen du redigerte, velger du koblingen i **Varenummer**-kolonnen.
    1. I dialogboksen **Produktinformasjon** velger du koblingen i feltet **Varenummer** for å åpne den relaterte frigitte produktposten.
    1. Velg **Varedekning** i **Dekning**-gruppen i **Plan**-fanen i handlingsruten.
    1. Legg merke til at **Minimum**-verdien for området og lageret du justerte ved å bruke den posterte sikkerhetslagerjournalen, nå er oppdatert slik at den stemmer overens med redigeringen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Fullføring av sikkerhetslager for varer](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
