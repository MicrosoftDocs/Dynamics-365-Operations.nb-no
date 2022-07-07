---
title: Innføring i funksjonslokasjoner
description: Denne artikkelen gir en oversikt over funksjonslokasjoner i Aktivastyring.
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
ms.openlocfilehash: a94b366dc725db3af01c156ae517a241213f7d52
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016050"
---
# <a name="introduction-to-functional-locations"></a>Innføring i funksjonslokasjoner

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen gir en oversikt over funksjonslokasjoner i Aktivastyring. Funksjonslokasjoner er elementer i en teknisk struktur, for eksempel funksjonsenhetene i et system. Funksjonslokasjoner opprettes hierarkisk, og du installerer ressurser på dem. Oppsettet av funksjonslokasjoner i firmaet avhenger av firmaets behov.

Her er noen eksempler på hvordan du kan bruke funksjonslokasjoner:

- **Funksjonelt** – funksjonslokasjonene kan være brukerorienterte og brukes til å administrere aktiva som har lignende virkemåter.
- **Prosessrelatert** – funksjonslokasjonene kan være arbeidsflytorientert.
- **Romlig** – funksjonslokasjonene kan representere geografiske steder eller områder.

Hvert funksjonslokasjon administreres uavhengig i Aktivastyring. Her er noen av de nyttige trekkene ved funksjonslokasjoner:

- Definer spesifikasjoner for funksjonslokasjoner.
- Definer spesifikasjonskrav for aktiva.
- Definer vedlikeholdssekvenser for forebyggende og reaktivt vedlikehold.
- Administrer installerte aktiva.
- Spore aktive forespørsler og arbeidsordrer som er relatert til installerte aktiva.
- Spor feil som er registrert på aktiva.
- Spor vedlikeholdskostnader for aktivaene som er knyttet til en funksjonslokasjon til enhver tid.

Funksjonslokasjoner gir sporbarhet for aktiva i forhold til forespørsler, arbeidsordrer, feilregistreringer, tilstandsvurderinger, registreringer av produksjonsstopp og registreringer av anleggsmiddeltellere.

> [!NOTE]
> Selv om et aktivum er installert på ulike funksjonslokasjoner i løpet av levetiden, kan kostnadene relateres til hvert sted. Aktivakostnader er med andre ord alltid knyttet til funksjonslokasjonen som aktivumet ble installert på, til et gitt tidspunkt.

Funksjonslokasjoner er **ikke** fleksible. Derfor, når du har definert et funksjonslokasjonshierarki, kan du ikke flytte steder rundt i det. 

Når du har opprettet et funksjonslokasjonshierarki, er neste trinn å installere ressurser på det. For mer informasjon, se [Installere aktiva på funksjonslokasjoner](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Alle funksjonslokasjoner

Velg **Aktivastyring** \> **Funksjonslokasjoner** \> **Alle funksjonslokasjoner** for å åpne listesiden **Alle funksjonslokasjoner**. Denne siden viser alle funksjonslokasjoner og noe av informasjonen som er relatert til hvert av dem. Hvis du bare vil vise aktive funksjonslokasjoner, velger du **Aktive funksjonslokasjoner**. Hvis du bare vil vise funksjonslokasjonene du er knyttet til som en arbeider, velger du **Mine aktive funksjonslokasjoner**. (Denne relasjonen er definert på **Arbeidere**-siden. Hvis du vil ha mer informasjon, se [Vedlikeholdspersoner og arbeidergrupper](../setup-for-objects/workers-and-worker-groups.md).)

På listesiden **Alle funksjonslokasjoner** velger du en kobling i kolonnen **Funksjonslokasjon** for å vise detaljene for den valgte posten. Hvis du vil redigere funksjonslokasjonen, velger du **Rediger**-knappen. Detaljvisningen viser detaljert informasjon som er knyttet til stedet. Den inneholder også en **Beslektet informasjon**-rute til høyre. Denne ruten viser funksjonslokasjonshierarkiet. Du kan vise og skjule **Beslektet informasjon**-ruten.

Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.

| Navn på knapp                         | Beskrivelse                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Rediger                                | Veksle mellom redigeringsmodus og visningsmodus for siden.                                                                                         |
| Nye                                 | Opprett en ny funksjonslokasjon.                                                                                                            |
| Slett                              | Slett den valgte funksjonslokasjonen.                                                                                                     |
| Gi nytt navn                              | Gi nytt navn til den valgte funksjonslokasjonen.                                                                                                     |
| Kopier struktur av funksjonslokasjon  | Kopier funksjonslokasjonshierarkiet.                                                                                                      |
| Installer aktivum                       | Installer et aktivum, inkludert underordnede aktiva, på funksjonslokasjonen.                                                                        |
| Erstatt aktivum                       | Erstatt aktivahierarkiet med et annet aktivahierarki på funksjonslokasjonen.                                                         |
| Kostkontroll                        | Åpne siden **Kostnadskontroll for funksjonslokasjon**, der du kan utføre en kostnadsberegning for den valgte funksjonslokasjonen.                |
| Timekontroll                        | Åpne siden **Timekontroll for funksjonslokasjon**, der du kan utføre en kostnadsberegning for den valgte funksjonslokasjonen.                |
| Aktiva                              | Åpne siden **Alle aktiva**, der du kan vise en liste over aktiva som er knyttet til den valgte funksjonslokasjonen.                      |
| Forespørsler                            | Åpne siden **Aktive forespørsler**, der du kan vise en liste over forespørsler som er knyttet til den valgte funksjonslokasjonen.               |
| Arbeidsordrer                         | Åpne siden **Aktive arbeidsordrer**, der du kan vise en liste over arbeidsordrer som er knyttet til den valgte funksjonslokasjonen.         |
| Feil                              | Åpne siden **Aktivafeil**, der du kan vise en liste over registreringer av aktivafeil som er knyttet til den valgte funksjonslokasjonen. |
| Oppdater tilstand for funksjonslokasjon    | Oppdater tilstanden til den valgte funksjonslokasjonen.                                                                                        |
| Logg for livssyklustilstand                 | Vis en logg som viser tilstandene til den valgte funksjonslokasjonen.                                                                        |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]