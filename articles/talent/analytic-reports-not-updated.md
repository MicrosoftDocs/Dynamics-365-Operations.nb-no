---
title: Analyserapporter blir ikke oppdatert
description: "Dette emnet forklarer hva du gjør hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>Analyserapporter blir ikke oppdatert

[!include [banner](includes/banner.md)]

**Utstede**

Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.

**Årsak**

Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.

**Oppløsning**

Dette problemet kan bare være et spørsmål om tidsberegning. Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.

1. Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**. Du kan også bruke Søk og angi **Satsvise jobber**.
1. Finn **Distribuer mål**-jobben i listen.
1. Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.

![Satsvise jobber](media/batch-jobs.png)
