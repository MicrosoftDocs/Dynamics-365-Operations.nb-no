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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2246024d7d70947690173f3d0768292abe43efd7
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="3115b-103">Administrere produktkategorier for detaljhandel og produkter</span><span class="sxs-lookup"><span data-stu-id="3115b-103">Manage Retail product categories and products</span></span>

[!INCLUDE [banner](./includes/banner.md)]

<span data-ttu-id="3115b-104">Dette emnet beskriver en utvidet måte å administrere produktkategorier for detaljhandel og produkter i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3115b-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3115b-105">Forbedringene lar forhandleransvarlige se en struktur av produktegenskaper som deles mellom hierarkiet for detaljhandelprodukt og detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="3115b-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="3115b-106">Hvis du vil lære mer om hvordan du administrerer produktkategorier for detaljhandel, velger du flisen **Hierarki for detaljhandelprodukt** i **Kategori- og produktstyring**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="3115b-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="3115b-107">Legg merke til den utvidede strukturen for **Hierarki for detaljhandelprodukt**-siden som vises.</span><span class="sxs-lookup"><span data-stu-id="3115b-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="3115b-108">I tidligere utgaver av detaljhandel, ble produktegenskaper delt inn i *grunnleggende produktegenskaper* og *Detaljhandelproduktegenskaper*, basert på omfanget av anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="3115b-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="3115b-109">Egenskaper for detaljhandelprodukt er *globale* basert på deres relevans.</span><span class="sxs-lookup"><span data-stu-id="3115b-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="3115b-110">Med andre ord, for en gitt egenskap for detaljhandelsprodukt, deles samme verdi over alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="3115b-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="3115b-111">Grunnleggende produktegenskaper derimot er *spesifikk for hver juridiske enhet*.</span><span class="sxs-lookup"><span data-stu-id="3115b-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="3115b-112">Med andre ord kan en gitt grunnleggende produktegenskap være forskjellig på tvers av juridiske enheter, avhengig av individuelle forretningsbehov til hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="3115b-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="3115b-113">I den utvidede strukturen for detaljhandelproduktkategorien, er produktegenskapene atskilt basert på deres anvendelighet i en gruppe, for å gjenspeile skjemastrukturen til detaljer om frigitt produkt.</span><span class="sxs-lookup"><span data-stu-id="3115b-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Felt gruppert basert på egenskapenes relevans](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="3115b-115">Du kan bytte mellom å administrere juridiske enhetsspesifikke egenskaper i alle juridiske enheter og administrere dem for en bestemt juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="3115b-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="3115b-116">Hvis du vil behandle egenskaper på tvers av alle juridiske enheter, velger du **Vis for alle juridiske enheter** (eller **Rediger for alle juridiske enheter**).</span><span class="sxs-lookup"><span data-stu-id="3115b-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Vise/redigere for alle juridiske enheter](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="3115b-118">Hvis du vil behandle egenskapene for en bestemt juridisk enhet, velger du **Vis for en bestemt juridisk enhet** (eller **Rediger for en bestemt juridisk enhet**).</span><span class="sxs-lookup"><span data-stu-id="3115b-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Vise/redigere for en bestemt juridisk enhet](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="3115b-120">I den forbedrede strukturen for detaljhandelproduktkategorien kan en varehandelsleder nå også definere standardverdier for et ekstra sett med produktegenskaper på nivået av den individuelle kategorien.</span><span class="sxs-lookup"><span data-stu-id="3115b-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="3115b-121">Når produktene da opprettes, arver de standardverdiene for produktegenskapene, basert på tilknytningen til disse egenskapene med en individuell kategori i hierarkiet for detaljhandelprodukt.</span><span class="sxs-lookup"><span data-stu-id="3115b-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="3115b-122">Disse arvede produktegenskaper kan endres for hvert produkt slik at de passer til individuelle forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="3115b-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="3115b-123">Velge egenskaper for å oppdatere produkter på siden for hierarki for detaljhandelprodukt</span><span class="sxs-lookup"><span data-stu-id="3115b-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="3115b-124">Du kan bruke den nye utvidede strukturen for produktegenskaper til å velge oppdaterte produktegenskaper som må overføres til tilknyttede produkter.</span><span class="sxs-lookup"><span data-stu-id="3115b-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="3115b-125">På **Hierarki for detaljhandelprodukt**-siden i handlingsruten, velger du **Kategori** og deretter **Oppdater produkter** for å åpne **Oppdater produkter**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="3115b-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Dialogboksen Oppdater produkter](media/NewUpdateProductsEnhancedView.PNG)


