---
title: Legge til feil i arbeidsordre
description: Dette emnet beskriver hvordan du legger til feilregistreringer i arbeidsordrer i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
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
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 489add5befe3660ad49e238b659bc8adbe1418a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263764"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="db898-103">Legge til feil i arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="db898-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="db898-104">Du kan legge til feil som er definert i feilutformingen, i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="db898-104">You can add faults that were set up in the fault designer to a work order.</span></span> <span data-ttu-id="db898-105">Én eller flere feilposter må knyttes til aktivatyper som brukes for aktivumet som velges i arbeidsordren.</span><span class="sxs-lookup"><span data-stu-id="db898-105">One or more fault records must be connected to the asset types that are used for the asset that is selected in the work order.</span></span> <span data-ttu-id="db898-106">Hvis du vil ha mer informasjon om det generelle oppsettet for vurdering, kan du se [Feilstyring](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="db898-106">For more information about the setup, see [Fault management](../setup-for-work-orders/fault-management.md).</span></span>

1. <span data-ttu-id="db898-107">Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="db898-107">Select **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="db898-108">Velg arbeidsordren det skal utføres en feilregistrering på, og deretter går du til handlingsruten, fanen **Arbeidsordre**, gruppen **Aktiva** og velger **Aktivumfeil**.</span><span class="sxs-lookup"><span data-stu-id="db898-108">Select the work order to make a fault registration on, and then, on the Action Pane, on the **Work order** tab, in the **Asset** group, select **Asset fault**.</span></span>

3. <span data-ttu-id="db898-109">Velg **Legg til linje** på hurtigfanen **Symptomer**.</span><span class="sxs-lookup"><span data-stu-id="db898-109">On the **Symptoms** FastTab, select **Add line**.</span></span> <span data-ttu-id="db898-110">Et sekvensielt feilnummer settes automatisk inn i **Feil**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db898-110">A sequential fault number is automatically entered in the **Fault** field.</span></span>

4. <span data-ttu-id="db898-111">Velg det relevante symptomet i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db898-111">In the **Fault symptom** field, select the relevant symptom.</span></span>

5. <span data-ttu-id="db898-112">Velg de aktuelle verdiene i feltene **Feilområde** og **Feiltype**.</span><span class="sxs-lookup"><span data-stu-id="db898-112">In the **Fault area** and **Fault type** fields, select the appropriate values.</span></span>

6. <span data-ttu-id="db898-113">Den gjeldende datoen settes automatisk inn i **Feildato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="db898-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="db898-114">Du kan velge en annen dato etter behov.</span><span class="sxs-lookup"><span data-stu-id="db898-114">You can select a different date as you require.</span></span>

7. <span data-ttu-id="db898-115">I hurtigfanen **Årsaker til valgte symptom** legger du til en linje som beskriver årsaken til problemet.</span><span class="sxs-lookup"><span data-stu-id="db898-115">On the **Causes for selected symptom** FastTab, add a line to describe the cause of the issue.</span></span>

8. <span data-ttu-id="db898-116">I hurtigfanen **Løsninger på valgte symptom** legger du til en linje som beskriver en mulig løsning på problemet.</span><span class="sxs-lookup"><span data-stu-id="db898-116">On the **Remedies for selected symptom** FastTab, add a line to describe a possible solution to the issue.</span></span>

9. <span data-ttu-id="db898-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="db898-117">Select **Save**.</span></span>

<span data-ttu-id="db898-118">Illustrasjonen nedenfor viser et eksempel på en feilregistrering.</span><span class="sxs-lookup"><span data-stu-id="db898-118">The illustration below shows an example of a fault registration.</span></span>

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="db898-120">Vis aktivafeil</span><span class="sxs-lookup"><span data-stu-id="db898-120">View asset faults</span></span>

<span data-ttu-id="db898-121">I listen **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva.</span><span class="sxs-lookup"><span data-stu-id="db898-121">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="db898-122">På listesiden **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva.</span><span class="sxs-lookup"><span data-stu-id="db898-122">On the **Asset faults** list page, you can get an overview of all faults that have been registered on assets.</span></span> <span data-ttu-id="db898-123">Velg **Aktivastyring** > **Forespørsler** > **Aktivafeil** > **Aktivafeil** for å åpne listen.</span><span class="sxs-lookup"><span data-stu-id="db898-123">To open the page, select **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="db898-124">Skriv ut rapport for aktivumfeil</span><span class="sxs-lookup"><span data-stu-id="db898-124">Print asset fault report</span></span>

<span data-ttu-id="db898-125">Fra listesiden **Alle aktiva** kan du skrive ut en rapport om aktivumfeil som viser alle feilregistreringer, i tillegg til en grafisk oversikt over feilstatistikk.</span><span class="sxs-lookup"><span data-stu-id="db898-125">From the **All assets** list page, you can print an asset fault report that shows all fault registrations and a graphical overview of fault statistics.</span></span>

1. <span data-ttu-id="db898-126">Velg **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="db898-126">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="db898-127">Velg aktivumet det skal skrives ut en rapport for.</span><span class="sxs-lookup"><span data-stu-id="db898-127">Select the asset to print a fault report for.</span></span>

3. <span data-ttu-id="db898-128">I handlingsruten velger du fanen **Generelt** i gruppen **Rapporter** og deretter **Aktivafeil**.</span><span class="sxs-lookup"><span data-stu-id="db898-128">On the Action Pane, on the **General** tab, in the **Reports** group, select **Asset fault**.</span></span>

4. <span data-ttu-id="db898-129">Sett inn en bestemt periode, eller velg en feiltype.</span><span class="sxs-lookup"><span data-stu-id="db898-129">Enter a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="db898-130">Velg **OK** for å skrive ut rapporten.</span><span class="sxs-lookup"><span data-stu-id="db898-130">Select **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="db898-131">For å skrive ut en feilrapport for flere aktiva eller aktivatyper, velg **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivafeil**.</span><span class="sxs-lookup"><span data-stu-id="db898-131">To print a fault report for several assets or asset types, select **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]