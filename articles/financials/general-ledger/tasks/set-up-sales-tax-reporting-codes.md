---
title: Definer mva-rapporteringskoder
description: Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "335675"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Definer mva-rapporteringskoder

[!include [task guide banner](../../includes/task-guide-banner.md)]

Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport. De brukes på landspesifikke rapportoppsett og Mva-betaling etter rapporteringskode for å skrive ut mva-beløp for en utligningsperiode som er summert per rapporteringskode. Når du har opprettet mva-rapporteringskodene, kan du referere til dem i hurtigkategoriene Rapportoppsett på siden Mva-kode. 

Denne registreringen bruker demonstrasjonsfirmaet DEMF.



1. Gå til Avgift > Oppsett > Merverdiavgift > Mva-rapporteringskoder.
2. Klikk Ny.
3. Velg rapportoppsettet som rapporteringskoden tilhører.
    * Dette oppsettet brukes til å filtrere de tilgjengelige rapporteringskodene for en mva-kode. Hver mva-kode tilhører en utligningsperiode som tilhører en skattemyndighet som bruker et rapportoppsett.  
4. Angi et nummer som refererer til et felt i en mva-rapport.
5. I Rapporttekst-feltet angir du en beskrivelse som skal vises på rapporter.
6. I feltet Kort beskrivelse skriver du inn en kort beskrivelse for intern bruk.
7. Klikk Lagre.

