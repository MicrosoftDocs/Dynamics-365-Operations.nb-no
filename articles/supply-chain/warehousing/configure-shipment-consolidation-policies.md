---
title: Konfigurer policyer for forsendelseskonsolidering
description: Denne artikkelen beskriver hvordan du definerer standard og egendefinerte policyer for forsendelseskonsolidering.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427989"
---
# <a name="configure-shipment-consolidation-policies"></a>Konfigurere policyer for forsendelseskonsolidering

[!include [banner](../includes/banner.md)]

Prosessen for forsendelseskonsolidering som bruker policyer for forsendelseskonsolidering, tillater automatisk forsendelseskonsolidering under automatisk og manuell frigivelse til lageret. Når du har aktivert denne funksjonen, må du konfigurere policyene for førstegangsbehandling. Hvis ingen policyer er konfigurert, vil hver salgslinje generere en egen forsendelse som har én lastlinje.

Scenarioene som presenteres i denne artikkelen, viser hvordan du definerer standard og egendefinerte policyer for forsendelseskonsolidering.

> [!WARNING]
> Hvis du oppgraderer et Microsoft Dynamics 365 Supply Chain Management-system der du har brukt den eldre funksjonen for forsendelseskonsolidering, kan det hende at konsolideringen slutter å fungere som forventet, med mindre du følger anbefalingene som er gitt her.
>
> For Supply Chain Management-installasjoner der funksjonen *Policyer for forsendelseskonsolidering* er slått av, kan du aktivere forsendelseskonsolidering ved å bruke innstillingen **Konsolider forsendelse ved frigivelse til lager** for hvert individuelle lager. Denne funksjonen er obligatorisk fra versjon 10.0.29. Når den er aktivert, blir innstillingen **Konsolider forsendelse ved frigivelse til lager** skjult, og funksjonaliteten erstattes av *policyene for forsendelseskonsolidering* som er beskrevet i denne artikkelen. Hver policy fastsetter konsolideringsregler og inkluderer en spørring for å bestemme hvor policyen gjelder. Når du slår på funksjonen for første gang, blir det ikke definert noen policyer for forsendelseskonsolidering på siden **Policyer for forsendelseskonsolidering**. Når ingen policyer er definert, bruker systemet den eldre virkemåten. Derfor fortsetter hvert eksisterende lager å overholde innstillingen **Konsolider forsendelse ved frigivelse til lager**, selv om innstillingen nå er skjult. Når du har opprettet minst én policy for forsendelseskonsolidering, vil imidlertid innstillingene under **Konsolider forsendelse ved frigivelse til lager** ikke lenger ha noen effekt, og konsolideringsfunksjonaliteten styres fullstendig av policyene.
>
> Når du har definert minst én policy for forsendelseskonsolidering, vil systemet kontrollere konsolideringspolicyene hver gang en ordre frigis til lageret. Systemet behandler policyene ved å bruke rangeringen som er definert av **Policysekvens**-verdien for hver policy. Det bruker den første policyen der spørringen samsvarer med den nye ordren. Hvis ingen spørringer samsvarer med ordren, genererer hver ordrelinje en egen forsendelse som har én lastlinje. Vi anbefaler derfor at du, som et tilbakefall, oppretter en standardpolicy som gjelder alle lagre og grupper etter ordrenummer. Gi denne tilbakefallspolicyen den høyeste **Policysekvens**-verdien, slik at den behandles sist.
>
> Hvis du vil reprodusere den gamle virkemåten, må du opprette en policy som ikke grupperer etter ordrenummer, og som har spørringskriterier som omfatter alle relevante lagre.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Aktivere funksjonen Policyer for forsendelseskonsolidering

For å bruke funksjonen *Policyer for forsendelseskonsolidering* må den aktiveres for systemet. Funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Policyer for forsendelseskonsolidering* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a>Konfigurere innledende konsolideringspolicyer

Hvis du jobber med et nytt system eller et system der du nettopp har aktivert funksjonen *Policyer for forsendelseskonsolidering* for første gang, følger du denne fremgangsmåten for å konfigurere de første policyene for forsendelseskonsolidering.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. I handlingsruten velger du **Opprett standardoppsett** for å opprette følgende policyer:

    - En policy med navnet *Standard* for policytypen *Salgsordrer*.
    - En policy med navnet *Standard* for policytypen *Utstedelse for overføring*.
    - En policy med navnet *Kryssordre* for policytypen *Utstedelse for overføring*. (Denne policyen opprettes bare hvis du hadde minst ett lager der den eldre innstillingen **Konsolider forsendelse ved frigivelse til lager** var aktivert.)
    - En policy med navnet *Kryssordre* for policytypen *Salgsordrer*. (Denne policyen opprettes bare hvis du hadde minst ett lager der den eldre innstillingen **Konsolider forsendelse ved frigivelse til lager** var aktivert.)

    > [!NOTE]
    > - Begge *Kryssordre*-policyene vurderer det samme settet med felt som den forrige logikken. De vurderer imidlertid også ordrenummerfeltet. (Dette feltet brukes til å konsolidere linjer i forsendelser, basert på faktorer som lager, transportmåte for levering og adresse.)
    > - Begge *Standard*-policyene vurderer det samme settet med felt som den forrige logikken. De vurderer imidlertid også ordrenummerfeltet. (Dette feltet brukes til å konsolidere linjer i forsendelser, basert på faktorer som ordrenummeret, lager, transportmåte for levering og adresse.)

1. Hvis systemet genererte en *Kryssordre*-policy for policytypen *Salgsordrer*, velger du den og velger deretter **Rediger spørring** i handlingsruten. I redigeringsprogrammet for spørring kan du se hvilke av lagrene som innstillingen **Konsolider forsendelse ved frigivelse til lager** tidligere var aktivert for. Derfor reproduserer denne policyen dine tidligere innstillinger for disse lagrene.
1. Tilpass de nye standardpolicyene etter behov ved å legge til eller fjerne felt og/eller redigere spørringene. Du kan også legge til så mange nye policyer du trenger. Hvis du vil ha eksempler som viser hvordan du tilpasser og konfigurerer policyene, kan du se eksempelscenarioet senere i denne artikkelen.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Scenario: Konfigurere egendefinerte policyer for forsendelseskonsolidering

Dette scenarioet gir et eksempel som viser hvordan du konfigurerer egendefinerte policyer for forsendelseskonsolidering og tester dem ved hjelp av demodata. Egendefinerte policyer kan støtte komplekse forretningskrav når forsendelseskonsolidering avhenger av flere betingelser. For hver eksempelpolicy senere i dette scenarioet er en kort beskrivelse av forretningssaken inkludert. Disse eksempelpolicyene må defineres i en rekkefølge som sikrer et pyramideaktig diagram som evaluering av spørringene. (Med andre ord må policyene som har flest betingelser, evalueres med høyest prioritet.)

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Dette scenarioet refererer til verdier og poster som er inkludert i standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) som leveres for Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til *USMF* før du begynner.

### <a name="prepare-master-data-for-this-scenario"></a>Klargjør hoveddata for dette scenarioet

Før du kan gå gjennom øvelsene i dette scenarioet, må du klargjøre hoveddataene som kreves for å utføre filtreringen, som beskrevet i følgende underinndelinger. (Disse forutsetningene gjelder også for scenarioene som er oppført i delen [Eksempelscenarioer for hvordan du bruker policyer for forsendelseskonsolidering](#example-scenarios).)

#### <a name="create-two-new-product-filter-codes"></a>Opprette to nye produktfilterkoder

1. Gå til **Lagerbehandling \> Oppsett \> Produktfiltre \> Produktfilter** og legg til to produktfiltre:

    - Produktfilter 1:

        - **Filterkode:** *Brannfarlig*
        - **Filtertittel:** *Kode 4*

    - Produktfilter 2:

        - **Filterkode:** *Eksplosivt*
        - **Filtertittel:** *Kode 4*

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne produktet som har artikkelnummer *M9200*. (Produktet du velger, må være aktivert for avanserte \[WMS\]-prosesser for lager, og dette produktet er forhåndsaktivert for WMS-prosesser i demodataene for **USMF**.)
1. I hurtigfanen **Lager** angir du verdien *Brannfarlig* for feltet **Kode 4**.
1. Lukk siden.
1. Åpne produktet som har artikkelnummer *M9201*. (Dette produktet er også forhåndsaktivert for WMS-prosesser i demodataene for **USMF**.)
1. I hurtigfanen **Lager** angir du verdien *Eksplosivt* for feltet **Kode 4**.
1. Lukk siden.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Opprette en ny transportmåte for levering

1. Gå til **Transportstyring \> Oppsett \> Transportører \> Modus**.
1. Opprett en transportmodus som skal brukes i konsolideringsspørringer, og gi den navnet *Airways*.
1. Gå til **Transportstyring \> Oppsett \> Transpotører \> Transportører**.
1. Opprett en transportør med følgende innstillinger:

    - **Transportør:** *Airways*
    - **Navn:** *Airways*
    - **Modus:** *Airways*

1. I hurtigfanen **Tjenester** for den nye transportøren legger du til en rad som har følgende innstillinger:

    - **Transportørtjeneste:** *Lufttransport*
    - **Transportmetode:** *Lufttransport*

1. Velg **Lagre** i handlingsruten.

    > [!NOTE]
    > Når du lagrer den nye transportøren, blir feltet **Leveringsmåte** for den nye raden i rutenettet **Tjenester** satt til *Airwa-Air*. Når du bruker leveringsmåten *Airwa-Air* for en salgsordre, vil transportmodusen *Airways* bli brukt for relaterte forsendelser.

#### <a name="create-an-order-pool"></a>Opprette en ordrepulje

1. Gå til **Salg og markedsføring \> Oppsett \> Salgsordrer \> Ordrepuljer**.
1. Opprett en ordrepulje som skal brukes for konsolideringsspørringen. Denne ordrepuljen må ha følgende innstillinger:

    - **Pulje:** Skriv inn et heltall som ikke allerede brukes av en annen pulje.
    - **Navn:** *ShipCons*

1. Gå til **Salg og markedsføring \> Kunder \> Alle kunder**.
1. Åpne kunden som har kontonummer *US-003*.
1. I hurtigfanen **Standarder for salgsordrer** setter du feltet **Salgsordrepulje** til ordrepuljen du akkurat opprettet.
1. Lukk siden, og gjenta deretter trinn 4 og 5 for kunden som har kontonummer *US-004*.

### <a name="create-example-policy-1"></a>Opprette eksempelpolicy 1

I dette eksemplet skal du opprette en policy av typen *Kunde+modus* som kan brukes til følgende forretningssak:

- Policyen vil spørre etter en bestemt kundekonto (*US-001*) og en bestemt leveringsmåte (*Airwa-Air*).
- Konsolidering med åpne forsendelser er deaktivert.
- Konsolidering utføres per ordre-ID. (Med andre ord vil det være separate forsendelser per ordre, lager og så videre.)

Følg disse trinnene for å opprette en policy for forsendelseskonsolidering for denne forretningssaken.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. I handlingsruten velger du **Ny** for å opprette en policy som har følgende innstillinger:

    - **Policynavn:** *CustomerMode*
    - **Policybeskrivelse:** *Kundekonto og leveringsmåte*

1. La verdien for alternativet **Konsolider med åpne forsendelser** være *Nei*.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Konsolideringsfelt** i listen **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Leveringsmåte*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I handlingsruten velger du **Rediger spørring**.
1. I rutenettet i fanen **Område** i dialogboksen for redigeringsprogrammet for spørring finner du raden der feltet **Felt** er satt til *Kundekonto*, og deretter angir du verdien *US-001* for feltet **Vilkår** for den raden.
1. Velg **Legg til** for å legge til en rad som har følgende innstillinger i rutenettet:

    - **Tabell:** *Ordrelinjer*
    - **Avledet tabell:** *Ordrelinjer*
    - **Felt:** *Leveringsmåte*
    - **Vilkår:** *Airwa-Air*

1. Velg **OK** for å lukke dialogboksen.

> [!NOTE]
> For denne forretningssaken vil ordrelinjer for kunden *US-001* som bruker leveringsmåten *Airwa-Air*, ikke bli konsolidert på tvers av ordrer. Denne policyen er ment å bli brukt først i en sekvens, i tilfeller der forsendelser for alle andre leveringsmåter konsolideres for denne kunden.

### <a name="create-example-policy-2"></a>Opprette eksempelpolicy 2

I dette eksemplet skal du opprette en policy av typen *Farlig materiale* som kan brukes til følgende forretningssak:

- Policyen vil spørre etter en bestemt filterkode (*farlig*) og en bestemt leveringsmåte (*Airwa-Air*).
- Konsolidering med åpne forsendelser er aktivert.
- Konsolidering utføres på tvers av ordrer. (Med andre ord vil det være separate forsendelser per konto, lager og så videre, men bare innenfor varegruppen som er angitt i spørringen.)

Følg disse trinnene for å opprette en policy for forsendelseskonsolidering for denne forretningssaken.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. I handlingsruten velger du **Ny** for å opprette en policy som har følgende innstillinger:

    - **Policynavn:** *Varetype*
    - **Policybeskrivelse:** *Konsolider samme type vare på tvers av ordrer*

1. Sett verdien for alternativet **Konsolider med åpne forsendelser** til *Ja*.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Konsolideringsfelt** i listen **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Leveringsmåte*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I handlingsruten velger du **Rediger spørring**.
1. I fanen **Sammenkoblinger** i dialogboksen for redigeringsprogrammet for spørring viser og velger du **Tabeller \> Lastdetaljer** i treet.
1. Velg **Legg til tabellsammenkobling**.
1. I rutenettet med relasjoner som vises, finner du og velger raden der feltet **Relasjon** har verdien *Lagervarenummer (varenummer)*, deretter velger du **Velg**. 
1. Velg **Legg til** i fanen **Område** for å legge til en rad som har følgende innstillinger i rutenettet:

    - **Tabell:** *Lagervarenummer*
    - **Avledet tabell:** *Lagervarenummer*
    - **Felt:** *Kode 4*
    - **Vilkår:** *Brannfarlig*

1. Velg **OK** for å lukke dialogboksen.

> [!NOTE]
> For denne forretningssaken vil alle ordrelinjer der varer har en bestemt filterkode (det vil si filterkoden der feltet **Kode 4** er satt til *Brannfarlig*) konsolideres med andre varer av samme type på tvers av ordrer. Hvis det finnes en åpen forsendelse for samme konto, lager og varegruppe, blir de nye linjene tilknyttet.

### <a name="create-example-policy-3"></a>Opprette eksempelpolicy 3

I dette eksemplet skal du opprette en policy av typen *Kunders krav* som kan brukes til følgende forretningssak:

- Policyen vil spørre etter en bestemt kundekonto.
- Konsolidering med åpne forsendelser er aktivert.
- Konsolideringen utføres på tvers av ordrer, men er basert på kunderekvisisjoner. (Med andre ord blir flere ordrer gruppert i forsendelser, basert på det samme kunderekvisisjonsnummeret og lageret.)

Følg disse trinnene for å opprette en policy for forsendelseskonsolidering for denne forretningssaken.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. I handlingsruten velger du **Ny** for å opprette en policy som har følgende innstillinger:

    - **Policynavn:** *CustomerOrderNo*
    - **Policybeskrivelse:** *Konsolider linjer basert på kundebestilling*

1. Sett verdien for alternativet **Konsolider med åpne forsendelser** til *Ja*.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Konsolideringsfelt** i listen **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Kunderekvisisjon*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I listen **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Leveringsmåte*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I handlingsruten velger du **Rediger spørring**.
1. I fanen **Område** i dialogboksen for redigeringsprogrammet for spørring finner du raden der feltet **Felt** er satt til *Kundekonto*, og deretter angir du verdien *US-001* for feltet **Vilkår** for den raden.
1. Velg **OK** for å lukke dialogboksen.

> [!NOTE]
> For denne forretningssaken konsolideres alle ordrelinjer der salgsordrene har samme kunderekvisisjonsnummer, i én forsendelse, uavhengig av salgsordrenummer. (Kunderekvisisjonsnummeret brukes som kundens \[bestillingsnummer\].) Hvis det finnes en åpen forsendelse for samme konto, lager og kunderekvisisjon, blir de nye linjene knyttet til den. Denne policyen kan brukes hvis kunden sender flere ordrelinjer som har samme bestillingsnummer flere ganger i løpet av en dag, og vil at alle linjene skal grupperes i én forsendelse. (Med andre ord vil det være ett fraktbrev og én følgeseddel.)

### <a name="create-example-policy-4"></a>Opprette eksempelpolicy 4

I dette eksemplet skal du opprette en policy av typen *Kunder som tillater konsolidering* som kan brukes til følgende forretningssak:

- Policyen vil spørre etter en bestemt ordrepulje for å identifisere kunder som godtar konsoliderte forsendelser.
- Konsolidering med åpne forsendelser er deaktivert.
- Konsolidering skjer på tvers av ordrer ved hjelp av feltene som velges som standard av CrossOrder-policyen (for å replikere den tidligere avmerkingsboksen **Konsolider forsendelse ved frigivelse til lager**).

- Du kan overstyre regelen for en salgsordre ved å velge en annen ordrepulje.

Følg disse trinnene for å opprette en policy for forsendelseskonsolidering for denne forretningssaken.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. I handlingsruten velger du **Ny** for å opprette en policy som har følgende innstillinger:

    - **Policynavn:** *Ordrepulje*
    - **Policybeskrivelse:** *Konsolider på tvers av ordrer basert på ordrepulje*

1. La verdien for alternativet **Konsolider med åpne forsendelser** være *Nei*.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Konsolideringsfelt** i listen **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Leveringsmåte*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I handlingsruten velger du **Rediger spørring**.
1. Velg **Legg til** i fanen **Område** i dialogboksen for redigeringsprogrammet for spørring for å legge til en rad som har følgende innstillinger i rutenettet:

    - **Tabell:** *Salgsordrer*
    - **Avledet tabell:** *Salgsordrer*
    - **Felt:** *Pulje*
    - **Vilkår:** *ShipCons*

1. Velg **OK** for å lukke dialogboksen.

> [!NOTE]
> For denne forretningssaken vil alle ordrelinjer der salgsordrene tilhører samme ordrepulje, konsolideres til én forsendelse på tvers av salgsordrer for samme konto, lager og transportmåte for levering. I stedet for ordre puljen, kan du bruke et hvilket som helst annet felt til å skille en gruppe av kunder, og bruke salgsordrehodet som standard. Du kan bruke denne fremgangsmåten hvis kunden, ikke lageret, driver behovet for konsolidering. (I den tidligere konsolideringslogikken styrte lageret behovet for konsolidering.)

### <a name="create-example-policy-5"></a>Opprette eksempelpolicy 5

I dette eksemplet skal du opprette en policy av typen *Lagere som tillater konsolidering* som kan brukes til følgende forretningssak:

- Policyen vil spørre etter en bestemt ordrepulje for å identifisere lagere som kan konsoliderte forsendelser.
- Konsolidering med åpne forsendelser er deaktivert.
- Konsolidering skjer på tvers av ordrer ved hjelp av feltene som velges som standard av CrossOrder-policyen (for å replikere den tidligere avmerkingsboksen **Konsolider forsendelse ved frigivelse til lager**).

Denne forretningssaken kan vanligvis løses ved hjelp av standardpolicyene du opprettet i [Konfigurere innledende konsolideringspolicyer](#initial-policies). Du kan imidlertid også opprette lignende policyer manuelt ved å følge disse trinnene.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. I handlingsruten velger du **Ny** for å opprette en policy som har følgende innstillinger:

    - **Policynavn:** *Kryssordre*
    - **Policybeskrivelse:** *Kryssordrekonsolidering for bestemte lagere*

1. La verdien for alternativet **Konsolider med åpne forsendelser** være *Nei*.
1. Velg **Lagre** i handlingsruten.
1. I hurtigfanen **Konsolideringsfelt** i feltet **Gjenværende felt** velger du raden der feltet **Feltnavn** er satt til *Leveringsmåte*.
1. Velg **Legg til**-knappen ![høyre pil.](media/forward-button.png) for å flytte feltet til **Valgte felt**-listen.
1. I handlingsruten velger du **Rediger spørring**.
1. I fanen **Område** i dialogboksen for redigeringsprogrammet for spørring finner du raden der feltet **Felt** er satt til *Lager*, og deretter angir du verdien *61, 63* for feltet **Vilkår** for den raden.
1. Velg **OK** for å lukke dialogboksen.

### <a name="set-the-order"></a>Angi rekkefølgen

Nå som du har opprettet alle policyene, må du angi rekkefølgen de skal brukes i. Hvis du vil bruke en pyramideaktig metode, der policyene som har flest betingelser, evalueres med høyest prioritet, følger du disse trinnene.

1. Gå til **Lagerbehandling \> Oppsett \> Frigi til lager \> Policyer for forsendelseskonsolidering**.
1. Angi verdien *Salgsordrer* for feltet **Policytype**.
1. Velg hver policy som står oppført i venstre kolonne, og bruk deretter knappene **Flytt opp** og **Flytt ned** i handlingsruten til å ordne policyene i følgende rekkefølge:

    1. CustomerMode
    1. Varetype
    1. CustomerOrderNo
    1. Ordrepulje
    1. Kryssordre
    1. Standard

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Eksempelscenarioer for hvordan du bruker policyer for forsendelseskonsolidering

Scenarioene nedenfor illustrerer hvordan du kan bruke policyene for forsendelseskonsolidering som du opprettet under lesing av denne artikkelen. Hvert secnario veileder deg gjennom prosessen for forsendelseskonsolidering som bruker policyer for forsendelseskonsolidering, eller manuell frigivelse til lageret:

- Scenario 1 [Konsolidere forsendelser når de frigis til lageret ved hjelp av automatisk frigivelse av salgsordrer](../warehousing/consolidate-shipments-automatic.md)
- Scenario 2 [Konsolidere forsendelser når policyen for forsendelseskonsolidering overstyres fra siden Frigi til lager](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Scenario 3 [Konsolidere forsendelser ved hjelp av siden Frigi til lager fra arbeidsområdet for lastplanlegging](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Scenario 4 [Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering](../warehousing/consolidate-shipments-manual-workbench.md)
- Scenario 5 [Konsolidere forsendelser manuelt ved hjelp av siden Konsolider forsendelser](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
