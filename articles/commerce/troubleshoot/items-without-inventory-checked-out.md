---
title: Varer uten lager kan sjekkes ut
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6df9c77248c7f4e16765b98327fe5838f0fce7e4
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585463"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="4a80b-103">Varer uten lager kan sjekkes ut</span><span class="sxs-lookup"><span data-stu-id="4a80b-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a80b-104">Dette emnet gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.</span><span class="sxs-lookup"><span data-stu-id="4a80b-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="4a80b-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4a80b-105">Description</span></span>

<span data-ttu-id="4a80b-106">Brukerne kan legge til en vare i handlekurven, selv om det ikke finnes lagerbeholdning i butikken, og deretter gå videre til betalingssiden.</span><span class="sxs-lookup"><span data-stu-id="4a80b-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="4a80b-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="4a80b-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="4a80b-108">Aktivere egenskapen Vis ut av lagerfeil i Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="4a80b-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="4a80b-109">Hvis du vil aktivere egenskapen **Vis feil for utsolgte varer** i Commerce-områdebyggeren, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="4a80b-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4a80b-110">Velg området du arbeider på.</span><span class="sxs-lookup"><span data-stu-id="4a80b-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="4a80b-111">Velg **Sider** i navigasjonsruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="4a80b-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="4a80b-112">Velg **CartPage** for å åpne den.</span><span class="sxs-lookup"><span data-stu-id="4a80b-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="4a80b-113">Velg sporet **Handlekurv 1**, velg **Rediger**, og merk deretter av for **Vis feil for utsolgte varer** i ruten for egenskaper.</span><span class="sxs-lookup"><span data-stu-id="4a80b-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="4a80b-114">Lagre og publiser siden.</span><span class="sxs-lookup"><span data-stu-id="4a80b-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a80b-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4a80b-115">Additional resources</span></span>

[<span data-ttu-id="4a80b-116">Bruke lagerinnstillinger</span><span class="sxs-lookup"><span data-stu-id="4a80b-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="4a80b-117">Beregne lagertilgjengelighet for detaljhandelskanaler</span><span class="sxs-lookup"><span data-stu-id="4a80b-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="4a80b-118">Konfigurere lagerbuffere og lagernivåer</span><span class="sxs-lookup"><span data-stu-id="4a80b-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
