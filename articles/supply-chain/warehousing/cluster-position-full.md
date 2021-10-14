---
title: Gruppestilling full
description: Dette emnet inneholder informasjon om funksjonen Gruppeposisjon full. Denne funksjonen gir et alternativ til mer rigid håndhevelse av arbeidsstoppregler når gruppueplukking brukes, ettersom det muliggjør en større margin med feil i de volumetriske begrensningene i beholdere eller transportkasser.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: a23168b550bfa2bb6a51c8df5d0a558431c23ebb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574263"
---
# <a name="cluster-position-full"></a>Gruppestilling full

[!include [banner](../includes/banner.md)]

Funksjonen *Gruppeposisjon full* gir et alternativ til mer rigid håndhevelse av arbeidsstoppregler når gruppeplukking brukes, ettersom det muliggjør en større margin med feil i de volumetriske begrensningene i beholdere eller transportkasser. I et vanlig scenario vil ikke alle varer i en arbeidsordre få plass i en valgt beholder. Lagerarbeidere som plukker i grupper, har få alternativer i dette scenarioet: de må enten endre til en større beholderstørrelse, eller samarbeide med sin overordnede for å finne en annen løsning.

Denne funksjonen gir mulighet til å kjøre knappen **Full** på en av arbeidsenhetene i en gruppe. I eldre versjoner var dette alternativet bare tilgjengelig for vanlig ordreplukking, ikke for gruppeplukking. Denne funksjonen er imidlertid forskjellig fra standardknappen **Full** ved at den avbryter det gjenstående arbeidet. Den foreslår ikke at brukeren legger til en ny hylle i den samme gruppen, og den oppretter ikke automatisk nytt arbeid.

## <a name="turn-on-the-cluster-position-full-feature"></a>Aktivere funksjonen Gruppeposisjon full

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Gruppeposisjon full*

## <a name="setup"></a>Installasjon

Denne delen inneholder retningslinjer, og et eksempel som viser hvordan du definerer og bruker funksjonen *Gruppeposisjon full*.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette [eksempelscenarioet](#example-scenario) ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke dette eksempelscenarioet som en veiledning for å bruke denne funksjonen i et produksjonssystem. I så fall må du imidlertid bytte dine egne verdier for innstillingene som beskrives her.

### <a name="cluster-profiles"></a>Gruppeprofiler

Du må angi om gruppe-ID-er skal genereres automatisk, hvor mange stillinger som brukes, når sektorgrupper brytes og hvordan plukkarbeidet blir sekvensiert og verifisert.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Gruppeprofiler**.
1. I listeruten velger du posten **Opprett gruppe**.
1. Bekreft følgende verdier i hurtigkategorin **Generelt**:

    - **Generer gruppe-ID:** *Ja*
    - **Aktiver stillinger:** *Ja*
    - **Antall stillinger:** *2*
    - **Stillingsnavn:** *Numerisk*
    - **Bryt opp gruppe ved:** *Plasser*
    - **Type sorteringsbekreftelse:** *Posisjonsskanning*

1. I hurtigkategorin **Gruppesortering**. Rutenettet bør være tomt (det vil si at det ikke inneholder linjer).

### <a name="work-templates"></a>Arbeidsmaler

Du må definere hvordan plukkarbeidet for gruppeplukking opprettes.

1. Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidsmaler**.
1. Øverst på siden setter du feltet **Arbeidsordretype** til *Salgsordrer*.
1. Kontroller at følgende arbeidsmaler fra demonstrasjonsdataene er oppført. Hvis de ikke er tilgjengelige, kan du ikke fullføre scenarioet.

    - 61 SO Stadium
    - 61 SO Gruppeplukking

### <a name="location-directives"></a>Lokasjonsdirektiver

Du må angi hvor varene skal plukkes fra og hvor de blir plassert.

1. Gå til **Lagerstyring \> Oppsett \> Lokasjonsdirektiver**.
1. I listetoppteksten setter du feltet *Arbeidsordretype* til **Salgsordrer**.
1. Kontroller at følgende salgsordredirektivene fra demonstrasjonsdataene er oppført. Hvis de ikke er tilgjengelige, kan du ikke fullføre scenarioet.

    - 61 Gruppeplukking
    - 61 SO Plukkordre

### <a name="mobile-device-menu-items"></a>Menyelementer på mobilenheten

Du må konfigurere et menyelement for mobilenhet til å bruke eksisterende arbeid styres av gruppeplukking. I menyelementet for mobilenhet for gruppeplukking må parameteren **Tillat arbeidsoppdeling** være aktivert, og arbeidsklassen *Salgsordreplukking* må legges til.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. I listeruten velger du posten **Oppretting av gruppeplukking**.
1. Velg **Rediger** i handlingsruten.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Styrt av:** *Gruppeplukking*
    - **Generer nummerskilt:** *Ja*
    - **Tillat arbeidsoppdeling:** *Ja*
    - **ID for gruppeprofil:** *Opprett gruppe*

    Godta standardverdiene for alle de andre feltene.

1. I hurtigkategorin **Arbeidsklasser** legger du til følgende to linjer etter behov:

    - Linje 1 (finnes vanligvis i demodata):

        - **Arbeidsklasse-ID:** *Salg* 
        - **Arbeidsordretype:** *Salgsordrer*

    - Linje 2 (finnes sannsynligvis ikke i demodata):

        - **Arbeidsklasse-ID:** *Salgsordreplukking*
        - **Arbeidsordretype:** *Salgsordrer*

1. Gå til **Arbeidsbekreftelsesoppsett** i handlingsruten.
1. Velg **Rediger**.
1. Angi følgende verdier på linjen i rutenettet.
    - **Arbeidstype** - *Plukking*
    - **Produktbekreftelse** - *Merk av i avmerkingsboksen*

1. Velg **Lagre** i handlingsruten og lukk siden.

## <a name="create-picking-work"></a>Opprett plukkarbeid

Før du kan starte gruppeplukking, må du opprette noe utgående arbeid. Gruppeprofilen du opprettet tidligere, angir to gruppestillinger. Det må derfor opprettes minst to arbeids-ID-er for plukking av salgsordre. I dette scenarioet vil det oppstå transaksjoner i lager *61*, og de vil bruke varene *L0101* og *T0100*. Demonstrasjonsdataene bør ha tilstrekkelig lagerbeholdning av disse varene. Kontroller at du har tilstrekkelig beholdning til å fullføre transaksjonene.

### <a name="create-sales-order-1"></a>Opprett salgsordre 1

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette salgsordre 1.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-010*
    - **Lager:** *61*

1. Velg **OK**.
1. Den nye salgsordren åpnes. På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:

    - **Varenummer:** *T0100*
    - **Antall:** *5*

1. På hurtigkategorin **Linjedetaljer** i fanen **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.
1. I hurtigfanen **Salgsordrelinjer** legger du til ytterligere en linje som har følgende innstillinger:

    - **Varenummer:** *L0101*
    - **Antall:** *20*

1. På hurtigkategorin **Linjedetaljer** i fanen **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.
1. For hver linje du legger til, kan du følge denne fremgangsmåten for å reservere lager:

    1. Velg linjen som skal reserveres.
    2. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
    3. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
    4. Lukk **Reservasjon**-siden.

1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Når frigivelsen er fullført, mottar du informasjonsmeldinger som viser bølge- og last-ID-er som ble opprettet.

### <a name="create-sales-order-2"></a>Opprett salgsordre 2

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette salgsordre 2.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-011*
    - **Lager:** *61*

1. Velg **OK**.
1. Den nye salgsordren åpnes. På hurtigfanen **Salgsordrelinjer** legger du til en linje som har følgende innstillinger:

    - **Varenummer:** *L0101*
    - **Antall:** *20*

1. På hurtigkategorin **Linjedetaljer** i fanen **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.
1. I hurtigfanen **Salgsordrelinjer** legger du til ytterligere en linje som har følgende innstillinger:

    - **Varenummer:** *T0100*
    - **Antall:** *2*

1. På hurtigkategorin **Linjedetaljer** i fanen **Levering** setter du verdien for feltet **Bekreftet forsendelsesdato** til dagens dato.
1. For hver linje du legger til, kan du følge denne fremgangsmåten for å reservere lager:

    1. Velg linjen som skal reserveres.
    2. På hurtigfanen **Salgsordrelinjer** velger du **Beholdning \> Reservasjon**.
    3. På **Reservasjon**-siden, i handlingspanelet, velger du **Reserver parti** for å reservere lageret.
    4. Lukk **Reservasjon**-siden.

1. Velg **Frigi til lager** i fanen **Lager** i handlingsruten.

    Når frigivelsen er fullført, mottar du informasjonsmeldinger som viser bølge- og last-ID-er som ble opprettet.

### <a name="get-work-ids-and-license-plate-numbers"></a>Hent arbeids-ID-er og nummerskilt

To arbeids-ID-er bør være opprettet, og hver av dem har to plukklinjer. Følg denne fremgangsmåten for å finne arbeids-ID-ene og nummerskilttilordningene.

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. I rutenettet **Oversikt** søker du i kolonnen **Ordrenummer** etter de to salgsordrene du nettopp opprettet. For hver salgsordre noterer du den tilsvarende arbeids-ID-en.
1. Velg raden for hver salgsordre for å vise relatert informasjon i rutenettet **Linjer**. Noter deg hvor hver vare blir plukket fra.
1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Beholdningsliste**.
1. I handlingsruten velger du **Dimensjoner** for å åpne dialogboksen **Dimensjonsvisning**.
1. Kontroller at det er merket av for **Nummerskilt**, **Lager** og **Varenummer**, og velg deretter **OK**.
1. Angi følgende filtre i ruten **Filter**:

    - **Varenummer** – **er enten** – *L0101* eller *T100*
    - **Lager** – **starter med** – *61*

1. Noter deg verdiene for **Nummerskilt** som vises.

## <a name="example-scenario"></a><a name="example-scenario"></a>Eksempelscenario

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Flytutføring for mobilenhet – behandling av arbeidsbekreftelse for produktet

1. Logg på mobilappen Lagerstyring som en bruker som er aktivert i lager *61*.
1. Gå til **Utgående \> Oppretting av gruppeplukking**.

    Siden **OPPGAVE: Tilordne arbeid til gruppe** vises.

1. Angi arbeids-ID-en for salgsordre 1 for å tilordne den til gruppeposisjon 1.
1. Velg **OK** (hakesymbol).
1. Angi arbeids-ID-en for salgsordre 2 for å tilordne den til gruppeposisjon 2.
1. Velg **OK** (hakesymbol).

    Siden **OPPGAVE: Oppretting av gruppeplukking: Plukk** vises med *Vare L0101 2 PL*.

Ettersom gruppeprofilen setter antall posisjoner til 2, vil systemet automatisk omdirigere deg til den første konsolideringplukkingen: to paller (PL) av varen *L0101*.

Når som helst i trinnene nedenfor kan du velge fanen **Detaljer** for å vise mer informasjon om oppgaven, for eksempel plukklokasjon.

1. Sett verdien i feltet **VARE** til *L0101*. Dette bekrefter varenummeret, som er nødvendig for dette menyelementet (du konfigurerte dette tidligere ved å velge **Arbeidsbekreftelsesoppsett** på siden **Menyelement for mobilenhet** da du opprettet dette menyelementet).
1. Angi nummerskiltet som er knyttet til varen på lokasjonen som blir plukket. Du skal plukke to paller.
1. Sett verdien i feltet **LP** til *LP\_PLUKK\_01*.
1. Velg **OK** (hakesymbol).

    Siden **OPPGAVE: Sortere: Oppretting av gruppeplukking** vises. Her skal du sortere de to plukkede pallene til en plukkposisjon. Denne posisjonen kan være en transportkasse eller en beholder som brukes til å skille den plukkede beholdningen etter salgsordre.

1. Vis detaljene som vises for varen (*L0101*) og antallet (*20* EA) som skal sorteres i posisjon 1 (for salgsordre 1).
1. Sett feltet **POSISJONSNAVN** til *1*.
1. Velg **OK** (hakesymbol).
1. Vis detaljene som vises for varen (*L0101*) og antallet (*20* EA) som skal sorteres i posisjon 2 (for salgsordre 2).
1. Sett feltet **POSISJONSNAVN** til *2*.
1. Velg **OK** (hakesymbol).

    Siden **OPPGAVE: Oppretting av gruppeplukking: Plukk** vises med *Vare T0100 7 EA*.

I dette scenarioet kan ikke posisjon 1 godta hele antallet varer som må plukkes for å oppfylle salgsordre 1. En posisjon må merkes som full. I dette scenarioet skal du utføre en delvis plukking av den andre varen. Den andre varen plukkes delvis for posisjon 1, og nytt arbeid blir opprettet for å plukke det gjenstående antallet for å oppfylle ordren.

1. Velg menyknappen (noen ganger kalt hamburger eller hamburgerknappen), og velg deretter **Posisjon full**.
1. Identifiser posisjonen som er full og velg *1*.
1. Velg **OK** (hakesymbol).
1. Angi plukkantallet som fremdeles kan plukkes i posisjon 1. Systemet kan bestemme hvilket varenummer som skal plukkes.
1. Angi *2*.
1. Velg **OK** (hakesymbol).
1. Bekreft at varenummeret skal fullføre plukkingen av den gjenværende varen i posisjon 2.
1. Sett verdien i feltet **VARE** til *T0100*.
1. Velg **OK** (hakesymbol).
1. Angi nummerskiltet som varen blir plukket fra, ved å sette feltet **LP** til *LPREPL04*.
1. Velg **OK** (hakesymbol).
1. Vis detaljene som vises for varen (*T0100*) og antallet (*2* EA) som skal sorteres i posisjon 2 (for salgsordre 2).
1. Sett feltet **POSISJONSNAVN** til *2*.
1. Velg **OK** (hakesymbol).
1. Vis detaljene som vises for varen (*T0100*) og antallet (*2* EA) som skal sorteres i posisjon 1 (for salgsordre 1).
1. Sett feltet **POSISJONSNAVN** til *1*.
1. Velg **OK** (hakesymbol).

    Siden **OPPGAVE: Oppretting av gruppeplukking: Plassere** vises.

I dette scenarioet er gruppeplukkingen fullført, og brukeren blir omdirigert til å plassere plukkede varer fra posisjon 1 og 2 på oppsamlingslokasjon *STAGE01*.

1. Gå gjennom informasjonen på siden. Det viser at et totalt antall på *44* vil bli lagt til på oppsamlingslokasjonen.
1. Velg **OK** (hakesymbol).

    Du mottar meldingen Gruppe fullført.

Du kan nå bruke menyelementet **Salgsplukking** til å plukke restantallet. Du kan deretter bruke menyelementet **Salgslasting** til å flytte varene fra lokasjonsplasseringen til lasterampen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]