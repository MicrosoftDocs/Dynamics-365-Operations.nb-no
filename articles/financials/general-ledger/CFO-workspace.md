---
title: Legge til finansdimensjoner i CFO-arbeidsområdet
description: Dette emnet forklarer hvordan du legger til finansdimensjoner i CFO-arbeidsområdet, slik at de kan brukes for økonomi- og budsjettrapportene.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a15414eff99751d4e77e5b3bf315a556efb7ad5d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "332685"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="ac3b1-103">Legge til finansdimensjoner i CFO-arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="ac3b1-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac3b1-104">Dette emnet forklarer hvordan du legger til finansdimensjoner i CFO-arbeidsområdet, slik at de kan brukes for økonomi- og budsjettrapportene.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="ac3b1-105">CFO-arbeidsområdet har en **Oversikt**-kategori og en **Finans**-kategori. Rapportene i disse to kategoriene støttes av to mål: LedgerActivityMeasure og BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="ac3b1-106">I Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), er det en sammenheng mellom disse to målene og DimensionCombinationEntity-enheten.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="ac3b1-107">Derfor kan du velge dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="ac3b1-108">I Finance and Operations, på **Enhetsbutikk**-siden, oppdaterer du målene **LedgerActivityMeasure** og **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="ac3b1-109">Åpne Programutforsker i Microsoft Visual Studio, og søk etter **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="ac3b1-110">Under **Ressurser** åpner du **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="ac3b1-111">Når ressursen åpnes i Microsoft Power BI-skrivebordet, velger du **Hent data**, velger **SQL Server-database**, og velger deretter **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="ac3b1-112">Angi servernavnet, og angi deretter **AxDW** som databasen.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="ac3b1-113">Velg **DirectQuery**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="ac3b1-114">Søk etter og velg **LedgerActivityMeasure\_DimensionCombination**, og velg deretter **Last inn**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="ac3b1-115">I **Felt**-listen gir du nytt navn til tabellen **Finansdimensjoner**, slik at den er enkel å identifisere.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="ac3b1-116">Velg **Behandle relasjoner**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="ac3b1-117">I det første feltet velger du **Aktiviteter i øknomimodulen**, og deretter velger du **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="ac3b1-118">I det andre feltet velger du **LedgerActivityMeasure\_DimensionCombination** (eller **Finansdimensjoner** hvis du endret navnet på tabellen).</span><span class="sxs-lookup"><span data-stu-id="ac3b1-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="ac3b1-119">Velg **DimensionCombinationRECID**-hodet.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="ac3b1-120">I **Kardinalitet**-feltet velger du **Mange til en**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="ac3b1-121">Endre verdien **Kryssfiltreringsretning** til **Enkelt**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="ac3b1-122">Merk av for både **Gjør denne relasjonen aktiv** og **Anta referanseintegritet**, velg **OK**, og velg deretter **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="ac3b1-123">[![Opprette en relasjon](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="ac3b1-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="ac3b1-124">I **Felt**-listen skal du se tabellen og de tilgjengelige finansdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="ac3b1-125">Dra finansdimensjonene som du vil bruke, til rapportnivåfiltrene.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="ac3b1-126">Lagre endringene.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-126">Save your changes.</span></span>
15. <span data-ttu-id="ac3b1-127">I applikasjonsobjekttreet høyreklikker du prosjektet, og velger deretter **Synkroniser**.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="ac3b1-128">Bygge prosjektet, og åpne deretter programmet for å vise resultatene.</span><span class="sxs-lookup"><span data-stu-id="ac3b1-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="ac3b1-129">[![Fullført arbeidsområde](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="ac3b1-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
