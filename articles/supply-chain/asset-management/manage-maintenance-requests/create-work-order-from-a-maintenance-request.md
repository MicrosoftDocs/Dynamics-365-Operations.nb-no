---
title: Opprette arbeidsordrer fra meldinger
description: Denne artikkelen forklarer hvordan du oppretter en arbeidsordre fra en melding i Aktivastyring.
author: johanhoffmann
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb54ec3466086afbd87a023a40e346a6a3464c98
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017181"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Opprette arbeidsordrer fra meldinger

[!include [banner](../../includes/banner.md)]

 


Når du har opprettet meldinger, kan du enkelt konvertere dem til arbeidsordrer. Denne artikkelen beskriver den raskeste måten å arbeide med meldinger på, oppdatere flere meldinger samtidig og deretter opprette en arbeidsordre for flere meldinger samtidig. På siden **Aktive meldinger** eller **Mine meldinger for funksjonslokasjon** kan du også arbeide med én melding om gangen og konvertere en vedlikeholdssforespørsel til en arbeidsordre.

> [!NOTE]
> Hver melding kan være relatert til bare én arbeidsordre. Flere meldinger kan imidlertid inkluderes i én arbeidsordre, selv om meldingene har forskjellige aktiva.

1. Velg **Aktivastyring** \> **Meldinger** \> **Alle meldinger**.
2. Før du kan opprette en arbeidsordre fra meldinger, må du minst velge en vedlikeholdsjobbtype for meldingene, og også en type variant og fag for vedlikeholdsjobber, hvis denne informasjonen er relevant. I rutenettvisningen kan du enkelt oppdatere informasjon for en melding.
3. Når du er klar til å opprette en arbeidsordre, velger du meldingene du vil inkludere i den.

    - Hvis du velger flere meldinger for å konvertere til en arbeidsordre, må både feltet **Aktiva** og **Vedlikeholdsjobbtype** være angitt før du oppretter arbeidsordren.
    - Hvis du velger én melding for å konvertere til en arbeidsordre, må bare feltet **Aktiva** være angitt før du oppretter arbeidsordren. Når du oppretter arbeidsordren, kan du imidlertid velge en vedlikeholdsjobbtype (og en tilknyttet variant og fag for vedlikeholdsjobbtypen hvis denne informasjonen er relevant), i dialogboksen **Opprett Arbeidsordre**.

4. Velg **Arbeidsordre**.
5. Angi feltene i dialogboksen **Opprett arbeidsordre**, og velg deretter **OK**.

    En meldingslinje kan varsle deg om at det er opprettet en ny arbeidsordre.

    I tillegg når du oppretter en arbeidsordre som er basert på en melding, hvis aktivumet som er knyttet til meldingen er inkludert i en garantiavtale, varsler en meldingslinje deg om garantiavtalen.

6. Velg **Aktivastyring** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, og åpne den nye arbeidsordren.

    ![Åpne ny arbeidsordre.](media/05-manage-maintenance-requests.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]