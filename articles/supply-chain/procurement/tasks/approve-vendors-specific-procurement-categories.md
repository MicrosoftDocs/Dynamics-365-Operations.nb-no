---
title: Godkjenne leverandører for spesifikke innkjøpskategorier
description: Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 887905c35c684f2f60c3ce17eb652532831193cc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812452"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="fc07b-103">Godkjenne leverandører for spesifikke innkjøpskategorier</span><span class="sxs-lookup"><span data-stu-id="fc07b-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc07b-104">Dette emnet forklarer hvordan du godkjenner leverandører for bestemte innkjøpskategorier i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fc07b-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fc07b-105">Når det opprettes en innkjøpsrekvisisjon, kan det være et krav om å velge en godkjent eller foretrukket leverandør, avhengig av hvordan innkjøpspolicyene er definert.</span><span class="sxs-lookup"><span data-stu-id="fc07b-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="fc07b-106">Denne fremgangsmåten viser hvordan du angir at en leverandør er godkjent eller foretrukket for en spesifikk innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="fc07b-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="fc07b-107">Denne oppgaven vil vanligvis utføres av en innkjøpsansvarlig.</span><span class="sxs-lookup"><span data-stu-id="fc07b-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="fc07b-108">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="fc07b-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="fc07b-109">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="fc07b-110">Velg leverandøren du vil angi som en godkjent eller foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="fc07b-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="fc07b-111">Klikk på **Generelt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="fc07b-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="fc07b-112">Velg **Kategorier**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-112">Select **Categories**.</span></span>
5. <span data-ttu-id="fc07b-113">Velg **Legg til kategori**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-113">Select **Add category**.</span></span>
6. <span data-ttu-id="fc07b-114">I **Kategori**-feltet velger du **KONTOR- OG SKRIVEBORDSTILBEHØR (KONTOR- OG SKRIVEBORDSTILBEHØR)**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="fc07b-115">I feltet **Status for leverandørkategori** velger du **Foretrukket**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="fc07b-116">Det er mulig å angi flere enn én foretrukket leverandør for en kategori.</span><span class="sxs-lookup"><span data-stu-id="fc07b-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="fc07b-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-117">Select **Save**.</span></span>
9. <span data-ttu-id="fc07b-118">I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Innkjøpskategorier**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="fc07b-119">Velg **FIRMAINNKJØPSKATEGORIER\KONTOR- OG SKRIVEBORDSTILBEHØR i treet**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="fc07b-120">Vis **Leverandør**-delen.</span><span class="sxs-lookup"><span data-stu-id="fc07b-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="fc07b-121">Kontroller om leverandøren du har valgt, vises som en foretrukket leverandør for kategorien Kontor- og skrivebordtilbehør.</span><span class="sxs-lookup"><span data-stu-id="fc07b-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="fc07b-122">Hvis du kjører denne fremgangsmåten som en oppgaveveiledning, må du kanskje klikke **Lås opp** for å kunne bla gjennom listen over leverandører.</span><span class="sxs-lookup"><span data-stu-id="fc07b-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="fc07b-123">Det er også mulig å legge til foretrukne og godkjente leverandører på denne siden.</span><span class="sxs-lookup"><span data-stu-id="fc07b-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="fc07b-124">Vis **KONTOR- OG SKRIVEBORDSTILBEHØR** i treet, og velg **Saks**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="fc07b-125">Velg **Nei** i feltet **Arv leverandører fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="fc07b-126">Velg **Ja** i feltet **Arv leverandører fra overordnet kategori**.</span><span class="sxs-lookup"><span data-stu-id="fc07b-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]