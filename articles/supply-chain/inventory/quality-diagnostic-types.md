---
title: Diagnosetyper for avvik
description: Dette emnet beskriver hvordan du bruker og oppretter diagnosetyper som kan brukes med avvik.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19fcd57e28efabd6ca32c444ab961b876bde424d
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956768"
---
# <a name="diagnostic-types-for-nonconformances"></a><span data-ttu-id="9593d-103">Diagnosetyper for avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-103">Diagnostic types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9593d-104">Dette emnet beskriver hvordan du bruker og oppretter diagnosetyper som kan brukes med avvik.</span><span class="sxs-lookup"><span data-stu-id="9593d-104">This topic describes how to use and create diagnostic types that can be used with nonconformances.</span></span>

<span data-ttu-id="9593d-105">Du bruker **Diagnosetyper**-siden til å definere en klassifisering av diagnosehandlinger.</span><span class="sxs-lookup"><span data-stu-id="9593d-105">You use the **Diagnostic types** page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="9593d-106">Når du deretter oppretter en korrigering for et avvik, velger du en diagnose.</span><span class="sxs-lookup"><span data-stu-id="9593d-106">Then, when you create a correction for a nonconformance, you select a diagnostic.</span></span> <span data-ttu-id="9593d-107">En rettelse angir hvilken type diagnosehandling som skal utføres for et godkjent avvik, og hvem som skal utføre denne handlingen.</span><span class="sxs-lookup"><span data-stu-id="9593d-107">A correction specifies what type of diagnostic action should be taken for an approved nonconformance, and who should take that action.</span></span> <span data-ttu-id="9593d-108">Den angir også den ønskede fullføringsdatoen og den planlagte fullføringsdatoen.</span><span class="sxs-lookup"><span data-stu-id="9593d-108">It also specifies the requested completion date and the planned completion date.</span></span>

## <a name="examples-of-diagnostic-types"></a><span data-ttu-id="9593d-109">Eksempler på diagnosetyper</span><span class="sxs-lookup"><span data-stu-id="9593d-109">Examples of diagnostic types</span></span>

<span data-ttu-id="9593d-110">Du jobber for et produksjonsfirma, og flere varer har mislykkede kvalitetstester.</span><span class="sxs-lookup"><span data-stu-id="9593d-110">You work for a manufacturing company, and several items have failed quality tests.</span></span> <span data-ttu-id="9593d-111">Disse varene flyttes inn i et karanteneområde og merkes som produkter med avvik.</span><span class="sxs-lookup"><span data-stu-id="9593d-111">Those items are moved into a quarantine area and marked as nonconforming products.</span></span> <span data-ttu-id="9593d-112">En avvikspost opprettes i Microsoft Dynamics 365 Supply Chain Management for å spore detaljene ved hjelp av problemløsning.</span><span class="sxs-lookup"><span data-stu-id="9593d-112">A nonconformance record is created in Microsoft Dynamics 365 Supply Chain Management to track the details through issue resolution.</span></span>

<span data-ttu-id="9593d-113">I dette tilfellet oppstår kvalitetsproblemene fordi lagre i maskinen som pakker varene har blitt overopphetet.</span><span class="sxs-lookup"><span data-stu-id="9593d-113">In this case, the quality issues are occurring because bearings in the machine that packages the items have gone bad and are overheating.</span></span> <span data-ttu-id="9593d-114">Løsningen på dette problemet er å erstatte delene i maskinen.</span><span class="sxs-lookup"><span data-stu-id="9593d-114">The correction for this problem is to replace the parts in the machine.</span></span>

<span data-ttu-id="9593d-115">Når du konfigurerer diagnosetypene, kan du opprette flere poster, som hver representerer en forskjellig type problem som maskinen kan ha.</span><span class="sxs-lookup"><span data-stu-id="9593d-115">When you configure the diagnostic types, you can create multiple records, each of which represents a different type of problem that the machine might have.</span></span> <span data-ttu-id="9593d-116">Du kan også opprette en generisk diagnosetype som representerer maskinreparasjon.</span><span class="sxs-lookup"><span data-stu-id="9593d-116">Alternatively, you can create one generic diagnostic type that represents machine repair.</span></span>

## <a name="create-a-diagnostic-type"></a><span data-ttu-id="9593d-117">Opprette en diagnosetype</span><span class="sxs-lookup"><span data-stu-id="9593d-117">Create a diagnostic type</span></span>

1. <span data-ttu-id="9593d-118">Gå til **Lagerstyring \> Oppsett \> Kvalitetsstyring \> Diagnosetyper**.</span><span class="sxs-lookup"><span data-stu-id="9593d-118">Go to **Inventory management \> Setup \> Quality management \> Diagnostic types**.</span></span>
1. <span data-ttu-id="9593d-119">I handlingsruten velger du **Ny** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="9593d-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="9593d-120">Angi deretter følgende felter for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="9593d-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="9593d-121">**Diagnose** – Angi en unik identifikator eller et unikt navn for diagnosetypen.</span><span class="sxs-lookup"><span data-stu-id="9593d-121">**Diagnostic** – Enter a unique ID or name for the diagnostic type.</span></span>
    - <span data-ttu-id="9593d-122">**Beskrivelse** – Angi en detaljert beskrivelse av diagnosetypen.</span><span class="sxs-lookup"><span data-stu-id="9593d-122">**Description** – Enter a detailed description of the diagnostic type.</span></span>

1. <span data-ttu-id="9593d-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9593d-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9593d-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9593d-124">Additional resources</span></span>

- [<span data-ttu-id="9593d-125">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="9593d-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="9593d-126">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="9593d-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="9593d-127">Arbeidere som er ansvarlige for å godkjenne avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-127">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="9593d-128">Karantenesoner for avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="9593d-129">Problemtyper for avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-129">Problem types for nonconformances</span></span>](quality-problem-types.md)
- [<span data-ttu-id="9593d-130">Kvalitetsendringer for avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="9593d-131">Operasjoner for avvik</span><span class="sxs-lookup"><span data-stu-id="9593d-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="9593d-132">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="9593d-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
