---
title: Bygge inn Power Apps-apper i Dynamics 365 Human Resources
description: Dette emnet beskriver hvordan du løser problemet der Microsoft Power Apps-menyelementet er fjernet fra systemadministrasjonsmodulen.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017879"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="1bd84-103">Bygge inn Power Apps-apper i Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="1bd84-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="1bd84-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="1bd84-104">**Issue**</span></span>

<span data-ttu-id="1bd84-105">**Power Apps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.</span><span class="sxs-lookup"><span data-stu-id="1bd84-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="1bd84-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="1bd84-106">**Cause**</span></span>

<span data-ttu-id="1bd84-107">Brukergrensesnittutformingen (UI) er endret, og Microsoft Power Apps er nå inkludert i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="1bd84-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="1bd84-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="1bd84-108">**Resolution**</span></span>

<span data-ttu-id="1bd84-109">Måten Power Apps er innebygget på, er endret.</span><span class="sxs-lookup"><span data-stu-id="1bd84-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="1bd84-110">Power Apps legges nå til via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="1bd84-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="1bd84-111">Du kan legge til Power Apps på nesten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="1bd84-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="1bd84-112">Hvis du vil ha mer informasjon om hvordan du bygger inn Power Apps i Talent, se [Bygge inn Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="1bd84-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="1bd84-113">Power Apps-kunder som bygget inn apper før endringen, skal ha blitt oppgradert til den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="1bd84-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="1bd84-114">**Power Apps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent.</span><span class="sxs-lookup"><span data-stu-id="1bd84-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="1bd84-115">Du kan bruke denne knappen for å sette inn apper.</span><span class="sxs-lookup"><span data-stu-id="1bd84-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="1bd84-116">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="1bd84-116">Here is an example.</span></span>

1. <span data-ttu-id="1bd84-117">Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.</span><span class="sxs-lookup"><span data-stu-id="1bd84-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="1bd84-118">Velg **Power Apps**-knappen og velg deretter **Legg til en app fra Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="1bd84-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps-knappen](media/png.png)

3. <span data-ttu-id="1bd84-120">Fyll ut feltene i **Legg til en app fra Power Apps**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="1bd84-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Legge til en app fra Power Apps-dialogboksen](media/insert-powerapp.png)

<span data-ttu-id="1bd84-122">Eller følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="1bd84-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="1bd84-123">I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass denne siden**.</span><span class="sxs-lookup"><span data-stu-id="1bd84-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    <span data-ttu-id="1bd84-125">Verktøylinjen for tilpassing vises.</span><span class="sxs-lookup"><span data-stu-id="1bd84-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="1bd84-126">På verktøylinjen velger du **Legg til en app fra Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="1bd84-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Legge til en app fra Power Apps ved hjelp av Tilpasning-verktøylinjen](media/powerapp-bar.png)
