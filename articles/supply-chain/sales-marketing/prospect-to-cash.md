---
title: Kundeemne til kontanter
description: Emnet gir en oversikt over Kundeemne til kontanter mellom Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: nb-no
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="ddb2a-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="ddb2a-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ddb2a-104">Kundeemne til kontanter-løsningen bruker [Dataintegrasjon](/common-data-service/entity-reference/dynamics-365-integration) for å synkronisere data på tvers av Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="ddb2a-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="ddb2a-105">Kundeemne til kontanter-maler som er tilgjengelige med dataintegrasjon-funksjonen, gjør det mulig å flytte kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="ddb2a-106">Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales og håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="ddb2a-107">Denne løsningen gir integrasjon i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="ddb2a-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="ddb2a-108">Behold kontoer i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="ddb2a-109">Behold kontakter i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="ddb2a-110">Behold produkter i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="ddb2a-111">Opprett salgstilbud i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="ddb2a-112">Opprett salgsordrer i Finance and Operations og synkroniser dem til Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="ddb2a-113">Opprett salgsfakturaer i Finance and Operations og synkroniser dem til Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="ddb2a-114">Denne løsningen gir direkte synkronisering i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="ddb2a-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="ddb2a-115">Beholde kontoer i Sales og synkroniser dem direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="ddb2a-116">Beholde produkter i Finance and Operations og synkroniser dem til direkte til Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="ddb2a-117">Beholde kontakter i Sales og synkroniser dem direkte til kontakter eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="ddb2a-118">Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="ddb2a-119">Opprette salgsordrer i Finance and Operations og synkroniser dem direkte til Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="ddb2a-120">Synkronisere salgsordrehoder og -linjer direkte mellom Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="ddb2a-121">Synkronisere salgsordrer direkte mellom Sales og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ddb2a-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="ddb2a-122">Opprette salgsfakturaer i Finance and Operations og synkroniser dem direkte til Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="ddb2a-123">Systemkrav for Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="ddb2a-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="ddb2a-124">For å bruke Kundeemne til kontanter-løsningen må du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="ddb2a-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="ddb2a-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med plattformoppdatering 8 (App 7.2.11792.56024 m/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="ddb2a-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="ddb2a-126">Hurtigreparasjoner for Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="ddb2a-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="ddb2a-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre med dataintegreringsfunksjonen fra Sales til Finance and Operations, sammen med en rekke andre forbedringer.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="ddb2a-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordreline med dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="ddb2a-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre med dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="ddb2a-130">**Obs!** Du trenger bare å installere KB4045570 fordi installasjonen inkluderer endringene fra de andre KB-ene.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="ddb2a-131">Systemkrav for Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="ddb2a-132">For å bruke Kundeemne til kontanter-løsningen må du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="ddb2a-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="ddb2a-133">Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) online.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="ddb2a-134">Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ddb2a-135">Installere Kundeemne til kontanter-løsningen for Sales</span><span class="sxs-lookup"><span data-stu-id="ddb2a-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="ddb2a-136">Last ned [Kundeemne til kontanter for Dynamics 365 for Sales, løsningspakke zip-fil](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="ddb2a-137">Sørge for at zip-filen ikke er blokkert, så du ikke får feilmeldingen «No import packages were found», når du installer løsningspakken.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="ddb2a-138">Gjør følgende for å sørge for at filen ikke er blokkert:</span><span class="sxs-lookup"><span data-stu-id="ddb2a-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="ddb2a-139">Høyreklikk zip-filen.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="ddb2a-140">Velg **Egenskaper** og velg deretter **Opphev blokkering**.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="ddb2a-141">Pakk ut og kjøre PackageDeployer.exe</span><span class="sxs-lookup"><span data-stu-id="ddb2a-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="ddb2a-142">Installer Kundeemne til kontanter-løsningen for forekomsten din av Sales.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="ddb2a-143">Velg **Office 365** Implementasjonstype</span><span class="sxs-lookup"><span data-stu-id="ddb2a-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="ddb2a-144">Velg **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="ddb2a-145">For en hurtiginstallasjon, velg en **Region**.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="ddb2a-146">Hvis du velger **Vet ikke** vil systemet søke alle regioner, og det vil ta lengre tid å installere.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="ddb2a-147">Skriv inn **Brukernavn** og **Passord** for en administratorbruker som har brukerrettigheter til å installere.</span><span class="sxs-lookup"><span data-stu-id="ddb2a-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

