---
title: Prioritetsbasert planlegging
description: Dette emnet beskriver funksjonen for prioritetsbasert planlegging i Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: bdca7ef99716cebee5c4eb41d1e51793b9468dd4
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468307"
---
# <a name="priority-based-planning"></a>Prioritetsbasert planlegging

[!include [banner](../../includes/banner.md)]

Dette emnet beskriver funksjonen for prioritetsbasert planlegging i Microsoft Dynamics 365 Supply Chain Management. Funksjonen gir støtte for etterspørselsdrevet planlegging, som er ett trinn i DDMRP (etterspørselsdrevet planlegging av materialkrav). Prioritetsbasert planlegging gjør det mulig for Planleggingsoptimalisering å generere planlagte bestillinger som drives av planleggingsprioriteter i stedet for behovsdatoer.

Med prioritetsbasert planlegging kan du prioritere etterfyllingsordrer for å sikre at behovet prioriteres over mindre viktig etterspørsel. En etterfyllingsordre for manko blir for eksempel prioritert over en standard etterfyllingsordre for påfylling. Systemet kan automatisk dele større ordrer i separate mindre ordrer, der ordrelinjer grupperes etter prioritet. Det kan deretter behandle alle ordrer med høy prioritet først.

Hvis du vil ha en rask oversikt over denne funksjonen, kan du se følgende video: [Støtte for Planleggingsoptimalisering for prioritetsbasert planlegging i Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Aktiver prioritetsbasert planlegging i systemet

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *Prioritetsdrevet MRP-støtte for planleggingsoptimalisering*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Hvor og hvordan planleggingsprioriteter tilordnes

Informasjon om *planleggingsprioritet* for tilbud og etterspørsel er ryggraden i prioritetsbasert planlegging. Planleggingsprioritet definerer viktigheten av en en etterspørsels- eller forsyningslinje. Planleggingsoptimalisering bruker dette når **Dekningskode**-feltet er satt til *Prioritet*.

Planleggingsprioriteten er vanligvis et tall mellom 0 (null) og 100, der 0 representerer den høyeste viktigheten. Den vises og angis i **Planleggingsprioritet**-feltet. Du finner dette feltet på følgende sider: **Behovsprognoselinjer**, **Salgsordredetaljer**, **Bestillingsdetaljer**, **Overføringsordredetaljer** og **Detaljer om planlagt bestilling**.

Når **Dekningskode**-feltet for den relevante varen eller dekningsgruppen er satt til *Prioritet*, balanserer Planleggingsoptimalisering forsyning med behov ved å bruke en behovsdrevet tilnærming når det beregner planleggingsprioriteten, og for hvert frigitte produkt vurderes verdiene som er angitt for feltene **Minimum**, **Gjenbestillingspunkt** og **Maksimum** på **Varedekning**-siden.

> [!NOTE]
> *Prioritet*-verdien er bare tilgjengelig for **Dekningskode**-feltet når Planleggingsoptimalisering er aktivert.

De relaterte *planleggingsprioritetsmodellene* styrer planleggingsprioriteten og deler planlagte bestillinger etter prioritetsområde. Du kan også angi standard planleggingsprioritetsverdier for hver tilbuds- eller behovstype, og definere beregningsmåten for prioritet.

## <a name="types-of-priority-calculation-methods"></a>Typer beregningsmetoder for prioritet

Hver planleggingsprioritetsmodell har en innstilling for **prioritetsberegningsmetode** som kontrollerer hvordan hovedplanlegging bruker prioritet for planlagte bestillinger. De tilgjengelige verdiene er *Prosent av maksimalt lagerantall* og *Prioritetsområder*. *Prioritetsområder* representerer en mer avansert versjon av metoden *Prosent av maksimalt lagerantall*.

### <a name="percent-of-maximum-inventory-quantity"></a>Prosent av maksimalt lagerantall

I beregningsmåten *Prosent av maksimalt lagerantall* finner beregning av forsyningsprioriteten det gjeldende *totalt tilgjengelig beholdning* (nettoflyt) som en prosent av verdien for **Maksimalt lagerantall** som er definert for en vare. Én enkelt planlagt bestilling opprettes deretter per vare og leverandør (med mindre maksimalt ordreantall brukes til å tvinge en deling). Planleggingsprioriteten for ordren blir beregnet som en prosent av maksimumsverdien.

Følgende formel brukes:

*Prosent av maksimum* = (*nettoflytposisjon* × 100) ÷ *verdien for maksimalt lagerantall fra varedekningen*

I denne formelen beregnes *nettoflytposisjon* på følgende måte:

*Nettoflytposisjon* = *tilgjengelig* + *i bestilling* – *kvalifisert behov*

- *I bestilling* er den forventede forsyningen.
- *Kvalifisert behov* representerer nettobehovene som har behovsdatoen innen planleggingshorisonten.

Under hovedplanleggingen blir det opprettet nye planlagte bestillinger når nettoflytposisjonen er mindre enn antallet for gjenbestillingspunkt for en vare. Det planlagte ordreantallet er forskjellen mellom verdien for **Maksimalt lagerantall** som er angitt på varenivå og nettoflytposisjon. Prioriteten for den planlagte bestillingen beregnes som en prosentverdi for *nettoflytposisjon* av verdien for **Maksimalt lagerantall**.

> [!NOTE]
> Den beregnede prioriteten kan ikke være negativ, selv om behovet overskrider total forsyning. Hvis behovet overskrider den totale forsyningen, blir den beregnede prioriteten satt til 0 (null).

### <a name="priority-ranges"></a>Prioritetsområder

Beregningsmåten for *prioritetsområder* er mer avansert enn metoden *Prosent av maksimalt lagerantall*, og konfigureres på nivået til planleggingsprioritetsmodellen. Flere nye planlagte forsyningsordrer kan opprettes for å tilfredsstille behovet per vare. Prioritetene for den planlagte forsyningen følger verdiene som er definert i rutenettet **Områder for planleggingsprioritet** på siden **Modeller for planleggingsprioritet**.

Følgende tilleggsregler blir gjeldende når feltet **Beregningsmetode for prioritet** settes til *Prioritetsområder*:

- Hvis alternativet **Vurder behovsprioritet** for den planlagte prioritetsmodellen er satt til *Ja*, vil prioritet som er angitt på hver behovslinje, begrense prioritetsområdesamlingen. Prioriteten til nye, planlagte forsyningsordrer vil ikke være lavere enn behovets prioritet. Områdets øvre verdi regnes som en terskel som behovets prioritetsverdi sammenlignes med. Hvis behovets prioritet er nøyaktig i midten mellom de øvre terskelverdiene for to områder, velges området som har høyest prioritet (det vil si den laveste prioritetsverdien).
- Hvis feltet **Planlagt ordreoppretting** for den planlagte prioritetsmodellen er satt til *Enkelt forsyning med viktigst prioritet*, opprettes bare én forsyning for å oppfylle hele opp til maksimumsverdien. Prioriteten settes til prioriteten for det første området som vil utløse en forsyning.
- Hvis det ikke er lagerbeholdning, ingen forsyning og ingen etterspørsel, vil linjen i rutenettet **Områder for planleggingsprioritet** der **Fra antall**-feltet er satt til *Null*, brukes.
- Hvis det er behov, men ikke lagerbeholdning eller forventet forsyning, vil linjen i rutenettet **Områder for planleggingsprioritet** der **Fra antall**-feltet er satt til *Null eller mindre*, brukes.
- Når området som behovet er en del av, blir evaluert, vil innstillingen for alternativet **Vurder behovsprioritet** fremdeles ha en virkning.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Forskjeller mellom tradisjonelle tidslinjeberegninger og prioritetsbasert planlegging

Prioritetsbasert planlegging avviker fra tradisjonelle tidslinjeberegninger på følgende måter:

- Alle de vanlige forhåndsplanleggingsprosessorene er fremdeles gjeldende. Disse forhåndsprosessorene omfatter utligning av godkjente planlagte ordrer mot salgsbehov, tilordning av innkjøpsrekvisisjon og reservasjonslogikk. Bare etterspørselen som disse forhåndsprosessorene ikke oppfyller, behandles.
- Ved utligning vurderes all forsyning, uansett prioritet. Denne forsyningen omfatter lagerbeholdning, frigitt forsyning og den ikke-utlignede delen av godkjente planlagte bestillinger.
- Ingen negative dager-behov kan utlignes mot forsyning under hele dekningstiden.
- Når forsyningen utlignes mot etterspørsel, brukes forsyningen som har høyest prioritet (det vil si den laveste prioritetsverdien), først. Lagerbeholdning vurderes å ha prioritetsverdien 0 (null). Derfor vil den bli brukt som den aller første kilden.
- Nye planlagte forsyningslinjer blir opprettet i henhold til de vanlige reglene for minimum ordrestørrelse, maksimal ordrestørrelse, multiplumsantall og så videre.

## <a name="planning-priority-models"></a>Modeller for planleggingsprioritet

*Modeller for planleggingsprioritet* tilordnes dekningsgrupper og kontrollerer planleggingsprioriteten for planlagte bestillinger. De definerer logikken som bestemmer hvordan planleggingens prioritetsverdi beregnes for hver planlagte bestilling, og hvordan prioritet tilordnes planlagte bestillinger, forsyningslinjer og behovslinjer.

Hvis du vil arbeide med modellene for planleggingsprioritet, kan du gå til **Hovedplanlegging \> Oppsett \> Modeller for planleggingsprioritet**. Som det ble omtalt tidligere, er verdien for **Beregningsmetode for prioritet** en av de viktigste innstillingene for en modell. Denne innstillingen styrer beregningsmetoden som brukes når hovedplanlegging tilordner en prioritetsverdi til planlagte bestillinger.

> [!NOTE]
> Modeller for planleggingsprioritet gjelder hele organisasjonen, på tvers av alle juridiske enheter.

### <a name="coverage-group"></a>Dekningsgruppe

Definer en ny dekningsgruppe som du planlegger å bruke for prioritetsbasert planlegging, som beskrevet i [Definer dekningsregler for varer](../tasks/define-coverage-rules-items.md). Når du har opprettet dekningsgruppen, angir du følgende tilleggsfelter:

- **Dekningskode** – Velg *Prioritet* hvis dekningsgruppen skal bruke prioritetsbasert planlegging.
- **Modell for planleggingsprioritet** – Velg en hvilken som helst modell for planleggingsprioritet for hele organisasjonen.

### <a name="item-coverage"></a>Varedekning

Definer varedekningsinnstillinger som beskrevet i [Dekningsinnstillinger](../coverage-settings.md). Som standard kopieres verdien for **Dekningskode** som er valgt for dekningsgruppen, til varedekningsinnstillingene. Du kan imidlertid overstyre standardverdien etter behov. I noen tilfeller er **Dekningskode**-feltet for en varedekningspost satt til *Planlegging*, men ingen modell for planleggingsprioritet er definert for den relaterte dekningsgruppen. I disse tilfellene blir alle modeller der feltet **Beregningsmetode for prioritet** er satt til *Prosent av maksimalt lagerantall*, og feltet **Planlagt ordreoppretting** er satt til *Enkelt forsyning med viktigst prioritet*, brukt som standard.

Sett **Dekningskode**-feltet til *Prioritet* for å gjøre feltet **Gjenbestillingspunkt** i innstillingene for varedekning tilgjengelig. I dette feltet angir du antallet for gjenbestillingspunkt som systemet skal bruke mens det bestemmer når planlagte bestillinger med **Dekningskode**-verdien *Prioritet*, skal plasseres.

Antallet for gjenbestillingspunkt beregnes ofte som behovet i løpet av leveringstiden pluss en minimumsverdi (sikkerhetslager). Det må være en verdi mellom **Minimum**- og **Maksimum**-verdiene.

Du kan for eksempel angi feltene på følgende måte:

- **Minimum:** *10*
- **Gjenbestillingspunkt:** *45*
- **Maksimum:** *60*

Antallet for gjenbestillingspunkt er for eksempel basert på en leveringstid på sju dager og gjennomsnittlig daglig bruk på 5. Derfor er behovet i leveringstiden 35. Minimumsverdien på 10 (sikkerhetslager) legges deretter til for å få et gjenbestillingspunkt på 45. Når dette oppsettet brukes, vil forsyningen foreslås når prosjektert lagerbeholdningsnivå er under 45. Ordreprioriteten blir basert på oppsettet av planleggingsprioritet.

### <a name="manage-planning-priority-models"></a>Administrer modeller for planleggingsprioritet

Slik arbeider du med modeller for planleggingsprioritet Følg disse trinnene:

1. Gå til **Hovedplanlegging \> Oppsett \> Modeller for planleggingsprioritet**.
1. Velg en eksisterende modell i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny modell.
1. I toppteksten for den nye posten angir du følgende felt:

    - **Navn** – Angi et navn for modellen. Navnet må være unikt på tvers av alle juridiske enheter i organisasjonen.
    - **Beskrivelse** – Angi en beskrivelse av modellen.
    - **Beregningsmetode for prioritet** – Velg en av følgende verdier:

        - *Prioritetsområder* – Når du velger denne verdien, blir rutenettet **Områder for planleggingsprioritet** tilgjengelig. Der må du opprette flere prioritetsområder for å definere planleggingsprioritetsverdien.
        - *Prosent av maksimalt lagerantall* – Beregn planleggingsprioritetsverdien som en prosent, basert på prosjektert lagernivå over det maksimale lagerantallet.

    - **Planlagt ordreoppretting** – Dette feltet er tilgjengelig når feltet **Beregningsmetode for prioritet** er satt til *Prioritetsområder*. Velg én av følgende verdier:

        - *Enkelt forsyning med viktigst prioritet* – Ikke del planlagte bestillinger basert på prioritetsområdet. Planleggingsprioriteten for en planlagt bestilling er basert på det viktigste prioritetsområdet (det vil si den laveste planleggingsprioritetsverdien).
        - *Del i henhold til prioritetsområder* – Del behovet inn i flere planlagte bestillinger basert på planleggingsprioritetsområdene. Planleggingsprioriteten for individuelle planlagte bestillinger er definert av planleggingsprioriteten for det relaterte planleggingsprioritetsområdet.

    - **Vurder behovsprioritet** – Sett dette alternativet til *Ja* for å begrense prioriteten til en ny planlagt bestilling som er opprettet for forsyning. (Prioriteten vil ikke være lavere enn den tilknyttede behovsprioriteten.) Hvis du setter dette alternativet til *Nei*, vil det ikke tas hensyn til behovsordreprioriteten når forsyningsordreprioriteten beregnes.

1. Hvis du setter feltet **Beregningsmetode for prioritet** til *Prioritetsområder*, bruker du knappene **Legg til** og **Fjern** på verktøylinjen på hurtigfanen **Områder for planleggingsprioritet** til å legge til eller fjerne prioritetsområderader etter behov. Hvis det finnes flere rader, og du setter inn en ny rad, settes planleggingsprioriteten automatisk til gjennomsnittet for den valgte raden og raden over. For hver rad angir du feltene nedenfor:

    - **Planleggingsprioritet** – Angi en verdi mellom 0,00 og 100,00. Denne verdien representerer planleggingsprioriteten som brukes for raden. Laveste verdi for prioritet representerer høyeste prioritet. En standardverdi er tilordnet, men du kan endre den etter behov. Den samme verdien for **Planleggingsprioritet** kan ikke brukes for mer enn ett planleggingsprioritetsområde i den samme planleggingsprioritetsmodellen.
    - **Beskrivelse** – Skriv inn en beskrivelse av planleggingsprioritetsområdet (for eksempel *Gjenbestillingspunkt til maksimum*).
    - **Fra antall** – Den nedre grensen til planleggingsprioritetsområdet. Denne verdien er skrivebeskyttet, og er basert på verdiene for **Til-antall** og **Prosent av Til-antall** for det forrige planleggingsprioritetsområdet.
    - **Til-antall** – Velg feltet fra varedekningen som skal brukes til å definere områdets øvre grense. Følgende verdier støttes og vil påvirke verdien for **Fra-antall** for neste område:

        - *Null* – Denne verdien representerer et område fra negativt til null (*Null eller mindre* til *Null*). For rader der denne verdien er valgt, er feltet **Prosent av til-antall** skrivebeskyttet og blir alltid satt til *100* prosent.
        - *Minimum lagerantall* – Denne verdien representerer **Minimum**-verdien for en vare på siden **Varedekning**. For rader der denne verdien er valgt, kan feltet **Prosent av til-antall** redigeres, og det brukes til å angi verdien for **Fra-antall** for det neste området (for eksempel til *80 % av Minimum lagerantall*).
        - *Gjenbestillingspunkt* – Denne verdien representerer verdien for **Gjenbestillingspunkt** for en vare på siden **Varedekning**. For rader der denne verdien er valgt, kan feltet **Prosent av til-antall** redigeres, og det brukes til å angi verdien for **Fra-antall** for det neste området (for eksempel til *80 % av Gjenbestillingspunkt*).
        - *Maksimum lagerantall* – Denne verdien representerer **Maksimum**-verdien for en vare på siden **Varedekning**. For rader der denne verdien er valgt, kan feltet **Prosent av til-antall** redigeres, og det brukes til å angi **Fra-antall** for det neste området (for eksempel til *80 % av Minimum lagerantall*).
        - *Ubegrenset* – Denne verdien representerer et ubegrenset øvre nivå i området (*Ubegrenset eller mindre* til *Ubegrenset*). For rader der denne verdien er valgt, er feltet **Prosent av til-antall** skrivebeskyttet og blir alltid satt til *100* prosent.

    - **Prosent av til-antall** – Angi en prosentverdi som skal brukes til å beregne den øvre grensen til området for planleggingsprioritet, basert på verdien som er valgt i feltet **Til-antall**. Hvis for eksempel feltet **Til-antall** er angitt til *Minimum lagerantall* og feltet **Prosent av til-antall** er angitt til *50*, vil den øvre grensen være 50 prosent av minimum lageranttal fra den relaterte varedekningen.

1. På hurtigfanen **Standarder for planleggingsprioritet** angir du feltene etter behov for å definere standard planleggingsprioritet for hver type forsynings- eller behovslinje (salgsordre, bestilling, overføringsordre eller behovsprognose). Bare positive verdier kan angis.

## <a name="view-and-maintain-planning-priority"></a>Vis og oppretthold planleggingsprioritet

Planleggingsprioriteten vises og angis i feltet **Planleggingsprioritet**. Du finner dette feltet på sidene som vises i følgende tabell. Prioriteten er angitt som et tall mellom 0 (null) og 100, der 0 representerer den høyeste viktigheten.

| Side | Feltlokasjon | Verdikilde |
|---|---|---|
| Behovsprognoselinjer | <p>**Vare**-fanen</p><p>(Velg en linje i den øvre delen, og velg deretter **Vare**-fanen.)</p> | Standardverdi eller verdi som er angitt manuelt |
| Salgsordredetaljer | <p>**Levering**-fanen på hurtigfanen **Linjedetaljer**</p><p>(Velg en linje på hurtigfanen **Salgsordrelinjer**, og gå deretter til hurtigfanen **Linjedetaljer** og velg **Levering**-fanen.)</p> | Standardverdi, konsernintern verdi eller verdi som er angitt manuelt |
| Bestillingsdetaljer | <p>**Levering**-fanen på hurtigfanen **Linjedetaljer**</p><p>(Velg en linje på hurtigfanen **Bestillingslinjer**, og gå deretter til hurtigfanen **Linjedetaljer** og velg **Levering**-fanen.)</p> | Verdi som er angitt under autorisering fra planlagte ordrer, konsernintern verdi eller verdi som er angitt manuelt |
| Overføringsordredetaljer | <p>**Levering**-fanen på hurtigfanen **Linjedetaljer**</p><p>(Velg en linje på hurtigfanen **Overføringsordrelinjer**, og gå deretter til hurtigfanen **Linjedetaljer** og velg **Levering**-fanen.)</p> | Verdi som er angitt under autorisering fra planlagte ordrer, eller verdi som er angitt manuelt |
| Detaljer for planlagt bestilling | Hurtigfanen **Generelt** | Verdi som beregnes under hovedplanlegging, eller verdi som er angitt manuelt |

### <a name="intercompany-trade"></a>Konsernintern handel

Verdien for **Planleggingsprioritet** for konserninterne forsynings- og behovslinjer deles mellom de koblede enhetene. En endring på hver side vil gjenspeiles på den koblede ordrelinjen.

Her er noen eksempler:

- En bruker endrer planleggingsprioriteten for en konsernintern salgsordrelinje fra 20 til 30. Denne endringen gjenspeiles på den koblede konserninterne bestillingslinjen.
- En bruker endrer planleggingsprioriteten for en konsernintern bestillingslinje fra 40 til 50. Denne endringen gjenspeiles på den koblede konserninterne salgsordrelinjen.
