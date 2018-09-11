--- 
title: "Opprette en postmal for å forenkle dataregistrering"
description: "Denne fremgangsmåten beskriver hvordan du oppretter en postmal slik at verdiene som brukes ofte, ikke trenger å angis eksplisitt for hver nye post."
author: margoc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: d64f32de2fb90397a72d938b937bd1f90e675287
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="b9784-103">Opprette en postmal for å forenkle dataregistrering</span><span class="sxs-lookup"><span data-stu-id="b9784-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9784-104">Denne fremgangsmåten beskriver hvordan du oppretter en postmal slik at verdiene som brukes ofte, ikke trenger å angis eksplisitt for hver nye post.</span><span class="sxs-lookup"><span data-stu-id="b9784-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="b9784-105">I denne prosedyren skal du opprette en ny post for nye bærbare datamaskiner som skal legges til anleggsmidlene.</span><span class="sxs-lookup"><span data-stu-id="b9784-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="b9784-106">Denne prosedyren bruker eksempelfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="b9784-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="b9784-107">Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="b9784-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b9784-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b9784-108">Click New.</span></span>
3. <span data-ttu-id="b9784-109">Angi eller velg en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="b9784-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="b9784-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b9784-111">Angi for eksempel "firmakundeemne, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="b9784-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="b9784-112">Skriv inn en verdi i Søkenavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="b9784-113">Angi for eksempel "bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="b9784-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="b9784-114">Vis delen Teknisk informasjon.</span><span class="sxs-lookup"><span data-stu-id="b9784-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="b9784-115">Skriv inn en verdi i Fabrikat-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="b9784-116">Skriv inn en verdi i Modell-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="b9784-117">Skriv inn en verdi i Modellår-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="b9784-118">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="b9784-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="b9784-119">Klikk Postinformasjon.</span><span class="sxs-lookup"><span data-stu-id="b9784-119">Click Record info.</span></span>
12. <span data-ttu-id="b9784-120">Klikk Brukermal.</span><span class="sxs-lookup"><span data-stu-id="b9784-120">Click User template.</span></span>
13. <span data-ttu-id="b9784-121">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b9784-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b9784-122">Angi for eksempel "firma, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="b9784-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="b9784-123">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b9784-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b9784-124">Angi for eksempel "firma, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="b9784-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="b9784-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b9784-125">Click OK.</span></span>
16. <span data-ttu-id="b9784-126">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="b9784-126">Click Close.</span></span>


