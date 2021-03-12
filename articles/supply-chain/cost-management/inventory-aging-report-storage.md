---
title: Lagring av rapport for aldersfordeling for lager
description: Dette emnet beskriver funksjonaliteten som lar deg kjøre en rapport for aldersfordeling for lager, og gjør utdataene tilgjengelige som et skjema og et diagram.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a292bd7a7ccbb09af1955e1e253b45e230c1009
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005433"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="e3324-103">Lagring av rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="e3324-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3324-104">I Microsoft Dynamics 365 Supply Chain Management kan du kjøre en rapport for **lagring av rapport for aldersfordeling for lager** og få utdataene tilgjengelige som et skjema og et diagram.</span><span class="sxs-lookup"><span data-stu-id="e3324-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="e3324-105">I skjemaet justeres kolonner og samlesaldoer dynamisk, avhengig av oppsettet som er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="e3324-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="e3324-106">Diagrammet gir en visuell oversikt som støtter filtrering, og lar deg drille ned til detaljer.</span><span class="sxs-lookup"><span data-stu-id="e3324-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="e3324-107">I tillegg kan du bruke en dataenhet som heter **Rapport for aldersfordeling for lager** til å eksportere resultatene av en rapport for **lagring av rapport for aldersfordeling for lager** til et format som f.eks. Microsoft Excel-fil eller en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="e3324-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="e3324-108">Denne metoden for å kjøre en rapport for **lagring av rapport for aldersfordeling for lager** er nyttig i tilfeller der utdataene inneholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="e3324-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="e3324-109">Utdataene vil for eksempel inneholde mange linjer hvis du har 50 000 varer og 300 butikker som opprettes som lagre, og du ber om aldersfordeling for lager etter vare, område og lager.</span><span class="sxs-lookup"><span data-stu-id="e3324-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="e3324-110">Aktiver funksjonen Rapport for oppbevaring av lagerverdi</span><span class="sxs-lookup"><span data-stu-id="e3324-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="e3324-111">Før du kan bruke denne funksjonen, må du aktivere den i systemet.</span><span class="sxs-lookup"><span data-stu-id="e3324-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="e3324-112">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e3324-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="e3324-113">Her vises funksjonen som:</span><span class="sxs-lookup"><span data-stu-id="e3324-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="e3324-114">**Modul** - Kostnadsstyring</span><span class="sxs-lookup"><span data-stu-id="e3324-114">**Module** - Cost management</span></span>
- <span data-ttu-id="e3324-115">**Funksjonsnavn** - Lagring av rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="e3324-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="e3324-116">Kjøre en lagring av rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="e3324-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="e3324-117">Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagring av rapport for aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="e3324-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="e3324-118">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e3324-118">Select **New**.</span></span>
1. <span data-ttu-id="e3324-119">I feltet **Prosess-ID – navn** angir du et unikt navn på rapporten.</span><span class="sxs-lookup"><span data-stu-id="e3324-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="e3324-120">Velg **Identifikasjon – ID**-rapporten, og filtrer den slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="e3324-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="e3324-121">Rapportutførelse utføres alltid i en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="e3324-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="e3324-122">Når den satsvise jobben er fullført, vises utdataene på siden **Lagring av rapport for aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="e3324-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="e3324-123">Hvis du vil vise utdata som et skjema som har et tradisjonelt rutenettoppsett, velger du **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="e3324-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="e3324-124">Hvis du vil vise utdata som et oppsamlet diagram, velger du **Vis diagram**.</span><span class="sxs-lookup"><span data-stu-id="e3324-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3324-125">Skjemaet inkluderer ikke delsummer som er definert i rapportoppsettet.</span><span class="sxs-lookup"><span data-stu-id="e3324-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="e3324-126">Ved hjelp av dateenheten **Rapport for aldersfordeling for lager** kan du eksportere utdataene for en **lagring av rapport for aldersfordeling for lager**-rapport ved å bruke et filter for **Prosess-ID – navn**-feltet til et hvilket som helst format som databehandling støtter.</span><span class="sxs-lookup"><span data-stu-id="e3324-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
