---
title: Avansert bankavstemming MT940-import – oppgradering for sammensatt dataenhet
description: Et serienummer må legges til importenheten for bankkontoutdraget for å støtte MT940-formatet.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "343794"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="e6913-103">Avansert bankavstemming MT940-import – oppgradering for sammensatt dataenhet</span><span class="sxs-lookup"><span data-stu-id="e6913-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6913-104">Et serienummer må legges til importenheten for bankkontoutdraget for å støtte MT940-formatet.</span><span class="sxs-lookup"><span data-stu-id="e6913-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="e6913-105">Bruk fremgangsmåten nedenfor for å legge til importenheten for bankkontoutdrag for å støtte MT940-formatet.</span><span class="sxs-lookup"><span data-stu-id="e6913-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="e6913-106">Kompiler og synkroniser følgende:</span><span class="sxs-lookup"><span data-stu-id="e6913-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="e6913-107">Sammensatt Entity\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="e6913-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="e6913-108">Entity\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="e6913-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="e6913-109">Entity\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="e6913-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="e6913-110">Entity\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="e6913-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="e6913-111">Entity\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="e6913-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="e6913-112">Tabeller\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="e6913-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="e6913-113">Databehandling\\dataprosjekter.</span><span class="sxs-lookup"><span data-stu-id="e6913-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="e6913-114">Laste inn MT940-importprosjekter</span><span class="sxs-lookup"><span data-stu-id="e6913-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="e6913-115">Endre XSLT.</span><span class="sxs-lookup"><span data-stu-id="e6913-115">Change XSLT.</span></span>
            -   <span data-ttu-id="e6913-116">Klikk **Vis tilordning**.</span><span class="sxs-lookup"><span data-stu-id="e6913-116">Click **View map**.</span></span>
            -   <span data-ttu-id="e6913-117">Klikk **Vis tilordning** på dokumentet for bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="e6913-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="e6913-118">Klikk **Transformasjoner**</span><span class="sxs-lookup"><span data-stu-id="e6913-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="e6913-119">Slett filen BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="e6913-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="e6913-120">Legg til den nye versjonen av BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="e6913-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="e6913-121">Vise **Serienummer** på **Kildedata**-oppsettet.</span><span class="sxs-lookup"><span data-stu-id="e6913-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="e6913-122">Kildedataformat = XML-element.</span><span class="sxs-lookup"><span data-stu-id="e6913-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="e6913-123">Enhetsnavn = Bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="e6913-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="e6913-124">Last opp datafil = ny versjon SampleBankCompositeEntity.xml.</span><span class="sxs-lookup"><span data-stu-id="e6913-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="e6913-125">Klikk **Ja** for å overskrive den eksisterende filen.</span><span class="sxs-lookup"><span data-stu-id="e6913-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="e6913-126">Klikk **Ja** for å generere en ny tilordning.</span><span class="sxs-lookup"><span data-stu-id="e6913-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="e6913-127">Kontroller at S**equenceNumber** er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="e6913-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="e6913-128">Klikk **Vis tilordning** på utdragsenheten.</span><span class="sxs-lookup"><span data-stu-id="e6913-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="e6913-129">Kontroller at **SequenceNumber** er tilordnet fra Kilde til Oppsamling.</span><span class="sxs-lookup"><span data-stu-id="e6913-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="e6913-130">Importer det nye utdraget.</span><span class="sxs-lookup"><span data-stu-id="e6913-130">Import the new statement.</span></span>




