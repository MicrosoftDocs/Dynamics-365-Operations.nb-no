---
title: Ekstra lokasjonssoner
description: Dette emnet gir en oversikt over de nye lokasjonssonene som er lagt til i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 662725edf5bf8d95be038f7c989b73d8d05fa0df
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996432"
---
# <a name="additional-location-zones"></a>Ekstra lokasjonssoner

[!include [banner](../includes/banner.md)]

Tre nye sonefelt er tilgjengelige i Microsoft Dynamics 365 Supply Chain Management. Lagerledere kan bruke dem til å definere flere lagerorganisasjoner eller -oppsett. De nye sonefeltene kan enten angis manuelt eller ved hjelp av veiviseren for **lokasjonsoppsett**. De kan brukes i alle spørringer eller filtreringer som bruker Lokasjoner-tabellen.

Ingen ekstra oppsett er nødvendig for å bruke sonefeltene.

## <a name="turn-on-the-additional-location-zone-feature"></a>Aktiver funksjonen for Ekstra lokasjonssone

Før du kan bruke *Ekstra lokasjonssone*-funksjonen, må den aktiveres i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Ekstra lokasjonssone*

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
