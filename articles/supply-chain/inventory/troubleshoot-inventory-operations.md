---
title: Feilsøke lageroperasjoner
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med lageroperasjoner.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832064"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="1ef0f-103">Feilsøke lageroperasjoner</span><span class="sxs-lookup"><span data-stu-id="1ef0f-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ef0f-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med lageroperasjoner.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="1ef0f-105">Jeg finner ikke rullegardinboksen Arbeidsflyt for lagerjournaler.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-106">Issue description</span></span>

<span data-ttu-id="1ef0f-107">Du finner ikke rullegardinboksen **Arbeidsflyt** på journalsiden, eller relaterte arbeidsflytoperasjoner er ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="1ef0f-108">Dette problemet kan oppstå av tre årsaker, som beskrevet i underdelene nedenfor.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="1ef0f-109">Problemløsning 1</span><span class="sxs-lookup"><span data-stu-id="1ef0f-109">Issue resolution 1</span></span>

<span data-ttu-id="1ef0f-110">Hvis problemet gjelder alle brukere, kan årsaken være at godkjenningsarbeidsflyten ikke er tilordnet til journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="1ef0f-111">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="1ef0f-112">Gå til **Lagerstyring &gt; Oppsett &gt; Journalnavn &gt; Beholdning**.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="1ef0f-113">I listeruten velger du et journalnavn for å åpne innstillingene for den.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="1ef0f-114">I hurtigfanen **Generelt** angir du *Ja* for alternativet **Arbeidsflyt for godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="1ef0f-115">Hvis du blir bedt om å bekrefte endringen, velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="1ef0f-116">Velg arbeidsflyten du vil bruke for det valgte journalnavnet, i **Arbeidsflyt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="1ef0f-117">Problemløsning 2</span><span class="sxs-lookup"><span data-stu-id="1ef0f-117">Issue resolution 2</span></span>

<span data-ttu-id="1ef0f-118">Hvis arbeidsflyten bruker tilpasset kode, kan det oppstå problemer etter at du har oppgradert systemet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="1ef0f-119">**Send inn**-knappen kan for eksempel være nedtonet i journalarbeidsflyten, slik at du ikke kan velge den for å godkjenne en innsending.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="1ef0f-120">Hvis **Send inn**-knappen er nedtonet, kan arbeidsflyten ha blitt tilpasset, som betyr at metoden for arbeidsflyten, `canSubmitToWorkflow()` i `FormDataUtil`, har blitt utvidet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="1ef0f-121">Du kan rette dette problemet ved å endre hvordan du utvider metoden for `canSubmitToWorkflow()`, slik at den bruker strukturen i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="1ef0f-122">Problemløsning 3</span><span class="sxs-lookup"><span data-stu-id="1ef0f-122">Issue resolution 3</span></span>

<span data-ttu-id="1ef0f-123">Hvis problemet bare gjelder noen få bestemte brukere, kan det hende at disse brukerne ikke har sikkerhetsrettighetene som kreves for å kjøre arbeidsflytoperasjoner på lagerjournaler.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="1ef0f-124">Kontroller at hver berørte bruker har sikkerhetsrettigheten *Vedlikehold lagerjournalarbeidsflyt*.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="1ef0f-125">Denne rettigheten er som standard tilordnet til en plikt med samme navn, og denne plikten brukes på rollene *Lagerarbeider* og *Lagersjef*.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="1ef0f-126">Lagerjournalen forblir låst av systemet, og den satsvise arbeidsflytjobben fungerer ikke.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-127">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-127">Issue description</span></span>

<span data-ttu-id="1ef0f-128">En av lagerjournalene er låst av en eller annen operasjon og blir ikke frigitt.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="1ef0f-129">Hvis det for eksempel oppstår en ukjent feil under postering (som er en systemlåst operasjon), kan det hende at journalen forblir låst av systemet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="1ef0f-130">I dette tilfellet vil behandlingsprogrammet for arbeidselement for arbeidsflyt generere en feil mens det foretar låsvalidering.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ef0f-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-131">Issue resolution</span></span>

<span data-ttu-id="1ef0f-132">Logg deg på SQL Server-forekomsten for Supply Chain Management, og kontroller om **InventJournalTable.SystemBlocked** er satt til *1*.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="1ef0f-133">Hvis den er det, må du kontrollere at journalen ikke er låst, og deretter tilbakestille **InventJournalTable.SystemBlocked** til *0*.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="1ef0f-134">Lagerjournalarbeidsflyten min blir aldri fullført, og journalen kan ikke redigeres eller posteres.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-135">Issue description</span></span>

<span data-ttu-id="1ef0f-136">Når du har sendt inn en arbeidsflyt for journalgodkjenning, slutter arbeidsflytbehandlingen å svare, og du kan ikke redigere eller behandle journalene.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ef0f-137">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-137">Issue resolution</span></span>

<span data-ttu-id="1ef0f-138">Det er flere årsaker til at arbeidsflytbehandling kanskje ikke fullføres.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="1ef0f-139">Se etter følgende problemer:</span><span class="sxs-lookup"><span data-stu-id="1ef0f-139">Check for the following issues:</span></span>

- <span data-ttu-id="1ef0f-140">Gå til **Lagerstyring &gt; Oppsett &gt; Arbeidsflyter for lagerstyring**, og gå gjennom konfigurasjonen til den berørte arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="1ef0f-141">Hvis du vil ha mer informasjon, kan du se [Godkjenningsarbeidsflyter for lagerjournal](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="1ef0f-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="1ef0f-142">Arbeidsflyten kan bli utsatt for et unntak eller en feil.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="1ef0f-143">Gå gjennom loggen for arbeidselement i den berørte arbeidsflyten for å se om den omfatter en programfeil som avslutter arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="1ef0f-144">Lagerjournalen kan bare oppdateres eller redigeres hvis den er godkjent.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="1ef0f-145">Hvis tilbakekalling er aktiv, kan du prøve å tilbakekalle journalen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="1ef0f-146">Kjøring av den satsvise arbeidsflytjobben kan bli avbrutt av flere årsaker.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="1ef0f-147">Noen av disse årsakene kan være forårsaket av problemer med arbeidsflytrammeverket.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="1ef0f-148">Betingelser for lagerjournalarbeidsflyt gjelder bare på journalnivå, ikke på linjenivå</span><span class="sxs-lookup"><span data-stu-id="1ef0f-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-149">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-149">Issue description</span></span>

<span data-ttu-id="1ef0f-150">Du kan få dette problemet hvis du for eksempel prøver å definere en betingelse for lagerjournalarbeidsflyt for kostbeløpet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="1ef0f-151">Du definerer betingelsen slik at trinn 1 bare kjøres når kostbeløpet er mindre enn 100.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="1ef0f-152">Deretter definerer du en ny betingelse slik at trinn 2 bare kjøres når kostbeløpet er større enn eller lik 100.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="1ef0f-153">Når arbeidsflyten deretter kjøres, viser arbeidsflytloggen deretter bare én linje, og den første betingelsen evalueres alltid som *sann*, uavhengig av verdien som sendes.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="1ef0f-154">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-154">Issue workaround</span></span>

<span data-ttu-id="1ef0f-155">I gjeldende utgivelse gjelder betingelser for lagerarbeidsflyt bare på journalnivå, ikke på linjenivå.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="1ef0f-156">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-156">This behavior is by design.</span></span> <span data-ttu-id="1ef0f-157">Det anbefales at du bare angir betingelseskriteriene for attributter på journalnivå.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="1ef0f-158">Filterruten på siden Beholdningsliste filtrerer ikke resultatene slik jeg forventer.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-159">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-159">Issue description</span></span>

<span data-ttu-id="1ef0f-160">Filtrene i filterruten på siden **Beholdningsliste**  filtrerer ikke resultater slik du forventer.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ef0f-161">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-161">Issue resolution</span></span>

<span data-ttu-id="1ef0f-162">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-162">This behavior is by design.</span></span>

<span data-ttu-id="1ef0f-163">Siden  **Beholdningsliste**  er satt sammen fra en detaljert lagerbeholdningstabell som inkluderer alle tilgjengelige dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="1ef0f-164">Listen på denne siden er imidlertid et sammendrag.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="1ef0f-165">Derfor kan den kombinere rader fra kildetabellen ved å samle verdier i henhold til dimensjonene som vises.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="1ef0f-166">Filtre som er definert i filterruten, gjelder for kildetabellen, ikke for den aggregerte listen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="1ef0f-167">Denne virkemåten kan av og til gi uventede resultater, som vist i [disse eksemplene](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="1ef0f-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="1ef0f-168"> [Filtrene som oppgis i rutenettet](inventory-on-hand-list.md#grid-filters), \*gjelder* imidlertid for den aggregerte listen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="1ef0f-169">Disse filtrene inkluderer både hurtigfilteret øverst i rutenettet og filteret for hver kolonneoverskrift.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="1ef0f-170">Enheten og enhetsantallet fungerer ikke riktig i lagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-171">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-171">Issue description</span></span>

<span data-ttu-id="1ef0f-172">Ett eller begge av følgende problemer kan oppstå når du arbeider med enheter og antall i en lagerjournal:</span><span class="sxs-lookup"><span data-stu-id="1ef0f-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="1ef0f-173">Du ser ikke enheter eller enhetsantall i lagerjournalen mens en omregningsenhet er definert for det frigitte produktet, og du kan ikke endre enheten i lagerjournalen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="1ef0f-174">Du ser feltene **Antall** og **Enhet** i lagerjournalen, men ikke feltet **Enhetsantall**.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="1ef0f-175">Hvis du endrer enheten, angir et antall og posterer journalen, viser journalen fortsatt den opprinnelige måleenheten for dette antallet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ef0f-176">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-176">Issue resolution</span></span>

<span data-ttu-id="1ef0f-177">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="1ef0f-178">I arbeidsområdet **Funksjonsbehandling** må du kontrollere at funksjonen *Bruke måleenhet og enhetsantall i lagerjournaler* er aktivert.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="1ef0f-179">Denne funksjonen legger til feltene **Enhet** og **Enhetsantall** i journalen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="1ef0f-180">Etter at funksjonen er aktivert, bruker du feltene **Antall**, **Enhetsantall** og **Enhet** på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="1ef0f-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="1ef0f-181">**Antall** – Angi antallet ved å bruke standardenheten som er definert for det frigitte produktet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="1ef0f-182">Selve standardenheten vises imidlertid ikke her.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="1ef0f-183">Hvis det defineres en omregning mellom standardenheten og enheten som er valgt i **Enhet**-feltet, oppdateres **Antall**-feltet automatisk basert på valgene i feltene **Enhetsantall** og **Enhet**.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="1ef0f-184">**Enhetsantall** – Angi antallet ved å bruke enheten som er valgt i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="1ef0f-185">**Enhet** – Velg enheten som skal brukes på verdien i **Enhetsantall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="1ef0f-186">Jeg får følgende feilmelding: «Maksimalt antall desimaler for lagerføringsenheten er 0.»</span><span class="sxs-lookup"><span data-stu-id="1ef0f-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1ef0f-187">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1ef0f-187">Issue description</span></span>

<span data-ttu-id="1ef0f-188">Når du prøver å postere en lagertransaksjon eller lagerreservasjon, får du følgende feilmelding: «Maksimalt antall desimaler for lagerføringsenheten er 0.»</span><span class="sxs-lookup"><span data-stu-id="1ef0f-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="1ef0f-189">Dette problemet oppstår når lagertransaksjonsantallet er angitt som en desimalverdi som er under presisjonsnivået som feltet støtter.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="1ef0f-190">Et antall på *0,5* er for eksempel angitt for en lagertransaksjon, men bare heltallsantall støttes.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="1ef0f-191">Verdien må derfor være *1* i stedet for *0,5*.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1ef0f-192">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1ef0f-192">Issue resolution</span></span>

1. <span data-ttu-id="1ef0f-193">Kjør følgende skript på SQL Server-forekomsten for å avrunde antall i lagertransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="1ef0f-194">Dette skriptet retter verdiene i **inventTrans**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="1ef0f-195">Kjør en konsekvenskontroll for lagerbeholdning der alternativet **Rett feil** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="1ef0f-196">Denne kontrollen retter verdiene i **inventSum**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ef0f-197">Det anbefales på det sterkeste at du redigerer skriptet nøye etter behov for miljøet, tester det i et testmiljø og kontrollerer de resulterende dataene før du kjører skriptet i et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="1ef0f-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]