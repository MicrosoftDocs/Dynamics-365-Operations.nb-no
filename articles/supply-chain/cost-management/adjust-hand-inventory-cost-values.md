---
title: Justere kostnadsverdier for lagerbeholdning
description: "Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 78a97e1ff893ecfb864052b79e56ad48efa5191c
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="af5d9-103">Justere kostnadsverdier for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="af5d9-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af5d9-104">Bruk siden Justering av lagerbeholdning til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt.</span><span class="sxs-lookup"><span data-stu-id="af5d9-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="af5d9-105">Du kan bruke siden **Justering av lagerbeholdning** til å justere kostnadsverdien til lagerbeholdningsantall etter at en lagerlukkingsprosess er kjørt.</span><span class="sxs-lookup"><span data-stu-id="af5d9-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="af5d9-106">**Obs!**  Du åpner siden **Justering av lagerbeholdning** ved å velge posten for en fullført lagerlukkingsprosess på siden **Lukking og justering** og deretter klikke **Justering** &gt; **Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="af5d9-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="af5d9-107">**Eksempel:** Du har følgende transaksjoner i februar:</span><span class="sxs-lookup"><span data-stu-id="af5d9-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="af5d9-108">1. februar: Et økonomisk lagermottak av et antall på 2 til en kostnad på USD 10,00</span><span class="sxs-lookup"><span data-stu-id="af5d9-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="af5d9-109">5. februar: Et økonomisk lagermottak av et antall på 1 til en kostnad på USD 13,00</span><span class="sxs-lookup"><span data-stu-id="af5d9-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="af5d9-110">19. februar: En økonomisk lageravgang av et antall på 1 til en løpende gjennomsnittlig kostnad på USD 11,00</span><span class="sxs-lookup"><span data-stu-id="af5d9-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="af5d9-111">Denne varen ble definert med først-inn-først-ut-lagermodellen, og lagerlukkingen ble utført per 28. februar.</span><span class="sxs-lookup"><span data-stu-id="af5d9-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="af5d9-112">Den økonomiske avgangstransaksjonen på USD 11,00 vil bli utlignet til det økonomiske mottaket datert 1. februar, og en justering på USD 1,00 blir foretatt.</span><span class="sxs-lookup"><span data-stu-id="af5d9-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="af5d9-113">Følgende lagermottak vil dermed inneholde åpne lagerantall:</span><span class="sxs-lookup"><span data-stu-id="af5d9-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="af5d9-114">1. februar: Et antall på 1 til en kostnad på USD 10,00</span><span class="sxs-lookup"><span data-stu-id="af5d9-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="af5d9-115">5. februar: Et antall på 1 til en kostnad på USD 13,00</span><span class="sxs-lookup"><span data-stu-id="af5d9-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="af5d9-116">Når du skal definere disse to varenes kost til USD 15,00, bruker du alternativet for lagerjustering til å justere åpne lagerantall per siste lagerlukkingsperiode.</span><span class="sxs-lookup"><span data-stu-id="af5d9-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="af5d9-117">**Obs!** Posteringsdatoen for lagerjusteringstransaksjonen blir datoen for den siste lagerlukkingen.</span><span class="sxs-lookup"><span data-stu-id="af5d9-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="af5d9-118">Denne datoen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="af5d9-118">This date can't be modified.</span></span>

