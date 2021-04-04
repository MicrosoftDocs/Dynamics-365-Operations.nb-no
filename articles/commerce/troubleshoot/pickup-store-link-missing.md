---
title: Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene
description: Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585462"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Alternativet Hent vises ikke på handlekurv- eller produktdetaljsidene

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsretningsinformasjon som kan hjelpe når alternativet for henting i butikken ikke vises på handlekurvsiden eller produktdetaljersidene.

## <a name="description"></a>beskrivelse

Knappen **Hent** vises ikke på handlekurv- eller produktdetaljsidene.

Illustrasjonen nedenfor viser et eksempel på en side som inneholder knappen **Hent**.

![Knappen Hent](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Oppløsning

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Aktivere BOPIS-tillegget i Commerce-områdebyggeren

Følg denne fremgangsmåten for å aktivere tillegget Kjøpe på Internett og hente i butikk (BOPIS) i Commerce-områdebyggeren:

1. Velg området ditt.
1. Velg **Områdeinnstillinger** og deretter **Utvidelser**.
1. Kontroller at det ikke er merket av for alternativet **Deaktiver BOPIS**.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Konfigurere leveringsmåter i Commerce Headquarters

Følg denne fremgangsmåten for å konfigurere leveringsmåter i Commerce Headquarters.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Leveringsmåter**.
1. Kontroller at leveringsmåten **Kundehenting** er opprettet, og at det er tilordnet produkter og adresser til den.
1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.
1. Velg **Kundeordrer** i navigasjonsruten til venstre.
1. Kontroller at **Henteleveringsmåte** er riktig konfigurert.

### <a name="configure-customer-orders-payments"></a>Konfigurere betalinger for kundeordrer

Følg denne fremgangsmåten for å konfigurere betalinger for kundeordrer i Commerce Headquarters.

1. Gå til **Detaljhandel og handel \> Hovedkvarteroppsett \> Parametere**.
1. Velg **Kundeordrer** i navigasjonsruten til venstre.
1. Kontroller at feltene **Betalingsbetingelser** og **Betalingsmåte** er riktig angitt i hurtigfanen **Betalinger**.

## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere BOPIS](../cpe-bopis.md)

[Aktiver flere henteleveringsmåter for kundeordrer](../multiple-pickup-modes.md)

[Commerce-ordrebetalinger for omnikanal](../dev-itpro/commerce-payments.md)

[Butikkvelgermodul](../store-selector.md)