---
title: Vanlige kilder til produksjonsavvik
description: Denne artikkelen beskriver forskjellige vanlige kilder til hver type produksjonsavvik.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50f8cd7904e1d32175edd321fbd6533e985fb324
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553536"
---
# <a name="common-sources-of-production-variances"></a>Vanlige kilder til produksjonsavvik

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver forskjellige vanlige kilder til hver type produksjonsavvik. 

Her er noen vanlige kilder til et **partistørrelsesavvik**:

-   Det korrekte antallet for en produksjonsordre avviker fra det beregnede antallet som brukes i standard kostnadsberegning. Antallet gir grunnlaget for nedbetaling av konstante kostnader.
-   Verdien av konstante kostnader på produksjonsordren avviker fra de konstante kostnadene som er brukt i standard kostnadsberegning. De konstante kostnadene på produksjonsordren kan være forskjellige av flere årsaker. De konstante kostnadene kan for eksempel gjenspeile følgende faktorer:
    -   Manuelle endringer i produksjonsstykklisten stykklisten eller ruten
    -   Valget av en annen stykklisteversjon eller ruteversjon når du oppretter produksjonsordren
    -   Planlagte tekniske endringer med den stykklisteversjonen eller ruteversjonen som er tilordnet varen

Her er noen vanlige kilder til et avvik i **produksjonspris**:

-   Kostnadskategorien (og kostkategoripris) for det rapporterte forbruket av en ruteoperasjon avviker fra den kostnadskategorien som er brukt i standard kostnadsberegning.
-   Den aktive kostnaden for kostkategoriprisen avviker fra den kostkategoriprisen som er brukt i standard kostnadsberegning.

Her er noen vanlige kilder til et avvik i **produksjonsantall**:

-   Du overproduserer eller underproduserer komponentmateriale.
-   Du overrapporterer ruteoperasjon eller underrapporterer en ruteoperasjon.
-   Du overmottar over eller undermottar det korrekte antallet for den overordnede varen, relativt til ordreantallet. Du kan imidlertid utstede komponenter og rapportere operasjoner fullstendig, basert på ordreantallet for produksjonsordren.

Her er noen vanlige kilder til et avvik i **produksjonserstatning**:

-   Du utsteder et komponentmateriale som ikke er i produksjonsstykklisten.
-   Du legger manuelt til en komponent til produksjonsstykklisten og rapporterer denne komponenten som forbruk.
-   Du rapporterer en vare som forbrukt, men uten å legge den til manuelt i produksjonsstykklisten.
-   Du legger manuelt til en operasjon til produksjonsruten og rapporterer operasjonen som forbrukt.
-   Når du oppretter produksjonsordren, velger du en stykklisteversjon som avviker fra stykklisteversjonen den som ble brukt i standard kostnadsberegning.
-   Når du oppretter produksjonsordren, velger du ruteversjonen som avviker fra ruteversjonen som ble brukt i standard kostnadsberegning.




