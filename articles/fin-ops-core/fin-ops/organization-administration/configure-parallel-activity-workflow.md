---
title: Konfigurere parallelle aktiviter i en arbeidsflyt
description: Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee559a092c4acd34a6df05e893bdbf4289099
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698321"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Konfigurere parallelle aktiviter i en arbeidsflyt

[!include [banner](../includes/banner.md)]

Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.

En parallell aktivitet består av grener i arbeidsflyten som kjører samtidig.

## <a name="name-a-parallel-activity"></a>Navngi en parallell aktivitet

Følg denne fremgangsmåten for å angi et navn for en parallell aktivitet.

1. Høyreklikk den parallelle aktiviteten, og klikk deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.
2. Klikk **Grunnleggende innstillinger** i ruten til venstre.
3. I feltet **Navn** angir du et unikt navn på den parallelle aktiviteten.
4. Klikk **Lukk**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurere grenene til en parallell aktivitet

Følg denne fremgangsmåten for å legge til og konfigurere grenene til denne parallelle aktiviteten.

1. Dobbeltklikk den parallelle aktiviteten for å vise grenene til den parallelle aktiviteten.
2. Hvis du vil legge til en gren, kan du dra **Gren**-elementet fra **Arbeidsflytelementer**-området til et innsettingspunkt på lerretet. Den følgende illustrasjonen viser et innsettingspunkt.

    ![Innsettingspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Rekkefølgen på grenene er ikke viktig fordi alle grenene til en parallell aktivitet kjøres samtidig.

3. Hvis du vil konfigurere hver gren, kan du se [Konfigurere parallelle avdelinger i en arbeidsflyt](configure-parallel-branch-workflow.md).
