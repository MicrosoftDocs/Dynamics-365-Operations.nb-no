---
title: Fordelingsarbeidsordre
description: Dette emnet forklarer hvordan du fordeler arbeidsordrer i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b4b05dfe351bb61dc47c9c2bfe30831ab7b0a16
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016862"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="036d3-103">Fordelingsarbeidsordre</span><span class="sxs-lookup"><span data-stu-id="036d3-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="036d3-104">Du kan planlegge én arbeidsordre eller arbeidsordrejobber til én arbeider ved hjelp av **fordeling**-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="036d3-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="036d3-105">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="036d3-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="036d3-106">Velg arbeidsordren i listen.</span><span class="sxs-lookup"><span data-stu-id="036d3-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="036d3-107">Gå til fanen **Generelt**, og klikk på **Fordeling**.</span><span class="sxs-lookup"><span data-stu-id="036d3-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="036d3-108">I dialogboksen **Planlegg arbeidsordre** velger du arbeideren i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="036d3-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="036d3-109">I feltet **Planlegg timer** kan du sette inn forventede arbeidstimer i tilfelle forventede arbeidstimer avviker fra prognosetimer.</span><span class="sxs-lookup"><span data-stu-id="036d3-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="036d3-110">I **Planlagt start** -feltet kan du redigere startdato og -klokkeslett om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="036d3-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="036d3-111">Hvis planleggingsprosessen skal observere kapasitetsbegrensninger for ressurser som allerede er planlagt for andre jobber, må du kontrollere at veksleknappene for **Aktivum**, **Verktøy** og **Arbeider** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="036d3-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="036d3-112">Hvis du vil ha detaljert informasjon om planleggingsprosessen, velger du **Ja** på **Detaljert**-veksleknappen.</span><span class="sxs-lookup"><span data-stu-id="036d3-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="036d3-113">Dette betyr at detaljert informasjon om de beregnede resultatene for arbeidsordren vises i informasjonsloggen.</span><span class="sxs-lookup"><span data-stu-id="036d3-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="036d3-114">Velg **Ja** på veksleknappen **Ignorer tidsplan** for å ignorere lukkede dager i kalenderen (gjelder for aktiva, arbeider og verktøy).</span><span class="sxs-lookup"><span data-stu-id="036d3-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="036d3-115">Velg **Ja** på veksleknappen **Ignorer planlagt kjøring** for å ignorere begrensninger som kan ha blitt valgt for arbeidsordren angående planlegging.</span><span class="sxs-lookup"><span data-stu-id="036d3-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="036d3-116">Se delen [Planlagt kjøring](../setup-for-work-orders/scheduled-execution.md) hvis du vil ha informasjon om oppsett av planlagt kjøring.</span><span class="sxs-lookup"><span data-stu-id="036d3-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="036d3-117">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="036d3-117">Click **OK**.</span></span> <span data-ttu-id="036d3-118">Livssyklustilstanden for arbeidsordren oppdateres automatisk til livssyklustilstanden **Planlagt** som er angitt i **Aktivastyring** > **Oppsett** > **Arbeidsordrer** > **Livssyklusmodeller**.</span><span class="sxs-lookup"><span data-stu-id="036d3-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="036d3-119">Figuren nedenfor viser et eksempel på fordelingsvalg i dialogboksen **Planlegge arbeidsordre**.</span><span class="sxs-lookup"><span data-stu-id="036d3-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Figur 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="036d3-121">Hvis du vil slette tidsplanen for en arbeidsordre, velger du arbeidsordren i **Alle arbeidsordrer**, og deretter klikker du på **Slett tidsplan** i fanen **Generelt**. Husk å oppdatere livssyklustilstanden for arbeidsordren manuelt hvis du sletter tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="036d3-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

