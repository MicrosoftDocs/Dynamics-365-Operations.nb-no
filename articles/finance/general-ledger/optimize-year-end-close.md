---
title: Optimaliser årsavslutningen
description: Denne artikkelen beskriver tilleggsprogrammet for tjenesten Optimaliser årsavslutningen som er tilgjengelig for årsavslutningen i økonomimodulen.
author: moaamer
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: bc6ab7e36f37707442f8d5d5b6e0d5f5d42e2171
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831536"
---
# <a name="optimize-year-end-close"></a>Optimaliser årsavslutningen 

Når du bruker tilleggsprogrammet for tjenesten Optimaliser årsavslutningen for Microsoft Dynamics 365 Finance, kan årsavslutningen kjøre utenfor forekomsten av Application Object Server (AOS) for Dynamics 365 Finance-ressurser. Det bruker mikrotjenesteteknologi. Fordelene som er knyttet til funksjonaliteten Optimaliser årsavslutningen, omfatter forbedret ytelse og minimert innvirkning på SQL-databasen under behandlingen av årsavslutningen.

>[!NOTE]
> Det optimaliserte årsavslutningen er tilgjengelig på Microsoft Dynamics 365 Finance-versjon 10.0.31. Denne funksjonen er tilbakeportert til Dynamics Finance-versjonene 10.0.30 og 10.0.29, og du må ta den siste kvalitetsoppdateringen.   

For å kunne bruke funksjonaliteten Optimaliser årsavslutningen må du fullføre følgende oppgaver:

1. Installer tilleggsprogrammet for tjenesten Optimaliser årsavslutningen fra prosjektet i Microsoft Dynamics Lifecycle Service.
2. Aktiver funksjonen **Optimaliser årsavslutningen** i Funksjonsbehandling.

> [!NOTE]
> Du kan fortsatt bruke gjeldende funksjonalitet for årsavslutning for Finance ved å deaktivere funksjonen **Optimaliser årsavslutningen** i Funksjonsbehandling.

## <a name="improved-performance"></a>Ytelsen er forbedret

Funksjonen **Optimaliser årsavslutningen** er utviklet for å akselerere behandlingen av årsavslutningen, særlig for kunder med mye data. Når årsavslutningen kjører på en tjeneste, blir den tunge behandlingen avlastet fra Finance-ressurser for å redusere behandlingstiden og frigjøre ressursene som kan påvirke de daglige oppgavene til andre brukere.

Funksjonen **Optimaliser årsavslutningen** kan hjelpe deg å oppnå følgende mål:

- Forbedre ytelsen til årsavslutningen ved å redusere kjøretiden.
- Reduser innvirkningen på andre prosesser under kjøring av årsavslutningen.
- Forbedre rapportering og justeringer for årsavslutningsresultatene, fordi kjøring av årsavslutningen tar kortere tid.

## <a name="new-options-and-visibility"></a>Nye alternativer og synlighet

Når funksjonen **Optimaliser årsavslutningen** er aktivert, blir to nye kolonner, **Resultater** og **Status**, lagt til på følgende steder:

- På siden **Årsavslutning**
- Dialogboksen **Årsavslutningsresultater**
- I alternativene for **Overføring av finansdimensjoner for balanse** på siden **Årsavslutningsmal**

Illustrasjonen nedenfor viser et eksempel på kolonnene **Resultater** og **Status** på siden **Årsavslutning**. Du kan velge koblingen **Vis resultater** i **Resultater**-kolonnen for å åpne resultatene for årsavslutningen. **Status**-kolonnen viser den gjeldende tilstanden til årsavslutningen. De nye kolonnene gir derfor innsyn i fremdriften til årsavslutningen.

[![Kolonnene Resultater og Status på siden Årsavslutning.](./media/Optimize-year-end-close-Image3.png)](./media/Optimize-year-end-close-Image3.png)

Når funksjonen **Optimaliser årsavslutningen** er aktivert, blir i tillegg hurtigfanen **Finansdimensjoner for balanse** tilgjengelig på siden **Årsavslutningsmal**. Du kan bruke denne hurtigfanen til å angi finansdimensjoner for balanse i detalj når du avslutter et år. Denne funksjonen er parallell med funksjonen som allerede er tilgjengelig for resultatkontoer.

[![Hurtigfanen Finansdimensjoner for balanse.](./media/Optimize-year-end-close-Image4.png)](./media/Optimize-year-end-close-Image4.png)

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflyt

Hvis du vil bruke funksjonen **Optimaliser årsavslutningen** og kjøre årsavslutningen på en mikrotjeneste, må du installere **tilleggsprogrammet for tjenesten Optimaliser årsavslutningen** fra Lifecycle Services og deretter aktivere funksjonen **Optimaliser årsavslutningen** i Funksjonsbehandling.

Illustrasjonen nedenfor viser at behandlingen av årsavslutningen bekrefter at tilleggsprogrammet er installert og funksjonen aktivert. Hvis begge forutsetningene oppfylles, kjøres årsavslutningen på mikrotjenesten.

[![Dataflytdiagram.](./media/Optimize-year-end-close-Image5.png)](./media/Optimize-year-end-close-Image5.png)

## <a name="high-level-flow-for-year-end-close-processing"></a>Høynivåflyt for behandling av årsavslutning

1. Årsavslutningen begynner i Finance, gå til **Økonomimodul \> Lukket periode \> Årsavslutning**. Prosessen oppretter satsvise jobber og oppgaver for avslutning for de juridiske enhetene som avsluttes.
2. Årsavslutningen fastsetter om årsavslutningen skal kjøres på mikrotjenesten eller på den gjeldende avslutningslogikken.

    - Hvis **tilleggsprogrammet for tjenesten Optimaliser årsavslutningen** er installert i Lifecycle Services og funksjonen **Optimaliser årsavslutningen** er aktivert i Funksjonsbehandling, kjører årsavslutningen på mikrotjenesten.

        1. Funksjonaliteten Optimaliser årsavslutningen oppretter en tjenestejobb for årsavslutning for hver juridiske enhet som avsluttes, og kjører deretter årsavslutningslogikken. Mikrotjenesten utfører årsavslutningen.
        2. Finance lytter til årsavslutningen på mikrotjenesten for å finne ut når mikrotjenesten er ferdig. Årsavslutningsresultatene blir deretter oppdatert på siden **Årsavslutning** i Finance.

    - Ellers kjøres årsavslutningen på den gjeldende avslutningslogikken.
