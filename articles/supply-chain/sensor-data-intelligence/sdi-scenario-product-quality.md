---
title: Scenarioet for produktkvalitet
description: Denne artikkelen inneholder informasjon om scenarioet for produktkvalitet. Dette scenarioet bruker en sensor til å måle kvaliteten på et produktparti og genererer et varsel hvis en måling faller utenfor en definert terskel.
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
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690055"
---
# <a name="the-product-quality-scenario"></a>Scenarioet for produktkvalitet

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

I scenarioet for *produktkvalitet* settes det opp en sensor for å måle kvaliteten på et produktparti i butikken. Hvis en måling faller utenfor en definert terskel for produktet, vises det en varsling på lederens instrumentbord. Eksempel: En sensor måler fuktigheten i et matprodukt som er levert fra produksjonslinjen. Hvis målingen er utenfor den tillatte minimums- eller maksimumsverdien for fuktighet for produktet, genereres det en varsling.

## <a name="scenario-dependencies"></a>Avhengigheter for scenarioet

Scenarioet for *produktkvalitet* har følgende avhengigheter:

- Et varsel utløses bare hvis en produksjonsordre kjører på en tilordnet maskin, og hvis denne maskinen produserer et produkt med et tilordnet partiattributt.
- Et signal som representerer partiattributtet, må sendes til IoT-huben, og et unikt egenskapsnavn må inkluderes.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Klargjøre demodata for scenarioet for produktkvalitet

Hvis du vil bruke et demosystem til å teste scenarioet for *produktkvalitet*, må du bruke et system der [demodataene](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert, velge den juridiske enheten *USMF* (bedrift) og klargjøre de ekstra demodataene som beskrevet i denne delen. Hvis du bruker dine egne sensorer og data, kan du hoppe over denne delen.

I denne delen konfigurerer du demodataene slik at du kan bruke det frigitte produktet *P0111* (*Komposittkasse*) med scenarioet for *produktkvalitet*. I dette scenarioet sporer systemet om en partiattributtverdi som måles av en sensor, er utenfor den definerte terskelen for et partiattributt som er tilknyttet produktet.

### <a name="set-up-a-sensor-simulator"></a>Konfigurer en sensorsimulator

Hvis du vil prøve dette scenarioet uten å bruke en fysisk sensor, kan du sette opp en simulator for å generere de nødvendige signalene. Hvis du vil ha mer informasjon, kan du se [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Knytte et partiattributt og en ressurs til produkt P0111

Følg denne fremgangsmåten for å knytte et partiattributt til produkt *P0111* (*Komposittkasse*), og bekreft at ressurs *3118* (*Stoffskjærer*) brukes.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Finn og velg produktet der feltet **Varenummer** er satt til *P0111*.
1. I handlingsruten i **Partiattributter**-gruppen i kategorien **Administrer lager**, velger du **Produktspesifikk**.
1. På siden **Produktspesifikk** velger du **Ny** for å opprette et produktspesifikt partiattributt.
1. I hodet angir du følgende felter:

    - **Attributtkode** – Velg omfanget for attributter du vil overvåke (*Tabell*, *Gruppe* eller *Alle*). I dette scenarioet velger du *Tabell*, fordi du alltid skal overvåke ett enkelt attributt.
    - **Attributtrelasjon** – Velg attributtet du vil bruke til å overvåke verdien for i scenarioet for *produktkvalitet*. For dette eksemplet velger du *Konsentrasjon*, som er et attributt som er inkludert i standard demodata.

1. På hurtigfanen **Verdier**, i feltene **Minimum** og **Maksimum**, definerer du området for godtatte verdier som attributtet må rapportere, for å bestå kvalitetskontrollen. Hvis sensorrapportene viser en verdi utenfor dette området, vil systemet identifisere den som et kvalitetsbrudd. De andre feltene på denne hurtigfanen er ikke relevante for scenariet for *produktkvalitet*. Standardverdiene du ser for øyeblikket, kommer fra demodataene. La dem derfor være som de er, og lukk siden **Produktspesifikk** for å gå tilbake til siden **Detaljer om frigitt produkt** for varen *P0111*.
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

## <a name="set-up-the-product-quality-scenario"></a>Sett opp scenarioet for produktkvalitet

Følg disse trinnene for å sette opp scenarioet for *produktkvalitet* i Supply Chain Management.

1. Gå til **Produksjonskontroll \> Oppsett \> Sensordataintelligens \> Scenarioer**.
1. I scenarioboksen **Produktkvalitet** velger du **Konfigurer** for å åpne installasjonsveiseren for dette scenarioet.
1. På **Sensorer**-siden velger du **Ny** for å legge til en sensor i rutenettet. Angi deretter følgende felter for den:

    - **Sensor-ID** – Angi ID-en til sensoren du bruker. (Hvis du bruker Raspberry PI Azure IoT online-simulator og har konfigurert den som beskrevet i [Sett opp en simulert sensor for testing](sdi-set-up-simulated-sensor.md), angir du *Kvalitet*.)
    - **Sensorbeskrivelse** – Angi en beskrivelse av sensoren.

1. Gjenta det forrige trinnet for hver ekstra sensor du vil legge til nå. Du kan gå tilbake og legge til flere sensorer når som helst.
1. Velg **Neste**.
1. Velg posten for én av sensorene du nettopp la til, på siden **Tilordning av forretningsoppføring**, i delen **Sensorer**.
1. I delen **Tilordning av forretningsoppføring** velger du **Ny** for å legge til en rad i rutenettet.
1. I den nye raden skal feltet **Type forretningsoppføring** automatisk settes til *Resources(WrkCtrTable)*. Angi feltet **Forretningsoppføring** til ressursen du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du det til *3118, Stoffskjærer*.)
1. Rett etter at du har valgt en forretningsposttype for raden du la til i det forrige trinnet, legges det automatisk til en ny rad i rutenettet. I denne raden må feltet **Type forretningsoppføring** settes til *Batch attributes(PdsBatchAttrib)*. Angi feltet **Forretningsoppføring** til partiattributtet du bruker den valgte sensoren til å overvåke. (Hvis du bruker demodataene du opprettet tidligere i denne artikkelen, setter du det til *Konsektrasjon, Konsentrasjonsprosent*.)
1. Velg **Neste**.
1. I rutenettet på siden **Aktiver sensorer** velger du sensoren du har lagt til, og velger deretter **Aktiver**. For hver aktiverte kontakt i rutenettet vises det en hake i **Aktiv**-kolonnen.
1. Velg **Fullfør**.

## <a name="work-with-the-product-quality-scenario"></a>Arbeid med scenarioet for produktkvalitet

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Vise produktkvalitetsdata på Ressursstatus-siden

På **Ressursstatus**-siden kan arbeidsledere overvåke en tidslinje over produktkvalitetssignalet som mottas fra sensorene som er tilordnet hver maskinressurs. Gjør følgende for å konfigurere tidslinjen.

1. Gå til **Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus**.
1. I **Konfigurer**-dialogboksen angir du følgende felter:

    - **Ressurs** – Velg ressursene du vil overvåke. (Hvis du arbeider med demodataene, velger du *3118*.)
    - **Tidsserie 1** – Velg posten (metrisk nøkkel) som har følgende format for navnet på maskinen: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Visningsnavn** – Angi *Partiattributtverdier*.

Illustrasjonen nedenfor viser et eksempel på produktkvalitetsdata på **Ressursstatus**-siden når verdien er innenfor området for akseptable verdier.

![Produktkvalitetsdata på Ressursstatus-siden når verdien er innenfor området.](media/sdi-product-quality-in-range.png "Produktkvalitetsdata på Ressursstatus-siden når verdien er innenfor området")

Illustrasjonen nedenfor viser et eksempel på produktkvalitetsdata når det oppdages en verdi utenfor området.

![Produktkvalitetsdata på Ressursstatus-siden når en verdi utenfor området er oppdaget.](media/sdi-product-quality-out-of-range.png "Produktkvalitetsdata på Ressursstatus-siden når en verdi utenfor området er oppdaget")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Vise produktkvalitetsdata på Varslinger-siden

På **Varslinger**-siden kan arbeidsledere vise varslingen som genereres når sensoren måler en partiattributtverdi som faller utenfor den definerte terskelen for partiattributtet. Hver varsling gir en oversikt over produksjonsjobben som blir påvirket av strømbruddet, og gir muligheten til å tilordne den berørte jobben på nytt til en annen ressurs.

Du kan åpne **Varslinger**-siden ved å gå til **Produksjonskontroll \> Forespørsler og rapporter \> Sensordataintelligens \> Varslinger**.

Illustrasjonen nedenfor viser et eksempel på en produktkvalitetsvarsling.

![Eksempel på en produktkvalitetsvarsling.](media/sdi-product-quality-notification.png "Eksempel på en produktkvalitetsvarsling")
