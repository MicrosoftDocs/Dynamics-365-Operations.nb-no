---
title: Lagre oppgaveveiledninger i LCS og spille dem av på nytt
description: Denne artikkelen forklarer hvordan du lagrer oppgaveveiledninger til Microsoft Dynamics Lifecycle Services (LCS) og deretter spiller dem av på nytt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a18bb14ba8c3c926065c97b0ee26c38ee86ded2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053281"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Lagre oppgaveveiledninger i LCS og spille dem av på nytt

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Miljødetaljer** 

Microsoft Dynamics 365 Human Resources, som ble distribuert via Microsoft Dynamics Lifecycle Services (LCS)

**Problem**

Kunden ønsker å lagre nye oppgaveopptak til LCS-prosjektet og deretter spille av de lagrede oppgaveveiledningene på nytt.

**Oppløsning**

Følg disse trinnene for å lagre oppgaveopptak til LCS.

1. Logg på LCS, og velg prosjektet.
2. Velg **Forretningsprosessmodelerer**-flisen.
3. Vis denne siden i den "oppdaterte BPM-opplevelsen".
4. Velg et bibliotek, og velg deretter **Kopier**.
5. Angi et navn for Forretningsprosessmodelerer-modellen (BPM).
6. Logg på Human Resources fra LCS.
7. I **Søk**-feltet angir du **Hjelp**. Lifecycle Services-hjelpen åpnes.
8. Velg knappen **Oppdater** for konfigurasjon av Lifecycle Services-hjelpen.

    Det nye BPM-biblioteket skal vises, og det skal være aktivt.

9. Lukk siden.
10. Opprett et oppgaveopptak.
11. Når du er ferdig, velger **Lagre i Lifecycle Services**.

    ![Lagre i Lifecycle Services](media/task-guides.png)

12. Velg BPM-biblioteket og noden for å lagre oppgaveopptaket.

Følg denne fremgangsmåten for å spille av en oppgaveveiledningen på nytt fra LCS.

1. Start oppgaveopptakeren.
2. Velg **Åpne fra LCS**.
3. Velg biblioteket og BPM-noden som har den lagrede oppgaveveiledningen.
4. Åpne oppgaveveiledningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]