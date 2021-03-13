---
title: Feilsøke analyserapporter
description: Denne artikkelen forklarer hva du gjør hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113708"
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
