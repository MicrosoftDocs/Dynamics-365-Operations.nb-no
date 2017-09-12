--- 
title: Opprette format for telling og summering for elektronisk rapportering (ER)
description: "De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: cac3748182ba27735264acc947403d7b857f1b6e
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="503b3-103">Opprette format for telling og summering for elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="503b3-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="503b3-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="503b3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="503b3-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="503b3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="503b3-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="503b3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="503b3-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="503b3-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="503b3-108">Få tilgang til listen over konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="503b3-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="503b3-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="503b3-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="503b3-110">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="503b3-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="503b3-111">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="503b3-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="503b3-112">Velg Litware, Inc. som</span><span class="sxs-lookup"><span data-stu-id="503b3-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="503b3-113">leverandør.</span><span class="sxs-lookup"><span data-stu-id="503b3-113">provider.</span></span>
3. <span data-ttu-id="503b3-114">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="503b3-114">Click Repositories.</span></span>
    * <span data-ttu-id="503b3-115">Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.</span><span class="sxs-lookup"><span data-stu-id="503b3-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="503b3-116">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="503b3-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="503b3-117">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="503b3-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="503b3-118">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="503b3-118">Click Create repository.</span></span>
7. <span data-ttu-id="503b3-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="503b3-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="503b3-120">Få Intrastat-konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="503b3-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="503b3-121">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="503b3-121">Click Open.</span></span>
2. <span data-ttu-id="503b3-122">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="503b3-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="503b3-123">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="503b3-123">Click Import.</span></span>
    * <span data-ttu-id="503b3-124">Klikk Importer for versjon 1.1 av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="503b3-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="503b3-125">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="503b3-125">Click Yes.</span></span>
5. <span data-ttu-id="503b3-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="503b3-126">Close the page.</span></span>
6. <span data-ttu-id="503b3-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="503b3-127">Close the page.</span></span>
7. <span data-ttu-id="503b3-128">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="503b3-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="503b3-129">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="503b3-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="503b3-130">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="503b3-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


