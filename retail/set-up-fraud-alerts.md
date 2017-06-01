---
title: Definere svindelvarsler
description: "Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles. Du kan definere spesifikke sperrekoder som skal brukes automatisk eller manuelt til å sette mistenkelige ordrer på vent."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7255f2b7e49f56a731d0e3745b4752091013668b
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-fraud-alerts"></a>Definere svindelvarsler

[!include[banner](includes/banner.md)]


Dette emnet forklarer hvordan du definerer regler for å varsle kundeservicerepresentanter om potensiell falsk informasjon når ordrer behandles. Du kan definere spesifikke sperrekoder som skal brukes automatisk eller manuelt til å sette mistenkelige ordrer på vent. 

Før du definerer og bruker svindelkontrollregler, må du aktivere svindelkontroll og definere de grunnleggende verdiene for svindelkontroll i telefonsenterparameterne. Det finnes to typer svindelregler:

-   **Statiske regler** bruker en bestemt verdi, for eksempel et telefonnummer som har blitt svartelistet.
-   **Dynamiske regler** kan bestå av variabler og betingelser.

Før du oppretter en dynamisk regel, må du opprette variablene og betingelsene som definerer hvem regelen gjelder for, og når regelen skal brukes. La oss si at du vil opprette en regel som krever at alle salgsordrer som kunde 1202 legger inn som er verdt 1 000,00 eller mer, må settes på vent til kundebetalingen kan bekreftes. I dette tilfellet er variablene kunde 1202 og en ordretotal på 1 000,00. Betingelsen angir at når kunde 1202 plasserer en ordre, og totalbeløpet for ordren er lik eller mer enn 1 000,00, må salgsordren settes på vent til kundebetalingen kan bekreftes.




