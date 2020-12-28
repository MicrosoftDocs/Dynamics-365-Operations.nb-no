---
title: Hva er nytt eller endret i Dynamics 365 Talent (7. januar 2020)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462121"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="216df-103">Hva er nytt eller endret i Dynamics 365 Talent (7. januar 2020)</span><span class="sxs-lookup"><span data-stu-id="216df-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="216df-104">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="216df-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="216df-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="216df-105">Changes in Attract</span></span>

<span data-ttu-id="216df-106">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="216df-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="216df-107">Endringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="216df-107">Changes in Onboard</span></span>

<span data-ttu-id="216df-108">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="216df-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="216df-109">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="216df-109">Changes in Core HR</span></span>

<span data-ttu-id="216df-110">Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="216df-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="216df-111">Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="216df-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="216df-112">Kan ikke slette arbeidere som ikke har ansettelsesposter – (386157)</span><span class="sxs-lookup"><span data-stu-id="216df-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="216df-113">Denne endringen legger til et slettealternativ i skjemaet **Arbeidere uten ansettelse**.</span><span class="sxs-lookup"><span data-stu-id="216df-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="216df-114">Arbeidere vises i dette skjemaet når det ikke finnes fremtidige, aktive eller historiske ansettelsesforhold for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="216df-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="216df-115">I denne versjonen er sletting bare aktivert for systemansvarlige.</span><span class="sxs-lookup"><span data-stu-id="216df-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="216df-116">I neste ukes versjon vil imidlertid sikkerhet bli oppdatert slik at alle brukere med rollen personalassistent kan fjerne ansatte uten ansettelser.</span><span class="sxs-lookup"><span data-stu-id="216df-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="216df-117">Du kan også utføre disse endringene manuelt ved å følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="216df-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="216df-118">Gå til **Sikkerhetskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="216df-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="216df-119">I kategorien **Rettigheter** filtrerer du **Rettigheter**-listen til **Vedlikehold arbeidere**.</span><span class="sxs-lookup"><span data-stu-id="216df-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="216df-120">I **Referanser**-kolonnen velger du **Vis menyelementer**.</span><span class="sxs-lookup"><span data-stu-id="216df-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="216df-121">I **Vis menyelementer** velger du **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="216df-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="216df-122">Angi **Slett**-tillatelsen som skal gis.</span><span class="sxs-lookup"><span data-stu-id="216df-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="216df-123">Velg kategorien **Upubliserte objekter**.</span><span class="sxs-lookup"><span data-stu-id="216df-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="216df-124">Velg **Publiser alle**.</span><span class="sxs-lookup"><span data-stu-id="216df-124">Select **Publish all**.</span></span>
