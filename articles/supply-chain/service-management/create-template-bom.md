---
title: Opprette en malstykkliste
description: Du kan opprette en malstykkliste ved å bruke flere metoder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b34cc2e9921df6e3ef619e2b2adaf8d2069fbac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974566"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="2a884-103">Opprette en malstykkliste</span><span class="sxs-lookup"><span data-stu-id="2a884-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2a884-104">Du kan opprette en malstykkliste ved å bruke en av følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="2a884-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="2a884-105">For alle metodene er feltene **Fra dato** og **Til dato** valgfrie og bare til informasjon.</span><span class="sxs-lookup"><span data-stu-id="2a884-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="2a884-106">Opprette en malstykkliste manuelt</span><span class="sxs-lookup"><span data-stu-id="2a884-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="2a884-107">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="2a884-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2a884-108">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2a884-109">Under **Kopier stykklistelinjer fra referanse** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="2a884-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="2a884-110">I **Varenummer**-feltet angir du en vare av typen **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="2a884-111">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="2a884-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2a884-112">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="2a884-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2a884-113">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a884-113">Click **OK**.</span></span>

<span data-ttu-id="2a884-114">Det opprettes en ny, tom malstykkliste.</span><span class="sxs-lookup"><span data-stu-id="2a884-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="2a884-115">Opprette en malstykkliste basert på en annen malstykkliste</span><span class="sxs-lookup"><span data-stu-id="2a884-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="2a884-116">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="2a884-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2a884-117">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2a884-118">Under **Kopier stykklistelinjer fra referanse** velger du **Malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="2a884-119">I **Referansenummer**-feltet velger du en eksisterende malstykkliste som skal kopieres til den nye malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="2a884-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="2a884-120">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="2a884-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2a884-121">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="2a884-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2a884-122">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a884-122">Click **OK**.</span></span>

<span data-ttu-id="2a884-123">En ny malstykkliste opprettes ved hjelp av linjer som svarer til linjene i den opprinnelige malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="2a884-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="2a884-124">Opprette en malstykkliste basert på en varestykkliste</span><span class="sxs-lookup"><span data-stu-id="2a884-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="2a884-125">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="2a884-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2a884-126">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2a884-127">Under **Kopier stykklistelinjer fra referanse** velger du **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="2a884-128">I **Referansenummer**-feltet velger du en stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="2a884-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="2a884-129">En vare av typen stykkliste kopieres til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="2a884-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="2a884-130">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="2a884-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2a884-131">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="2a884-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2a884-132">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a884-132">Click **OK**.</span></span>

<span data-ttu-id="2a884-133">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykklister**.</span><span class="sxs-lookup"><span data-stu-id="2a884-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="2a884-134">Opprette en malstykkliste basert på en produksjonsstykkliste</span><span class="sxs-lookup"><span data-stu-id="2a884-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="2a884-135">Klikk på **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="2a884-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="2a884-136">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="2a884-137">Under **Kopier stykklistelinjer fra referanse** velger du **Produksjon**.</span><span class="sxs-lookup"><span data-stu-id="2a884-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="2a884-138">I **Referansenummer**-feltet velger du en produksjonsstykkliste.</span><span class="sxs-lookup"><span data-stu-id="2a884-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="2a884-139">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="2a884-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="2a884-140">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="2a884-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="2a884-141">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a884-141">Click **OK**.</span></span>

<span data-ttu-id="2a884-142">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="2a884-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="2a884-143">Se også</span><span class="sxs-lookup"><span data-stu-id="2a884-143">See also</span></span>

[<span data-ttu-id="2a884-144">Stykklistemaler </span><span class="sxs-lookup"><span data-stu-id="2a884-144">Template BOMs</span></span>](template-boms.md)

  


