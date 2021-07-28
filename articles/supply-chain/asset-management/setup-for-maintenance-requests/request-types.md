---
title: Typer meldinger
description: Dette emnet forklarer hvordan du definerer typer meldinger i Aktivastyring.
author: johanhoffmann
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 125a4efda6fe8e9e65e2a0c166355235727e6cfa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356446"
---
# <a name="maintenance-request-types"></a>Typer meldinger

[!include [banner](../../includes/banner.md)]

 

Typer vedlikeholds anmodninger brukes til å kategorisere meldinger. Du kan for eksempel ha typer meldinger som er knyttet til forebyggende vedlikehold og korrigerende vedlikehold. Eller du kan ha en spesiell type melding som brukes til å administrere reparasjon av aktiva (depotreparasjon).

En type melding definerer tilknytningen med en livssyklusgruppe for meldinger (livssyklusmodell for vedlikehold). Livssyklusmodeller for meldinger definerer livssyklustilstandene som kan angis for en melding. (Eksempler på livssyklustilstander for meldinger omfatter **Opprettet**, **Aktiv** og **Avsluttet**.)

1. Velg **Aktivastyring** \> **Oppsett** \> **Meldinger** \> **Typer meldinger**.
2. Velg **Ny** for å opprette en type melding.
3. Angi en ID for typen melding i feltet **Type melding**.
4. Angi et navn i **Navn**-feltet.
5. På hurtigfanen **Generelt**, i feltet **Livssyklusmodell for melding**, velger du en livssyklusmodell for melding.
6. Velg en arbeidsordretype i feltet **Arbeidsordretype**. Når en melding konverteres til en arbeidsordre, får arbeidsordren automatisk arbeidsordretypen som er knyttet til typen melding.

Illustrasjonen nedenfor viser et eksempel på siden **Typer meldinger**.

![Siden Typer meldinger.](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]