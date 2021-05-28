---
title: Meldinger
description: Dette emnet gir en oversikt over administrasjon av meldinger i Aktivastyring.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3c72a16b8f3865129ad737c511e50eb34c9f2e91
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015884"
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

Hvis du vil vise meldinger, velger du **Aktivastyring** \> **Felles** \> **Vedlikeholdsanmondninger** \> **Alle meldinger**, **Aktive meldinger** eller **Mine vedlikeholdsforespørsler for arbeidssted**. Hver listeside viser noe av informasjonen som er knyttet til en melding.

![Vis forespørsler om vedlikehold](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Bruk listesiden **Mine vedlikeholdsforespørsler for arbeidssted** for å vise en liste over vedlikeholdsforespørsler som inneholder enten arbeidssteder som du er knyttet til som arbeider, eller aktiva som er installert på arbeidssteder som du knyttet til som arbeider. (Hvis du vil ha informasjon om hvordan du definerer arbeidssteder for vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Selv om kundekontoinformasjon er tilgjengelig i Aktivaservicestyring (eksternt vedlikehold), er den ikke tilgjengelig i Aktivastyring (internt vedlikehold).

Hvis du vil åpne detaljvisningen for en post, går du til listesiden **Alle meldinger**, og i rutenettvisningen velger du en kobling i kolonnen **Melding**.

![Vise detaljer for vedlikeholdsforespørsel](media/02-manage-maintenance-requests.png)

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