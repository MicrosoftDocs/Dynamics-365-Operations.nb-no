---
title: Autoriser planlagte ordrer
description: Denne artikkelen beskriver hvordan du autoriserer planlagte ordrer. Når planlagte bestillinger autoriseres, blir de faktiske bestillinger, overføringsordrer eller produksjonsordrer.
author: t-benebo
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 24b5c6cb7e97924ebace8f7131a87e9bffea22e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857525"
---
# <a name="firm-planned-orders"></a>Autoriser planlagte ordrer

[!include [banner](../../includes/banner.md)]

Planlagte bestillinger må *autoriseres* (det vil si frigis) som en del av hovedplanleggingsprosessen. Når planlagte bestillinger autoriseres, blir de faktiske bestillinger, overføringsordrer eller produksjonsordrer. Disse ordrene kalles også *frigitte ordrer* eller *åpne ordrer*.

Det finnes tre metoder for autorisering av planlagte bestillinger:

- **Manuell autorisering** – Velg bestemte planlagte bestillinger i en liste, og start deretter prosessen manuelt.
- **Automatisk autorisasjon** – Definer en standard autorisasjonshorisont for dekningsgrupper, individuelle varer og kombinasjoner av varer og hovedplaner. I løpet av hovedplanleggingen vil planlagte bestillinger automatisk bli autorisert hvis ordredatoen er innenfor den angitte horisonten for autorisering.
- **Spørringsbasert autorisering** – Definer en spørring for å velge planlagte ordrer basert på egenskapene. Du kan sette opp en satsvis jobb for å kjøre spørringen og autorisere samsvarsordrer regelmessig.

I denne artikkelen beskrives hver metode i detalj.

## <a name="enable-the-features-that-are-described-in-this-article"></a><a name="enable-features"></a>Aktivere funksjonene som er beskrevet i denne artikkelen

De fleste planlagte bestillingsfunksjoner er tilgjengelige i alle standardinstallasjoner av Microsoft Dynamics 365 Supply Chain Management som bruker Planleggingsoptimalisering. Noen av funksjonene som er beskrevet i denne artikkelen, må imidlertid aktiveres i Funksjonsadministrasjon før du kan bruke dem.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Aktivere eller deaktivere parallellisert autorisering av planlagte bestillinger

Parallell autorisering gjør det raskere å autorisere prosessen ved å parallellisere den over flere tråder. Denne fremgangsmåten kan være nyttig når mange planlagte bestillinger autoriseres. Du må aktivere funksjonen *Parallell autorisering av planlagte bestillinger* for systemet for å kunne bruke denne funksjonaliteten. Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management 10.0.25 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.25, kan du aktivere eller deaktivere denne funksjonaliteten ved å gå til [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og søke etter funksjonen *Parallell autorisering av planlagte bestillinger*.

### <a name="enable-planned-order-firming-with-filtering"></a>Aktivere autorisering av planlagt bestilling med filtrering

Med autorisering av planlagt bestilling med filtrering kan du definere logiske kriterier for å velge hvilke planlagte bestillinger som skal autoriseres. Du kan også forhåndsvise hvilke planlagte bestillinger som er valgt, kjøre prosessen i bakgrunnen og/eller planlegge det som en satsvis jobb.

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Autorisering av planlagt bestilling med filtrering* i arbeidsområdet [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="enable-auto-firming-for-planning-optimization"></a>Aktivere automatisk autorisasjon for planleggingsoptimalisering

Automatisk autorisering gjør det mulig å autorisere planlagte bestillinger som en del av hovedplanlegging-prosessen under horisonten for autorisering. Automatisk autorisering støttes alltid for planleggingsmotoren som er innebygd i Supply Chain Management. Hvis du også vil bruke det med planleggingsoptimalisering, må du aktivere funksjonen.

Hvis du vil gjøre denne funksjonaliteten tilgjengelig i systemet, kan du gå til [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Automatisk autorisasjon med planleggingsoptimalisering*. (Per Supply Chain Management versjon 10.0.21 er denne funksjonen aktivert som standard.)

## <a name="manually-firm-planned-orders"></a>Autorisere planlagte ordrer manuelt

Hvis du vil autorisere planlagte bestillinger manuelt, finner du og velger de planlagte bestillingene du vil autorisere, og deretter starter du autoriseringsprosessen manuelt.

1. [Åpne en hvilken som helst listeside for planlagte bestillinger](approved-planned-order.md#view-planned-orders).
1. Bruk **Filter**-feltet, **Plan**-feltet og kolonneoverskrifter til å filtrere og sortere listen slik at du kan finne de planlagte bestillingene du er på jakt etter.
1. Merk av i avmerkingsboksen for hver planlagte bestilling du vil autorisere. Hvis du vil autorisere alle de planlagte bestillingene som vises på siden (basert på filtrene du har brukt), kan du hoppe over dette trinnet.
1. Velg en av følgende knapper i handlingsruten:

    - **Autoriser** – Autoriser bare de valgte planlagte bestillingene.
    - **Autoriser alle** – Autoriser alle de planlagte bestillingene som vises på siden (basert på filtrene du brukte), uavhengig av avmerkingsboksene som er merket. Dette alternativet kan være nyttig hvis du autoriserer mange planlagte bestillinger.

1. I dialogboksen **Autorisasjon** angir du følgende felt i hurtigfanen **Parametere**. (Mange av disse feltene tar standardverdiene fra kategorien **Standardoppdatering** på siden **Parametere for hovedplanlegging**.)

    - **Oppdater merking** – Velg lagermerkingspolicyen som skal brukes under autorisering av planlagte bestillinger.
    - **Avbryt autorisasjon ved feil** – Sett dette alternativet til *Ja* for å stoppe autorisingen av alle valgte planlagte ordrer hvis det oppstår en feil på en av dem. Du må velge *Nei* hvis alternativet **Parallelliser autorisasjon** er satt til *Ja*.
    - **Parallelliser autorisasjon** – Dette alternativet er bare tilgjengelig hvis [*Parallell autorisering av planlagte bestillinger*-funksjonen](#enable-features) er aktivert i systemet, og hvis du har valgt to eller flere planlagte bestillinger for autorisasjon. Sett den til *Ja* for å kjøre autoriseringsprosessen parallelt. Parallell autorisering kan hjelpe deg med å forbedre ytelsen.
    - **Antall tråder** – Dette alternativet er bare tilgjengelig hvis [*Parallell autorisering av planlagte bestillinger*-funksjonen](#enable-features) er aktivert i systemet, og hvis du har satt alternativet **Parallelliser autorisasjon** til *Ja*. Angi antallet tråder som skal brukes til å parallellisere autoriseringsprosessen. Hvis du vil ha informasjon om hvordan du bruker dette alternativet i hovedplanlegging, kan du se [Forbedre ytelsen til hovedplanlegging](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Hvis du angir *0* (null) for feltet **Antall tråder**, øker kjøretiden for hovedplanlegging. Derfor anbefaler vi at du alltid angir en verdi i dette feltet som er større enn 0.

    - **Grupper etter leverandør** – Sett dette alternativet til *Ja* for å gruppere planlagte bestillinger og opprette én bestilling per leverandør under autorisering. Du kan også opprette én bestilling med en linje per planlagt bestilling.
    - **Grupper etter innkjøpergruppe** – Sett dette alternativet til *Ja* for å gruppere bestillingsforslag og opprette én bestilling som kombinerer leverandør- og innkjøpergruppen. Hvis du vil velge dette alternativet, må du også sette alternativet **Grupper etter leverandør** til *Ja*.
    - **Grupper etter innkjøpsavtale** – Sett dette alternativet til *Ja* for å gruppere planlagte bestillinger som har samme leverandør som eksisterende innkjøpsavtaler, og opprett én bestilling per bestillingsavtale. Dette alternativet blir automatisk aktivert når **Grupper etter leverandør** er aktivert. Hvis du vil bruke **Grupper etter kjøpsavtale**, må **Søk etter kjøpsavtaler** være satt til *Ja* på siden **Parametere for hovedplanlegging**.
    - **Grupper etter periode** (i **Bestillinger**-delen) – Velg perioden du vil gruppere planlagte bestillinger etter. Hvis du vil velge dette alternativet, må du også velge alternativet **Grupper etter leverandør**.
    - **Grupper etter periode** (i **Overføringer**-delen) – Velg perioden du vil gruppere planlagte overføringer etter. Ordrene blir gruppert basert på verdiene **Fra lager** og **Til lager**.

    > [!NOTE]
    > Hvert av alternativene Grupper etter fører til at systemet konverterer hver planlagte bestilling til en linje i den enkelte bestillingen som er resultatet av grupperingen.

    ![Parametere-hurtigfanen i dialogboksen Autorisasjon.](./media/manual-firming.png "Parametere-hurtigfanen i dialogboksen Autorisasjon")

1. I hurtigfanen **Kjør i bakgrunnen** definerer du jobben slik at den kjøres i satsvis modus. Det er imidlertid ingen vits i å definere en gjentakende tidsplan når du gjør manuell autorising. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management. For manuell autorisering vil imidlertid den satsvise jobben bare behandle de valgte planlagte ordrene. Den behandler ikke ordrer som passer til filtrene som for øyeblikket brukes på siden.
1. Velg **OK** for å bruke innstillingene og generere de autoriserte ordrene.

## <a name="auto-firm-planned-orders"></a>Autorisere planlagte ordrer automatisk

Automatisk autorisasjon gjør det mulig å autorisere planlagte bestillinger som en del av hovedplanlegging-prosessen. Du kan definere en standard autorisasjonshorisont for dekningsgrupper, individuelle varer og kombinasjoner av varer og hovedplaner. I løpet av hovedplanleggingen vil planlagte bestillinger automatisk bli autorisert hvis ordredatoen er innenfor den angitte horisonten for autorisering. Planlagte bestillinger som genereres av Planleggingsoptimalisering og den innebygde hovedplanleggingsoperasjonen håndterer ordredatoen (det vil si startdatoen) på en annen måte.

> [!NOTE]
> Automatisk autorisasjon av planlagte bestillinger kan bare skje for varer som er knyttet til en leverandør.
> 
> Avledede ordrer (dvs bestillinger fra underleverandør) som er autoriserte, viser statusen *Til vurdering* hvis sporing av saksendringer er aktivert.

> [!IMPORTANT]
> Før funksjonen som er beskrevet i denne delen, kan brukes med planleggingsoptimalisering, må [*Automatisk autorisasjon med planleggingsoptimalisering*-funksjonen](#enable-features) aktiveres i systemet, som beskrevet i begynnelsen av denne artikkelen. Automatisk autorisering kan alltid brukes med den innebygde hovedplanleggingsmotoren.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatisk autorisering med planleggingsoptimalisering i forhold til den innebygde planleggingsmotoren

Både planleggingsoptimalisering og den innebygde planleggingsmotoren kan brukes til automatisk autorisering av planlagte bestillinger. Det er imidlertid noen viktige forskjeller. Mens planleggingsoptimalisering for eksempel bruker ordredatoen (det vil si startdatoen) for å bestemme hvilke planlagte bestillinger som skal autoriseres, bruker den innebygde planleggingsmotoren behovsdatoen (det vil si sluttdatoen). Følgende tabell viser en oversikt over forskjellene.

| Funksjon | Planleggingsoptimalisering | Innebygd planleggingsmotor |
|---|---|---|
| **Datogrunnlag** | Automatisk autorisasjon er basert på ordredatoen (Startdato). | Automatisk autorisasjon er basert på behovsdatoen (sluttdato). |
| **Leveringstid** | Fordi ordredatoen (Startdato) utløser autorisering, trenger du ikke å ta hensyn til leveringstiden som en del av autorisasjonshorisonten. | Hvis du vil ha hjelp til å sikre at ordrer blir autorisert til rett tid, må autorisasjonshorisonten være lenger enn leveringstiden. |
| **Ordrer for den gjeldende uken** | Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være én uke. | Hvis du vil autorisere alle ordrer som må starte i løpet av den gjeldende uken, må autorisasjonshorisonten være leveringstiden pluss én uke. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Definere automatisk autorisering og autoriseringshorisonten

Du aktiverer automatisk autorisering ved å tilordne en automatisert autoriseringshorisont til det relevante dekningsoppsettet, som beskrevet senere i denne delen. Hvis automatisk autorisering ikke er aktivert for et dekningsoppsett, eller hvis planlegging startes fra en bestemt side, for eksempel **Nettobehov**-siden for et frigitt produkt, hoppes den automatiske autorisasjonsprosessen over.

Alternativer for gruppering og merking for automatisk autorisering tar verdiene fra kategorien **Standard oppdatering** på siden **Parametere for hovedplanlegging**.

Horisonten for automatisk autorisering defineres av antall dager du angir for det relevante dekningsoppsettet. Du kan aktivere automatisk autorisasjon og styre autorisasjonshorisonten på følgende måter:

- Hvis du vil definere standard autorisasjonshorisonten for en dekningsgruppe, går du til **Hovedplanlegging \> Oppsett \> Dekning \> Dekningsgrupper**, og velger en dekningsgruppe. Deretter angir du antall dager i feltet **Horisont for automatisk autorisasjon (dager)** i hurtigfanen **Annet**.
- Hvis du vil overskrive autoriseringshorisonten som er definert for dekningsgruppen for en bestemt vare, kan du gå til **Behandling av produktinformasjon \> Frigitte produkter**. Velg **Plan** i handlingsruten, og velg deretter **Varedekning**. I fanen **Generelt** velger du **Overstyr horisont** og angir deretter antall dager i feltet **Horisont for automatisk autorisasjon (dager)**.
- Hvis du vil overskrive autorisasjonshorisonten som er definert for dekningsgruppen og varedekningen for en bestemt hovedplan, går du til **Hovedplanlegging \> Oppsett \> Hovedplaner**, og velger en hovedplan. Deretter setter du alternativet **Autorisasjon** til **Ja** i hurtigfanen *Horisont i antall dager*, og angir antall dager.

Hvis du setter alle de tidligere nevnte tidshorisontene til *0* (null), blir automatisk autorisering effektivt deaktivert for de relevante varene som dekkes.

## <a name="firm-planned-orders-by-using-a-query"></a>Autorisere planlagte ordrer ved hjelp av en spørring

Spørringsbasert autorisering lar deg planlegge autorisering basert på kriterier som er definert på forhånd. I motsetning til automatisk autorisering tillater spørringsbasert autorisering automatisert autorisering av ulike delsett av ordrer på ulike tidspunkt. I tillegg kan du bruke enten manuelle eller automatiserte operasjoner til å autorisere ulike typer planlagte bestillinger. Du kan også forhåndsvise hvilke autoriserte ordrer som er valgt, basert på innstillingene. Derfor kan du bekrefte at valget passer til dine forventninger.

Du kan kombinere automatisk autorisering med spørringsbasert autorising. En spørringsbasert autoriseringsjobb har for eksempel en fremoverhorisont som er lengre enn horisonten for en samsvarende automatisk autorisering av dekningskonfigurasjonen. Derfor vil den spørringsbaserte autoriseringsjobben behandle de planlagte bestillingene før automatisk autorisering utløses. Du kan dra nytte av denne virkemåten til å planlegge ordrer for bestemte leverandører på en annen måte enn ordrer for lignende produkter fra andre leverandører.

> [!IMPORTANT]
> Før funksjonen som er beskrevet i denne delen kan brukes, må [*Autorisering av planlagt bestilling med filtrering*-funksjonen](#enable-features) aktiveres i systemet, som beskrevet i begynnelsen av denne artikkelen.

Følg denne fremgangsmåten for å autorisere en planlagt bestilling ved hjelp av den spørringsbaserte autoriseringsprosessen.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Kjør \> Autorisering av planlagt bestilling**.
1. I dialogboksen **Autorisering av planlagt bestilling**, i **Parametere**-hurtigfanen, angir du grunnleggende alternativer for behandling, merking og gruppering. Disse alternativene fungerer på samme som de gjør i dialogboksen **Autorisering**. (Se den forrige delen hvis du vil ha beskrivelser.) I **Plan**-delen kan du deretter definere følgende felt som er unike for dialogboksen **Autorisering av planlagt bestilling**.

    - **Plan** – Velg hovedplanen som skal brukes ved autorisering av de planlagte bestillingene som blir funnet av denne spørringen.
    - **Autorisasjonshorisont antall dager forover** – Velg hvor langt inn i fremtiden de ulike behovene og andre hensyn må beregnes ved hjelp av hovedplanlegging.
    - **Autorisasjonshorisont antall dager bakover** – Velg hvor langt tilbake i tid de ulike behovene og andre hensyn må beregnes ved hjelp av hovedplanlegging.

    ![Parametere-hurtigfanen i dialogboksen Autorisering av planlagt bestilling.](./media/planned-order-firming-main-1.png "Parametere-hurtigfanen i dialogboksen Autorisering av planlagt bestilling")

1. Hvis du vil angi hvilke poster som skal være med i ordren, velger du **Filter**-knappen i hurtigfanen **Poster som skal inkluderes**. Det vises en standard dialogboks for spørring der du kan definere utvalgskriterier, sorteringskriterier og koblinger. Feltene fungerer på samme måte som for andre typer spørringer i Supply Chain Management. Feltene her er skrivebeskyttet, og viser verdier som er knyttet til spørringen.

    ![Hurtigfanen Poster som skal inkluderes i dialogboksen Autorisering av planlagt bestilling.](./media/planned-order-firming-main-2.png "Hurtigfanen Poster som skal inkluderes i dialogboksen Autorisering av planlagt bestilling")

1. Velg **Forhåndsvis** for å forhåndsvise innholdet i den autoriserte ordren, basert på innstillingene dine så langt. Listen over planlagte bestillinger som skal autoriseres, vises som en melding. Du kan deretter justere innstillingene etter behov til forhåndsvisningen viser den autoriserte ordren slik du har til hensikt å gjøre.

    ![Eksempel på forhåndsvisning av autorisert ordre.](./media/planned-order-firming-preview.png "Eksempel på forhåndsvisning av autorisert ordre")

    > [!WARNING]
    > Denne funksjonen vil autorisere alle planlagte bestillinger som samsvarer med filterkriteriene. Ukritisk autorisering av planlagte bestillinger kan føre til at det opprettes mange uønskede innkjøps-, overførings- og produksjonsordrer. Før du fortsetter, må du alltid bruke **Forhånds**-knappen til å validere postene som skal tas med.

1. I hurtigfanen **Kjør i bakgrunnen** definerer du jobben slik at den kjøres i satsvis modus, og/eller angir en gjentakende tidsplan. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å bruke innstillingene og generere de autoriserte ordrene.

## <a name="track-firmed-orders"></a>Spore autoriserte ordrer

Følg denne fremgangsmåten for å spore en planlagt bestilling som er autorisert.

1. [Åpne en hvilken som helst listeside for planlagte bestillinger](approved-planned-order.md#view-planned-orders).
1. Åpne eller merk den planlagte bestillingen du vil spore.
1. På handlingsruten, i fanen **Vis** i **Vis**-gruppen, velger du **Autorisasjonshistorikk**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
