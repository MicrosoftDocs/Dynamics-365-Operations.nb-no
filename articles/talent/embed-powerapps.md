---
title: Bygge inn PowerApps-apper i Dynamics 365 – Core HR
description: Dette emnet beskriver hvordan du løser problemet der PowerApps-menyelementet er fjernet fra systemadministrasjonsmodulen.
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
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551009"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="2fc9c-103">Bygge inn PowerApps-apper i Dynamics 365 – Core HR</span><span class="sxs-lookup"><span data-stu-id="2fc9c-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2fc9c-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="2fc9c-104">**Issue**</span></span>

<span data-ttu-id="2fc9c-105">**PowerApps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="2fc9c-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="2fc9c-106">**Cause**</span></span>

<span data-ttu-id="2fc9c-107">Brukergrensesnittutformingen (UI) er endret, og Microsoft PowerApps er nå inkludert i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="2fc9c-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="2fc9c-108">**Resolution**</span></span>

<span data-ttu-id="2fc9c-109">Måten PowerApps-programmer er innebygget på, er endret.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="2fc9c-110">PowerApps-apper legges nå til via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="2fc9c-111">Du kan legge til PowerApps-apper på nesten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="2fc9c-112">Hvis du vil ha mer informasjon om hvordan du bygger inn PowerApps-apper i Talent, kan du se [Bygge inn PowerApps-apper](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="2fc9c-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="2fc9c-113">PowerApps-kunder som bygget inn apper før endringen, skal ha blitt oppgradert til den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="2fc9c-114">**PowerApps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="2fc9c-115">Du kan bruke denne knappen for å sette inn en PowerApps-app.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="2fc9c-116">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="2fc9c-116">Here is an example.</span></span>

1. <span data-ttu-id="2fc9c-117">Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="2fc9c-118">Velg **PowerApps**, og velg deretter **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps-knappen](media/png.png)

3. <span data-ttu-id="2fc9c-120">Fyll ut feltene i dialogboksen **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Sette inn en PowerApp-dialogboks](media/insert-powerapp.png)

<span data-ttu-id="2fc9c-122">Eller følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="2fc9c-123">I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass dette skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    <span data-ttu-id="2fc9c-125">Verktøylinjen for tilpassing vises.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="2fc9c-126">På verktøylinjen velger du **Sett inn \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="2fc9c-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Sette inn en PowerApps-app ved hjelp av verktøylinjen for tilpasning](media/powerapp-bar.png)
