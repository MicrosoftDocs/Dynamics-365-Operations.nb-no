---
title: Feilsøkingsveiledning for dataintegrering
description: Dette emnet inneholder feilsøkingsinformasjon om dataintegrasjon mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771031"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="822b2-103">Feilsøkingsveiledning for dataintegrering</span><span class="sxs-lookup"><span data-stu-id="822b2-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="822b2-104">Aktivere sporingslogger for plugin-modul i Common Data Service og sjekke feildetaljene for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="822b2-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="822b2-105">Hvis det oppstår et problem eller en feil med synkronisering av dobbel skriving, følger du denne fremgangsmåten for å kontrollere feilene i sporingsloggen.</span><span class="sxs-lookup"><span data-stu-id="822b2-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="822b2-106">Før du kan kontrollere feilene, må du aktivere sporingslogger for plugin-modul.</span><span class="sxs-lookup"><span data-stu-id="822b2-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="822b2-107">Hvis du vil ha instruksjoner, kan du se delen "Vise sporingslogger" i [Opplæring: Skrive og registrere en plugin-modul](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="822b2-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="822b2-108">Nå kan du inspisere feilene.</span><span class="sxs-lookup"><span data-stu-id="822b2-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="822b2-109">Logg på Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="822b2-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="822b2-110">Velg **Innstillinger**-knappen (tannhjulsymbolet), og velg deretter **Avanserte innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="822b2-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="822b2-111">I **Innstillinger**-menyen velger du **Tilpassing \> Sporingslogg for plugin-modul**.</span><span class="sxs-lookup"><span data-stu-id="822b2-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="822b2-112">Velg **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** som typenavn for å vise feildetaljene.</span><span class="sxs-lookup"><span data-stu-id="822b2-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="822b2-113">Kontrollere feil ved synkronisering av dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="822b2-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="822b2-114">Følg disse trinnene for å undersøke feil under testing.</span><span class="sxs-lookup"><span data-stu-id="822b2-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="822b2-115">Logg på Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="822b2-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="822b2-116">Åpne LCS-prosjektet for å utføre testing av dobbelt skriving.</span><span class="sxs-lookup"><span data-stu-id="822b2-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="822b2-117">Velg **Skybaserte miljøer**.</span><span class="sxs-lookup"><span data-stu-id="822b2-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="822b2-118">Opprett en eksternt skrivebord-tilkobling til den virtuelle maskinen for programmet ved hjelp av den lokale kontoen som vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="822b2-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="822b2-119">Åpne hendelseslisten.</span><span class="sxs-lookup"><span data-stu-id="822b2-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="822b2-120">Gå til **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.</span><span class="sxs-lookup"><span data-stu-id="822b2-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="822b2-121">Feilene og detaljene vises.</span><span class="sxs-lookup"><span data-stu-id="822b2-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="822b2-122">Fjerne en tilknytning til Common Data Service-miljøet fra programmet, og koble til et annet miljø</span><span class="sxs-lookup"><span data-stu-id="822b2-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="822b2-123">Gjør følgende for å oppdatere koblinger:</span><span class="sxs-lookup"><span data-stu-id="822b2-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="822b2-124">Gå til programmiljøet.</span><span class="sxs-lookup"><span data-stu-id="822b2-124">Go to the application environment.</span></span>
2. <span data-ttu-id="822b2-125">Åpne Databehandling.</span><span class="sxs-lookup"><span data-stu-id="822b2-125">Open Data Management.</span></span>
3. <span data-ttu-id="822b2-126">Velg **Kobling til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="822b2-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="822b2-127">Velg alle tilordningene som kjører, og velg deretter **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="822b2-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="822b2-128">Velg alle tilordningene, og velg deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="822b2-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="822b2-129">Alternativet **Slett** vises ikke hvis malen **CustomerV3-Account** er valgt.</span><span class="sxs-lookup"><span data-stu-id="822b2-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="822b2-130">Fjern valget av denne malen etter behov.</span><span class="sxs-lookup"><span data-stu-id="822b2-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="822b2-131">**CustomerV3-Account** er en eldre klargjort mal og fungerer med Kundeemne til kontanter-løsningen.</span><span class="sxs-lookup"><span data-stu-id="822b2-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="822b2-132">Fordi den er globalt lansert, viser den under alle maler.</span><span class="sxs-lookup"><span data-stu-id="822b2-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="822b2-133">Klikk **Koble fra miljø**.</span><span class="sxs-lookup"><span data-stu-id="822b2-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="822b2-134">Velg **Ja** for å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="822b2-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="822b2-135">Hvis du vil koble til det nye miljøet, følger du trinnene i [installasjonsveiledningen](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="822b2-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
