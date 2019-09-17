---
title: Bygge inn PowerApps-apper i Core HR
description: Dette emnet forklarer hvordan du løser problemet der PowerApps-menyelementet er fjernet fra systemadministrasjonsmodulen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7c0dcdd7e2f407267cf99906b4d0b317858710af
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742825"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="00f20-103">Bygge inn PowerApps-apper i Core HR</span><span class="sxs-lookup"><span data-stu-id="00f20-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="00f20-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="00f20-104">**Issue**</span></span>

<span data-ttu-id="00f20-105">**PowerApps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.</span><span class="sxs-lookup"><span data-stu-id="00f20-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="00f20-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="00f20-106">**Cause**</span></span>

<span data-ttu-id="00f20-107">Brukergrensesnittutformingen (UI) er endret, og Microsoft PowerApps er nå inkludert i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="00f20-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="00f20-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="00f20-108">**Resolution**</span></span>

<span data-ttu-id="00f20-109">Måten PowerApps-programmer er innebygget på, er endret.</span><span class="sxs-lookup"><span data-stu-id="00f20-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="00f20-110">PowerApps-programmer legges nå til via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="00f20-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="00f20-111">Du kan legge til PowerApps-programmer på nesten alle sider i Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="00f20-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="00f20-112">Hvis du vil ha mer informasjon om hvordan du bygger inn PowerApps-apper i Talent, kan du se  [Bygge inn PowerApps-apper](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="00f20-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="00f20-113">PowerApps-kunder som bygde inn apper før endringen, skal ha blitt oppgradert til den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="00f20-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="00f20-114">**PowerApps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent.</span><span class="sxs-lookup"><span data-stu-id="00f20-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="00f20-115">Du kan bruke denne knappen for å sette inn en PowerApps-app.</span><span class="sxs-lookup"><span data-stu-id="00f20-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="00f20-116">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="00f20-116">Here is an example.</span></span>

1. <span data-ttu-id="00f20-117">Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.</span><span class="sxs-lookup"><span data-stu-id="00f20-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="00f20-118">Velg **PowerApps**, og velg deretter **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="00f20-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-knappen](media/png.png)

3. <span data-ttu-id="00f20-120">Fyll ut feltene i dialogboksen **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="00f20-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Sette inn en PowerApp-dialogboks](media/insert-powerapp.png)

<span data-ttu-id="00f20-122">Eller følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="00f20-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="00f20-123">I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass dette skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="00f20-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    <span data-ttu-id="00f20-125">Verktøylinjen for tilpassing vises.</span><span class="sxs-lookup"><span data-stu-id="00f20-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="00f20-126">På verktøylinjen velger du **Sett inn \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="00f20-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Sette inn et PowerApps-program ved hjelp av verktøylinjen for tilpasning](media/powerapp-bar.png)
