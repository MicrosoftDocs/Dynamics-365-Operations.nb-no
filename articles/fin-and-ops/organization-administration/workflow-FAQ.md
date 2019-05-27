---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509297"
---
# <a name="workflow-system"></a><span data-ttu-id="9cd58-103">Arbeidsflytsystem</span><span class="sxs-lookup"><span data-stu-id="9cd58-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cd58-104">Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9cd58-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="9cd58-105">Varslinger</span><span class="sxs-lookup"><span data-stu-id="9cd58-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="9cd58-106">Hvorfor mottas flere varslinger når et arbeidselement avvises?</span><span class="sxs-lookup"><span data-stu-id="9cd58-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="9cd58-107">Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist.</span><span class="sxs-lookup"><span data-stu-id="9cd58-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="9cd58-108">Et annet arbeidselement opprettes og tilordnes til avsenderen.</span><span class="sxs-lookup"><span data-stu-id="9cd58-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="9cd58-109">Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet.</span><span class="sxs-lookup"><span data-stu-id="9cd58-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="9cd58-110">Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring.</span><span class="sxs-lookup"><span data-stu-id="9cd58-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="9cd58-111">Vi ser på måter å forbedre dette på i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="9cd58-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="9cd58-112">Hvorfor mislykkes arbeidsflyteksportene mine?</span><span class="sxs-lookup"><span data-stu-id="9cd58-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="9cd58-113">Det er for øyeblikket en begrensning i funksjonen for arbeidsflyteksport som hindrer at arbeidsflytnavn overskrider 48 tegn.</span><span class="sxs-lookup"><span data-stu-id="9cd58-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="9cd58-114">Hvis du bruker et navn som er lengre enn 48 tegn, kan det resultere i feilen «Serveren kan ikke godkjenne forespørselen» og/eller hindre at en fil blir eksportert uten en filtype.</span><span class="sxs-lookup"><span data-stu-id="9cd58-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="9cd58-115">Følgende blogginnlegg gir mer informasjon [Feilsøke arbeidsflyteksport](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="9cd58-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
