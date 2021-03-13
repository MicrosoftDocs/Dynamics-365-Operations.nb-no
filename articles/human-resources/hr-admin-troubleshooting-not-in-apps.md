---
title: Human Resources vises ikke i Microsoft Dynamics 365-apper
description: Denne artikkelen forklarer hva du gjør hvis kunden ikke kan du se appen Microsoft Dynamics 365 Human Resources blant Microsoft Dynamics 365-appene.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d78199cf0e76ffd0676a26961a8e646938dc7333
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113749"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="3b515-103">Human Resources vises ikke i Microsoft Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="3b515-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="3b515-104">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="3b515-104">**Issue**</span></span>

<span data-ttu-id="3b515-105">Kunden kan ikke se Dynamics 365 Human Resources blant Microsoft Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="3b515-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="3b515-106">**Oppløsning**</span><span class="sxs-lookup"><span data-stu-id="3b515-106">**Resolution**</span></span>

<span data-ttu-id="3b515-107">Brukeren må legges til Miljøskaper-rollen for miljøet i Microsoft Power Apps.</span><span class="sxs-lookup"><span data-stu-id="3b515-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="3b515-108">Admin-brukeren som har en Power Apps Plan 2-lisens, må åpne [Power Apps-administrasjonsportalen](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="3b515-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="3b515-109">Velg **Miljøer**, og velg riktig miljø for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="3b515-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="3b515-110">I fanen **Sikkerhet** i fanen **Miljøroller** velger du **Miljøskaper**.</span><span class="sxs-lookup"><span data-stu-id="3b515-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Fanen Miljøroller](media/environment-roles.png)

4. <span data-ttu-id="3b515-112">I fanen **Brukere** legger du til brukeren eller organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="3b515-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Fanen Brukere](media/environment-maker.png)

5. <span data-ttu-id="3b515-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="3b515-114">Select **Save**.</span></span>

6. <span data-ttu-id="3b515-115">Brukeren må nå logge på [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="3b515-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="3b515-116">Velg **Synkroniser** for å oppdatere brukerappene.</span><span class="sxs-lookup"><span data-stu-id="3b515-116">Select **Sync** to update the user apps.</span></span>

    ![Synkroniser-knappen](media/get-more.png)

    <span data-ttu-id="3b515-118">Når synkroniseringen er fullført, vises Human Resources på startsiden.</span><span class="sxs-lookup"><span data-stu-id="3b515-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
