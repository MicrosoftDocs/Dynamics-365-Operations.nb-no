---
title: Pakkearbeid for pakking av utgående beholdere og behandling av forsendelser
description: Denne artikkelen beskriver arbeidsordretypen Pakking, som styrer arbeid for pakkebeholdere og støtter delvise forsendelser av pakkede beholdere som er knyttet til belastninger der lagervarer ikke er pakket.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220591"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Pakkearbeid for pakking av utgående beholdere og behandling av forsendelser

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver arbeidsordretypen *Pakking*, som styrer arbeid for pakkebeholdere og støtter delvise forsendelser av pakkede beholdere som er knyttet til belastninger der lagervarer ikke er pakket. Ved hjelp av pakkearbeid kan du bruke funksjonaliteten for [bekreftelse og overføring](confirm-and-transfer.md) til å bekrefte utgående forsendelser som er tilknyttet beholdere.

Pakkearbeid opprettes automatisk når lager som er relatert til kildedokumentarbeid, legges på lokasjoner av typen *Pakkelokasjon*. Arbeidet består av to linjer, en for *plukking* og en for *plassering*, og vedlikeholdes automatisk som en del av en beholderlukkingsprosess som åpnes på nytt.

Hvis du vil ha mer informasjon om hvordan du definerer og bruker beholderpakkeprosessen, kan du se [Pakk beholdere for forsendelse](packing-containers.md).

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i denne artikkelen, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere følgende funksjoner i følgende rekkefølge. Begge funksjonene er den del av modulen for **Lagerstyring**.

1. *Bekreft og overfør*
1. *Pakkearbeid for pakkestasjoner*

## <a name="set-up-a-location-for-packing-work"></a>Konfigurer en lokasjon for pakkearbeid

Bruk fremgangsmåten nedenfor for å konfigurere pakkelokasjoner. For hver lokasjon kan du velge om systemet automatisk oppretter pakkearbeid.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkestasjonsoppsett**.
1. I handlingsruten velger du **Ny** for å legge til en post for pakkestasjonsoppsett.
1. I den nye posten angir du følgende felter:

    - **Lager** – Velg eller angi lageret der pakkelokasjonen finnes.
    - **Lokasjon** – Velg eller angi pakkelokasjonen. Denne lokasjonen må være tildelt en lokasjonsprofil som bruker lokasjonstypen som er konfigurert som pakkelokasjonstype for firmaet på siden **Lagerstyringsparametere**. Hvis du vil ha mer informasjon , kan du se [Pakk beholdere for forsendelse](packing-containers.md).
    - **Opprett pakkearbeid** – Merk av for denne avmerkingsboksen for å opprette pakkearbeid hver gang varer leveres til pakkelokasjonen. Arbeidet vil inneholde koblinger til tilknyttede belastningslinjer, slik at delvise belastninger kan pakkes og sendes.

## <a name="example-scenario"></a>Eksempelscenario

Dette eksempelscenarioet viser hvordan du behandler en utgående salgsordreflyt ved å pakke en beholder og sende en delvis belastning.

### <a name="make-sample-data-available"></a>Gjøre eksempeldata tilgjengelig

For å arbeide deg gjennom dette scenariet ved å bruke de angitte eksempelpostene og -verdiene som er angitt her, må du være på et system der standard [demodata](../../fin-ops-core/fin-ops/get-started/demo-data.md) er installert. Du må også velge den juridiske enheten **USMF** før du begynner.

Du kan også bruke dette scenarioet som en veiledning for å bruke funksjonen i et produksjonssystem. I så fall må du imidlertid bytte dine egne verdier for hver innstilling som beskrives her.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Konfigurer pakkearbeid for lagerets pakkelokasjon

For å komme i gang må du konfigurere arbeidsprosessen *Pakking* for et bestemt lager og en bestemt lokasjon.

1. Gå til **Lagerstyring \> Oppsett \> Pakking \> Pakkestasjonsoppsett**.
1. Velg **Ny** for å legge til en oppsettpost i handlingsruten.
1. I den nye oppføringen angir du følgende verdier:

    - **Lager:** *62*
    - **Plassering:** *Pakke*
    - **Opprett pakkearbeid:** *Ja*

1. Lukk siden **Pakkestasjonsoppsett**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Opprett en belastningsmal som tillater delvis levering

Hvis du vil gjøre det mulig å levere en belastning for flere forsendelser, må du knytte den til en belastningsmal som tillater dellevering. Følg denne fremgangsmåten for å opprette den nødvendige malen.

1. Gå til **Lagerstyring \> Oppsett \> Last \> Lastmaler**.
1. Velg **Ny** for å legge til en oppsettpost i handlingsruten.
1. I den nye oppføringen angir du følgende verdier:

    - **Lastmal-ID:** *Delvis*
    - **Tillat deling av belastning under forsendelsesbekreftelse:** *Ja*

1. Lukk siden **Belastningsmaler**.

Hvis du vil ha mer informasjon, kan du se [Bekreft og overfør](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Behandle en salgsordre

Følg denne fremgangsmåten for å behandle en salgsordre og sende den delvis.

1. Fullfør [eksempelscenarioet](packing-containers.md#scenario) som finnes i [Pakk beholdere for forsendelse](packing-containers.md). I løpet av dette scenarioet oppretter du en salgsordre for to stykker av én vare. Deretter pakkes bare én av delene i en beholder og lukker beholderen. Du bør notere deg forsendelses-ID-en du oppretter, slik det er instruert i scenarioet.
1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid**.
1. Merk av for **Vis lukket arbeid** i filterområdet. Deretter angir du forsendelses-ID-en i **Filter**-feltet og velger å filtrere etter verdien **Forsendelses-ID**. Du skal nå se tre arbeidshoder. Den ene er for salgsordreplukkingen og har statusen *Lukket*. To er for pakkeprosessen: en er knyttet til den lukkede beholderen og har statusen *Lukket*, og den andre er knyttet til den utpakkede gjenværende varen og har statusen *Åpen*.
1. Velg verdien **Belastnings-ID** for et av arbeidshodene for å åpne siden **Belastningsdetaljer**.
1. Bytt til **Topptekst**-visningen.
1. I hurtigfanen **Generelt** velger du **Rediger**-knappen for feltet **Belastningsmal-ID**. Deretter velger du den delvise forsendelsesbelastningsmalen du opprettet for dette scenarioet (*Delvis*).
1. Velg **Utgående forsendelse** i **Send og motta**-fanen i **Bekreft**-gruppen.
1. Velg alternativet **Del antall til ny belastning** i dialogboksen **Forsendelsesbekreftelse**.
1. Velg **OK**.

Du har nå sendt én beholder som er knyttet til den opprinnelige belastningen, og systemet har opprettet en ny belastning for de gjenværende varene som fortsatt må pakkes i beholdere.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
