---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b783d1ce8f02ad119dc6768e6d9cd3c61ae07e70
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566439"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="0ef8b-103">Godkjenne leverandører for spesifikke innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="0ef8b-103">Approve vendors for specific procurement categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ef8b-104">Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-104">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="0ef8b-105">Denne fremgangsmåten viser hvordan du angir at en leverandør er godkjent eller foretrukket for en spesifikk innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-105">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="0ef8b-106">Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-106">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="0ef8b-107">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-107">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="0ef8b-108">Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-108">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="0ef8b-109">Velg leverandøren du vil angi som en godkjent eller foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-109">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="0ef8b-110">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-110">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="0ef8b-111">Klikk Kategorier.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-111">Click Categories.</span></span>
5. <span data-ttu-id="0ef8b-112">Klikk Legg til kategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-112">Click Add category.</span></span>
6. <span data-ttu-id="0ef8b-113">I Kategori-feltet velger du KONTOR- OG SKRIVEBORDSTILBEHØR (KONTOR- OG SKRIVEBORDSTILBEHØR).</span><span class="sxs-lookup"><span data-stu-id="0ef8b-113">In the Category field, select OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES).</span></span>
7. <span data-ttu-id="0ef8b-114">I feltet Status for leverandørkategori velger du Foretrukket.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-114">In the Vendor category status field, select 'Preferred'.</span></span>
    * <span data-ttu-id="0ef8b-115">Det er mulig å angi flere enn én foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-115">It’s possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="0ef8b-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-116">Click Save.</span></span>
9. <span data-ttu-id="0ef8b-117">Gå til Innkjøp og leverandører > Innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-117">Go to Procurement and sourcing > Procurement categories.</span></span>
10. <span data-ttu-id="0ef8b-118">Velg FIRMAINNKJØPSKATEGORIER\KONTOR- OG SKRIVEBORDSTILBEHØR i treet.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-118">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES'.</span></span>
11. <span data-ttu-id="0ef8b-119">Vis Leverandør-delen.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-119">Expand the Vendors section.</span></span>
    * <span data-ttu-id="0ef8b-120">Kontroller om leverandøren du har valgt, vises som en foretrukket leverandør for kategorien Kontor- og skrivebordtilbehør.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-120">Check if the vendor that you selected  appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="0ef8b-121">Hvis du kjører denne fremgangsmåten som en oppgaveveiledning, må du kanskje klikka Lås opp for å kunne bla gjennom listen over leverandører.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-121">If you’re running this procedure as a task guide, you may have to click the Unlock button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="0ef8b-122">Det er også mulig å legge til foretrukne og godkjente leverandører på denne siden.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-122">It’s also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="0ef8b-123">Vis KONTOR- OG SKRIVEBORDSTILBEHØR i treet.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-123">In the tree, expand 'OFFICE AND DESK ACCESSORIES'.</span></span>
13. <span data-ttu-id="0ef8b-124">Velg Sakser i treet .</span><span class="sxs-lookup"><span data-stu-id="0ef8b-124">In the tree, select 'Scissors'.</span></span>
14. <span data-ttu-id="0ef8b-125">Velg Nei i feltet Arv leverandører fra overordnet kategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-125">Select No in the Inherit vendors from parent category: field.</span></span>
15. <span data-ttu-id="0ef8b-126">Velg Ja i feltet Arv leverandører fra overordnet kategori.</span><span class="sxs-lookup"><span data-stu-id="0ef8b-126">Select Yes in the Inherit vendors from parent category: field.</span></span>

