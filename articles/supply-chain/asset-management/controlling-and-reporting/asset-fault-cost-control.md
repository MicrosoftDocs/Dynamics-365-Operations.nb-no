---
title: Kostnadskontroll for aktivumfeil
description: Dette emnet beskriver kostnadskontroll for aktivumfeil i Aktivastyring.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b101c3b386c3edd8aec4c44e8ee834519718ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811188"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="cf52a-103">Kostnadskontroll for aktivumfeil</span><span class="sxs-lookup"><span data-stu-id="cf52a-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cf52a-104">I Aktivastyring kan du beregne kostnader ved registreringer av aktivafeil for å få en oversikt over faktiske kostnader sammenlignet med budsjettkostnader.</span><span class="sxs-lookup"><span data-stu-id="cf52a-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="cf52a-105">Faktiske kostnader er basert på posterte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="cf52a-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="cf52a-106">Datoen er feildatoen da symptomet ble registrert.</span><span class="sxs-lookup"><span data-stu-id="cf52a-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="cf52a-107">Klikk på **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Kostnadskontroll for aktivumfeil**.</span><span class="sxs-lookup"><span data-stu-id="cf52a-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="cf52a-108">I dialogboksen **Kostnadskontroll for aktivumfeil** velger du et finansdimensjonssett som skal tas med i beregningen, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="cf52a-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="cf52a-109">Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med en nullverdi.</span><span class="sxs-lookup"><span data-stu-id="cf52a-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="cf52a-110">Du kan bruke **Nivå**-feltet til å angi hvor detaljert kostnadskontrollinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="cf52a-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="cf52a-111">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle kostnadskontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="cf52a-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="cf52a-112">Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kostnadskontrollinjer for aktivafeil på alle arbeidsstedsnivåer de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="cf52a-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="cf52a-113">Hvis du vil begrense søket, kan du velge bestemte anleggsmidler, feildatoer og feilårsaker i hurtigfanen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="cf52a-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="cf52a-114">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="cf52a-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="cf52a-115">Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="cf52a-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="cf52a-116">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="cf52a-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="cf52a-117">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="cf52a-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="cf52a-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cf52a-118">Example</span></span>

<span data-ttu-id="cf52a-119">Dette eksemplet viser beregning av kostnadskontroll for aktivumfeil.</span><span class="sxs-lookup"><span data-stu-id="cf52a-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="cf52a-120">Feltet **Opprinnelig budsjett** viser budsjettkostnader fra arbeidsordreprognosen.</span><span class="sxs-lookup"><span data-stu-id="cf52a-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="cf52a-121">Feltet **Faktiske kostnader** viser posterte kostnader på arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="cf52a-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="cf52a-122">Feltet **Igangsatt kost** viser totale kostnader som firmaet har forpliktet seg til i forhold til arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="cf52a-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![Figur 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="cf52a-124">Se emnet [Feilstyring](../setup-for-work-orders/fault-management.md) hvis du vil ha informasjon om hvordan du definerer feil.</span><span class="sxs-lookup"><span data-stu-id="cf52a-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]