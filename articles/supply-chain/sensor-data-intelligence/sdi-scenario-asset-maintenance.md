---
title: Scenario for vedlikehold av ressurser
description: Denne artikkelen beskriver scenarioet for vedlikehold av ressurser, som lar deg bruke sensordata for å opprette tellerposter som sporer bruken av en maskinressurs.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: fcd16d09b4293046c457b602857ef8950e8259c6
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644064"
---
# <a name="the-asset-maintenance-scenario"></a>Scenario for vedlikehold av ressurser

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Ved hjelp av scenarioet for *vedlikehold av ressurser* kan du bruke sensordata til å opprette tellerposter. Tellerposter sporer bruken av en maskinressurs og brukes som inndata til å generere vedlikeholdsplanen for maskinressurser.

## <a name="video-instructions"></a>Videoinstruksjoner

Følgende video viser hvordan du konfigurerer og prøver ut vedlikeholdsscenarioet for anleggsmidler ved hjelp av standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md). Resten av delene i denne artikkelen inneholder de samme instruksjonene i et tekstbasert format.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58aRW]

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Klargjøre demodata for scenarioet for vedlikehold av ressurser

Hvis du vil bruke et demosystem til å teste scenarioet for *vedlikehold av ressurser*, må du bruke et system der [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert, velge den juridiske enheten *USMF* (bedrift) og klargjøre de ekstra demodataene som beskrevet i denne delen. Hvis du bruker dine egne sensorer og data, kan du hoppe over denne delen.

I denne delen konfigurerer du ressursen *AK-101, Air knife* i demodataene som et eksempel. Du vil deretter se hvordan kommende vedlikeholdsarbeid kan forutses, basert på forskjellige sensorsignaler som måler hvor mange timer trykkluftkniven har kjørt. Du skal også opprette en vedlikeholdsplan der trykkluftkniven må vedlikeholdes hver 10 000. time.

### <a name="set-up-a-sensor-simulator"></a>Konfigurer en sensorsimulator

Hvis du vil prøve dette scenarioet uten å bruke en fysisk sensor, kan du sette opp en simulator for å generere de nødvendige signalene. Hvis du vil ha mer informasjon, kan du se [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Opprett en ressursteller for å spore produksjonstimer

Følg disse trinnene for å opprette en ressursteller for å spore produksjonstimer.

1. Gå til **Aktivastyring \> Oppsett \> Aktivatyper \> Tellere**.
1. I handlingsruten velger du **Ny** for å opprette en teller.
1. I hodet angir du følgende verdier:

    - **Teller:** *ProductionHr*
    - **Navn:** *Produksjonstimer*

1. Angi følgende verdier i **Generelt**-hurtigfanen:

    - **Enhet:** *t*
    - **Oppdatering:** *Manuell*
    - **Aggregert total:** *Sum*

1. Velg **Legg til linje** på hurtigfanen **Aktivatyper**.
1. Angi *Trykkluftkniv* i feltet **Ressurstype** på den nye linjen.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Opprett en vedlikeholdsplan for ressursen

Gjør følgende for å opprette en vedlikeholdsplan for ressursen.

1. Gå til **Aktivastyring \> Oppsett \> Forebyggende vedlikehold \> Vedlikeholdsplan**.
1. I handlingsruten velger du **Ny** for å opprette en vedlikeholdsplan.
1. I hodet angir du følgende verdier:

    - **Vedlikeholdsplan:** *AirKnife*
    - **Navn:** *Plan for trykkluftkniver*

1. Angi følgende verdier i **Detaljer**-hurtigfanen:

    - **Plandato:** Angi dagens dato.
    - **Aktiv:** *Ja*

1. På **Linjer**-hurtigfanen velger du **Legg til aktivatellerlinje** for å legge til en linje i rutenettet. Angi deretter følgende verdier for den:

    - **Beskrivelse av arbeidsordre:** *Vedlikehold for trykkluftkniv*
    - **Vedlikeholdsjobbtype:** *Preventiv*
    - **Intervalltype:** *Gjentatt fra siste arbeidsordre*
    - **Periodefrekvens:** *10000*
    - **Teller:** *ProductionHr*

## <a name="set-up-the-asset-maintenance-scenario"></a>Sett opp scenarioet for vedlikehold av ressurser

Følg disse trinnene for å sette opp scenarioet for *vedlikehold av ressurser* i Supply Chain Management.

1. Gå til **Ressursbehandling \> Oppsett \> Sensordataintelligens \> Scenarioer**.
1. I scenarioboksen **Ressursbehandling** velger du **Konfigurer** for å åpne installasjonsveiseren for dette scenarioet.
1. På **Sensorer**-siden velger du **Ny** for å legge til en sensor i rutenettet. Angi deretter følgende felter for den:

    - **Sensor-ID** – Angi ID-en til sensoren du bruker. (Hvis du bruker Raspberry PI Azure IoT online-simulator og har konfigurert den som beskrevet i [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md), angir du *AssetMaintenance*.)
    - **Sensorbeskrivelse** – Angi en beskrivelse av sensoren.

1. Gjenta det forrige trinnet for hver ekstra sensor du vil legge til nå. Du kan gå tilbake og legge til flere sensorer når som helst.
1. Velg **Neste**.
1. Velg posten for én av sensorene du nettopp la til, på siden **Tilordning av forretningsoppføring**, i delen **Sensorer**.
1. I delen **Tilordning av forretningsoppføring** velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden skal feltet **Type forretningsoppføring** automatisk settes til *Ressurser (EntAssetObjectTable)*. Angi feltet **Forretningsoppføring** til ressursen du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du det til *AK-101, AK-101 Air Knife for Line 1*.)
1. Rett etter at du har valgt en forretningsposttype for raden du la til i det forrige trinnet, legges det automatisk til en ny rad i rutenettet. I denne raden må feltet **Type forretningsoppføring** settes til *Counters(EntAssetCounterType)*. Sett feltet **Forretningsoppføring** til ressurstelleren du oppdaterer, basert på signaler fra den valgte sensoren. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du det til *ProductionHr, Produksjonstimer*.)
1. Velg **Neste**.
1. I rutenettet på siden **Aktiver sensorer** velger du sensoren du har lagt til, og velger deretter **Aktiver**. For hver aktiverte kontakt i rutenettet vises det en hake i **Aktiv**-kolonnen.
1. Velg **Fullfør**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Arbeid med scenarioet for vedlikehold av ressurser

### <a name="view-counter-values"></a>Vis tellerverdier

Når dataene er klargjort, og scenarioet for *vedlikehold av ressurser* er konfigurert og aktivert, kan du se hvordan poster for en ressursteller settes inn, basert på sensordata.

1. Gå til **Aktivastyring \> Aktiva \> Alle aktiva**.
1. Finn og velg ressursen du vil undersøke. (Hvis du bruker demodataene som du opprettet tidligere i denne artikkelen, velger du *AK-101*.)
1. Gå til handlingsruten, **Ressurs**-fanen, **Preventiv**-gruppen, og velg **Tellere** for å åpne siden for tellerposter for ressursen *AK-101*.

### <a name="generate-maintenance-work-orders"></a>Generer arbeidsordrer for vedlikehold

Når du har aktivert scenario for *vedlikehold av ressurser* og definert vedlikeholdsplanen, kan du kjøre vedlikeholdsplanen for å generere arbeidsordrer for vedlikehold. Du finner mer informasjon om hvordan du arbeider med preventivt vedlikehold, ved å se [Oversikt over preventivt vedlikehold](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
