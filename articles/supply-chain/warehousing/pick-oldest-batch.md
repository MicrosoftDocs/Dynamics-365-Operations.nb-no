---
title: Plukke eldste parti på en mobil enhet
description: Dette emnet beskriver hvordan du definerer og bruker alternativene for å velge det eldste partiet fra en mobilenhet.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a592425ed28f591783ec45bdfd61574bb889557
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "320610"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Plukke eldste parti på en mobil enhet

[!include [banner](../includes/banner.md)]

Du kan få tilgang til konfigurasjonen **Plukk eldste parti** via en mobilenhetsmeny, og det gjør det mulig å tvinge eller instruere lagermedarbeidere til å plukke det eldste partiet på gjeldende sted.  

## <a name="where-it-applies"></a>Der det er aktuelt
Plukk eldste parti er konfigurert på menyelementer for mobilenhet, og påvirker plukkingen for partivarer under.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Hvordan du definerer konfigurasjonen for plukk eldste parti 
For varer som er angitt til å bruke eksisterende arbeid, kan **Plukk eldste parti** settes til **Ingen**, **Varsle**, eller **Fremtving** fra en mobilenhetsmeny.

**Ingen**: Arbeidere vil ikke motta meldinger og de kan plukke alle partier på plasseringen.

**Varsle** og **Fremtving**: En liste over partiene med den eldste utløpsdatoen vises over partikontrollen når arbeideren velger et parti. Hvis lokasjonen er nummerskiltkontrollert, vises en liste over lisensplater med den eldste batchen over nummerskiltkontrollen. 
-   **Varsle**: Hvis en arbeider velger et nummerskilt eller parti som ikke er i listen som vises, er kontrollen nedtonet, og det vises en advarsel om at det finnes et eldre parti å velge. For at arbeideren skal kunne fortsette arbeidet må han/hun velge samme nummerskilt eller parti på nytt.  
-   **Fremtving**: Arbeidere vil fortsette å motta meldingen om at det er et eldre parti som skal plukkes.
