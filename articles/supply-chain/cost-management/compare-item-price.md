---
title: Rapport for sammenligning av lagervarepriser
description: Lær hvordan du genererer rapport for sammenligning av lagervarepriser og deretter bla gjennom og/eller eksportere resultatet.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 73e43a685f390fd718028de6add0370dfcd6cf3b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434608"
---
# <a name="compare-item-prices-storage-report"></a>Rapport for sammenligning av lagervarepriser

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du kjører en rapport for **sammenligning av lagervarepriser** og gjør utdataene tilgjengelig digitalt, enten som en interaktiv side i Dynamics 365 Supply Chain Management eller som et eksportert dokument i et av flere formater.

Når du viser rapporten i nettleseren, justeres kolonner og aggregatsaldoer dynamisk, avhengig av det konfigurerte oppsettet. Du kan sortere resultatene, filtrere dem, drille ned til dataene og mye mer.

Rapportresultater lagres i dataenheten **Sammenlign varepriser**, slik at du kan filtrere og eksportere resultatene til et format som for eksempel CSV eller Microsoft Excel.

Rapporten for **sammenligning av lagervarepriser** er nyttig i tilfeller der utdataene inneholder mange linjer. Utdataene vil for eksempel inneholde mange linjer hvis du har mer enn 40 000 varer som inneholder en uavsluttet varepris i kostversjonen.

## <a name="enable-compare-item-prices-storage"></a>Aktivere sammenligning av lagervarepriser

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. Her vises funksjonen som:

- **Modul** - Kostnadsstyring
- **Funksjonsnavn** – Sammenligning av lagervarepriser

## <a name="generate-a-compare-item-prices-storage-report"></a>Generer en rapport for sammenligning av lagervarepriser

Følg denne fremgangsmåten for å generere og lagre en rapport for **sammenligning av lagervarepriser**:

1. Gå til **Kostnadsstyring > Forespørsler og rapporter > Forhåndsbestemte kostnadsrapporter > Sammenligning av lagervarepriser**.

1. Velg **Ny** for å åpne ruten **Sammenlign varepriser**. Angi følgende alternativer for å definere hvilke priser som skal sammenlignes i rapporten:

    - På hurtigfanen **Parametere** gir du rapporten et **navn** og bruker feltene i delene **Ventende priser som skal sammenlignes** og **Priser som brukes for sammenligning** til å definere hvilke priser og datoer som skal sammenlignes.
    - I hurtigfanen **Poster som skal inkluderes** definerer du filtre og betingelser for å definere hvilke data som skal tas med i rapporten.
    - På hurtigfanen **Kjør i bakgrunnen** definerer du hvordan, når og frekvensen for når du ønsker å generere rapporten.
    > [!NOTE]
    > Denne rapporten blir alltid utført som en del av en satsvis jobb.

1. Velg **OK** for å bruke innstillingene og lukke ruten.

1. Når den satsvise jobben er fullført, vil den vises på siden **Sammenligning av lagervarepriser**. Det kan hende at du må oppdatere siden for å se rapporten.

## <a name="explore-the-compare-item-prices-storage-report"></a>Se nærmere på rapporten for sammenligning av lagervarepriser

Når du har generert en rapport, kan du vise og utforske den når som helst på følgende måte:

1. Gå til **Kostnadsstyring > Forespørsler og rapporter > Forhåndsbestemte kostnadsrapporter > Sammenligning av lagervarepriser**.

1. Velg en rapport fra listen.

1. Gjør ett av følgende:

    - Velg **Oversikt** for å få en oversikt over rapportresultatene.
    - Velg **Vis detaljer** for å få en mer detaljert visning av rapporten

1. Når den valgte visningen åpnes, kan du gjøre følgende:

    - Velg nesten hvilken som helst kolonneoverskrift for å sortere eller filtrere tabellen etter verdier i denne kolonnen, på samme måte som med de fleste standardskjemaene i Supply Chain Management. Merk at du ikke kan sortere eller filtrere kolonnen **Nettoprisendring i prosent** fordi det er et beregnet felt.
    - Velg **Dimensjonsvisningvisning** for å åpne en rute der du kan velge hvilken dimensjonskolonne som skal tas med i skjemaet. Sett **Lagre oppsett** til **Ja** hvis du vil lagre disse innstillingene slik at de blir bevart neste gang du åpner rapporten. Velg **OK** for å bruke innstillingene og lukke.
    - Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis detaljer** for å se mer informasjon om den valgte varen. Du kan drille ned til dataene herfra.
    - Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis sammenligningsdiagram** for å se en interaktiv grafisk fremstilling av resultatene slik de er relatert til det valgte elementet. Du kan utforske disse resultatene ved å velge ulike grafiske elementer i diagrammet og diagramforklaringen.
    - Velg en hvilken som helst rad i skjemaet, og velg deretter **Vis beregningsdetaljer** for å se mer informasjon om beregninger relatert til den valgte varen. Du kan drille ned til dataene herfra.

## <a name="export-the-compare-item-prices-storage-report"></a>Eksportere rapporten for sammenligning av lagervarepriser

Hver rapport du genererer, lagres i dataenheten **Sammenlign varepriser**. Du kan bruke standardfunksjonene i Supply Chain Management til å eksportere data fra denne enheten til alle støttede dataformater, inkludert CSV eller Microsoft Excel.

Nedenfor vises et eksempel på hvordan du eksporterer en rapport for **sammenligning av lagervarepriser**:

1. Gå til **Systemadministrasjon > Arbeidsområder > Databehandling**.

1. Velg **Eksporter**-knappen i delen **Databehandling**.

1. Siden **Eksporers** åpnes, som du vil bruke til å konfigurere eksportjobben. Start ved å gi jobben et **gruppenavn**.

1. I delen **Valgte enheter** velger du **Legg til enhet** for å åpne en dialogboks der du kan angi følgende alternativer:

    - **Enhetsnavn** – Velg **Sammenlign varepriser**.
    - **Måldataformat** – Velg formatet du vil eksportere til.

1. Velg **Legg til** for å legge til en ny rad, og velg deretter **Lukk** for å lukke dialogboksen.

1. Vanligvis eksporterer du én rapport om gangen. Hvis du vil gjøre dette, definerer du et **filter** for raden du nettopp la til, i **Forespørsel**-ruten. På denne måten kan du definere hvilke rapporter fra enheten **Sammenlign varepriser** som du vil inkludere i eksporten. Angi følgende filteralternativer for å eksportere en enkelt rapport:

    - I kategorien **Område** velger du **Legg til** for å legge til en ny rad.
    - Sett **Tabell** til **Sammenlign varepriser**.
    - Sett **Avledet tabell** til **Sammenlign varepriser**.
    - Sett **Felt** til feltet som du vil filtrere etter. Vanligvis vil du bruke **Kjørenavn** eller **Kjøretid**.
    - Angi **Kriterier** til verdien fra det valgte feltet som du vil søke etter (enten navnet på rapporten eller klokkeslettet da rapporten ble generert).
    - Hvis det er nødvendig, legger du til flere rader i **Område**-tabellen til du har unikt angitt hvilken rapport du vil søke etter.

1. Velg **OK** for å lagre innstillingene og lukke.

1. Velg **Lagre** for å lagre eksportoppsettet.

1. Åpne kategorien **Eksportalternativer**, og velg **Eksporter nå** for å generere eksportfilen.

1. Siden **Kjøringssammendrag** åpnes, der du kan se statusen for eksportjobben og en liste over enheter som ble eksportert. Velg enheten **Sammenlign varepriser** som er oppført i området **Behandlingsstatus for enhet**, og velg deretter **Last ned fil** for å laste ned dataene som er eksportert fra denne enheten.

Hvis du vil ha mer informasjon om hvordan du bruker databehandling til å eksportere data, se [Oversikt over dataimport- og -eksportjobber](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
