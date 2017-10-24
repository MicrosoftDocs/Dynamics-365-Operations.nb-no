---
title: "Overvåkingspolicybrudd og -saker"
description: "Artikkelen forklarer hvordan overvåkingssaker genereres basert på brudd på overvåkingspolicyregler. Den inneholder også informasjon om de forskjellige måtene overvåkingspolicyer bruker datoområdet for dokumentvalg."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 24ee0dbf01208f8decc167e11e84191eaae03edf
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="d31f4-104">Overvåkingspolicybrudd og -saker</span><span class="sxs-lookup"><span data-stu-id="d31f4-104">Audit policy violations and cases</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d31f4-105">Artikkelen forklarer hvordan overvåkingssaker genereres basert på brudd på overvåkingspolicyregler.</span><span class="sxs-lookup"><span data-stu-id="d31f4-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="d31f4-106">Den inneholder også informasjon om de forskjellige måtene overvåkingspolicyer bruker datoområdet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="d31f4-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="d31f4-107">Hvordan overvåkingssaker genereres</span><span class="sxs-lookup"><span data-stu-id="d31f4-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="d31f4-108">Overvåkingspolicyer brukes til å identifisere utgiftsrapporter, bestillinger og leverandørfakturaer som ikke er i tråd med forretningsregler du definerer og konfigurerer som overvåkingspolicyregler.</span><span class="sxs-lookup"><span data-stu-id="d31f4-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="d31f4-109">Overvåkingspolicyer kjører i satsvis modus.</span><span class="sxs-lookup"><span data-stu-id="d31f4-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="d31f4-110">Når du kjører en overvåkingspolicy, kjøres alle policyreglene som er en del av policyen, samtidig.</span><span class="sxs-lookup"><span data-stu-id="d31f4-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="d31f4-111">Hver policyregel vurderer et sett med dokumenter.</span><span class="sxs-lookup"><span data-stu-id="d31f4-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="d31f4-112">Policyregelen velger dokumenter som er i datoområdet for dokumentutvalg og oppfyller de angitte kriteriene.</span><span class="sxs-lookup"><span data-stu-id="d31f4-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="d31f4-113">En policyregel kan for eksempel velge utgiftsrapporter som har måltider som overskrider 500,00.</span><span class="sxs-lookup"><span data-stu-id="d31f4-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="d31f4-114">En annen policyregel kan velge leverandørfakturaer som betales til en bestemt leverandør.</span><span class="sxs-lookup"><span data-stu-id="d31f4-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="d31f4-115">Det genereres et brudd for hvert dokument som velges i settet.</span><span class="sxs-lookup"><span data-stu-id="d31f4-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="d31f4-116">Dette bruddet er en post der et bestemt dokument, for eksempel faktura 12345, ikke er i tråd med policyregelen.</span><span class="sxs-lookup"><span data-stu-id="d31f4-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="d31f4-117">Flere poster for overvåkingsbrudd grupperes og knyttes til overvåkingssaker.</span><span class="sxs-lookup"><span data-stu-id="d31f4-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="d31f4-118">Saker for hver overvåkingspolicy grupperes som standard etter overvåkingspolicyregel.</span><span class="sxs-lookup"><span data-stu-id="d31f4-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="d31f4-119">Hvis du vil, kan du velge andre grupperingskriterier ved på siden **Kriterier for saksgruppering**.</span><span class="sxs-lookup"><span data-stu-id="d31f4-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="d31f4-120">Du kan for eksempel gruppere utgiftshoder etter prosjekt-ID og leverandørfakturaer etter leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="d31f4-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="d31f4-121">I dette tilfellet grupperes alle utgiftshodebrudd som har samme prosjekt-ID, i samme sak, og alle leverandørfakturaer som har samme leverandørkonto, grupperes i samme sak.</span><span class="sxs-lookup"><span data-stu-id="d31f4-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="d31f4-122">Når det gjelder overvåkingspolicyregler som er basert på spørringstypen **Duplikat**, grupperes ikke brudd etter policyregel eller kriteriene som er angitt på siden **Kriterier for saksgruppering**.</span><span class="sxs-lookup"><span data-stu-id="d31f4-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="d31f4-123">I stedet grupperes de etter kriteriene som er innebygd i overvåkingspolicyregelen.</span><span class="sxs-lookup"><span data-stu-id="d31f4-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="d31f4-124">Hvis en policyregel for eksempel evaluerer utgiftsrapporter for dupliserte utgifter av samme beløp, forretningsenhets-ID og dato, er alle utgifter som har de samme verdiene i disse feltene, én sak.</span><span class="sxs-lookup"><span data-stu-id="d31f4-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="d31f4-125">Alle utgifter som har andre verdier, er en separat sak.</span><span class="sxs-lookup"><span data-stu-id="d31f4-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="d31f4-126">Etter at overvåkingssakene er generert, behandles de ved hjelp av de vanlige fremgangsmåtene for saksbehandling.</span><span class="sxs-lookup"><span data-stu-id="d31f4-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="d31f4-127">Datoområder for dokumentutvalg</span><span class="sxs-lookup"><span data-stu-id="d31f4-127">Document selection date ranges</span></span>
<span data-ttu-id="d31f4-128">Når en overvåkingspolicy kjøres, velger hver policyregel dokumenter av den angitte typen som har en dato som er i datoområdet for dokumentutvalg.</span><span class="sxs-lookup"><span data-stu-id="d31f4-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="d31f4-129">Datoområdet for dokumentvalg angis på **Tilleggsalternativer**-siden.</span><span class="sxs-lookup"><span data-stu-id="d31f4-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="d31f4-130">Mange dokumenter har flere datoer tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="d31f4-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="d31f4-131">Datofeltet som overvåkingspolicyregelen bruker, er angitt på siden **Type policyregel**.</span><span class="sxs-lookup"><span data-stu-id="d31f4-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="d31f4-132">Her er noen andre måter en overvåkingspolicy bruker datoområdet for dokumentvalg på:</span><span class="sxs-lookup"><span data-stu-id="d31f4-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="d31f4-133">Policyen bruker versjonen av hver policyregel som gjelder på den siste dagen i datoområdet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="d31f4-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="d31f4-134">Du kan vise gyldighetsdatoene for hver policyregel på listesiden **Overvåkingspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="d31f4-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d31f4-135">Policyen bruker organisasjonsnodene som er knyttet til policyen, på den siste dagen i datoområdet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="d31f4-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="d31f4-136">Bare organisasjonsnodene som for øyeblikket er knyttet til policyen, vises på listesiden **Overvåkingspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="d31f4-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d31f4-137">Når det gjelder policyregler som er basert på spørringstypen **Listesøk**, evaluerer policyen dokumenter basert på overvåkede enheter som er gyldige på den siste dagen i datoområdet for dokumentvalg.</span><span class="sxs-lookup"><span data-stu-id="d31f4-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="d31f4-138">Hvis du vil ha mer informasjon, se [Overvåkingspolicyregler](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="d31f4-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




