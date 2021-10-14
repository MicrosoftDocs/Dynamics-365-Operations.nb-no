---
title: Opprette varebehov for serviceordrer
description: Dette emnet beskriver hvordan du oppretter varebehov for serviceordrer.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75a05147883f1592b3a09e02e238661f6c20cf27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575297"
---
# <a name="create-item-requirements-for-service-orders"></a>Opprette varebehov for serviceordrer

[!include [banner](../includes/banner.md)]

Du kan opprette en serviceordre for å spore og behandle tjenestene du tilbyr kundene dine. Hvis du må reservere bestemte varer for en serviceordre, kan du opprette lagervarebehov for den. Et varebehov kan brukes umiddelbart fra lageret, eller det kan starte en produksjonsordre for varen.

Når du bruker et varebehov i stedet for en varetransaksjon, kan du planlegge levering like før varen faktisk brukes, opprette en bestilling, inkludere varen i rammeverket for forretningsavtalen, og inkludere varebehovet i produksjonsplanlegging.

Varebehov for serviceordrer behandles via et prosjekt. Hvis du vil opprette et varebehov opprettes på en serviceordre, må serviceordren tilordnes et prosjekt. Når du har opprettet et varebehov for en serviceordre, kan du vise varebehovet i **Prosjekter**-skjemaet for det valgte prosjektet.

## <a name="create-an-item-requirement-for-a-service-order"></a>Opprette et varebehov for en serviceordre

1. Gå til **Servicestyring** \> **Felles** \> **Serviceordrer** \> **Serviceordrer**.
1. Velg serviceordren du vil opprette et varebehov for.
1. I **handlingsruten** på fanen **Fordeling** klikker du på **Varebehov**.
1. Skriv inn informasjon for den nødvendige varen i **Varebehov**-skjemaet. Hvis du vil ha mer informasjon om de spesifikke feltene, kan du se [Varebehov (skjema)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Opprette et varebehov for en serviceavtale

1. Gå til **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**.
1. Åpne serviceavtalen som du vil opprette et varebehov for.
1. På hurtigfanen **Linjer** velger du **Legg til** for å opprette en ny linje.
1. I **Transaksjonstype**-feltet velger du **Vare**.
1. I **Vareoppsett**-feltet velger du **Varebehov**.
1. I **Varenummer**-feltet velger du varen som er nødvendig for serviceavtalen.
1. På hurtigfanen **Linjedetaljer** på fanen **Produktdimensjoner** i feltet **Område** velger du lagerområdet for varen.
1. Hvis du vil opprette en serviceordre fra avtalelinjen, går du til hurtigfanen **Linjer**, klikker på **Opprett serviceordrer** og skriver deretter inn den relevante informasjonen i skjemaet **Opprett serviceordrer**.

## <a name="see-also"></a>Se også

[Opprette serviceordrer automatisk](create-service-orders-automatically.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
