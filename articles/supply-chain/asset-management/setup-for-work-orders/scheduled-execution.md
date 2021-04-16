---
title: Planlagt utførelse
description: Dette emnet beskriver planlagt utførelse i Aktivastyring.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fae899bcfa8bb2566d1a9aee3f0dbe22bc219edf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825644"
---
# <a name="scheduled-execution"></a>Planlagt utførelse

[!include [banner](../../includes/banner.md)]

 

Du kan bruke servicenivåer for arbeidsordrer til å definere planlagt utførelse. (Hvis du vil ha mer informasjon om servicenivåer for arbeidsordrer, se [Servicenivå og -beskrivelse](service-level-and-description.md).) Planlagt utførelse gir fleksibilitet i arbeidsplanlegging for vedlikeholdspersoner fordi du kan definere mer detaljerte eller mindre detaljerte krav for intervallet som en arbeidsordre skal fullføres i. For eksempel kan en vedlikeholdsperson som fullfører en jobb raskere enn forventet i et produksjonslokale, kunne gå videre til en annen jobb i nærheten som var planlagt for gjeldende uke, men ikke nødvendigvis for gjeldende dag. Denne metoden gjør det mulig å optimalisere arbeiderplanlegging og jobbfullførelse.

Oppsett av planlagt utførelse, som er knyttet til arbeidsordrer, kan være generisk eller spesifikt. Du kan definere generelle linjer som ikke er begrenset til bestemte arbeidsordretyper, anleggsmiddeltyper og så videre. Du kan også opprette planlagte utførelseslinjer som gjelder for en bestemt arbeidsordretype, anleggsmiddeltype, vedlikeholdsjobbtype og så videre.

1. Velg **Aktivastyring** \> **Oppsett** \> **Arbeidsordrer** \> **Planlagt utførelse**.
2. Velg **Ny** for å opprette en planlagt utførelseslinje.
3. Velg aktuelle verdier i feltene **Arbeidssted**, **Arbeidsordretype**, **Aktivatype**, **Produsent**, **Modell**, **Kategori for vedlikeholdsjobbtype**, **Vedlikeholdsjobbtype**, **Variant av vedlikeholdsjobbtype** og **Handel**.
4. Velg et servicenivå for arbeidsordren i **Servicenivå**-feltet. Hvis du lar dette feltet stå tomt, får du den mest generelle typen av planlagt utførelseslinje. Hvis du vil ha et eksempel på en generisk linje, kan du se den første posten i illustrasjonen nedenfor. Denne linjen gjør at alle arbeidsordrer som ikke har noe arbeidsordreservicenivå, kan planlegges for en bestemt dato og klokkeslett.
5. Velg tidsintervall i **Planlagt utførelse**-feltet.
6. Velg **Lagre**.

![Planlagt utførelse](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]