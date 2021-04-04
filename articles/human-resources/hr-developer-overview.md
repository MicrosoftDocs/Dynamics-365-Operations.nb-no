---
title: Oversikt over utvikling
description: Denne utviklerveiledningen har en referanse til et API og egendefinerte felt. Den inneholder også informasjon om integrering med andre apper.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e390592b000c8f6006aa489fd3823c4f15cb2cb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467801"
---
# <a name="development-overview"></a><span data-ttu-id="23461-104">Oversikt over utvikling</span><span class="sxs-lookup"><span data-stu-id="23461-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="23461-105">Denne utviklerveiledningen har en referanse til et API og egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="23461-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="23461-106">Den inneholder også informasjon om integrering med andre apper.</span><span class="sxs-lookup"><span data-stu-id="23461-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="23461-107">Oversikt</span><span class="sxs-lookup"><span data-stu-id="23461-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="23461-108">Utvide med Power Apps og Power Automate</span><span class="sxs-lookup"><span data-stu-id="23461-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="23461-109">Human Resources-enheter i Dataverse</span><span class="sxs-lookup"><span data-stu-id="23461-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="23461-110">Tilpassede felt</span><span class="sxs-lookup"><span data-stu-id="23461-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="23461-111">Konfigurere dataintegrering</span><span class="sxs-lookup"><span data-stu-id="23461-111">Set up data integration</span></span>
  - [<span data-ttu-id="23461-112">Velg en dataintegreringsteknologi</span><span class="sxs-lookup"><span data-stu-id="23461-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="23461-113">Konfigurere Dataverse-integrering</span><span class="sxs-lookup"><span data-stu-id="23461-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="23461-114">Konfigurere integrering med Finance</span><span class="sxs-lookup"><span data-stu-id="23461-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="23461-115">Konfigurere integrering med Dayforce</span><span class="sxs-lookup"><span data-stu-id="23461-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="23461-116">Opprette en app for regelmessig dataeksport</span><span class="sxs-lookup"><span data-stu-id="23461-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="23461-117">Integrere med Office</span><span class="sxs-lookup"><span data-stu-id="23461-117">Integrate with Office</span></span>
    - [<span data-ttu-id="23461-118">Opplæring i Office-integrering</span><span class="sxs-lookup"><span data-stu-id="23461-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="23461-119">Oppdatere enhetsdata i Excel</span><span class="sxs-lookup"><span data-stu-id="23461-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="23461-120">Opprette opplevelser for Åpne i Excel</span><span class="sxs-lookup"><span data-stu-id="23461-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="23461-121">Feilsøke Office-integrering</span><span class="sxs-lookup"><span data-stu-id="23461-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="23461-122">API-referanse for enhet</span><span class="sxs-lookup"><span data-stu-id="23461-122">Entity API reference</span></span>
  - [<span data-ttu-id="23461-123">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="23461-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="23461-124">Enheter</span><span class="sxs-lookup"><span data-stu-id="23461-124">Entities</span></span>
    - [<span data-ttu-id="23461-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="23461-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="23461-126">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="23461-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="23461-127">Se også</span><span class="sxs-lookup"><span data-stu-id="23461-127">See also</span></span>

- [<span data-ttu-id="23461-128">Hva er nytt eller endret i Human Resources</span><span class="sxs-lookup"><span data-stu-id="23461-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="23461-129">Administratorveiledning</span><span class="sxs-lookup"><span data-stu-id="23461-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="23461-130">Brukerveiledning</span><span class="sxs-lookup"><span data-stu-id="23461-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]