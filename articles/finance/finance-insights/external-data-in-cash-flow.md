---
title: Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)
description: Dette emnet beskriver oppsettrinnene som må fullføres, slik at eksterne data kan registreres eller importeres i kontantstrømprognoser.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 03318eaae0b3329dc758c48202f8f47ca2c4ab08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245574"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="db382-103">Bruke eksterne data i kontantstrømprognoser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="db382-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="db382-104">Eksterne data kan registreres eller importeres til kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="db382-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="db382-105">Dette emnet beskriver oppsettrinnene som gjelder spesielt for bruk av eksterne data, og som gjør det mulig å inkludere de eksterne dataene i en kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="db382-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="db382-106">Oppsett av eksterne data</span><span class="sxs-lookup"><span data-stu-id="db382-106">External data setup</span></span>

<span data-ttu-id="db382-107">Bruk kategorien **Ekstern kilde** på siden **Oppsett for kontantstrømprognose** (**Kontant- og bankbehandling \> Kontantstrømprognose**) for å angi innstillinger som støtter bruk av eksterne data i kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="db382-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="db382-108">Hvis du vil ha informasjon om oppsettet, se [Kontantstrømprognose](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="db382-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="db382-109">Hvis du vil angi eksterne data for kontantstrømprognoser, kan du bruke Åpne i Excel-opplevelsen for å registrere og endre eksterne data.</span><span class="sxs-lookup"><span data-stu-id="db382-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="db382-110">Velg knappen **Eksterne data**, og velg deretter enten **Legg til eksterne data** eller **Rediger eksisterende eksterne data**.</span><span class="sxs-lookup"><span data-stu-id="db382-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="db382-111">Når Microsoft Excel-filen åpnes, kan du angi informasjon i følgende felt:</span><span class="sxs-lookup"><span data-stu-id="db382-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="db382-112">**Post-ID**</span><span class="sxs-lookup"><span data-stu-id="db382-112">**Entry ID**</span></span>
- <span data-ttu-id="db382-113">**Beskrivelse** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="db382-113">**Description** (optional)</span></span>
- <span data-ttu-id="db382-114">**Eksternt kildenavn** – Velg en av verdiene i listen som du definerte da du konfigurerte Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="db382-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="db382-115">**Juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="db382-115">**Legal Entity**</span></span>
- <span data-ttu-id="db382-116">**Dato**</span><span class="sxs-lookup"><span data-stu-id="db382-116">**Date**</span></span>
- <span data-ttu-id="db382-117">**Beløp i transaksjonsvaluta**</span><span class="sxs-lookup"><span data-stu-id="db382-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="db382-118">**Valutakode**</span><span class="sxs-lookup"><span data-stu-id="db382-118">**Currency Code**</span></span>
- <span data-ttu-id="db382-119">**Standarddimensjon** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="db382-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="db382-120">**Dokumentnummer** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="db382-120">**Document number** (optional)</span></span>
- <span data-ttu-id="db382-121">**Kontonummer** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="db382-121">**Account number** (optional)</span></span>
- <span data-ttu-id="db382-122">**Kontonavn** (valgfritt)</span><span class="sxs-lookup"><span data-stu-id="db382-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="db382-123">Importere eksterne data ved hjelp av dataadministrasjonsrammeverk</span><span class="sxs-lookup"><span data-stu-id="db382-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="db382-124">Du kan importere eksterne data for kontantstrømprognoser ved hjelp av **Dataadministrasjon**-arbeidsområdet og enheten for **ekstern kildeoppføring for kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="db382-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="db382-125">Hvis du i tillegg må flytte oppsettdata fra ett miljø til et annet, er følgende enhetsområde tilgjengelig for oppsettabellene som kreves:</span><span class="sxs-lookup"><span data-stu-id="db382-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="db382-126">Oppsett av ekstern kilde for kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="db382-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="db382-127">Oppsett av juridisk enhet for ekstern kilde for kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="db382-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="db382-128">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="db382-128">Privacy notice</span></span>
<span data-ttu-id="db382-129">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="db382-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]