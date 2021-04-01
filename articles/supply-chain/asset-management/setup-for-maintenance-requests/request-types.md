---
title: Typer meldinger
description: Dette emnet forklarer hvordan du definerer typer meldinger i Aktivastyring.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e4f622cda62cad13a8146cbc26bc2e5f1a45222
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261195"
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

![Siden Typer meldinger](media/07-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]