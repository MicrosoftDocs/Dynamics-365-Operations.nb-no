---
title: Opprette et dataintegratorprosjekt (forhåndsversjon)
description: Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186474"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="3ebd0-103">Opprette et dataintegratorprosjekt (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="3ebd0-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3ebd0-104">Dette emnet forklarer hvordan du oppretter et dataintegratorprosjekt.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="3ebd0-105">Logg på Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="3ebd0-106">Gå til **Arbeidsområder \> Databehandling**, og velg **Dataenheter**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="3ebd0-107">Vent til alle dataenhetene er oppdatert før du går videre til neste trinn.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="3ebd0-108">Åpne [Power Apps-portalen](https://make.powerapps.com/), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="3ebd0-109">Velg det aktuelle miljøet.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="3ebd0-110">Velg **Data \> Tilkoblinger** i venstre navigasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="3ebd0-111">Koble til riktige forekomster av følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="3ebd0-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3ebd0-112">Dynamics 365</span></span>
        - <span data-ttu-id="3ebd0-113">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="3ebd0-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="3ebd0-114">Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="3ebd0-115">Velg **Dataintegrator**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="3ebd0-116">Velg **Tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="3ebd0-117">Velg **Nytt tilkoblingssett**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="3ebd0-118">Skriv inn et navn for tilkoblingen.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="3ebd0-119">Velg de riktige tilkoblingene for følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="3ebd0-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="3ebd0-120">Dynamics 365</span></span>
        - <span data-ttu-id="3ebd0-121">Dynamics 365 for Fin & Ops</span><span class="sxs-lookup"><span data-stu-id="3ebd0-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="3ebd0-122">Velg den aktuelle organisasjonstilordningen.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="3ebd0-123">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-123">Select **Create**.</span></span>

5. <span data-ttu-id="3ebd0-124">Åpne [Power Apps-miljøene](https://admin.powerapps.com/environments), og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="3ebd0-125">Opprett dataintegrasjonsprosjekter for følgende maler ved hjelp av tilkoblingssettet du nettopp opprettet:</span><span class="sxs-lookup"><span data-stu-id="3ebd0-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="3ebd0-126">Resultater av innsikt i kundebetaling (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3ebd0-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="3ebd0-127">Hvis du bruker versjon 10.0.17 eller senere, må du bruke malen med navnet Resultater av innsikt i kundebetaling (CDS til Fin and Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="3ebd0-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="3ebd0-128">Resultater av tidsserie for kontantstrøm (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3ebd0-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="3ebd0-129">Resultater av tidsserie for budsjett (CDS til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3ebd0-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="3ebd0-130">Angi den riktige planleggingen for hvert prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="3ebd0-131">Hvis du ikke ser de nødvendige enhetene i CDS, kan du gå til **Kreditt og innkreving > Oppsett > Finance Insights > Parametere for økonomisk innsikt**, aktivere funksjonen for kundebetalingsprognoser og klikke på knappen **Opprett prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="3ebd0-132">Når distribusjonen av modell for kunstig intelligens er fullført (vellykket eller mislykket), vil CDS-enhetene som kreves for å opprette integrering, bli distribuert i CDS.</span><span class="sxs-lookup"><span data-stu-id="3ebd0-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
