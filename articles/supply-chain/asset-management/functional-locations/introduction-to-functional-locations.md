---
title: Innføring i arbeidssteder
description: Denne artikkelen gir en oversikt over arbeidssteder i Aktivastyring.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a1c8c4db9aee68584ab35949745132091a34a58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882844"
---
# <a name="introduction-to-functional-locations"></a>Innføring i arbeidssteder

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen gir en oversikt over arbeidssteder i Aktivastyring. Arbeidssteder er elementer i en teknisk struktur, for eksempel funksjonsenhetene i et system. Arbeidssteder opprettes hierarkisk, og du installerer ressurser på dem. Oppsettet av arbeidssteder i firmaet avhenger av firmaets behov.

Her er noen eksempler på hvordan du kan bruke arbeidssteder:

- **Funksjonelt** – arbeidsstedene kan være brukerorienterte og brukes til å administrere aktiva som har lignende virkemåter.
- **Prosessrelatert** – arbeidsstedene kan være arbeidsflytorientert.
- **Romlig** – arbeidsstedene kan representere geografiske steder eller områder.

Hvert arbeidssted administreres uavhengig i Aktivastyring. Her er noen av de nyttige trekkene ved arbeidssteder:

- Definer spesifikasjoner for arbeidssteder.
- Definer spesifikasjonskrav for aktiva.
- Definer vedlikeholdssekvenser for forebyggende og reaktivt vedlikehold.
- Administrer installerte aktiva.
- Spore aktive forespørsler og arbeidsordrer som er relatert til installerte aktiva.
- Spor feil som er registrert på aktiva.
- Spor vedlikeholdskostnader for aktivaene som er knyttet til et arbeidssted til enhver tid.

Arbeidssteder gir sporbarhet for aktiva i forhold til forespørsler, arbeidsordrer, feilregistreringer, tilstandsvurderinger, registreringer av produksjonsstopp og registreringer av anleggsmiddeltellere.

> [!NOTE]
> Selv om et aktivum er installert på ulike arbeidssteder i løpet av levetiden, kan kostnadene relateres til hvert sted. Aktivakostnader er med andre ord alltid knyttet til arbeidsstedet som aktivumet ble installert på, til et gitt tidspunkt.

Arbeidssteder er **ikke** fleksible. Derfor, når du har definert et arbeidsstedshierarki, kan du ikke flytte steder rundt i det. 

Når du har opprettet et arbeidsstedshierarki, er neste trinn å installere ressurser på det. For mer informasjon, se [Installere aktiva på arbeidssteder](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Alle arbeidssteder

Velg **Aktivastyring** \> **Felles** \> **Arbeidssteder** \> **Alle arbeidssteder** for å åpne listesiden **Alle arbeidssteder**. Denne siden viser alle arbeidssteder og noe av informasjonen som er relatert til hvert av dem. Hvis du bare vil vise aktive arbeidssteder, velger du **Aktive arbeidssteder**. Hvis du bare vil vise arbeidsstedene du er knyttet til som en arbeider, velger du **Mine aktive arbeidssteder**. (Denne relasjonen er definert på **Arbeidere**-siden. Hvis du vil ha mer informasjon, se [Vedlikeholdspersoner og arbeidergrupper](../setup-for-objects/workers-and-worker-groups.md).)

På listesiden **Alle arbeidssteder** velger du en kobling i kolonnen **Arbeidssted** for å vise detaljene for den valgte posten. Hvis du vil redigere arbeidsstedet, velger du **Rediger**-knappen. Detaljvisningen viser detaljert informasjon som er knyttet til stedet. Den inneholder også en **Beslektet informasjon**-rute til høyre. Denne ruten viser arbeidsstedshierarkiet. Du kan vise og skjule **Beslektet informasjon**-ruten.

Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.

| Navn på knapp                         | Beskrivelse                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                                | Veksle mellom redigeringsmodus og visningsmodus for siden.                                                                                         |
| Nye                                 | Opprett et nytt arbeidssted.                                                                                                            |
| Slett                              | Slett det valgte arbeidsstedet.                                                                                                     |
| Gi nytt navn                              | Gi nytt navn til det valgte arbeidsstedet.                                                                                                     |
| Kopier struktur av arbeidssted  | Kopier arbeidsstedshierarkiet.                                                                                                      |
| Installer aktivum                       | Installer et aktivum, inkludert underordnede aktiva, på arbeidsstedet.                                                                        |
| Erstatt aktivum                       | Erstatt aktivahierarkiet med et annet aktivahierarki på arbeidsstedet.                                                         |
| Kostkontroll                        | Åpne siden **Kostnadskontroll for arbeidssted**, der du kan utføre en kostnadsberegning for det valgte arbeidsstedet.                |
| Timekontroll                        | Åpne siden **Timekontroll for arbeidssted**, der du kan utføre en kostnadsberegning for det valgte arbeidsstedet.                |
| Aktiva                              | Åpne siden **Alle aktiva**, der du kan vise en liste over aktiva som er knyttet til det valgte arbeidsstedet.                      |
| Forespørsler                            | Åpne siden **Aktive forespørsler**, der du kan vise en liste over forespørsler som er knyttet til det valgte arbeidsstedet.               |
| Arbeidsordrer                         | Åpne siden **Aktive arbeidsordrer**, der du kan vise en liste over arbeidsordrer som er knyttet til det valgte arbeidsstedet.         |
| Feil                              | Åpne siden **Aktivafeil**, der du kan vise en liste over registreringer av aktivafeil som er knyttet til det valgte arbeidsstedet. |
| Oppdater tilstand for arbeidssted    | Oppdater tilstanden til det valgte arbeidsstedet.                                                                                        |
| Logg for livssyklustilstand                 | Vis en logg som viser tilstandene til det valgte arbeidsstedet.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]