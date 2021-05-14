---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921017"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="c1424-103">Opprette en produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="c1424-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1424-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="c1424-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="c1424-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="c1424-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="c1424-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="c1424-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c1424-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="c1424-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="c1424-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="c1424-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="c1424-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="c1424-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="c1424-110">Gå til **Behandling av produktinformasjon \> Oppsett \> Produktterminologi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="c1424-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1424-111">Select **New**.</span></span>
1. <span data-ttu-id="c1424-112">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="c1424-113">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="c1424-114">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-114">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-115">Velg **Produktstandardnummer**.</span><span class="sxs-lookup"><span data-stu-id="c1424-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="c1424-116">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-116">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-117">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="c1424-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="c1424-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-119">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="c1424-120">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-120">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-121">Velg **Konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="c1424-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="c1424-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="c1424-123">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="c1424-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="c1424-124">Gå til **Behandling av produktinformasjon \> Produkter \> Produktstandarder**.</span><span class="sxs-lookup"><span data-stu-id="c1424-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="c1424-125">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="c1424-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c1424-126">Du kan for eksempel filtrere på **Produktnummer**-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="c1424-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="c1424-127">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="c1424-128">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c1424-128">Select **Edit**.</span></span>
1. <span data-ttu-id="c1424-129">Velg *Ja* i feltet **Bruk nomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="c1424-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="c1424-130">Angi eller velg en verdi i feltet **Produktvariantnummerterminologi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-131">Close the page.</span></span>
1. <span data-ttu-id="c1424-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="c1424-133">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="c1424-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="c1424-134">Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="c1424-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="c1424-135">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="c1424-136">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="c1424-137">Velg **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c1424-137">Select **Edit**.</span></span>
1. <span data-ttu-id="c1424-138">Velg *Ja* i feltet **Bruk konfigurasjonsnomenklatur**.</span><span class="sxs-lookup"><span data-stu-id="c1424-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="c1424-139">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-139">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-140">Velg **Attributtverdi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="c1424-141">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-142">Angi eller velg en verdi i feltet **Attributt**.</span><span class="sxs-lookup"><span data-stu-id="c1424-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-143">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-143">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-144">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="c1424-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="c1424-145">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-146">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="c1424-147">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-147">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-148">Velg **Attributtverdi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="c1424-149">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-150">Angi eller velg en verdi i feltet **Attributt**.</span><span class="sxs-lookup"><span data-stu-id="c1424-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-151">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-151">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-152">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="c1424-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="c1424-153">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-154">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="c1424-155">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-155">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-156">Velg **Attributtverdi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="c1424-157">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-158">Angi eller velg en verdi i feltet **Attributt**.</span><span class="sxs-lookup"><span data-stu-id="c1424-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-159">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-159">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-160">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="c1424-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="c1424-161">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-162">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="c1424-163">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-163">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-164">Velg **Attributtverdi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="c1424-165">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-166">Angi eller velg en verdi i feltet **Attributt**.</span><span class="sxs-lookup"><span data-stu-id="c1424-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-167">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-167">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-168">Velg **Tekstkonstant**.</span><span class="sxs-lookup"><span data-stu-id="c1424-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="c1424-169">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-170">Skriv inn en verdi i **Tekst**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="c1424-171">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="c1424-171">Select **Add**.</span></span>
1. <span data-ttu-id="c1424-172">Velg **Nummerserieverdi**.</span><span class="sxs-lookup"><span data-stu-id="c1424-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="c1424-173">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c1424-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="c1424-174">Angi eller velg en verdi i **Nummerserieverdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c1424-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="c1424-175">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-175">Close the page.</span></span>
1. <span data-ttu-id="c1424-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-176">Close the page.</span></span>
1. <span data-ttu-id="c1424-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c1424-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]