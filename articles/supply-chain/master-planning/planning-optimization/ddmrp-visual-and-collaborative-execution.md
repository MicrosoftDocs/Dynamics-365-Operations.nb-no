---
title: Visuell og samarbeidsbasert kjøring
description: Denne artikkelen beskriver hvordan du overvåker DDMRP-utkoblingspunkter, buffersoner, planlagte bestillinger og historikk.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: e3afdd10860494b3cfe73a113a0e4e8fb07682a1
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186708"
---
# <a name="visual-and-collaborative-execution"></a>Visuell og samarbeidsbasert kjøring

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du overvåker DDMRP-utkoblingspunkter, buffersoner, planlagte bestillinger og historikk.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Spor buffere og antall visuelt for en valgt vare

I Microsoft Dynamics 365 Supply Chain Management kan du visualisere hvordan buffere, beholdningsantall og nettoflytnivåer endres over tid for et hvilket som helst valgt frigitt produkt. Følg denne fremgangsmåten for å åpne og se gjennom diagrammene.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg en frigitt vare som er definert som et utkoblingspunkt. (For mer informasjon, se [Lagerplassering](ddmrp-inventory-positioning.md).)
1. Gå til **Plan**-fanen i handlingsruten, og velg deretter **Varedekning**.
1. Velg en varedekningspost som oppretter et utkoblingspunkt, på **Varedekning**-siden. (Denne posten vil vise navnet på en dekningsgruppe som er konfigurert til å opprette utkoblingspunkter.)
1. Velg **Beholdning**-fanen. Denne fanen inneholder et diagram som viser hvordan lagerbeholdninger endres over tid, sammen med verdien av lagerbeholdningsnivå som ble registrert for en bestemt periode hver gang planleggingsoptimaliseringen kjøres. Fanen inneholder også en tabell som viser hvilke av følgende kategorier hver registrerte lagerbeholdning faller inn under:

    - **Kritisk lav** – Mindre enn halvparten av minimum for perioden.
    - **Lav** – Mellom halvparten av minimum og minimum.
    - **Gjennomsnittlig beholdning** – Mellom minimum og minimum pluss den grønne sonen.
    - **Høyere enn gjennomsnitt** – Høyere enn gjennomsnittet.

    ![Historiske lagerbeholdningnivåer på Beholdning-fanen.](media/ddmrp-on-hand-graph.png "Historiske lagerbeholdningnivåer på Beholdning-fanen")

    > [!NOTE]
    > Fargene som brukes på **Beholdning**-fanen, representerer andre områder enn de lignende fargene som brukes på **Bufferverdier**-fanen.

1. Hvis du vil vise hvordan bufferverdiene endres over tid og hvordan de kan sammenlignes med lagerbeholdnings- og nettoflytnivåer, velger du **Bufferverdier**-fanen.

    ![Historiske lagerbeholdnings- og nettoflytnivåer på Bufferverdier-fanen.](media/ddmrp-buffer-values-graph.png "Historiske lagerbeholdnings- og nettoflytnivåer på Bufferverdier-fanen")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Spor status og planlagte bestillinger for alle utkoblingspunkter

Arbeidsområdet **Behovsdrevet MRP** inneholder flere verktøy, sammen med KPI-er (nøkkelytelsesindikatorer) og oversikter over statusen til varer med utkoblingspunkter og tilknyttede planlagte bestillinger. Du kan åpne det ved å gå til **Hovedplanlegging \> Arbeidsområder \> Behovsdrevet MRP**.

![Arbeidsområdet Behovsdrevet MRP.](media/ddmrp-workspace.png "Arbeidsområdet Behovsdrevet MRP")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Få oversikt over utkoblingspunkter og planlagte bestillinger

I tillegg til arbeidsområdet **Behovsdrevet MRP** har Supply Chain Management flere sider der du kan vise informasjon om DDMRP-oppsettet, utkoblingspunkter og planlagte bestillinger. På noen av disse sidene finner du også knapper som er nyttige i handlingsruten, der du kan administrere buffere, kjøre hovedplanlegging og åpne andre relaterte visninger.

- Hvis du vil vise status for utkoblingspunkter etter nettoflytnivå, kan du gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Utkoblingspunktstatus etter nettoflyt**.
- Hvis du vil vise status for utkoblingspunkter etter lagerbeholdningsnivå, kan du gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Utkoblingspunktstatus etter beholdning**.
- Hvis du vil vise planlagte bestillinger for utkoblingspunkter, kan du gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Planlagte ordrer for utkoblingspunkter**.
- Hvis du vil vise utkoblede leveringstider, går du til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Utkoblet leveringstid**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Bufferverdier for oppryddingsutkoblingspunkt

Over tid vil systemet bygge opp en stor mengde historiske data som er knyttet til pågående bufferberegninger. Disse historiske dataene vil føre til at datavolumet øker, og til slutt kan det påvirke systemets ytelse. Vi anbefaler derfor at du av og til rydder opp i de gamle bufferverdiene for de utkoblingspunkter.

> [!WARNING]
> Oppryddingsjobben vil fjerne historiske innstillinger for bufferverdi og historisk informasjon om lagerbeholdning/nettoflyt. Den kan ikke tilbakestilles.

Følg denne fremgangsmåten for å rydde opp bufferverdier for utkoblingspunkter.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> DDMRP \> Bufferverdier for oppryddingsutkoblingspunkt**.
1. I dialogboksen **Bufferverdier for oppryddingsutkoblingspunkt** angir du verdier i følgende felter:

    - **Slett poster som er eldre enn (dager)** – Angi alderen på postene du vil beholde, i dager. Alle bufferverdiposter for utkoblingspunkter som er eldre enn denne verdien, blir slettet.
    - **Hovedplan** – Velg en hovedplan som inkluderer varene som vil bli påvirket av denne oppryddingen. Oppryddingen vil gjelde for alle varene i planen etter at **Filter**-innstillingene du angir i denne dialogboksen, er brukt.

1. Hvis du vil begrense settet med poster som den satsvise jobben skal kjøres på, går du til hurtigfanen **Poster som skal inkluderes**, og velger **Filter** for å åpne dialogboksen **Forespørsel**. Denne dialogbosen fungerer på samme måte som den fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Angi hvordan, når og hvor ofte oppryddinger skal utføres, på hurtigfanen **Kjør i bakgrunnen**. Feltene fungerer på samme måte som de fungerer for andre typer [bakgrunnsjobber](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) i Supply Chain Management.
1. Velg **OK** for å legge til den nye jobben i en satsvis kø for kjøring.
