---
title: "Eksempel på leverandørsjekker ved elektronisk rapportering"
description: Dette emnet gir generell informasjon om hvordan du bruker eksempelsjekkformatene i elektronisk rapportering.
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="ca80c-103">Eksempel på sjekkformater ved elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="ca80c-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="ca80c-104">Du kan bruke elektronisk rapportering (ER) til å formatere leverandørsjekker.</span><span class="sxs-lookup"><span data-stu-id="ca80c-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="ca80c-105">Mange bank-spesifikke og sjekkleverandør-spesifikke sjekkformater er tilgjengelig på markedet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="ca80c-106">Eksempler på sjekkformater er tatt med i sjekkbetalingsmodellen i repositoriet til ER-verktøyet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="ca80c-107">Disse eksempelsjekkene er kalt **Sjekk i midten (USA)** og **Sjekk øverst stub under (USA)**.</span><span class="sxs-lookup"><span data-stu-id="ca80c-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="ca80c-108">Hvilke sjekkformater støttes for tiden?</span><span class="sxs-lookup"><span data-stu-id="ca80c-108">What check formats are currently supported?</span></span>

<span data-ttu-id="ca80c-109">Du bør alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og viser den gjeldende listen over tilgjengelige filer som har aktivatypen **TYSK konfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="ca80c-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="ca80c-110">Den neste delen, "Hva må jeg konfigurere?", inneholder en kobling til et emne som forklarer hvordan du oppretter et LCS-repositorium, slik at du kan se gjennom tilgjengelige konfigurasjoner og importere valgte konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="ca80c-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="ca80c-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition inneholder et eksempelformat der sjekken er øverst, etterfulgt av to deler for remittering.</span><span class="sxs-lookup"><span data-stu-id="ca80c-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="ca80c-112">Det inneholder også et eksempelformat hvor sjekken er i midten, mellom to remitteringsdeler.</span><span class="sxs-lookup"><span data-stu-id="ca80c-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="ca80c-113">Disse eksempelformatene tilsvarer formatet for Deluxe-forretningssjekker.</span><span class="sxs-lookup"><span data-stu-id="ca80c-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="ca80c-114">Hva må jeg konfigurere?</span><span class="sxs-lookup"><span data-stu-id="ca80c-114">What do I have to set up?</span></span>

- <span data-ttu-id="ca80c-115">Før du kan skrive ut sjekker ved hjelp av ER må minst én aktiv sjekk-konfigurasjon importeres til dine ER-konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="ca80c-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="ca80c-116">hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="ca80c-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="ca80c-117">Når du konfigurerer kontant- og bankbehandlingssjekker for bankkontoen, merker du av for **Generisk elektronisk eksportformat**, og velger deretter riktig sjekkformat som en eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="ca80c-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="ca80c-118">Du må også angi hvor mange seddellinjer som skal skrives ut på remitteringen.</span><span class="sxs-lookup"><span data-stu-id="ca80c-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="ca80c-119">Husk å inkludere radoverskrifter når du beregner dette antallet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="ca80c-120">For de to eksempelsjekkformatene er anbefalt antall følgeseddellinjer 17.</span><span class="sxs-lookup"><span data-stu-id="ca80c-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="ca80c-121">Dette nummeret vil imidlertid variere, avhengig av sjekkpapiret og skriverdriverne.</span><span class="sxs-lookup"><span data-stu-id="ca80c-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="ca80c-122">Vi anbefaler at du skriver ut en testsjekk for å validere sjekkoppsettet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="ca80c-123">Hvis du vil skrive ut en testsjekk, velg  **Skriv ut test**-alternativet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="ca80c-124">Eksempelsjekkformatene fungerer best når **Marginer** er satt til **Ingen** i de avanserte skriveregenskapene for Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ca80c-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="ca80c-125">Etter at testsjekken er generert, aktiverer du redigering av Excel-utdataene, og konfigurerer sideoppsettet slik at alle margene er satt til **0** (null).</span><span class="sxs-lookup"><span data-stu-id="ca80c-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="ca80c-126">Sammenlign testeksemplaret av sjekkene med sjekkpapiret, og juster innstillingene til du er fornøyd med justeringen.</span><span class="sxs-lookup"><span data-stu-id="ca80c-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="ca80c-127">Når du genererer betalinger for den konfigurerte bankkontoen i betalingsjournalen, må sjekkene skrives ut ved hjelp av det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="ca80c-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="ca80c-128">Hvis du vil ha mer informasjon, se [Endre et format for elektronisk rapportering](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="ca80c-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

