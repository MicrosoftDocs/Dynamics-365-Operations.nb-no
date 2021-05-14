---
title: Problemtyper for avvik
description: Dette emnet beskriver hvordan du oppretter og bruker problemtyper for avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956779"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="bfb60-103">Problemtyper for avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfb60-104">Dette emnet beskriver hvordan du oppretter og bruker problemtyper for avvik.</span><span class="sxs-lookup"><span data-stu-id="bfb60-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="bfb60-105">Du bruker **Problemtyper**-siden til å definere en klassifisering av kvalitetsproblemer som kan oppstå for de ulike avvikstypene.</span><span class="sxs-lookup"><span data-stu-id="bfb60-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="bfb60-106">For hver problemtype du oppretter må du angi avvikstypene som problemtypen kan brukes med.</span><span class="sxs-lookup"><span data-stu-id="bfb60-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="bfb60-107">Du kan definere følgende avvikstyper:</span><span class="sxs-lookup"><span data-stu-id="bfb60-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="bfb60-108">**Intern**– Avvik av denne typen er knyttet til lagerbeholdning (for eksempel kvalitetsordrer eller karanteneordrer).</span><span class="sxs-lookup"><span data-stu-id="bfb60-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="bfb60-109">**Kunde** – Avvik av denne typen er knyttet til salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="bfb60-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="bfb60-110">**Leverandør** – Avvik av denne typen er knyttet til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="bfb60-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="bfb60-111">**Tjenesteforespørsel** – Avvik av denne typen er knyttet til serviceordrer.</span><span class="sxs-lookup"><span data-stu-id="bfb60-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="bfb60-112">**Produksjon** – Avvik av denne typen er knyttet til parti- eller produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="bfb60-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="bfb60-113">**Koproduktproduksjon** – Avvik av denne typen er knyttet til partiordrer for koprodukter.</span><span class="sxs-lookup"><span data-stu-id="bfb60-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="bfb60-114">Når du oppretter en ny problemtype, velger du **Avvikstyper** i handlingsruten for å opprette en liste over én eller flere avvikstyper som er autorisert for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="bfb60-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="bfb60-115">Problemtyper som er knyttet til feilkoder, kan for eksempel gjelde for alle avvikstyper.</span><span class="sxs-lookup"><span data-stu-id="bfb60-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="bfb60-116">En problemtype som er knyttet til klager fra kunder, kan imidlertid bare gjelde for avvikstypene **Kunde** og **Tjenesteforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="bfb60-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="bfb60-117">Eksempler på problemtyper</span><span class="sxs-lookup"><span data-stu-id="bfb60-117">Examples of problem types</span></span>

<span data-ttu-id="bfb60-118">Her er noen eksempler på scenarier for problemtyper som kan brukes med de forskjellige avvikstypene:</span><span class="sxs-lookup"><span data-stu-id="bfb60-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="bfb60-119">**Kunde:** En kunde rapporterte en klage, en kunde returnerte en vare, eller kvalitetsspesifikasjoner ble ikke oppfylt.</span><span class="sxs-lookup"><span data-stu-id="bfb60-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="bfb60-120">**Leverandør:** Produktet ble skadet, kvalitetsspesifikasjoner ble ikke oppfylt eller feil produkt ble mottatt.</span><span class="sxs-lookup"><span data-stu-id="bfb60-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="bfb60-121">**Tjenesteforespørsel:** Kvalitetsspesifikasjoner ble ikke oppfylt, en kunde la inn en klage eller vedlikehold på maskinen er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="bfb60-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="bfb60-122">**Produksjon:** Kvalitetsspesifikasjoner ble ikke oppfylt, maskinvedlikehold er nødvendig eller produktet ble skadet.</span><span class="sxs-lookup"><span data-stu-id="bfb60-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="bfb60-123">**Koproduktproduksjon:** Kvalitetsspesifikasjoner ble ikke oppfylt, maskinvedlikehold er nødvendig eller produktet ble skadet.</span><span class="sxs-lookup"><span data-stu-id="bfb60-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="bfb60-124">Opprette en problemtype og tilordne den til avvikstyper</span><span class="sxs-lookup"><span data-stu-id="bfb60-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="bfb60-125">Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Problemtyper**.</span><span class="sxs-lookup"><span data-stu-id="bfb60-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="bfb60-126">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="bfb60-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bfb60-127">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="bfb60-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bfb60-128">**Problemtype** – Angi en unik ID eller et unikt navn for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="bfb60-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="bfb60-129">**Beskrivelse** – Angi en detaljert beskrivelse av problemtypen.</span><span class="sxs-lookup"><span data-stu-id="bfb60-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="bfb60-130">Mens den nye raden fremdeles er valgt, velger du **Avvikstyper** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bfb60-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="bfb60-131">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="bfb60-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bfb60-132">For den nye raden setter du deretter **Avvikstype**-feltet til avvikstypen som du vil tillate for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="bfb60-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="bfb60-133">Gjenta det forrige trinnet for hver ekstra avvikstype du vil autorisere for problemtypen.</span><span class="sxs-lookup"><span data-stu-id="bfb60-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="bfb60-134">Lukk sidene.</span><span class="sxs-lookup"><span data-stu-id="bfb60-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfb60-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bfb60-135">Additional resources</span></span>

- [<span data-ttu-id="bfb60-136">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="bfb60-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="bfb60-137">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="bfb60-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="bfb60-138">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="bfb60-139">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="bfb60-140">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="bfb60-141">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="bfb60-142">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="bfb60-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="bfb60-143">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="bfb60-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
