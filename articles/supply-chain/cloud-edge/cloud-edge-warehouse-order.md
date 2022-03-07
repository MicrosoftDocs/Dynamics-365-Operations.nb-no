---
title: Lagerordrer for sky- og kantskalaenheter
description: Dette emnet inneholder informasjon om funksjonen for lagerordre som brukes som en del av arbeidsbelastningen for lagerskalaenhet.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105722"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Lagerordrer for sky- og kantskalaenheter

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ikke alle forretningsfunksjoner støttes fullstendig i den offentlige forhåndsversjonen når arbeidsbelastninger for skalaenhet brukes. Hvis du bruker skalaenheter, må du passe på at du bare bruker de prosessene som dette emnet beskriver som støttet.

## <a name="what-are-warehouse-orders"></a>Hva er lagerordrer?

*Lagerordrer* er en type ordre som ble opprettet for å støtte lagerdistribusjoner for senter og skalaenhet. De gjør at du kan motta beholdning når du kjører en lagerarbeidsbelastning på en skalaenhet. De brukes for øyeblikket bare med bestillinger.

Lagerordrer brukes som en del av lagerstyringsbehandling, for eksempel når lagerappen brukes til å registrere fysisk lagerbeholdning under behandling av en innkommende bestilling. Lagerordrer opprettes som en del av prosessen *Frigi til lager*, som er tilgjengelig for bestillinger som angir et skalaenhetslager, og varer som er aktivert for å bruke lagerstyringsprosesser.

> [!IMPORTANT]
> Lagerordrer er bare tilgjengelige i distribusjoner som bruker [arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Opprette en lagerordre

Følg denne fremgangsmåten for å opprette en lagerordre.

1. Logg deg på forekomsten av Microsoft Dynamics 365 Supply Chain Management som kjører i senteret. (Du må starte prosessen *Frigi til lager* mens du er logget på senteret.)
1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Hvis du vil vise de relaterte lagerordrelinjene, åpner du den relevante bestillingen, velger en linje i **Bestillingslinjer**-delen og velger deretter **Lager \> Lagerordrelinjer** på verktøylinjen. Hvis du vil vise alle linjene, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.

## <a name="cancel-a-warehouse-order"></a>Annullere en lagerordre

Som en del av prosessen *Frigi til lager* er lagertransaksjoner for bestilling koblet til lagerordrer og låst fra å bli oppdatert av senteret. Hvis du frigir til lageret ved en feiltakelse, eller hvis du har en annen grunn til å tilbakeføre opprettelsen av lagerordrelinjer, kan du be om å få annullere lagerordrelinjer.

Følg denne fremgangsmåten for å annullere lagerordrelinjer.

1. Logg deg på forekomsten av Supply Chain Management som kjører i senteret.
1. Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.
1. Velg relevant linje.
1. Velg **Annuller lagerordrelinjer** i handlingsruten.

> [!NOTE]
> Forespørselen om å få annullere linjer blir avslått for alle linjer som allerede venter på annullering, eller som aktivt behandles på et lager som kjører arbeidsbelastningen på en skalaenhet.

## <a name="monitor-a-warehouse-order"></a>Overvåke en lagerordre

I visningen **Lagerordrelinjer** kan du overvåke fremdriften til innkommende mottak ved å se gjennom verdiene i kolonnen **Gjenstående antall å motta**. Følg ett av disse trinnene for å vise detaljer som er knyttet til arbeid som er gjort ved å bruke lagerappen.

- Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**, og bruk filteret til å finne linjene du ser etter.
- Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**, og åpne den relevante bestillingen. Velg én eller flere linjer i delen **Bestillingslinjer**, og velg deretter **Lager \> Oppføringer for lagermottak** på verktøylinjen.
