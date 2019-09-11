---
title: Kostnadskontroll for aktivumfeil
description: Dette emnet beskriver kostnadskontroll for aktivumfeil i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2fe75c327cdc2bdd76173430ed551895f5941c7b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918309"
---
# <a name="asset-fault-cost-control"></a>Kostnadskontroll for aktivumfeil

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring kan du beregne kostnader ved registreringer av aktivafeil for å få en oversikt over faktiske kostnader sammenlignet med budsjettkostnader ved feil. Faktiske kostnader er basert på posterte transaksjoner. Datoen er feildatoen da symptomet ble registrert.

1. Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Kostnadskontroll for aktivumfeil**.

2. I dialogboksen **Kostnadskontroll for aktivumfeil** velger du et finansdimensjonssett som skal tas med i beregningen, om nødvendig.

4. Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med en nullverdi.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert kostnadskontrollinjene skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle kostnadskontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kostnadskontrollinjer for aktivafeil på alle arbeidsstedsnivåer de er relatert til.

6. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer og feilårsaker i hurtigfanen **Poster som skal inkluderes**.

7. Klikk på **OK** for å starte beregningen.

8. I handlingsrutegruppene **Grupper etter...** klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

Figuren nedenfor viser et eksempel på beregning av kostnadskontroll for aktivumfeil.

![Figur 1](media/05-controlling-and-reporting.png)

Se i delen [Feilstyring](../setup-for-work-orders/fault-management.md) hvis du vil ha informasjon om hvordan du definerer feil.

>[!NOTE]
>Feltet **Opprinnelig budsjett** viser budsjettkostnader fra arbeidsordreprognosen. Feltet **Faktiske kostnader** viser posterte kostnader på arbeidsordrer. Feltet **Igangsatt kost** viser totale kostnader som firmaet har forpliktet seg til i forhold til arbeidsordrer.

