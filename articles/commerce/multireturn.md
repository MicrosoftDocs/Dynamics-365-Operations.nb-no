---
title: Returnere varer på tvers av flere kunder, ordrer og fakturaer
description: Dette emnet beskriver funksjonen for aktivering av returer på tvers av flere ordrer fra kunder og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004464"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="76e7a-103">Returnere varer på tvers av flere kunder, ordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="76e7a-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="76e7a-104">Returer kan utføres på tvers av flere ordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="76e7a-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="76e7a-105">Konfigurere Commerce til å støtte returer på tvers av flere kundeordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="76e7a-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="76e7a-106">Gå til **Handelsparametere \> Kundeordrer**.</span><span class="sxs-lookup"><span data-stu-id="76e7a-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="76e7a-107">Aktiver parameteren **Aktiver returer for flere ordrer**.</span><span class="sxs-lookup"><span data-stu-id="76e7a-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="76e7a-108">Behandle returer</span><span class="sxs-lookup"><span data-stu-id="76e7a-108">Process returns</span></span>

<span data-ttu-id="76e7a-109">Når parameteren er aktivert og endringene synkronisert til butikkene, kan kassereren i butikken velge flere salgsordrer for en kunde for kundens retur.</span><span class="sxs-lookup"><span data-stu-id="76e7a-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="76e7a-110">Når ordrene er valgt, vises det en liste over alle returnerbare produkter på tvers av alle fakturaene for ordrene.</span><span class="sxs-lookup"><span data-stu-id="76e7a-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="76e7a-111">Kassereren kan deretter velge produktene som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="76e7a-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="76e7a-112">Én returordre opprettes for alle de valgte produktene.</span><span class="sxs-lookup"><span data-stu-id="76e7a-112">A single return order will be created for all the selected products.</span></span>
