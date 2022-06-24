---
title: Plukk eldste parti på en mobilenhet
description: Denne artikkelen beskriver hvordan du definerer og bruker alternativene for å velge det eldste partiet fra en mobilenhet.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885645"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]