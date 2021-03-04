---
title: Feilsøke analyserapporter
description: Denne artikkelen forklarer hva du gjør hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419925"
---
# <a name="troubleshoot-analytic-reports"></a>Feilsøke analyserapporter

**Avgang**

Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.

**Årsak**

Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.

**Oppløsning**

Dette problemet kan bare være et spørsmål om tidsberegning. Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.

1. Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**. Du kan også bruke Søk og angi **Satsvise jobber**.
1. Finn **Distribuer mål**-jobben i listen.
1. Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.

![Satsvise jobber](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]