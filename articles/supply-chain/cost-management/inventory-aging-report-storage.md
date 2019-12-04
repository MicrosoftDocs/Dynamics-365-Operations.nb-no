---
title: Rapport for aldersfordeling for lager
description: Dette emnet beskriver funksjonaliteten som lar deg kjøre en rapport for aldersfordeling for lager, og gjør utdataene tilgjengelige som et skjema og et diagram.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810257"
---
# <a name="inventory-aging-report"></a>Rapport for aldersfordeling for lager


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

I Microsoft Dynamics 365 Supply Chain Management kan du kjøre en rapport for **aldersfordeling for lager** og få utdataene tilgjengelige som et skjema og et diagram. I skjemaet justeres kolonner og samlesaldoer dynamisk, avhengig av oppsettet som er konfigurert. Diagrammet gir en visuell oversikt som støtter filtrering, og lar deg drille ned til detaljer. I tillegg kan du bruke en dataenhet som heter **Rapport for aldersfordeling for lager** til å eksportere resultatene av en rapport for **aldersfordeling for lager** til et format som f.eks. Microsoft Excel-fil eller en PDF-fil.

Denne metoden for å kjøre en rapport for **aldersfordeling for lager** er nyttig i tilfeller der utdataene inneholder mange linjer. Utdataene vil for eksempel inneholde mange linjer hvis du har 50 000 varer og 300 butikker som opprettes som lagre, og du ber om aldersfordeling for lager etter vare, område og lager.

## <a name="run-an-inventory-aging-report"></a>Kjøre en rapport for aldersfordeling for lager

1. Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagring av rapport for aldersfordeling for lager**.
1. Velg **Ny**.
1. I feltet **Prosess-ID – navn** angir du et unikt navn på rapporten.
1. Velg **Identifikasjon – ID**-rapporten, og filtrer den slik du ønsker.

    Rapportutførelse utføres alltid i en satsvis jobb.

1. Når den satsvise jobben er fullført, vises utdataene på siden **Lagring av rapport for aldersfordeling for lager**.
1. Hvis du vil vise utdata som et skjema som har et tradisjonelt rutenettoppsett, velger du **Vis detaljer**. Hvis du vil vise utdata som et oppsamlet diagram, velger du **Vis diagram**.

    > [!NOTE]
    > Skjemaet inkluderer ikke delsummer som er definert i rapportoppsettet.

Ved hjelp av dateenheten **Rapport for aldersfordeling for lager** kan du eksportere utdataene for en **Aldersfordeling for lager**-rapport ved å bruke et filter for **Prosess-ID – navn**-feltet til et hvilket som helst format som databehandling støtter.
