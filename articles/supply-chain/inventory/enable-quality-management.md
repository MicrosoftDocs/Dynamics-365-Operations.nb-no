---
title: Aktivere kvalitets- og avviksstyring
description: Dette emnet gir en oversikt over prosessen for å definere og konfigurere funksjoner for kvalitets- og avviksstyring i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956260"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="f0706-103">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0706-104">Dette emnet gir en oversikt over prosessen for å definere og konfigurere funksjoner for kvalitets- og avviksstyring i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0706-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="f0706-105">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="f0706-106">Følg denne fremgangsmåten for å aktivere kvalitetsstyring på systemet.</span><span class="sxs-lookup"><span data-stu-id="f0706-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="f0706-107">Gå til **Lagerstyring \> Oppsett \> Parametere for beholdnings- og lagerstyring**.</span><span class="sxs-lookup"><span data-stu-id="f0706-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="f0706-108">I kategorien **Kvalitetsstyring** setter du alternativet **Bruk kvalitetsstyring** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="f0706-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="f0706-109">I **Timepris**-feltet angir du en timepris for arbeid i lokal valuta.</span><span class="sxs-lookup"><span data-stu-id="f0706-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="f0706-110">Timeprisen brukes til å beregne kostnader for operasjoner som er knyttet til et avvik.</span><span class="sxs-lookup"><span data-stu-id="f0706-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="f0706-111">Timeprisen og de beregnede kostnadene gir referanseinformasjon for et avvik.</span><span class="sxs-lookup"><span data-stu-id="f0706-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="f0706-112">De samhandler ikke med annen funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="f0706-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="f0706-113">Velg **Rapportoppsett**.</span><span class="sxs-lookup"><span data-stu-id="f0706-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="f0706-114">Legg til nye linjer for de ulike rapporttypene, og velg dokumenttypen som skal brukes for hver rapport.</span><span class="sxs-lookup"><span data-stu-id="f0706-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="f0706-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f0706-115">Close the page.</span></span>
1. <span data-ttu-id="f0706-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f0706-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="f0706-117">Konfigurasjonsprosess for kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-117">Quality management configuration process</span></span>

<span data-ttu-id="f0706-118">Før du kan begynne å bruke kvalitetsstyringsfunksjonene og generere kvalitetsordrer, må du konfigurere systemet og forutsetningene.</span><span class="sxs-lookup"><span data-stu-id="f0706-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="f0706-119">Her er en liste over trinnene som kreves for å konfigurere kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="f0706-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="f0706-120">[Aktivere kvalitets- og avviksstyring](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="f0706-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="f0706-121">Valgfritt: [Konfigurere testinstrumenter](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="f0706-122">[Konfigurere tester](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="f0706-123">[Konfigurere testvariabler og -resultater](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="f0706-124">[Konfigurere testgrupper](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="f0706-125">Valgfritt: [Konfigurere kvalitetsgrupper, og koble til produkter](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="f0706-126">Valgfritt: [Konfigurere kvalitettilordninger](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="f0706-127">Når konfigurasjonen er fullført, kan du begynne å opprette og behandle kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="f0706-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="f0706-128">Hvis du vil ha mer informasjon om hvordan du oppretter og jobber med kvalitetsordrer, kan du [Kvalitetsordrer](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="f0706-129">Konfigurasjonsprosess for avviksstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="f0706-130">Før du kan begynne å bruke avviksstyringsfunksjonene og generere avvik, må du konfigurere systemet og forutsetningene.</span><span class="sxs-lookup"><span data-stu-id="f0706-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="f0706-131">Her er en liste over trinnene som kreves for å konfigurere avviksstyring.</span><span class="sxs-lookup"><span data-stu-id="f0706-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="f0706-132">[Aktivere kvalitets- og avviksstyring](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="f0706-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="f0706-133">[Konfigurere arbeidere som er ansvarlige for å godkjenne avvik](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="f0706-134">[Konfigurere problemtyper](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="f0706-135">[Konfigurere karantenesoner](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="f0706-136">[Konfigurere diagnosetyper](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="f0706-137">[Konfigurere operasjoner](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="f0706-138">Valgfritt: [Konfigurere kvalitetsgebyrer](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="f0706-139">Når konfigurasjonen er fullført, kan du begynne å opprette og behandle avvik.</span><span class="sxs-lookup"><span data-stu-id="f0706-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="f0706-140">Hvis du vil ha mer informasjon om hvordan du oppretter og arbeider med avvik, kan du se [Opprette og behandle avvik](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="f0706-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0706-141">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f0706-141">Additional resources</span></span>

- [<span data-ttu-id="f0706-142">Oversikt over kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="f0706-143">Aktivere kvalitets- og avviksstyring</span><span class="sxs-lookup"><span data-stu-id="f0706-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="f0706-144">Kvalitetsstyring for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="f0706-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
