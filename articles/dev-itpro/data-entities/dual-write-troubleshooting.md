---
title: Feilsøkingsveiledning for dataintegrering
description: Dette emnet inneholder feilsøkingsinformasjon om dataintegrasjon mellom Microsoft Dynamics 365 for Finance and Operations og Common Data Service.
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797281"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="d8a6a-103">Feilsøkingsveiledning for dataintegrering</span><span class="sxs-lookup"><span data-stu-id="d8a6a-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="d8a6a-104">Aktivere Sporing for plugin-modul i Common Data Service og sjekke feildetaljene for dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="d8a6a-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="d8a6a-105">Hvis du står overfor et problem eller en feil med dobbel skriving-synkronisering, kan du undersøke feilene i sporingsloggen:</span><span class="sxs-lookup"><span data-stu-id="d8a6a-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="d8a6a-106">Før du kan inspisere feilene, må du aktivere sporing for plugin-modul ved hjelp av instruksjonene i [Registrere plugin](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) for å aktivere sporing for plugin-modul.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="d8a6a-107">Nå kan du inspisere feilene.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="d8a6a-108">Logg på Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="d8a6a-109">Klikk på innstillinger-ikonet (et tannhjul), og velg **Avanserte innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="d8a6a-110">I **Innstillinger**-menyen velger du **Tilpassing > Sporingslogg for plugin-modul**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="d8a6a-111">Klikk på typenavnet **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** for å vise feildetaljene.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="d8a6a-112">Sjekke feil ved synkronisering av dobbel skriving i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d8a6a-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="d8a6a-113">Du kan kontrollere feilene under testing ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="d8a6a-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="d8a6a-114">Logg på LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="d8a6a-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="d8a6a-115">Åpne LCS-prosjektet du har valgt til å utføre testing av dobbelt skriving.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="d8a6a-116">Gå til Skybaserte miljøer.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="d8a6a-117">Eksternt skrivebord til Finance and Operations VM ved hjelp av lokal konto som vises i LCS.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="d8a6a-118">Åpne hendelseslisten.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="d8a6a-119">Naviger til **Program- og tjenestelogger > Microsoft > Dynamics > AX-DualWriteSync > Drift**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="d8a6a-120">Feilene og detaljene vises.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="d8a6a-121">Slik fjerner du tilknytningen til og kobler til et annet Common Data Service-miljø fra Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d8a6a-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="d8a6a-122">Du kan oppdatere koblinger ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="d8a6a-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="d8a6a-123">Naviger til Finance and Operations-miljøet.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="d8a6a-124">Åpne Databehandling.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-124">Open Data Management.</span></span>
+ <span data-ttu-id="d8a6a-125">Klikk på **Kobling til CDS for apper**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="d8a6a-126">Velg alle kjørende tilordninger, og klikk på **Stopp**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="d8a6a-127">Velg alle tilordningene, og klikk på **Slett**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d8a6a-128">Alternativet **Slett** vises ikke hvis malen **CustomerV3-Account** er valgt.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="d8a6a-129">Opphev merkingen om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-129">Unselect it if needed.</span></span> <span data-ttu-id="d8a6a-130">**CustomerV3-Account** er en eldre klargjort mal og fungerer med Kundeemne til kontanter-løsningen.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="d8a6a-131">Fordi den er globalt lansert, viser den under alle maler.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="d8a6a-132">Klikk **Koble fra miljø**.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="d8a6a-133">Klikk **Ja** for bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="d8a6a-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="d8a6a-134">Hvis du vil koble til det nye miljøet, følger du trinnene i [installasjonsveiledningen](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="d8a6a-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

