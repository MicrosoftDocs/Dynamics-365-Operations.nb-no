---
title: Definer årsakskoder
description: Dynamics 365 Human Resources bruker årsaks koder til å forklare hvorfor en ansatts fordeler blir endret.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468401"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="a6b84-103">Definer årsakskoder</span><span class="sxs-lookup"><span data-stu-id="a6b84-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a6b84-104">Dynamics 365 Human Resources bruker årsaks koder til å forklare hvorfor en ansatts fordeler blir endret.</span><span class="sxs-lookup"><span data-stu-id="a6b84-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="a6b84-105">Per januar 2021 migrerer årsakskoder til arbeidsområdet for **Personaladministrasjon** i stedet for arbeidsområdet for **Fordelsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="a6b84-106">Hvis du vil ha mer informasjon, kan du se [Migrere årsakskoder manuelt til Personaladministrasjon](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="a6b84-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="a6b84-107">Opprette årsakskoder</span><span class="sxs-lookup"><span data-stu-id="a6b84-107">Create reason codes</span></span>

1. <span data-ttu-id="a6b84-108">I arbeidsområdet **Personaladministrasjon** (eller **Fordelsbehandling** hvis årsakskodene ennå ikke er migrert), velger du **Koblinger**, og deretter velger du **Årsakskoder**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="a6b84-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-109">Select **New**.</span></span>

3. <span data-ttu-id="a6b84-110">Angi verdier for de følgende feltene:</span><span class="sxs-lookup"><span data-stu-id="a6b84-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a6b84-111">Felt</span><span class="sxs-lookup"><span data-stu-id="a6b84-111">Field</span></span> | <span data-ttu-id="a6b84-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a6b84-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a6b84-113">**Årsakskode**</span><span class="sxs-lookup"><span data-stu-id="a6b84-113">**Reason code**</span></span> | <span data-ttu-id="a6b84-114">Et unikt navn som identifiserer årsaken til at en ansatt ville endre en fordelsplanregistrering.</span><span class="sxs-lookup"><span data-stu-id="a6b84-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="a6b84-115">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="a6b84-115">**Description**</span></span> | <span data-ttu-id="a6b84-116">En beskrivelse av årsakskoden.</span><span class="sxs-lookup"><span data-stu-id="a6b84-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="a6b84-117">Under **Gjeldende scenarier** angir du **Fordelsbehandling** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="a6b84-118">(Gjelder ikke hvis årsakskodene enda ikke er migrert til **Personaladministrasjon**-arbeidsområdet.)</span><span class="sxs-lookup"><span data-stu-id="a6b84-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="a6b84-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="a6b84-120">Migrere årsakskoder manuelt til Personaladministrasjon</span><span class="sxs-lookup"><span data-stu-id="a6b84-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="a6b84-121">I januar 2021 migrerer årsakskoder til arbeidsområdet for **Personaladministrasjon** i stedet for arbeidsområdet for **Fordelsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="a6b84-122">De fleste årsakskodedata migreres automatisk i miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="a6b84-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="a6b84-123">Det kan hende at enkelte årsakskodedata ikke migreres.</span><span class="sxs-lookup"><span data-stu-id="a6b84-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="a6b84-124">Årsakskoder har for eksempel nå en maksimumsgrense på 15 tegn, slik at alle årsakskoder som er lengre enn 15 tegn, ikke migrerer automatisk.</span><span class="sxs-lookup"><span data-stu-id="a6b84-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="a6b84-125">Du vil se et banner på **Koblinger**-siden i arbeidsområdet **Fordelsadministrasjon** som informerer deg om migrering og om årsakskoder ikke migreres.</span><span class="sxs-lookup"><span data-stu-id="a6b84-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="a6b84-126">Velg **Årsakskoder** for å få detaljer om migreringsstatus.</span><span class="sxs-lookup"><span data-stu-id="a6b84-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="a6b84-127">[![Årsakskoder](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="a6b84-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="a6b84-128">Velg en årsakskode som ikke kan migreres.</span><span class="sxs-lookup"><span data-stu-id="a6b84-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="a6b84-129">[![Årsakskode for migreringsstatus](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="a6b84-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="a6b84-130">Velg **Migrer årsakskode**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="a6b84-131">[![Overfør årsakskode](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="a6b84-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="a6b84-132">I ruten **Migrering av fordelsårsakskode** har du to alternativer for tilordning av en årsakskode for Personaladministrasjon:</span><span class="sxs-lookup"><span data-stu-id="a6b84-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="a6b84-133">Hvis du vil bruke en eksisterende årsakskode i Personaladministrasjon, velger du en fra rullegardinlisten **Bruk eksisterende årsakskode**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="a6b84-134">Du kan bare bruke en eksisterende årsakskode i Personaladministrasjon hvis en annen årsakskode for fordelsadministrasjon ikke allerede har migrert til den.</span><span class="sxs-lookup"><span data-stu-id="a6b84-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="a6b84-135">Hvis du vil opprette en ny årsakskode i Personaladministrasjon, angir du en ny i **Ny årsakskode**, og deretter skriver inn en beskrivelse i **Ny beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="a6b84-136">[![Tilordne til en årsakskode for personaladministrasjon](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="a6b84-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="a6b84-137">Etter at årsakskoder er migrert til Personaladministrasjon, blir alternativet for å bruke dem i Fordelsbehandling automatisk satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a6b84-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="a6b84-138">[![Bruke årsakskode i Fordelsbehandling](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="a6b84-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]