---
title: Definere tilgangsrettigheter for kontrollere for kostnadsobjekt
description: Dette emnet inneholder informasjon om tilgangsrettigheter for kontrollere for kostnadsobjekt.
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 89497e49b85eecec5da31e76786ab950db088746
ms.contentlocale: nb-no
ms.lasthandoff: 01/19/2018

---

# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="06059-103">Tilgangsrettigheter til en kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="06059-103">Access rights of a cost object controller</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="06059-104">Arbeidsområdet **Kostnadskontroll** er et sentralt punkt der ledere kan vise ytelsen til kostnadsobjektene sine.</span><span class="sxs-lookup"><span data-stu-id="06059-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="06059-105">Dette arbeidsområdet lar ledere forbruke kostnadsregnskapsdata selv om de ikke er regnskapsførere.</span><span class="sxs-lookup"><span data-stu-id="06059-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="06059-106">Av sikkerhetsmessige årsaker må ledere bare kunne se kostnadsregnskapsdataene som er knyttet til de bestemte kostnadsobjektene de har ansvaret for.</span><span class="sxs-lookup"><span data-stu-id="06059-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="06059-107">Det er fire unike roller i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="06059-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="06059-108">Rollenavn</span><span class="sxs-lookup"><span data-stu-id="06059-108">Role name</span></span>               | <span data-ttu-id="06059-109">Lisens</span><span class="sxs-lookup"><span data-stu-id="06059-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="06059-110">Behandling av kostnadsregn</span><span class="sxs-lookup"><span data-stu-id="06059-110">Cost accounting manager</span></span> | <span data-ttu-id="06059-111">Aktivitet</span><span class="sxs-lookup"><span data-stu-id="06059-111">Activity</span></span>     |
| <span data-ttu-id="06059-112">Regnskapsfører lager</span><span class="sxs-lookup"><span data-stu-id="06059-112">Cost accountant</span></span>         | <span data-ttu-id="06059-113">Operations</span><span class="sxs-lookup"><span data-stu-id="06059-113">Operations</span></span>   |
| <span data-ttu-id="06059-114">Assisterende lagerregnskapsfører</span><span class="sxs-lookup"><span data-stu-id="06059-114">Cost accountant clerk</span></span>   | <span data-ttu-id="06059-115">Operations</span><span class="sxs-lookup"><span data-stu-id="06059-115">Operations</span></span>   |
| <span data-ttu-id="06059-116">Kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="06059-116">Cost object controller</span></span>  | <span data-ttu-id="06059-117">Teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="06059-117">Team members</span></span> |

<span data-ttu-id="06059-118">Dette emnet forklarer hvordan du tilordner rollen **Kontroller for kostnadsobjekt** til en leder.</span><span class="sxs-lookup"><span data-stu-id="06059-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="06059-119">Når rollen **Kontroller for kostnadsobjekt** er tilordnet en leder, kan lederen utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="06059-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="06059-120">Gå til arbeidsområdet **Kostnadskontroll** (i klienten).</span><span class="sxs-lookup"><span data-stu-id="06059-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="06059-121">Gå gjennom og få visningstilgang til sidene som støtter gjennomgangsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="06059-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="06059-122">Gå til arbeidsområdet **Kostnadskontroll** (i mobilprogrammet).</span><span class="sxs-lookup"><span data-stu-id="06059-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="06059-123">Rollen **Kontroller for kostnadsobjekt** styrer ikke hvilke objekter brukeren kan få tilgang til og vise data for.</span><span class="sxs-lookup"><span data-stu-id="06059-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="06059-124">Radnivåsikkerhet oppnås via dimensjonshierarkier og hierarkiet for tilgangsliste.</span><span class="sxs-lookup"><span data-stu-id="06059-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="06059-125">Gi tilgangsrettigheter</span><span class="sxs-lookup"><span data-stu-id="06059-125">Grant access rights</span></span>
<span data-ttu-id="06059-126">Følgende eksempel viser hvordan et dimensjonshierarki kan se ut.</span><span class="sxs-lookup"><span data-stu-id="06059-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="06059-127">**Detaljer for dimensjonshierarki**</span><span class="sxs-lookup"><span data-stu-id="06059-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="06059-128">Dimensjonshierarkinavn</span><span class="sxs-lookup"><span data-stu-id="06059-128">Dimension hierarchy name</span></span> | <span data-ttu-id="06059-129">Dimensjon</span><span class="sxs-lookup"><span data-stu-id="06059-129">Dimension</span></span>    | <span data-ttu-id="06059-130">Navn på dimensjonshierarkitype</span><span class="sxs-lookup"><span data-stu-id="06059-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="06059-131">Hierarki for tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="06059-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="06059-132">Organisasjon</span><span class="sxs-lookup"><span data-stu-id="06059-132">Organization</span></span>             | <span data-ttu-id="06059-133">Kostsentre</span><span class="sxs-lookup"><span data-stu-id="06059-133">Cost centers</span></span> | <span data-ttu-id="06059-134">Hierarki for dimensjonsklassifisering</span><span class="sxs-lookup"><span data-stu-id="06059-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="06059-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="06059-135">**Yes**</span></span>               |

<span data-ttu-id="06059-136">Du kan bruke hurtigfanen **Brukere** i hierarkidesigner til å sette inn én eller flere bruker-ID-er for hver node.</span><span class="sxs-lookup"><span data-stu-id="06059-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="06059-137">Brukere</span><span class="sxs-lookup"><span data-stu-id="06059-137">Users</span></span>            | <span data-ttu-id="06059-138">Dimensjonsmedlemsområder</span><span class="sxs-lookup"><span data-stu-id="06059-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="06059-139">**Noder**</span><span class="sxs-lookup"><span data-stu-id="06059-139">**Nodes**</span></span>                         | <span data-ttu-id="06059-140">**Bruker-ID**</span><span class="sxs-lookup"><span data-stu-id="06059-140">**User ID**</span></span>      | <span data-ttu-id="06059-141">**Fra dimensjonsmedlem**</span><span class="sxs-lookup"><span data-stu-id="06059-141">**From dimension member**</span></span> | <span data-ttu-id="06059-142">**Til dimensjonsmedlem**</span><span class="sxs-lookup"><span data-stu-id="06059-142">**To dimension member**</span></span> |
| <span data-ttu-id="06059-143">Organisasjon</span><span class="sxs-lookup"><span data-stu-id="06059-143">Organization</span></span>                      | <span data-ttu-id="06059-144">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="06059-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="06059-145">&nbsp;&nbsp;Administrator</span><span class="sxs-lookup"><span data-stu-id="06059-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="06059-146">April</span><span class="sxs-lookup"><span data-stu-id="06059-146">April</span></span>            |                           |                         |
| <span data-ttu-id="06059-147">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="06059-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="06059-148">Charlotte</span><span class="sxs-lookup"><span data-stu-id="06059-148">Alicia</span></span>           | <span data-ttu-id="06059-149">CC002</span><span class="sxs-lookup"><span data-stu-id="06059-149">CC002</span></span>                     | <span data-ttu-id="06059-150">CC003</span><span class="sxs-lookup"><span data-stu-id="06059-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="06059-151">CC007</span><span class="sxs-lookup"><span data-stu-id="06059-151">CC007</span></span>                     | <span data-ttu-id="06059-152">CC007</span><span class="sxs-lookup"><span data-stu-id="06059-152">CC007</span></span>                   |
| <span data-ttu-id="06059-153">&nbsp;&nbsp;&nbsp;&nbsp;Personale</span><span class="sxs-lookup"><span data-stu-id="06059-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="06059-154">Magnus</span><span class="sxs-lookup"><span data-stu-id="06059-154">Arnie</span></span>            | <span data-ttu-id="06059-155">CC001</span><span class="sxs-lookup"><span data-stu-id="06059-155">CC001</span></span>                     | <span data-ttu-id="06059-156">CC001</span><span class="sxs-lookup"><span data-stu-id="06059-156">CC001</span></span>                   |
| <span data-ttu-id="06059-157">&nbsp;&nbsp;Produksjon</span><span class="sxs-lookup"><span data-stu-id="06059-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="06059-158">David</span><span class="sxs-lookup"><span data-stu-id="06059-158">David</span></span>            |                           |                         |
| <span data-ttu-id="06059-159">&nbsp;&nbsp;&nbsp;&nbsp;Innpakning</span><span class="sxs-lookup"><span data-stu-id="06059-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="06059-160">Ellen</span><span class="sxs-lookup"><span data-stu-id="06059-160">Ellen</span></span>            | <span data-ttu-id="06059-161">CC005</span><span class="sxs-lookup"><span data-stu-id="06059-161">CC005</span></span>                     | <span data-ttu-id="06059-162">CC005</span><span class="sxs-lookup"><span data-stu-id="06059-162">CC005</span></span>                   |
| <span data-ttu-id="06059-163">&nbsp;&nbsp;&nbsp;&nbsp;Samling</span><span class="sxs-lookup"><span data-stu-id="06059-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="06059-164">Chris</span><span class="sxs-lookup"><span data-stu-id="06059-164">Chris</span></span>            | <span data-ttu-id="06059-165">CC006</span><span class="sxs-lookup"><span data-stu-id="06059-165">CC006</span></span>                     | <span data-ttu-id="06059-166">CC006</span><span class="sxs-lookup"><span data-stu-id="06059-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="06059-167">Regnskapsførere må tilordnes det øverste nivået i hierarkiet, slik at de kan se alle oppføringene i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="06059-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="06059-168">Før hierarkiet for tilgangsliste og sikkerhetsinnstillingene for det kan brukes, må alternativet **Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt** settes til **Ja** i **Generelt**-fanen på siden **Kostnadsregnskapsparametere** (**Kostnadsregnskap** > **Oppsett** > **Parametere**).</span><span class="sxs-lookup"><span data-stu-id="06059-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="06059-169">Innstillingene for hierarkiet for tilgangsliste brukes til å styre dataene som vises på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="06059-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="06059-170">Arbeidsområdet **Kostnadskontroll** (i klienten):</span><span class="sxs-lookup"><span data-stu-id="06059-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="06059-171">Data på sidene som brukes til gjennomgang</span><span class="sxs-lookup"><span data-stu-id="06059-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="06059-172">Arbeidsområdet **Kostnadskontroll** (i mobilprogrammet):</span><span class="sxs-lookup"><span data-stu-id="06059-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="06059-173">Saldoer i kort</span><span class="sxs-lookup"><span data-stu-id="06059-173">Balances in cards</span></span>

- <span data-ttu-id="06059-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="06059-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="06059-175">Data som vises i Power BI-visualiseringer</span><span class="sxs-lookup"><span data-stu-id="06059-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="06059-176">Power BI-datavisualiseringer som er innebygd i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, klienten</span><span class="sxs-lookup"><span data-stu-id="06059-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="06059-177">Før hierarkiet for tilgangsliste kan påvirke data i Power BI, må hierarkiet for tilgangsliste og radnivåsikkerhet pares i Power BI.</span><span class="sxs-lookup"><span data-stu-id="06059-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="06059-178">Hvis du vil ha mer informasjon, kan du se [Definere sikkerhet for innholdspakken Kostnadsregnskap](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="06059-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="06059-179">Dette emnet viser forutsetningene som må være på plass før du kan bruke arbeidsområdet **Kostnadskontroll**.</span><span class="sxs-lookup"><span data-stu-id="06059-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="06059-180">Se også</span><span class="sxs-lookup"><span data-stu-id="06059-180">See also</span></span>

- [<span data-ttu-id="06059-181">Arbeidsområde for kostnadskontroll</span><span class="sxs-lookup"><span data-stu-id="06059-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="06059-182">Dimensjonshierarki</span><span class="sxs-lookup"><span data-stu-id="06059-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="06059-183">Definere sikkerhet for innholdspakken Kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="06059-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

