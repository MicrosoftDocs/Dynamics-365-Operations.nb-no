---
title: Bygge inn Power Apps-apper i Dynamics 365 – Core HR
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830215"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="17f90-103">Bygge inn Power Apps-apper i Dynamics 365 – Core HR</span><span class="sxs-lookup"><span data-stu-id="17f90-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17f90-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="17f90-104">**Issue**</span></span>

<span data-ttu-id="17f90-105">**Power Apps**-menyelementet er fjernet fra **Systemadministrasjon**-modulen.</span><span class="sxs-lookup"><span data-stu-id="17f90-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="17f90-106">**Årsak**</span><span class="sxs-lookup"><span data-stu-id="17f90-106">**Cause**</span></span>

<span data-ttu-id="17f90-107">Brukergrensesnittutformingen (UI) er endret, og Microsoft Power Apps er nå inkludert i standardtilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="17f90-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="17f90-108">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="17f90-108">**Resolution**</span></span>

<span data-ttu-id="17f90-109">Måten Power Apps er innebygget på, er endret.</span><span class="sxs-lookup"><span data-stu-id="17f90-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="17f90-110">Power Apps legges nå til via tilpasningsmodellen.</span><span class="sxs-lookup"><span data-stu-id="17f90-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="17f90-111">Du kan legge til Power Apps på nesten alle sider i Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="17f90-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="17f90-112">Hvis du vil ha mer informasjon om hvordan du bygger inn Power Apps i Talent, se [Bygge inn Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="17f90-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="17f90-113">Power Apps-kunder som bygget inn apper før endringen, skal ha blitt oppgradert til den nye modellen.</span><span class="sxs-lookup"><span data-stu-id="17f90-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="17f90-114">**Power Apps**-knappen er i det øvre høyre hjørnet på nesten alle sidene i Talent.</span><span class="sxs-lookup"><span data-stu-id="17f90-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="17f90-115">Du kan bruke denne knappen for å sette inn Power Apps.</span><span class="sxs-lookup"><span data-stu-id="17f90-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="17f90-116">Her er et eksempel:</span><span class="sxs-lookup"><span data-stu-id="17f90-116">Here is an example.</span></span>

1. <span data-ttu-id="17f90-117">Gå til **Personaladministrasjon \> Koblinger \> Arbeidere \> Ansatte**.</span><span class="sxs-lookup"><span data-stu-id="17f90-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="17f90-118">Velg **Power Apps**, og velg deretter **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="17f90-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps-knappen](media/png.png)

3. <span data-ttu-id="17f90-120">Fyll ut feltene i dialogboksen **Sett inn en PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="17f90-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Sette inn en PowerApp-dialogboks](media/insert-powerapp.png)

<span data-ttu-id="17f90-122">Eller følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="17f90-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="17f90-123">I handlingsruten på siden, i fanen **Alternativer**, i gruppen **Tilpass**, velger du **Tilpass dette skjemaet**.</span><span class="sxs-lookup"><span data-stu-id="17f90-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Tilpasse gruppen i kategorien Alternativer](media/options.png)

    <span data-ttu-id="17f90-125">Verktøylinjen for tilpassing vises.</span><span class="sxs-lookup"><span data-stu-id="17f90-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="17f90-126">På verktøylinjen velger du **Sett inn \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="17f90-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Sette inn en Power Apps-app ved hjelp av verktøylinjen for tilpasning](media/powerapp-bar.png)
