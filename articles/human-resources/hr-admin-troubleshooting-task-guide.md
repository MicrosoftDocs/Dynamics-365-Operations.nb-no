---
title: Lagre oppgaveveiledninger i LCS og spille dem av på nytt
description: Dette emnet forklarer hvordan du lagrer oppgaveveiledninger til Microsoft Dynamics Lifecycle Services (LCS) og deretter spiller dem av på nytt.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fad014590abebf159b71227a44eb8df60bf05e
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416887"
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

    ![Lagre i Lifecycle Services.](media/task-guides.png)

12. Velg BPM-biblioteket og noden for å lagre oppgaveopptaket.

Følg denne fremgangsmåten for å spille av en oppgaveveiledningen på nytt fra LCS.

1. Start oppgaveopptakeren.
2. Velg **Åpne fra LCS**.
3. Velg biblioteket og BPM-noden som har den lagrede oppgaveveiledningen.
4. Åpne oppgaveveiledningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
