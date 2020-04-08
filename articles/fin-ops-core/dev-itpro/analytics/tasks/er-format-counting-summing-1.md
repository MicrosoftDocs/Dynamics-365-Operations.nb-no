---
title: ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)
description: De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141931"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="aea7a-103">ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)</span><span class="sxs-lookup"><span data-stu-id="aea7a-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aea7a-104">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="aea7a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="aea7a-105">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="aea7a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="aea7a-106">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="aea7a-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="aea7a-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="aea7a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="aea7a-108">Få tilgang til listen over konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="aea7a-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="aea7a-109">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="aea7a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="aea7a-110">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="aea7a-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="aea7a-111">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="aea7a-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="aea7a-112">Velg Litware, Inc. som</span><span class="sxs-lookup"><span data-stu-id="aea7a-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="aea7a-113">leverandør.</span><span class="sxs-lookup"><span data-stu-id="aea7a-113">provider.</span></span>
3. <span data-ttu-id="aea7a-114">Klikk Repositorier.</span><span class="sxs-lookup"><span data-stu-id="aea7a-114">Click Repositories.</span></span>
    * <span data-ttu-id="aea7a-115">Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.</span><span class="sxs-lookup"><span data-stu-id="aea7a-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="aea7a-116">Klikk Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="aea7a-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="aea7a-117">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="aea7a-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="aea7a-118">Klikk Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="aea7a-118">Click Create repository.</span></span>
7. <span data-ttu-id="aea7a-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="aea7a-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="aea7a-120">Få Intrastat-konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="aea7a-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="aea7a-121">Klikk Åpne.</span><span class="sxs-lookup"><span data-stu-id="aea7a-121">Click Open.</span></span>
2. <span data-ttu-id="aea7a-122">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="aea7a-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="aea7a-123">Klikk Importer.</span><span class="sxs-lookup"><span data-stu-id="aea7a-123">Click Import.</span></span>
    * <span data-ttu-id="aea7a-124">Klikk Importer for versjon 1.1 av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="aea7a-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="aea7a-125">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="aea7a-125">Click Yes.</span></span>
5. <span data-ttu-id="aea7a-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="aea7a-126">Close the page.</span></span>
6. <span data-ttu-id="aea7a-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="aea7a-127">Close the page.</span></span>
7. <span data-ttu-id="aea7a-128">Klikk Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="aea7a-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="aea7a-129">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="aea7a-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="aea7a-130">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="aea7a-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

