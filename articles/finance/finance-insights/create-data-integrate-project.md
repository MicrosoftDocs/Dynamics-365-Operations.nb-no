---
title: Opprette et dataintegratorprosjekt (forhåndsversjon)
description: Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009457"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="cc630-103">Opprette et dataintegratorprosjekt (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="cc630-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cc630-104">Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.</span><span class="sxs-lookup"><span data-stu-id="cc630-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="cc630-105">Logg på Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cc630-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="cc630-106">Gå til **Arbeidsområder \> Databehandling**, og velg **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="cc630-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="cc630-107">Vent til alle dataenhetene er oppdatert før du går videre til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="cc630-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="cc630-108">Åpne [Power Apps-portalen](https://make.powerapps.com/), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="cc630-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="cc630-109">Velg det aktuelle miljøet.</span><span class="sxs-lookup"><span data-stu-id="cc630-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="cc630-110">Velg **Data \> Tilkoblinger** i venstre navigasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="cc630-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="cc630-111">Koble til riktige forekomster av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="cc630-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="cc630-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc630-112">Dynamics 365</span></span>
        - <span data-ttu-id="cc630-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="cc630-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="cc630-114">Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="cc630-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="cc630-115">Velg **Dataintegrator**.</span><span class="sxs-lookup"><span data-stu-id="cc630-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="cc630-116">Velg **Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="cc630-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="cc630-117">Velg **Nytt tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="cc630-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="cc630-118">Skriv inn et navn for tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="cc630-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="cc630-119">Velg de riktige tilkoblingene for følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="cc630-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="cc630-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc630-120">Dynamics 365</span></span>
        - <span data-ttu-id="cc630-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="cc630-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="cc630-122">Velg den aktuelle organisasjonstilordningen.</span><span class="sxs-lookup"><span data-stu-id="cc630-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="cc630-123">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="cc630-123">Select **Create**.</span></span>

5. <span data-ttu-id="cc630-124">Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="cc630-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="cc630-125">Opprett dataintegrasjonsprosjekter for følgende maler ved hjelp av tilkoblingssettet du nettopp opprettet:</span><span class="sxs-lookup"><span data-stu-id="cc630-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="cc630-126">Resultater av innsikt i kundebetaling (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cc630-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="cc630-127">Resultater av tidsserie for kontantstrøm (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cc630-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="cc630-128">Resultater av tidsserie for budsjett (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="cc630-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="cc630-129">Angi den riktige planleggingen for hvert prosjekt.</span><span class="sxs-lookup"><span data-stu-id="cc630-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="cc630-130">Hvis du ikke ser de nødvendige enhetene i CDS, kan du gå til **Kreditt og innkreving > Oppsett > Finance Insights > Parametere for økonomisk innsikt**, aktivere funksjonen for kundebetalingsprognoser og klikke på knappen **Opprett prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="cc630-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="cc630-131">Når distribusjonen av modell for kunstig intelligens er fullført (vellykket eller mislykket), vil CDS-enhetene som kreves for å opprette integrering, bli distribuert i CDS.</span><span class="sxs-lookup"><span data-stu-id="cc630-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="cc630-132">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="cc630-132">Privacy notice</span></span>

<span data-ttu-id="cc630-133">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="cc630-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
