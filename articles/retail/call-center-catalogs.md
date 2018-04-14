---
title: Telefonsenterkataloger
description: Denne artikkelen beskriver telefonsenterspesifikke funksjoner for kataloger i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9df8682769254f44cc23675fe2237080b447925
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="call-center-catalogs"></a><span data-ttu-id="e28d9-103">Telefonsenterkataloger</span><span class="sxs-lookup"><span data-stu-id="e28d9-103">Call center catalogs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="e28d9-104">Denne artikkelen beskriver telefonsenterspesifikke funksjoner for kataloger i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e28d9-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="e28d9-105">I et telefonsenter kan du bruke produktkataloger til å identifisere produktene du vil tilby kundene.</span><span class="sxs-lookup"><span data-stu-id="e28d9-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="e28d9-106">Telefonsentre bruker vanligvis trykte kataloger.</span><span class="sxs-lookup"><span data-stu-id="e28d9-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="e28d9-107">Utforming og produksjonen av en trykt katalog håndteres utenfor Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="e28d9-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="e28d9-108">Du kan imidlertid opprette og lagre en digital versjon av en katalog ved hjelp av de samme sidene du bruker til å definere detaljhandelskataloger for nettbutikker.</span><span class="sxs-lookup"><span data-stu-id="e28d9-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="e28d9-109">Før du kan opprette en katalog, må du definere produktsortimenter og tilordne sortimentene til et telefonsenter.</span><span class="sxs-lookup"><span data-stu-id="e28d9-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="e28d9-110">Deretter legger du til produkter i katalogen ved å velge produkter fra disse assortementene.</span><span class="sxs-lookup"><span data-stu-id="e28d9-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="e28d9-111">Når produkter er lagt til i katalogen, og katalogen er fullstendig, må du validere katalogen for å kontrollere dataene.</span><span class="sxs-lookup"><span data-stu-id="e28d9-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="e28d9-112">Deretter må du sende katalogen til vurdering og godkjenning.</span><span class="sxs-lookup"><span data-stu-id="e28d9-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="e28d9-113">Når katalogen er godkjent, kan den publiseres.</span><span class="sxs-lookup"><span data-stu-id="e28d9-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="e28d9-114">Når det opprettes en telefonsenterkatalog, kan du ta et øyeblikksbilde av katalogdataene når katalogen publiseres.</span><span class="sxs-lookup"><span data-stu-id="e28d9-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="e28d9-115">Denne funksjonen for øyeblikksbilde gir deg tilgang til en bestemt versjon av katalogen selv om katalogen er endret og oppdatert senere.</span><span class="sxs-lookup"><span data-stu-id="e28d9-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="e28d9-116">Telefonsenterkataloger kan også defineres slik at de omfatter følgende valgfrie funksjoner:</span><span class="sxs-lookup"><span data-stu-id="e28d9-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="e28d9-117">**Kildekoder** – Kildekoder som brukes til å spore kunderesponsen på spesifikke katalogutsendelser.</span><span class="sxs-lookup"><span data-stu-id="e28d9-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="e28d9-118">**Gratisprodukter** – Produkter som kan inkluderes i en kundes ordre uten ekstra kostnad.</span><span class="sxs-lookup"><span data-stu-id="e28d9-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="e28d9-119">Disse produktene legges automatisk til en ordre når kildekoden for katalogen angis i ordren.</span><span class="sxs-lookup"><span data-stu-id="e28d9-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="e28d9-120">**Skript** – Skript er tekster som en telefonsenterarbeider leser for en kunde når det opprettes en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="e28d9-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="e28d9-121">Skript kan inkludere hilsener eller kjøpsforslag.</span><span class="sxs-lookup"><span data-stu-id="e28d9-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="e28d9-122">**Sideoppsett** – Et sideoppsett viser sideposisjonen for produkter i den trykte katalogen.</span><span class="sxs-lookup"><span data-stu-id="e28d9-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="e28d9-123">Denne informasjonen brukes til analyserapporten for katalogområdet.</span><span class="sxs-lookup"><span data-stu-id="e28d9-123">This information is used for the catalog area analysis report.</span></span>





