---
title: Kundeemne til kontanter
description: Emnet gir en oversikt over Kundeemne til kontanter mellom Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e9cb3-103">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="e9cb3-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9cb3-104">Kundeemne til kontanter-løsningen bruker [Dataintegrasjon](/common-data-service/entity-reference/dynamics-365-integration) for å synkronisere data på tvers av Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="e9cb3-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="e9cb3-105">Kundeemne til kontanter-maler som er tilgjengelige med dataintegrasjon-funksjonen, gjør det mulig å flytte kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="e9cb3-106">Når dataene flyter mellom Finance and Operations og Sales kan du utføre salgs- og markedsaktiviteter i Sales og håndtere ordrenes oppfyllelse med lagerstyring i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="e9cb3-107">Denne løsningen gir integrasjon i følgende områder:</span><span class="sxs-lookup"><span data-stu-id="e9cb3-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="e9cb3-108">Behold kontoer i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9cb3-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="e9cb3-109">Behold kontakter i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9cb3-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="e9cb3-110">Behold produkter i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9cb3-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="e9cb3-111">Opprett salgstilbud i Sales og synkroniser dem til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9cb3-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="e9cb3-112">Opprett salgsordrer i Finance and Operations og synkroniser dem til Sales</span><span class="sxs-lookup"><span data-stu-id="e9cb3-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="e9cb3-113">Opprett salgsfakturaer i Finance and Operations og synkroniser dem til Sales</span><span class="sxs-lookup"><span data-stu-id="e9cb3-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="e9cb3-114">Systemkrav for Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="e9cb3-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="e9cb3-115">For å bruke Kundeemne til kontanter-løsningen må du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="e9cb3-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e9cb3-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) med plattformoppdatering 8 (App 7.2.11792.56024 m/ Platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="e9cb3-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="e9cb3-117">To hurtigreparasjoner for Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="e9cb3-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="e9cb3-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordreline med dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="e9cb3-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – Denne hurtigreparasjonen gjør det mulig å synkronisere salgsordre med dataintegreringsfunksjonen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="e9cb3-120">**Merk**: Du trenger bare å installere KB4036524 fordi installasjonen inkluderer endringene fra KB4036461.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="e9cb3-121">Systemkrav for Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="e9cb3-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="e9cb3-122">For å bruke Kundeemne til kontanter-løsningen må du installere følgende:</span><span class="sxs-lookup"><span data-stu-id="e9cb3-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e9cb3-123">Dynamics 365 for Sales versjon 1612 (8.2.1.207) (DB 8.2.1.207) nett eller senere.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="e9cb3-124">Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e9cb3-125">Installere Kundeemne til kontanter-løsningen for Sales</span><span class="sxs-lookup"><span data-stu-id="e9cb3-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="e9cb3-126">Last ned [Kundeemne til kontanter for Dynamics 365 for Sales, løsningspakke zip-fil](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) på CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="e9cb3-127">Sørge for at zip-filen ikke er blokkert, så du ikke får feilmeldingen «No import packages were found», når du installer løsningspakken.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="e9cb3-128">Gjør følgende for å sørge for at filen ikke er blokkert:</span><span class="sxs-lookup"><span data-stu-id="e9cb3-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="e9cb3-129">Høyreklikk zip-filen.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="e9cb3-130">Velg **Egenskaper** og velg deretter **Opphev blokkering**.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="e9cb3-131">Pakk ut og kjøre PackageDeployer.exe</span><span class="sxs-lookup"><span data-stu-id="e9cb3-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="e9cb3-132">Installer Kundeemne til kontanter-løsningen for forekomsten din av Sales.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="e9cb3-133">Velg **Office 365** Implementasjonstype</span><span class="sxs-lookup"><span data-stu-id="e9cb3-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="e9cb3-134">Velg **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="e9cb3-135">For en hurtiginstallasjon, velg en **Region**.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="e9cb3-136">Hvis du velger **Vet ikke** vil systemet søke alle regioner, og det vil ta lengre tid å installere.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="e9cb3-137">Skriv inn **Brukernavn** og **Passord** for en administratorbruker som har brukerrettigheter til å installere.</span><span class="sxs-lookup"><span data-stu-id="e9cb3-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

