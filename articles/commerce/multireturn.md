---
title: Returnere varer på tvers av flere kunder, ordrer og fakturaer
description: Dette emnet beskriver funksjonen for aktivering av returer på tvers av flere ordrer fra kunder og fakturaer i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976669"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="ba914-103">Returnere varer på tvers av flere kunder, ordrer og fakturaer</span><span class="sxs-lookup"><span data-stu-id="ba914-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ba914-104">Denne artikkelen beskriver to funksjoner som optimaliserer kundeordrereturer via flere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="ba914-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="ba914-105">Aktiver refunderinger på tvers av flere registreringer</span><span class="sxs-lookup"><span data-stu-id="ba914-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="ba914-106">Denne funksjonen aktiverer flere sammenkoblede refusjoner mot samme kundeordre.</span><span class="sxs-lookup"><span data-stu-id="ba914-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="ba914-107">Gå til arbeidsområdet **Funksjonsbehandling** og søk etter **Aktiver refusjoner over flere registreringer**.</span><span class="sxs-lookup"><span data-stu-id="ba914-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="ba914-108">Velg **Aktiver refusjoner over flere ordrer**, og klikk deretter **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="ba914-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="ba914-109">Aktiver riktig avgiftsberegning for returer med delvis antall</span><span class="sxs-lookup"><span data-stu-id="ba914-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="ba914-110">Denne funksjonen sikrer at når en ordre returneres ved hjelp av flere fakturaer, vil avgiften være lik avgiftsbeløpet som opprinnelig ble belastet.</span><span class="sxs-lookup"><span data-stu-id="ba914-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="ba914-111">Gå til arbeidsområdet **Funksjonsbehandling** og søk etter **Aktiver riktig avgiftsberegning for returer med delvis antall**.</span><span class="sxs-lookup"><span data-stu-id="ba914-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="ba914-112">Velg **Aktiver riktig avgiftsberegning for returer med delvis antall**, og klikk deretter **Aktiver**.</span><span class="sxs-lookup"><span data-stu-id="ba914-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="ba914-113">Behandle returer</span><span class="sxs-lookup"><span data-stu-id="ba914-113">Process returns</span></span>

<span data-ttu-id="ba914-114">Når disse funksjonene er aktivert og endringene synkronisert til butikkene, kan kassereren i butikken velge flere salgsordrer for en kunde for kundens retur.</span><span class="sxs-lookup"><span data-stu-id="ba914-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="ba914-115">Når ordrene er valgt, vises det en liste over alle returnerbare produkter på tvers av alle fakturaene for ordrene.</span><span class="sxs-lookup"><span data-stu-id="ba914-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="ba914-116">Kassereren kan deretter velge produktene som skal returneres.</span><span class="sxs-lookup"><span data-stu-id="ba914-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="ba914-117">Én returordre opprettes for alle de valgte produktene.</span><span class="sxs-lookup"><span data-stu-id="ba914-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="ba914-118">Hvis ordren er fullstendig returnert, vil beløpet som returneres til kunden, være lik avgiftsbeløpet som opprinnelig ble belastet.</span><span class="sxs-lookup"><span data-stu-id="ba914-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

