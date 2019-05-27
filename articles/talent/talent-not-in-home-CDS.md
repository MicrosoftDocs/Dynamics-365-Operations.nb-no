---
title: Talent vises ikke blant appene i Microsoft Dynamics 365 (Common Data Service 1.0)
description: Dette emnet forklarer hva du gjør hvis kunden ikke kan du se appen Microsoft Dynamics 365 for Talent blant Microsoft Dynamics 365-appene.
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
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518789"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="5b8df-103">Talent vises ikke blant appene i Microsoft Dynamics 365 (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="5b8df-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b8df-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="5b8df-104">**Issue**</span></span>

<span data-ttu-id="5b8df-105">Kunden kan ikke se Microsoft Dynamics 365 for Talent-appen blant Microsoft Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="5b8df-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="5b8df-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="5b8df-106">**Resolution**</span></span>

<span data-ttu-id="5b8df-107">Brukeren må legges til Miljøskaper-rollen for miljøet i Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="5b8df-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="5b8df-108">Admin-brukeren som har en PowerApps Plan 2-lisens, må åpne [PowerApps-administrasjonsportalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="5b8df-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="5b8df-109">Velg **Miljøer**, og velg riktig miljø for Talent.</span><span class="sxs-lookup"><span data-stu-id="5b8df-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="5b8df-110">I fanen **Sikkerhet** i fanen **Miljøroller** velger du **Miljøskaper**.</span><span class="sxs-lookup"><span data-stu-id="5b8df-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="5b8df-112">I fanen **Brukere** legger du til brukeren eller organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5b8df-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brukere](media/environment-maker.png)

5. <span data-ttu-id="5b8df-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5b8df-114">Select **Save**.</span></span>
6. <span data-ttu-id="5b8df-115">Brukeren må nå logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="5b8df-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="5b8df-116">Velg **Synkroniser** for å oppdatere brukerappene.</span><span class="sxs-lookup"><span data-stu-id="5b8df-116">Select **Sync** to update the user apps.</span></span>

    ![Synkroniser-knappen](media/get-more.png)

    <span data-ttu-id="5b8df-118">Når synkroniseringen er fullført, vises Talent på startsiden.</span><span class="sxs-lookup"><span data-stu-id="5b8df-118">After synchronization is completed, Talent will appear on the home page.</span></span>
