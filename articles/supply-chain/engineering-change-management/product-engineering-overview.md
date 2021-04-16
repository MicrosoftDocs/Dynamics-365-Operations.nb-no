---
title: Oversikt over behandling av teknisk endring
description: Dette emnet gir en oversikt over behandling av teknisk endring, som hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 964db71efc9dc81d60199e37de8668de9d667496
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842087"
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

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Aktivere funksjonene for administrasjon av teknisk endring og versjonsdimensjon for systemet

Før du kan bruke Behandling av teknisk endring, må du aktivere både funksjonen *Behandling av teknisk endring* og funksjonens konfigurasjosnøkkel. Hvis du også vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), må du også aktivere funksjonen *Dimensjon for produktversjon* og funksjonens konfigurasjonsnøkkel.

Først aktiverer du funksjonene ved å følge disse trinnene.

1. Gå til [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Se etter oppdateringer.
1. Aktiver funksjonen som heter **Behandling av teknisk endring**.
1. Hvis du vil bruke funksjonen, aktiverer du også funksjonen som kalles **Produktdimensjon – Versjon**.

Deretter aktiverer du konfigurasjonsnøklene ved å følge disse trinnene.

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Utvid noden **Handel**
1. Merk av for **Behandling av teknisk endring**.
1. Hvis du vil bruke funksjonen, merker du også av for **Produktdimensjon – Versjon**.
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
