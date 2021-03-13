---
title: Opprette aktiva basert på bestillinger
description: Dette emnet forklarer hvordan du kan opprette en liste over aktiva som kan brukes som grunnlag for oppretting av aktiva for vedlikeholdsjobber i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016990"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="63a02-103">Opprette aktiva basert på bestillinger</span><span class="sxs-lookup"><span data-stu-id="63a02-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="63a02-104">Dette emnet forklarer hvordan du kan opprette en liste over aktiva som kan brukes som grunnlag for oppretting av aktiva for vedlikeholdsjobber i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="63a02-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="63a02-105">Du kan vise en liste over bestillingslinjene som er opprettet på disse varene, basert på aktivavarene.</span><span class="sxs-lookup"><span data-stu-id="63a02-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="63a02-106">Formålet med denne funksjonaliteten er å enkelt opprette et aktivum i Aktivastyring basert på en bestilling.</span><span class="sxs-lookup"><span data-stu-id="63a02-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="63a02-107">Først definerer du varene som skal brukes til å opprette aktiva fra en bestilling, i **Aktivavarer**.</span><span class="sxs-lookup"><span data-stu-id="63a02-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="63a02-108">Når du har opprettet en bestillingslinje, oppretter du aktivaene i **Ventende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="63a02-109">Det er mulig å bestemme på hvilket stadium av bestillingen aktivumet skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="63a02-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="63a02-110">Velg aktivavarer</span><span class="sxs-lookup"><span data-stu-id="63a02-110">Select asset items</span></span>

1. <span data-ttu-id="63a02-111">Klikk på **Aktivastyring** > **Oppsett** > **Aktiva** > **Varer**.</span><span class="sxs-lookup"><span data-stu-id="63a02-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="63a02-112">Klikk på **Ny** for å opprette en ny aktivavare.</span><span class="sxs-lookup"><span data-stu-id="63a02-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="63a02-113">Velg varen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="63a02-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="63a02-114">Når du forlater dette feltet, settes vare navnetautomatisk inn i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="63a02-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="63a02-115">På hurtigfanen **Generelt** velger du en aktivatype for varen.</span><span class="sxs-lookup"><span data-stu-id="63a02-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="63a02-116">Velg aktivaprodusenten og -modellen for varen.</span><span class="sxs-lookup"><span data-stu-id="63a02-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="63a02-117">Lagre varen.</span><span class="sxs-lookup"><span data-stu-id="63a02-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="63a02-118">Opprette aktiva fra ventende aktiva</span><span class="sxs-lookup"><span data-stu-id="63a02-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="63a02-119">Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Ventende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="63a02-120">Du vil se en oppdatert liste over bestillingene basert på varene som er valgt, i **Aktivavarer**.</span><span class="sxs-lookup"><span data-stu-id="63a02-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="63a02-121">Du kan filtrere statusen for bestillinger for å velge i hvilken livssyklustilstand aktivumet skal opprettes.</span><span class="sxs-lookup"><span data-stu-id="63a02-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="63a02-122">Du vil for eksempel kanskje bare opprette aktiva når en produktkvittering er postert på en bestilling.</span><span class="sxs-lookup"><span data-stu-id="63a02-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="63a02-123">Velg koblingen **Referansenummer** på en bestillingslinje for å vise detaljert informasjon om varen.</span><span class="sxs-lookup"><span data-stu-id="63a02-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="63a02-124">Hvis du vil redigere hvilke dimensjoner som vises i hurtigfanen **Lagerdimensjoner**, klikker du på knappen **Visningsdimensjoner** og gjør dine valg.</span><span class="sxs-lookup"><span data-stu-id="63a02-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="63a02-125">Hvis du vil opprette et aktivum basert på en bestillingslinje, merker du av i **Merk**-kolonnen for denne linjen på listesiden, og klikker på **Opprett aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="63a02-126">Det vises en melding som informerer deg om ID-en for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="63a02-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="63a02-127">Velg aktivumet i **Alle aktiva**-listen, og klikk på **Rediger** for å legge til mer informasjon om aktivumet.</span><span class="sxs-lookup"><span data-stu-id="63a02-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="63a02-128">I **Ventende aktiva**, hvis du ikke vil slette en linje fordi du ikke ønsker å opprette et aktivum, merker du av i **Merk**-kolonnen for denne linjen og klikker på **Forkast ventende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="63a02-129">Det vises en melding som informerer deg om ID-en for aktivumet.</span><span class="sxs-lookup"><span data-stu-id="63a02-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="63a02-130">Du sletter ikke bestillingen eller salgsordren, bare posten som du kunne ha opprettet et aktivum for, i **Aktivastyring**.</span><span class="sxs-lookup"><span data-stu-id="63a02-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="63a02-131">Alle produktdimensjoner (størrelse, farge, konfigurasjon etc.) blir automatisk overført til aktivaattributtene.</span><span class="sxs-lookup"><span data-stu-id="63a02-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="63a02-132">Sporingsdimensjoner (serienummer) lagres direkte på aktivumet når det opprettes.</span><span class="sxs-lookup"><span data-stu-id="63a02-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="63a02-133">Finne ventende aktiva</span><span class="sxs-lookup"><span data-stu-id="63a02-133">Find pending assets</span></span>

<span data-ttu-id="63a02-134">Du kan kjøre en **telling av ventende aktiva** for å se etter ventende aktiva.</span><span class="sxs-lookup"><span data-stu-id="63a02-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="63a02-135">Denne funksjonen kan for eksempel brukes til å motta et varsel hver gang et ventende aktivum er klart til å opprettes som et aktivum.</span><span class="sxs-lookup"><span data-stu-id="63a02-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="63a02-136">Klikk på **Aktivastyring** > **Periodisk** > **Aktiva** > **Telling av ventende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="63a02-137">Klikk på **OK** for å kjøre jobben og oppdatere listen i **Ventende aktiva**.</span><span class="sxs-lookup"><span data-stu-id="63a02-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="63a02-138">Du kan angi at denne jobben skal kjøres som en satsvis jobb, for eksempel én gang per dag.</span><span class="sxs-lookup"><span data-stu-id="63a02-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="63a02-139">**Forsiktig:** Hvis data endres på en bestilling *etter* at du har opprettet et aktivum basert på den fra varen, gjenspeiles ikke disse endringene på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="63a02-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
