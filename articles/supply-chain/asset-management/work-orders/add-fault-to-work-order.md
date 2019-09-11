---
title: Legge til feil i arbeidsordre
description: Dette emnet beskriver hvordan du legger til feilregistreringer i arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875824"
---
# <a name="add-fault-to-work-order"></a><span data-ttu-id="272c2-103">Legge til feil i arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="272c2-103">Add fault to work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="272c2-104">Du kan legge til feil som er definert i feilutformingen, i en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="272c2-104">You can add faults set up in the fault designer to a work order.</span></span> <span data-ttu-id="272c2-105">Anleggsmiddelet som er valgt i arbeidsordren, må inneholde anleggsmiddeltyper som har én eller flere feilposter tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="272c2-105">The asset selected in the work order must contain asset types that have one or more fault records connected to it.</span></span> <span data-ttu-id="272c2-106">Les mer om oppsett i delen [Feilstyring](../setup-for-work-orders/fault-management.md).</span><span class="sxs-lookup"><span data-stu-id="272c2-106">Read more about setup in the [Fault management](../setup-for-work-orders/fault-management.md) section.</span></span>

1. <span data-ttu-id="272c2-107">Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.</span><span class="sxs-lookup"><span data-stu-id="272c2-107">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="272c2-108">I listen velger du arbeidsordren du vil utføre en feilregistrering for, og klikker på **Aktivumfeil**.</span><span class="sxs-lookup"><span data-stu-id="272c2-108">In the list, select the work order on which you want to make a fault registration and click **Asset fault**.</span></span>

3. <span data-ttu-id="272c2-109">Klikk på **Legg til linje** på hurtigfanen **Symptomer**.</span><span class="sxs-lookup"><span data-stu-id="272c2-109">On the **Symptoms** FastTab, click **Add line**.</span></span> <span data-ttu-id="272c2-110">Et sekvensielt feilnummer settes automatisk inn i **Feil**-feltet.</span><span class="sxs-lookup"><span data-stu-id="272c2-110">A sequential fault number is automatically inserted in the **Fault** field.</span></span>

4. <span data-ttu-id="272c2-111">Velg det relevante symptomet i **Feilsymptom**-feltet.</span><span class="sxs-lookup"><span data-stu-id="272c2-111">Select the relevant symptom in the **Fault symptom** field.</span></span>

5. <span data-ttu-id="272c2-112">Velg **Feilområde** og **Feiltype**.</span><span class="sxs-lookup"><span data-stu-id="272c2-112">Select **Fault area** and **Fault type**.</span></span>

6. <span data-ttu-id="272c2-113">Den gjeldende datoen settes automatisk inn i **Feildato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="272c2-113">In the **Fault date** field, the current date is automatically inserted.</span></span> <span data-ttu-id="272c2-114">Hvis det er nødvendig, kan du velge en annen dato.</span><span class="sxs-lookup"><span data-stu-id="272c2-114">You can select another date, if necessary.</span></span>

7. <span data-ttu-id="272c2-115">I hurtigfanen **Årsaker til valgte symptom** legger du til en linje som beskriver årsaken til problemet.</span><span class="sxs-lookup"><span data-stu-id="272c2-115">On the **Causes for selected symptom** FastTab, add a line describing the cause of the problem.</span></span>

8. <span data-ttu-id="272c2-116">I hurtigfanen **Løsninger på valgte symptom** legger du til en linje som beskriver en mulig løsning problemet.</span><span class="sxs-lookup"><span data-stu-id="272c2-116">On the **Remedies for selected symptom** FastTab, add a line describing a possible solution to the problem.</span></span>

9. <span data-ttu-id="272c2-117">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="272c2-117">Click **Save**.</span></span>

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a><span data-ttu-id="272c2-119">Vis aktivafeil</span><span class="sxs-lookup"><span data-stu-id="272c2-119">View asset faults</span></span>

<span data-ttu-id="272c2-120">I listen **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva.</span><span class="sxs-lookup"><span data-stu-id="272c2-120">In the **Asset faults** list, you can get an overview of all faults registered on assets.</span></span>

<span data-ttu-id="272c2-121">Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Aktivafeil** for å åpne listen.</span><span class="sxs-lookup"><span data-stu-id="272c2-121">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults** to open the list.</span></span>


## <a name="print-asset-fault-report"></a><span data-ttu-id="272c2-122">Skriv ut rapport for aktivumfeil</span><span class="sxs-lookup"><span data-stu-id="272c2-122">Print asset fault report</span></span>

<span data-ttu-id="272c2-123">Fra listesiden **Alle aktiva** kan du skrive ut en rapport om aktivumfeil som viser alle feilregistreringer, i tillegg til en grafisk oversikt over feilstatistikk.</span><span class="sxs-lookup"><span data-stu-id="272c2-123">From the **All assets** list page, you can print an asset fault report displaying all fault registrations as well as a graphic overview of fault statistics.</span></span>

1. <span data-ttu-id="272c2-124">Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.</span><span class="sxs-lookup"><span data-stu-id="272c2-124">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="272c2-125">I listen **Aktiva** velger du aktivumet du vil skrive ut en feilrapport for.</span><span class="sxs-lookup"><span data-stu-id="272c2-125">In the **Assets** list, select the asset for which you want to print a fault report.</span></span>

3. <span data-ttu-id="272c2-126">I fanen **Generelt** > **delen Rapporter** klikker du **Aktivumfeil**.</span><span class="sxs-lookup"><span data-stu-id="272c2-126">On the **General** tab > **Reports section**, click **Asset fault**.</span></span>

4. <span data-ttu-id="272c2-127">Sett inn en bestemt periode, eller velg en feiltype.</span><span class="sxs-lookup"><span data-stu-id="272c2-127">Insert a specific period, or select a fault type.</span></span>

5. <span data-ttu-id="272c2-128">Velg **OK** for å skrive ut rapporten.</span><span class="sxs-lookup"><span data-stu-id="272c2-128">Click **OK** to print the report.</span></span>

>[!NOTE]
><span data-ttu-id="272c2-129">Du kan også skrive ut en feilrapport for flere aktiva eller aktivatyper ved å klikke **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivafeil**.</span><span class="sxs-lookup"><span data-stu-id="272c2-129">You can also print a fault report for several assets or asset types by clicking **Asset management** > **Reports** > **Assets** > **Asset fault**.</span></span>

