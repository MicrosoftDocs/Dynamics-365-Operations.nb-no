---
title: Bytte mellom leverandørutforminger
description: Dette emnet beskriver hvordan du bytter integreringen av leverandørdata mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750600"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="4a0e9-103">Bytte mellom leverandørutforminger</span><span class="sxs-lookup"><span data-stu-id="4a0e9-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="4a0e9-104">Flyt for leverandørdata</span><span class="sxs-lookup"><span data-stu-id="4a0e9-104">Vendor data flow</span></span> 

<span data-ttu-id="4a0e9-105">Hvis du velger å bruke **Konto**-tabellen til å lagre leverandører av **Organisasjon**-typen og **Kontakt**-tabellen til å lagre leverandører av **Person**-typen, konfigurerer du følgende arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="4a0e9-106">Hvis ikke kreves ikke denne konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="4a0e9-107">Bruke den utvidede leverandørutformingen for leverandører av typen Organisasjon</span><span class="sxs-lookup"><span data-stu-id="4a0e9-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="4a0e9-108">**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler:</span><span class="sxs-lookup"><span data-stu-id="4a0e9-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4a0e9-109">Du vil opprette en arbeidsflyt for hver mal.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4a0e9-110">Opprette leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="4a0e9-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="4a0e9-111">Opprette leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="4a0e9-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="4a0e9-112">Oppdatere leverandører i tabellen Kontoer</span><span class="sxs-lookup"><span data-stu-id="4a0e9-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="4a0e9-113">Oppdatere leverandører i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="4a0e9-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="4a0e9-114">Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="4a0e9-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4a0e9-115">Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører i tabellen Kontoer**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="4a0e9-116">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-116">Then select **OK**.</span></span> <span data-ttu-id="4a0e9-117">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Arbeidsflytprosessen Opprette leverandører i tabellen Kontoer](media/create_process.png)

2. <span data-ttu-id="4a0e9-119">Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører i tabellen Kontoer**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="4a0e9-120">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-120">Then select **OK**.</span></span> <span data-ttu-id="4a0e9-121">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="4a0e9-122">Opprett en ny arbeidsflytprosess for **Konto**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører i tabellen Leverandører**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="4a0e9-123">Opprett en ny arbeidsflytprosess for **Konto**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører i tabellen Leverandører**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="4a0e9-124">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4a0e9-125">Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Knappen Konverter til en bakgrunnsarbeidsflyt](media/background_workflow.png)

6. <span data-ttu-id="4a0e9-127">Aktiver arbeidsflytene du opprettet for tabellene **Konto** og **Leverandør**, for å begynne å bruke **Konto**-tabellen til å lagre informasjon for leverandører av **Organisasjon**-typen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="4a0e9-128">Bruke den utvidede leverandørutformingen for leverandører av typen Person</span><span class="sxs-lookup"><span data-stu-id="4a0e9-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="4a0e9-129">**Dynamics365FinanceExtended**-løsningspakken inneholder følgende arbeidsflytprosess-maler:</span><span class="sxs-lookup"><span data-stu-id="4a0e9-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="4a0e9-130">Du vil opprette en arbeidsflyt for hver mal.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="4a0e9-131">Opprette leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="4a0e9-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="4a0e9-132">Opprette leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="4a0e9-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="4a0e9-133">Oppdatere leverandører av typen Person i tabellen Kontakter</span><span class="sxs-lookup"><span data-stu-id="4a0e9-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="4a0e9-134">Oppdatere leverandører av typen Person i tabellen Leverandører</span><span class="sxs-lookup"><span data-stu-id="4a0e9-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="4a0e9-135">Slik oppretter du nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="4a0e9-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="4a0e9-136">Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i tabellen Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="4a0e9-137">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-137">Then select **OK**.</span></span> <span data-ttu-id="4a0e9-138">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Kontakt**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="4a0e9-139">Opprett en ny arbeidsflytprosess for **Leverandør**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i tabellen Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="4a0e9-140">Velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-140">Then select **OK**.</span></span> <span data-ttu-id="4a0e9-141">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Kontakt**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="4a0e9-142">Opprett en ny arbeidsflytprosess for **Kontakt**-tabellen, og velg arbeidsflytprosess-malen **Opprette leverandører av typen Person i tabellen Leverandører**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="4a0e9-143">Opprett en ny arbeidsflytprosess for **Kontakt**-tabellen, og velg arbeidsflytprosess-malen **Oppdatere leverandører av typen Person i tabellen Leverandører**.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="4a0e9-144">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="4a0e9-145">Velg **Konverter til en bakgrunnsarbeidsflyt** for å konfigurere en arbeidsflyt som en bakgrunnsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="4a0e9-146">Aktiver arbeidsflytene du opprettet for tabellene **Kontakt** og **Leverandør**, for å begynne å bruke **Kontakt**-tabellen til å lagre informasjon for leverandører av **Person**-typen.</span><span class="sxs-lookup"><span data-stu-id="4a0e9-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]