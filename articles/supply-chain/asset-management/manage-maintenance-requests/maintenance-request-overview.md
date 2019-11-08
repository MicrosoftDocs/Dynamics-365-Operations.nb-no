---
title: Vedlikeholdsanmodninger
description: Dette emnet gir en oversikt over administrasjon av vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b19a92924d73847d9d2c09cd0ed111a9cbfdccbf
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571651"
---
# <a name="maintenance-requests"></a>Vedlikeholdsanmodninger

[!include [banner](../../includes/banner.md)]

 

Vedlikeholdsanmodninger er notater eller deklarasjoner som opprettes for å varsle en leder eller planlegger at et aktivum kan kreve en vedlikeholds- eller reparasjonsjobb, men uten å opprette en arbeidsordre. Hvis innholdet i en vedlikeholdsanmodning anses som gyldig, kan en arbeidsordre opprettes basert på vedlikeholdsanmodningen.

Vedlikeholdsanmodninger kan opprettes for alle aktiva i Aktivastyring. Ulike typer vedlikeholdsanmodninger kan opprettes, avhengig av hvordan firmaet bruker vedlikeholdsanmodninger. Her er noen eksempler:

- Vedlikeholdsanmodninger
- Notater
- Korrigeringer eller forbedringer
- Investeringer
- Depotreparasjon (denne typen brukes når du mottar aktiva fra et annet sted, slik at du kan utføre en vedlikeholds- eller reparasjonsjobb, og deretter returnere aktivaet etter at jobben er fullført.)

## <a name="view-maintenance-requests"></a>Vis vedlikeholdsanmodninger

Hvis du vil vise vedlikeholdsanmodninger, velger du **Aktivastyring** \> **Felles** \> **Vedlikeholdsanmondninger** \> **Alle vedlikeholdsanmodninger**, **Aktive vedlikeholdsanmodninger** eller **Mine vedlikeholdsforespørsler for arbeidssted**. Hver listeside viser noe av informasjonen som er knyttet til en vedlikeholdsanmodning.

![Vis forespørsler om vedlikehold](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Bruk listesiden **Mine vedlikeholdsforespørsler for arbeidssted** for å vise en liste over vedlikeholdsforespørsler som inneholder enten arbeidssteder som du er knyttet til som arbeider, eller aktiva som er installert på arbeidssteder som du knyttet til som arbeider. (Hvis du vil ha informasjon om hvordan du definerer arbeidssteder for vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Selv om kundekontoinformasjon er tilgjengelig i Aktivaservicestyring (eksternt vedlikehold), er den ikke tilgjengelig i Aktivastyring (internt vedlikehold).

Hvis du vil åpne detaljvisningen for en post, går du til listesiden **Alle vedlikeholdsanmodninger**, og i rutenettvisningen velger du en kobling i kolonnen **Vedlikeholdsanmodning**.

![Vise detaljer for vedlikeholdsforespørsel](media/02-manage-maintenance-requests.png)

Knappene i handlingsruten er ordnet i kategorier. Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.

| Navn på knapp                      | Beskrivelse |
|----------------------------------|-------------|
| Rediger                             | Rediger den valgte vedlikeholdsanmodningen. |
| Nye                              | Opprett en ny vedlikeholdsanmodning. |
| Slett                           | Slett den valgte vedlikeholdsanmodningen. |
| Arbeidsordresamling                  | Koble den valgte vedlikeholdsanmodningen til en arbeidsordresamling. |
| Arbeidsordre                       | Opprett en arbeidsordre, basert på den valgte vedlikeholdsanmodningen. |
| Aktivumfeil                      | Klikk på **Aktivumfeil**, der du kan opprette en feilregistrering for den valgte vedlikeholdsanmodningen. |
| Arbeidsordrer                      | Vis en liste over alle arbeidsordrer som er koblet til den valgte vedlikeholdsanmodningen. |
| Oppdater tilstand for vedlikeholdsanmodning | Oppdater tilstanden for vedlikeholdsanmodningen. |
| Logg for livsløpstilstand              | Vis en logg som viser livsløpstilstandene til den valgte vedlikeholdsanmodningen. |
| Detaljer om vedlikeholdsanmodninger      | Skriv ut en rapport som viser detaljer om den valgte vedlikeholdsanmodningen. |
| Send ut aktivumlån                  | Velg et aktivumlån som skal være en midlertidig erstatning for aktivumet som er valgt i den valgte vedlikeholdsanmodningen. |
| Returner lån av gjenstander                | Registrer aktivumlånet som returnert. |

