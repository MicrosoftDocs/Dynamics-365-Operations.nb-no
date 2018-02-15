---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter mellom Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1f76359878d162e93d8f8b7c11be529c43c94455
ms.openlocfilehash: 9b150bfca362303b4ac35a38ab818229082c7330
ms.contentlocale: nb-no
ms.lasthandoff: 02/08/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="c1d11-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="c1d11-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1d11-104">Løsningen Kundeemne til kontanter gir direkte synkronisering på tvers av Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="c1d11-105">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="c1d11-106">Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1d11-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="c1d11-107">Hvis du vil ha mer informasjon om kundeemne til kontanter-integrering, se den korte YouTube-videoen:</span><span class="sxs-lookup"><span data-stu-id="c1d11-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="c1d11-108">I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:</span><span class="sxs-lookup"><span data-stu-id="c1d11-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="c1d11-109">Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="c1d11-110">Beholde produkter i Finance and Operations og synkronisere dem til direkte til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="c1d11-111">Beholde kontakter i Sales og synkronisere dem direkte til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="c1d11-112">Synkronisere salgstilbud direkte fra Sales til Finance and Operations (mal venter på frigivelse)</span><span class="sxs-lookup"><span data-stu-id="c1d11-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="c1d11-113">Synkronisere salgsordrer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="c1d11-114">Synkronisere salgsordrer direkte mellom Sales og Finance and Operations (mal venter på frigivelse)</span><span class="sxs-lookup"><span data-stu-id="c1d11-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="c1d11-115">Synkronisere salgsfaktura direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="c1d11-116">I tidligere versjoner inneholder Kundeemne til kontanter-løsningen følgende typer ikke-direkte synkronisering:</span><span class="sxs-lookup"><span data-stu-id="c1d11-116">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="c1d11-117">Behold kontoer i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-117">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="c1d11-118">Beholde kontakter i Sales og synkronisere dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-118">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="c1d11-119">Beholde produkter i Finance and Operations og synkronisere dem til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-119">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="c1d11-120">Opprette salgstilbud i Sales og synkronisere dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-120">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="c1d11-121">Opprette salgsordrer i Finance and Operations og synkronisere dem til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-121">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="c1d11-122">Opprette salgsfakturaer i Finance and Operations og synkronisere dem til Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-122">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="c1d11-123">Systemkrav for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1d11-123">System requirements for Finance and Operations</span></span>

<span data-ttu-id="c1d11-124">Kundeemne til kontanter-integrasjon støttes i følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="c1d11-124">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="c1d11-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (desember 2017)</span><span class="sxs-lookup"><span data-stu-id="c1d11-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="c1d11-126">Dynamics 365 for Finance and Operations, Enterprise edition (desember 2017) - programbygg 7.3.11971.56116 med plattformoppdatering 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="c1d11-126">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="c1d11-127">Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="c1d11-127">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="c1d11-128">Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) – plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="c1d11-128">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="c1d11-129">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="c1d11-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="c1d11-130">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1d11-130">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="c1d11-131">I tillegg inneholder den flere forbedringer.</span><span class="sxs-lookup"><span data-stu-id="c1d11-131">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="c1d11-132">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinjer via dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-132">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="c1d11-133">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-133">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c1d11-134">Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre hurtigreparasjonene.</span><span class="sxs-lookup"><span data-stu-id="c1d11-134">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="c1d11-135">Dynamics 365 for Finance and Operations versjon 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="c1d11-135">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="c1d11-136">Dynamics 365 for Finance and Operations versjon 1611 (november 2016) med plattformoppdatering 8 eller høyere</span><span class="sxs-lookup"><span data-stu-id="c1d11-136">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="c1d11-137">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="c1d11-137">The following hotfixes are required:</span></span>

    - <span data-ttu-id="c1d11-138">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Aktiver salgsordresynkronisering med dataintegrator fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-138">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="c1d11-139">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Aktiver salgsordrehode- og linjesynkronisering med dataintegrator fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="c1d11-139">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="c1d11-140">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves.</span><span class="sxs-lookup"><span data-stu-id="c1d11-140">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c1d11-141">Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="c1d11-141">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="c1d11-142">Dette skjemaet skjules siden du bare trenger det én gang.</span><span class="sxs-lookup"><span data-stu-id="c1d11-142">This form is hidden because you only need it once.</span></span> <span data-ttu-id="c1d11-143">Hvis du vil ha tilgang til skjemaet, logger du på miljøet og legger til følgende i URL-en i leseradressen: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="c1d11-143">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="c1d11-144">Når skjemaet åpnes, klikker du på OK.</span><span class="sxs-lookup"><span data-stu-id="c1d11-144">When the form opens, click OK.</span></span> <span data-ttu-id="c1d11-145">Dette vil fylle ut et nytt felt **LineCreationSequnceNumber** i tabellen **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med unike verdier og oppdatere varelisten.</span><span class="sxs-lookup"><span data-stu-id="c1d11-145">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="c1d11-146">Dette er nødvendig for at kundeemne til kontanter-integrasjonen skal fungere.</span><span class="sxs-lookup"><span data-stu-id="c1d11-146">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="c1d11-147">Systemkrav for Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-147">System requirements for Sales</span></span>

<span data-ttu-id="c1d11-148">For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="c1d11-148">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="c1d11-149">Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online</span><span class="sxs-lookup"><span data-stu-id="c1d11-149">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="c1d11-150">Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="c1d11-150">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="c1d11-151">Maler med versjon 1.0.0.0 og 1.0.0.1 støttes for Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.1.0</span><span class="sxs-lookup"><span data-stu-id="c1d11-151">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="c1d11-152">Maler med versjon 2.0.0.0 og 2.1.0.0 støttes for Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.15.0.0</span><span class="sxs-lookup"><span data-stu-id="c1d11-152">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c1d11-153">Installere Kundeemne til kontanter-løsningen for Sales</span><span class="sxs-lookup"><span data-stu-id="c1d11-153">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="c1d11-154">Last ned [Kundeemne til kontanter for Dynamics 365 for Sales, løsningspakke zip-fil](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) fra CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="c1d11-154">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="c1d11-155">Kontroller at zip-filen ikke er blokkert.</span><span class="sxs-lookup"><span data-stu-id="c1d11-155">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="c1d11-156">Ellers, når du prøver å installere løsningspakken, kan du få følgende feilmelding: "Finner ingen importpakker".</span><span class="sxs-lookup"><span data-stu-id="c1d11-156">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="c1d11-157">Hvis du vil fjerne blokkeringen av ZIP-filen, høyreklikker du den og velger **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="c1d11-157">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="c1d11-158">Velg **Fjern blokkering**.</span><span class="sxs-lookup"><span data-stu-id="c1d11-158">Select **Unblock**.</span></span>
3. <span data-ttu-id="c1d11-159">Pakk ut og kjør **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="c1d11-159">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="c1d11-160">Installer Kundeemne til kontanter-løsningen på forekomsten din av Sales:</span><span class="sxs-lookup"><span data-stu-id="c1d11-160">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="c1d11-161">Velg **Office 365** som implementasjonstype.</span><span class="sxs-lookup"><span data-stu-id="c1d11-161">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="c1d11-162">Velg **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="c1d11-162">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="c1d11-163">For en hurtiginstallasjon, velg et område.</span><span class="sxs-lookup"><span data-stu-id="c1d11-163">For a quick installation, select a region.</span></span> <span data-ttu-id="c1d11-164">Hvis du velger **Vet ikke** vil systemet søke alle områder, og det vil ta lengre tid å installere.</span><span class="sxs-lookup"><span data-stu-id="c1d11-164">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="c1d11-165">Skriv inn brukernavn og passord for en administratorbruker som har installasjonsrettigheter.</span><span class="sxs-lookup"><span data-stu-id="c1d11-165">Enter the user name and password of an admin user who has installation rights.</span></span>



