---
title: Konfigurere delte parametere
description: Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter. Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 297141ab17660533b441629ccdfc624bbcb9c82b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467295"
---
# <a name="configure-shared-parameters"></a><span data-ttu-id="e4c92-104">Konfigurere delte parametere</span><span class="sxs-lookup"><span data-stu-id="e4c92-104">Configure shared parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e4c92-105">Du må definerte delte parametere for poster som deles på tvers av firmaer, for eksempel stillingsposter.</span><span class="sxs-lookup"><span data-stu-id="e4c92-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="e4c92-106">Denne artikkelen forklarer hvordan du definerer personalparametere på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="e4c92-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="e4c92-107">Noen typer poster, for eksempel stillingsposter, deles på tvers av firmaer.</span><span class="sxs-lookup"><span data-stu-id="e4c92-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="e4c92-108">Du må sette opp delte parametere for disse postene.</span><span class="sxs-lookup"><span data-stu-id="e4c92-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="e4c92-109">Du bruker for eksempel siden **Delte parametere for personaladministrasjon** til å definere parametere for personale på tvers av juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="e4c92-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="e4c92-110">På siden **Delte parametere for personaladministrasjon** grupperes parameterne i områder, basert på deres funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="e4c92-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="e4c92-111">Tidligere utgitt funksjonalitet</span><span class="sxs-lookup"><span data-stu-id="e4c92-111">Previously released functionality</span></span>
<span data-ttu-id="e4c92-112">I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden.</span><span class="sxs-lookup"><span data-stu-id="e4c92-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="e4c92-113">Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="e4c92-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="e4c92-114">Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="e4c92-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="e4c92-115">Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personaladministrasjon** &gt; **Koblinger** &gt; **Oppsett** &gt; **Identifikasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="e4c92-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="e4c92-116">Du kan angi en enkelt kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e4c92-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-human-resources"></a><span data-ttu-id="e4c92-117">Hvis du bruker Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="e4c92-117">If you're using Dynamics 365 Human Resources</span></span>
<span data-ttu-id="e4c92-118">I kategorien **Identifikasjon** må du velge identifikasjonstypene som representerer identifikasjonsnumrene som er oppført på siden.</span><span class="sxs-lookup"><span data-stu-id="e4c92-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="e4c92-119">Du må definere identifikasjonstyper før du kan angi identifikasjonsopplysninger for arbeidere.</span><span class="sxs-lookup"><span data-stu-id="e4c92-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="e4c92-120">Informasjonen om personnummer, nasjonale ID-nummer, fremmed ID-nummer og personlig ID-kode vedlikeholdes på siden **Identifikasjonstype**.</span><span class="sxs-lookup"><span data-stu-id="e4c92-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="e4c92-121">Hvis du vil definere en ny ID-type eller gå gjennom listen over eksisterende typer, klikker du **Personale** &gt; **Oppsett** &gt; **Identifikasjonstyper**.</span><span class="sxs-lookup"><span data-stu-id="e4c92-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="e4c92-122">Du kan angi en enkelt kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e4c92-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="e4c92-123">I kategorien **Nummerserier** kan du velge nummerseriene som brukes for følgende poster: personalnummer, stilling, brukerforespørsels-ID, I-9-dokument, søker, diskusjon, fordel-ID og personalhandling (hvis denne posttypen er aktivert).</span><span class="sxs-lookup"><span data-stu-id="e4c92-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="e4c92-124">Hvis du vil vedlikeholde nummerseriereferanser og -koder, kan du bruke listesiden **Nummerserier**.</span><span class="sxs-lookup"><span data-stu-id="e4c92-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="e4c92-125">Hvis du vil finne denne siden, kan du bruke søkefunksjonen for sider.</span><span class="sxs-lookup"><span data-stu-id="e4c92-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="e4c92-126">I kategorien **Stillinger** angi om nye stillinger er tilgjengelige for tilordning som standard:</span><span class="sxs-lookup"><span data-stu-id="e4c92-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="e4c92-127">**Alltid** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="e4c92-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="e4c92-128">Når det opprettes stillinger, blir dato og klokkeslett for **Tilgjengelig for tilordning** på i kategorien **Generelt** på **Stilling**-siden, automatisk satt til opprettelsesdato og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="e4c92-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="e4c92-129">**Aldri** – Du kan ikke tilordne arbeidere til nye stillinger når stillinger opprettes.</span><span class="sxs-lookup"><span data-stu-id="e4c92-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="e4c92-130">Hvis du velger dette alternativet, må du åpne siden **Stilling** for hver nye stilling etter hvert som de blir tilgjengelig, og deretter angi datoen for **Tilgjengelig for tilordning** i kategorien **Generelt** for å aktivere arbeidertilordning.</span><span class="sxs-lookup"><span data-stu-id="e4c92-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]