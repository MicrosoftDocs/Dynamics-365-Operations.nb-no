---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/01/2019
ms.locfileid: "773225"
---
# <a name="workflow-system"></a><span data-ttu-id="f3327-103">Arbeidsflytsystem</span><span class="sxs-lookup"><span data-stu-id="f3327-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3327-104">Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f3327-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="f3327-105">Varslinger</span><span class="sxs-lookup"><span data-stu-id="f3327-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="f3327-106">Hvorfor mottas flere varslinger når et arbeidselement avvises?</span><span class="sxs-lookup"><span data-stu-id="f3327-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="f3327-107">Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist.</span><span class="sxs-lookup"><span data-stu-id="f3327-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="f3327-108">Et annet arbeidselement opprettes og tilordnes til avsenderen.</span><span class="sxs-lookup"><span data-stu-id="f3327-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="f3327-109">Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet.</span><span class="sxs-lookup"><span data-stu-id="f3327-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="f3327-110">Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring.</span><span class="sxs-lookup"><span data-stu-id="f3327-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="f3327-111">Vi ser på måter å forbedre dette på i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="f3327-111">We are looking at ways to improve this in a future release.</span></span>
