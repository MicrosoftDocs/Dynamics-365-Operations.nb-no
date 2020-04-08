---
title: Definere avskrivningstablåer
description: Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154609"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="525a9-103">Definere avskrivningstablåer</span><span class="sxs-lookup"><span data-stu-id="525a9-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="525a9-104">Denne fremgangsmåten går gjennom prosessen med å opprette et nytt avskrivningstablå og knytte det til en anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="525a9-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="525a9-105">Opprette et avskrivningstablå</span><span class="sxs-lookup"><span data-stu-id="525a9-105">Create a depreciation book</span></span>
1. <span data-ttu-id="525a9-106">Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="525a9-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="525a9-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="525a9-107">Click New.</span></span>
3. <span data-ttu-id="525a9-108">Skriv inn en verdi i feltet Avskrivningstablå.</span><span class="sxs-lookup"><span data-stu-id="525a9-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="525a9-109">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="525a9-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="525a9-110">Merk av eller fjern merket i boksen Beregn avskrivning.</span><span class="sxs-lookup"><span data-stu-id="525a9-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="525a9-111">Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="525a9-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="525a9-112">Finn og velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="525a9-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="525a9-114">Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="525a9-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="525a9-115">Velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="525a9-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="525a9-117">Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="525a9-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="525a9-118">Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="525a9-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="525a9-119">Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="525a9-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="525a9-120">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="525a9-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="525a9-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="525a9-122">Knytte avskrivningstablået til en anleggsmiddelgruppe</span><span class="sxs-lookup"><span data-stu-id="525a9-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="525a9-123">Klikk Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="525a9-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="525a9-124">Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="525a9-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="525a9-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="525a9-126">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="525a9-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="525a9-127">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="525a9-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="525a9-128">Angi et tall i Levetid-feltet.</span><span class="sxs-lookup"><span data-stu-id="525a9-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="525a9-129">Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="525a9-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

