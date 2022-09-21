---
title: Maskinstatusscenarioet
description: Denne artikkelen beskriver maskinstatusscenarioet, som lar deg bruke sensordata for å overvåke tilgjengeligheten av utstyret.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 1f2b424dccf1963a7917059d412b5df7937496ee
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428410"
---
# <a name="the-machine-status-scenario"></a>Maskinstatusscenarioet

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Med *maskinstatusscenarioet* kan du bruke sensordata til å overvåke tilgjengeligheten av utstyret. Hvis du setter opp en sensor som sender et signal når en produksjonsjobb på en maskinressurs produserer utdata, men det ikke mottas noe signal innen et bestemt intervall, vises det et varsel på lederens instrumentbord.

## <a name="scenario-dependencies"></a>Avhengigheter for scenarioet

*Maskinstatus*-scenarioet har følgende avhengigheter:

- En varsling kan bare utløses hvis en produksjonsjobb pågår på en tilordnet maskin.
- Et signal som representerer et *del ut*-signal, må sendes til IoT-huben.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Klargjøre demodata for maskinstatusscenarioet

Hvis du vil bruke et demosystem til å teste *maskinstatus*-scenarioet, må du bruke et system der [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert, velge den juridiske enheten *USMF* (bedrift) og klargjøre de ekstra demodataene som beskrevet i denne delen. Hvis du bruker dine egne sensorer og data, kan du hoppe over denne delen.

### <a name="set-up-a-sensor-simulator"></a>Konfigurer en sensorsimulator

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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Konfigurere grensesnittet for produksjonsutførelse

Du bruker grensesnittet for kjøring på produksjonsgulv til å starte jobben som ble planlagt og frigitt for varenummer *P0111* i den forrige delen. Følg disse trinnene for å konfigurere grensesnittet for produksjonsutførelse:

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Produksjonsutførelse**.
1. Hvis du ikke har konfigurert grensesnittet tidligere, vises en påloggingsside. Angi legitimasjon.
1. På velkomstsiden velger du **Konfigurer** for å åpne veiviseren **Konfigurer enhetd**.
1. På siden **Konfigurer enhet – Trinn 1 – Velg konfigurasjon** velger du *Standard*-konfigurasjonen.
1. Velg **Neste**.
1. På siden **Konfigurer enhet – Trinn 2 – Definer produksjonsområdet** setter du **Ressurs**-feltet til *3118*.
1. Velg **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Aktiver søkealternativet i grensesnittet for produksjonsutførelse

For å gjøre det enklere å finne produksjonsjobben for produksjonsordren som ble frigitt tidligere, følger du denne fremgangsmåten for å aktivere søkealternativet i grensesnittet for produksjonsutførelse.

1. Gå til **Produksjonskontroll \> Oppsett \> Produksjonsutførelse \> Konfigurere produksjonsutførelse**.
1. Velg *Standard*-konfigurasjonen.
1. I handlingsruten velger du **Rediger**.
1. På **Generelt**-hurtigfanen angir du **Aktiver søk**-alternativet til *Ja*.
1. Lukk siden.

### <a name="start-the-first-job-in-the-batch-order"></a>Start den første jobben i partiordren

Følg denne fremgangsmåten for å starte jobben som er planlagt for ressurs *3118*.

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Produksjonsutførelse**.
1. Angi *123* i **Kort-ID**-feltet. Velg deretter **Logg på**.
1. Hvis du blir bedt om å angi fraværsårsak, velger du ett av kortene for fravær, og deretter velger du **OK**.
1. I **Søk**-feltet angir du partiordrenummeret du tidligere noterte. Trykk deretter på **Enter**-tasten.
1. Velg ordren, og velg deretter **Start jobb**.
1. I dialogboksen **Start jobb** velger du **Start**.

## <a name="set-up-the-machine-status-scenario"></a>Sett opp maskinstatusscenarioet

Følg disse trinnene for å sette opp *maskinstatusscenarioet* i Supply Chain Management.

1. Gå til **Produksjonskontroll \> Oppsett \> Sensordataintelligens \> Scenarioer**.
1. I boksen **Maskinstatus**-scenario velger du **Konfigurer** for å åpne installasjonsveiseren for dette scenarioet.
1. På **Sensorer**-siden velger du **Ny** for å legge til en sensor i rutenettet. Angi deretter følgende felter for den:

    - **Sensor-ID** – Angi ID-en til sensoren du bruker. (Hvis du bruker Raspberry PI Azure IoT online-simulator og har konfigurert den som beskrevet i [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md), angir du *MachineStatus*.)
    - **Sensorbeskrivelse** – Angi en beskrivelse av sensoren.

1. Gjenta det forrige trinnet for hver ekstra sensor du vil legge til nå. Du kan gå tilbake og legge til flere sensorer når som helst.
1. Velg **Neste**.
1. Velg posten for én av sensorene du nettopp la til, på siden **Tilordning av forretningsoppføring**, i delen **Sensorer**.
1. I delen **Tilordning av forretningsoppføring** velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden angir du feltet **Forretningsoppføring** til ressursen du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du feltet til *3118, Stoffskjærer*.)
1. Velg **Neste**.
1. På siden **Maskinstatusterskel** definerer du hvor lenge etter det siste *del ut*-signalet systemet skal sende en varsling om maskinstatus. Terskelen kan defineres på to måter:

    - **Standardterskel (minutter)** – Angi dette feltet for å definere standardterskelen. Verdien vil da gjelde for alle ressurser der feltet **Terskel for å fastslå at maskinen ikke svarer (i minutter)** er satt til to minutter eller mindre. Minimumsverdien er *2* (minutter).
    - **Terskel for å fastslå at maskinen ikke svarer (i minutter)** – For hver ressurs i rutenettet som du ikke vil bruke standardterskelen for, angir du en overstyringsverdi i dette feltet. Ressurser som er satt til å bruke en terskel på to minutter eller mindre, bruker i stedet innstillingen **Standardterskel (minutter)**.

    > [!NOTE]
    > Vanligvis vil du bruke et *del ut*-signal til å overvåke maskinstatusen. Derfor bør du kontrollere at terskelen for hver maskinressurs er lengre enn tiden maskinen trenger for å produsere hver del.

1. Velg **Neste**.
1. I rutenettet på siden **Aktiver sensorer** velger du sensoren du har lagt til, og velger deretter **Aktiver**. For hver aktiverte kontakt i rutenettet vises det en hake i **Aktiv**-kolonnen.
1. Velg **Fullfør**.

## <a name="work-with-the-machine-status-scenario"></a>Arbeid med maskinstatusscenarioet

Når du har installert sensorene og konfigurert scenarioet, kan du vise maskinstatushendelser i Supply Chain Management. Denne delen beskriver hvor og hvordan du viser denne informasjonen.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Vise maskinstatusdata på Ressursstatus-siden

På **Ressursstatus**-siden kan arbeidsledere overvåke en tidslinje over *del ut*-signalet som mottas fra sensorene som er tilordnet hver maskinressurs. Gjør følgende for å konfigurere tidslinjen.

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus**.
1. I **Konfigurer**-dialogboksen angir du følgende felter:

    - **Ressurs** – Velg ressursene du vil overvåke. (Hvis du arbeider med demodataene, velger du *3118*.)
    - **Tidsserie 1** – Velg posten (metrisk nøkkel) som har følgende format for navnet på maskinen: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Visningsnavn** – Angi *Deler ut-signal*.

Illustrasjonen nedenfor viser et eksempel på maskinstatusdata på **Ressursstatus**-siden under standard drift.

![Maskinstatusdata på Ressursstatus-siden under standard drift.](media/sdi-resource-status-downtime-up.png "Maskinstatusdata på Ressursstatus-siden under standard drift")

Illustrasjonen nedenfor viser et eksempel på maskinstatusdata når nedetid er oppdaget.

![Maskinstatusdata på Ressursstatus-siden når nedetid er oppdaget.](media/sdi-resource-status-downtime-down.png "Maskinstatusdata på Ressursstatus-siden når nedetid er oppdaget")

### <a name="view-machine-status-on-the-notifications-page"></a>Vis maskinstatus på Varslinger-siden

På **Varslinger**-siden kan arbeidsledere vise meldingene som genereres når det er gått for mye tid siden sensoren sist leverte et *del ut*-signal. Hver varsling gir en oversikt over produksjonsjobben som blir påvirket av strømbruddet, og gir muligheten til å tilordne den berørte jobben på nytt til en annen ressurs.

Du kan åpne **Varslinger**-siden ved å gå til **Produksjonskontroll \> Forespørsler og rapporter \> Sensordataintelligens \> Varslinger**.

Illustrasjonen nedenfor viser et eksempel på en varsling om maskinstatus.

![Eksempel på en varsling om maskinstatus.](media/sdi-resource-status-downtime-notification.png "Eksempel på en varsling om maskinstatus")
