---
title: Opprette en postmal for å forenkle dataregistrering
description: Denne fremgangsmåten beskriver hvordan du oppretter en postmal slik at verdiene som brukes ofte, ikke trenger å angis eksplisitt for hver nye post.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544258"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="48fe8-103">Opprette en postmal for å forenkle dataregistrering</span><span class="sxs-lookup"><span data-stu-id="48fe8-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48fe8-104">Denne fremgangsmåten beskriver hvordan du oppretter en postmal slik at verdiene som brukes ofte, ikke trenger å angis eksplisitt for hver nye post.</span><span class="sxs-lookup"><span data-stu-id="48fe8-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="48fe8-105">I denne prosedyren skal du opprette en ny post for nye bærbare datamaskiner som skal legges til anleggsmidlene.</span><span class="sxs-lookup"><span data-stu-id="48fe8-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="48fe8-106">Denne prosedyren bruker eksempelfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="48fe8-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="48fe8-107">Gå til Anleggsmidler > Anleggsmidler > Anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="48fe8-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="48fe8-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="48fe8-108">Click New.</span></span>
3. <span data-ttu-id="48fe8-109">Angi eller velg en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="48fe8-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="48fe8-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="48fe8-111">Angi for eksempel "firmakundeemne, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="48fe8-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="48fe8-112">Skriv inn en verdi i Søkenavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="48fe8-113">Angi for eksempel "bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="48fe8-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="48fe8-114">Vis delen Teknisk informasjon.</span><span class="sxs-lookup"><span data-stu-id="48fe8-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="48fe8-115">Skriv inn en verdi i Fabrikat-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="48fe8-116">Skriv inn en verdi i Modell-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="48fe8-117">Skriv inn en verdi i Modellår-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="48fe8-118">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="48fe8-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="48fe8-119">Klikk Postinformasjon.</span><span class="sxs-lookup"><span data-stu-id="48fe8-119">Click Record info.</span></span>
12. <span data-ttu-id="48fe8-120">Klikk Brukermal.</span><span class="sxs-lookup"><span data-stu-id="48fe8-120">Click User template.</span></span>
13. <span data-ttu-id="48fe8-121">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="48fe8-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="48fe8-122">Angi for eksempel "firma, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="48fe8-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="48fe8-123">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="48fe8-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="48fe8-124">Angi for eksempel "firma, bærbar datamaskin".</span><span class="sxs-lookup"><span data-stu-id="48fe8-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="48fe8-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="48fe8-125">Click OK.</span></span>
16. <span data-ttu-id="48fe8-126">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="48fe8-126">Click Close.</span></span>

