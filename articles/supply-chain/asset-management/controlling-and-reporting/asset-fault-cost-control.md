---
title: Kostnadskontroll for aktivumfeil
description: Dette emnet beskriver kostnadskontroll for aktivumfeil i Aktivastyring.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bbf2d6b8e22981db76ca028073f8170cbe7f40b2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361072"
---
# <a name="asset-fault-cost-control"></a>Kostnadskontroll for aktivumfeil

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du beregne kostnader ved registreringer av aktivafeil for å få en oversikt over faktiske kostnader sammenlignet med budsjettkostnader. Faktiske kostnader er basert på posterte transaksjoner. Datoen er feildatoen da symptomet ble registrert.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Kostnadskontroll for aktivumfeil**.

2. I dialogboksen **Kostnadskontroll for aktivumfeil** velger du et finansdimensjonssett som skal tas med i beregningen, om nødvendig.

4. Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med en nullverdi.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert kostnadskontrollinjene skal være når det gjelder arbeidssted. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle kostnadskontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
    
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kostnadskontrollinjer for aktivafeil på alle arbeidsstedsnivåer de er relatert til.

6. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer og feilårsaker i hurtigfanen **Poster som skal inkluderes**.

7. Klikk på **OK** for å starte beregningen.

8. Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen. De valgte **Grupper etter**-knappen er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

Dette eksemplet viser beregning av kostnadskontroll for aktivumfeil.

- Feltet **Opprinnelig budsjett** viser budsjettkostnader fra arbeidsordreprognosen. 
- Feltet **Faktiske kostnader** viser posterte kostnader på arbeidsordrer. 
- Feltet **Igangsatt kost** viser totale kostnader som firmaet har forpliktet seg til i forhold til arbeidsordrer.

    ![Figur 1.](media/05-controlling-and-reporting.png)

Se emnet [Feilstyring](../setup-for-work-orders/fault-management.md) hvis du vil ha informasjon om hvordan du definerer feil.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]