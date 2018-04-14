---
title: Behandling av generell journal
description: "Denne artikkelen beskriver funksjoner i Microsoft Dynamics 365 for Finance and Operations som kan hjelpe med å gjøre behandling av generell enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 038833752f5e96055fc1449a473705ecd937b5a4
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="7648c-103">Behandling av generell journal</span><span class="sxs-lookup"><span data-stu-id="7648c-103">General journal processing</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="7648c-104">Denne artikkelen beskriver funksjoner i Microsoft Dynamics 365 for Finance and Operations som kan hjelpe med å gjøre behandling av generell enklere, og som også kan bidra til å sikre at riktige data blir registrert og intern kontroll ikke settes på spill.</span><span class="sxs-lookup"><span data-stu-id="7648c-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="7648c-105">Journalnavn</span><span class="sxs-lookup"><span data-stu-id="7648c-105">Journal names</span></span>

<span data-ttu-id="7648c-106">Ett av de viktigste områdene å konfigurere er journalnavn.</span><span class="sxs-lookup"><span data-stu-id="7648c-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="7648c-107">Det er lurt å definere bestemte journalnavn for hvert formål, for eksempel konsernintern, justering av avsetning og korrigering.</span><span class="sxs-lookup"><span data-stu-id="7648c-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="7648c-108">Du kan tilpasse hvert enkelt journalnavn for å gjøre dataregistrering enkelt og sikker for hvert formål.</span><span class="sxs-lookup"><span data-stu-id="7648c-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="7648c-109">På siden **Journalnavn** kan du definere følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="7648c-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="7648c-110">**Arbeidsflytgodkjenning** – Hvis du vil øke den interne kontrollen, definerer du journalarbeidsflyter som etablerer materialgrenser for gjennomgangs- og godkjenningstrinnene, basert på kriterier som total debetbeløp.</span><span class="sxs-lookup"><span data-stu-id="7648c-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="7648c-111">Du konfigurerer arbeidsflyter for økonomijournaler på siden **Arbeidsflyter for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="7648c-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="7648c-112">**Standardverdier** – Velg standardverdier for motkontoer, valuta og finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="7648c-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="7648c-113">**Journalkontroll** – Du kan definere begrensninger for firma, kontotype og segmentverdier.</span><span class="sxs-lookup"><span data-stu-id="7648c-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="7648c-114">**Eksempler**</span><span class="sxs-lookup"><span data-stu-id="7648c-114">**Examples**</span></span>

<span data-ttu-id="7648c-115">Et journalnavn kan bare brukes til justeringer.</span><span class="sxs-lookup"><span data-stu-id="7648c-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="7648c-116">I så fall kan du angi at bare **Finans**-kontotypen er gyldig på tvers av alle firmaer.</span><span class="sxs-lookup"><span data-stu-id="7648c-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="7648c-117">[![Journalkontrollkontotyper](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="7648c-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="7648c-118">Et journalnavn kan bare brukes bare for et bestemt segment eller et område for hovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="7648c-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="7648c-119">[![Journalkontrollsegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="7648c-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="7648c-120">Alternativet **Automatisk tilbakeføring** er tilgjengelig i økonomijournaler.</span><span class="sxs-lookup"><span data-stu-id="7648c-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="7648c-121">Du har for eksempel en justering av avsetning der det faktiske dokumentet ikke har blitt behandlet ennå, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="7648c-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="7648c-122">[![Tilbakeføring for økonomijournal](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="7648c-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="7648c-123">Microsoft Excel-tillegget for journaloppføring gir et ekstra nivå med automatisering og gjør dataregistrering enklere.</span><span class="sxs-lookup"><span data-stu-id="7648c-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="7648c-124">Handlingen **Åpne linjer i Excel** er tilgjengelig på sidene **Økonomijournal** og **Journalbilag**.</span><span class="sxs-lookup"><span data-stu-id="7648c-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="7648c-125">På siden **Periodiske journaler** kan du definere at gjentakelsesjournaler skal automatisere behandlingen av journalen.</span><span class="sxs-lookup"><span data-stu-id="7648c-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="7648c-126">Du kan bruke bilagsmaler til enhver tid.</span><span class="sxs-lookup"><span data-stu-id="7648c-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="7648c-127">På siden **Økonomijournaler** finnes handlingene **Lagre** og **Velg bilagsmal** på **Journalbilag**-siden, under **Funksjoner** for bilagslinjene.</span><span class="sxs-lookup"><span data-stu-id="7648c-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="7648c-128">Relatert oppsett</span><span class="sxs-lookup"><span data-stu-id="7648c-128">Related setup</span></span>
<span data-ttu-id="7648c-129">Dette oppsettet er ikke spesifikk for økonomijournaler, men vil garantere at dataregistrering er riktig og enkel.</span><span class="sxs-lookup"><span data-stu-id="7648c-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="7648c-130">Hovedkonto</span><span class="sxs-lookup"><span data-stu-id="7648c-130">Main account</span></span>

<span data-ttu-id="7648c-131">Hovedkontoen oppsettet gir mange muligheter til økonomijournalen behandling:</span><span class="sxs-lookup"><span data-stu-id="7648c-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="7648c-132">**DK-krav** – Bruk dette alternativet hvis en hovedkontoen er begrenset til debet- eller kredittransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="7648c-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="7648c-133">Oppsettet kontrolleres når en journal er godkjent eller postert.</span><span class="sxs-lookup"><span data-stu-id="7648c-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="7648c-134">**Standard motkonto**</span><span class="sxs-lookup"><span data-stu-id="7648c-134">**Default offset account**</span></span>
-   <span data-ttu-id="7648c-135">**Suspendert** – Suspendere en hovedkonto for dataregistrering på tvers av alle firmaer eller for et bestemt firma / juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="7648c-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="7648c-136">**Ikke tillat manuell registrering** – Hindre at brukere manuelt angir en verdi for kontoen i journaler.</span><span class="sxs-lookup"><span data-stu-id="7648c-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="7648c-137">**Standard / valider valutakoder**</span><span class="sxs-lookup"><span data-stu-id="7648c-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="7648c-138">**Overstyring for juridisk enhet** – Dette oppsettet er spesifikk for definert firma / juridisk enhet:</span><span class="sxs-lookup"><span data-stu-id="7648c-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="7648c-139">**Standard / Valider merverdiavgift**</span><span class="sxs-lookup"><span data-stu-id="7648c-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="7648c-140">**Standarddimensjon** – **Ikke fast** eller **Fast verdi**.</span><span class="sxs-lookup"><span data-stu-id="7648c-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="7648c-141">**Fast verdi** vil bidra til å garantere at alle posteringer for denne hovedkontoen alltid bruker en dimensjonsverdi som er definert som **Fast**.</span><span class="sxs-lookup"><span data-stu-id="7648c-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="7648c-142">**Posteringsvalidering**</span><span class="sxs-lookup"><span data-stu-id="7648c-142">**Posting validation**</span></span>
    -   <span data-ttu-id="7648c-143">**Brukervalidering** – Dette alternativet styrer hvilke brukere som har tillatelse til å postere til en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="7648c-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="7648c-144">**Validering av posteringstype** – Dette alternativet styrer hvilke posteringstyper som er tillatt for en hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="7648c-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="7648c-145">Regnskapsstrukturer og strukturer for avanserte regler</span><span class="sxs-lookup"><span data-stu-id="7648c-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="7648c-146">Regnskapsstrukturer og strukturer for avanserte regler er svært viktige for å garantere at dataene som er nødvendige for økonomisk rapportering og sporing av ytelse, blir registrert under behandling av økonomijournalen og eventuell dokumentasjon.</span><span class="sxs-lookup"><span data-stu-id="7648c-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="7648c-147">Regnskapsstrukturer og strukturer for avanserte regler lar deg tilpasse dataregistreringsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="7648c-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="7648c-148">Du kan tillate dataregistrering bare for finansdimensjoner som er relevante i hvert tilfelle, og kan også sikre at obligatorisk og riktig data alltid registreres.</span><span class="sxs-lookup"><span data-stu-id="7648c-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="7648c-149">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="7648c-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="7648c-150">[Planlegging: kontoplan](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7648c-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="7648c-151">Opprette avanserte regler for journaler</span><span class="sxs-lookup"><span data-stu-id="7648c-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="7648c-152">Opprette en journaloppføring ved hjelp av en mal</span><span class="sxs-lookup"><span data-stu-id="7648c-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="7648c-153">Opprette og validere journaler</span><span class="sxs-lookup"><span data-stu-id="7648c-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="7648c-154">Postere periodiske journaler</span><span class="sxs-lookup"><span data-stu-id="7648c-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="7648c-155">Behandle finansfordelingsjournal</span><span class="sxs-lookup"><span data-stu-id="7648c-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



