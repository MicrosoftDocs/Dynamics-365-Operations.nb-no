---
title: Legge til variantprodukter i bestillinger ved hjelp av variantvekt
description: Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0199f4b05c23eec5c03c770c37111a6ee6d13efe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208392"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="3c29d-103">Legge til variantprodukter i bestillinger ved hjelp av variantvekt</span><span class="sxs-lookup"><span data-stu-id="3c29d-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c29d-104">Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt.</span><span class="sxs-lookup"><span data-stu-id="3c29d-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="3c29d-105">Når du velger antallet for produktet du vil kjøpe, opprettes bestillingslinjer for alle variantene av produktet med foreslåtte antall basert på vekten som er konfigurert for produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="3c29d-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="3c29d-106">Denne prosedyren inkluderer ikke trinn for å konfigurere vektverdier for produktdimensjoner og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="3c29d-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="3c29d-107">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="3c29d-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3c29d-108">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="3c29d-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="3c29d-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="3c29d-109">Click New.</span></span>
3. <span data-ttu-id="3c29d-110">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3c29d-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3c29d-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c29d-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3c29d-112">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="3c29d-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="3c29d-113">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3c29d-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3c29d-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c29d-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3c29d-115">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3c29d-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3c29d-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3c29d-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="3c29d-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c29d-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="3c29d-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3c29d-118">Click OK.</span></span>
12. <span data-ttu-id="3c29d-119">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="3c29d-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="3c29d-120">Klikk kategorien Varianter.</span><span class="sxs-lookup"><span data-stu-id="3c29d-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="3c29d-121">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="3c29d-121">Click Add line.</span></span>
15. <span data-ttu-id="3c29d-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3c29d-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="3c29d-123">Skriv inn 0140 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="3c29d-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="3c29d-124">Sett verdien for Antall til 1000.</span><span class="sxs-lookup"><span data-stu-id="3c29d-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="3c29d-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="3c29d-125">Click Save.</span></span>

