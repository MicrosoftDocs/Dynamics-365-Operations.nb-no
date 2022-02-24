---
title: Oversikt over behandling av teknisk endring
description: Dette emnet gir en oversikt over behandling av teknisk endring, som hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514356"
---
# <a name="engineering-change-management-overview"></a>Oversikt over behandling av teknisk endring

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funksjonssammendrag

Dagens produsenter krever sterk produktdataadministrasjon, versjonskontroll og behandling av teknisk endring for å lykkes i en verden med stadig reduserende produktlivssykluser, økte krav til kvalitet og pålitelighet og et større fokus på produktsikkerhet.

Behandling av teknisk endring bringer struktur og disiplin til prosessen med produktdataadministrasjon, og gjør at produkter kan defineres, frigis og endres på en kontrollert måte som støttes av arbeidsflyter. Gjennom produktversjoner og behandling av teknisk endring kan du dokumentere, vurdere virkningen av og bruke tekniske endringer gjennom hele livssyklusen til et produkt.

Behandling av teknisk endring hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer. Her er en liste over hovedfunksjonene:

- Produktversjonering
- Forbedrede produktfrigivelsesfunksjoner som lar deg vedlikeholde produkthoveddata i én juridisk enhet (det tekniske firmaet) og publisere det fullstendig konfigurerte, frigitte produktet på andre juridiske enheter
- Regler for validering som krever at informasjon blir angitt før en produktversjon aktiveres (klargjøringskontroll)
- Forbedret behandling av produktlivssyklus ved finjustert kontroll over når et frigitt produkt kan brukes i bestemte forretningsprosesser
- Forespørsler om teknisk endring som støttes av arbeidsflyter
- Ordrer om teknisk endring som støttes av arbeidsflyter

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Den forrige videoen ([Endre administrasjonsfunksjoner i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

## <a name="turn-on-engineering-change-management-for-your-system"></a>Aktiver behandling av teknisk endring for systemet

Aktiver først behandling av teknisk endring ved å følge denne fremgangsmåten.

1. Gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Se etter oppdateringer.
1. Aktiver funksjonen som heter **Behandling av teknisk endring**.

Deretter aktiverer du **Behandling av teknisk endring**-konfigurasjonsnøkkelen ved å følge denne fremgangsmåten.

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Utvid **Handel**-noden, og velg deretter avmerkingsboksen **Behandling av teknisk endring**.
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
