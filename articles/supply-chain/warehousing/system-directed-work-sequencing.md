---
title: Systemstyrt arbeidssekvensiering
description: Dette emnet inneholder informasjon om systemstyrt arbeidssekvensering. Med denne funksjonaliteten kan du sortere og filtrere arbeidsordrene som systemet viser for brukere for kjøring. Det er nyttig i scenarier der det kreves tilleggskriterier for å styre lagerplukkprosessen.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017036"
---
# <a name="system-directed-work-sequencing"></a>Systemstyrt arbeidssekvensiering

[!include [banner](../includes/banner.md)]

Med systemstyrt arbeidssekvensering kan du sortere og filtrere arbeidsordrene som systemet viser for brukere for kjøring. Det er nyttig i scenarier der tilleggskriterier (for eksempel leveringstiden, plukksonen, lokasjonsprofilen eller en kombinasjon av ulike kriterier) er nødvendig for å drive lagerplukkprosessen.

Denne funksjonaliteten utvider den gjeldende systemstyrte plukkfunksjonaliteten ved å legge til en omadressert spørringsrekkefølge, der brukere kan definere en sekvens og én eller flere spørringer som vil evaluere alle arbeidsordrene som opprettes. Bare arbeidsordrer som oppfyller kriteriene som er angitt i oppsettet til menyelementet for den mobile enhetene, blir tatt opp og presentert.

Denne funksjonaliteten gjør derfor at du kan optimalisere lagerplukkprosessene samtidig som den identifiserer arbeidsordrer som samsvarer med de angitte kriteriene, tilordner dem til det riktige menyelementet på den mobile enheten, og presenterer dem deretter til en arbeider, basert på et bestemt kompetansesett, et plukkutstyr eller et annet krav.

> [!NOTE]
> Hvis det er behov for andre kriterier, må du bruke flere menyelementer for mobile enheter.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Aktiver Systemstyrt arbeidssekvensering i hele organisasjonen-funksjonen

Før du kan bruke systemstyrt arbeidssekvensering-funksjonen, må den aktiveres i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Systemstyrt arbeidssekvensering i hele organisasjonen*

## <a name="setup"></a>Installasjon

### <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke verdiene som presenteres i dette emnet, må du arbeide på et system der standard demodata er installert. Du må også velge den juridiske enheten **USMF**. Scenariene bruker lager *51* fra demodataene.

> [!IMPORTANT]
> Før du frigir ordrene til lageret, må du kontrollere at plukklokasjonene har nok beholdning for alle varene på ordrene.
>
> Standard USMF-data bør støtte dette scenariet. Hvis du ikke bruker demodata, kan du se gjennom **Lokasjonsdirektiv** -innstillingen for å lære hvilke plukklokasjoner som skal brukes for plukking av salgsordre. Hvis du må justere beholdninge, kan du opprette manuelle flyttinger, bruke etterfylling eller bruke en annen flyt.

### <a name="set-up-a-mobile-device-menu-item"></a>Definere en mobilenhetsmenyelement

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. I listen over mobilenhetsmenyelementer velger du **Salgsplukking – system**. Det nødvendige menyelementet bør allerede finnes. 
1. Bekreft følgende innstillinger:

    - På **Generelt** -hurtigfanen skal **Styrt av** -feltet angis til *Systemstyrt*.
    - **Arbeidsklasser** -hurtigfanen skal vise følgende innstillinger.

        | Arbeidsklasse-ID | Arbeidsordretype |
        |---|---|
        | Salg | Salgsordre |
        | Salgsordreplukking | Salgsordre |

1. I handlingsruten velger du **Systemstyrte spørringer om arbeidssekvens**.
1. Velg **Rediger**.
1. Slett den eksisterende linjen, og bekreft deretter handlingen ved å velge **Ja**.
1. I handlingsruten velger du **Ny** for å opprette en linje.
1. På den nye linjen angir du følgende verdier:

    - **Sekvensnummer:** *1*
    - **Beskrivelsesfelt:** *Arbeidsantall mindre enn 20 og synkende*

1. Velg **Lagre**.
1. I handlingsruten velger du **Rediger spørring**.
1. På **Sammenkoblinger** -fanen utvides sammenkoblingshierarkiet for å vise **Arbeidslinjer** -tabellen.
1. Velg **Arbeidslinjer** -tabellsammenkobling.
1. Velg **Legg til tabellsammenkobling**.
1. I listen som vises, finner du og velger raden med følgende innstillinger:

    - **Sammenkoblingsmodus:** *n:1*
    - **Relasjon:** *Lokasjoner (lokasjon)*

1. Velg **Velg**.

    Lokasjoner legges til i tabellsammenkoblingen.

1. I **Sortering** -fanen velger du **Legg til** for å legge til en linje.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidsantall* (i meldingsboksen som vises, velger du **Ja** for å legge til sortering i dette feltet.)
    - **Søkeretning:** *Synkende*

1. Velg **Område** -fanen.

    Hvis bare bestemte arbeidskriterier skal inkluderes i sekvensen, kan du angi dem i **Område** -fanen. I dette eksemplet vil du bare ta med arbeid der antallet er mindre enn 20 ea (den laveste måleenheten).

    Legg merke til at noen linjer allerede er inkludert. Disse linjene bør ikke fjernes.

1. Velg **Legg til** for å legge til en linje.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Beholdningsarbeidsantall*
    - **Kriterier:** *\<20* (mindre enn 20)

1. Velg **Legg til** for å legge til en ny linje.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Arbeidslinjer*
    - **Avledet tabell:** *Arbeidslinjer*
    - **Felt:** *Arbeidstype*
    - **Kriterier:** *Plukk*

1. Velg **Legg til** for å legge til en ny linje.
1. På den nye linjen angir du følgende verdier:

    - **Tabell:** *Plasseringer*
    - **Avledet tabell:** *Lokasjoner*
    - **Felt:** *ID for lokasjonsprofil*
    - **Kriterier:** *!SCENE*

        > [!IMPORTANT]
        > Husk å ta med utropstegnet ( *!* ) foran *STAGE*.

1. Velg **OK** for å lagre og lukke spørringen.
1. Velg **Lagre**.
1. Lukk siden for å gå tilbake til **Menyelementer på mobilenhet**.

> [!NOTE]
> Dette oppsettet definerer kriteriene som vil bli brukt til å mate det berettigede arbeidet til menyelementet på mobilenheten. Hvis du legger til flere kriterielinjer i spørringen, vil systemet bruke spørringslinjen som har laveste sekvensnummer først. Med andre ord vil alt kvalifisert arbeid for sekvensnummer 1 bli presentert for brukeren først, og deretter alt arbeid for sekvensnummer 2. Hvis et bestemt område og en sortering må brukes sammen, bør derfor de angis i den samme systemstyrte arbeidssekvensspørringen.
>
> Dette oppsettet vil fange opp alt arbeid som har minst én linje der antallet er mindre enn 20 ea. Hvis arbeidet har en linje der antallet er nøyaktig 20 eller mer enn 20 ea, vil det derfor være gyldig, forutsatt at det også har minst én linje der antallet er mindre enn 20 ea.

### <a name="location-directives"></a>Lokasjonsdirektiver

Hvis du bruker standard Contoso-data, trenger ikke spørringen for handlingen for lokasjonsdirektiv endringer. Hvis du imidlertid vil være sikker på at lokasjonsdirektivene vil hente varene på salgsordrene når du bruker funksjonen i et ikke-Contoso-miljø, oppretter du et nytt lokasjonsdirektiv. Følg denne fremgangsmåten for å kontrollere innstillingene i demomiljøet.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lokasjonsdirektiver**.
1. Velg *Salgsordrer* i feltet **Arbeidsordretype**.
1. Velg lokasjonsdirektivet som heter *51 Plukk*.
1. På **Handlinger for lokasjonsdirektiv** -hurtigfanen velger du linjen for **Plukk** -handlingen.
1. Velg **Rediger spørring** over rutenettet.
1. Gå gjennom **Område** -spørringen.

    1. Finn linjen der **Felt** -feltet er satt til *Lokasjon*.
    2. Kontroller at **Kriterier** -feltet er tomt (det vil si at det ikke er noen begrensninger).

## <a name="scenario"></a>Scenario

### <a name="create-sales-order-picking-work"></a>Opprette et plukkarbeid for salgsordre

Før systemstyrt plukking kjøres, bør noe utgående arbeid opprettes. I dette scenariet skal du opprette fire salgsordrer som er basert på den angitte systemstyrte arbeidssekvensspørringer.

Du vil reservere beholdningsantall for hver salgsordre. Derfor kan ikke reservert beholdning trekkes tilbake fra lageret for andre ordrer hvis ikke lagerreserveringen, eller deler av lagerreserveringen, avbrytes.

Du vil deretter frigi hver salgsordre til beholdning for å opprette det utgående arbeidet.

#### <a name="sales-order-1"></a>Salgsordre 1

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruten velger du **Ny** for å opprette salgsordre 1.
1. I **Opprett salgsordre** -dialogboksen angir du følgende verdier:

    - I **Kunde** -delen angir du **Kundekonto** -feltet til *US-004*.
    - I **Generelt** -delen angir du **Lager** -feltet til *51*.

1. Velg **OK** for å lukke dialogboksen. Noter deg salgsordrenummeret.
1. Legg til en linje i den nye salgsordren, og angi følgende verdier:

    - **Varenummer:** *M9200*
    - **Antall:** *20*

1. Velg **Reservasjon** på **Beholdning** -menyen over rutenettet.
1. På **Reservasjon** -siden velger du **Reserver parti** for å reservere beholdningen.
1. Lukk **Reservasjon** -siden.
1. I handlingsruten på **Lager** -fanen, velger du **Frigi til lager** for å opprette arbeidet for lageret.

    Du mottar informasjonsmeldinger som viser bølge-ID og forsendelses-ID-er som er opprettet for salgsordren.

#### <a name="sales-order-2"></a>Salgsordre 2

1. I handlingsruten velger du **Ny** for å opprette salgsordre 2.
1. I **Opprett salgsordre** -dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-007*
    - **Lager:** *51*

1. Velg **OK** for å lukke dialogboksen. Noter deg salgsordrenummeret.
1. Legg til en linje i den nye salgsordren, og angi følgende verdier:

    - **Varenummer:** *M9200*
    - **Antall:** *5*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *M9201*
    - **Antall:** *1*

1. Reserver beholdning for begge linjer.
1. Frigi ordren til beholdning.

#### <a name="sales-order-3"></a>Salgsordre 3

1. I handlingsruten velger du **Ny** for å opprette salgsordre 3.
1. I **Opprett salgsordre** -dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-009*
    - **Lager:** *51*

1. Velg **OK** for å lukke dialogboksen. Noter deg salgsordrenummeret.
1. Legg til en linje i den nye salgsordren, og angi følgende verdier:

    - **Varenummer:** *M9200*
    - **Antall:** *7*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *M9202*
    - **Antall:** *8*

1. Reserver beholdning for begge linjer.
1. Frigi ordren til beholdning.

#### <a name="sales-order-4"></a>Salgsordre 4

1. I handlingsruten velger du **Ny** for å opprette salgsordre 4.
1. I **Opprett salgsordre** -dialogboksen angir du følgende verdier:

    - **Kundekonto:** *US-010*
    - **Lager:** *51*

1. Velg **OK** for å lukke dialogboksen. Noter deg salgsordrenummeret.
1. Legg til en linje i den nye salgsordren, og angi følgende verdier:

    - **Varenummer:** *M9200*
    - **Antall:** *25*

1. Velg **Legg til linje** for å legge til en ny linje, og angi deretter følgende verdier:

    - **Varenummer:** *M9202*
    - **Antall:** *10*

1. Reserver beholdning for begge linjer.
1. Frigi ordren til beholdning.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Hent arbeids-ID-er for arbeidet som ble opprettet

1. Gå til **Lagerstyring \> Arbeid \> Arbeidsdetaljer**.
1. Filtrere på **Lager** -feltet slik at bare arbeid på lager *51* vises.
1. Fire arbeids-ID-er skal ha blitt opprettet. Skriv ned arbeids-ID-en for hver salgsordre.

    | Salgsordre-ID | Arbeids-ID | Arbeidsmengde |
    |---|---|---|
    | Salgsordre 1 | Arbeids-ID 1 | 20 ea |
    | Salgsordre 2 | Arbeids-ID 2 | 6 ea (sum av begge linjer) |
    | Salgsordre 3 | Arbeids-ID 3 | 15 ea (sum av begge linjer) |
    | Salgsordre 4 | Arbeids-ID 4 | 35 ea (sum av begge linjer) |

Før du kjører flyten på den mobile enheten, må du kontrollere at bare arbeidet du nettopp opprettet, er i *Åpen* -status for lager *51* og *Salgsordre* -arbeidsordretypen. Ellers kan resultatene av testen variere, fordi den systemstyrte plukkingen vil inkludere alt kvalifisert arbeid.

1. Gå til **Lagerstyring \> Arbeid \> Utgående \> Åpnet salgsarbeid**.
1. Filtrere på **Lager** -feltet slik at bare arbeid på lager *51* vises i **Åpent salgsarbeid**.
1. Bekreft at bare de fire arbeids-ID-ene som du opprettet tidligere, vises.
1. Lukk **Arbeid** -siden.

### <a name="mobile-device-flow-execution"></a>Kjøring for mobilenhetflyt

På grunnlag av oppsettet vil systemet mate bruker arbeidet som er sortert etter det høyeste arbeidslinjeantallet, til det laveste. Antall på hver linje vil være mindre enn 20 ea.

Husk at dette oppsettet vil fange opp alt arbeid som har minst én linje der antallet er mindre enn 20 ea. Hvis arbeidet har en annen linje der antallet er nøyaktig 20 ea eller mer enn 20 ea, vil det også være gyldig.

#### <a name="mobile-app"></a>Mobilapp

1. Logg på lagerappen som en bruker i lageret *51*.
1. Gå til **Utgående \> Salgsplukking – system**.

    Plukktrinnet for arbeids-ID *4* presenteres. Denne arbeids-ID-en vises først på grunn av oppsettet til den systemstyrte spørringsrekkefølgen, der du angav at arbeidet skal utføres i rekkefølge basert på synkende arbeidslinjeantall.

1. Fullfør ønsket plukking og plasser for å lukke arbeids-ID-en.

    Deretter presenteres arbeids-ID *3*. En av arbeidslinjene er neste i sekvensen, basert på arbeidslinjeantallet.

1. Fullfør plukking og plasser for å lukke arbeids-ID-en.

    Deretter presenteres arbeids-ID *2*. Dette arbeidets plukklinje er neste i sekvensen.

1. Fullfør plukking og plasser for å lukke arbeids-ID-en.

    Det skal ikke presenteres noe mer arbeid for deg. Arbeids-ID *1* er ikke kvalifisert for dette menyelementet på mobilenheter, fordi spørringen angir at arbeidshoder bare skal regnes med hvis antallet på arbeidslinjene er mindre enn 20 ea.

## <a name="tips"></a>Tips!

De systemstyrte arbeidssekvensspørringene er *inklusive*. Det er viktig at du husker dette faktumet for noen oppsett. Du vil for eksempel at et bestemt menyelement skal behandle bare arbeid der arbeidsenheten er *ea* , og du angir denne begrensningen i **Område** -fanen i spørringen. I dette tilfellet vil alt arbeid der minst én arbeidslinje har arbeidsenheten som angis til *ea* , bli matet til arbeideren. Derfor kan dette arbeidet også omfatte arbeid der arbeidslinjer har en annen arbeidsenhet enn *ea* (for eksempel *boks* eller *pall* ). Spørringen vil bare ekskludere arbeidslinjer der arbeidslinjen er satt til *ea*.

I eksemplet fra dette scenariet ble derfor arbeids-ID *4* også hentet av spørringen. Når den ble opprettet, ble to linjer lagt til: én for 25 ea og en annen for 10 ea. Arbeidet ble fortsatt presentert for brukeren fordi minst én arbeidslinje har et antall på mindre enn 20 ea.

Avhengig av scenariet kan du forhindre denne virkemåten ved å bruke arbeidspauser.
