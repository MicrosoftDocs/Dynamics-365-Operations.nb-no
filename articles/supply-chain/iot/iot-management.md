---
title: Overvåke og behandle IoT-intelligens
description: Dette emnet forklarer hvordan du overvåker og administrerer IoT-intelligens.
author: robinarh
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813081"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="34b06-103">Overvåke og behandle IoT-intelligens</span><span class="sxs-lookup"><span data-stu-id="34b06-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34b06-104">Dette emnet forklarer hvordan du overvåker og administrerer IoT-intelligens.</span><span class="sxs-lookup"><span data-stu-id="34b06-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="34b06-105">Overvåkingsscenarioer i Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="34b06-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="34b06-106">Du kan overvåke behandling av IoT-intelligens fra flere steder:</span><span class="sxs-lookup"><span data-stu-id="34b06-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="34b06-107">**Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Varslinger** – Vis listen over uløste varslinger.</span><span class="sxs-lookup"><span data-stu-id="34b06-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="34b06-108">**Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Lukkede varslinger** – Vis listen over varslinger som er løst eller forkastet.</span><span class="sxs-lookup"><span data-stu-id="34b06-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="34b06-109">**Moduler \> Produksjonskontroll \> Forespørsler og rapporter \> IoT-intelligens \> Måleverdinøkler** – Vis måleverdinøklene for tidsoversiktsdiagrammet **Ressursstatus**.</span><span class="sxs-lookup"><span data-stu-id="34b06-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="34b06-110">**Moduler \> Produksjonskontroll \> Produksjonsutførelse \> Ressursstatus** – Spor spesifikke måleverdier ved hjelp av dialogboksen **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="34b06-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="34b06-111">Hvis et scenario oppdager et unntak, viser en varsling detaljer om unntaket.</span><span class="sxs-lookup"><span data-stu-id="34b06-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="34b06-112">**Arbeidsområder \> Produksjonsstyring \> Varslinger** – Vis listen over uløste varslinger.</span><span class="sxs-lookup"><span data-stu-id="34b06-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="34b06-113">Endre et kjørende scenario for IoT-intelligens</span><span class="sxs-lookup"><span data-stu-id="34b06-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="34b06-114">Når et scenario kjøres, kan du gjøre disse endringene:</span><span class="sxs-lookup"><span data-stu-id="34b06-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="34b06-115">Legge til nye definisjoner for sensorskjema.</span><span class="sxs-lookup"><span data-stu-id="34b06-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="34b06-116">Velge nye dataverdier for signaler.</span><span class="sxs-lookup"><span data-stu-id="34b06-116">Select new signal data values.</span></span>
+ <span data-ttu-id="34b06-117">Avbryte valget av eksisterende signaldataverdier.</span><span class="sxs-lookup"><span data-stu-id="34b06-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="34b06-118">Legge til og tilordne nye signaldataverdier.</span><span class="sxs-lookup"><span data-stu-id="34b06-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="34b06-119">Oppdatere terskelverdier.</span><span class="sxs-lookup"><span data-stu-id="34b06-119">Update threshold values.</span></span>

<span data-ttu-id="34b06-120">Når et scenario kjøres, kan du ikke gjøre disse endringene:</span><span class="sxs-lookup"><span data-stu-id="34b06-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="34b06-121">Slette eller endre skjemadefinisjoner som for tiden brukes av et aktivert scenario.</span><span class="sxs-lookup"><span data-stu-id="34b06-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="34b06-122">Endre de valgte skjemabanene for det aktiverte .</span><span class="sxs-lookup"><span data-stu-id="34b06-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="34b06-123">Simuleringsalternativer</span><span class="sxs-lookup"><span data-stu-id="34b06-123">Simulation options</span></span>

<span data-ttu-id="34b06-124">Du kan simulere fabrikkmaskinsignaler.</span><span class="sxs-lookup"><span data-stu-id="34b06-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="34b06-125">Hvis du vil ha mer informasjon, kan du se disse emnene:</span><span class="sxs-lookup"><span data-stu-id="34b06-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="34b06-126">Koble IoT DevKit AZ3166 til Azure IoT-hub</span><span class="sxs-lookup"><span data-stu-id="34b06-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="34b06-127">Koble Raspberry PI online-simulator til Azure IoT-hub (Node.js)</span><span class="sxs-lookup"><span data-stu-id="34b06-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="34b06-128">Oversikt over løsningsakselerator for enhetssimulering</span><span class="sxs-lookup"><span data-stu-id="34b06-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]