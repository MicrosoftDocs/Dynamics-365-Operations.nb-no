---
title: Lagerapphendelser
description: Denne artikkelen beskriver behandling av lagerapphendelser som brukes til å behandle hendelsesmeldinger for lagerappen som en del av en satsvis jobb.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2dc24fed1ec71432d9e2a3e1cb5b366267c2938b
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218750"
---
# <a name="warehouse-app-event-processing"></a>Behandling av lagerapphendelse

[!include [banner](../includes/banner.md)]

Satsvise jobber som kjører i Supply Chain Management, kan bruke data fra en kø for behandling av hendelser som utstedes av mobilappen Lagerstyring, for å reagere etter behov på signaliserte hendelser. Denne funksjonen legger til relevante hendelser i køen som svar på bestemte typer handlinger utført av arbeidere ved hjelp av appen. Et eksempel er at når du bruker funksjonen *Opprette og behandle overføringsordre fra lagerappen*, blir overføringsordrehodet og -linjene opprettet og oppdatert i serverdelen når systemet kjører den satsvise jobben **Behandle lagerapphendelser**.

## <a name="turn-the-process-warehouse-app-events-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Behandle lagerapphendelser

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Denne funksjonen er obligatorisk fra og med Supply Chain Management versjon 10.0.29. Derfor er den aktivert som standard, og kan ikke deaktiveres på nytt. Hvis du kjører en versjon som er eldre enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Behandle lagerapphendelser* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Konfigurere en satsvis jobb for å behandle lagerapphendelser

### <a name="process-warehouse-app-events"></a>Behandle lagerapphendelser

Konfigurer en planlagt satsvis jobb for å behandle lagerapphendelsene for oppretting og linjeoppdateringer for overføringsordrer.

1. Gå til **Lagerstyring \> Periodiske oppgaver \> Behandle lagerapphendelser**.
1. Dialogboksen Behandle lagerapphendelser åpnes. Vis hurtigfanen **Kjør i bakgrunnen**, og sett **Satsvis behandling** til **Ja**.
1. På hurtigfanen **Kjør i bakgrunnen** velger du **Regelmessighet**.
1. Dialogboksen **Definer regelmessighet** åpnes. Angi kjøretidsplanen etter behov for firmaet.
1. Velg **OK** for å gå tilbake til dialogboksen **Behandle lagerapphendelser**.
1. Velg **OK** i dialogboksen **Behandle lagerapphendelser** for å legge til den satsvise jobben i den satsvise køen.

## <a name="query-warehouse-app-events"></a>Spørre etter lagerapphendelser

Du kan vise hendelseskøen og hendelsesmeldingene som genereres av mobilappen Lagerstyring, ved å gå til **Lagerstyring \> Forespørsler og rapporter \> Logger for mobilenheter \> Lagerapphendelser**.

## <a name="the-standard-event-queue-process"></a>Standardprosess for hendelseskø

Køen for lagerapphendelser vil vanligvis bli brukt med følgende beskrevet flyt:

1. En hendelse blir lagt til i køen med en hendelsesmelding. Den nye meldingen har i utgangspunktet hendelsestilstanden **Venter**, noe som betyr at den satsvise jobben **Behandle lagerapphendelser** ikke vil hente og behandle denne meldingen.
1. Så snart meldingstilstanden er oppdatert til **I kø**, vil den satsvise jobben **Behandle lagerapphendelser** hente og behandle hendelsen.
1. Den satsvise jobben oppdaterer hendelsestilstandene til **Fullført** eller **Mislykket**, avhengig av om den forespurte prosessen var mulig.
1. Når alle relaterte hendelsesmeldinger er **Fullført**, slettes hendelsen fra køen.

 Hvis du vil ha et detaljert eksempel, kan du se [Opprette overføringsordre fra lagerapprosess](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Håndtere hendelsesfeil

Som en del av behandling av lagerhendelser, kan det hende at den ønskede meldingsaktiviteten ikke mottar prosesser fra den satsvise jobben. I slike tilfeller blir hendelsesmeldingen endret til **Mislykket**. Du kan bruke informasjonen til **loggen for den satsvise jobben** til å finne ut hvorfor og gjøre nødvendige tiltak for å løse eventuelle problemer.

Hvis du vil ha et detaljert eksempel, kan du se [Opprette overføringsordre fra lagerapp](create-transfer-order-from-warehouse-app.md).

Slik tilbakestiller du en mislykket hendelsesmelding for en lagerapp:

1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Loger for mobilenheter \> Lagerapphendelser**.
1. I hurtigfanen **Hendelsesmeldinger for lagrapp** finner du og velger en relevant hendelse som vises **Mislykket** i kolonnen **Hendelsestilstand**.
1. Velg **Tilbakestill** fra verktøylinjen **Hendelsesmeldinger for lagerapp**.
1. Fortsett å arbeide til alle relevante meldinger er tilbakestilt.

Du kan også fjerne en **Mislykket** hendelsesmelding ved hjelp av **Slett**-alternativet på verktøylinjen **Hendelsesmeldinger for lagerapp**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
