---
title: Handlekurvikonmodul
description: Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793087"
---
# <a name="cart-icon-module"></a><span data-ttu-id="17f30-103">Handlekurvikonmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17f30-104">Dette emnet dekker handlekurvikonmodulen og beskriver hvordan du legger den til på områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17f30-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="17f30-105">Handlekurvikonmodulen representerer diagrammet i hodemodulen på siden, og den viser antall varer i handlekurven.</span><span class="sxs-lookup"><span data-stu-id="17f30-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="17f30-106">Handlekurvikonmodulen viser også et handlekurvsammendrag (også kjent som en minikurv) når du holder markøren over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="17f30-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="17f30-107">Minikurven gir brukeren et sammendrag av varene i handlekurven uten å måtte gå til handlekurvsiden.</span><span class="sxs-lookup"><span data-stu-id="17f30-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="17f30-108">I tillegg kan brukerne også gå direkte til kassesiden hvis de er fornøyd med sammendraget.</span><span class="sxs-lookup"><span data-stu-id="17f30-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="17f30-109">Dette reduserer antall sidenavigasjoner, og betalingen blir raskere.</span><span class="sxs-lookup"><span data-stu-id="17f30-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="17f30-110">Støtte for handlekurvikon-modulen er tilgjengelig i Dynamics 365 Commerce 10.0.11-versjonen.</span><span class="sxs-lookup"><span data-stu-id="17f30-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="17f30-111">Bildet nedenfor viser et eksempel på en handlekurv-ikonmodul som viser en minihandlevogn i Fabrikam-overskriften.</span><span class="sxs-lookup"><span data-stu-id="17f30-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Eksempel på en handlevogn-ikonmodul](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="17f30-113">Modulegenskaper</span><span class="sxs-lookup"><span data-stu-id="17f30-113">Module properties</span></span>

- <span data-ttu-id="17f30-114">**Vis minikurv** – Hvis Sann aktiverer denne egenskapen at det vises et handlekurvsammendrag (minikurv) når pekeren holdes over handlekurvikonet.</span><span class="sxs-lookup"><span data-stu-id="17f30-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="17f30-115">Denne funksjonaliteten støttes bare for skrivebordsvisningsporter.</span><span class="sxs-lookup"><span data-stu-id="17f30-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="17f30-116">Legge til en handlekurvikonmodul på en side</span><span class="sxs-lookup"><span data-stu-id="17f30-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="17f30-117">Hvis du vil legge til en handlekurvikonmodul, kan du se [Hodemodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="17f30-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17f30-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="17f30-118">Additional resources</span></span>

[<span data-ttu-id="17f30-119">Handlekurvmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="17f30-120">Kassemodul</span><span class="sxs-lookup"><span data-stu-id="17f30-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="17f30-121">Betalingsmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="17f30-122">Leveringsadressemodul</span><span class="sxs-lookup"><span data-stu-id="17f30-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="17f30-123">Leveringsalternativmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="17f30-124">Henteinformasjonsmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="17f30-125">Ordredetaljermodul</span><span class="sxs-lookup"><span data-stu-id="17f30-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="17f30-126">Gavekortmodul</span><span class="sxs-lookup"><span data-stu-id="17f30-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]