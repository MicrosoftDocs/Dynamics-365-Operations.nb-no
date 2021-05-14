---
title: Arbeidere som er ansvarlige for å godkjenne avvik
description: Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956777"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="c5361-103">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5361-104">Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.</span><span class="sxs-lookup"><span data-stu-id="c5361-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="c5361-105">Avvik må godkjennes før brukere kan begynne å angi detaljer som rettelser eller operasjoner.</span><span class="sxs-lookup"><span data-stu-id="c5361-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="c5361-106">Før brukere kan godkjenne eller avvise avvik, må bruker-IDen (brukerposten) være knyttet til en arbeiderpost.</span><span class="sxs-lookup"><span data-stu-id="c5361-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="c5361-107">Du kan velge å konfigurere arbeidere som er ansvarlige for kvalitet, og deretter tillate at én arbeider godkjenner arbeid på vegne av en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="c5361-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="c5361-108">Aktivere en bruker for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="c5361-109">Før en bruker kan godkjenne eller avvise avvik, må du knytte brukerposten til en arbeiderpost.</span><span class="sxs-lookup"><span data-stu-id="c5361-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="c5361-110">Godkjenningsfeltene kan deretter angis automatisk, og gjeldende bruker kan fylles ut automatisk for timeregistreringen.</span><span class="sxs-lookup"><span data-stu-id="c5361-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="c5361-111">Før brukeren kan bruke merknader i dokumentet, må du også aktivere dokumenthåndtering i brukeralternativene deres.</span><span class="sxs-lookup"><span data-stu-id="c5361-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="c5361-112">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="c5361-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="c5361-113">Finn og åpne brukeren som skal kunne godkjenne eller avvise avvik.</span><span class="sxs-lookup"><span data-stu-id="c5361-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="c5361-114">Sett **Person**-feltet til navnet på arbeideren som er knyttet til den gjeldende brukerposten.</span><span class="sxs-lookup"><span data-stu-id="c5361-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="c5361-115">Velg **Brukeralternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c5361-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="c5361-116">På **Alternativer**-siden for den gjeldende brukerposten, i kategorien **Innstillinger**, setter du alternativet **Aktiver dokumentbehandling** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c5361-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="c5361-117">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="c5361-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="c5361-118">Definere arbeidere som er ansvarlige for kvalitet</span><span class="sxs-lookup"><span data-stu-id="c5361-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="c5361-119">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Arbeidere som er ansvarlige for kvalitet**.</span><span class="sxs-lookup"><span data-stu-id="c5361-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="c5361-120">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c5361-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="c5361-121">Velg arbeideren som angir kvalitetsdata, i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c5361-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="c5361-122">I feltet **Ansvarlig arbeider** velger du arbeideren som den valgte arbeideren angir arbeid på vegne av.</span><span class="sxs-lookup"><span data-stu-id="c5361-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="c5361-123">Når avvikene opprettes og oppdateres, angis denne arbeideren som standard i **Arbeider**-felt.</span><span class="sxs-lookup"><span data-stu-id="c5361-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5361-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c5361-124">Additional resources</span></span>

- [<span data-ttu-id="c5361-125">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="c5361-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="c5361-126">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="c5361-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="c5361-127">Kvalitetsstyringstillegg</span><span class="sxs-lookup"><span data-stu-id="c5361-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="c5361-128">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="c5361-129">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="c5361-130">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="c5361-131">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="c5361-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="c5361-132">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="c5361-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
