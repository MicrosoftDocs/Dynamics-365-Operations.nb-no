---
title: Oversikt over tillegget for lagersynlighet
description: Denne artikkelen beskriver hva lagersynlighet er, og beskriver funksjonene i det.
author: yufeihuang
ms.date: 03/18/2022
ms.topic: overview
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 782545ea38a209eb4430607f5bca96e4e930efdc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897639"
---
# <a name="inventory-visibility-add-in-overview"></a>Oversikt over tillegget for lagersynlighet

[!include [banner](../includes/banner.md)]

Tillegget for lagersynlighet (også referert til som *Lagersynlighet*-tjenesten), tilbyr en uavhengig og høyt skalerbar mikrotjeneste som muliggjør posteringer av beholdningsendringer og synlighetssporing i sanntid på tvers av alle datakilder og kanaler. Her finner du en plattform som gjør det mulig å administrere det globale lageret ved hjelp av funksjonalitet som inkluderer (men som ikke er begrenset til) følgende liste:

- Sentral sporing av den siste lagerstatusen (for eksempel beholdning, bestilt, kjøpt, i transitt, returnert og satt i karantene) på tvers av alle datakildene, lagrene og lokasjonene ved å koble Supply Chain Management eller datakilder fra tredjepartslogistikk (for eksempel ordrestyringssystemer, tredjeparts systemer for ressursplanlegging for bedrifter \[ERP\], salgsstedssystemer \[POS\] og lagerstyringssystemer) i Lagersynlighet-tjenesten.
- Spør om tilgjengelighet og mangler for lagerbeholdning, og få umiddelbare svar ved å kalle opp Lagerstyring-tjenesten direkte.
- Unngå oversalg, spesielt når behovet kommer fra ulike kanaler, ved å foreta myke reserveringer i sanntid i Lagersynlighet-tjenesten.
- Bedre styring av lovte ordrer og kundeforventninger ved å angi nøyaktige nåværende eller neste tilgjengelige datoer, slik at ATP-funksjonen i omnikanal (tilgjengelig for ordre) kan beregne forventede datoer for innfrielse av ordrer.

## <a name="extensibility"></a>Utvidelsesmuligheter

Tjenesten Lagersynlighet er svært utvidbar, fordi datainndata og utdata ikke er begrenset til Microsoft-apper. Eksterne systemer kan få tilgang til tjenesten via RESTful-API-er (Application Programming Interface). I tillegg til å bruke medfølgende tilordninger som er angitt for Supply Chain Management-datakilden og -dimensjonene, kan du integrere Lagersynlighet med flere tredjepartssystemer ved å definere flere datakilder, lagerstatusmål (referert til som *fysiske mål* i Lagersynlighet-tjenesten) og lagerdimensjoner via konfigurasjonsappen. På denne måten kan du utføre fleksible spørringer og endre dine mange datakilder og forhåndsdefinerte lagerdimensjoner.

Fordi Lagersynlighet er bygd på Microsoft Dataverse, kan dessuten dataene brukes til å bygge og integreres med Power Apps. Du kan også bruke Power BI til å opprette tilpassede instrumentbord som oppfyller dine forretningskrav.

## <a name="scalability"></a>Skalerbarhet

Lagersynlighet-tjenesten kan skaleres opp eller ned, avhengig av datavolumet. Skalerbarhetsopplevelsen er som regel sømløs og utføres av Microsofts plattformteam, basert på automatisk registrering og vurdering av transaksjonsdatavolumet.

## <a name="feature-highlights"></a>Funksjonsfremhevinger

### <a name="get-a-global-view-of-real-time-inventory"></a>Få en global visning av beholdning i sanntid

Lagersynlighet sikrer at du har tilgang til de mest oppdaterte lagerantallene til enhver tid, på tvers av alle kanalene, lokasjonene og lagrene. Du vil dra mest nytte av å bruke det til å støtte den daglige driften hver gang du må hente lagerposter. Fysisk lagerbeholdning, antall solgt og antall kjøpt, er alle tilgjengelige fra boksen. Du kan også konfigurere andre fysiske lagermål (for eksempel returnerte, satt i karantene og posterte data) etter behov, for å hente disse opplysningene i sanntid. Lagersynlighet kan på en effektiv måte behandle millioner av lagerendringsposter. Disse dataene kan samles opp og gjenspeiles i de siste lagerantallene i tjenesten umiddelbart, per sekund eller per minutt, avhengig av intervallet som dataene er postert i. Hvis du vil ha mer informasjon, kan du se [Offentlige API-er for lagersynlighet](inventory-visibility-api.md).

### <a name="soft-reservation-to-avoid-overselling-across-all-order-channels"></a>Myk reservasjon for å unngå oversalg over alle ordrekanalene

Med *en myk reservasjon* kan du tilordne eller merke bestemte antall for å oppfylle en ordre eller et behov. En myk reservering påvirker ikke den fysiske beholdningen, men trekker fra beholdningsantallet som er *tilgjengelig for reservering*, og gir et oppdatert antall for fremtidig innfrielse av ordren. Denne funksjonen vil være nyttig hvis det kommer salgsforespørsler eller ordrer inn i virksomheten fra én eller flere kanaler eller datakilder som er utenfor ERP-systemet for planlegging av systemoppføringer.

Hvis du ikke bruker myke reserveringer i Lagersynlighet-tjenesten, må du vente til ordren er synkronisert til og behandlet av ERP-systemet for å få en oppdatering av det fysiske beholdningsantallet. Denne prosessen har vanligvis stor ventetid. Myke reserveringer har imidlertid umiddelbar innvirkning hver gang en salgsforespørsel eller ordre genereres i salgskanalene. De bidrar derfor til å forhindre oversalgssituasjoner ved å sørge for at omnikanalordrene ikke påvirker hverandre når de til slutt når ERP-systemet. Myke reserveringer sikrer også at du kan oppfylle alle ordrene du har lovt. Derfor hjelper de deg til å innfri kundenes forventninger og opprettholde kundelojaliteten. Hvis du vil ha mer informasjon, kan du se [Lagersynlighetsreservasjoner](inventory-visibility-reservations.md).

### <a name="immediate-response-of-atp-dates-confirmation"></a>Umiddelbart svar på ATP-datobekreftelse

Det er viktig å se nærmere på prosjektert lagerbeholdning (blant annet informasjon om forsyning, etterspørsel og prosjektert lagerbeholdning), fordi det hjelper firmaet ditt med å oppnå følgende mål:

- Minimer beholdningsnivåer for å redusere kostnadene til beholdningsstyring.
- Støtt intern ordrebehandling, slik at selgere kan beregne forsendelses- og leveringsdatoer basert på tilgjengeligheten av produktene som er bestilt.
- Sørg for oversikt over når kunder kan forvente at en vare som ikke er på lager, skal bli tilgjengelig, ved å angi neste tilgjengelige dato.

ATP-funksjonen er enkel å ta i bruk i din daglige innfrielsesprosess. På samme måte som andre Lagersynlighet-tilbud er ATP-funksjonen *global og i sanntid*. Derfor kan du konfigurere flere ATP-beregningsformler for å ha spørringer om fullstendig beholdningstilgjengelighet som dekker alle forretningskanalene og datakildene. Hvis du vil ha mer informasjon, kan du se [Tidsplaner for lagerendringer i Lagersynlighet og leveringskapasitet](inventory-visibility-available-to-promise.md).

### <a name="compatibility-with-advanced-warehouse-management-items"></a>Kompatibilitet med avanserte Warehouse Management-varer

Microsoft har som mål å gi direkte integrering med avansert Warehouse Management (WHS), slik at WHS-kunder også kan benytte seg av fordelene til Lagersynlighet-tjenesten. Per versjonen i bølge 1 i 2022 (offentlig forhåndsversjon i mars), støtter beholdningstjenesten WHS-varebeholdningsspørringer og ATP. Funksjonen for myk reservering og tildeling vil bli støttet for WHS-kunder i neste bølge. Hvis du vil ha mer informasjon, kan du se [Støtte i Lagersynlighet for WHS-varer](inventory-visibility-whs-support.md).

## <a name="licensing"></a>Lisensiering

Lagersynlighet-tjenesten er tilgjengelig i følgende versjoner:

- **Lagersynlighet-tillegg for Microsoft Dynamics 365 Supply Chain Management** – For firmaer som har en gyldig Supply Chain Management-lisens, er Lagersynlighet tilgjengelig uten ekstra lisenskostnader. Du kan begynne å prøve det ut i dag. Hvis du vil ha mer informasjon om installasjonen, kan du se [Installere og definere lagersynlighet](inventory-visibility-setup.md).
- **Lagersynlighet-tjenesten som en komponent i IOM** – Denne versjonen er enten for IOM-kunder (Intelligent Order Management) eller firmaer som ikke bruker Supply Chain Management som sitt ERP-system. Lisensen er inkludert i IOM-bunten. Hvis du vil ha mer informasjon, kan du se [Oversikt over Intelligent Order Management](/dynamics365/intelligent-order-management/overview).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
