---
title: Lagerordrer for sky- og kantskalaenheter
description: Dette emnet inneholder informasjon om funksjonen for lagerordre som brukes som en del av arbeidsbelastningen for lagerskalaenhet.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: bd3c72f2c008b936ceda53a3fcdde79df1e6b1b7
ms.sourcegitcommit: a21166da59675e37890786ebf7e0f198507f7c9b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/03/2021
ms.locfileid: "7471698"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Lagerordrer for sky- og kantskalaenheter

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Ikke alle forretningsfunksjoner støttes fullstendig i den offentlige forhåndsversjonen når arbeidsbelastninger for skalaenhet brukes. Hvis du bruker skalaenheter, må du passe på at du bare bruker de prosessene som dette emnet beskriver som støttet.

## <a name="what-are-warehouse-orders"></a>Hva er lagerordrer?

*Lagerordrer* er en type ordre som brukes for å støtte lagerdistribusjoner for senter og skalaenhet. De gjør at du kan motta og sende beholdning når du kjører en lagerarbeidsbelastning på en skalaenhet.

Lagerordrer brukes som en del av behandling av både innkommende og utgående lagerstyring. De opprettes som en del av *Frigi til lager*-prosessen, som initialiseres på senteret.
For innkommende behandling brukes Warehouse Mobile App til å registrere fysisk lagerbeholdning under behandling av innkommende ordrer. Dette er tilgjengelig for bestillinger og produksjonsordrer som angir et skalaenhetslager og varer som er aktivert til å bruke lagerstyringsprosesser.
De utgående lagerordrene brukes som en del av forsendelsesbølgeprosessen for overføring og salgsordrer.

> [!IMPORTANT]
> Lagerordrer er bare tilgjengelige i distribusjoner som bruker [arbeidsbelastninger for lagerstyring for sky- og kantskalaenheter](cloud-edge-workload-warehousing.md).

## <a name="create-an-inbound-warehouse-order"></a>Opprette en innkommende lagerordre

Følg denne fremgangsmåten for å opprette en innkommende lagerordre for en bestillingsprosess.

1. Logg deg på forekomsten av Microsoft Dynamics 365 Supply Chain Management som kjører i senteret. (Du må starte prosessen *Frigi til lager* mens du er logget på senteret.)
1. Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.
1. Velg **Frigi til lager** i gruppen **Handlinger** i fanen **Lager** i handlingsruten.
1. Hvis du vil vise de relaterte lagerordrelinjene, åpner du den relevante bestillingen, velger en linje i **Bestillingslinjer**-delen og velger deretter **Lager \> Lagerordrelinjer** på verktøylinjen. Hvis du vil vise alle linjene, kan du gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**.

Du kan også utløse prosessen *Frigi til lager* fra en satsvis jobb ved å gå til **Lagerstyring > Frigi til lager > Automatisk frigivelse av bestillinger**. Når du definerer den satsvise jobben, kan du velge bestemte bestillingslinjer basert på en spørring. Et typisk scenario vil være å sette opp en gjentakende satsvis jobb som frigir alle bekreftede bestillingslinjer som forventes å ankomme neste dag.

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

I visningen **Lagerordrelinjer** kan du overvåke fremdriften til innkommende mottak ved å se gjennom verdiene i kolonnen **Gjenstående antall å motta**. Følg ett av disse trinnene for å vise detaljer som er knyttet til arbeid som er gjort ved å bruke mobilappen Lagerstyring.

- Gå til **Lagerstyring \> Forespørsler og rapporter \> Lagerordrelinjer**, og bruk filteret til å finne linjene du ser etter.
- Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**, og åpne den relevante bestillingen. Velg én eller flere linjer i delen **Bestillingslinjer**, og velg deretter **Lager \> Oppføringer for lagermottak** på verktøylinjen.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
