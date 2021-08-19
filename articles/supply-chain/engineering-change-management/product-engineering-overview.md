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
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8f2d577d9e48ced9d4c516a66e4f53671417875cbfb51bd6bdc2cb0938d83c01
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714962"
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

1. Gå til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Se etter oppdateringer.
1. Aktiver funksjonen som heter *Behandling av teknisk endring*.
1. Hvis du vil bruke funksjonen, aktiverer du også funksjonen som kalles *Produktdimensjon – Versjon*.

Deretter aktiverer du konfigurasjonsnøklene ved å følge disse trinnene.

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Utvid noden **Handel**.
1. Aktiver konfigurasjonsnøkkelen for hovedfunksjonen ved å merke av for **Behandling av teknisk endring**.
1. Utvid noden **Behandling av teknisk endring**, og merk av for eller fjern merket i de følgende avmerkingsboksene etter behov (avhengig av funksjonene du vil bruke):

    - **Attributtsøk** – Merk av i avmerkingsboksen for å aktivere [attributtsøkfunksjonen](engineering-attributes-and-search.md). Vi anbefaler at du aktiverer denne funksjonen, men du kan fjerne merket i denne boksen hvis du ikke vil bruke den.
    - **Endringsstyring for prosessproduksjon** – Merk av i denne avmerkingsboksen hvis du vil bruke Styring av teknisk endring til å administrere endringer i formler for prosessproduksjon. Hvis du ikke trenger å administrere formler, kan du fjerne merket i denne avmerkingsboksen. Hvis du vil ha mer informasjon, kan du se [Behandle endringer i formler og ingrediensene](manage-formula-changes.md).

1. Hvis du også vil bruke versjonsdimensjonen, merker du av for **Produktdimensjon – Versjon**. (Denne avmerkingsboksen er lengre nede i listen, og ikke nestet under noden **Behandling av teknisk endring**.)
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Fra og med april 2022 blir lisensnøklene for både **Behandling av teknisk endring** og **Produktdimensjon – Versjon** aktivert som standard for alle nye installasjoner, men du kan fremdeles deaktivere dem hvis du ønsker det.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
