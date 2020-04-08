---
title: Bytte mellom leverandørutforminger
description: Dette emnet beskriver hvordan du bytter integreringen av leverandørdata mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173045"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="820a1-103">Bytte mellom leverandørutforminger</span><span class="sxs-lookup"><span data-stu-id="820a1-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="820a1-104">Flyt for leverandørdata</span><span class="sxs-lookup"><span data-stu-id="820a1-104">Vendor data flow</span></span> 

<span data-ttu-id="820a1-105">Hvis du velger å bruke **Konto**-enheten til å lagre leverandører av **Organisasjon**-typen og **Kontakt**-enheten til å lagre leverandører av **Person**-typen, konfigurerer du følgende arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="820a1-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="820a1-106">Hvis ikke kreves ikke denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="820a1-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="820a1-107">Bruke den utvidede leverandørutformingen for leverandører av typen Organisasjon</span><span class="sxs-lookup"><span data-stu-id="820a1-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="820a1-108">**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler:</span><span class="sxs-lookup"><span data-stu-id="820a1-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="820a1-109">Du vil opprette en arbeidsflyt for hver mal.</span><span class="sxs-lookup"><span data-stu-id="820a1-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="820a1-110">Opprette leverandører i kontoenhet</span><span class="sxs-lookup"><span data-stu-id="820a1-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="820a1-111">Opprette leverandører i leverandørenhet</span><span class="sxs-lookup"><span data-stu-id="820a1-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="820a1-112">Oppdatere leverandører i kontoenhet</span><span class="sxs-lookup"><span data-stu-id="820a1-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="820a1-113">Oppdatere leverandører i leverandørenhet</span><span class="sxs-lookup"><span data-stu-id="820a1-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="820a1-114">Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="820a1-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="820a1-115">Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører i kontoenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="820a1-116">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="820a1-116">Then select **OK**.</span></span> <span data-ttu-id="820a1-117">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="820a1-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Arbeidsflytprosessen Opprette leverandører i kontoenhet](media/create_process.png)

2. <span data-ttu-id="820a1-119">Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører i kontoenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="820a1-120">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="820a1-120">Then select **OK**.</span></span> <span data-ttu-id="820a1-121">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="820a1-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="820a1-122">Opprett en ny arbeidsflytprosess for **Konto**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører i leverandørenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="820a1-123">Opprett en ny arbeidsflytprosess for **Konto**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører i leverandørenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="820a1-124">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="820a1-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="820a1-125">Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="820a1-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Knappen Konverter til en bakgrunnsarbeidsflyt](media/background_workflow.png)

6. <span data-ttu-id="820a1-127">Aktiver arbeidsflytene du opprettet for **konto**- og **leverandør**-enhetene for å begynne å bruke **Konto** -enheten til å lagre informasjon for leverandører av **Organisasjon**-typen.</span><span class="sxs-lookup"><span data-stu-id="820a1-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="820a1-128">Bruke den utvidede leverandørutformingen for leverandører av typen Person</span><span class="sxs-lookup"><span data-stu-id="820a1-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="820a1-129">**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler:</span><span class="sxs-lookup"><span data-stu-id="820a1-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="820a1-130">Du vil opprette en arbeidsflyt for hver mal.</span><span class="sxs-lookup"><span data-stu-id="820a1-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="820a1-131">Opprette leverandører av typen Person i leverandørenheten</span><span class="sxs-lookup"><span data-stu-id="820a1-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="820a1-132">Opprette leverandører av typen Person i kontaktenheten</span><span class="sxs-lookup"><span data-stu-id="820a1-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="820a1-133">Oppdatere leverandører av typen Person i kontaktenheten</span><span class="sxs-lookup"><span data-stu-id="820a1-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="820a1-134">Oppdatere leverandører av typen Person i leverandørenheten</span><span class="sxs-lookup"><span data-stu-id="820a1-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="820a1-135">Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="820a1-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="820a1-136">Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i kontaktenheten**.</span><span class="sxs-lookup"><span data-stu-id="820a1-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="820a1-137">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="820a1-137">Then select **OK**.</span></span> <span data-ttu-id="820a1-138">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Kontakt**-enheten.</span><span class="sxs-lookup"><span data-stu-id="820a1-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="820a1-139">Opprett en ny arbeidsflytprosess for **Leverandør**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i kontaktenheten**.</span><span class="sxs-lookup"><span data-stu-id="820a1-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="820a1-140">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="820a1-140">Then select **OK**.</span></span> <span data-ttu-id="820a1-141">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Kontakt**-enheten.</span><span class="sxs-lookup"><span data-stu-id="820a1-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="820a1-142">Opprett en ny arbeidsflytprosess for **Kontakt**-enheten, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i leverandørenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="820a1-143">Opprett en ny arbeidsflytprosess for **Kontakt**-enheten, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i leverandørenhet**.</span><span class="sxs-lookup"><span data-stu-id="820a1-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="820a1-144">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="820a1-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="820a1-145">Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="820a1-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="820a1-146">Aktiver arbeidsflytene du opprettet for **kontakt**- og **leverandør**-enhetene for å begynne å bruke **Kontakt** -enheten til å lagre informasjon for leverandører av **Person**-typen.</span><span class="sxs-lookup"><span data-stu-id="820a1-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
