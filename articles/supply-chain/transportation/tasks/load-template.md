---
title: Lastmaler
description: Dette emnet beskriver hvordan du konfigurerer lastmaler og hvordan du knytter en lastmal til en ny last.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0a4070a1dd5d53bb502ba2ab0c91dbdc90ded34d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005058"
---
# <a name="load-templates"></a><span data-ttu-id="1cae3-103">Lastmaler</span><span class="sxs-lookup"><span data-stu-id="1cae3-103">Load templates</span></span>

<span data-ttu-id="1cae3-104">Når du oppretter en ny last, kan du tilordne en lastmal.</span><span class="sxs-lookup"><span data-stu-id="1cae3-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="1cae3-105">Lastmalen inneholder informasjon om utstyr og om mål, for eksempel høyde, bredde, dybde og mengde for lasten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="1cae3-106">Dette emnet beskriver hvordan du konfigurerer lastmaler og hvordan du knytter en lastmal til en ny last.</span><span class="sxs-lookup"><span data-stu-id="1cae3-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="1cae3-107">Konfigurere en lastmal</span><span class="sxs-lookup"><span data-stu-id="1cae3-107">Set up a load template</span></span>

1. <span data-ttu-id="1cae3-108">Gå til **Transportstyring \> Oppsett \> Lastplanlegging \> Lastmal**.</span><span class="sxs-lookup"><span data-stu-id="1cae3-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="1cae3-109">Velg **Ny** i handlingsruten for å legge til en ny mal eller **Rediger** for å redigere en eksisterende mal.</span><span class="sxs-lookup"><span data-stu-id="1cae3-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="1cae3-110">I raden for den nye eller eksisterende malen angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="1cae3-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="1cae3-111">**Lastmal-ID** – Angi en unik identifikator (ID) for lastmalen.</span><span class="sxs-lookup"><span data-stu-id="1cae3-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="1cae3-112">**Utstyr** – Velg utstyret som skal brukes til å levere lasten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="1cae3-113">**Lasthøyde**, **Lastbredde** og **Lastdybde** – Angi dimensjonene for lasten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="1cae3-114">**Maks. tillatte lastvolum** og **Maks. tillatte lastvekt** – Angi maksimalt tillatt volum og vekt for lasten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="1cae3-115">**Maksimalt tillatte bruttovekt** – Angi den maksimale tillatte bruttovekten for lasten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="1cae3-116">En lasts bruttovekt inkluderer både taravekten og lastvekten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="1cae3-117">**Maksimalt antall fraktdeler som er tillatt** – Angi det største antallet fraktdeler som lasten kan inneholde.</span><span class="sxs-lookup"><span data-stu-id="1cae3-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="1cae3-118">**Stable last på gulv** – Merk av i denne avmerkingsboksen for å bruke gulvlasting.</span><span class="sxs-lookup"><span data-stu-id="1cae3-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="1cae3-119">I et scenario med gulvlasting stables bokser fra gulv til tak og vegg til vegg i containeren for å utnytte plassen maksimalt.</span><span class="sxs-lookup"><span data-stu-id="1cae3-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="1cae3-120">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="1cae3-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="1cae3-121">Knytt en lastmal til en ny last</span><span class="sxs-lookup"><span data-stu-id="1cae3-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="1cae3-122">Gå til **Transportstyring \> Planlegging \> Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="1cae3-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="1cae3-123">I den øvre delen av siden velger du én av følgende kategorier, avhengig av hvilken type kilde dokument du oppretter en last for: **Leveringer**, **Salgslinjer**, **Overføringslinjer** eller **Bestillingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1cae3-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="1cae3-124">Velg det bestemte dokumentet du vil planlegge lasten for.</span><span class="sxs-lookup"><span data-stu-id="1cae3-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="1cae3-125">I handlingsruten, på **Forsyning og behov**-fanen, i **Legg til**-gruppen, velg **Til ny last**.</span><span class="sxs-lookup"><span data-stu-id="1cae3-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="1cae3-126">I dialogboksen **Lastmal**, i **Lastmal-ID**-feltet, velger du malen som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="1cae3-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="1cae3-127">Velg **OK** for å bruke malen.</span><span class="sxs-lookup"><span data-stu-id="1cae3-127">Select **OK** to apply the template.</span></span>
