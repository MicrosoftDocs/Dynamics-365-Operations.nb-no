---
title: Feilsøke analyserapporter
description: Denne artikkelen forklarer hva du gjør hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4e76f3b6231b6f307173fa176360daf775c8a7950bc4ab2f2162c768102c369
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717420"
---
# <a name="troubleshoot-analytic-reports"></a>Feilsøke analyserapporter

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