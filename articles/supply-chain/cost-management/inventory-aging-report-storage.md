---
title: Lagring av rapport for aldersfordeling for lager
description: Dette emnet beskriver funksjonaliteten som lar deg kjøre en rapport for aldersfordeling for lager, og gjør utdataene tilgjengelige som et skjema og et diagram.
author: AndersGirke
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 17ca0a105521f3216dfefcc170d60c1eb7137bf6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809764"
---
# <a name="inventory-aging-report-storage"></a>Lagring av rapport for aldersfordeling for lager

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du kjøre en rapport for **lagring av rapport for aldersfordeling for lager** og få utdataene tilgjengelige som et skjema og et diagram. I skjemaet justeres kolonner og samlesaldoer dynamisk, avhengig av oppsettet som er konfigurert. Diagrammet gir en visuell oversikt som støtter filtrering, og lar deg drille ned til detaljer. I tillegg kan du bruke en dataenhet som heter **Rapport for aldersfordeling for lager** til å eksportere resultatene av en rapport for **lagring av rapport for aldersfordeling for lager** til et format som f.eks. Microsoft Excel-fil eller en PDF-fil.

Denne metoden for å kjøre en rapport for **lagring av rapport for aldersfordeling for lager** er nyttig i tilfeller der utdataene inneholder mange linjer. Utdataene vil for eksempel inneholde mange linjer hvis du har 50 000 varer og 300 butikker som opprettes som lagre, og du ber om aldersfordeling for lager etter vare, område og lager.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Aktiver funksjonen Rapport for oppbevaring av lagerverdi

Før du kan bruke denne funksjonen, må du aktivere den i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig. Her vises funksjonen som:

- **Modul** - Kostnadsstyring
- **Funksjonsnavn** - Lagring av rapport for aldersfordeling for lager

## <a name="run-an-inventory-aging-report-storage"></a>Kjøre en lagring av rapport for aldersfordeling for lager

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagring av rapport for aldersfordeling for lager**.
1. Velg **Ny**.
1. I feltet **Prosess-ID – navn** angir du et unikt navn på rapporten.
1. Velg **Identifikasjon – ID**-rapporten, og filtrer den slik du ønsker.

    Rapportutførelse utføres alltid i en satsvis jobb.

1. Når den satsvise jobben er fullført, vises utdataene på siden **Lagring av rapport for aldersfordeling for lager**.
1. Hvis du vil vise utdata som et skjema som har et tradisjonelt rutenettoppsett, velger du **Vis detaljer**. Hvis du vil vise utdata som et oppsamlet diagram, velger du **Vis diagram**.

    > [!NOTE]
    > Skjemaet inkluderer ikke delsummer som er definert i rapportoppsettet.

Ved hjelp av dateenheten **Rapport for aldersfordeling for lager** kan du eksportere utdataene for en **lagring av rapport for aldersfordeling for lager**-rapport ved å bruke et filter for **Prosess-ID – navn**-feltet til et hvilket som helst format som databehandling støtter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]