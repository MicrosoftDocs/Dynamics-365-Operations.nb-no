---
title: Endre en behovsprognose manuelt
description: Dette emnet viser hvordan du endrer prognosen for en vare.
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889030"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="066dd-103">Endre en behovsprognose manuelt</span><span class="sxs-lookup"><span data-stu-id="066dd-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="066dd-104">Denne fremgangsmåten viser hvordan du endrer prognosen for en vare.</span><span class="sxs-lookup"><span data-stu-id="066dd-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="066dd-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="066dd-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="066dd-106">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="066dd-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="066dd-107">Endre prognosen for en utvalgt vare</span><span class="sxs-lookup"><span data-stu-id="066dd-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="066dd-108">Slik endrer du prognosen for en utvalgt vare:</span><span class="sxs-lookup"><span data-stu-id="066dd-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="066dd-109">Gå til **Moduler \> Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</span><span class="sxs-lookup"><span data-stu-id="066dd-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="066dd-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="066dd-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="066dd-111">Velg varen du vil endre prognosen for.</span><span class="sxs-lookup"><span data-stu-id="066dd-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="066dd-112">Åpne Kategorien **Plan** i handlingsruten, og velg **Behovsprognose**.</span><span class="sxs-lookup"><span data-stu-id="066dd-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="066dd-113">Velg en rad i listen.</span><span class="sxs-lookup"><span data-stu-id="066dd-113">In the list, select a row.</span></span> <span data-ttu-id="066dd-114">Hvis det ikke finnes noen prognoselinjer, kan du opprette en ny linje ved å velge **Ny** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="066dd-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="066dd-115">Angi et positivt tall i **Salgsantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="066dd-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="066dd-116">Dette tallet representerer det prognoseberegnede antallet for varen.</span><span class="sxs-lookup"><span data-stu-id="066dd-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="066dd-117">Det vises en feil hvis du angir et negativt tall.</span><span class="sxs-lookup"><span data-stu-id="066dd-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="066dd-118">Fyll ut de andre feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="066dd-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="066dd-119">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="066dd-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="066dd-120">Endre prognosen for én eller flere varer i Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="066dd-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="066dd-121">Slik endrer du prognosen for én eller flere varer i Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="066dd-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="066dd-122">Gjør ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="066dd-122">Do one of the following:</span></span>
    - <span data-ttu-id="066dd-123">Åpne **Behovsprognose**-siden for en hvilken som helst vare (det spiller ingen rolle hvilken), som beskrevet i forrige del.</span><span class="sxs-lookup"><span data-stu-id="066dd-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="066dd-124">Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Behovsprognoselinjer**.</span><span class="sxs-lookup"><span data-stu-id="066dd-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="066dd-125">I handlingsruten velger du **Åpne i Microsoft Office \> Behovsprognoseoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="066dd-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="066dd-126">Velg en nedlastingsplassering, lagre og åpne deretter den nedlastede filen i Excel.</span><span class="sxs-lookup"><span data-stu-id="066dd-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="066dd-127">Hvis du får en advarsel, velger du **Aktiver redigering**.</span><span class="sxs-lookup"><span data-stu-id="066dd-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="066dd-128">I Excel logger du deg på Supply Chain Management ved å bruke oppgaveruten i Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="066dd-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="066dd-129">Du må logge på med alternativet **La meg være pålogget** aktivert, og du må klarere datatilkoblingsappen.</span><span class="sxs-lookup"><span data-stu-id="066dd-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="066dd-130">Excel-regnearket viser nå alle gjeldende behovsprognoselinjer for firmaet.</span><span class="sxs-lookup"><span data-stu-id="066dd-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="066dd-131">Du kan legge til, slette og redigere behovsprognoselinjer etter behov.</span><span class="sxs-lookup"><span data-stu-id="066dd-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="066dd-132">Velg **Publiser** i Microsoft Dynamics-oppgaverute for å laste opp endringene tilbake til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="066dd-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
