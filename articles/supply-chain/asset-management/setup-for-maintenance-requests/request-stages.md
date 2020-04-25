---
title: Livsløpstilstander for vedlikeholdsanmodning
description: Dette emnet beskriver hvordan du definerer livsløpstilstander for vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1e4412af0619b57467b5bcba75ea7259604d1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209013"
---
# <a name="maintenance-request-lifecycle-states"></a>Livsløpstilstander for vedlikeholdsanmodning

[!include [banner](../../includes/banner.md)]

 


Livsløpstilstander for vedlikeholdsanmodninger definerer stadiene som en forespørsel kan gå gjennom. Eksempler er **Opprettet**, **Aktiv** og **Avsluttet**. Når en vedlikeholdsanmondning konverteres til en arbeidsordre, bør livsløpstilstanden for vedlikeholdsanmodningen oppdateres til **Avsluttet** eller **Lukket** for å indikere at vedlikeholdsanmodningen ikke lenger er aktiv. På listesiden **Alle vedlikeholdsanmodninger** kan du vise alle vedlikeholdsanmodninger, uavhengig av livsløpstilstanden.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Definer livsløpstilstander for vedlikeholdsanmodninger

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Livsløpstilstander**.
2. Velg **Ny** for å opprette en livsløpstilstand for vedlikeholdsanmodning.
3. I feltet **Livsløpstilstand** angir du en ID for livsløpstilstanden.
4. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livsløpsmodeller** viser antall livsløpsmodeller for vedlikeholdsanmodninger som bruker denne livsløpstilstanden.

5. På hurtigfanen **Generelt** setter du alternativet **Aktiv** til **Ja** hvis en vedlikeholdsanmodning skal være aktiv mens den er i denne livsløpstilstanden.
6. Angi alternativet **Angi faktisk slutt** til **Ja** hvis en faktisk sluttdato og et klokkeslett automatisk skal angis på en vedlikeholdsanmodning som er i denne livsløpstilstanden.
7. Angi alternativet **Opprett arbeidsordre** til **Ja** hvis en arbeidsordre kan opprettes fra en vedlikeholdsanmodning som er i denne livsløpstilstanden.
8. Sett alternativet **Slett** til **Ja** hvis en vedlikeholdsanmodning kan slettes mens den er i denne livsløpstilstanden.
9. På hurtigfanen **Oppdater** er alternativene **Innkommende** og **Utgående** i **Aktiva**-delen relevante hvis du bruker depotreparasjon. Angi det aktuelle alternativet til **Ja** hvis livsløpstilstnaden for aktivaene som er valgt i en vedlikeholdsanmodning, skal oppdateres automatisk til **Innkommende** eller **Utgående** når livsløpstilstanden for denne vedlikeholdsanmodningen er angitt til **Innkommende** eller **Utgående**.

Illustrasjonen nedenfor viser et eksempel på siden **Livsløpstilstander for vedlikeholdsanmodning**.

![Siden Livsløpstilstander for vedlikeholdsanmodning](media/02-setup-for-requests.png)

> [!NOTE]
> Livsløpstilstander for vedlikeholdsanmodninger, livsløpstilstandsgrupper og -typer er knyttet til, og brukes på samme måte som, livsløpstilstander for arbeidsordre, livsløpstilstandsgrupper og -typer. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Definer livsløpsmodeller for vedlikeholdsanmodninger

Når du har opprettet livsløpstilstandene som kreves for vedlikeholdsanmodningene dine, kan de deles inn i livsløpstilstandsgrupper eller livsløpsmodeller. Livsløpsmodeller for vedlikeholdsanmodninger brukes til å opprette flyten som kan brukes for ulike typer vedlikeholdsanmodninger. Som et minimum bør en standard livsløpsmodell for vedlikeholdsanmodninger opprettes.

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Livsløpsmodeller**.
2. Velg **Ny** for å opprette en livsløpsmodell for vedlikeholdsanmodning.
3. I feltet **Livsløpsmodell** angir du en ID for livsløpsmodellen.
4. Angi et navn i **Navn**-feltet.

    På hurtigfanen **Detaljer** viser feltet **Livsløpstilstander** viser antall livsløpstilstander som er valgt i denne livsløpsmodellen. Feltet **Typer vedlikeholdsanmodninger** viser antall typer vedlikeholdsanmodninger som bruker denne livsløpsmodellen.

5. I hurtigfanen **Livsløpstilstander** velger du livsløpstilstandene som skal inkluderes i livsløpsmodellen:

    - Hvis du vil inkludere en livsløpstilstand i livsløpsmodellen, velger du den i delen **Gjenværende livsløpstilstander**, og deretter velger du pil høyre ![Pil høyre](media/03-setup-for-requests.png) for å flytte den til delen **Valgte livsløpstilstander**.
    - Hvis du vil inkludere alle tilgjengelige livsløpstilstander i livsløpsmodellen, velger du **Velg alle tilgjengelige tilstander**-knappen ![Velg alle tilgjengelige tilstander](media/04-setup-for-requests.png). Alle livsløpstilstander flyttes til delen **Valgte livsløpstilstander**.
    - Hvis du vil fjerne en livsløpstilstand fra livsløpsmodellen, velger du den i delen **Valgte livsløpstilstander**, og deretter velger du pil venstre ![Pil venstre](media/05-setup-for-requests.png) for å flytte den til delen **Gjenværende livsløpstilstander**.

6. I hurtigfanen **Generelt** er feltene i delen **Oppdateringer** relevante hvis du bruker depotreparasjon.

    - I feltet **Livsløpstilstand for mottatt aktiva** velger du livsløpstilstanden som aktiva som er valgt i en vedlikeholdsanmodning skal oppdateres automatisk til når de mottas for depotreparasjon.
    - I feltet **Livsløpstilstand for levert aktiva** velger du livsløpstilstanden som aktiva som er valgt i en vedlikeholdsanmodning skal oppdateres automatisk til når de returneres etter reparasjon.

Illustrasjonen nedenfor viser et eksempel på siden **Livsløpsmodeller for vedlikeholdsanmodning**.

![Siden Livsløpsmodeller for vedlikeholdsanmodning](media/06-setup-for-requests.png)
