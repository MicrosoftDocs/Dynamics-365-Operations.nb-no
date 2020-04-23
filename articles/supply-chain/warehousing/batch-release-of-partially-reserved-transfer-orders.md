---
title: Satsvis frigivelse av delvis reserverte overføringsordrer
description: Dette emnet beskriver hvordan du konfigurerer og bruker batchfrigjøring av delvis reserverte overføringsordrer fra en mobilenhet.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0707731caaf9b4852e3c19be899ad92f5b84e29
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201301"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Satsvis frigivelse av delvis reserverte overføringsordrer

[!include [banner](../includes/banner.md)]

Funksjonaliteten for batchfrigivelse av delvis reserverte overføringsordrer lar deg delvis frigi overføringsordrer til et lager ved å bruke en batchjobb.
Fordi du har muligheten til å frigjøre en delmengde, behøver du ikke vente på at hele bestillingsmengden er tilgjengelig på lageret før du frigir en ordre.

Å frigi bestillinger til et lager er en avansert varehusprosess. Denne prosessen omfatter aktiviteter som plukking, pakking og frakt, som en lagerbehandler kan utføre ved bruk av en mobil enhet.

## <a name="where-it-applies"></a>Der det er aktuelt

For denne funksjonaliteten blir overføringsordrer frigitt til et lager ved å bruke en batchjobb. Denne funksjonaliteten er nyttig når du ikke har nok varer på lageret, men du fortsatt vil overføre varer fra ett lager til et annet.

## <a name="how-it-is-set-up"></a>Hvordan det er satt opp

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Angi oppfyllelseskriterier for overføringsordrer og salgsordrer

Før en bestilling kan frigis ut til et lager i et parti, må oppfyllelseskriteriene være oppfylt. Disse oppfyllelseskriteriene bestemmes av oppfyllingsregelen.

Oppfyllingsregler for overføringsordrer og salgsordrer er spesifisert på bedriftsnivå. Avhengig av oppsettet av oppfyllelsesreglene, vil frigivelsen av bestillinger i en batch aksepteres eller avvises. Ordrene blir deretter behandlet tilsvarende.

-   For å opprette oppfyllelsesregler for overføringsordrer og salgsordrer, klikk på **Lagerstyring** \> **Oppsett** \> **Frigi til lager** \> **Oppfyllelsesregler**, og opprett deretter oppfyllelsesregler ved å skrive inn et navn og en beskrivelse.

-   For å angi en oppfyllelseshastighet, en verditype og meldingen som vises hvis oppfyllelsesreglene brytes, klikker du **Lagerstyring** \> **Oppsett** \> **Frigi til lager** \> **Oppfyllelsesregler**, og setter deretter feltene **Oppfyllelsessats**,**Verditype** og **Melding ved brudd på oppfyllelse**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Angi oppfyllelsessregler for overføringsordrer og salgsordrer

-   For å angi oppfyllelsesregler for overføringsordrer, klikk **Administrering av lagerbeholdning** \> **Oppsett** \> **Parametere for beholdning og lagerstyring** \> **Overføringsordrer** \> **Lagerstyring**, og velger deretter en oppfyllelsesregel for overføringsordre.

-   For å angi oppfyllelsesregler for salgsordrer, klikk **Kundefordringer** \> **Oppsett** \> **Parametere for kundefordringer** \> **Lagerstyring**, og velger deretter en oppfyllelsesregel for salgsordre.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Tillat frigivelse i en batch og angi mengden som skal frigis i en batch

En batchjobb brukes til å frigi ordrer til et lager i en batch. Parametrene som skiller ordrene som skal kjøres i en batchjobb, settes på selve batchjobben.

Parameteren **Mengde** angir om hele mengden eller den fysisk reserverte mengden skal frigis i batchen. Parameteren **Tillate frigivelse av delvis frigitte ordrer** bestemmer om bestillinger i batchen skal aksepteres eller avvises dersom de delvis ble frigitt tidligere.

-   For å angi parametere for overføringsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer**, klikk **Lagerstyring** \> **Frigi til lager** \> **Automatisk frigivelse for overføringsordrer**

-   For å angi parametere for salgsordre, **Mengde** og **Tillate frigivelse av delvis frigitte ordrer**, klikk **Lagerstyring** \> **Frigi til lager** \> **Automatisk frigivelse for salgsordrer**
