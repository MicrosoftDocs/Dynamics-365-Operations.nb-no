---
title: Attract-brukere kan ikke søke på jobber fra karriereportalen
description: Dette emnet forklarer hvordan du feilsøker et problem der Attract-brukere ikke kan søke på jobber fra karriereportalen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462080"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="9c6ba-103">Attract-brukere kan ikke søke på jobber fra karriereportalen</span><span class="sxs-lookup"><span data-stu-id="9c6ba-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="9c6ba-104">Problem</span><span class="sxs-lookup"><span data-stu-id="9c6ba-104">Issue</span></span>

<span data-ttu-id="9c6ba-105">Attract-brukere kan ikke søke på jobber fra karriereportalen.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="9c6ba-106">Når de prøver å søke på en jobb som ble opprettet i Dynamics 365 Talent: Attract, laster nettleseren inn siden kontinuerlig og fullfører ikke handlingen.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="9c6ba-107">Årsak</span><span class="sxs-lookup"><span data-stu-id="9c6ba-107">Cause</span></span>

<span data-ttu-id="9c6ba-108">Dette problemet oppstår når talentrelasjonsteamet ikke har Talentbruker-rolle.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="9c6ba-109">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="9c6ba-109">Resolution</span></span>

<span data-ttu-id="9c6ba-110">Tilordne Talentbruker-rollen til talentrelasjonsteamet.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="9c6ba-111">Logg på [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com) med en av følgende administratorlegitimasjoner:</span><span class="sxs-lookup"><span data-stu-id="9c6ba-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="9c6ba-112">Dynamics 365-administrator</span><span class="sxs-lookup"><span data-stu-id="9c6ba-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="9c6ba-113">Global administrator</span><span class="sxs-lookup"><span data-stu-id="9c6ba-113">Global admin</span></span>
   - <span data-ttu-id="9c6ba-114">Power Platform-administrator</span><span class="sxs-lookup"><span data-stu-id="9c6ba-114">Power Platform admin</span></span>

2. <span data-ttu-id="9c6ba-115">I navigasjonsruten velger du **Miljøer**, og deretter velger du miljøet som Talentbruker-rollen til talentrelasjonsteamet skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Velg miljø](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="9c6ba-117">I **Miljøer**-ruten velger du **URL-adressen for miljø** og logger på administrasjonsportalen for miljøet (for eksempel https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9c6ba-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="9c6ba-118">Velg **Innstillinger**, velg **System** og velg deretter **Sikkerhet**.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Gå til Sikkerhet](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="9c6ba-120">Velg **Team**.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-120">Select **Teams**.</span></span>

   ![Velg Team](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="9c6ba-122">Søk etter **talentrelasjonsteam** i søkefeltet, og velg deretter teamet fra søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="9c6ba-123">Velg **ADMINISTRER ROLLER** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="9c6ba-124">I dialogen **Administrer teamroller** velger du **Talentbruker** fra listen over tilgjengelige roller, og deretter velger du **OK** for å bruke rollen.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Bruk rolle](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="9c6ba-126">Test endringene:</span><span class="sxs-lookup"><span data-stu-id="9c6ba-126">Test your changes:</span></span>

   1. <span data-ttu-id="9c6ba-127">Logg deg på karriereportalen fra et nytt nettleservindu.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="9c6ba-128">Søk på jobben fra karriereportalen.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-128">Apply for the job from the career portal.</span></span> 