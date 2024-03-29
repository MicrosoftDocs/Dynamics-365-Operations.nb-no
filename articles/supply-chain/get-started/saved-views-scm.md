---
title: Standard lagrede visninger for Supply Chain Management
description: Denne artikkelen beskriver standard lagrede visninger som er tilgjengelige, og forklarer hvordan du aktiverer dem.
author: kamaybac
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f94fffb9aa2c208b8c2c0005a2892853eda66a01
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334843"
---
# <a name="standard-saved-views-for-supply-chain-management"></a>Standard lagrede visninger for Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management har flere lagrede visninger du kan aktivere og bruke etter behov. Noen av disse standard lagrede visningene er optimalisert og navngitt for en bestemt rolle eller oppgave (for eksempel «Kvalitetskontroll» eller «Mottak»). Andre er optimalisert slik at de bare inneholder feltene og innstillingene som Microsoft-bruksstatistikk angir brukes oftest av kunder. Disse lagrede visningene kalles vanligvis *forenklede* visninger. Denne artikkelen beskriver standard lagrede visninger som er tilgjengelige, og forklarer hvordan du aktiverer og tilpasser dem.

Hvis du vil ha fullstendig informasjon om hvordan du arbeider med lagrede visninger, inkludert de standard lagrede visningene etter at du har aktivert dem, kan du se [Lagrede visninger](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="customizing-the-standard-saved-views"></a>Tilpasse standard lagrede visninger

Du kan tilpasse standard lagrede visninger slik du kan tilpasse dine egne lagrede visninger. Når du tilpasser en standard lagret visning, anbefaler vi imidlertid på det sterkeste at du lagrer den egendefinerte versjonen med et nytt navn. Ellers kan tilpassingene bli overskrevet når du oppdaterer Supply Chain Management.

Hvis du vil ha mer informasjon om hvordan du tilpasser og gir nytt navn til lagrede visninger, kan du se [Lagrede visninger](../../fin-ops-core/fin-ops/get-started/saved-views.md?toc=/dynamics365/supply-chain/toc.json).

## <a name="available-saved-views-and-how-to-enable-them"></a>Tilgjengelige lagrede visninger og hvordan du aktiverer dem

Hvis du vil bruke lagrede visninger, må du aktivere funksjonen *Lagrede visninger* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), uavhengig av om du vil bruke standard lagrede visninger (denne funksjonen er aktivert som standard fra og med versjon 10.0.21).

Resten av delene i denne artikkelen inneholder tabeller som beskriver standard lagrede visninger som for øyeblikket er tilgjengelige for hver relevante modul. Hver tabell viser navnet på hver lagrede visning, siden der du finner den, og en beskrivelse av den. Hver tabell viser også navnet på funksjonen som omfatter den lagrede visningen. Hvis du vil se en standard lagret visning i systemet, må du aktivere den angitte funksjonen i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Fra og med versjon 10.0.25 er alle visninger i listen aktivert som standard.

## <a name="saved-views-for-the-inventory-management-module"></a>Lagrede visninger for lagerstyringsmodulen

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for lagerstyringsmodulen.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Beholdningsliste | Finans | Med denne forenklede visningen kan du fokusere på økonomisk informasjon mens du administrerer lagerbeholdning. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Beholdningsliste | Kvalitetskontroll | Med denne forenklede visningen kan du fokusere på kvalitetskontroll mens du administrerer lagerbeholdning. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Beholdningsliste | Mottak | Med denne forenklede visningen kan du fokusere på mottaksoperasjoner mens du administrerer lagerbeholdning. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Beholdningsliste | Forsendelse | Med denne forenklede visningen kan du fokusere på forsendelsesoperasjoner mens du administrerer lagerbeholdning. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Transaksjoner | Forenklet | Med denne forenklede visningen kan du se gjennom lagerstatusen uten å bli distrahert av økonomisk informasjon og andre felter som ikke brukes så ofte. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Overføringsordrer | Forsendelse | Med denne forenklede visningen kan du fokusere på forsendelsesoperasjoner mens du administrerer overføringsordrer. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Overføringsordrer | Mottak | Med denne forenklede visningen kan du fokusere på mottaksoperasjoner mens du administrerer overføringsordrer. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Overføringsordrer | Kvalitetskontroll | Med denne forenklede visningen kan du fokusere på kvalitetskontroll mens du administrerer overføringsordrer. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Overføringsordrer | Finans | Med denne forenklede visningen kan du fokusere på økonomisk informasjon mens du administrerer overføringsordrer. | Lagrede visninger for lagerstyring<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-master-planning-module"></a>Lagrede visninger for hovedplanleggingsmodulen

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for hovedplanleggingsmodulen.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Planlagte bestillinger: detaljside for planlagt bestilling | Forenklet | Denne forenklede visningen omfatter bare feltene som oftest brukes til å arbeide med detaljene for én enkelt planlagt bestilling. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for planlagte bestillinger<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Planlagte bestillinger: listeside for planlagte bestillinger | Forenklet | Denne forenklede visningen omfatter bare feltene som oftest brukes til å arbeide med listen over planlagte bestillinger. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for planlagte bestillinger<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-procurement-and-sourcing-module"></a>Lagrede visninger for modulen Innkjøp og leverandører

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for modulen Innkjøp og leverandører.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Bestillingsdetaljer | Ordreopprettelse | Denne forenklede visningen er optimalisert for oppretting av nye bestillinger. | Lagrede visninger for bestillinger<br><br>Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Bestillingsdetaljer | Beholdningsstyring | Denne forenklede visningen er optimalisert for å utføre lagerrelaterte aktiviteter, for eksempel å følge opp beholdning som er mottatt, motta beholdning, kontrollere nettobehov og justere ordreantall. | Lagrede visninger for bestillinger<br><br>Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Bestillingsdetaljer | Økonomistyring | Denne forenklede visningen er optimalisert for å utføre økonomirelaterte aktiviteter, for eksempel fakturering og kontroll av priser, totaler og tillegg. | Lagrede visninger for bestillinger<br><br>Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Bestillingsdetaljer | Bestillingsgodkjenning | Denne forenklede visningen er optimalisert for godkjenning av nye bestillinger. | Lagrede visninger for bestillinger<br><br>Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-product-information-management-module"></a>Lagrede visninger for Produktinformasjon-styringsmodulen

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for Produktinformasjon-styringsmodulen.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Liste over frigitte produkter | Produktoppretting | En forenklet sidevisning som bare inneholder feltene som oftest brukes ved oppretting av produkter. | Lagrede visninger for frigitte produkter<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Detaljer om frigitt produkt | Produktoppretting | En forenklet sidevisning som bare inneholder feltene som oftest brukes ved oppretting av produkter. | Lagrede visninger for frigitte produkter<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Detaljer om frigitt produkt | Administrasjon av logistikkinformasjon | En forenklet sidevisning som bare inneholder feltene som oftest brukes ved administrering av logistikkinformasjon for produkter. | Lagrede visninger for frigitte produkter<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Detaljer om frigitt produkt | Behandling av innkjøpsinformasjon | En forenklet sidevisning som bare inneholder feltene som oftest brukes ved administrering av innkjøpsinformasjon for produkter. | Lagrede visninger for frigitte produkter<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Detaljer om frigitt produkt | Behandling av salgsinformasjon | En forenklet sidevisning som bare inneholder feltene som oftest brukes ved administrering av salgsrelatert informasjon for produkter. | Lagrede visninger for frigitte produkter<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-production-control-module"></a>Lagrede visninger for modulen Produksjonskontroll

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for modulen Produksjonskontroll.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Side for stykkliste for produksjonsordre | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for produksjonskontroll<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Side for produksjonsordredetaljer | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for produksjonskontroll<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Side for plukkliste for produksjonsordre | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for produksjonskontroll<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |
| Listeside for produksjonsordrer | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagrede visninger for produksjonskontroll<br><br>(Aktivert som standard fra og med versjon 10.0.21. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-sales-and-marketing-module"></a>Lagrede visninger for modulen Salg og markedsføring

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for modulen Salg og markedsføring.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Følgeseddeljournal | Journalgjennomgang | Denne forenklede visningen omfatter bare feltene som oftest brukes til å gå gjennom følgeseddeljournaler. | Lagrede visninger for salg og markedsføring<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Salgsordre | Bestillingsoppretting | Denne forenklede visningen omfatter bare feltene som oftest brukes til å opprette salgsordrer. | Lagrede visninger for salg og markedsføring<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Salgsordre | Ordregjennomgang | Denne forenklede visningen omfatter bare feltene som oftest brukes til å gå gjennom salgsordrer. | Lagrede visninger for salg og markedsføring<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Salgstilbud | Tilbudsoppretting | Denne forenklede visningen omfatter bare feltene som oftest brukes til å opprette salgstilbud. | Lagrede visninger for salg og markedsføring<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |

## <a name="saved-views-for-the-warehouse-management-module"></a>Lagrede visninger for modulen Lagerstyring

Tabellen nedenfor beskriver de lagrede visningene som er tilgjengelige for modulen Lagerstyring.

| Side | Visningsnavn | Vis beskrivelse | Funksjonsnavn |
|---|---|---|---|
| Alle laster | Innkommende behandling | Denne forenklede visningen omfatter bare feltene som oftest brukes til å behandle innkommende last. | Lagrede visninger for lastbehandling<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Alle laster | Utgående behandling | Denne forenklede visningen omfatter bare feltene som oftest brukes til å behandle utgående last. | Lagrede visninger for lastbehandling<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Alle forsendelser | Innkommende behandling | Denne forenklede visningen omfatter bare feltene som oftest brukes til å behandle innkommende forsendelser. | Lagrede visninger for forsendelsesbehandling<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Alle forsendelser | Utgående behandling | Denne forenklede visningen omfatter bare feltene som oftest brukes til å behandle utgående forsendelser. | Lagrede visninger for forsendelsesbehandling<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Alle bølger | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagret visning for bølgebehandling<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Arbeidsområde for lastplanlegging | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagret visning for arbeidsområdet for lastplanlegging<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |
| Arbeidsdetaljer | Forenklet | Denne forenklede visningen omfatter bare feltene som brukes oftest. Dermed får du en raskere oversikt og en effektivisert arbeidsprosess. | Lagret visning for arbeidsdetaljsiden<br><br>(Aktivert som standard fra og med versjon 10.0.25. Obligatorisk fra og med versjon 10.0.29.) |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]