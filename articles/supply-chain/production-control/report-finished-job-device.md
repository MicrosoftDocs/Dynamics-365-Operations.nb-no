---
title: Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten
description: Dette emnet beskriver prosessen for å fullføre ferdige produkter på en produksjonsordre til lager når et nummerskilt styrer lokasjonen.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995148"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="482d9-103">Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="482d9-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="482d9-104">Prosessen som kalles Ferdigmelding, fullfører ferdig produkter på en produksjonsordre til lageret.</span><span class="sxs-lookup"><span data-stu-id="482d9-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="482d9-105">Hvis det ferdige produktet er aktivert for de avanserte lagerprosessene, blir produktet rapportert som ferdig til en lokasjon som kalles produksjonsutleveringssted.</span><span class="sxs-lookup"><span data-stu-id="482d9-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="482d9-106">Hvis du vil ha informasjon om hvordan du definerer produksjonsutleveringssted, kan du se [Produksjonsutleveringssted](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="482d9-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="482d9-107">Du må velge et eksisterende skiltnummeret for å fullføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="482d9-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="482d9-108">Hvis produksjonsutleveringsstedet er konfigurert for sporing etter nummerskilt, må et skiltnummer inkluderes ved rapportering av produksjonsutleveringsstedet som ferdig.</span><span class="sxs-lookup"><span data-stu-id="482d9-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="482d9-109">Feltet **Nummerskilt** vises i meldingen **Rapportfremdrift** på siden **Jobbkortenhet**.</span><span class="sxs-lookup"><span data-stu-id="482d9-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="482d9-110">Feltet vises bare i meldingen **Rapportfremdrift** ved rapportering om den siste operasjonen i produksjonsordren.</span><span class="sxs-lookup"><span data-stu-id="482d9-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="482d9-111">Feltet vises bare hvis varen for produksjonsordren er aktivert for lagerstyrings prosessene.</span><span class="sxs-lookup"><span data-stu-id="482d9-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
