---
title: Rapport for aldersfordeling for lager
description: Dette emnet beskriver funksjonaliteten som lar deg kjøre en rapport for aldersfordeling for lager, og gjør utdataene tilgjengelige som et skjema og et diagram.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 790c8fe3a52bce652227f1cef97eff6496476100
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201629"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="539fc-103">Rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="539fc-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="539fc-104">I Microsoft Dynamics 365 Supply Chain Management kan du kjøre en rapport for **aldersfordeling for lager** og få utdataene tilgjengelige som et skjema og et diagram.</span><span class="sxs-lookup"><span data-stu-id="539fc-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="539fc-105">I skjemaet justeres kolonner og samlesaldoer dynamisk, avhengig av oppsettet som er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="539fc-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="539fc-106">Diagrammet gir en visuell oversikt som støtter filtrering, og lar deg drille ned til detaljer.</span><span class="sxs-lookup"><span data-stu-id="539fc-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="539fc-107">I tillegg kan du bruke en dataenhet som heter **Rapport for aldersfordeling for lager** til å eksportere resultatene av en rapport for **aldersfordeling for lager** til et format som f.eks. Microsoft Excel-fil eller en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="539fc-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="539fc-108">Denne metoden for å kjøre en rapport for **aldersfordeling for lager** er nyttig i tilfeller der utdataene inneholder mange linjer.</span><span class="sxs-lookup"><span data-stu-id="539fc-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="539fc-109">Utdataene vil for eksempel inneholde mange linjer hvis du har 50 000 varer og 300 butikker som opprettes som lagre, og du ber om aldersfordeling for lager etter vare, område og lager.</span><span class="sxs-lookup"><span data-stu-id="539fc-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="539fc-110">Kjøre en rapport for aldersfordeling for lager</span><span class="sxs-lookup"><span data-stu-id="539fc-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="539fc-111">Gå til **Kostnadsstyring \> Forespørsler og rapporter \> Lagring av rapport for aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="539fc-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="539fc-112">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="539fc-112">Select **New**.</span></span>
1. <span data-ttu-id="539fc-113">I feltet **Prosess-ID – navn** angir du et unikt navn på rapporten.</span><span class="sxs-lookup"><span data-stu-id="539fc-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="539fc-114">Velg **Identifikasjon – ID**-rapporten, og filtrer den slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="539fc-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="539fc-115">Rapportutførelse utføres alltid i en satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="539fc-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="539fc-116">Når den satsvise jobben er fullført, vises utdataene på siden **Lagring av rapport for aldersfordeling for lager**.</span><span class="sxs-lookup"><span data-stu-id="539fc-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="539fc-117">Hvis du vil vise utdata som et skjema som har et tradisjonelt rutenettoppsett, velger du **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="539fc-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="539fc-118">Hvis du vil vise utdata som et oppsamlet diagram, velger du **Vis diagram**.</span><span class="sxs-lookup"><span data-stu-id="539fc-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="539fc-119">Skjemaet inkluderer ikke delsummer som er definert i rapportoppsettet.</span><span class="sxs-lookup"><span data-stu-id="539fc-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="539fc-120">Ved hjelp av dateenheten **Rapport for aldersfordeling for lager** kan du eksportere utdataene for en **Aldersfordeling for lager**-rapport ved å bruke et filter for **Prosess-ID – navn**-feltet til et hvilket som helst format som databehandling støtter.</span><span class="sxs-lookup"><span data-stu-id="539fc-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
