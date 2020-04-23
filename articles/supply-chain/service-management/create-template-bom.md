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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 815b6b726e9a76a9294995bc5689b030cf623ec0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202589"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="b3438-103">Opprette en malstykkliste</span><span class="sxs-lookup"><span data-stu-id="b3438-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b3438-104">Du kan opprette en malstykkliste ved å bruke en av følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="b3438-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="b3438-105">For alle metodene er feltene **Fra dato** og **Til dato** valgfrie og bare til informasjon.</span><span class="sxs-lookup"><span data-stu-id="b3438-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="b3438-106">Opprette en malstykkliste manuelt</span><span class="sxs-lookup"><span data-stu-id="b3438-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="b3438-107">Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="b3438-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b3438-108">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b3438-109">Under **Kopier stykklistelinjer fra referanse** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="b3438-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="b3438-110">I **Varenummer**-feltet angir du en vare av typen **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="b3438-111">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="b3438-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b3438-112">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="b3438-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b3438-113">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3438-113">Click **OK**.</span></span>

<span data-ttu-id="b3438-114">Det opprettes en ny, tom malstykkliste.</span><span class="sxs-lookup"><span data-stu-id="b3438-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="b3438-115">Opprette en malstykkliste basert på en annen malstykkliste</span><span class="sxs-lookup"><span data-stu-id="b3438-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="b3438-116">Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="b3438-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b3438-117">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b3438-118">Under **Kopier stykklistelinjer fra referanse** velger du **Malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="b3438-119">I **Referansenummer**-feltet velger du en eksisterende malstykkliste som skal kopieres til den nye malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="b3438-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="b3438-120">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="b3438-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b3438-121">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="b3438-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b3438-122">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3438-122">Click **OK**.</span></span>

<span data-ttu-id="b3438-123">En ny malstykkliste opprettes ved hjelp av linjer som svarer til linjene i den opprinnelige malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="b3438-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="b3438-124">Opprette en malstykkliste basert på en varestykkliste</span><span class="sxs-lookup"><span data-stu-id="b3438-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="b3438-125">Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="b3438-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b3438-126">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b3438-127">Under **Kopier stykklistelinjer fra referanse** velger du **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="b3438-128">I **Referansenummer**-feltet velger du en stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="b3438-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="b3438-129">En vare av typen stykkliste kopieres til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="b3438-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="b3438-130">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="b3438-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b3438-131">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="b3438-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b3438-132">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3438-132">Click **OK**.</span></span>

<span data-ttu-id="b3438-133">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykklister**.</span><span class="sxs-lookup"><span data-stu-id="b3438-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="b3438-134">Opprette en malstykkliste basert på en produksjonsstykkliste</span><span class="sxs-lookup"><span data-stu-id="b3438-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="b3438-135">Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="b3438-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="b3438-136">Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="b3438-137">Under **Kopier stykklistelinjer fra referanse** velger du **Produksjon**.</span><span class="sxs-lookup"><span data-stu-id="b3438-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="b3438-138">I **Referansenummer**-feltet velger du en produksjonsstykkliste.</span><span class="sxs-lookup"><span data-stu-id="b3438-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="b3438-139">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="b3438-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="b3438-140">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="b3438-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="b3438-141">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3438-141">Click **OK**.</span></span>

<span data-ttu-id="b3438-142">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="b3438-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3438-143">Se også</span><span class="sxs-lookup"><span data-stu-id="b3438-143">See also</span></span>

[<span data-ttu-id="b3438-144">Stykklistemaler </span><span class="sxs-lookup"><span data-stu-id="b3438-144">Template BOMs</span></span>](template-boms.md)

  


