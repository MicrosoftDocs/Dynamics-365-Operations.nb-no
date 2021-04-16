---
title: ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)
description: Dette emnet beskriver hvordan du konfigurerer et elektronisk rapporteringsformat som teller og summerer basert på data fra tekstutdataene som allerede er generert. (Del 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f1db144b2bfafa72abeaa92c6b21de717e4acbf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749051"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="f5a4c-104">ER Konfigurere format for å utføre telling og summering (del 1 - Opprette format)</span><span class="sxs-lookup"><span data-stu-id="f5a4c-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5a4c-105">De følgende trinnene forklarer hvordan en bruker som er tilordnet rollen som systemansvarlig eller utvikler av elektronisk rapportering kan konfigurere et elektronisk rapportering (ER)-format til å utføre telling og summering basert på data i allerede genererte tekstutdata.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f5a4c-106">Denne fremgangsmåten kan utføres i alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="f5a4c-107">For å fullføre disse trinnene må du først fullføre trinnene i fremgangsmåten "Opprette en konfigurasjonsleverandør og merke den som aktiv".</span><span class="sxs-lookup"><span data-stu-id="f5a4c-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="f5a4c-108">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="f5a4c-109">Få tilgang til listen over konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5a4c-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f5a4c-110">Gå til Organisasjonsstyring > Arbeidsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f5a4c-111">Forsikre deg om at leverandøren Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="f5a4c-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="f5a4c-112">er tilgjengelig og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f5a4c-113">Velg Litware, Inc. som</span><span class="sxs-lookup"><span data-stu-id="f5a4c-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="f5a4c-114">leverandør.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-114">provider.</span></span>
3. <span data-ttu-id="f5a4c-115">Klikk på Repositorier.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-115">Click Repositories.</span></span>
    * <span data-ttu-id="f5a4c-116">Hvis det allerede finnes et repositorium av typen operasjonsressurser, kan du hoppe over resten av trinnene i gjeldende underoppgave.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="f5a4c-117">Klikk på Legg til for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="f5a4c-118">Skriv inn Operasjonsressurser i feltet Type konfigurasjonsrepositorium.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="f5a4c-119">Klikk på Opprett repositorium.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-119">Click Create repository.</span></span>
7. <span data-ttu-id="f5a4c-120">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="f5a4c-121">Få Intrastat-konfigurasjoner som leveres av Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5a4c-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="f5a4c-122">Klikk på Åpne.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-122">Click Open.</span></span>
2. <span data-ttu-id="f5a4c-123">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="f5a4c-124">Klikk på Importer.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-124">Click Import.</span></span>
    * <span data-ttu-id="f5a4c-125">Klikk på Importer for versjon 1.1 av den valgte konfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="f5a4c-126">Klikk på Ja.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-126">Click Yes.</span></span>
5. <span data-ttu-id="f5a4c-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-127">Close the page.</span></span>
6. <span data-ttu-id="f5a4c-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-128">Close the page.</span></span>
7. <span data-ttu-id="f5a4c-129">Klikk på Rapporteringskonfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="f5a4c-130">Utvid Intrastat-modell i treet.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="f5a4c-131">Velg Intrastat-modell\Intrastat (DE) i treet.</span><span class="sxs-lookup"><span data-stu-id="f5a4c-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]