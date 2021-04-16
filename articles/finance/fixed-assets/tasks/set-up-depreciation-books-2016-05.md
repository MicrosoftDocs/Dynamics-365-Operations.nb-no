---
title: Definere avskrivningstablåer
description: Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815602"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="161f7-103">Definere avskrivningstablåer</span><span class="sxs-lookup"><span data-stu-id="161f7-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="161f7-104">Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="161f7-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="161f7-105">Opprette et avskrivningstablå</span><span class="sxs-lookup"><span data-stu-id="161f7-105">Create a depreciation book</span></span>
1. <span data-ttu-id="161f7-106">Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="161f7-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="161f7-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="161f7-107">Click New.</span></span>
3. <span data-ttu-id="161f7-108">Skriv inn en verdi i feltet Avskrivningstablå.</span><span class="sxs-lookup"><span data-stu-id="161f7-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="161f7-109">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="161f7-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="161f7-110">Merk av eller fjern merket i boksen Beregn avskrivning.</span><span class="sxs-lookup"><span data-stu-id="161f7-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="161f7-111">Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="161f7-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="161f7-112">Finn og velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="161f7-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="161f7-114">Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="161f7-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="161f7-115">Velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="161f7-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="161f7-117">Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="161f7-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="161f7-118">Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="161f7-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="161f7-119">Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="161f7-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="161f7-120">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="161f7-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="161f7-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="161f7-122">Knytte avskrivningstablået til en anleggsmiddelgruppe</span><span class="sxs-lookup"><span data-stu-id="161f7-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="161f7-123">Klikk Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="161f7-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="161f7-124">Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="161f7-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="161f7-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="161f7-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="161f7-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="161f7-127">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="161f7-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="161f7-128">Angi et tall i Levetid-feltet.</span><span class="sxs-lookup"><span data-stu-id="161f7-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="161f7-129">Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="161f7-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]