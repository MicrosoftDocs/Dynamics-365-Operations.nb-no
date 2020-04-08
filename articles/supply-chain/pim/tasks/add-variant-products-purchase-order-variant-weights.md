---
title: Legge til variantprodukter i bestillinger ved hjelp av variantvekt
description: Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae45dc0ed5332242a12efbb7f8ca37f97a244cce
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147992"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="8204b-103">Legge til variantprodukter i bestillinger ved hjelp av variantvekt</span><span class="sxs-lookup"><span data-stu-id="8204b-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8204b-104">Denne prosedyren hjelper deg gjennom trinnene med å bruke variantvekter for å fylle ut bestillingslinjer automatisk for hver variant av et produkt.</span><span class="sxs-lookup"><span data-stu-id="8204b-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="8204b-105">Når du velger antallet for produktet du vil kjøpe, opprettes bestillingslinjer for alle variantene av produktet med foreslåtte antall basert på vekten som er konfigurert for produktvariantene.</span><span class="sxs-lookup"><span data-stu-id="8204b-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="8204b-106">Denne prosedyren inkluderer ikke trinn for å konfigurere vektverdier for produktdimensjoner og produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="8204b-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="8204b-107">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="8204b-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8204b-108">Gå til Leverandører > Bestillinger > Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="8204b-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8204b-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8204b-109">Click New.</span></span>
3. <span data-ttu-id="8204b-110">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8204b-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8204b-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8204b-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8204b-112">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="8204b-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="8204b-113">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8204b-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8204b-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8204b-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8204b-115">Klikk rullegardinknappen i Lager-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="8204b-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8204b-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8204b-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8204b-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8204b-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8204b-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8204b-118">Click OK.</span></span>
12. <span data-ttu-id="8204b-119">Aktiver/deaktiver utvidelsen av delen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="8204b-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="8204b-120">Klikk kategorien Varianter.</span><span class="sxs-lookup"><span data-stu-id="8204b-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="8204b-121">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="8204b-121">Click Add line.</span></span>
15. <span data-ttu-id="8204b-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8204b-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="8204b-123">Skriv inn 0140 i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="8204b-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="8204b-124">Sett verdien for Antall til 1000.</span><span class="sxs-lookup"><span data-stu-id="8204b-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="8204b-125">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="8204b-125">Click Save.</span></span>

