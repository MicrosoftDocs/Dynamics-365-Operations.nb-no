---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661153"
---
# <a name="cart-icon-module"></a><span data-ttu-id="c8e29-103">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8e29-104">Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c8e29-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8e29-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="c8e29-105">Overview</span></span>

<span data-ttu-id="c8e29-106">Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="c8e29-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="c8e29-107">Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="c8e29-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="c8e29-108">Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden.</span><span class="sxs-lookup"><span data-stu-id="c8e29-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="c8e29-109">I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget.</span><span class="sxs-lookup"><span data-stu-id="c8e29-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="c8e29-110">Dette reduserer antall sidenavigasjoner, og betalingen blir raskere.</span><span class="sxs-lookup"><span data-stu-id="c8e29-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="c8e29-111">Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.</span><span class="sxs-lookup"><span data-stu-id="c8e29-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på en handlevogn-ikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="c8e29-113">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="c8e29-113">Module properties</span></span>

- <span data-ttu-id="c8e29-114">**Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="c8e29-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="c8e29-115">Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.</span><span class="sxs-lookup"><span data-stu-id="c8e29-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="c8e29-116">Legge til en handlekurvikonmodul på en side</span><span class="sxs-lookup"><span data-stu-id="c8e29-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="c8e29-117">Hvis du vil legge til en handlekurvikonmodul, kan du se [Hodemodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c8e29-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8e29-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c8e29-118">Additional resources</span></span>

[<span data-ttu-id="c8e29-119">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c8e29-120">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c8e29-121">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c8e29-122">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c8e29-123">Modul for leveringsalternativer</span><span class="sxs-lookup"><span data-stu-id="c8e29-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c8e29-124">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c8e29-125">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="c8e29-125">Gift card module</span></span>](add-giftcard.md)
