---
title: Produktkategoriledelse og opprettelse
description: Dette emnet beskriver forbedringene som er gjort i ledelseserfaringen for produktkategorier for detaljhandel. Disse forbedringene lar forhandleransvarlige ha en sammenheng mellom detaljprodukthierarkiet og utgitte produktdetaljer.
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: e269f6c3815cea55b69b7eb6a9a65bf7c9e15378
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="1cc32-104">Produktkategoriledelse og opprettelse</span><span class="sxs-lookup"><span data-stu-id="1cc32-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="1cc32-105">Forbedringer som er gjort i ledelseserfaring for produktkategorier for detaljhandel, gjør det mulig for forhandleransvarlige å ha en sammenheng mellom produkthierarkiet for detaljhandel og utgitte produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="1cc32-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="1cc32-106">For å se disse forbedringene i arbeidsområdet **Kategori og produkadminsitrasjon**, velg **Produkthierarki for detalhandel** for å åpne siden **Ny struktur for produktkategori for detaljhandel**.</span><span class="sxs-lookup"><span data-stu-id="1cc32-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="1cc32-107">I tidligere utgaver ble produktegenskaper delt inn i Grunnleggende produktegenskaper og Detaljhandelproduktegenskaper, basert på omfanget av anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="1cc32-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="1cc32-108">Detaljhandelprodukters egenskaper var *globale*.</span><span class="sxs-lookup"><span data-stu-id="1cc32-108">Retail product properties were *global*.</span></span> <span data-ttu-id="1cc32-109">Med andre ord, for en gitt produktegenskap, deles samme verdi over alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="1cc32-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="1cc32-110">Basisproduktegenskaper var *juridisk enhetsspesifikke*.</span><span class="sxs-lookup"><span data-stu-id="1cc32-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="1cc32-111">Med andre ord kan en gitt produktegenskap være forskjellig på tvers av juridiske enheter, basert på individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="1cc32-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="1cc32-112">Med disse forbedringene, for produktegenskaper i produktkategorien Detaljhandel, fortsetter vi å skille feltene, basert på deres anvendelighet innen en gruppe, for å gjenspeile den formelle strukturen for produktdetaljer.</span><span class="sxs-lookup"><span data-stu-id="1cc32-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="1cc32-113">Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="1cc32-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="1cc32-114">Bare vel **Se/rediger for alle juridiske enheter** eller **Se/rediger for en spesifikk juridisk enhet** etter behov.</span><span class="sxs-lookup"><span data-stu-id="1cc32-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="1cc32-115">Forhandleransvarlige kan også definere standardverdier for et ekstra sett med produktegenskaper på nivået av en enkelt kategori.</span><span class="sxs-lookup"><span data-stu-id="1cc32-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="1cc32-116">Disse egenskapsverdiene er arvet av et produkt, basert på deres tilknytning til en kategori på tidspunktet for produktopprettelsen.</span><span class="sxs-lookup"><span data-stu-id="1cc32-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="1cc32-117">Velg egenskaper for å oppdatere produkter fra skjemaet for detaljert produktkategori</span><span class="sxs-lookup"><span data-stu-id="1cc32-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="1cc32-118">Du kan bruke logiske grupperingsegenskaper til å velge hvilke oppdaterte produktegenskaper som skal dyttes til tilhørende produkter.</span><span class="sxs-lookup"><span data-stu-id="1cc32-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="1cc32-119">Forhandleransvarlige kan endre disse arvede produktegenskaper for hvert produkt for å møte individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="1cc32-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

