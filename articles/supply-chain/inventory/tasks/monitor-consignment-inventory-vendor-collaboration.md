---
title: "Overvåke forsendelseslager ved hjelp av leverandørsamarbeid"
description: "Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8e4a620fe5f5ab3c0fae8b04d79e9912111b7ece
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="31413-103">Overvåke forsendelseslager ved hjelp av leverandørsamarbeid</span><span class="sxs-lookup"><span data-stu-id="31413-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31413-104">Denne fremgangsmåten viser hvordan du bruker leverandørsamarbeid til å se informasjon om lagernivået for produktet som du har plassert i forsendelse hos en kunde.</span><span class="sxs-lookup"><span data-stu-id="31413-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="31413-105">Du kan også overvåke forbruket av lageret når kunden blir eier av lageret.</span><span class="sxs-lookup"><span data-stu-id="31413-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="31413-106">Du kan bruke prosedyren i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="31413-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="31413-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="31413-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="31413-108">Vise brukt beholdning</span><span class="sxs-lookup"><span data-stu-id="31413-108">View consumed inventory</span></span>
1. <span data-ttu-id="31413-109">Gå til Leverandørsamarbeid > Forsendelseslager > Produkter mottatt fra forsendelseslager.</span><span class="sxs-lookup"><span data-stu-id="31413-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="31413-110">Listen viser mottaksseddellinjene som ble generert da eierskap av forsendelseslageret ble endret fra leverandøren til kunden.</span><span class="sxs-lookup"><span data-stu-id="31413-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="31413-111">Du må kanskje gå til høyre for å se antall og annen informasjon.</span><span class="sxs-lookup"><span data-stu-id="31413-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="31413-112">Du kan bruke informasjonen i denne listen til å generere fakturaer for kunden.</span><span class="sxs-lookup"><span data-stu-id="31413-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="31413-113">Du kan også eksportere dataene til Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="31413-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="31413-114">Klikk Vis bestilling.</span><span class="sxs-lookup"><span data-stu-id="31413-114">Click View purchase order.</span></span>
3. <span data-ttu-id="31413-115">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="31413-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="31413-116">Linjen er merket som Forsendelse, og topptekstdelen viser at bestillingen har statusen Mottatt.</span><span class="sxs-lookup"><span data-stu-id="31413-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="31413-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="31413-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="31413-118">Vise lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="31413-118">View on-hand inventory</span></span>
1. <span data-ttu-id="31413-119">Gå til Leverandørsamarbeid > Forsendelseslager > Forsendelseslager for beholdning.</span><span class="sxs-lookup"><span data-stu-id="31413-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="31413-120">Siden Forsendelseslager for beholdning viser lageret du eier på kundens lager.</span><span class="sxs-lookup"><span data-stu-id="31413-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="31413-121">Du kan vise flere dimensjoner, for eksempel område og lager, ved å klikke kategorien Visningsdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="31413-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

