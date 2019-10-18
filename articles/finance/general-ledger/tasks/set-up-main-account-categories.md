---
title: Definere hovedkontokategorier
description: Dette emnet forklarer hvordan du definerer hovedkontokategorier i Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e2ba1d900f5d87a76fa93bf53f2970320e7d84c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186009"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="6c7ce-103">Definere hovedkontokategorier</span><span class="sxs-lookup"><span data-stu-id="6c7ce-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c7ce-104">Dette emnet forklarer hvordan du definerer hovedkontokategorier.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="6c7ce-105">Hovedkontokategorier brukes til standardrapportene i finansiell rapportering og Power BI.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="6c7ce-106">Hovedkontokategorier som opprettes som standard kan gis nytt navn, men ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="6c7ce-107">Flere kontokategorier kan opprettes og brukes for rapportering og analyse.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="6c7ce-108">Dette emnet bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="6c7ce-109">Opprette en hovedkontokategori</span><span class="sxs-lookup"><span data-stu-id="6c7ce-109">Create a main account category</span></span>
1. <span data-ttu-id="6c7ce-110">I navigasjonsruten går du til **Moduler > Økonomimodul > Kontoplan > Kontoer > Hovedkontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="6c7ce-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-111">Select **New**.</span></span>
3. <span data-ttu-id="6c7ce-112">Angi et unikt navn i feltet **Hovedkontokategori**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="6c7ce-113">Angi en beskrivelse for hovedkontokategorien i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="6c7ce-114">Velg typen hovedkonto som skal knyttes til kategorien i feltet **Hovedkontotype**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="6c7ce-115">Koble hovedkontoer til kontokategori</span><span class="sxs-lookup"><span data-stu-id="6c7ce-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="6c7ce-116">Klikk **Koble hovedkontoer**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="6c7ce-117">I listen velger du hovedkontoene som skal tilordnes til hovedkontokategorien, ved å merke av boksene i **Koblet**-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="6c7ce-118">Når du tilordner hovedkontoer til en hovedkontokategori, samles saldoene for kontoene når denne kategorien brukes til økonomisk rapportering og analyse.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="6c7ce-119">Aktiver eller deaktiver alternativet **Koblet** for å velge hovedkontoene.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="6c7ce-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-120">Select **OK**.</span></span>
5. <span data-ttu-id="6c7ce-121">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6c7ce-121">Select **Yes**.</span></span>
