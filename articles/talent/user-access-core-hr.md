---
title: Brukeren har tilgang til Human Resources, men ikke Onboard eller Attract
description: Dette emnet forklarer hvordan du løser problemet der en bruker får tilgang til Microsoft Dynamics 365 Talent – Human Resources, men ikke får tilgang til Attract eller Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462097"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="06619-103">Brukeren har tilgang til Human Resources, men ikke Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="06619-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06619-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="06619-104">**Environment details**</span></span>

- <span data-ttu-id="06619-105">Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.</span><span class="sxs-lookup"><span data-stu-id="06619-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="06619-106">Bruker A la til bruker B som bruker i Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="06619-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="06619-107">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="06619-107">**Issue**</span></span>

<span data-ttu-id="06619-108">Bruker B har tilgang til Human Resources, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="06619-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="06619-109">Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.</span><span class="sxs-lookup"><span data-stu-id="06619-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="06619-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="06619-110">**Solution**</span></span>

<span data-ttu-id="06619-111">Bruker B må tilordnes rettigheter til å vise Microsoft Power Apps-miljøet som bruker A opprettet under klargjøringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="06619-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="06619-112">Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="06619-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="06619-113">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="06619-113">**Long-term solution**</span></span>

<span data-ttu-id="06619-114">Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="06619-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
