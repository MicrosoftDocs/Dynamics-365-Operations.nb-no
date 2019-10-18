---
title: Definere avskrivningstablå (mai 2016)
description: Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe.
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
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186906"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="cb0a2-103">Definere avskrivningstablå (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="cb0a2-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb0a2-104">Denne oppgaveveiledningen oppretter et nytt avskrivningstablå og knytter den til en anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="cb0a2-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="cb0a2-106">Opprette et avskrivningstablå</span><span class="sxs-lookup"><span data-stu-id="cb0a2-106">Create a depreciation book</span></span>
1. <span data-ttu-id="cb0a2-107">Gå til Anleggsmidler > Oppsett > Avskrivningstablåer.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="cb0a2-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-108">Click New.</span></span>
3. <span data-ttu-id="cb0a2-109">Skriv inn en verdi i feltet Avskrivningstablå.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="cb0a2-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cb0a2-111">Merk av eller fjern merket i boksen Beregn avskrivning.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="cb0a2-112">Klikk rullegardinknappen i feltet Avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cb0a2-113">Finn og velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="cb0a2-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cb0a2-115">Klikk rullegardinknappen i feltet Alternativ avskrivningsprofil for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="cb0a2-116">Velg ønsket avskrivningsprofil i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="cb0a2-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cb0a2-118">Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="cb0a2-119">Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="cb0a2-120">Merk av eller fjern merket i boksen Opprett avskrivningsjusteringer med basisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="cb0a2-121">Klikk rullegardinknappen i Kalender-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="cb0a2-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="cb0a2-123">Knytte avskrivningstablået til en anleggsmiddelgruppe</span><span class="sxs-lookup"><span data-stu-id="cb0a2-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="cb0a2-124">Klikk Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="cb0a2-125">Klikk rullegardinknappen i feltet Anleggsmiddelgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cb0a2-126">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cb0a2-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cb0a2-128">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="cb0a2-129">Angi et tall i Levetid-feltet.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="cb0a2-130">Legg merke til at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="cb0a2-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

