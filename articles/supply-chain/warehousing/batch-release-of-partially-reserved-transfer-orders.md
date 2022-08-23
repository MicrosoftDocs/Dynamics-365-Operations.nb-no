---
title: Satsvis frigivelse av delvis reserverte overføringsordrer
description: Denne artikkelen beskriver hvordan du konfigurerer og bruker batchfrigjøring av delvis reserverte overføringsordrer fra en mobilenhet.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218690"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Satsvis frigivelse av delvis reserverte overføringsordrer

[!include [banner](../includes/banner.md)]

Funksjonaliteten for batchfrigivelse av delvis reserverte overføringsordrer lar deg delvis frigi overføringsordrer til et lager ved å bruke en batchjobb.
Fordi du har muligheten til å frigjøre en delmengde, behøver du ikke vente på at hele bestillingsmengden er tilgjengelig på lageret før du frigir en ordre.

Å frigi bestillinger til et lager er en Warehouse Management-prosess (WMS). Denne prosessen omfatter aktiviteter som plukking, pakking og frakt, som en lagerbehandler kan utføre ved bruk av en mobil enhet.

## <a name="where-it-applies"></a>Der det er aktuelt

For denne funksjonaliteten blir overføringsordrer frigitt til et lager ved å bruke en batchjobb. Denne funksjonaliteten er nyttig når du ikke har nok varer på lageret, men du fortsatt vil overføre varer fra ett lager til et annet.

## <a name="how-it-is-set-up"></a>Hvordan det er satt opp

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Angi oppfyllelseskriterier for overføringsordrer og salgsordrer

Før en bestilling kan frigis ut til et lager i et parti, må oppfyllelseskriteriene være oppfylt. Disse oppfyllelseskriteriene bestemmes av oppfyllingsregelen.

Oppfyllingsregler for overføringsordrer og salgsordrer er spesifisert på bedriftsnivå. Avhengig av oppsettet av oppfyllelsesreglene, vil frigivelsen av bestillinger i en batch aksepteres eller avvises. Ordrene blir deretter behandlet tilsvarende.

- For å opprette oppfyllelsesregler for overføringsordrer og salgsordrer går du til **Lagerstyring \> Oppsett \> Frigi til lager \> Oppfyllelsesregler**, og opprett deretter oppfyllelsesregler ved å skrive inn et navn og en beskrivelse.
- For å angi en oppfyllelseshastighet, en verditype og meldingen som vises hvis oppfyllelsesreglene brytes, går du til **Lagerstyring \> Oppsett \> Frigi til lager \> Oppfyllelsesregler**, og setter deretter feltene **Oppfyllelsessats**, **Verditype** og **Melding ved brudd på oppfyllelse**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Angi oppfyllelsessregler for overføringsordrer og salgsordrer

- For å angi oppfyllelsesregler for overføringsordrer går du til **Lagerstyring \> Oppsett \> Parametere for beholdning og lagerstyring**, og velger deretter en oppfyllelsesregel for overføringsordre på fanen **Overføringsordrer** i delen **Lagerstyring**.
- For å angi oppfyllelsesregler for salgsordrer går du til **Kundefordringer \> Oppsett \> Parametere for kundefordringer**, og velger deretter en oppfyllelsesregel for salgsordre på fanen **Lagerstyring**.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Tillat frigivelse i en batch og angi mengden som skal frigis i en batch

En batchjobb brukes til å frigi ordrer til et lager i en batch. Parametrene som skiller ordrene som skal kjøres i en batchjobb, settes på selve batchjobben.

Parameteren **Mengde** angir om hele mengden eller den fysisk reserverte mengden skal frigis i batchen. Parameteren **Tillate frigivelse av delvis frigitte ordrer** bestemmer om bestillinger i batchen skal aksepteres eller avvises dersom de delvis ble frigitt tidligere.

- For å angi parametere for overføringsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer** går du til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse for overføringsordrer**
- For å angi parametere for salgsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer** går du til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse for salgsordrer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
