---
title: Typer vedlikeholdsanmodninger
description: Dette emnet forklarer hvordan du definerer typer vedlikeholdsanmodninger i Aktivastyring.
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434520"
---
# <a name="maintenance-request-types"></a>Typer vedlikeholdsanmodninger

[!include [banner](../../includes/banner.md)]

 

Typer vedlikeholds anmodninger brukes til å kategorisere vedlikeholdsanmodninger. Du kan for eksempel ha typer vedlikeholdsanmodninger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold. Eller du kan ha en spesiell type vedlikeholdsanmodning som brukes til å administrere reparasjon av aktiva (depotreparasjon).

En type vedlikeholdsanmodning definerer tilknytningen med en livsløpsgruppe for vedlikeholdsanmodninger (livsløpsmodell for vedlikehold). Livsløpsmodeller for vedlikeholdsanmodninger definerer livsløpstilstandene som kan angis for en vedlikeholdsanmodning. (Eksempler på livsløpstilstander for vedlikeholdsanmodninger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Typer vedlikeholdsanmodninger**.
2. Velg **Ny** for å opprette en type vedlikeholdsanmodning.
3. Angi en ID for typen vedlikeholdsanmodning i feltet **Type vedlikeholdsanmodning**.
4. Angi et navn i **Navn**-feltet.
5. På hurtigfanen **Generelt**, i feltet **Livsløpsmodell for vedlikeholdsanmodning**, velger du en livsløpsmodell for vedlikeholdsanmodning.
6. Velg en arbeidsordretype i feltet **Arbeidsordretype**. Når en vedlikeholdsanmodning konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen vedlikeholdsanmodning.

Illustrasjonen nedenfor viser et eksempel på siden **Typer vedlikeholdsanmodninger**.

![Siden Typer vedlikeholdsanmodninger](media/07-setup-for-requests.png)
