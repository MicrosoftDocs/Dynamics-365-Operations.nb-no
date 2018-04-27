---
title: "Definere parametere for Personale på tvers av juridiske enheter"
description: "Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e73441a3f4190561d1d16db40ee1581267c8dfb
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-hr-parameters-across-legal-entities"></a><span data-ttu-id="bdaa3-104">Definere parametere for Personale på tvers av juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="bdaa3-104">Set up HR parameters across legal entities</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="bdaa3-105">Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="bdaa3-106">Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="bdaa3-107">Noen typer poster, for eksempel stillingsposter, deles på tvers av firmaer.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="bdaa3-108">Du må sette opp delte parametere for disse postene.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="bdaa3-109">Du bruker for eksempel siden **Delte parametere for personaladministrasjon** til å definere parametere for personale på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="bdaa3-110">På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="bdaa3-111">Tidligere utgitt funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="bdaa3-111">Previously released functionality</span></span>
<span data-ttu-id="bdaa3-112">I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="bdaa3-113">Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="bdaa3-114">Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="bdaa3-115">Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="bdaa3-116">Du kan angi en enkelt kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="bdaa3-117">Hvis du bruker Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="bdaa3-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="bdaa3-118">I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="bdaa3-119">Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="bdaa3-120">Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="bdaa3-121">Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personale** &gt; **Oppsett** &gt; **Identifikasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="bdaa3-122">Du kan angi en enkelt kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="bdaa3-123">I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: personalnummer, stilling, brukerforespørsels-ID, I-9-dokument, søker, diskusjon, fordel-ID og personalhandling (hvis denne posttypen er aktivert).</span><span class="sxs-lookup"><span data-stu-id="bdaa3-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="bdaa3-124">Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="bdaa3-125">Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="bdaa3-126">I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:</span><span class="sxs-lookup"><span data-stu-id="bdaa3-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="bdaa3-127">**Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="bdaa3-128">Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="bdaa3-129">**Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="bdaa3-130">Hvis du velger dette alternativet, må du åpne siden **Stilling** for hver nye stilling etter hvert som de blir tilgjengelig, og deretter angi datoen for **Tilgjengelig for tilordning** i kategorien **Generelt** for å aktivere arbeidertilordning.</span><span class="sxs-lookup"><span data-stu-id="bdaa3-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="see-also"></a><span data-ttu-id="bdaa3-131">Se også</span><span class="sxs-lookup"><span data-stu-id="bdaa3-131">See also</span></span>
--------

[<span data-ttu-id="bdaa3-132">Definere firmaspesifikke parametere for Personale</span><span class="sxs-lookup"><span data-stu-id="bdaa3-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




