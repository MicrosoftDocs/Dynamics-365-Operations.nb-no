---
title: Brukeren har tilgang til Core HR, men ikke Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 Talent – Core HR, men får tilgang til Attract eller Onboard.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009312"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a><span data-ttu-id="f5823-103">Brukeren har tilgang til Core HR, men ikke Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="f5823-103">User can access Core HR but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5823-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="f5823-104">**Environment details**</span></span>

- <span data-ttu-id="f5823-105">Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.</span><span class="sxs-lookup"><span data-stu-id="f5823-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="f5823-106">Bruker A la til bruker B som bruker i Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="f5823-106">User A added user B as a user to Microsoft Dynamics 365 Talent: Core HR.</span></span>

<span data-ttu-id="f5823-107">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="f5823-107">**Issue**</span></span>

<span data-ttu-id="f5823-108">Bruker B har tilgang til Core HR, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="f5823-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="f5823-109">Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.</span><span class="sxs-lookup"><span data-stu-id="f5823-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="f5823-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="f5823-110">**Solution**</span></span>

<span data-ttu-id="f5823-111">Bruker B må tilordnes rettigheter til å vise Microsoft PowerApps-miljøet som bruker A opprettet under klargjøringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f5823-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="f5823-112">Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="f5823-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="f5823-113">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="f5823-113">**Long-term solution**</span></span>

<span data-ttu-id="f5823-114">Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Core HR.</span><span class="sxs-lookup"><span data-stu-id="f5823-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
