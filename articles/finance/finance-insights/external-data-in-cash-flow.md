---
title: Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)
description: Dette emnet beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186696"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="c2865-103">Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="c2865-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c2865-104">Eksterne data kan registreres eller importeres til kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="c2865-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="c2865-105">Dette emnet beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="c2865-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="c2865-106">Oppsett av eksterne data</span><span class="sxs-lookup"><span data-stu-id="c2865-106">External data setup</span></span>

<span data-ttu-id="c2865-107">Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="c2865-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="c2865-108">Hvis du vil ha informasjon om oppsettet, se [Kontantstrømprognose](../cash-bank-management/cash-flow-forecasting.md).</span><span class="sxs-lookup"><span data-stu-id="c2865-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="c2865-109">Hvis du vil angi eksterne data for kontantstrømprognoser, kan du bruke Åpne i Excel-opplevelsen for å registrere og endre eksterne data.</span><span class="sxs-lookup"><span data-stu-id="c2865-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="c2865-110">Velg knappen **Eksterne data**, og velg deretter enten **Legg til eksterne data** eller **Rediger eksisterende eksterne data**.</span><span class="sxs-lookup"><span data-stu-id="c2865-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="c2865-111">Når Microsoft Excel-filen åpnes, kan du angi informasjon i følgende felt:</span><span class="sxs-lookup"><span data-stu-id="c2865-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="c2865-112">**Post-ID**</span><span class="sxs-lookup"><span data-stu-id="c2865-112">**Entry ID**</span></span>
- <span data-ttu-id="c2865-113">**Beskrivelse** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="c2865-113">**Description** (optional)</span></span>
- <span data-ttu-id="c2865-114">**Eksternt kildenavn** – Velg en av verdiene i listen som du definerte da du konfigurerte Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="c2865-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="c2865-115">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="c2865-115">**Legal Entity**</span></span>
- <span data-ttu-id="c2865-116">**Dato**</span><span class="sxs-lookup"><span data-stu-id="c2865-116">**Date**</span></span>
- <span data-ttu-id="c2865-117">**Beløp i transaksjonsvaluta**</span><span class="sxs-lookup"><span data-stu-id="c2865-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="c2865-118">**Valutakode**</span><span class="sxs-lookup"><span data-stu-id="c2865-118">**Currency Code**</span></span>
- <span data-ttu-id="c2865-119">**Standarddimensjon** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="c2865-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="c2865-120">**Dokumentnummer** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="c2865-120">**Document number** (optional)</span></span>
- <span data-ttu-id="c2865-121">**Kontonummer** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="c2865-121">**Account number** (optional)</span></span>
- <span data-ttu-id="c2865-122">**Kontonavn** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="c2865-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="c2865-123">Importere eksterne data ved hjelp av dataadministrasjonsrammeverk</span><span class="sxs-lookup"><span data-stu-id="c2865-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="c2865-124">Du kan importere eksterne data for kontantstrømprognoser ved hjelp av **Dataadministrasjon**-arbeidsområdet og enheten for **ekstern kildeoppføring for kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="c2865-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="c2865-125">Hvis du i tillegg må flytte oppsettdata fra ett miljø til et annet, er følgende enhetsområde tilgjengelig for oppsettabellene som kreves:</span><span class="sxs-lookup"><span data-stu-id="c2865-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="c2865-126">Oppsett av ekstern kilde for kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="c2865-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="c2865-127">Oppsett av juridisk enhet for ekstern kilde for kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="c2865-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
