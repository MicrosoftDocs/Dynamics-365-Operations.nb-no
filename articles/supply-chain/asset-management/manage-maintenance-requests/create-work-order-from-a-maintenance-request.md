---
title: Opprette arbeidsordrer fra vedlikeholdsforespørsler
description: Dette emnet forklarer hvordan du oppretter en arbeidsordre fra en vedlikeholdsforespørsel i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847465"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Opprette arbeidsordrer fra vedlikeholdsforespørsler

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Når du har opprettet vedlikeholdsforespørsler, kan du enkelt konvertere dem til arbeidsordrer. Dette emnet beskriver den raskeste måten å arbeide med vedlikeholdsforespørsler på, oppdatere flere vedlikeholdsforespørsler samtidig og deretter opprette en arbeidsordre for flere vedlikeholdsforespørsler samtidig. På siden **Aktive vedlikeholdsforespørsler** eller **Mine vedlikeholdsforespørsler for arbeidssted** kan du også arbeide med én vedlikeholdsforespørsel om gangen og konvertere en vedlikeholdssforespørsel til en arbeidsordre.

> [!NOTE]
> Hver vedlikeholdsforespørsel kan være relatert til bare én arbeidsordre. Flere vedlikeholdsforespørsler kan imidlertid inkluderes i én arbeidsordre, selv om vedlikeholdsforespørslene har forskjellige aktiva.

1. Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlikeholdsforespørsler**.
2. Før du kan opprette en arbeidsordre fra vedlikeholdsforespørsler, må du minst velge en vedlikeholdsjobbtype for vedlikeholdsforespørslene, og også en type variant og fag for vedlikeholdsjobber, hvis denne informasjonen er relevant. I rutenettvisningen kan du enkelt oppdatere informasjon for en vedlikeholdsforespørsel.
3. Når du er klar til å opprette en arbeidsordre, velger du vedlikeholdsforespørslene du vil inkludere i den.

    - Hvis du velger flere vedlikeholdsforespørsler for å konvertere til en arbeidsordre, må både feltet **Aktiva** og **Vedlikeholdsjobbtype** være angitt før du oppretter arbeidsordren.
    - Hvis du velger én vedlikeholdsforespørsel for å konvertere til en arbeidsordre, må bare feltet **Aktiva** være angitt før du oppretter arbeidsordren. Når du oppretter arbeidsordren, kan du imidlertid velge en vedlikeholdsjobbtype (og en tilknyttet variant og fag for vedlikeholdsjobbtypen hvis denne informasjonen er relevant), i dialogboksen **Opprett Arbeidsordre**.

4. Velg **Arbeidsordre**.
5. Angi feltene i dialogboksen **Opprett arbeidsordre**, og velg deretter **OK**.

    En meldingslinje kan varsle deg om at det er opprettet en ny arbeidsordre.

    I tillegg når du oppretter en arbeidsordre som er basert på en vedlikeholdsforespørsel, hvis aktivaet som er knyttet til vedlikeholdsforespørselen er inkludert i en garantiavtale, varsler en meldingslinje deg om garantiavtalen.

6. Velg **Aktivastyring** \> **Felles** \> **Arbeidsordrer** \> **Alle arbeidsordrer**, og åpne den nye arbeidsordren.

    ![Figur 1](media/05-manage-maintenance-requests.png)

