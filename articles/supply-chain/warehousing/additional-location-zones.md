---
title: Ekstra lokasjonssoner
description: Dette emnet gir en oversikt over de nye lokasjonssonene som er lagt til i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/01/2020
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
ms.openlocfilehash: dd9e97cabe5e3d3bdc261a7280930b73eb8e1419
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103844"
---
# <a name="additional-location-zones"></a>Ekstra lokasjonssoner

[!include [banner](../includes/banner.md)]

Tre nye sonefelt er tilgjengelige i Microsoft Dynamics 365 Supply Chain Management. Lagerledere kan bruke dem til å definere flere lagerorganisasjoner eller -oppsett. De nye sonefeltene kan enten angis manuelt eller ved hjelp av veiviseren for **lokasjonsoppsett**. De kan brukes i alle spørringer eller filtreringer som bruker Lokasjoner-tabellen.

Ingen ekstra oppsett er nødvendig for å bruke sonefeltene.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Aktivere eller deaktivere funksjonen Ekstra lokasjonssone

Per Supply Chain Management versjon 10.0.25 er denne funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Ekstra lokasjonssone* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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