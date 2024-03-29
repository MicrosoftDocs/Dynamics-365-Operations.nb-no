---
title: Aktiva og arbeidsordrer
description: Denne artikkelen beskriver aktiva og arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df2d0fcc5162900ad2ad67f2629d14015f694bd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869698"
---
# <a name="assets-and-work-orders"></a>Aktiva og arbeidsordrer

[!include [banner](../../includes/banner.md)]

 

Denne artikkelen beskriver aktiva og arbeidsordrer i Aktivastyring. Aktiva og arbeidsordrer er de sentrale delene av Aktivastyring. Et *aktivum* er en maskin eller maskindel som krever kontinuerlig vedlikehold og service. Aktiva kan opprettes i en hierarkisk struktur, og de kan være relatert til arbeidssteder. Vedlikeholdsjobber kan planlegges på alle nivåer i aktivastrukturen.

Forskjellige data, for eksempel produktinformasjon og spesifikasjon av aktiva, og nødvendige vedlikeholdsplaner er definert for hvert aktivum. Illustrasjonen nedenfor viser en oversikt over aktivadata og tilknytningen av aktiva til jobbtyper. Rød tekst brukes til eksempler som viser arv og avhengigheter.

![Diagram som viser aktivadata knyttet til jobbtyper.](media/05-overview-image.png)

Hver arbeidsordre har en arbeidsordretype, for eksempel forebyggende vedlikehold, korrigerende vedlikehold eller inspeksjon. Arbeidsordren inneholder én eller flere arbeidsordrejobber. Hver arbeidsordrejobb definerer en jobb som må utføres på et aktivum og en relatert jobbtype. Eksempler på relaterte jobbtyper omfatter 10 000 km, 50 000 km, 1-års service og sikkerhetsinspeksjon. Én arbeidsordre kan knyttes til flere aktiva.

Følgende illustrasjon viser en oversikt over nøkkeldataene i en arbeidsordre.

![Diagram som viser nøkkeldata i en arbeidsordre.](media/06-overview-image.png)

En arbeidsordre kan knyttes til en annen arbeidsordre, og jobbtyper kan inneholde etterfølgende jobber som oppretter en arbeidsordre. Generelt er det ingen avhengigheter mellom arbeidsordrer. De kan derfor endre livssyklustilstanden for arbeidsordrer og kan planlegges uavhengig av hverandre.

Arbeidsordrer kan opprettes på forskjellige måter som er relatert til korrigerende, forebyggende eller reaktivt vedlikehold. Du kan også opprette arbeidsordrer manuelt. Illustrasjonen nedenfor viser en oversikt over prosessen for automatisk eller manuell oppretting av arbeidsordrer.

![Diagram som viser automatisk eller manuell oppretting av arbeidsordrer.](media/07-overview-image.png)

Du må fylle ut flere trinn når du vil planlegge og kjøre en vedlikeholdsjobb på en arbeidsordre. Følgende illustrasjon viser en oversikt over behandlingen for en arbeidsordre.

![Diagram som viser en oversikt over behandling av en arbeidsordre.](media/08-overview-image.png)

> [!NOTE]
> Generelt, når du arbeider i Dynamics 365 Supply Chain Management og **Aktivastyring**-modulen, velger du **Ny** for å opprette en ny post, du velger **Rediger** for å oppdatere en eksisterende post, og du velger **Lagre** for å lagre nye eller redigerte data.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]