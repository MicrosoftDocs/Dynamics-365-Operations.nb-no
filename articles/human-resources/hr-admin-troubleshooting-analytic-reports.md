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
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053545"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="83d53-103">Feilsøke analyserapporter</span><span class="sxs-lookup"><span data-stu-id="83d53-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83d53-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="83d53-104">**Issue**</span></span>

<span data-ttu-id="83d53-105">Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="83d53-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="83d53-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="83d53-106">**Cause**</span></span>

<span data-ttu-id="83d53-107">Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.</span><span class="sxs-lookup"><span data-stu-id="83d53-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="83d53-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="83d53-108">**Resolution**</span></span>

<span data-ttu-id="83d53-109">Dette problemet kan bare være et spørsmål om tidsberegning.</span><span class="sxs-lookup"><span data-stu-id="83d53-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="83d53-110">Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.</span><span class="sxs-lookup"><span data-stu-id="83d53-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="83d53-111">Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="83d53-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="83d53-112">Du kan også bruke Søk og angi **Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="83d53-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="83d53-113">Finn **Distribuer mål**-jobben i listen.</span><span class="sxs-lookup"><span data-stu-id="83d53-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="83d53-114">Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="83d53-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Satsvise jobber](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]