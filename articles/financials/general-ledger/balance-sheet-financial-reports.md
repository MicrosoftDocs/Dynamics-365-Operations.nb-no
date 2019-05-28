---
title: Finansrapporter for balanse
description: Denne artikkelen beskriver standardrapportene for balansen. Den beskriver også byggeblokker som er knyttet til disse rapportene.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff778af1bb3af3a10132ab3193ad1cd5daa24e1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567335"
---
# <a name="balance-sheet-financial-reports"></a>Finansrapporter for balanse

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver standardrapportene for balansen. Den beskriver også byggeblokker som er knyttet til disse rapportene. 

<a name="default-balance-sheet-reports"></a>Standardrapporter for balanse
-----------------------------

Det finnes to standardrapporter for balanse. På en av rapportene er delene er stablet. På den andre rapporten er delene ved siden av hverandre.

| Standardrapport                       | Resultat                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Balanse – Standard              | Gir en oversikt over organisasjonens finansiell stilling for året.                                                                 |
| Side ved side Balanse – Standard | Gir en oversikt over organisasjonens finansiell stilling for året. Aktiva og gjeld og egenkapital for aksjeeiere er ved siden av hverandre. |

## <a name="building-blocks"></a>Byggeblokker
Finansrapportene for balansen bruker byggeblokkene nedenfor.

| Standardrapport                       | Raddefinisjon                       | Kolonnedefinisjon             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balanse – Standard              | Balanse – Standard              | Hittil i år og avvik – Standard    |
| Side ved side Balanse – Standard | Side ved side Balanse – Standard | Hittil i år-kolonne – Standard |

### <a name="row-definition"></a>Raddefinisjon

Raddefinisjonene for begge balanserapportene inneholder inndelinger for hver del av en tradisjonell balanse. Side-ved-side-rapporten inneholder et spalteskift, slik at gjeld og eiernes egenkapital vises ved siden av anleggsmidler. Dimensjonen for hovedkontokategorien brukes til å opprette begge raddefinisjoner. Derfor kan alle generere rapportene uten å gjøre endringer.

### <a name="column-definition"></a>Kolonnedefinisjon

Kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.

-   **Hittil i år og avvik – Standard kolonnetyper:**
    -   **DESC** – Beskrivelsen fra raddefinisjonen.
    -   **FD** – Økonomiske data hittil i år for inneværende år
    -   **FD** – Økonomiske data hittil i år for forrige år
    -   **CALC** – Avviket fra å trekke forrige år fra i år

<!-- -->

-   **Hittil i år-kolonne – Standard:**
    -   **DESC** – Beskrivelsen fra raddefinisjonen.
    -   **FD** – Økonomiske data hittil i år for inneværende år



<a name="additional-resources"></a>Tilleggsressurser
--------

[Finansrapportering](financial-reporting-getting-started.md)

[Vise finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](http://blogs.msdn.com/b/dynamics_financial_reporting/)



