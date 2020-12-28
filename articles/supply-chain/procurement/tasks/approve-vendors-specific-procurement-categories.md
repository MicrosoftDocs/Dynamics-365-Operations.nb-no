---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.
author: mkirknel
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e53102d732e9befcaca183adfd2a756c12e0162b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434353"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="30554-103">Godkjenne leverandører for spesifikke innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="30554-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30554-104">Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="30554-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="30554-105">Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert.</span><span class="sxs-lookup"><span data-stu-id="30554-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="30554-106">Denne fremgangsmåten viser hvordan du angir at en leverandør er godkjent eller foretrukket for en spesifikk innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="30554-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="30554-107">Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="30554-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="30554-108">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="30554-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="30554-109">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="30554-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="30554-110">Velg leverandøren du vil angi som en godkjent eller foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="30554-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="30554-111">Klikk på **Generelt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="30554-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="30554-112">Velg **Kategorier**.</span><span class="sxs-lookup"><span data-stu-id="30554-112">Select **Categories**.</span></span>
5. <span data-ttu-id="30554-113">Velg **Legg til kategori**.</span><span class="sxs-lookup"><span data-stu-id="30554-113">Select **Add category**.</span></span>
6. <span data-ttu-id="30554-114">I **Kategori**-feltet velger du **KONTOR- OG SKRIVEBORDSTILBEHØR (KONTOR- OG SKRIVEBORDSTILBEHØR)**.</span><span class="sxs-lookup"><span data-stu-id="30554-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="30554-115">I feltet **Status for leverandørkategori** velger du **Foretrukket**.</span><span class="sxs-lookup"><span data-stu-id="30554-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="30554-116">Det er mulig å angi flere enn én foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="30554-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="30554-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="30554-117">Select **Save**.</span></span>
9. <span data-ttu-id="30554-118">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpskategorier**.</span><span class="sxs-lookup"><span data-stu-id="30554-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="30554-119">Velg **FIRMAINNKJØPSKATEGORIER\KONTOR- OG SKRIVEBORDSTILBEHØR i treet**.</span><span class="sxs-lookup"><span data-stu-id="30554-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="30554-120">Vis **Leverandør**-delen.</span><span class="sxs-lookup"><span data-stu-id="30554-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="30554-121">Kontroller om leverandøren du har valgt, vises som en foretrukket leverandør for kategorien Kontor- og skrivebordtilbehør.</span><span class="sxs-lookup"><span data-stu-id="30554-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="30554-122">Hvis du kjører denne fremgangsmåten som en oppgaveveiledning, må du kanskje klikke **Lås opp** for å kunne bla gjennom listen over leverandører.</span><span class="sxs-lookup"><span data-stu-id="30554-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="30554-123">Det er også mulig å legge til foretrukne og godkjente leverandører på denne siden.</span><span class="sxs-lookup"><span data-stu-id="30554-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="30554-124">Vis **KONTOR- OG SKRIVEBORDSTILBEHØR** i treet, og velg **Saks**.</span><span class="sxs-lookup"><span data-stu-id="30554-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="30554-125">Velg **Nei** i feltet **Arv leverandører fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="30554-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="30554-126">Velg **Ja** i feltet **Arv leverandører fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="30554-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

