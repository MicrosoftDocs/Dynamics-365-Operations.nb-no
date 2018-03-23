---
title: Produktkategoristyring
description: "Dette emnet beskriver hvordan forhandleransvarlige kan bruke produktkategorier for detaljhandel til å styre relasjoner mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: nb-no
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="8ec1a-103">Utvidet kategori- og produktstyring</span><span class="sxs-lookup"><span data-stu-id="8ec1a-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="8ec1a-104">Dette emnet beskriver en utvidet måte å administrere produktkategorier for detaljhandel og produkter i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="8ec1a-105">Disse forbedringene lar forhandleransvarlige se en vanlig struktur av produktegenskaper mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="8ec1a-106">Hvis du vil vite mer om hvordan du behandler produktkategorier for detaljhandel, kan du gå til **Hierarki for detaljhandelprodukt** fra arbeidsområdet **Kategori- og produktstyring** og se på den utvidete strukturen for **Detaljhandelproduktkategori**-siden.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Arbeidsområdet kategori- og produktstyring](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="8ec1a-108">I tidligere utgaver ble produktegenskaper delt inn i **Grunnleggende produktegenskaper** og **Detaljhandelproduktegenskaper**, basert på omfanget av anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="8ec1a-109">**Produktegenskaper for detaljhandel** ble *globale* basert på deres relevans, noe som betyr at for en gitt **Produktegenskap for detaljhandel**, er den samme verdien lik på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="8ec1a-110">**Grunnleggende produktegenskaper** er *spesifikk for hver juridiske enhet*.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="8ec1a-111">Med andre ord kan en gitt **grunnleggende produktegenskap** være forskjellig på tvers av juridiske enheter, basert på individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="8ec1a-112">I den utvidede strukturen for detaljhandelproduktkategorien, er produktegenskapene atskilt basert på deres anvendelighet innen en gruppe, for å gjenspeile skjemastrukturen til detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Gruppering av felt basert på deres relevans](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="8ec1a-114">Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="8ec1a-115">Du gjør dette ved å velge enten **Se/rediger for alle juridiske enheter** eller **Se/rediger for en spesifikk juridisk enhet**.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Veksle mellom visning for en enkel eller alle juridiske enheter](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Veksle mellom visning for en enkel eller alle juridiske enheter](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="8ec1a-118">Sammenlignet med i tidligere versjoner, kan en varehandelsleder i den nye strukturen for detaljhandelproduktkategorien nå også definere standardverdier for et ekstra sett med egenskaper på nivået av en enkelt kategori.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="8ec1a-119">Ved produktoppretting arves disse standardverdiene for produktegenskaper av et produkt, basert på tilknytningen til en individuell kategori fra hierarkiet for detaljhandelprodukt.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="8ec1a-120">Disse arvede produktegenskaper kan endres for hvert produkt slik at de passer til individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="8ec1a-121">Velg egenskaper for å oppdatere produkter fra skjemaet for detaljert produktkategori</span><span class="sxs-lookup"><span data-stu-id="8ec1a-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="8ec1a-122">Du kan bruke denne nye utvidede strukturen for produktegenskaper til å velge hvilke produktegenskaper må overføres til tilknyttede produkter.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Ny utvidet visning av Oppdater produkter](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="8ec1a-124">Forhandleransvarlige kan endre disse arvede produktegenskaper for hvert produkt for å møte individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="8ec1a-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


