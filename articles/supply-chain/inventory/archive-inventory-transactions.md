---
title: Arkivere beholdningstransaksjoner
description: Dette emnet beskriver hvordan du arkiverer lagertransaksjonsdata for å forbedre systemytelsen.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: bacc27c1a9066892c51110d28ba9a2ad26bebe77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839301"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="129b7-103">Arkivere beholdningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="129b7-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="129b7-104">Over tid vil lagertransaksjonstabellen (`InventTrans`) fortsette å vokse og bruke mer databaseplass.</span><span class="sxs-lookup"><span data-stu-id="129b7-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="129b7-105">Spørringer som opprettes mot tabellen, vil derfor gradvis gå saktere.</span><span class="sxs-lookup"><span data-stu-id="129b7-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="129b7-106">Dette emnet beskriver hvordan du kan bruke funksjonen *Arkiv for lagertransaksjoner* til å arkivere data om lagertransaksjoner for å forbedre systemytelsen.</span><span class="sxs-lookup"><span data-stu-id="129b7-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="129b7-107">Bare økonomisk oppdaterte lagertransaksjoner kan arkiveres i en valgt lukket finansperiode.</span><span class="sxs-lookup"><span data-stu-id="129b7-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="129b7-108">Hvis du vil arkivere, må økonomisk oppdaterte utgående lagertransaksjoner ha avgangsstatusen *Solgt*, og innkommende lagertransaksjoner må ha tilgangsstatusen *Kjøpt*.</span><span class="sxs-lookup"><span data-stu-id="129b7-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="129b7-109">Når du arkiverer lagertransaksjoner, flyttes alle relaterte transaksjoner til tabellen `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="129b7-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="129b7-110">Lageravgangstransaksjoner og lagermottakstransaksjoner arkiveres separat, basert på kombinasjonen av vare-IDen (`itemId`) og lagerdimensjons-ID (`inventDimId`), og de settes inn i den summerte avgangen og summerte mottakstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="129b7-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="129b7-111">Hvis en kombinasjon av `itemId` og `inventDimId` bare inneholder én mottaks- eller avgangstransaksjon, blir ikke transaksjonen arkivert.</span><span class="sxs-lookup"><span data-stu-id="129b7-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="129b7-112">Aktivere funksjonen i systemet</span><span class="sxs-lookup"><span data-stu-id="129b7-112">Turn on the feature in your system</span></span>

<span data-ttu-id="129b7-113">Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Arkiv for lagertransaksjoner*.</span><span class="sxs-lookup"><span data-stu-id="129b7-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="129b7-114">Ting du bør vurdere før du arkiverer lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="129b7-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="129b7-115">Før du arkiverer lagertransaksjoner, bør du vurdere følgende forretningsscenarioer, fordi de vil bli påvirket av operasjonen:</span><span class="sxs-lookup"><span data-stu-id="129b7-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="129b7-116">Når du kontrollerer lagertransaksjoner fra tilknyttede dokumenter, for eksempel bestillingslinjer, vises de som arkivert.</span><span class="sxs-lookup"><span data-stu-id="129b7-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="129b7-117">Hvis du vil gå gjennom de arkiverte transaksjonene, må du gå til **Lagerstyring \> Periodiske oppgaver \> Opprydding \> Arkiv for lagertransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="129b7-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="129b7-118">Lagerlukking kan ikke avbrytes for arkiverte perioder.</span><span class="sxs-lookup"><span data-stu-id="129b7-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="129b7-119">Før du kan avbryte en lagerlukking, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.</span><span class="sxs-lookup"><span data-stu-id="129b7-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="129b7-120">Standard kostnadskonvertering kan ikke utføres for arkiverte perioder.</span><span class="sxs-lookup"><span data-stu-id="129b7-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="129b7-121">Før du kan utføre standard kostnadskonvertering, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.</span><span class="sxs-lookup"><span data-stu-id="129b7-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="129b7-122">Lagerrapporter som kommer fra lagertransaksjoner, vil påvirkes når du arkiverer lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="129b7-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="129b7-123">Disse rapportene omfatter rapporten for aldersfordeling for lager og lagerverdirapporter.</span><span class="sxs-lookup"><span data-stu-id="129b7-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="129b7-124">Lagerprognoser kan bli påvirket hvis de kjøres i løpet av arkiverte perioders tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="129b7-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="129b7-125">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="129b7-125">Prerequisites</span></span>

<span data-ttu-id="129b7-126">Lagertransaksjoner kan bare arkiveres i perioder der følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="129b7-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="129b7-127">Finansperioden må være avsluttet.</span><span class="sxs-lookup"><span data-stu-id="129b7-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="129b7-128">Lagerlukking må kjøres på eller etter til-periodedatoen for arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="129b7-129">Perioden må være minst ett år før fra-periodedatoen til arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="129b7-130">Det må ikke finnes eksisterende lagerberegninger.</span><span class="sxs-lookup"><span data-stu-id="129b7-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="129b7-131">Arkivere beholdningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="129b7-131">Archive inventory transactions</span></span>

<span data-ttu-id="129b7-132">Hvis du vil arkivere lagertransaksjoner, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="129b7-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="129b7-133">Gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding** \> **Arkiv for lagertransaksjon**.</span><span class="sxs-lookup"><span data-stu-id="129b7-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="129b7-134">Siden **Arkiv for lagertransaksjoner** vises med en liste over arkiverte prosessposter.</span><span class="sxs-lookup"><span data-stu-id="129b7-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="129b7-135">![Siden Arkiv for lagertransaksjoner](media/archive-inventory-empty.png "Siden Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="129b7-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="129b7-136">Velg **Arkiv for lagertransaksjoner** på handlingssiden for å opprette et arkiv for lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="129b7-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="129b7-137">I dialogboksen **Arkiv for lagertransaksjoner** angir du følgende feilt i hurtigfanen **Parametere**:</span><span class="sxs-lookup"><span data-stu-id="129b7-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="129b7-138">**Fra-dato i lukket finansperiode** – Velg den tidligste transaksjonsdatoen som skal tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="129b7-139">**Til-dato i lukket finansperiode** – Velg den seneste transaksjonsdatoen som skal tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="129b7-140">![Dialgoboksen Arkiv for lagertransaksjoner](media/archive-inventory-dates.png "Dialgoboksen Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="129b7-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="129b7-141">Bare perioder som oppfyller [forutsetningene](#prerequisites), vil være tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="129b7-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="129b7-142">Definer detaljer for satsvis behandling i hurtigfanen **Kjør i bakgrunnen** etter behov.</span><span class="sxs-lookup"><span data-stu-id="129b7-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="129b7-143">Følg de vanlige trinnene for satsvise jobber i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="129b7-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="129b7-144">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="129b7-144">Select **OK**.</span></span>
1. <span data-ttu-id="129b7-145">Du får en melding som ber deg om å bekrefte at du ønsker å fortsette.</span><span class="sxs-lookup"><span data-stu-id="129b7-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="129b7-146">Les meldingen nøye, og velg deretter **Ja** hvis du vil fortsette.</span><span class="sxs-lookup"><span data-stu-id="129b7-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="129b7-147">Du mottar en melding som angir at arkivjobben for lagertransaksjoner er lagt til i den satsvise køen.</span><span class="sxs-lookup"><span data-stu-id="129b7-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="129b7-148">Jobben vil nå begynne å arkivere lagertransaksjoner fra den valgte perioden.</span><span class="sxs-lookup"><span data-stu-id="129b7-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="129b7-149">Vis arkiverte lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="129b7-149">View archived inventory transactions</span></span>

<span data-ttu-id="129b7-150">Siden **Arkiv for lagertransaksjoner** viser din fullstendige arkiveringshistorikk.</span><span class="sxs-lookup"><span data-stu-id="129b7-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="129b7-151">Hver rad i rutenettet viser informasjon som datoen da arkivet ble opprettet, brukeren som opprettet den og statusen den ble opprettet på.</span><span class="sxs-lookup"><span data-stu-id="129b7-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="129b7-152">![Arkivere historikk på siden Arkiv for lagertransaksjoner](media/archive-inventory-full.png "Arkivere historikk på siden Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="129b7-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="129b7-153">I rullegardinlisten øverst på siden velger du en av følgende verdier for å filtrere arkivene som vises i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="129b7-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="129b7-154">**Aktive** – Vis bare aktive arkiver, ikke tilbakeførte arkiver.</span><span class="sxs-lookup"><span data-stu-id="129b7-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="129b7-155">**Alle** – Vis alle arkiver, både aktive og tilbakeførte.</span><span class="sxs-lookup"><span data-stu-id="129b7-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="129b7-156">Følgende informasjon vises for hvert arkiv i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="129b7-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="129b7-157">**Aktive** – En hake angir at arkivet er aktivt.</span><span class="sxs-lookup"><span data-stu-id="129b7-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="129b7-158">**Fra-dato** – Datoen for den eldste transaksjonen som kan tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="129b7-159">**Til-dato** – Datoen for den yngste transaksjonen som kan tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="129b7-160">**Planlagt av** – Brukerkontoen som opprettet arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="129b7-161">**Utført** – Datoen da arkivet ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="129b7-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="129b7-162">**Tilbakeført** – En hake angir at arkivet er tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="129b7-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="129b7-163">**Stopp gjeldende oppdatering** – En hake angir at arkivering pågår, men at den er stoppet midlertidig.</span><span class="sxs-lookup"><span data-stu-id="129b7-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="129b7-164">**Tilstand** – Behandlingsstatusen til arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="129b7-165">De mulige verdiene er *Venter*, *Pågår* og *Avsluttet*.</span><span class="sxs-lookup"><span data-stu-id="129b7-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="129b7-166">Verktøylinjen over rutenettet inneholder følgende knapper som du kan bruke til å arbeide med et valgt arkiv:</span><span class="sxs-lookup"><span data-stu-id="129b7-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="129b7-167">**Arkiverte transaksjoner** – Vis alle detaljene i det valgte arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="129b7-168">Siden **Arkiverte transaksjoner** vises med alle transaksjonene i arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="129b7-169">![Siden Arkiverte transaksjoner](media/archive-inventory-transactions.png "Siden Arkiverte transaksjoner")</span><span class="sxs-lookup"><span data-stu-id="129b7-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="129b7-170">Hvis du vil vise mer informasjon om en bestemt transaksjon på siden **Arkiverte transaksjoner**, kan du velge den i rutenettet og deretter velge **Arkiverte transaksjonsdetaljer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="129b7-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="129b7-171">Detaljsiden **Arkiverte transaksjoner** som vises, viser informasjon som finanspostering, relaterte underregnskapsreferanser og finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="129b7-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="129b7-172">**Stanse arkivering midlertidig** – Stans et valgt arkiv midlertidig som behandles.</span><span class="sxs-lookup"><span data-stu-id="129b7-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="129b7-173">Den midlertidige stansen aktiveres bare etter at arkiveringsoppgaven er generert.</span><span class="sxs-lookup"><span data-stu-id="129b7-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="129b7-174">Det kan derfor ta litt tid før den midlertidige stansen trer i kraft.</span><span class="sxs-lookup"><span data-stu-id="129b7-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="129b7-175">Hvis et arkiv er stoppet midlertidig, vises det en hake i feltet **Stopp gjeldende oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="129b7-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="129b7-176">**Fortsett arkivering** – Fortsett behandling for et valgt arkiv som midlertidig er stanset.</span><span class="sxs-lookup"><span data-stu-id="129b7-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="129b7-177">**Tilbakefør** – Tilbakefør det valgte arkivet.</span><span class="sxs-lookup"><span data-stu-id="129b7-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="129b7-178">Du kan bare tilbakeføre et arkiv hvis feltet **Tilstand** er satt til *Avsluttet*.</span><span class="sxs-lookup"><span data-stu-id="129b7-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="129b7-179">Hvis et arkiv er tilbakeført, vises det en hake i feltet **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="129b7-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
