---
title: Operasjoner for avvik
description: Dette emnet beskriver hvordan du oppretter og bruker operasjoner for avvik.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9a6cc88b80f82d77edac0341cb6a3c0db4b42ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022210"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="63f63-103">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63f63-104">Dette emnet beskriver hvordan du oppretter og bruker operasjoner for avvik.</span><span class="sxs-lookup"><span data-stu-id="63f63-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="63f63-105">Du kan bruke **Operasjoner**-siden til å definere klassifiseringer av arbeidet som kan utføres for et godkjent avvik.</span><span class="sxs-lookup"><span data-stu-id="63f63-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="63f63-106">Når du tilordner en relatert operasjon til et avvik, kan du også gi detaljert informasjon, for eksempel informasjon om tilknyttede materialer, arbeidstimer og tillegg som kreves for å utføre operasjonen.</span><span class="sxs-lookup"><span data-stu-id="63f63-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="63f63-107">Denne informasjonen brukes til å beregne en estimert kostnad for operasjonen.</span><span class="sxs-lookup"><span data-stu-id="63f63-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="63f63-108">Den detaljerte informasjonen og de estimerte kostnadene er til referanse.</span><span class="sxs-lookup"><span data-stu-id="63f63-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="63f63-109">De relaterte operasjonene for kvalitet er annerledes enn operasjonene som kan defineres for en produksjonsrute.</span><span class="sxs-lookup"><span data-stu-id="63f63-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="63f63-110">Selv om du kan spore kostnader, tid og varene som brukes i en operasjon som er relatert til et avvik, er dataene du angir, bare til informasjon.</span><span class="sxs-lookup"><span data-stu-id="63f63-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="63f63-111">De er ikke automatisk integrert med økonomimodulen, underfinans for beholdning eller **Timeregistrering**-modulen.</span><span class="sxs-lookup"><span data-stu-id="63f63-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="63f63-112">Eksempler på operasjoner</span><span class="sxs-lookup"><span data-stu-id="63f63-112">Examples of operations</span></span>

<span data-ttu-id="63f63-113">Du jobber for et produksjonsfirma.</span><span class="sxs-lookup"><span data-stu-id="63f63-113">You work for a manufacturing company.</span></span> <span data-ttu-id="63f63-114">Et avvik ble opprettet og godkjent for varer som mislyktes i en kvalitetstest.</span><span class="sxs-lookup"><span data-stu-id="63f63-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="63f63-115">Det ble opprettet en korrigering for å angi at problemet var knyttet til dårlige lagre på en maskin.</span><span class="sxs-lookup"><span data-stu-id="63f63-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="63f63-116">Det kreves flere trinn for å erstatte lagrene, og ansvarsområdet for hver operasjon spores.</span><span class="sxs-lookup"><span data-stu-id="63f63-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="63f63-117">Dette kan for eksempel være nødvendig:</span><span class="sxs-lookup"><span data-stu-id="63f63-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="63f63-118">Produksjonslinjen stoppes og ryddingsrutinen utføres.</span><span class="sxs-lookup"><span data-stu-id="63f63-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="63f63-119">Vedlikeholdspersonalet erstatter lageret.</span><span class="sxs-lookup"><span data-stu-id="63f63-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="63f63-120">Kvalitetssikringspersonell kontrollerer maskinen før den slås på igjen.</span><span class="sxs-lookup"><span data-stu-id="63f63-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="63f63-121">I dette eksemplet kan følgende operasjoner opprettes for å representere arbeidet som må utføres:</span><span class="sxs-lookup"><span data-stu-id="63f63-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="63f63-122">Stopp produksjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="63f63-122">Stop the production line.</span></span>
- <span data-ttu-id="63f63-123">Rydd opp i produksjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="63f63-123">Clean out the production line.</span></span>
- <span data-ttu-id="63f63-124">Utfør maskinvedlikehold.</span><span class="sxs-lookup"><span data-stu-id="63f63-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="63f63-125">Inspiser maskinen.</span><span class="sxs-lookup"><span data-stu-id="63f63-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="63f63-126">Opprette en operasjon</span><span class="sxs-lookup"><span data-stu-id="63f63-126">Create an operation</span></span>

1. <span data-ttu-id="63f63-127">Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Operasjoner**.</span><span class="sxs-lookup"><span data-stu-id="63f63-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="63f63-128">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="63f63-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="63f63-129">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="63f63-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="63f63-130">**Operasjon** – Angi en unik ID eller et unikt navn for operasjonen.</span><span class="sxs-lookup"><span data-stu-id="63f63-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="63f63-131">**Beskrivelse** – Angi en detaljert beskrivelse av operasjonen.</span><span class="sxs-lookup"><span data-stu-id="63f63-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="63f63-132">**Type** – Hvis operasjonen bare kan brukes med avvik som er knyttet til en bestemt ordretype, velger du ordretypen (*Bestilling* eller *Salgsordre*).</span><span class="sxs-lookup"><span data-stu-id="63f63-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="63f63-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="63f63-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="63f63-134">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="63f63-134">Additional resources</span></span>

- [<span data-ttu-id="63f63-135">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="63f63-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="63f63-136">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="63f63-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="63f63-137">Opprette og behandle avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="63f63-138">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="63f63-139">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="63f63-140">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="63f63-141">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="63f63-142">Problemtyper for avvik</span><span class="sxs-lookup"><span data-stu-id="63f63-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="63f63-143">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="63f63-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
