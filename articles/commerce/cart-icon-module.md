---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261582"
---
# <a name="cart-icon-module"></a><span data-ttu-id="320c6-103">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="320c6-104">Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="320c6-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="320c6-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="320c6-105">Overview</span></span>

<span data-ttu-id="320c6-106">Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="320c6-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="320c6-107">Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="320c6-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="320c6-108">Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden.</span><span class="sxs-lookup"><span data-stu-id="320c6-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="320c6-109">I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget.</span><span class="sxs-lookup"><span data-stu-id="320c6-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="320c6-110">Dette reduserer antall sidenavigasjoner, og betalingen blir raskere.</span><span class="sxs-lookup"><span data-stu-id="320c6-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="320c6-111">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="320c6-111">Module properties</span></span>

- <span data-ttu-id="320c6-112">**Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="320c6-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="320c6-113">Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.</span><span class="sxs-lookup"><span data-stu-id="320c6-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="320c6-114">Legge til en handlekurvikonmodul på en side</span><span class="sxs-lookup"><span data-stu-id="320c6-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="320c6-115">Hvis du vil legge til en handlekurvikonmodul, kan du se [Hodemodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="320c6-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="320c6-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="320c6-116">Additional resources</span></span>

[<span data-ttu-id="320c6-117">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="320c6-118">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="320c6-119">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="320c6-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="320c6-120">Ordrebekreftelsesmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="320c6-121">Topptekstmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="320c6-122">Bunntekstmodul</span><span class="sxs-lookup"><span data-stu-id="320c6-122">Footer module</span></span>](author-footer-module.md)
