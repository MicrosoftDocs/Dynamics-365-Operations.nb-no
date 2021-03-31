---
title: Definer mva-rapporteringskoder
description: Mva-rapporteringskodene refererer til et feltnummer som er oppført på en mva-rapport.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222149"
---
# <a name="set-up-sales-tax-reporting-codes"></a>Definer mva-rapporteringskoder

[!include [banner](../../includes/banner.md)]

Mva-rapporteringskodene refererer til et feltnummer som er oppført på en mva-rapport. De brukes på landspesifikke rapportoppsett. De brukes også på Mva-betaling etter kode-rapporten. Denne rapporten viser mva-beløp for en utligningsperiode oppsummert for hver rapporteringskode. Når du har opprettet mva-rapporteringskodene, kan du referere til kodene i hurtigkategoriene Rapportoppsett, som du får tilgang til fra siden **Mva-kode**. 

Denne registreringen bruker demonstrasjonsfirmaet DEMF.

1. I **navigasjonsruten** går du til **Avgift > Oppsett > Merverdiavgift > Mva-rapporteringskoder**.
2. Klikk på **Ny**.
3. Velg rapportoppsettet som rapporteringskoden tilhører. Dette oppsettet brukes til å filtrere de tilgjengelige rapporteringskodene for en mva-kode. Hver mva-kode tilhører en utligningsperiode som tilhører en skattemyndighet som bruker et rapportoppsett.  
4. Angi et tall i feltet **Rapporteringskode**.
5. I **Rapporttekst**-feltet angir du en beskrivelse som skal vises på rapporter.
6. I feltet **Kort beskrivelse** skriver du inn en kort beskrivelse for intern bruk.
7. Klikk **Lagre**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]