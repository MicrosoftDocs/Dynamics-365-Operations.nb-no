---
title: Opprette en bestilling for en engangsleverandør
description: Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434804"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="54b76-103">Opprette en bestilling for en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="54b76-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54b76-104">Denne fremgangsmåten viser hvordan du oppretter en bestilling manuelt for en engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="54b76-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="54b76-105">Leverandøren opprettes automatisk med bestillingen, i stedet for å opprette leverandørkontoen manuelt.</span><span class="sxs-lookup"><span data-stu-id="54b76-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="54b76-106">Bestillinger opprettes vanligvis av en innkjøpsagent.</span><span class="sxs-lookup"><span data-stu-id="54b76-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="54b76-107">Eksemplet som vises i denne veiledningen, kan brukes i demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="54b76-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="54b76-108">Det er en forutsetning at kontoen for engangsleverandør er definert på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="54b76-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="54b76-109">Opprette en bestilling for en engangsleverandør</span><span class="sxs-lookup"><span data-stu-id="54b76-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="54b76-110">Gå til Innkjøp og leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="54b76-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="54b76-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="54b76-111">Click New.</span></span>
3. <span data-ttu-id="54b76-112">Velg Ja i feltet Engangsleverandør.</span><span class="sxs-lookup"><span data-stu-id="54b76-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="54b76-113">En leverandørkonto blir automatisk opprettet og tilordnet bestillingen.</span><span class="sxs-lookup"><span data-stu-id="54b76-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="54b76-114">Leverandørkontoen blir opprettet basert på malen som er angitt i kategorien Generelt på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="54b76-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="54b76-115">I Navn-feltet skriver du inn et unikt navn for leverandøren.</span><span class="sxs-lookup"><span data-stu-id="54b76-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="54b76-116">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="54b76-116">Click OK.</span></span>
    * <span data-ttu-id="54b76-117">Bestillingen kan nå fullføres og behandles som hvilken som helst ordre.</span><span class="sxs-lookup"><span data-stu-id="54b76-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="54b76-118">Det finnes ingen spesielle egenskaper som er relatert til hvordan dette gjøres.</span><span class="sxs-lookup"><span data-stu-id="54b76-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="54b76-119">Fakturaen registrerer en forfallstransaksjon på leverandørkontoen som ble opprettet med ordren, og deretter behandles betalingen.</span><span class="sxs-lookup"><span data-stu-id="54b76-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

