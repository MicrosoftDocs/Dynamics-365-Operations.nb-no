---
title: Typer vedlikeholdsanmodninger
description: Dette emnet forklarer hvordan du definerer typer vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790525"
---
# <a name="maintenance-request-types"></a>Typer vedlikeholdsanmodninger

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Typer vedlikeholds anmodninger brukes til å kategorisere vedlikeholdsanmodninger. Du kan for eksempel ha typer vedlikeholdsanmodninger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold. Eller du kan ha en spesiell type vedlikeholdsanmodning som brukes til å administrere reparasjon av aktiva (depotreparasjon).

En type vedlikeholdsanmodning definerer tilknytningen med en livsløpsgruppe for vedlikeholdsanmodninger (livsløpsmodell for vedlikehold). Livsløpsmodeller for vedlikeholdsanmodninger definerer livsløpstilstandene som kan angis for en vedlikeholdsanmodning. (Eksempler på livsløpstilstander for vedlikeholdsanmodninger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)

1. Velg **Aktivastyring** \> **Oppsett** \> **Vedlikeholdsanmodninger** \> **Typer vedlikeholdsanmodninger**.
2. Velg **Ny** for å opprette en type vedlikeholdsanmodning.
3. Angi en ID for typen vedlikeholdsanmodning i feltet **Type vedlikeholdsanmodning**.
4. Angi et navn i **Navn**-feltet.
5. På hurtigfanen **Generelt**, i feltet **Livsløpsmodell for vedlikeholdsanmodning**, velger du en livsløpsmodell for vedlikeholdsanmodning.
6. Velg en arbeidsordretype i feltet **Arbeidsordretype**. Når en vedlikeholdsanmodning konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen vedlikeholdsanmodning.

Illustrasjonen nedenfor viser et eksempel på siden **Typer vedlikeholdsanmodninger**.

![Figur 1](media/07-setup-for-requests.png)
