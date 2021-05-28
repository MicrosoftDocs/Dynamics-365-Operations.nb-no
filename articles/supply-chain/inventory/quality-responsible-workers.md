---
title: Arbeidere som er ansvarlige for å godkjenne avvik
description: Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021786"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="fb2c8-103">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb2c8-104">Dette emnet beskriver hvordan du konfigurerer arbeidere som er ansvarlige for godkjenning av avvik.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="fb2c8-105">Avvik må godkjennes før brukere kan begynne å angi detaljer som rettelser eller operasjoner.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="fb2c8-106">Før brukere kan godkjenne eller avvise avvik, må bruker-IDen (brukerposten) være knyttet til en arbeiderpost.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="fb2c8-107">Du kan velge å konfigurere arbeidere som er ansvarlige for kvalitet, og deretter tillate at én arbeider godkjenner arbeid på vegne av en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="fb2c8-108">Aktivere en bruker for behandling av avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="fb2c8-109">Før en bruker kan godkjenne eller avvise avvik, må du knytte brukerposten til en arbeiderpost.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="fb2c8-110">Godkjenningsfeltene kan deretter angis automatisk, og gjeldende bruker kan fylles ut automatisk for timeregistreringen.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="fb2c8-111">Før brukeren kan bruke merknader i dokumentet, må du også aktivere dokumenthåndtering i brukeralternativene deres.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="fb2c8-112">Gå til **Systemadministrasjon \> Brukere \> Brukere**.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="fb2c8-113">Finn og åpne brukeren som skal kunne godkjenne eller avvise avvik.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="fb2c8-114">Sett **Person**-feltet til navnet på arbeideren som er knyttet til den gjeldende brukerposten.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="fb2c8-115">Velg **Brukeralternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="fb2c8-116">På **Alternativer**-siden for den gjeldende brukerposten, i kategorien **Innstillinger**, setter du alternativet **Aktiver dokumentbehandling** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="fb2c8-117">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="fb2c8-118">Definere arbeidere som er ansvarlige for kvalitet</span><span class="sxs-lookup"><span data-stu-id="fb2c8-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="fb2c8-119">Gå til **Lagerstyring \> Oppsett \> Kvalitetskontroll \> Arbeidere som er ansvarlige for kvalitet**.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="fb2c8-120">Velg **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="fb2c8-121">Velg arbeideren som angir kvalitetsdata, i **Arbeider**-feltet.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="fb2c8-122">I feltet **Ansvarlig arbeider** velger du arbeideren som den valgte arbeideren angir arbeid på vegne av.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="fb2c8-123">Når avvikene opprettes og oppdateres, angis denne arbeideren som standard i **Arbeider**-felt.</span><span class="sxs-lookup"><span data-stu-id="fb2c8-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb2c8-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fb2c8-124">Additional resources</span></span>

- [<span data-ttu-id="fb2c8-125">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="fb2c8-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="fb2c8-126">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="fb2c8-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="fb2c8-127">Kvalitetsstyringstillegg</span><span class="sxs-lookup"><span data-stu-id="fb2c8-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="fb2c8-128">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="fb2c8-129">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="fb2c8-130">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="fb2c8-131">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="fb2c8-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="fb2c8-132">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="fb2c8-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
