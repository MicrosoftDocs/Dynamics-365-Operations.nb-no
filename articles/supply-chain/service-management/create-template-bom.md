---
title: Opprette en malstykkliste
description: Du kan opprette en malstykkliste ved å bruke flere metoder.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 781df7611ec1e3ee9d3013f971232700df38ada0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836308"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="a3dba-103">Opprette en malstykkliste</span><span class="sxs-lookup"><span data-stu-id="a3dba-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a3dba-104">Du kan opprette en malstykkliste ved å bruke en av følgende metoder.</span><span class="sxs-lookup"><span data-stu-id="a3dba-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="a3dba-105">For alle metodene er feltene **Fra dato** og **Til dato** valgfrie og bare til informasjon.</span><span class="sxs-lookup"><span data-stu-id="a3dba-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="a3dba-106">Opprette en malstykkliste manuelt</span><span class="sxs-lookup"><span data-stu-id="a3dba-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="a3dba-107">Gå til **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a3dba-108">Velg **Ny** for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a3dba-109">Under **Kopier stykklistelinjer fra referanse** velger du **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="a3dba-110">I **Varenummer**-feltet angir du en vare av typen **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="a3dba-111">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="a3dba-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a3dba-112">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3dba-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a3dba-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-113">Select **OK**.</span></span>

<span data-ttu-id="a3dba-114">Det opprettes en ny, tom malstykkliste.</span><span class="sxs-lookup"><span data-stu-id="a3dba-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="a3dba-115">Opprette en malstykkliste basert på en annen malstykkliste</span><span class="sxs-lookup"><span data-stu-id="a3dba-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="a3dba-116">Velg **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a3dba-117">Velg **Ny** for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a3dba-118">Under **Kopier stykklistelinjer fra referanse** velger du **Malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="a3dba-119">I **Referansenummer**-feltet velger du en eksisterende malstykkliste som skal kopieres til den nye malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="a3dba-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="a3dba-120">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="a3dba-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a3dba-121">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3dba-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a3dba-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-122">Select **OK**.</span></span>

<span data-ttu-id="a3dba-123">En ny malstykkliste opprettes ved hjelp av linjer som svarer til linjene i den opprinnelige malstykklisten.</span><span class="sxs-lookup"><span data-stu-id="a3dba-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="a3dba-124">Opprette en malstykkliste basert på en varestykkliste</span><span class="sxs-lookup"><span data-stu-id="a3dba-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="a3dba-125">Velg **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a3dba-126">Velg **Ny** for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a3dba-127">Under **Kopier stykklistelinjer fra referanse** velger du **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="a3dba-128">I **Referansenummer**-feltet velger du en stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="a3dba-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="a3dba-129">En vare av typen stykkliste kopieres til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="a3dba-130">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="a3dba-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a3dba-131">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3dba-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a3dba-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-132">Select **OK**.</span></span>

<span data-ttu-id="a3dba-133">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykklister**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="a3dba-134">Opprette en malstykkliste basert på en produksjonsstykkliste</span><span class="sxs-lookup"><span data-stu-id="a3dba-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="a3dba-135">Velg **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="a3dba-136">Velg **Ny** for å åpne skjemaet **Opprett malstykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="a3dba-137">Under **Kopier stykklistelinjer fra referanse** velger du **Produksjon**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="a3dba-138">I **Referansenummer**-feltet velger du en produksjonsstykkliste.</span><span class="sxs-lookup"><span data-stu-id="a3dba-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="a3dba-139">I **Navn**-feltet angir du et navn på malen.</span><span class="sxs-lookup"><span data-stu-id="a3dba-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="a3dba-140">I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.</span><span class="sxs-lookup"><span data-stu-id="a3dba-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="a3dba-141">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-141">Select **OK**.</span></span>

<span data-ttu-id="a3dba-142">Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykkliste**.</span><span class="sxs-lookup"><span data-stu-id="a3dba-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3dba-143">Se også</span><span class="sxs-lookup"><span data-stu-id="a3dba-143">See also</span></span>

[<span data-ttu-id="a3dba-144">Stykklistemaler </span><span class="sxs-lookup"><span data-stu-id="a3dba-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]