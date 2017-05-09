---
title: Konfigurere en parallell aktivitet i en arbeidsflyt
description: "Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurere en parallell aktivitet i en arbeidsflyt

Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.

En parallell aktivitet består av grener i arbeidsflyten som kjører samtidig.

## <a name="name-a-parallel-activity"></a>Navngi en parallell aktivitet
Følg denne fremgangsmåten for å angi et navn for en parallell aktivitet.
1.  Høyreklikk den parallelle aktiviteten, og klikk deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.
2.  Klikk **Grunnleggende innstillinger** i ruten til venstre.
3.  I feltet **Navn** angir du et unikt navn på den parallelle aktiviteten.
4.  Klikk **Lukk**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurere grenene til en parallell aktivitet
Følg denne fremgangsmåten for å legge til og konfigurere grenene til denne parallelle aktiviteten.
1.  Dobbeltklikk den parallelle aktiviteten for å vise grenene til den parallelle aktiviteten.
2.  Hvis du vil legge til en gren, kan du dra **Gren**-elementet fra **Arbeidsflytelementer**-området til et innsettingspunkt på lerretet. Den følgende illustrasjonen viser et innsettingspunkt. ![Innsettingspunkt](./media/workflow_insertionpoint.gif)
    | **Obs! **                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Rekkefølgen på grenene er ikke viktig fordi alle grenene til en parallell aktivitet kjøres samtidig. |

3.  Hvis du vil konfigurere hver gren, kan du se [Konfigurere en parallell gren](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).




