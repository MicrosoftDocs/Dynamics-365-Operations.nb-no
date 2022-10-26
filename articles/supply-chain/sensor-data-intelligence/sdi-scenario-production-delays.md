---
title: Scenarioet for produksjonsforsinkelser
description: Denne artikkelen beskriver scenarioet for produksjonsforsinkelser, som genererer en varsling hvis produksjonsgjennomstrømningen faller under en spesifikk terskelverdi.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690028"
---
# <a name="the-production-delays-scenario"></a>Scenarioet for produksjonsforsinkelser

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Scenarioet for *produksjonsforsinkelser* genererer en varsling hvis produksjonsgjennomstrømningen faller under en spesifikk terskelverdi. I dette scenarioet sendes det et *del ut*-signal til Microsoft Azure IoT Hub for hver vare som produseres. I Dynamics 365 Supply Chain Management beregnes forsinkelsen på grunnlag av hvor lenge produksjonsordren er planlagt å kjøre, antall varer som skal produseres, hvor lenge jobben har vært aktiv, og antall *del ut*-signaler som er mottatt. Det vil bli generert en forsinkelsesvarsling hvis antallet *del ut*-signaler for jobben faller under terskelverdien.

## <a name="scenario-dependencies"></a>Avhengigheter for scenarioet

Scenarioet for *produksjonsforsinkelser* har følgende avhengigheter:

- Et varsel kan bare utløses hvis en produksjonsordre kjører på en tilordnet maskin.
- Et signal som representerer en tilordnet maskins *del ut*-signal, må sendes til IoT Hub, og et unikt egenskapsnavn må inkluderes.
- En UNIX timestamp-egenskap, der verdien angis i millisekunder (MS), må finnes i meldingen for Azure IoT-hub.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Klargjøre demodata for scenarioet for produktforsinkelser

Hvis du vil bruke et demosystem til å teste scenarioet for *produksjonsforsinkelser*, må du bruke et system der [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert, velge den juridiske enheten *USMF* (bedrift) og klargjøre de ekstra demodataene som beskrevet i denne delen. Hvis du bruker dine egne sensorer og data, kan du hoppe over denne delen.

### <a name="set-up-sensor-simulator"></a>Konfigurer sensorsimulatoren

Hvis du vil prøve dette scenarioet uten å bruke en fysisk sensor, kan du sette opp en simulator for å generere de nødvendige signalene. Hvis du vil ha mer informasjon, kan du se [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Kontroller at ressurs 3118 brukes for produkt P0111

En produksjonsordre vil bli planlagt og frigitt. Derfor frigis en produksjonsjobb til ressurs *3118* (*Stoffskjærer*). Følg denne fremgangsmåten for å kontrollere at ressurs *3118* brukes for produkt *P0111* i demodataene.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg produktet der feltet **Varenummer** er satt til *P0111*.
1. I handlingsruten, i fanen **Utvikling** i **Vis**-gruppen, velger du **Rute**.
1. På **Rute**-siden, på **Oversikt**-fanen nederst på siden, velger du linjen der feltet **Oper.nr.** er satt til *30*.
1. På fanen **Ressursbehov** nederst på siden må du kontrollere at ressurs *3118* (*Stoffskjærer*) er tilknyttet operasjonen.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Opprett og frigi en produksjonsordre for produkt P0111

Følg denne fremgangsmåten for å opprette og frigi en produksjonsordre for produkt *P0111*.

1. Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**.
1. På siden **Alle produksjonsordrer**, i handlingsruten, velger du **Ny partiordre**.
1. Angi følgende verdier i dialogboksen **Opprett parti**:

    - **Varenummer:** *P0111*
    - **Antall:** *10*

1. Velg **Opprett** for å opprette ordren og gå tilbake til siden **Alle produksjonsordrer**.
1. Bruk **Filter**-feltet til å søke etter produksjonsordrer der **Varenummer**-feltet er satt til *P0111*. Deretter må du finne og velge produksjonsordren du nettopp opprettet.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Estimat**.
1. Velg **OK** i dialogboksen **Estimat** for å kjøre estimatet.
1. I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Frigi**.
1. Skriv en merknad om nummeret på partiordren du akkurat opprettet, i dialogboksen **Frigi**.
1. Velg **OK** for å frigi ordren.

### <a name="configure-the-production-floor-execution-interface"></a>Konfigurere grensesnittet for produksjonsutførelse

Hvis du ikke allerede har gjort det, kan du konfigurere grensesnittet for kjøring på produksjonsgulvet for å vise jobber som er tilordnet til ressurs *3118* (*Stoffskjærer*). Se følgende deler hvis du vil ha instruksjoner:

- [Konfigurere grensesnittet for produksjonsutførelse](sdi-scenario-equipment-downtime.md#config-pfe)
- [Aktiver søkealternativet i grensesnittet for produksjonsutførelse](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Start den første jobben i partiordren

Følg denne fremgangsmåten for å starte den første jobben i partiordren.

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Produksjonsutførelse**.
1. Angi *123* i **Kort-ID**-feltet. Velg deretter **Logg på**.
1. Hvis du blir bedt om å angi fraværsårsak, velger du ett av kortene for fravær, og deretter velger du **OK**.
1. I **Søk**-feltet angir du partiordrenummeret du tidligere noterte. Trykk deretter på **Enter**-tasten.
1. Velg ordren, og velg deretter **Start jobb**.
1. I dialogboksen **Start jobb** velger du **Start**.

## <a name="set-up-the-production-delays-scenario"></a>Sett opp scenarioet for produksjonsforsinkelser

Følg disse trinnene for å sette opp scenarioet for *produksjonsforsinkelser* i Supply Chain Management.

1. Gå til **Produksjonskontroll \> Oppsett \> Sensordataintelligens \> Scenarioer**.
1. I scenarioboksen **Produksjonsforsinkelser** velger du **Konfigurer** for å åpne installasjonsveiseren for dette scenarioet.
1. På **Sensorer**-siden velger du **Ny** for å legge til en sensor i rutenettet. Angi deretter følgende felter for den:

    - **Sensor-ID** – Angi ID-en til sensoren du bruker. (Hvis du bruker Raspberry PI Azure IoT online-simulator og har konfigurert den som beskrevet i [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md), angir du *ProductionDelay*.)
    - **Sensorbeskrivelse** – Angi en beskrivelse av sensoren.

1. Gjenta det forrige trinnet for hver ekstra sensor du vil legge til nå. Du kan gå tilbake og legge til flere sensorer når som helst.
1. Velg **Neste**.
1. Velg posten for én av sensorene du nettopp la til, på siden **Tilordning av forretningsoppføring**, i delen **Sensorer**.
1. I delen **Tilordning av forretningsoppføring** velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du **Forretningsoppføring** til ressursen du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du det til *3118, Stoffskjærer*.)
1. Velg **Neste**.
1. Følg trinnene på siden **Avviksterskel for produksjonsforsinkelse** hvis du bruker demodataene du opprettet tidligere i denne artikkelen:

    1. Velg kolonneoverskriften **Varerelasjon** for å åpne en dialogboks som inneholder søkefiltre for kolonnen. Angi *P0111* i søkeboksen, og velg deretter **Bruk**.
    2. Velg linjen der **Operasjon**-feltet er satt til *Trimming/skjæring*. Angi feltet **Varslingsterskel for forsinkelse (%)** til terskelen (som en prosent) for når en varsling skal sendes.

1. Velg **Neste**.
1. I rutenettet på siden **Aktiver sensorer** velger du sensoren du har lagt til, og velger deretter **Aktiver**. For hver aktiverte kontakt i rutenettet vises det en hake i **Aktiv**-kolonnen.
1. Velg **Fullfør**.

## <a name="work-with-the-production-delays-scenario"></a>Arbeid med scenarioet for produksjonsforsinkelser

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Vise produksjonsforsinkelsesdata på Ressursstatus-siden

På **Ressursstatus**-siden kan arbeidsledere overvåke en tidslinje over signaler som mottas fra sensorene som er tilordnet hver maskinressurs. Gjør følgende for å konfigurere tidslinjen.

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus**.
1. I **Konfigurer**-dialogboksen angir du følgende felter:

    - **Ressurs** – Velg ressursene du vil overvåke. (Hvis du arbeider med demodataene, velger du *3118*.)
    - **Tidsserie 1** – Velg posten (metrisk nøkkel) som har følgende format for navnet på maskinen: *ProductionJobDelayed:ActualQuantity:&lt;JobId&gt;*
    - **Visningsnavn** – Angi *Deler ut-signal*.
