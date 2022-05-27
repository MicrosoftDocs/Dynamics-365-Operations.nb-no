---
title: Varebehov for serviceordre
description: Dette emnet beskriver hvordan du oppretter varebehov for serviceordrer.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6cd7e89e28b8fc00a8c09f51703995cd79ade5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674232"
---
# <a name="service-order-item-requirements"></a>Varebehov for serviceordre

[!include [banner](../includes/banner.md)]

Du kan opprette en serviceordre for å spore og behandle tjenestene du tilbyr kundene dine. Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den. Et varebehov kan brukes umiddelbart fra lageret, eller det kan starte en produksjonsordre for varen.

Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.

Varebehov for serviceordrer behandles via et prosjekt. Hvis du vil opprette et varebehov opprettes på en serviceordre, må serviceordren tilknyttes et prosjekt.

Så snart et varebehov er opprettet for en serviceordre, kan det vises fra **Prosjekt** i den enkelte serviceordren eller i **Salgsordre**-skjemaet.

## <a name="view-an-item-requirement-from-a-service-order"></a>Vise et varebehov fra en serviceordre

1. Gå til **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.
1. Klikk på **Fordeling**, og klikk deretter **Varebehov** for å åpne **Varebehov**-skjemaet.
1. Klikk på fanen **Prosjekt**, og merk deretter av for **Serviceordre** for å vise serviceordrene for varebehovet.

## <a name="delete-service-orders-with-item-requirements"></a>Slette serviceordrer med varebehov

Hvis et varebehov opprettes på en serviceordre, kan du ikke slette serviceordren. Du må slette varebehovet før du kan slette serviceordren.

1. Gå til **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.
1. Klikk på **Fordeling**, og klikk deretter **Varebehov** for å åpne **Varebehov**-skjemaet. Dette skjemaet viser varebehovene som er opprettet på serviceordren.
1. Velg varebehovslinjen som skal slettes, og klikk deretter **Slett**.

– eller –

1. Gå til **Prosjektstyring og regnskap** \> **Felles** \> **Prosjekter** \> **Alle prosjekter**.
1. Åpne prosjektet som har serviceordren der det er opprettet et varebehov.
1. I **Prosjekter**-skjemaet, i den høyre ruten, klikk **Varebehov**. **Varebehov**-skjemaet åpnes og viser varebehovene som er tilknyttet det valgte prosjektet.
1. Velg varebehovslinjen som skal slettes, og klikk deretter **Slett**.

## <a name="see-also"></a>Se også

[Varebehov (skjema)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]