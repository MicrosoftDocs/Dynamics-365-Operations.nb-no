---
title: Arbeidere uten ansettelse
description: Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises i skjemaet Arbeidere uten ansettelse.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051719"
---
# <a name="workers-without-employment"></a><span data-ttu-id="3ef22-103">Arbeidere uten ansettelse</span><span class="sxs-lookup"><span data-stu-id="3ef22-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3ef22-104">Arbeidere som ikke har en fremtidig, aktiv eller historisk ansettelse i organisasjonen, vises i skjemaet **Arbeidere uten ansettelse**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="3ef22-105">Arbeidere med denne statusen kan vises når du importerer arbeidere uten en ansettelsespost, eller når du sletter en arbeiders ansettelse via **Arbeidere > Ansettelseshistorikk**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="3ef22-106">Som standard er skjemaet **Arbeidere uten ansettelse** tilgjengelig for følgende roller:</span><span class="sxs-lookup"><span data-stu-id="3ef22-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="3ef22-107">Personalassistent</span><span class="sxs-lookup"><span data-stu-id="3ef22-107">Human Resources Assistant</span></span>
- <span data-ttu-id="3ef22-108">Personalsjef</span><span class="sxs-lookup"><span data-stu-id="3ef22-108">Human Resources Manager</span></span>
- <span data-ttu-id="3ef22-109">Rekrutterer</span><span class="sxs-lookup"><span data-stu-id="3ef22-109">Recruiter</span></span>
- <span data-ttu-id="3ef22-110">Kompensasjons og fordelsansvarlig</span><span class="sxs-lookup"><span data-stu-id="3ef22-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="3ef22-111">Lønnsadministrator</span><span class="sxs-lookup"><span data-stu-id="3ef22-111">Payroll Administrator</span></span>
- <span data-ttu-id="3ef22-112">Lønnsansvarlig</span><span class="sxs-lookup"><span data-stu-id="3ef22-112">Payroll Manager</span></span>
- <span data-ttu-id="3ef22-113">Opplæringsleder</span><span class="sxs-lookup"><span data-stu-id="3ef22-113">Training Manager</span></span>

<span data-ttu-id="3ef22-114">I listne **Arbeidere uten ansettelse** kan du slette personene som er oppført.</span><span class="sxs-lookup"><span data-stu-id="3ef22-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="3ef22-115">Som standard gis dette privilegiet til personalassistentrollen.</span><span class="sxs-lookup"><span data-stu-id="3ef22-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="3ef22-116">Du kan gi denne rettigheten til andre roller ved hjelp av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="3ef22-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="3ef22-117">Velg **Systemadministrasjon**, og velg deretter **Sikkerhetskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="3ef22-118">I kategorien **Rettigheter** filtrerer du **Rettigheter**-listen til **Vedlikehold arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="3ef22-119">[![Filterrettigheter-liste](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="3ef22-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="3ef22-120">I **Referanser**-kolonnen velger du **Vis menyelementer**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="3ef22-121">I **Vis menyelementer** velger du **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="3ef22-122">[![Velg skjema](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="3ef22-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="3ef22-123">Angi **Slett**-tillatelsen som du skal **innvilge**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="3ef22-124">Velg kategorien **Upubliserte objekter**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="3ef22-125">Velg **Publiser alle**.</span><span class="sxs-lookup"><span data-stu-id="3ef22-125">Select **Publish all**.</span></span>

   <span data-ttu-id="3ef22-126">[![Publiser endringer](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="3ef22-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]