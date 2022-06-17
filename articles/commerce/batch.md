---
title: Forbedret håndtering av varer med partisporing
description: Denne artikkelen beskriver den forbedrede håndteringen av varer med partisporing under posteringsprosessen for utdrag i Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 736ab8dd21f04d7119cca6d53bfeb5e408b8cbd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881885"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Forbedret håndtering av varer med partisporing

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver den forbedrede håndteringen av varer med partisporing under posteringsprosessen for utdrag i Microsoft Dynamics 365 Commerce.

Partinumre kan ikke registreres for varer med partisporing på salgstidspunktet på salgsstedet i Dynamics 365 Commerce. Når salg posteres i Commerce Headquarters via kundeordrer eller utdragspostering, forventer Commerce imidlertid at det finnes gyldige partinumre for varer med partisporing for bestemte konfigurasjoner, og at de skal brukes under faktureringen.

Hvis det finnes gyldige partinumre for produktene, brukes både kundeordrefaktureringen og salgsordrefaktureringen fra utdragspostering. Hvis gyldige partinumre ikke er tilgjengelige for produkter, kan ikke fakturaprosessen for kundeordre postere, og salgsstedsbrukeren får en feilmelding. Utdragspostering går deretter inn i en feilstatus, selv om negativt lager er aktivert for produktene.

Når negativ beholdning er aktivert for varer med partisporing, sikrer forbedringer i Commerce at kunde- og salgsordrefakturering via utdragspostering ikke blokkeres for disse varene hvis beholdningen er 0 (null) eller det ikke finnes et partinummer. Den forbedrede funksjonaliteten bruker en standard parti-ID for salgslinjene når partinumre ikke er tilgjengelige.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Definere standard parti-ID som skal brukes for kundeordrer

Hvis du vil definere standard parti-ID som skal brukes for kundeordrer, gjør du følgende.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere** i Commerce Headquarters.
1. Angi en verdi i feltet **Standard parti-ID** i hurtigfanen **Ordre** i fanen **Kundeordrer**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Definer standard parti-ID som brukes for salgsordrefakturering ved utdragspostering

Hvis du vil definere standard parti-ID som brukes for salgsordrefakturering ved utdragspostering, gjør du følgende.

1. Gå til **Retail og Commerce \> Hovedkvarteroppsett \> Parametere \> Commerce-parametere** i Commerce Headquarters.
1. Angi en verdi i feltet **Standard parti-ID** i hurtigfanen **Lageroppdatering** i fanen **Postering**.

> [!NOTE]
> - Funksjonaliteten for standard parti-ID er bare tilgjengelig når avanserte lageraktiviteter er aktivert for det spesifikke butikklageret og varene. I en fremtidig versjon vil funksjonaliteten for standard parti-ID også støttes for scenarioer der avansert lagerstyring ikke er aktivert.
> - Støtte for den forbedrede håndteringen av satsvise varer under utdragspostering for ikke-avanserte lagerstyringsscenarier ble innført i Commerce versjon 10.0.5.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
