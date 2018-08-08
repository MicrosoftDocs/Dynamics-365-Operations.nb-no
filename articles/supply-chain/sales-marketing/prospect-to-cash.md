---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 801407183ad90f08bde928a1d3da13cba38cfc27
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="8b72a-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="8b72a-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b72a-104">Løsningen Kundeemne til kontanter gir direkte synkronisering på tvers av Dynamics 365 for Finance and Operations og Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="8b72a-105">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8b72a-106">Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b72a-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="8b72a-107">Hvis du vil ha mer informasjon om Prospekt til kontanter-integrasjon, se den korte YouTube-videoen: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span><span class="sxs-lookup"><span data-stu-id="8b72a-107">For more information about the Prospect to cash integration, watch the short YouTube video: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span></span>


<span data-ttu-id="8b72a-108">I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:</span><span class="sxs-lookup"><span data-stu-id="8b72a-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="8b72a-109">Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b72a-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="8b72a-110">Beholde produkter i Finance and Operations og synkronisere dem til direkte til Sales</span><span class="sxs-lookup"><span data-stu-id="8b72a-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="8b72a-111">Beholde kontakter i Sales og synkronisere dem direkte til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b72a-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="8b72a-112">Synkronisere salgstilbud direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b72a-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="8b72a-113">Synkronisere salgsordrer direkte mellom Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b72a-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="8b72a-114">Synkronisere salgsfaktura direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="8b72a-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8b72a-115">Systemkrav for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b72a-115">System requirements for Finance and Operations</span></span>
<span data-ttu-id="8b72a-116">Kundeemne til kontanter-integrasjon støttes i følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="8b72a-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="8b72a-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (desember 2017)</span><span class="sxs-lookup"><span data-stu-id="8b72a-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="8b72a-118">Dynamics 365 for Finance and Operations, Enterprise edition (desember 2017) - programbygg 7.3.11971.56116 med plattformoppdatering 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="8b72a-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="8b72a-119">Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="8b72a-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="8b72a-120">Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) – plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="8b72a-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="8b72a-121">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="8b72a-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8b72a-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8b72a-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="8b72a-123">I tillegg inneholder den flere forbedringer.</span><span class="sxs-lookup"><span data-stu-id="8b72a-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="8b72a-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinjer via dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="8b72a-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b72a-126">Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre hurtigreparasjonene.</span><span class="sxs-lookup"><span data-stu-id="8b72a-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="8b72a-127">Dynamics 365 for Finance and Operations versjon 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="8b72a-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="8b72a-128">Dynamics 365 for Finance and Operations versjon 1611 (november 2016) med plattformoppdatering 8 eller høyere</span><span class="sxs-lookup"><span data-stu-id="8b72a-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="8b72a-129">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="8b72a-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8b72a-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Aktiver salgsordresynkronisering med dataintegrator fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="8b72a-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Aktiver salgsordrehode- og linjesynkronisering med dataintegrator fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="8b72a-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="8b72a-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves.</span><span class="sxs-lookup"><span data-stu-id="8b72a-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8b72a-133">Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="8b72a-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="8b72a-134">Dette skjemaet skjules siden du bare trenger det én gang.</span><span class="sxs-lookup"><span data-stu-id="8b72a-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="8b72a-135">For å få tilgang til skjemaet, må du logge på miljøet og legge til følgende i URL-adressen i nettleseradressen: *&mi=action:SalesPopulateProspectToCash*, for eksempel `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="8b72a-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="8b72a-136">Når skjemaet åpnes, klikker du på OK.</span><span class="sxs-lookup"><span data-stu-id="8b72a-136">When the form opens, click OK.</span></span> <span data-ttu-id="8b72a-137">Dette vil fylle ut et nytt felt **LineCreationSequnceNumber** i tabellen **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med unike verdier og oppdatere varelisten.</span><span class="sxs-lookup"><span data-stu-id="8b72a-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="8b72a-138">Dette er nødvendig for at kundeemne til kontanter-integrasjonen skal fungere.</span><span class="sxs-lookup"><span data-stu-id="8b72a-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="8b72a-139">Systemkrav for Sales</span><span class="sxs-lookup"><span data-stu-id="8b72a-139">System requirements for Sales</span></span>

<span data-ttu-id="8b72a-140">For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="8b72a-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="8b72a-141">Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) nett eller en senere versjon.</span><span class="sxs-lookup"><span data-stu-id="8b72a-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="8b72a-142">Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.15.0.0 eller en senere versjon.</span><span class="sxs-lookup"><span data-stu-id="8b72a-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="8b72a-143">Løsningen er tilgjengelig for nedlasting fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="8b72a-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="8b72a-144">[Last ned Dynamics 365, kundeemne til kontanter](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="8b72a-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>

