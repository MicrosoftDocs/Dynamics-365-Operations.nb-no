---
title: Flytte, erstatte og installere aktiva
description: Dette emnet forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec150adb35eb0600844245b14cbec9e9632ab337
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889559"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="02447-103">Flytte, erstatte og installere aktiva</span><span class="sxs-lookup"><span data-stu-id="02447-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="02447-104">Dette emnet forklarer hvordan du flytter, erstatter og installerer aktiva i Aktivabehandling.</span><span class="sxs-lookup"><span data-stu-id="02447-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="02447-105">Du kan opprette individuelle aktiva som ikke har noen relasjoner til andre aktiva, eller du kan opprette en aktivastruktur som inkluderer et overordnet objekt (aktiva på øverste nivå) og relaterte underordnede aktiva (underobjekter).</span><span class="sxs-lookup"><span data-stu-id="02447-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="02447-106">I Aktivabehandling er det tre tilnærminger til flytting og endre plasseringen av et aktivum:</span><span class="sxs-lookup"><span data-stu-id="02447-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="02447-107">**Flytte** – Flytt et aktivum til en annen aktivastruktur eller et annen sted i den samme aktivastrukturen.</span><span class="sxs-lookup"><span data-stu-id="02447-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="02447-108">**Erstatt** – Midlertidig fjern et aktivum fra en aktivastruktur slik at den kan repareres eller pusses opp, og deretter legge til det renoverte aktivumet tilbake til aktivastrukturen senere.</span><span class="sxs-lookup"><span data-stu-id="02447-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="02447-109">Du kan også erstatte et brukt aktivum permanent med et nytt aktivum.</span><span class="sxs-lookup"><span data-stu-id="02447-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="02447-110">**Installer** – Installer et overordnet objekt og tilknyttede underordnede aktiva på et arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="02447-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="02447-111">Aktivaet du flytter, erstatter eller installerer, kan være relatert til et annet arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="02447-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="02447-112">I så fall kan aktivumet bruke finansdimensjoner for arbeidsstedet.</span><span class="sxs-lookup"><span data-stu-id="02447-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="02447-113">På siden **Arbeidsstedstyper** definerer du håndteringen av finansdimensjoner på arbeidssteder.</span><span class="sxs-lookup"><span data-stu-id="02447-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="02447-114">Flytt aktivum</span><span class="sxs-lookup"><span data-stu-id="02447-114">Move asset</span></span>

<span data-ttu-id="02447-115">Bruk **Flytt aktivum**-funksjonen til å flytte et aktivum til en annen aktivastruktur eller et annet sted i den samme aktivastrukturen.</span><span class="sxs-lookup"><span data-stu-id="02447-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="02447-116">Du kan også flytte et aktivum ut av en aktivastruktur slik at det blir et frittstående aktivum som ikke har noen strukturrelasjoner.</span><span class="sxs-lookup"><span data-stu-id="02447-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="02447-117">Ikke bruk denne funksjonen hvis aktiva repareres eller byttes ut midlertidig.</span><span class="sxs-lookup"><span data-stu-id="02447-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="02447-118">Bruk i stedet funksjonen **Erstatt aktivum** som er beskrevet senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="02447-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="02447-119">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="02447-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="02447-120">Velg aktivumet som skal flyttes, fra listen.</span><span class="sxs-lookup"><span data-stu-id="02447-120">In the list, select the asset to move.</span></span> <span data-ttu-id="02447-121">Hvis aktivaet har underordnede aktiva, flytter du også disse.</span><span class="sxs-lookup"><span data-stu-id="02447-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="02447-122">Velg **Flytt aktivum**.</span><span class="sxs-lookup"><span data-stu-id="02447-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="02447-123">Hvis du vil flytte aktivumet slik at det blir en del av en aktivastruktur, velger du det nye overordnede objektet i feltet **Overordnet objekt**.</span><span class="sxs-lookup"><span data-stu-id="02447-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="02447-124">Hvis du flytter et underordnet aktivum og vil gjøre det til et frittstående aktivum som ikke har noen strukturrelasjoner, lar du feltet **Overordnet objekt** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="02447-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="02447-125">Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="02447-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="02447-126">Du kan imidlertid velge en annen dato og klokkeslett som flyttingen av aktivumet skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="02447-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="02447-127">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02447-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="02447-128">Erstatt aktivum</span><span class="sxs-lookup"><span data-stu-id="02447-128">Replace asset</span></span>

<span data-ttu-id="02447-129">Bruk funksjonen **Erstatt aktivum** i forbindelse med reparasjoner, oppussing eller permanent utskifting av et utslitt aktivum med et nytt aktivum.</span><span class="sxs-lookup"><span data-stu-id="02447-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="02447-130">Denne funksjonen brukes til å erstatte underordnede aktiva i en aktivastruktur.</span><span class="sxs-lookup"><span data-stu-id="02447-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="02447-131">For overordnede objekter (det vil si aktiva som for øyeblikket ikke har et overordnet objekt), utføres denne erstatningen på et arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="02447-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="02447-132">Hvis du vil ha mer informasjon om hvordan du erstatter overordnede objekter på et arbeidssted, kan du se [Installere aktiva på arbeidssteder](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="02447-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="02447-133">Hvis et verksted er knyttet til produksjonsavdelingen, kan du opprette arbeidssteder som **Reparasjon**, **Svinn**og **Lager** for å håndtere reparasjon og utskifting av aktiva.</span><span class="sxs-lookup"><span data-stu-id="02447-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="02447-134">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="02447-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="02447-135">Velg det underordnede aktivumet som skal erstattes, fra listen.</span><span class="sxs-lookup"><span data-stu-id="02447-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="02447-136">Hvis aktivaet har underordnede aktiva, erstatter du også disse.</span><span class="sxs-lookup"><span data-stu-id="02447-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="02447-137">Velg **Erstatt aktivum**.</span><span class="sxs-lookup"><span data-stu-id="02447-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="02447-138">Feltet **Strukturendring** viser siste dato og klokkeslett da det valgte aktivumet og tilknyttede underordnede aktiva ble flyttet i aktivastrukturen.</span><span class="sxs-lookup"><span data-stu-id="02447-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="02447-139">I delen **Valgte aktiva** i feltet **Målarbeidssted** velger du arbeidsstedet du vil flytte aktivumet til.</span><span class="sxs-lookup"><span data-stu-id="02447-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="02447-140">Velg for eksempel stedet **Reparasjon** eller **Svinn**.</span><span class="sxs-lookup"><span data-stu-id="02447-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="02447-141">I delen **Overordnet objekt** viser feltet **Gyldighet** den siste datoen og klokkeslettet da det overordnede objektet og relaterte underordnede aktiva ble installert eller flyttet på det gjeldende arbeidsstedet.</span><span class="sxs-lookup"><span data-stu-id="02447-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="02447-142">I delen **Nytt aktivum** i **Aktivum**-feltet velger du aktivumet som skal settes inn som en midlertidig eller permanent erstatning for det valgte aktivumet.</span><span class="sxs-lookup"><span data-stu-id="02447-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="02447-143">Dette aktivumet kan for øyeblikket være plassert på et annet arbeidssted, for eksempel **Lager**.</span><span class="sxs-lookup"><span data-stu-id="02447-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="02447-144">I delen **Gyldig fra** settes feltet **Gyldighet** til gjeldende dato og klokkeslett som standard.</span><span class="sxs-lookup"><span data-stu-id="02447-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="02447-145">Du kan imidlertid velge en annen dato og klokkeslett som erstatningen av aktivumet skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="02447-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="02447-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02447-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="02447-147">Installer aktivum</span><span class="sxs-lookup"><span data-stu-id="02447-147">Install asset</span></span>

<span data-ttu-id="02447-148">Bruk funksjonen **Installer aktivum** til å installere en aktivastruktur på et arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="02447-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="02447-149">Velg alltid et overordnet objekt.</span><span class="sxs-lookup"><span data-stu-id="02447-149">Always select a parent asset.</span></span> <span data-ttu-id="02447-150">Det overordnede objektet og tilknyttede underordnede aktiva vil bli flyttet til det valgte arbeidsstedet.</span><span class="sxs-lookup"><span data-stu-id="02447-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="02447-151">Velg **Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**.</span><span class="sxs-lookup"><span data-stu-id="02447-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="02447-152">I listen velger du det overordnede objektet som skal installeres på et annet arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="02447-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="02447-153">Velg **Installer aktivum**.</span><span class="sxs-lookup"><span data-stu-id="02447-153">Select **Install asset**.</span></span>

    <span data-ttu-id="02447-154">I **Attributter**-delen vises aktivaattributtene som er definert på det overordnede objektet.</span><span class="sxs-lookup"><span data-stu-id="02447-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="02447-155">Velg det nye arbeidsstedet i **Arbeidssted**-feltet.</span><span class="sxs-lookup"><span data-stu-id="02447-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="02447-156">Som standard settes feltet **Gyldighet** til gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="02447-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="02447-157">Du kan imidlertid velge en annen dato og klokkeslett som installeringen av aktivastrukturen skal være gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="02447-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="02447-158">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02447-158">Select **OK**.</span></span>
