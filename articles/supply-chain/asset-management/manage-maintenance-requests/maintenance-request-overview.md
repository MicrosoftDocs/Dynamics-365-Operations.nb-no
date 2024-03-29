---
title: Meldinger
description: Denne artikkelen gir en oversikt over administrasjon av meldinger i Aktivastyring
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015645"
---
# <a name="maintenance-requests"></a>Meldinger

[!include [banner](../../includes/banner.md)]

Meldinger er notater eller deklarasjoner som opprettes for å varsle en leder eller planlegger at et aktivum kan kreve en vedlikeholds- eller reparasjonsjobb, men uten å opprette en arbeidsordre. Hvis innholdet i en melding anses som gyldig, kan en arbeidsordre opprettes basert på meldingen.

Meldinger kan opprettes for alle aktiva i Aktivastyring. Ulike typer meldinger kan opprettes, avhengig av hvordan firmaet bruker meldinger. Her er noen eksempler:

- Meldinger
- Notater
- Korrigeringer eller forbedringer
- Investeringer
- Depotreparasjon (denne typen brukes når du mottar aktiva fra et annet sted, slik at du kan utføre en vedlikeholds- eller reparasjonsjobb, og deretter returnere aktivumet etter at jobben er fullført.)

## <a name="view-maintenance-requests"></a>Vis meldinger

Hvis du vil vise meldinger, velger du **Aktivastyring** \> **Meldinger** \> **Alle meldinger**, **Aktive meldinger** eller **Mine meldinger for funksjonslokasjon**. Hver listeside viser noe av informasjonen som er knyttet til en melding.

![Vis meldinger.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Bruk listesiden **Mine meldinger for funksjonslokasjon** for å vise en liste over meldinger som inneholder enten funksjonslokasjoner som du er knyttet til som arbeider, eller aktiva som er installert på funksjonslokasjoner som du knyttet til som arbeider. (Hvis du vil ha informasjon om hvordan du definerer funksjonslokasjoner for vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Selv om kundekontoinformasjon er tilgjengelig i Aktivaservicestyring (eksternt vedlikehold), er den ikke tilgjengelig i Aktivastyring (internt vedlikehold).

Hvis du vil åpne detaljvisningen for en post, går du til listesiden **Alle meldinger**, og i rutenettvisningen velger du en kobling i kolonnen **Melding**.

![Vise detaljer for melding.](media/02-manage-maintenance-requests.png)

Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.

| Navn på knapp                      | Beskrivelse |
|----------------------------------|-------------|
| Rediger                             | Rediger den valgte meldingen. |
| Nye                              | Opprett en ny melding. |
| Slett                           | Slett den valgte meldingen. |
| Arbeidsordresamling                  | Koble den valgte meldingen til en arbeidsordresamling. |
| Arbeidsordre                       | Opprett en arbeidsordre, basert på den valgte meldingen. |
| Aktivumfeil                      | Klikk på **Aktivumfeil**, der du kan opprette en feilregistrering for den valgte meldingen. |
| Arbeidsordrer                      | Vis en liste over alle arbeidsordrer som er koblet til den valgte meldingen. |
| Oppdater tilstand for melding | Oppdater tilstanden for meldingen. |
| Logg for livssyklustilstand              | Vis en logg som viser livssyklustilstandene til den valgte meldingen. |
| Detaljer om meldinger      | Skriv ut en rapport som viser detaljer om den valgte meldingen. |
| Send ut aktivumlån                  | Velg et aktivumlån som skal være en midlertidig erstatning for aktivumet som er valgt i den valgte meldingen. |
| Returner lån av gjenstander                | Registrer aktivumlånet som returnert. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]