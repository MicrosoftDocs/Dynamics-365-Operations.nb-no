---
title: " Konfigurere en arbeider"
description: Denne fremgangsmåten beskriver hvordan du konfigurerer en arbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 120705200f223e31c72290059e8634e7db6f9fdd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232623"
---
# <a name="configure-a-worker"></a><span data-ttu-id="836cc-103"> Konfigurere en arbeider</span><span class="sxs-lookup"><span data-stu-id="836cc-103">Configure a worker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="836cc-104">Denne fremgangsmåten beskriver hvordan du konfigurerer en arbeider som en selger som er kvalifisert for provisjon på salg i salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="836cc-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="836cc-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="836cc-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="836cc-106">Opprette en provisjonssalgsgruppe for arbeideren</span><span class="sxs-lookup"><span data-stu-id="836cc-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="836cc-107">Gå til Salg og markedsføring > Provisjoner > Salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="836cc-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="836cc-108">Arbeidere kan tilordnes til én eller flere salgsgrupper.</span><span class="sxs-lookup"><span data-stu-id="836cc-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="836cc-109">På salgsstedet kan du velge enhver salgsgruppe som inneholder arbeidere fra butikkens adressebok.</span><span class="sxs-lookup"><span data-stu-id="836cc-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="836cc-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="836cc-110">Click New.</span></span>
3. <span data-ttu-id="836cc-111">Skriv inn en verdi i feltet Gruppe.</span><span class="sxs-lookup"><span data-stu-id="836cc-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="836cc-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="836cc-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="836cc-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="836cc-113">Click Save.</span></span>
6. <span data-ttu-id="836cc-114">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="836cc-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="836cc-115">Klikk Selger.</span><span class="sxs-lookup"><span data-stu-id="836cc-115">Click Sales rep.</span></span>
    * <span data-ttu-id="836cc-116">En salgsgruppe kan inneholde mer enn én arbeider.</span><span class="sxs-lookup"><span data-stu-id="836cc-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="836cc-117">Provisjoner kan deles mellom arbeidere basert på hvordan du definerer provisjonsandelen.</span><span class="sxs-lookup"><span data-stu-id="836cc-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="836cc-118">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="836cc-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="836cc-119">Angi et tall i feltet Provisjonsandel.</span><span class="sxs-lookup"><span data-stu-id="836cc-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="836cc-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="836cc-120">Click Save.</span></span>
11. <span data-ttu-id="836cc-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="836cc-121">Close the page.</span></span>
12. <span data-ttu-id="836cc-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="836cc-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="836cc-123">Tilordne standard salgsgruppe til arbeiderne</span><span class="sxs-lookup"><span data-stu-id="836cc-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="836cc-124">Gå til Retail og Commerce > Ansatte > Arbeidere.</span><span class="sxs-lookup"><span data-stu-id="836cc-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="836cc-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="836cc-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="836cc-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="836cc-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="836cc-127">Klikk kategorien Commerce.</span><span class="sxs-lookup"><span data-stu-id="836cc-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="836cc-128">En arbeider kan tilordnes til en standard salgsgruppe.</span><span class="sxs-lookup"><span data-stu-id="836cc-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="836cc-129">Standard salgsgruppe legges automatisk til salgslinjer i salgsstedet hvis alternativet er aktivert i funksjonalitetsprofilen for butikken.</span><span class="sxs-lookup"><span data-stu-id="836cc-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="836cc-130">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="836cc-130">Click Edit.</span></span>
6. <span data-ttu-id="836cc-131">Angi eller velg en verdi i Standardgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="836cc-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="836cc-132">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="836cc-132">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]