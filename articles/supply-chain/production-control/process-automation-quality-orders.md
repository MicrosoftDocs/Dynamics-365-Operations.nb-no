---
title: Starte prosessautomeringsflyter for å opprette kvalitetsordrer
description: Dette emnet gir ressurser for bruk av Power Automate til å automatisere forretningsprosesser ved hjelp av eksempelet på kvalitetsordrer.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115207"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="3708d-103">Starte prosessautomeringsflyter for å opprette kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="3708d-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="3708d-104">Organisasjoner har et økende behov for å automatisere standard forretningsprosesser, gi bedre samhandling med staben og benytte forskjellige datasignaler og systemer til å drive forretningsprosesser automatisk.</span><span class="sxs-lookup"><span data-stu-id="3708d-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="3708d-105">Med automatisering med robotteknologi (RPA) og Microsoft Power Automate kan selskaper bruke en kodeløs opplevelse til å automatisere gjentagende prosesser, og dermed oppnå effektivitet og nøyaktighet.</span><span class="sxs-lookup"><span data-stu-id="3708d-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="3708d-106">Den nedlastbare malen for automatisk løsning for Supply Chain Management viser hvordan Power Automate kan brukes til å automatisere forretningsprosessene ved å bruke kvalitetsordrer som et eksempel.</span><span class="sxs-lookup"><span data-stu-id="3708d-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="3708d-107">Du kan laste ned malen for automatisk løsning [her](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="3708d-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="3708d-108">Hvis du vil ha en oversikt over denne funksjonen og egenskapene, kan du se følgende video: [Bruke RPA til å opprette kvalitetsordrer i Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="3708d-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="3708d-109">![Automatiseringsalternativer med RPA](media/rpa-automation-options.png "Automatiseringsalternativer med RPA")</span><span class="sxs-lookup"><span data-stu-id="3708d-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="3708d-110">Power Automate-løsningsmalen omfatter en skyautomatiseringsflyt og en automatisk flyt på skrivebord som automatiserer opprettelsen av kvalitetsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3708d-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="3708d-111">Automatiseringen kan startes som svar på mange hendelser og signaler, inkludert brukerinndata eller maskinsignaler (Tingenes Internett (IoT)).</span><span class="sxs-lookup"><span data-stu-id="3708d-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="3708d-112">Power Application-eksemplet *Q-order* er inkludert i løsningsmalen.</span><span class="sxs-lookup"><span data-stu-id="3708d-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="3708d-113">Den gir brukeren muligheten til å skanne en QR-kode for vare, angi antall og legge ved bilder ved hjelp av et kamera.</span><span class="sxs-lookup"><span data-stu-id="3708d-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="3708d-114">Løsningsparametere er inkludert for å konfigurere automatisering for et bestemt brukssted i et produksjonsanlegg.</span><span class="sxs-lookup"><span data-stu-id="3708d-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="3708d-115">![Opprett kvalitetsordre](media/rpa-create-quality-roder.png "Opprett kvalitetsordre")</span><span class="sxs-lookup"><span data-stu-id="3708d-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="3708d-116">Hvis du vil ha en trinnvis veiledning om hvordan du laster ned, installerer og bruker eksempelløsningen til å automatisere oppretting av kvalitetsordrer, kan du se [Automatisere oppretting av kvalitetsordrer på Dynamics 365 Supply Chain Management med automatisering med robotteknologi ved hjelp av Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="3708d-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>

