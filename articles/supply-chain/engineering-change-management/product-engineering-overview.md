---
title: Oversikt over behandling av teknisk endring (inneholder video)
description: Denne artikkelen gir en oversikt over behandling av teknisk endring, som hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.
author: t-benebo
ms.date: 08/09/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a01dfd72428c75d1bb24f32c73c9c799a6c5017e
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682513"
---
# <a name="engineering-change-management-overview"></a>Oversikt over behandling av teknisk endring

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funksjonssammendrag

Dagens produsenter krever sterk produktdataadministrasjon, versjonskontroll og behandling av teknisk endring for å lykkes i en verden med stadig reduserende produktlivssykluser, økte krav til kvalitet og pålitelighet og et større fokus på produktsikkerhet.

Behandling av teknisk endring bringer struktur og disiplin til prosessen med produktdataadministrasjon, og gjør at produkter kan defineres, frigis og endres på en kontrollert måte som støttes av arbeidsflyter. Gjennom produktversjoner og behandling av teknisk endring kan du dokumentere, vurdere virkningen av og bruke tekniske endringer gjennom hele livssyklusen til et produkt.

Behandling av teknisk endring hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer. Her er en liste over hovedfunksjonene:

- Produktversjonering
- Forbedrede produktfrigivelsesfunksjoner som lar deg vedlikeholde produkthoveddata i én juridisk enhet (det tekniske firmaet) og publisere det fullstendig konfigurerte, frigitte produktet på andre juridiske enheter
- Regler for validering som krever at informasjon blir angitt før en produktversjon aktiveres (klargjøringskontroll)
- Forbedret behandling av produktlivssyklus ved finjustert kontroll over når et frigitt produkt kan brukes i bestemte forretningsprosesser
- Forespørsler om teknisk endring som støttes av arbeidsflyter
- Ordrer om teknisk endring som støttes av arbeidsflyter

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Den forrige videoen ([Endre administrasjonsfunksjoner i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Aktivere funksjonene for behandling av teknisk endring for systemet

Før du kan bruke Behandling av teknisk endring, må du aktivere både funksjonen *Behandling av teknisk endring* og funksjonens konfigurasjosnøkkel. Hvis du også vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), må du også aktivere både funksjonen *Dimensjon for produktversjon* og funksjonens konfigurasjonsnøkkel. Når disse forutsetningene er definert som nødvendige, kan du aktivere flere valgfrie funksjoner for behandling av teknisk endring.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Aktivere eller deaktivere de grunnleggende funksjonene for behandling av teknisk endring

Følg denne fremgangsmåten for å aktivere eller deaktivere de grunnleggende funksjonene for behandling av teknisk endring. Fra og med Supply Chain Management versjon 10.0.25 er funksjonen *Behandling av teknisk endring* aktivert som standard.

1. Gå til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Se etter oppdateringer.
1. Aktiver eller deaktiver funksjonen kalt *Behandling av teknisk endring* etter behov.
1. Hvis du vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), aktiverer du funksjonen kalt *Produktdimensjon – versjon*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Aktiver eller deaktiver de nødvendige konfigurasjonsnøklene

Deretter aktiverer du konfigurasjonsnøklene ved å følge disse trinnene. Disse er ikke aktivert som standard.

1. Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.
1. Utvid noden **Handel**.
1. Aktiver eller deaktiver konfigurasjonsnøkkelen for hovedfunksjonen ved å merke av for **Behandling av teknisk endring**.
1. Utvid noden **Behandling av teknisk endring**, og merk av for eller fjern merket i de følgende avmerkingsboksene etter behov (avhengig av funksjonene du vil bruke):

    - **Attributtsøk** – Merk av i avmerkingsboksen for å aktivere [attributtsøkfunksjonen](engineering-attributes-and-search.md). Vi anbefaler at du aktiverer denne funksjonen, men du kan fjerne merket i denne boksen hvis du ikke vil bruke den.
    - **Endringsstyring for prosessproduksjon** – Merk av i denne avmerkingsboksen hvis du vil bruke Styring av teknisk endring til å administrere endringer i formler for prosessproduksjon. Hvis du ikke trenger å administrere formler, kan du fjerne merket i denne avmerkingsboksen. Hvis du vil ha mer informasjon, kan du se [Behandle endringer i formler og ingrediensene](manage-formula-changes.md).

1. Hvis du også vil bruke versjonsdimensjonen, merker du av for **Produktdimensjon – Versjon**. (Denne avmerkingsboksen er lengre nede i listen og ikke nestet under noden **Behandling av teknisk endring**.) Du kan fjerne merket i denne avmerkingsboksen hvis du ikke trenger denne funksjonen.
1. Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Databasen må synkroniseres for å sikre at konfigurasjonsnøklene er riktig oppdatert for å gjenspeile endringene. Gjør ett av følgende, avhengig av hvilken type miljø du arbeider i:
    - **For miljøer på nivå 1 (utvikling)**: Åpne prosjektet i Microsoft Visual Studio, og velg deretter **Dynamics 365 \> Synkroniser database \> Synkroniser**.
    - **For miljøer på nivå 2 (og høyere)**: Databasen synkroniseres automatisk etter at du har satt miljøet inn i og ut av vedlikeholdsmodus, så du kan hoppe over dette trinnet.

> [!NOTE]
> Hvis du vil bruke styring av teknisk endring, må både stykklistenummerserien og formelnummerserien (hvis du bruker formler) settes til *Automatisk* på **Nummerserier**-siden.

### <a name="turn-on-additional-engineering-change-management-features"></a>Aktivere ekstra funksjoner for behandling av teknisk endring for systemet

Når du har aktivert de grunnleggende funksjonene for teknisk endringsbehandlingog aktivert konfigurasjonsnøklene, blir flere tilleggs- og valgfrie funksjoner for teknisk endringsbehandling lagt til i funksjonsadministrasjon. Hver av disse funksjonene er oppført under modulen **Styring av teknisk endring**. Tabellen nedenfor beskriver hver valgfrie funksjon, og inneholder koblinger til mer informasjon.

| Funksjonsnavn i funksjonsbehandling | Beskrivelse | Funksjonstilstand |
|---|---|---|
| Aktiver endringsstyring på eksisterende produkter | <p>Ved hjelp av denne funksjonen kan du konvertere eksisterende produkter til tekniske produkter slik at du kan begynne å administrere dem ved å bruke teknisk endringsbehandling.</p><p>Hvis du vil ha mer informasjon, kan du se [Aktiver endringsstyring på eksisterende produkter](change-management-existing-products.md).</p> | Aktivert som standard fra og med versjon 10.0.25. |
| Tekniske varslinger for produksjon | <p>Når et produkt endres i ingeniørvirksomhet, kan det være viktig å varsle produksjonen om disse endringene. På den måten kan produksjonsarbeidere gjøre noe, for eksempel erstatning av komponent, stykkliste eller ruteerstatning. Ved hjelp av denne funksjonen kan du varsle produksjon om endringer i produkter som produseres.</p><p>Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).</p> |  Aktivert som standard fra og med versjon 10.0.25. |
| Forbedret attributtarv for Styring av teknisk endring | <p>Denne funksjonen forenkler administrasjon av attributter for ferdige varer eller midlertidige varer. Når denne funksjonen er aktivert, er det enklere å identifisere alle attributtene som tilhører en vare, og du kan velge attributtene som skal overføres fra denne varen til den overordnede varen. Denne funksjonen er nyttig hvis for eksempel én komponent av en ferdig vare er skjør, giftig eller brannfarlig, fordi du enkelt kan identifisere det skjøre, giftige eller brannfarlige attributtet og overføre det til ferdigvaren.</p><p>Hvis du vil ha mer informasjon, kan du se [Tekniske attributter og søk i tekniske attributter](engineering-attributes-and-search.md).</p> |  Aktivert som standard fra og med versjon 10.0.25. |
| Produktklargjøringskontroller | <p>Med denne funksjonen kan du sette opp beredskapskontroller for standardprodukter (ikke-tekniske). Bruk produktberedskapskontroller for å sikre at hvert produkt er fullstendig definert, og at alle de nødvendige policyene konfigureres før produktet gjøres tilgjengelig og brukes i transaksjoner. Hvis du deaktiverer denne funksjonen etter at den er brukt en stund, vil alle eksisterende beredskapskontroller for standardprodukter bli slettet.</p><p>Hvis du vil ha mer informasjon, kan du se [Produktklargjøring](product-readiness.md).</p> |  Aktivert som standard fra og med versjon 10.0.25. |
| Administrer endringer i formler og ingredienser | <p>Ved hjelp av denne funksjonen kan du spore endringer i formelingredienser, koprodukter og biprodukter.</p><p>Hvis du vil ha mer informasjon, kan du se [Behandle endringer i formler og ingrediensene](manage-formula-changes.md).</p> |  Aktivert som standard fra og med versjon 10.0.25. |
| Variantgenerering for tekniske produkter | <p>Ved hjelp av denne funksjonen kan du generere varianter for tekniske produkter basert på tilgjengelige dimensjonsverdier.</p><p>Hvis du vil ha mer informasjon, kan du se [Generere varianter for tekniske produkter](engineering-variants.md).</p> |  Aktivert som standard fra og med versjon 10.0.25. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

