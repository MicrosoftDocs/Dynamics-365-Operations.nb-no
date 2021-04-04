---
title: Kundeemne til kontanter
description: Dette emnet gir en oversikt over Kundeemne til kontanter-løsningen mellom Dynamics 365 Supply Chain Management og Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 70ea2638408296df283a030dedce03b22cb57d81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248745"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="650b3-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="650b3-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="650b3-104">Kundeemne til kontanter-løsningen gir direkte synkronisering på tvers av Dynamics 365 Supply Chain Management og Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="650b3-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="650b3-105">Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="650b3-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="650b3-106">Når dataene flyter, kan du utføre salgs- og markedsaktiviteter i Sales, og du kan håndtere ordrenes oppfyllelse med lagerstyring i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="650b3-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="650b3-107">Hvis du vil ha mer informasjon om Kundeemne til kontanter-integrasjonen, se den korte YouTube-videoen [Kundeemne til kontanter-integrasjon](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="650b3-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="650b3-108">I den gjeldende versjonen inneholder Kundeemne til kontanter-løsningen følgende typer direkte synkronisering:</span><span class="sxs-lookup"><span data-stu-id="650b3-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="650b3-109">Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="650b3-109">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="650b3-110">Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="650b3-110">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="650b3-111">Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="650b3-111">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="650b3-112">Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="650b3-112">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="650b3-113">Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="650b3-113">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="650b3-114">Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="650b3-114">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="650b3-115">Systemkrav for Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="650b3-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="650b3-116">Kundeemne til kontanter-integrasjon støttes i følgende versjoner:</span><span class="sxs-lookup"><span data-stu-id="650b3-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="650b3-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (desember 2017)</span><span class="sxs-lookup"><span data-stu-id="650b3-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="650b3-118">Dynamics 365 for Finance and Operations Enterprise Edition (desember 2017) – programbygg 7.3.11971.56116 med plattformoppdatering 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="650b3-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="650b3-119">Dynamics 365 for Finance and Operations Enterprise Edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="650b3-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="650b3-120">Dynamics 365 for Finance and Operations Enterprise Edition (juli 2017) – med plattformoppdatering 8 (programbygg 7.2.11792.56024 med plattformbygg 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="650b3-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="650b3-121">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="650b3-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="650b3-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="650b3-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="650b3-123">I tillegg inneholder den flere forbedringer.</span><span class="sxs-lookup"><span data-stu-id="650b3-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="650b3-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordrelinje via dataintegreringsfunksjonen fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="650b3-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="650b3-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre via dataintegreringsfunksjonen fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="650b3-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="650b3-126">Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre hurtigreparasjonene.</span><span class="sxs-lookup"><span data-stu-id="650b3-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="650b3-127">Dynamics 365 for Finance and Operations versjon 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="650b3-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="650b3-128">Dynamics 365 for Finance and Operations versjon 1611 (november 2016) med plattformoppdatering 8 eller høyere</span><span class="sxs-lookup"><span data-stu-id="650b3-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="650b3-129">Følgende hurtigreparasjoner vil kreves:</span><span class="sxs-lookup"><span data-stu-id="650b3-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="650b3-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – Aktiver salgsordresynkronisering med dataintegrator fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="650b3-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="650b3-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – Aktiver salgsordrehode- og linjesynkronisering med dataintegrator fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="650b3-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="650b3-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Støtte for kundeemne til kontanter-integrering gjennom dataenheter, kreves.</span><span class="sxs-lookup"><span data-stu-id="650b3-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="650b3-133">Når du har installert hurtigreparasjonene, må du starte den følgende kjørselen fra skjemaet **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="650b3-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="650b3-134">Dette skjemaet skjules siden du bare trenger det én gang.</span><span class="sxs-lookup"><span data-stu-id="650b3-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="650b3-135">For å få tilgang til skjemaet, må du logge på miljøet og legge til følgende i URL-adressen i nettleseradressen: *&mi=action:SalesPopulateProspectToCash*, for eksempel `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="650b3-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="650b3-136">Når skjemaet åpnes, klikker du på OK.</span><span class="sxs-lookup"><span data-stu-id="650b3-136">When the form opens, click OK.</span></span> <span data-ttu-id="650b3-137">Dette vil fylle ut et nytt felt **LineCreationSequnceNumber** i tabellen **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** med unike verdier og oppdatere varelisten.</span><span class="sxs-lookup"><span data-stu-id="650b3-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="650b3-138">Dette er nødvendig for at kundeemne til kontanter-integrasjonen skal fungere.</span><span class="sxs-lookup"><span data-stu-id="650b3-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="650b3-139">Systemkrav for Sales</span><span class="sxs-lookup"><span data-stu-id="650b3-139">System requirements for Sales</span></span>

<span data-ttu-id="650b3-140">For å bruke Kundeemne til kontanter-løsningen må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="650b3-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="650b3-141">Dynamics 365 Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="650b3-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="650b3-142">Kundeemne til kontanter-løsning for Dynamics 365 Sales versjon 1.15.0.0 eller en nyere versjon.</span><span class="sxs-lookup"><span data-stu-id="650b3-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="650b3-143">Løsningen er tilgjengelig for nedlasting fra AppSource.</span><span class="sxs-lookup"><span data-stu-id="650b3-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="650b3-144">[Last ned Dynamics 365, kundeemne til kontanter](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="650b3-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]