---
title: Konserninterne utgifter
description: En arbeidstaker som er ansatt av en juridisk enhet i en organisasjon kan utføre arbeid for en annen juridisk enhet i samme organisasjon. I denne situasjonen kan du bruke den konserninterne kostnadsfunksjonen til å tildele arbeidstakers utgifter til den juridiske enheten som arbeidet ble utført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390890"
---
# <a name="intercompany-expenses"></a>Konserninterne utgifter

[!include [banner](../includes/banner.md)]

En arbeidstaker som er ansatt av en juridisk enhet i en organisasjon kan utføre arbeid for en annen juridisk enhet i samme organisasjon. I denne situasjonen kan du bruke den konserninterne kostnadsfunksjonen til å tildele arbeidstakers utgifter til den juridiske enheten som arbeidet ble utført for. Den juridiske enheten som benytter arbeidstakeren kalles den utlånende juridiske enheten. Den juridiske enheten som påføres utgifter for arbeidstakeren, kalles den lånende juridiske enheten. 

Før en arbeidstaker kan opprette og sende utgifter for arbeid som utføres for en annen juridisk enhet, i den utlånende juridiske enheten, gå til siden for **Administrer kostnadsparametere** og velg alternativet **Tillatt konserninterne kostnadslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Avgiftspostering for konserninterne utgifter

[!include [banner](../includes/banner.md)]

Hvis du vil bruke mva-grupper som er tilknyttet den juridiske enheten som låner ut (kilde), i stedet for den juridiske enheten som låner (mål) i reiseregningsrapporten, må du konfigurere denne i dette mva-oppsettet for økonomimodulen. Når parameteren for økonomimodulen, **Juridisk enhet for konsernintern mva-postering** er satt til **Kilde** og **Bruk avgiftsregler for merverdiavgift** er satt til **Nei**, brukes mva-kombinasjonen for den juridiske enheten som låner ut. Når den samme parameteren er satt til **Mål**, brukes mva-kombinasjonen for den juridiske enheten som låner. Når det gjelder juridiske enheter i USA når parameteren er satt til **Kilde**, må også feltet **Innkommende merverdiavgift** også være konfigurert på siden **Finansposteringsgrupper**. Regnskapsmotoren bruker informasjonen fra dette feltet for mva-relatert regnskapspost.   
Virkemåten er konsekvent for utgiftslinjer som er postert med eller uten et prosjekt.  
