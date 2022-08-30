---
title: Ekstra lokasjonssoner
description: Denne artikkelen gir en oversikt over de nye lokasjonssonene som er lagt til i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336523"
---
# <a name="additional-location-zones"></a>Ekstra lokasjonssoner

[!include [banner](../includes/banner.md)]

Tre nye sonefelt er tilgjengelige i Microsoft Dynamics 365 Supply Chain Management. Lagerledere kan bruke dem til å definere flere lagerorganisasjoner eller -oppsett. De nye sonefeltene kan enten angis manuelt eller ved hjelp av veiviseren for **lokasjonsoppsett**. De kan brukes i alle spørringer eller filtreringer som bruker Lokasjoner-tabellen.

Ingen ekstra oppsett er nødvendig for å bruke sonefeltene.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Ekstra lokasjonssone

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.25 er funksjonen aktivert som standard. Funksjonen er obligatorisk fra og med Supply Chain Management, versjon 10.0.29 og kan ikke deaktiveres. Hvis du kjører en eldre versjon enn 10.0.29, kan administratorer aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Ekstra lokasjonssone* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="use-location-zones"></a>Bruke lokasjonssoner

1. Gå til **Lagerstyring \> Oppsett \> Lager \> Veiviser for lokasjonsoppsett**.
2. Angi følgende verdier:

    - I **Lager**-feltet velger du _62_.
    - Velg _GULV_ i feltet **Sone-ID**.
    - Velg _PICKZONE1_ i feltet **Ekstra sone 1**.
    - Velg _WEBSHOP1_ i feltet **Ekstra sone 2**.
    - Velg _GULV_ i **Lokasjonsprofil-ID**-feltet.

3. Velg **Gulv**-linjen.
4. Angi **1** i feltet _Fra-nummer_. Angi **3** i feltet _Til-nummer_.
5. Velg **Gang**-linjen.
6. Angi **1** i feltet _Fra-nummer_. Angi **5** i feltet _Til-nummer_.
7. Velg **Opprett**.
8. Du mottar meldinger som angir at nye lokasjoner er lagt til. Velg **Vis meldinger**-knappen for å vise meldingene.
9. Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**. De nye lokasjonene vises i listen, og alle sonefeltene er tilgjengelige (det vil si det eksisterende sonefeltet og de nye ekstra sonefeltene).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]