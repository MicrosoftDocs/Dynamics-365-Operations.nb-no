---
title: Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales
description: Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fa93b1262049d80148ff23b3d7223ec0f6c2fe68
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941172"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="bb643-103">Bruke prissettingsmotoren i Dynamics 365 Commerce med Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="bb643-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb643-104">Dette emnet beskriver hvordan du bruker prissettingsmotoren i Microsoft Dynamics 365 Commerce til å opprette salgstilbud i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="bb643-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="bb643-105">Prissettingsmotoren i Dynamics 365 Commerce støtter de fleste prisscenarioene for bedrift-til-kunde (B2C), for eksempel priser på butikknivå, tilknytningsbasert og lojalitetsbasert prissetting, samlerabatter, kvantumsrabatter og terskelrabatter.</span><span class="sxs-lookup"><span data-stu-id="bb643-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="bb643-106">Prissettingsmotoren bruker komplekse regler til å bestemme den beste prisen for et gitt tilbud eller ordre.</span><span class="sxs-lookup"><span data-stu-id="bb643-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="bb643-107">Når du bruker [dobbel skriving](./dual-write-overview.md), har du tre alternativer for prissettingsbehovene dine.</span><span class="sxs-lookup"><span data-stu-id="bb643-107">When you use [dual-write](./dual-write-overview.md), you have three options for your pricing needs.</span></span> <span data-ttu-id="bb643-108">Du kan bruke den statiske prissettingen som kommer fra prislisten i Dynamics 365 Sales, prissettingsmotoren i Dynamics 365 Supply Chain Management eller prissettingsmotoren i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb643-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bb643-109">Blant disse alternativene er prissettingsmotoren i Commerce best egnet i B2C-scenarioer.</span><span class="sxs-lookup"><span data-stu-id="bb643-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="bb643-110">Bruk prissettingsmotoren i Commerce i Sales</span><span class="sxs-lookup"><span data-stu-id="bb643-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="bb643-111">For øyeblikket kan prissettingsmotoren i Commerce bare brukes til opprettelse av tilbud i Sales.</span><span class="sxs-lookup"><span data-stu-id="bb643-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="bb643-112">Salgsordreintegrering med prissettingsmotoren i Commerce er ikke tilgjengelig ennå.</span><span class="sxs-lookup"><span data-stu-id="bb643-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="bb643-113">Når brukere starter et tilbud i Sales, kopierer rammeverket for dobbel skriving tilbudsdetaljene til Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb643-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="bb643-114">Endringer i eksisterende tilbudslinjer eller tilbudslinjer som nylig er lagt til i Sales, kopieres til Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb643-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="bb643-115">Når brukere vil bruke prissettingsmotoren i Commerce til å gi tilbudet en pris, kan de velge **Pristilbud** for å oppdatere prisene i tilbudet, basert på prissettingsmotoren i Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb643-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="bb643-116">Priser oppdateres deretter automatisk i både Sales og Commerce.</span><span class="sxs-lookup"><span data-stu-id="bb643-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb643-117">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="bb643-117">Prerequisites</span></span>

- <span data-ttu-id="bb643-118">Før du kan bruke prissettingsmotoren i Commerce i Sales, må du følge fremgangsmåten i [Kundeemne til kontanter i dobbel skriving](./dual-write-prospect-to-cash.md).</span><span class="sxs-lookup"><span data-stu-id="bb643-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](./dual-write-prospect-to-cash.md).</span></span>
- <span data-ttu-id="bb643-119">Du må deaktivere evaluering av forretningsavtale for manuell registrering ved å følge disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="bb643-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="bb643-120">Gå til **Kunder \> Oppsett \> Kundeparametere** i Commerce-miljøet ditt.</span><span class="sxs-lookup"><span data-stu-id="bb643-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="bb643-121">Fjern merket for **Manuell registrering** i hurtigfanen **Evaluering av handelsavtale** i **Priser**-fanen.</span><span class="sxs-lookup"><span data-stu-id="bb643-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb643-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bb643-122">Additional resources</span></span>

[<span data-ttu-id="bb643-123">Kundeemne til kontanter i dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="bb643-123">Prospect-to-cash in dual-write</span></span>](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]