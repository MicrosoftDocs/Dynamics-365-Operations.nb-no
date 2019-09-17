---
title: Brukeren har tilgang til Core HR, men ikke appen Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 for Talent Core HR, men får tilgang til appen Attract eller Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741730"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="6114c-103">Brukeren har tilgang til Core HR, men ikke appen Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="6114c-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6114c-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="6114c-104">**Environment details**</span></span>

- <span data-ttu-id="6114c-105">Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.</span><span class="sxs-lookup"><span data-stu-id="6114c-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="6114c-106">Bruker A la til bruker B som bruker i Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="6114c-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="6114c-107">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="6114c-107">**Issue**</span></span>

<span data-ttu-id="6114c-108">Bruker B har tilgang til Core HR, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="6114c-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="6114c-109">Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.</span><span class="sxs-lookup"><span data-stu-id="6114c-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="6114c-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="6114c-110">**Solution**</span></span>

<span data-ttu-id="6114c-111">Bruker B må tilordnes rettigheter til å vise Microsoft PowerApps-miljøet som bruker A opprettet under klargjøringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="6114c-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="6114c-112">Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="6114c-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="6114c-113">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="6114c-113">**Long-term solution**</span></span>

<span data-ttu-id="6114c-114">Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Core HR.</span><span class="sxs-lookup"><span data-stu-id="6114c-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
