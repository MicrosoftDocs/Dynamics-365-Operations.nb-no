---
title: Vis resultater for automatisering av leverandørfakturaer (forhåndsversjon)
description: Dette emnet forklarer hvordan du viser statusen for leverandørfakturaer som er i den automatiserte prosessen for sending til arbeidsflyt.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248100"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="b3b4b-103">Vise resultater for automatisering av leverandørfaktura</span><span class="sxs-lookup"><span data-stu-id="b3b4b-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3b4b-104">Dette emnet forklarer hvordan du viser statusen for leverandørfakturaer som er i den automatiserte prosessen for sending til arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="b3b4b-105">Detaljer om automatiseringsloggen vedlikeholdes for hver importerte leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="b3b4b-106">Avhengig av forretningsprosessene du har automatisert, vises siden **Ventende leverandørfakturaer** verdiene **Status for automatisert kvitteringssamsvar** og **Status for automatisert send til arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="b3b4b-107">Du kan vise detaljene og lage en plan for å fokusere på fakturaene som mislyktes på et automatisk trinn.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="b3b4b-108">Etter at du har rettet problemet, kan du gjenoppta den automatiserte prosessen for den importerte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="b3b4b-109">Før du kan redigere en faktura som er sendt, må du stoppe den automatiserte behandlingen midlertidig.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="b3b4b-110">Hvis en faktura i den automatiserte prosessen for sending til arbeidsflyt er stoppet midlertidig, setter du feltet **Inkluder i automatisert behandling** til **Nei** på siden **Leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="b3b4b-111">Automatisering vil da ikke kjøre før **Inkluder i automatisert behandling** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="b3b4b-112">En faktura kan stoppes midlertidig fra ytterligere automatisering hvis den ennå ikke er i arbeidsflytsystemet og ikke brukes av den automatiserte prosessen.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="b3b4b-113">Hvis den importerte fakturaen er underlagt prosessen for sending til arbeidsflyt, kan du vise verdien **Status for automatisering** på siden **Leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="b3b4b-114">Følgende statuser spores:</span><span class="sxs-lookup"><span data-stu-id="b3b4b-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="b3b4b-115">**Inkludert** – De automatiserte prosessene som er definert på siden **Leverandørparametere**, kjører på riktig måte, men er ennå ikke fullført.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="b3b4b-116">**Stoppet midlertidig** – De automatiserte prosessene som er definert på siden **Leverandørparametere**, er kjørt, men minst ett trinn i prosessen mislyktes.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="b3b4b-117">Statusen **Stoppet midlertidig** brukes også hvis feltet **Inkluder i automatisert behandling** er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="b3b4b-118">Du kan se feilene ved å velge **Vis de siste resultatene**.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="b3b4b-119">**I arbeidsflyt** – Den importerte fakturaen er sendt til arbeidsflytsystemet, enten av den automatiserte prosessen for sending til arbeidsflyt eller manuelt.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="b3b4b-120">**Arbeidsflyt fullført** – Arbeidsflytprosessen er fullført for den importerte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="b3b4b-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]