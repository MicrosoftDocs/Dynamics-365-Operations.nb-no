---
title: Aktiva og arbeidsordrer
description: Dette emnet beskriver aktiva og arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd55988578be2b0287b399549f17642bfb1693b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783484"
---
# <a name="assets-and-work-orders"></a>Aktiva og arbeidsordrer

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dette emnet beskriver aktiva og arbeidsordrer i Aktivastyring. Aktiva og arbeidsordrer er de sentrale delene av Aktivastyring. Et *aktivum* er en maskin eller maskindel som krever kontinuerlig vedlikehold og service. Aktiva kan opprettes i en hierarkisk struktur, og de kan være relatert til arbeidssteder. Vedlikeholdsjobber kan planlegges på alle nivåer i aktivastrukturen.

Forskjellige data, for eksempel produktinformasjon og spesifikasjon av aktiva, og nødvendige vedlikeholdsplaner er definert for hvert aktivum. Illustrasjonen nedenfor viser en oversikt over aktivadata og tilknytningen av aktiva til jobbtyper. Rød tekst brukes til eksempler som viser arv og avhengigheter.

![Figur 1](media/05-overview-image.png)

Hver arbeidsordre har en arbeidsordretype, for eksempel forebyggende vedlikehold, korrigerende vedlikehold eller inspeksjon. Arbeidsordren inneholder én eller flere arbeidsordrejobber. Hver arbeidsordrejobb definerer en jobb som må utføres på et aktivum og en relatert jobbtype. Eksempler på relaterte jobbtyper omfatter 10 000 km, 50 000 km, 1-års service og sikkerhetsinspeksjon. Én arbeidsordre kan knyttes til flere aktiva.

Følgende illustrasjon viser en oversikt over nøkkeldataene i en arbeidsordre.

![Figur 2](media/06-overview-image.png)

En arbeidsordre kan knyttes til en annen arbeidsordre, og jobbtyper kan inneholde etterfølgende jobber som oppretter en arbeidsordre. Generelt er det ingen avhengigheter mellom arbeidsordrer. De kan derfor endre livsløpstilstanden for arbeidsordrer og kan planlegges uavhengig av hverandre.

Arbeidsordrer kan opprettes på forskjellige måter som er relatert til korrigerende, forebyggende eller reaktivt vedlikehold. Du kan også opprette arbeidsordrer manuelt. Illustrasjonen nedenfor viser en oversikt over prosessen for automatisk eller manuell oppretting av arbeidsordrer.

![Figur 3](media/07-overview-image.png)

Du må fylle ut flere trinn når du vil planlegge og kjøre en vedlikeholdsjobb på en arbeidsordre. Følgende illustrasjon viser en oversikt over behandlingen for en arbeidsordre.

![Figur 4](media/08-overview-image.png)

> [!NOTE]
> Generelt, når du arbeider i Microsoft Dynamics 365 for Finance and Operations og **Aktivastyring**-modulen, velger du **Ny** for å opprette en ny post, du velger **Rediger** for å oppdatere en eksisterende post, og du velger **Lagre** for å lagre nye eller redigerte data.
