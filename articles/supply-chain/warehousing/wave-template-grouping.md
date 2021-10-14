---
title: Gruppering av bølgemal
description: Bølgemalgruppering gjør det mulig for systemet å bruke bølgemaloppsett til å fastslå, basert på kriterier du definerer, hvordan de skal dele frigitte linjer og tilordne dem til nye eller eksisterende bølger. Denne funksjonen kan være nyttig på lagre der bølger opprettes basert på bestemte kriterier, men der ledere foretrekker å opprette bølger automatisk i stedet for å bruke dem manuelt.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: b265c0d5cb43e151386fe90e3a3dea414ec0aca6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579910"
---
# <a name="wave-template-grouping"></a>Gruppering av bølgemal

[!include [banner](../includes/banner.md)]

Bølgemalgruppering gjør det mulig for systemet å bruke [bølgemaloppsett](tasks/configure-wave-processing.md) til å fastslå, basert på kriterier du definerer, hvordan de skal dele frigitte linjer og tilordne dem til nye eller eksisterende bølger. Denne funksjonen kan være nyttig på lagre der bølger opprettes basert på bestemte kriterier, men der ledere foretrekker å opprette bølger automatisk i stedet for å bruke dem manuelt. Det gjør det mulig for systemet å legge til alle nylig frigitte forsendelser i den første bølgen som blir funnet med samsvarende grupperingsfeltverdier. Hvis det ikke blir funnet noen treff, oppretter systemet en ny bølge for den nye forsendelsen.

> [!IMPORTANT]
> Bølgemalgruppering støttes ikke for arbeidstypene *råvareplukking for produksjon* eller *Kanban-plukking*. Dette skyldes at bølgegruppering er basert på forsendelser, og at disse arbeidstypene ikke bruker forsendelser.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Aktivere funksjonen Bølgemalgruppering

Før du kan bruke *Bølgemalgruppering*-funksjonen, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Bølgemalgruppering*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Angi en bølgemal for å bruke bølgemalgruppering

Hvis du vil gjøre bølgemalgruppering tilgjengelig, følger du disse trinnene for å konfigurere [bølgemalen](tasks/configure-wave-processing.md).

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. Velg bølgemalen du vil sette opp, i venstre rute. Hvis du forbereder deg til å arbeide gjennom scenariet senere i dette emnet ved hjelp av demodata, velger du **62 Standardforsendelse**-malen.
1. Velg **Rediger** for å legge siden inn i redigeringsmodus.
1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Automatiser bølgeoppretting:** *Ja*
    - **Tilordne til åpne bølger:** *Ja*
    - **Behandle bølge ved frigivelse til lager:** *Nei*

1. I handlingsruten velger du **Rediger spørring** for å åpne dialogboksen for spørring.
1. I dialogboksen for spørring, på **Sortering**-fanen, går du gjennom sorteringskriteriene, og kontroller at det finnes en regel som inkluderer feltet som du vil bruke til å gruppere bølger.

    Hvis du forbereder deg til å arbeide gjennom scenariet ved hjelp av demodata, legger du til en rad som har følgende verdier:

    - **Tabell:** *Forsendelser*
    - **Avledet tabell:** *Forsendelser*
    - **Felt:** *Transportørtjeneste*

        > [!NOTE]
        > Når du har valgt denne verdien, kan du få følgende melding: Feltet Transportørtjeneste er ikke et indeksfelt. Vil du legge til sortering på dette? Velg **Ja** for å legge til sortering.

    - **Søkeretning:** *Stigende*

1. Velg **OK** for å lagre endringene og lukke dialogboksen for spørring.
1. Velg **Bølgemalgruppering** i handlingsruten.
1. På **Bølgemalgruppering**-siden velger du **Grupper etter**-avmerkingsboksen for hver rad du vil bruke til å gruppere ordrelinjer i bølger, etter behov. Hvis du er klar til å arbeide gjennom scenariet ved hjelp av demondata, merker du av **Grupper etter**-avmerkingsboksen for *Transportørtjeneste*-raden.
1. Velg **Lagre**.
1. Lukk **Bølgemalgruppering**-siden.
1. Velg **Lagre** for å lagre malen.

## <a name="scenario"></a>Scenario

Denne delen inneholder et skript som du kan arbeide gjennom for å lære hva denne funksjonen gjør, og hvordan du arbeider med den.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke dette scenariet som en veiledning for å bruke funksjonen når du arbeider i et produksjonssystem. I så fall må du imidlertid erstatte dine egne verdier, og det kan hende du mangler noen typer obligatoriske oppføringer som standard demonstrasjonsdata gir.

### <a name="scenario-wave-template-grouping"></a>Scenario: Bølgemalgruppering

Dette scenariet viser hvordan du bruker bølgemalgruppering til å opprette flere bølger automatisk basert på grupperingskriterier som er definert i en bølgemal. I dette scenariet er bølgemalen satt opp i systemet for å opprette én bølge per transportørtjeneste.

Før du begynner, klargjør du bølgemalen som beskrevet i delen [Angi en bølgemal for å bruke bølgemalgruppering](#set-up-template) tidligere i dette emnet. Hvis du skal arbeide med demonstrasjonsdata for dette scenariet, må du passe på å bruke demodataverdiene som foreslås i denne prosedyren. Dette oppsettet vil gruppere bølger i henhold til transportørtjenesten som er angitt for hver salgsordre.

#### <a name="create-sales-order-1"></a>Opprett salgsordre 1

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-004*.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.

1. Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.
1. Den nye salgsordren åpnes i **Linjer**-visningen. Noter deg salgsordrenummeret.
1. Bytt til **Topptekst**-visningen.
1. På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:

    - **Transportør:** *Luftlast*
    - **Transportørtjeneste:** *Lufttransport*

1. Gå tilbake til **Linjer**-visningen.
1. I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Varenummer:** *A0002*
    - **Antall:** *2*

1. Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.
1. På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren. Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Vis bølgen som ble opprettet fra salgsordre 1

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølge-ID-en som ble opprettet fra salgsordren.
1. Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.
1. Legg merke til at forsendelsen er lagt til i **Bølgelinjer**-hurtigfanen.

#### <a name="create-sales-order-2"></a>Opprett salgsordre 2

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-005*.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.

1. Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.
1. Den nye salgsordren åpnes i **Linjer**-visningen. Noter deg salgsordrenummeret.
1. Bytt til **Topptekst**-visningen.
1. På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:

    - **Transportør:** *Blomsterflytting*
    - **Transportørtjeneste:** *Std*

1. Gå tilbake til **Linjer**-visningen.
1. I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *1*

1. Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.
1. På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren. Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre. Legg merke til at bølge-ID-en er forskjellig fra bølge-ID-en i den første salgsordren.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Vis bølgen som ble opprettet fra salgsordre 2

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølge-ID-en som ble opprettet fra den andre salgsordren.
1. Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.
1. Legg merke til at forsendelsen er lagt til i **Bølgelinjer**-hurtigfanen.

En ny bølge ble opprettet for denne forsendelsen, fordi den bruker en annen transportørtjeneste enn den første salgsordren.

#### <a name="create-sales-order-3"></a>Opprett salgsordre 3

1. Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**.
1. Velg **Ny** for å opprette en salgsordre.
1. I **Opprett salgsordre**-dialogboksen angir du følgende verdier:

    - På **Kunde**-hurtigfanen angir du **Kundekonto**-feltet til *US-006*.
    - På hurtigfanen **Generelt** angir du **Lager**-feltet til *62*.

1. Velg **OK** for å opprette salgsorden og lukke **Opprett salgsordre**-dialogboksen.
1. Den nye salgsordren åpnes i **Linjer**-visningen. Noter deg salgsordrenummeret.
1. Bytt til **Topptekst**-visningen.
1. På **Levering**-hurtigfanen, i **Transport**-inndelingen angir du følgende verdier:

    - **Transportør:** *Luftlast*
    - **Transportørtjeneste:** *Lufttransport*

1. Gå tilbake til **Linjer**-visningen.
1. I **Salgsordrelinjer**-inndelingen velger du **Legg til linje** for å legge til en linje i rutenettet.
1. På den nye linjen angir du følgende verdier:

    - **Varenummer:** *A0001*
    - **Antall:** *1*

1. Velg den nye ordrelinjen og deretter på **Beholdning**-menyen over rutenett, velger du **Reservasjon**.
1. På **Reservasjon**-siden, i handlingsruten, velger du **Reserver parti** for å reservere den valgte linjens fulle antall i lageret.
1. Lukk **Reservasjon**-siden for å gå tilbake til salgsordren.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Du mottar en informasjonsmelding som viser forsendelse og bølge for denne ordren. Skriv ned ID-nummeret for bølgen og forsendelses-ID-numre. Forsendelsen er tilordnet den eksisterende bølgen fra den første salgsordren.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Vis bølgen for salgsordrer 1 og 3

1. Gå til **Lagerstyring \> Utgående bølger \> Forsendelsesbølger \> Alle bølger**.
1. Velg bølge-ID-en som ble opprettet fra den tredje salgsordren.
1. Velg bølge-ID-koblingen for å åpne siden for bølgedetaljer.
1. Legg merke til at forsendelsen er lagt til på **Bølgelinjer**-hurtigfanen sammen med forsendelsen for den første salgsordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]