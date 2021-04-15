---
title: " Konfigurere en arbeider"
description: Denne fremgangsmåten beskriver hvordan du konfigurerer en arbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet.
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43e65de1fda223c2d0503848e7e57936898c1b73
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804071"
---
# <a name="configure-a-worker"></a><span data-ttu-id="ff4e6-103"> Konfigurere en arbeider</span><span class="sxs-lookup"><span data-stu-id="ff4e6-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff4e6-104">Denne fremgangsmåten beskriver hvordan du konfigurerer en arbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="ff4e6-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="ff4e6-106">Opprette en provisjonssalgsgruppe for arbeideren</span><span class="sxs-lookup"><span data-stu-id="ff4e6-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="ff4e6-107">Gå til Salg og markedsføring > Provisjoner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="ff4e6-108">Arbeidere kan tilordnes til én eller flere salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="ff4e6-109">På salgsstedet kan du velge enhver salgsgruppe som inneholder arbeidere fra butikkens adressebok.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="ff4e6-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-110">Click New.</span></span>
3. <span data-ttu-id="ff4e6-111">Skriv inn en verdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="ff4e6-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ff4e6-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-113">Click Save.</span></span>
6. <span data-ttu-id="ff4e6-114">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="ff4e6-115">Klikk Selger.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-115">Click Sales rep.</span></span>
    * <span data-ttu-id="ff4e6-116">En salgsgruppe kan inneholde mer enn én arbeider.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="ff4e6-117">Provisjoner kan deles mellom arbeidere basert på hvordan du definerer provisjonsandelen.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="ff4e6-118">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="ff4e6-119">Angi et tall i feltet Provisjonsandel.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="ff4e6-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-120">Click Save.</span></span>
11. <span data-ttu-id="ff4e6-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-121">Close the page.</span></span>
12. <span data-ttu-id="ff4e6-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="ff4e6-123">Tilordne standard salgsgruppe til arbeiderne</span><span class="sxs-lookup"><span data-stu-id="ff4e6-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="ff4e6-124">Gå til Retail og Commerce > Ansatte > Arbeidere.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="ff4e6-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ff4e6-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ff4e6-127">Klikk kategorien Commerce.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="ff4e6-128">En arbeider kan tilordnes til en standard salgsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="ff4e6-129">Standard salgsgruppe legges automatisk til salgslinjer i salgsstedet hvis alternativet er aktivert i funksjonalitetsprofilen for butikken.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="ff4e6-130">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-130">Click Edit.</span></span>
6. <span data-ttu-id="ff4e6-131">Angi eller velg en verdi i Standardgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="ff4e6-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ff4e6-132">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]