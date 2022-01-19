---
title: Oversikt over behandling av teknisk endring (inneholder video)
description: Dette emnet gir en oversikt over behandling av teknisk endring, som hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d667aef827addcf7c34075b08afffffe3fd71935
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952604"
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

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

Den forrige videoen ([Endre administrasjonsfunksjoner i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Aktivere funksjonene for behandling av teknisk endring for systemet

Før du kan bruke Behandling av teknisk endring, må du aktivere både funksjonen *Behandling av teknisk endring* og funksjonens konfigurasjosnøkkel. Hvis du også vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), må du også aktivere både funksjonen *Dimensjon for produktversjon* og funksjonens konfigurasjonsnøkkel. Når disse forutsetningene er definert som nødvendige, kan du aktivere flere valgfrie funksjoner for behandling av teknisk endring.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Aktivere de grunnleggende funksjonene for behandling av teknisk endring for systemet

Først aktiverer du funksjonene ved å følge disse trinnene.

1. Gå til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Se etter oppdateringer.
1. Aktiver funksjonen som heter *Behandling av teknisk endring*.
1. Hvis du vil bruke funksjonen, aktiverer du også funksjonen som kalles *Produktdimensjon – Versjon*.

### <a name="turn-on-the-required-configuration-keys"></a>Slå på de nødvendige konfigurasjonsnøklene

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
1. Kjør en databasesynkronisering for å sikre at konfigurasjonsnøklene er riktig aktivert.

> [!IMPORTANT]
> Fra og med april 2022 blir lisensnøklene for både **Behandling av teknisk endring** og **Produktdimensjon – Versjon** aktivert som standard for alle nye installasjoner, men du kan fremdeles deaktivere dem hvis du ønsker det.

### <a name="turn-on-additional-engineering-change-management-features"></a>Aktivere ekstra funksjoner for behandling av teknisk endring for systemet

Når du har aktivert de grunnleggende funksjonene for teknisk endringsbehandlingog aktivert konfigurasjonsnøklene, blir flere tilleggs- og valgfrie funksjoner for teknisk endringsbehandling lagt til i funksjonsadministrasjon. Hver av disse funksjonene er oppført under modulen **Styring av teknisk endring**. Tabellen nedenfor beskriver hver valgfrie funksjon, og inneholder koblinger til mer informasjon.

| Funksjonsnavn i funksjonsbehandling | beskrivelse |
|---|---|
| Aktiver endringsstyring på eksisterende produkter | <p>Ved hjelp av denne funksjonen kan du konvertere eksisterende produkter til tekniske produkter slik at du kan begynne å administrere dem ved å bruke teknisk endringsbehandling.</p><p>Hvis du vil ha mer informasjon, kan du se [Aktiver endringsstyring på eksisterende produkter](change-management-existing-products.md).</p> |
| Tekniske varslinger for produksjon | <p>Når et produkt endres i ingeniørvirksomhet, kan det være viktig å varsle produksjonen om disse endringene. På den måten kan produksjonsarbeidere gjøre noe, for eksempel erstatning av komponent, stykkliste eller ruteerstatning. Ved hjelp av denne funksjonen kan du varsle produksjon om endringer i produkter som produseres.</p><p>Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).</p> |
| Forbedret attributtarv for Styring av teknisk endring | <p>Denne funksjonen forenkler administrasjon av attributter for ferdige varer eller midlertidige varer. Når denne funksjonen er aktivert, er det enklere å identifisere alle attributtene som tilhører en vare, og du kan velge attributtene som skal overføres fra denne varen til den overordnede varen. Denne funksjonen er nyttig hvis for eksempel én komponent av en ferdig vare er skjør, giftig eller brannfarlig, fordi du enkelt kan identifisere det skjøre, giftige eller brannfarlige attributtet og overføre det til ferdigvaren.</p><p>Hvis du vil ha mer informasjon, kan du se [Tekniske attributter og søk i tekniske attributter](engineering-attributes-and-search.md).</p> |
| Produktklargjøringskontroller | <p>Med denne funksjonen kan du sette opp beredskapskontroller for standardprodukter (ikke-tekniske). Bruk produktberedskapskontroller for å sikre at hvert produkt er fullstendig definert, og at alle de nødvendige policyene konfigureres før produktet gjøres tilgjengelig og brukes i transaksjoner. Hvis du deaktiverer denne funksjonen etter at den er brukt en stund, vil alle eksisterende beredskapskontroller for standardprodukter bli slettet.</p><p>Hvis du vil ha mer informasjon, kan du se [Produktklargjøring](product-readiness.md).</p> |
| Administrer endringer i formler og ingredienser | <p>Ved hjelp av denne funksjonen kan du spore endringer i formelingredienser, koprodukter og biprodukter.</p><p>Hvis du vil ha mer informasjon, kan du se [Behandle endringer i formler og ingrediensene](manage-formula-changes.md).</p> |
| Variantgenerering for tekniske produkter | <p>Ved hjelp av denne funksjonen kan du generere varianter for tekniske produkter basert på tilgjengelige dimensjonsverdier.</p><p>Hvis du vil ha mer informasjon, kan du se [Generere varianter for tekniske produkter](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
