---
title: Tilgangsrettigheter til kontrollere for kostnadsobjekt
description: Dette emnet inneholder informasjon om tilgangsrettigheter for kontrollere for kostnadsobjekt.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897630"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="ab14c-103">Tilgangsrettigheter til kontrollere for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="ab14c-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab14c-104">Arbeidsområdet **Kostnadskontroll** er et sentralt punkt der ledere kan vise ytelsen til kostnadsobjektene sine.</span><span class="sxs-lookup"><span data-stu-id="ab14c-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="ab14c-105">Dette arbeidsområdet lar ledere forbruke kostnadsregnskapsdata selv om de ikke er regnskapsførere.</span><span class="sxs-lookup"><span data-stu-id="ab14c-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="ab14c-106">Av sikkerhetsmessige årsaker må ledere bare kunne se kostnadsregnskapsdataene som er knyttet til de bestemte kostnadsobjektene de har ansvaret for.</span><span class="sxs-lookup"><span data-stu-id="ab14c-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="ab14c-107">Det er fire unike roller i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="ab14c-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="ab14c-108">Rollenavn</span><span class="sxs-lookup"><span data-stu-id="ab14c-108">Role name</span></span>               | <span data-ttu-id="ab14c-109">Lisens</span><span class="sxs-lookup"><span data-stu-id="ab14c-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="ab14c-110">Behandling av kostnadsregn</span><span class="sxs-lookup"><span data-stu-id="ab14c-110">Cost accounting manager</span></span> | <span data-ttu-id="ab14c-111">Aktivitet</span><span class="sxs-lookup"><span data-stu-id="ab14c-111">Activity</span></span>     |
| <span data-ttu-id="ab14c-112">Regnskapsfører lager</span><span class="sxs-lookup"><span data-stu-id="ab14c-112">Cost accountant</span></span>         | <span data-ttu-id="ab14c-113">Operations</span><span class="sxs-lookup"><span data-stu-id="ab14c-113">Operations</span></span>   |
| <span data-ttu-id="ab14c-114">Assisterende lagerregnskapsfører</span><span class="sxs-lookup"><span data-stu-id="ab14c-114">Cost accountant clerk</span></span>   | <span data-ttu-id="ab14c-115">Operations</span><span class="sxs-lookup"><span data-stu-id="ab14c-115">Operations</span></span>   |
| <span data-ttu-id="ab14c-116">Kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="ab14c-116">Cost object controller</span></span>  | <span data-ttu-id="ab14c-117">Teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="ab14c-117">Team members</span></span> |

<span data-ttu-id="ab14c-118">Dette emnet forklarer hvordan du tilordner rollen **Kontroller for kostnadsobjekt** til en leder.</span><span class="sxs-lookup"><span data-stu-id="ab14c-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="ab14c-119">Når rollen **Kontroller for kostnadsobjekt** er tilordnet en leder, kan lederen utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="ab14c-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="ab14c-120">Gå til arbeidsområdet **Kostnadskontroll** (i klienten).</span><span class="sxs-lookup"><span data-stu-id="ab14c-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="ab14c-121">Gå gjennom og få visningstilgang til sidene som støtter gjennomgangsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="ab14c-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="ab14c-122">Gå til arbeidsområdet **Kostnadskontroll** (i mobilprogrammet).</span><span class="sxs-lookup"><span data-stu-id="ab14c-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="ab14c-123">Rollen **Kontroller for kostnadsobjekt** styrer ikke hvilke objekter brukeren kan få tilgang til og vise data for.</span><span class="sxs-lookup"><span data-stu-id="ab14c-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="ab14c-124">Radnivåsikkerhet oppnås via dimensjonshierarkier og hierarkiet for tilgangsliste.</span><span class="sxs-lookup"><span data-stu-id="ab14c-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="ab14c-125">Gi tilgangsrettigheter</span><span class="sxs-lookup"><span data-stu-id="ab14c-125">Grant access rights</span></span>
<span data-ttu-id="ab14c-126">Følgende eksempel viser hvordan et dimensjonshierarki kan se ut.</span><span class="sxs-lookup"><span data-stu-id="ab14c-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="ab14c-127">**Detaljer for dimensjonshierarki**</span><span class="sxs-lookup"><span data-stu-id="ab14c-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="ab14c-128">Dimensjonshierarkinavn</span><span class="sxs-lookup"><span data-stu-id="ab14c-128">Dimension hierarchy name</span></span> | <span data-ttu-id="ab14c-129">Dimensjon</span><span class="sxs-lookup"><span data-stu-id="ab14c-129">Dimension</span></span>    | <span data-ttu-id="ab14c-130">Navn på dimensjonshierarkitype</span><span class="sxs-lookup"><span data-stu-id="ab14c-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="ab14c-131">Hierarki for tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="ab14c-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="ab14c-132">Organisasjon</span><span class="sxs-lookup"><span data-stu-id="ab14c-132">Organization</span></span>             | <span data-ttu-id="ab14c-133">Kostsentre</span><span class="sxs-lookup"><span data-stu-id="ab14c-133">Cost centers</span></span> | <span data-ttu-id="ab14c-134">Hierarki for dimensjonsklassifisering</span><span class="sxs-lookup"><span data-stu-id="ab14c-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="ab14c-135">**Ja**</span><span class="sxs-lookup"><span data-stu-id="ab14c-135">**Yes**</span></span>               |

<span data-ttu-id="ab14c-136">Du kan bruke hurtigfanen **Brukere** i hierarkidesigner til å sette inn én eller flere bruker-ID-er for hver node.</span><span class="sxs-lookup"><span data-stu-id="ab14c-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="ab14c-137">Noder</span><span class="sxs-lookup"><span data-stu-id="ab14c-137">Nodes</span></span>                 | <span data-ttu-id="ab14c-138">Brukere</span><span class="sxs-lookup"><span data-stu-id="ab14c-138">Users</span></span>            | <span data-ttu-id="ab14c-139">Fra-dimensjonsmedlem</span><span class="sxs-lookup"><span data-stu-id="ab14c-139">From dimension member</span></span>     |   <span data-ttu-id="ab14c-140">Til-dimensjonsmedlem</span><span class="sxs-lookup"><span data-stu-id="ab14c-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="ab14c-141">Organisasjon</span><span class="sxs-lookup"><span data-stu-id="ab14c-141">Organization</span></span>                      | <span data-ttu-id="ab14c-142">Benjamin, Claire</span><span class="sxs-lookup"><span data-stu-id="ab14c-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="ab14c-143">&nbsp;&nbsp;Administrator</span><span class="sxs-lookup"><span data-stu-id="ab14c-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="ab14c-144">April</span><span class="sxs-lookup"><span data-stu-id="ab14c-144">April</span></span>            |                           |                         |
| <span data-ttu-id="ab14c-145">&nbsp;&nbsp;&nbsp;&nbsp;Finans</span><span class="sxs-lookup"><span data-stu-id="ab14c-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="ab14c-146">Charlotte</span><span class="sxs-lookup"><span data-stu-id="ab14c-146">Alicia</span></span>           | <span data-ttu-id="ab14c-147">CC002</span><span class="sxs-lookup"><span data-stu-id="ab14c-147">CC002</span></span>                     | <span data-ttu-id="ab14c-148">CC003</span><span class="sxs-lookup"><span data-stu-id="ab14c-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="ab14c-149">CC007</span><span class="sxs-lookup"><span data-stu-id="ab14c-149">CC007</span></span>                     | <span data-ttu-id="ab14c-150">CC007</span><span class="sxs-lookup"><span data-stu-id="ab14c-150">CC007</span></span>                   |
| <span data-ttu-id="ab14c-151">&nbsp;&nbsp;&nbsp;&nbsp;Personale</span><span class="sxs-lookup"><span data-stu-id="ab14c-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="ab14c-152">Magnus</span><span class="sxs-lookup"><span data-stu-id="ab14c-152">Arnie</span></span>            | <span data-ttu-id="ab14c-153">CC001</span><span class="sxs-lookup"><span data-stu-id="ab14c-153">CC001</span></span>                     | <span data-ttu-id="ab14c-154">CC001</span><span class="sxs-lookup"><span data-stu-id="ab14c-154">CC001</span></span>                   |
| <span data-ttu-id="ab14c-155">&nbsp;&nbsp;Produksjon</span><span class="sxs-lookup"><span data-stu-id="ab14c-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="ab14c-156">David</span><span class="sxs-lookup"><span data-stu-id="ab14c-156">David</span></span>            |                           |                         |
| <span data-ttu-id="ab14c-157">&nbsp;&nbsp;&nbsp;&nbsp;Innpakning</span><span class="sxs-lookup"><span data-stu-id="ab14c-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="ab14c-158">Ellen</span><span class="sxs-lookup"><span data-stu-id="ab14c-158">Ellen</span></span>            | <span data-ttu-id="ab14c-159">CC005</span><span class="sxs-lookup"><span data-stu-id="ab14c-159">CC005</span></span>                     | <span data-ttu-id="ab14c-160">CC005</span><span class="sxs-lookup"><span data-stu-id="ab14c-160">CC005</span></span>                   |
| <span data-ttu-id="ab14c-161">&nbsp;&nbsp;&nbsp;&nbsp;Samling</span><span class="sxs-lookup"><span data-stu-id="ab14c-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="ab14c-162">Chris</span><span class="sxs-lookup"><span data-stu-id="ab14c-162">Chris</span></span>            | <span data-ttu-id="ab14c-163">CC006</span><span class="sxs-lookup"><span data-stu-id="ab14c-163">CC006</span></span>                     | <span data-ttu-id="ab14c-164">CC006</span><span class="sxs-lookup"><span data-stu-id="ab14c-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="ab14c-165">Regnskapsførere må tilordnes det øverste nivået i hierarkiet, slik at de kan se alle oppføringene i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="ab14c-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="ab14c-166">Før hierarkiet for tilgangsliste og sikkerhetsinnstillingene for det kan brukes, må alternativet **Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt** settes til **Ja** i **Generelt**-fanen på siden **Kostnadsregnskapsparametere** (**Kostnadsregnskap** > **Oppsett** > **Parametere**).</span><span class="sxs-lookup"><span data-stu-id="ab14c-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="ab14c-167">Innstillingene for hierarkiet for tilgangsliste brukes til å styre dataene som vises på følgende områder:</span><span class="sxs-lookup"><span data-stu-id="ab14c-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="ab14c-168">Arbeidsområdet **Kostnadskontroll** (i klienten):</span><span class="sxs-lookup"><span data-stu-id="ab14c-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="ab14c-169">Data på sidene som brukes til gjennomgang</span><span class="sxs-lookup"><span data-stu-id="ab14c-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="ab14c-170">Arbeidsområdet **Kostnadskontroll** (i mobilprogrammet):</span><span class="sxs-lookup"><span data-stu-id="ab14c-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="ab14c-171">Saldoer i kort</span><span class="sxs-lookup"><span data-stu-id="ab14c-171">Balances in cards</span></span>

- <span data-ttu-id="ab14c-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="ab14c-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="ab14c-173">Data som vises i Power BI-visualiseringer</span><span class="sxs-lookup"><span data-stu-id="ab14c-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="ab14c-174">Power BI-datavisualiseringer som er innebygd i Dynamics 365 Finance-klienten</span><span class="sxs-lookup"><span data-stu-id="ab14c-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="ab14c-175">Før hierarkiet for tilgangsliste kan påvirke data i Power BI, må hierarkiet for tilgangsliste og radnivåsikkerhet i Power BI sammenkobles.</span><span class="sxs-lookup"><span data-stu-id="ab14c-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="ab14c-176">Hvis du vil ha mer informasjon, kan du se [Definere sikkerhet for innholdspakken Kostnadsregnskap](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="ab14c-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="ab14c-177">Dette emnet viser forutsetningene som må være på plass før du kan bruke arbeidsområdet **Kostnadskontroll**.</span><span class="sxs-lookup"><span data-stu-id="ab14c-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="ab14c-178">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ab14c-178">Additional resources</span></span>

- [<span data-ttu-id="ab14c-179">Arbeidsområde for kostnadskontroll</span><span class="sxs-lookup"><span data-stu-id="ab14c-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="ab14c-180">Dimensjonshierarki</span><span class="sxs-lookup"><span data-stu-id="ab14c-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="ab14c-181">Definere sikkerhet for innholdspakken Kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="ab14c-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
