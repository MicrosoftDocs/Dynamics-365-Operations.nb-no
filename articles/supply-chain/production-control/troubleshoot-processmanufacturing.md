---
title: Feilsøk prosessproduksjon
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med prosessproduksjon.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259728"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="42caa-103">Feilsøk prosessproduksjon</span><span class="sxs-lookup"><span data-stu-id="42caa-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="42caa-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med prosessproduksjon.</span><span class="sxs-lookup"><span data-stu-id="42caa-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="42caa-105">Når jeg bruker prosjektkortenheten til å rapportere et delvis antall i det siste prosjektet i en produksjonsordre, avsluttes alle de forrige prosjektene i den ordren som har statusen Pågår automatisk.</span><span class="sxs-lookup"><span data-stu-id="42caa-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="42caa-106">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="42caa-106">This behavior is by design.</span></span> <span data-ttu-id="42caa-107">På siden **Produksjonsordrestandarder** i fanen **Ferdigmeld** finnes det et alternativ som heter **Sluttmerk rute**.</span><span class="sxs-lookup"><span data-stu-id="42caa-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="42caa-108">Hvis dette emnet er satt til *Ja*, posteres en rutekortjournal når en arbeider bruker prosjektkortenheten eller prosjektkortterminalen til å rapportere den siste operasjonen.</span><span class="sxs-lookup"><span data-stu-id="42caa-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="42caa-109">Denne journalen markerer alle operasjoner som fullført, og avslutter alle produksjonsprosjektene.</span><span class="sxs-lookup"><span data-stu-id="42caa-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="42caa-110">Når **Sluttmerk rute**-alternativet er satt til *Ja*, vurderer ikke systemet prosjektstatusen som arbeideren valgte da vedkommende sist rapporterte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="42caa-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="42caa-111">Systemet vurderer heller ikke om arbeideren rapporterer et fullstendig eller delvis antall.</span><span class="sxs-lookup"><span data-stu-id="42caa-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="42caa-112">Når jeg prøver å foreta en lagerlukking, får jeg følgende advarsel: Ingen utførelse av beregning av backflush-etterkalkulering med en dato %1 som samsvarer med periodeslutt, er registrert.</span><span class="sxs-lookup"><span data-stu-id="42caa-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="42caa-113">Hvis du ikke bruker flyten for trimmet produksjons-kostnadsflyten i utgivelser før utgivelse 10.0.13, får du følgende feilaktige advarselsmeldinger under lagerlukking:</span><span class="sxs-lookup"><span data-stu-id="42caa-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="42caa-114">Du er i ferd med å utføre en lagerlukking med en dato %1.</span><span class="sxs-lookup"><span data-stu-id="42caa-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="42caa-115">Ingen kjøringer av beregning av backflush-etterkalkulering med en dato %1 som samsvarer med periodeslutt, er registrert.</span><span class="sxs-lookup"><span data-stu-id="42caa-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="42caa-116">Husk å kjøre en beregning av backflush-etterkalkulering med en dato for %1 som samsvarer med periodeslutt.</span><span class="sxs-lookup"><span data-stu-id="42caa-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="42caa-117">Verdien av lagerbeholdningene, solgte varers kost og avvik er kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.</span><span class="sxs-lookup"><span data-stu-id="42caa-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="42caa-118">Dette problemet er løst i utgivelsen 10.0.13 og nyere.</span><span class="sxs-lookup"><span data-stu-id="42caa-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="42caa-119">Hvis du vil ha mer informasjon, kan du se [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="42caa-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]