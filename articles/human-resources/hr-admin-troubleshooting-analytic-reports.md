---
title: Feilsøke analyserapporter
description: Denne artikkelen forklarer hvordan du feilsøker og diagnostiserer problemer hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6ae8931679feb2103172eb1a21649734acd995
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902234"
---
# <a name="troubleshoot-analytic-reports"></a>Feilsøke analyserapporter


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Avgang**

Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.

**Årsak**

Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.

**Oppløsning**

Dette problemet kan bare være et spørsmål om tidsberegning. Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.

1. Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**. Du kan også bruke Søk og angi **Satsvise jobber**.
1. Finn **Distribuer mål**-jobben i listen.
1. Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.

![Satsvise jobber.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
