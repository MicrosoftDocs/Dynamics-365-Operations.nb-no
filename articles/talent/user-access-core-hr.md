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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "855662"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="8acb2-103">Brukeren har tilgang til Core HR, men ikke appen Onboard eller Attract</span><span class="sxs-lookup"><span data-stu-id="8acb2-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8acb2-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="8acb2-104">**Environment details**</span></span>

- <span data-ttu-id="8acb2-105">Microsoft Dynamics Lifecycle Services-distribusjonen (LCS) ble utført av bruker A.</span><span class="sxs-lookup"><span data-stu-id="8acb2-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="8acb2-106">Bruker A la til bruker B som bruker i Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="8acb2-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="8acb2-107">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="8acb2-107">**Issue**</span></span>

<span data-ttu-id="8acb2-108">Bruker B har tilgang til Core HR, men har ikke tilgang til appene Talent: Attract eller Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="8acb2-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="8acb2-109">Når brukeren prøver å gå til **Opplev-appene**, kommer han eller hun til et prøvemiljø i stedet.</span><span class="sxs-lookup"><span data-stu-id="8acb2-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="8acb2-110">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="8acb2-110">**Solution**</span></span>

<span data-ttu-id="8acb2-111">Bruker B må tilordnes rettigheter til å vise Microsoft PowerApps-miljøet som bruker A opprettet under klargjøringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="8acb2-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="8acb2-112">Hvis du vil ha informasjon, kan du se delen "Gi tilgang til utviklingsmiljøet" i [Klargjøre Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="8acb2-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="8acb2-113">**Langsiktig løsning**</span><span class="sxs-lookup"><span data-stu-id="8acb2-113">**Long-term solution**</span></span>

<span data-ttu-id="8acb2-114">Microsoft vurderer å tilordne de nødvendige rettighetene til Onboard og Attract automatisk når en bruker legges til i Core HR.</span><span class="sxs-lookup"><span data-stu-id="8acb2-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
