---
title: Talent vises ikke blant appene i Microsoft Dynamics 365 (CDS1.0)
description: "Dette emnet forklarer hva du gjør hvis kunden ikke kan du se appen Microsoft Dynamics 365 for Talent blant Microsoft Dynamics 365-appene."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: nb-no
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="e50f6-103">Talent vises ikke blant appene i Microsoft Dynamics 365 (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="e50f6-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e50f6-104">**Utstede**</span><span class="sxs-lookup"><span data-stu-id="e50f6-104">**Issue**</span></span>

<span data-ttu-id="e50f6-105">Kunden ser ikke Microsoft Dynamics 365 for Talent-appen blant Microsoft Dynamics 365-appene.</span><span class="sxs-lookup"><span data-stu-id="e50f6-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="e50f6-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="e50f6-106">**Resolution**</span></span>

<span data-ttu-id="e50f6-107">Brukeren må legges til Miljøskaper-rollen for miljøet i Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="e50f6-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="e50f6-108">Admin-brukeren som har en PowerApps Plan 2-lisens, må åpne [PowerApps-administrasjonsportalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="e50f6-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="e50f6-109">Velg **Miljøer**, og velg riktig miljø for Talent.</span><span class="sxs-lookup"><span data-stu-id="e50f6-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="e50f6-110">I fanen **Sikkerhet** i fanen **Miljøroller** velger du **Miljøskaper**.</span><span class="sxs-lookup"><span data-stu-id="e50f6-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="e50f6-112">I fanen **Brukere** legger du til brukeren eller organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="e50f6-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brukere](media/environment-maker.png)

5. <span data-ttu-id="e50f6-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e50f6-114">Select **Save**.</span></span>
6. <span data-ttu-id="e50f6-115">Brukeren må nå logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="e50f6-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="e50f6-116">Velg **Synkroniser** for å oppdatere brukerappene.</span><span class="sxs-lookup"><span data-stu-id="e50f6-116">Select **Sync** to update the user apps.</span></span>

    ![Synkroniser-knappen](media/get-more.png)

    <span data-ttu-id="e50f6-118">Når synkroniseringen er fullført, vises Talent på startsiden.</span><span class="sxs-lookup"><span data-stu-id="e50f6-118">After synchronization is completed, Talent will appear on the home page.</span></span>

