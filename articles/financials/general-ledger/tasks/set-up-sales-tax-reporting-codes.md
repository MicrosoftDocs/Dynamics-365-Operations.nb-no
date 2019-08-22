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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 830a3465944b32cc17feee60e3cbc5ad0a4dc9d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834781"
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

