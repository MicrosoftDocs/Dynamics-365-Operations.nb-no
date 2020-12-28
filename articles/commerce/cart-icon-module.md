---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/07/2020
ms.locfileid: "4414803"
---
# <a name="cart-icon-module"></a><span data-ttu-id="35193-103">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="35193-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="35193-104">Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35193-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35193-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="35193-105">Overview</span></span>

<span data-ttu-id="35193-106">Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="35193-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="35193-107">Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="35193-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="35193-108">Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden.</span><span class="sxs-lookup"><span data-stu-id="35193-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="35193-109">I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget.</span><span class="sxs-lookup"><span data-stu-id="35193-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="35193-110">Dette reduserer antall sidenavigasjoner, og betalingen blir raskere.</span><span class="sxs-lookup"><span data-stu-id="35193-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="35193-111">Støtte for handlekurvikon-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.</span><span class="sxs-lookup"><span data-stu-id="35193-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="35193-112">Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.</span><span class="sxs-lookup"><span data-stu-id="35193-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på en handlevogn-ikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="35193-114">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="35193-114">Module properties</span></span>

- <span data-ttu-id="35193-115">**Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="35193-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="35193-116">Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.</span><span class="sxs-lookup"><span data-stu-id="35193-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="35193-117">Legge til en handlekurvikonmodul på en side</span><span class="sxs-lookup"><span data-stu-id="35193-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="35193-118">Hvis du vil legge til en handlekurvikonmodul, kan du se [Hodemodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="35193-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35193-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="35193-119">Additional resources</span></span>

[<span data-ttu-id="35193-120">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="35193-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="35193-121">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="35193-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="35193-122">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="35193-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="35193-123">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="35193-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="35193-124">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="35193-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="35193-125">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="35193-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="35193-126">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="35193-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="35193-127">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="35193-127">Gift card module</span></span>](add-giftcard.md)
