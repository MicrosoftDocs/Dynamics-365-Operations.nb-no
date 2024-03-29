---
title: Finansrapporter for balanse
description: Denne artikkelen beskriver standardrapportene for balansen. Den beskriver også byggeblokker som er knyttet til disse rapportene.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643830"
---
# <a name="balance-sheet-financial-reports"></a>Finansrapporter for balanse

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver standardrapportene for balansen. Den beskriver også byggeblokker som er knyttet til disse rapportene. 

## <a name="default-balance-sheet-reports"></a>Standardrapporter for balanse

Det finnes to standardrapporter for balanse. På en av rapportene er delene er stablet. På den andre rapporten er delene ved siden av hverandre.

| Standardrapport                       | Resultat                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Balanse – Standard              | Gir en oversikt over organisasjonens finansiell stilling for året.                    |
| Balanse og resultatregnskap side ved side – Standard | Gir en oversikt over organisasjonens finansiell stilling for året side ved side. |

## <a name="building-blocks"></a>Byggeblokker
Finansrapportene for balansen bruker byggeblokkene nedenfor.

| Standardrapport                       | Raddefinisjon                       | Kolonnedefinisjon             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balanse – Standard              | Balanse – Standard              | Hittil i år og avvik – Standard    |
| Balanse og resultatregnskap side ved side – Standard | Balanse og resultatregnskap side ved side – Standard | Hittil i år-kolonne – Standard |

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



## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over finansrapportering](financial-reporting-getting-started.md)

[Vise finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
