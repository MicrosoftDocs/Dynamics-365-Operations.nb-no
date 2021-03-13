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
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="66fbe-103">Feilsøke analyserapporter</span><span class="sxs-lookup"><span data-stu-id="66fbe-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="66fbe-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="66fbe-104">**Issue**</span></span>

<span data-ttu-id="66fbe-105">Dataendringene til en kunde vises ikke i fanene **Analyse** i noen av kundens arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="66fbe-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="66fbe-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="66fbe-106">**Cause**</span></span>

<span data-ttu-id="66fbe-107">Som standard oppdateres Microsoft Power BI-rapporter hver fjerde time, i henhold til tidsplanen for den satsvise jobben Distribuer mål.</span><span class="sxs-lookup"><span data-stu-id="66fbe-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="66fbe-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="66fbe-108">**Resolution**</span></span>

<span data-ttu-id="66fbe-109">Dette problemet kan bare være et spørsmål om tidsberegning.</span><span class="sxs-lookup"><span data-stu-id="66fbe-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="66fbe-110">Følg denne fremgangsmåten for å starte den satsvise jobben og oppdatere analysearbeidsområdene.</span><span class="sxs-lookup"><span data-stu-id="66fbe-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="66fbe-111">Åpne siden **Satsvise jobber** på **Systemadministrasjon \> Koblinger \> Satsvise jobber \> Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="66fbe-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="66fbe-112">Du kan også bruke Søk og angi **Satsvise jobber**.</span><span class="sxs-lookup"><span data-stu-id="66fbe-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="66fbe-113">Finn **Distribuer mål**-jobben i listen.</span><span class="sxs-lookup"><span data-stu-id="66fbe-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="66fbe-114">Velg **Rediger** øverst på siden, og angi planlagt startdato/-klokkeslett til en verdi som vil oppdatere analysen slik at den er nærmere gjeldende tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="66fbe-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Satsvise jobber](media/batch-jobs.png)
