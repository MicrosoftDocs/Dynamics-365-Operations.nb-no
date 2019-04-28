---
title: Analyserapporter blir ikke oppdatert
description: Dette emnet forklarer hva du gjør hvis en kundes dataendringer ikke vises i noen av kundens arbeidsområder.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "857459"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="86724-103">Analyserapporter blir ikke oppdatert</span><span class="sxs-lookup"><span data-stu-id="86724-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86724-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="86724-104">**Issue**</span></span>

<span data-ttu-id="86724-105">Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="86724-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="86724-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="86724-106">**Cause**</span></span>

<span data-ttu-id="86724-107">Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.</span><span class="sxs-lookup"><span data-stu-id="86724-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="86724-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="86724-108">**Resolution**</span></span>

<span data-ttu-id="86724-109">Dette problemet kan bare være et spørsmål om tidsberegning.</span><span class="sxs-lookup"><span data-stu-id="86724-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="86724-110">Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.</span><span class="sxs-lookup"><span data-stu-id="86724-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="86724-111">Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="86724-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="86724-112">Du kan også bruke Søk og angi **Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="86724-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="86724-113">Finn **Distribuer mål**-jobben i listen.</span><span class="sxs-lookup"><span data-stu-id="86724-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="86724-114">Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="86724-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Satsvise jobber](media/batch-jobs.png)
