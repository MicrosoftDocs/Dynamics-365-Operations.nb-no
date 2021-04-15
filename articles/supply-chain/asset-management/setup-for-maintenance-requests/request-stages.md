---
title: Livssyklustilstander for melding
description: Dette emnet beskriver hvordan du definerer livssyklustilstander for meldinger i Aktivastyring.
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c95704b944f86a1cfc0654f0ebf5bc7c79bbeec9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808694"
---
# <a name="maintenance-request-lifecycle-states"></a>Livssyklustilstander for melding

[!include [banner](../../includes/banner.md)]

 


Livssyklustilstander for meldinger definerer stadiene som en forespørsel kan gå gjennom. Eksempler er **Opprettet**, **Aktiv** og **Avsluttet**. Når en vedlikeholdsanmondning konverteres til en arbeidsordre, bør livssyklustilstanden for meldingen oppdateres til **Avsluttet** eller **Lukket** for å indikere at meldingen ikke lenger er aktiv. På listesiden **Alle meldinger** kan du vise alle meldinger, uavhengig av livssyklustilstanden.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Definer livssyklustilstander for meldinger

1. Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Livssyklustilstander**.
2. Velg **Ny** for å opprette en livssyklustilstand for melding.
3. I feltet **Livssyklustilstand** angir du en ID for livssyklustilstanden.
4. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livssyklusmodeller** viser antall livssyklusmodeller for meldinger som bruker denne livssyklustilstanden.

5. På hurtigfanen **Generelt** setter du alternativet **Aktiv** til **Ja** hvis en melding skal være aktiv mens den er i denne livssyklustilstanden.
6. Angi alternativet **Angi faktisk slutt** til **Ja** hvis en faktisk sluttdato og et klokkeslett automatisk skal angis på en melding som er i denne livssyklustilstanden.
7. Angi alternativet **Opprett arbeidsordre** til **Ja** hvis en arbeidsordre kan opprettes fra en melding som er i denne livssyklustilstanden.
8. Sett alternativet **Slett** til **Ja** hvis en melding kan slettes mens den er i denne livssyklustilstanden.
9. I hurtigfanen **Oppdater** er de **inngående** og **utgående** alternativene i **Aktiva**-delen relevante hvis du bruker depotreparasjon. Sett det riktige alternativet til **Ja** hvis livssyklustilstanden for aktivaene som er valgt i en vedlikeholdsforespørsel, automatisk skal oppdateres til **Inngående** eller **Utgående** når livssyklustilstanden for melding for vedlikeholdsforespørselen er satt til **Inngående** eller **Utgående**.

Illustrasjonen nedenfor viser et eksempel på siden **Livssyklustilstander for melding**.

![Siden Livssyklustilstander for melding](media/02-setup-for-requests.png)

> [!NOTE]
> Livssyklustilstander for meldinger, livssyklustilstandsgrupper og -typer er knyttet til, og brukes på samme måte som, livssyklustilstander for arbeidsordre, livssyklustilstandsgrupper og -typer. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Definer livssyklusmodeller for meldinger

Når du har opprettet livssyklustilstandene som kreves for meldingene dine, kan de deles inn i livssyklustilstandsgrupper eller livssyklusmodeller. Livssyklusmodeller for meldinger brukes til å opprette flyten som kan brukes for ulike typer meldinger. Som et minimum bør en standard livssyklusmodell for meldinger opprettes.

1. Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Livssyklusmodeller**.
2. Velg **Ny** for å opprette en livssyklusmodell for melding.
3. I feltet **Livssyklusmodell** angir du en ID for livssyklusmodellen.
4. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livssyklustilstander** viser antall livssyklustilstander som er valgt i denne livssyklusmodellen. Feltet **Typer meldinger** viser antall typer meldinger som bruker denne livssyklusmodellen.

5. I hurtigfanen **Livssyklustilstander** velger du livssyklustilstandene som skal inkluderes i livssyklusmodellen:

    - Hvis du vil inkludere en livssyklustilstand i livssyklusmodellen, velger du den i delen **Gjenværende livssyklustilstander**, og deretter velger du pil høyre ![Pil høyre](media/03-setup-for-requests.png) for å flytte den til delen **Valgte livssyklustilstander**.
    - Hvis du vil inkludere alle tilgjengelige livssyklustilstander i livssyklusmodellen, velger du **Velg alle tilgjengelige tilstander**-knappen ![Velg alle tilgjengelige tilstander](media/04-setup-for-requests.png). Alle livssyklustilstander flyttes til delen **Valgte livssyklustilstander**.
    - Hvis du vil fjerne en livssyklustilstand fra livssyklusmodellen, velger du den i delen **Valgte livssyklustilstander**, og deretter velger du pil venstre ![Pil venstre](media/05-setup-for-requests.png) for å flytte den til delen **Gjenværende livssyklustilstander**.

6. I hurtigfanen **Generelt** er feltene i delen **Oppdateringer** relevante hvis du bruker depotreparasjon.

    - I feltet **Livssyklustilstand for mottatt aktiva** velger du livssyklustilstanden som aktiva som er valgt i en melding skal oppdateres automatisk til når de mottas for depotreparasjon.
    - I feltet **Livssyklustilstand for levert aktiva** velger du livssyklustilstanden som aktiva som er valgt i en melding skal oppdateres automatisk til når de returneres etter reparasjon.

Illustrasjonen nedenfor viser et eksempel på siden **Livssyklusmodeller for melding**.

![Siden Livssyklusmodeller for melding](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]