---
title: Vanlige spørsmål om arbeidsflyt
description: Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
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
ms.openlocfilehash: 7ca04433937d0d7a16b450f190cd3814533e270d
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741062"
---
# <a name="workflow-faq"></a><span data-ttu-id="8421d-103">Vanlige spørsmål om arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="8421d-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8421d-104">Dette emnet gir svar på vanlige spørsmål om arbeidsflytsystemet i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8421d-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="8421d-105">Hvorfor mottas flere varslinger når et arbeidselement avvises?</span><span class="sxs-lookup"><span data-stu-id="8421d-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="8421d-106">Når et arbeidselement avvises, fullføres dette arbeidselementet som avvist.</span><span class="sxs-lookup"><span data-stu-id="8421d-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="8421d-107">Et annet arbeidselement opprettes og tilordnes til avsenderen.</span><span class="sxs-lookup"><span data-stu-id="8421d-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="8421d-108">Dette betyr at det er en melding til avsenderen for det avviste arbeidselementet og en egen melding til brukeren som er tilordnet til det nye "bedt om endring"-arbeidselementet.</span><span class="sxs-lookup"><span data-stu-id="8421d-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="8421d-109">Hver varsling er for et annet arbeidselement, men likheten kan føre til forvirring.</span><span class="sxs-lookup"><span data-stu-id="8421d-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="8421d-110">Vi ser på måter å forbedre dette på i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="8421d-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="8421d-111">Hvorfor mislykkes arbeidsflyteksportene mine?</span><span class="sxs-lookup"><span data-stu-id="8421d-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="8421d-112">Det er for øyeblikket en begrensning i funksjonen for arbeidsflyteksport som hindrer at arbeidsflytnavn overskrider 48 tegn.</span><span class="sxs-lookup"><span data-stu-id="8421d-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="8421d-113">Hvis du bruker et navn som er lengre enn 48 tegn, kan det resultere i feilen «Serveren kan ikke godkjenne forespørselen» og/eller hindre at en fil blir eksportert uten en filtype.</span><span class="sxs-lookup"><span data-stu-id="8421d-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="8421d-114">Følgende blogginnlegg gir mer informasjon [Feilsøke arbeidsflyteksport](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="8421d-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="8421d-115">Kan innsenderen av en arbeidsflyt også godkjenne arbeidsflyten?</span><span class="sxs-lookup"><span data-stu-id="8421d-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="8421d-116">Ja, en innsender av en arbeidsflyt kan også godkjenne arbeidsflyten hvis den er konfigurert slik.</span><span class="sxs-lookup"><span data-stu-id="8421d-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="8421d-117">Du kan unngå denne virkemåten ved å sette **Arbeidsflytparametere > Generelt > Godkjenner > Sperr godkjenning av innsender** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8421d-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="8421d-118">Kan jeg legge til varsler i arbeidsflyter for å gi brukere varslinger?</span><span class="sxs-lookup"><span data-stu-id="8421d-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="8421d-119">Det er viktig å være oppmerksom på følgende vedrørende tilføying av varsler i arbeidsflyter for å gi varslinger:</span><span class="sxs-lookup"><span data-stu-id="8421d-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="8421d-120">Varsler i forhold til arbeidsflytvarsling</span><span class="sxs-lookup"><span data-stu-id="8421d-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="8421d-121">Du kan konfigurere varsler for postendringer.</span><span class="sxs-lookup"><span data-stu-id="8421d-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="8421d-122">Arbeidsflyter endrer poster, så du kan konfigurere et varsel som er knyttet til en postendring som skyldes en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="8421d-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="8421d-123">Siden arbeidsflyter har ulike innebygde varslingsalternativer, er det imidlertid ikke best å bruke varsler.</span><span class="sxs-lookup"><span data-stu-id="8421d-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="8421d-124">Standardvarslinger fra arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="8421d-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="8421d-125">Arbeidsflyter har innebygde e-postvarslinger.</span><span class="sxs-lookup"><span data-stu-id="8421d-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="8421d-126">En kunde kan konfigurere varslingene slik at brukerne får tilsendt e-post.</span><span class="sxs-lookup"><span data-stu-id="8421d-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="8421d-127">Disse varslingene resulterer ikke i Handlingssenter-meldinger for brukere.</span><span class="sxs-lookup"><span data-stu-id="8421d-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="8421d-128">I en fremtidig oppdatering kommer vi til å legge til en Handlingssenter-melding slik at en bruker tilordnes et arbeidselement for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="8421d-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="8421d-129">Legge til varslinger i arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="8421d-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="8421d-130">Handlingssenter-meldinger kan opprettes for bestemte brukere, for eksempel en melding som er opprettet fra en arbeidsflyt i X++.</span><span class="sxs-lookup"><span data-stu-id="8421d-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="8421d-131">[Arbeidsflyter har forretningshendelser](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) som kunden kan bruke til å utløse flyter som har varslingene de ser etter.</span><span class="sxs-lookup"><span data-stu-id="8421d-131">[Workflows have Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="8421d-132">Hvis en bruker ikke får riktig varsling fra handlingssenteret når de tilordnes et arbeidselement for arbeidsflyt, bruker du [Forretningshendelser for arbeidsflyt](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) med Microsoft Flow til å gi flere eller andre varslinger.</span><span class="sxs-lookup"><span data-stu-id="8421d-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
