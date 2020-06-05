---
title: Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten
description: Dette emnet beskriver prosessen for å fullføre ferdige produkter på en produksjonsordre til lager når et nummerskilt styrer lokasjonen.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 74e1e30f5afe51cd0ecec2530ffcb9a59eec5fee
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367251"
---
# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="7e060-103">Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten</span><span class="sxs-lookup"><span data-stu-id="7e060-103">Report as finished to a license plate controlled location from the Job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e060-104">Prosessen som kalles Ferdigmelding, fullfører ferdig produkter på en produksjonsordre til lageret.</span><span class="sxs-lookup"><span data-stu-id="7e060-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="7e060-105">Hvis det ferdige produktet er aktivert for de avanserte lagerprosessene, blir produktet rapportert som ferdig til en lokasjon som kalles produksjonsutleveringssted.</span><span class="sxs-lookup"><span data-stu-id="7e060-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="7e060-106">Hvis du vil ha informasjon om hvordan du definerer produksjonsutleveringssted, kan du se [Produksjonsutleveringssted](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="7e060-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="7e060-107">Hvis produksjonsutleveringsstedet er nummerskiltkontrollert, må det oppgis et nummerskilt ved rapportering som fullført.</span><span class="sxs-lookup"><span data-stu-id="7e060-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="7e060-108">Feltet **Nummerskilt** vises i meldingen **Rapportfremdrift** på siden **Jobbkortenhet**.</span><span class="sxs-lookup"><span data-stu-id="7e060-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="7e060-109">Feltet er bare synlig i **Rapportfremdrift**-ledeteksten når rapportering på siste operasjon av produksjonsordren og varen for produksjonsordren er aktivert for lagerstyringsprosessene.</span><span class="sxs-lookup"><span data-stu-id="7e060-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span>

<span data-ttu-id="7e060-110">Det er to alternativer for å formidle nummerskiltet:</span><span class="sxs-lookup"><span data-stu-id="7e060-110">There are two options for providing the license plate:</span></span>

- <span data-ttu-id="7e060-111">Brukeren velger et eksisterende nummerskilt i nummerskiltfeltet.</span><span class="sxs-lookup"><span data-stu-id="7e060-111">The user selects an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="7e060-112">Nummerskiltet genereres automatisk fra en nummerserie og hentes som standard til nummerskiltfeltet.</span><span class="sxs-lookup"><span data-stu-id="7e060-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="7e060-113">Alternativet for å få nummerskiltet genererert automatisk, konfigureres ved å velge alternativet **Generer nummerskilt** på siden **Konfigurer jobbkort for enheter**.</span><span class="sxs-lookup"><span data-stu-id="7e060-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
