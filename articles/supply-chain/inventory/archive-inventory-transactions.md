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
ms.openlocfilehash: b740da1a8a349f4a1a80b41bf717c388fd3db0c0
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881838"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="0d38b-103">Arkivere beholdningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0d38b-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0d38b-104">Over tid vil lagertransaksjonstabellen (`InventTrans`) fortsette å vokse og bruke mer databaseplass.</span><span class="sxs-lookup"><span data-stu-id="0d38b-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="0d38b-105">Spørringer som opprettes mot tabellen, vil derfor gradvis gå saktere.</span><span class="sxs-lookup"><span data-stu-id="0d38b-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="0d38b-106">Dette emnet beskriver hvordan du kan bruke funksjonen *Arkiv for lagertransaksjoner* til å arkivere data om lagertransaksjoner for å forbedre systemytelsen.</span><span class="sxs-lookup"><span data-stu-id="0d38b-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="0d38b-107">Bare økonomisk oppdaterte lagertransaksjoner kan arkiveres i en valgt lukket finansperiode.</span><span class="sxs-lookup"><span data-stu-id="0d38b-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="0d38b-108">Hvis du vil arkivere, må økonomisk oppdaterte utgående lagertransaksjoner ha avgangsstatusen *Solgt*, og innkommende lagertransaksjoner må ha tilgangsstatusen *Kjøpt*.</span><span class="sxs-lookup"><span data-stu-id="0d38b-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="0d38b-109">Når du arkiverer lagertransaksjoner, flyttes alle relaterte transaksjoner til tabellen `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="0d38b-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="0d38b-110">Lageravgangstransaksjoner og lagermottakstransaksjoner arkiveres separat, basert på kombinasjonen av vare-IDen (`itemId`) og lagerdimensjons-ID (`inventDimId`), og de settes inn i den summerte avgangen og summerte mottakstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0d38b-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="0d38b-111">Hvis en kombinasjon av `itemId` og `inventDimId` bare inneholder én mottaks- eller avgangstransaksjon, blir ikke transaksjonen arkivert.</span><span class="sxs-lookup"><span data-stu-id="0d38b-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="0d38b-112">Aktivere funksjonen i systemet</span><span class="sxs-lookup"><span data-stu-id="0d38b-112">Turn on the feature in your system</span></span>

<span data-ttu-id="0d38b-113">Hvis systemet ikke allerede inneholder funksjonene som er beskrevet i dette emnet, kan du gå til [Funksjonsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Arkiv for lagertransaksjoner*.</span><span class="sxs-lookup"><span data-stu-id="0d38b-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span> <span data-ttu-id="0d38b-114">Merk deg at denne funksjonen ikke kan deaktiveres når den først er aktivert.</span><span class="sxs-lookup"><span data-stu-id="0d38b-114">Note that this feature cannot be disabled once it has been enabled.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="0d38b-115">Ting du bør vurdere før du arkiverer lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0d38b-115">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="0d38b-116">Før du arkiverer lagertransaksjoner, bør du vurdere følgende forretningsscenarioer, fordi de vil bli påvirket av operasjonen:</span><span class="sxs-lookup"><span data-stu-id="0d38b-116">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="0d38b-117">Når du kontrollerer lagertransaksjoner fra tilknyttede dokumenter, for eksempel bestillingslinjer, vises de som arkivert.</span><span class="sxs-lookup"><span data-stu-id="0d38b-117">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="0d38b-118">Hvis du vil gå gjennom de arkiverte transaksjonene, må du gå til **Lagerstyring \> Periodiske oppgaver \> Opprydding \> Arkiv for lagertransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0d38b-118">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="0d38b-119">Lagerlukking kan ikke avbrytes for arkiverte perioder.</span><span class="sxs-lookup"><span data-stu-id="0d38b-119">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="0d38b-120">Før du kan avbryte en lagerlukking, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.</span><span class="sxs-lookup"><span data-stu-id="0d38b-120">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="0d38b-121">Standard kostnadskonvertering kan ikke utføres for arkiverte perioder.</span><span class="sxs-lookup"><span data-stu-id="0d38b-121">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="0d38b-122">Før du kan utføre standard kostnadskonvertering, må du tilbakeføre lagertransaksjonsarkivet for den aktuelle perioden.</span><span class="sxs-lookup"><span data-stu-id="0d38b-122">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="0d38b-123">Lagerrapporter som kommer fra lagertransaksjoner, vil påvirkes når du arkiverer lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0d38b-123">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="0d38b-124">Disse rapportene omfatter rapporten for aldersfordeling for lager og lagerverdirapporter.</span><span class="sxs-lookup"><span data-stu-id="0d38b-124">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="0d38b-125">Lagerprognoser kan bli påvirket hvis de kjøres i løpet av arkiverte perioders tidshorisont.</span><span class="sxs-lookup"><span data-stu-id="0d38b-125">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0d38b-126">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="0d38b-126">Prerequisites</span></span>

<span data-ttu-id="0d38b-127">Lagertransaksjoner kan bare arkiveres i perioder der følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="0d38b-127">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="0d38b-128">Finansperioden må være avsluttet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-128">The ledger period must be closed.</span></span>
- <span data-ttu-id="0d38b-129">Lagerlukking må kjøres på eller etter til-periodedatoen for arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-129">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="0d38b-130">Perioden må være minst ett år før fra-periodedatoen til arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-130">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="0d38b-131">Det må ikke finnes eksisterende lagerberegninger.</span><span class="sxs-lookup"><span data-stu-id="0d38b-131">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="0d38b-132">Arkivere beholdningstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0d38b-132">Archive inventory transactions</span></span>

<span data-ttu-id="0d38b-133">Hvis du vil arkivere lagertransaksjoner, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="0d38b-133">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="0d38b-134">Gå til **Lagerstyring** \> **Periodiske oppgaver** \> **Opprydding** \> **Arkiv for lagertransaksjon**.</span><span class="sxs-lookup"><span data-stu-id="0d38b-134">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="0d38b-135">Siden **Arkiv for lagertransaksjoner** vises med en liste over arkiverte prosessposter.</span><span class="sxs-lookup"><span data-stu-id="0d38b-135">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="0d38b-136">![Siden Arkiv for lagertransaksjoner](media/archive-inventory-empty.png "Siden Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="0d38b-136">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="0d38b-137">Velg **Arkiv for lagertransaksjoner** på handlingssiden for å opprette et arkiv for lagertransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0d38b-137">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="0d38b-138">I dialogboksen **Arkiv for lagertransaksjoner** angir du følgende feilt i hurtigfanen **Parametere**:</span><span class="sxs-lookup"><span data-stu-id="0d38b-138">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="0d38b-139">**Fra-dato i lukket finansperiode** – Velg den tidligste transaksjonsdatoen som skal tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-139">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="0d38b-140">**Til-dato i lukket finansperiode** – Velg den seneste transaksjonsdatoen som skal tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-140">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="0d38b-141">![Dialgoboksen Arkiv for lagertransaksjoner](media/archive-inventory-dates.png "Dialgoboksen Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="0d38b-141">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0d38b-142">Bare perioder som oppfyller [forutsetningene](#prerequisites), vil være tilgjengelige for valg.</span><span class="sxs-lookup"><span data-stu-id="0d38b-142">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="0d38b-143">Definer detaljer for satsvis behandling i hurtigfanen **Kjør i bakgrunnen** etter behov.</span><span class="sxs-lookup"><span data-stu-id="0d38b-143">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="0d38b-144">Følg de vanlige trinnene for satsvise jobber i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0d38b-144">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="0d38b-145">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d38b-145">Select **OK**.</span></span>
1. <span data-ttu-id="0d38b-146">Du får en melding som ber deg om å bekrefte at du ønsker å fortsette.</span><span class="sxs-lookup"><span data-stu-id="0d38b-146">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="0d38b-147">Les meldingen nøye, og velg deretter **Ja** hvis du vil fortsette.</span><span class="sxs-lookup"><span data-stu-id="0d38b-147">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="0d38b-148">Du mottar en melding som angir at arkivjobben for lagertransaksjoner er lagt til i den satsvise køen.</span><span class="sxs-lookup"><span data-stu-id="0d38b-148">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="0d38b-149">Jobben vil nå begynne å arkivere lagertransaksjoner fra den valgte perioden.</span><span class="sxs-lookup"><span data-stu-id="0d38b-149">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="0d38b-150">Vis arkiverte lagertransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0d38b-150">View archived inventory transactions</span></span>

<span data-ttu-id="0d38b-151">Siden **Arkiv for lagertransaksjoner** viser din fullstendige arkiveringshistorikk.</span><span class="sxs-lookup"><span data-stu-id="0d38b-151">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="0d38b-152">Hver rad i rutenettet viser informasjon som datoen da arkivet ble opprettet, brukeren som opprettet den og statusen den ble opprettet på.</span><span class="sxs-lookup"><span data-stu-id="0d38b-152">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="0d38b-153">![Arkivere historikk på siden Arkiv for lagertransaksjoner](media/archive-inventory-full.png "Arkivere historikk på siden Arkiv for lagertransaksjoner")</span><span class="sxs-lookup"><span data-stu-id="0d38b-153">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="0d38b-154">I rullegardinlisten øverst på siden velger du en av følgende verdier for å filtrere arkivene som vises i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="0d38b-154">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="0d38b-155">**Aktive** – Vis bare aktive arkiver, ikke tilbakeførte arkiver.</span><span class="sxs-lookup"><span data-stu-id="0d38b-155">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="0d38b-156">**Alle** – Vis alle arkiver, både aktive og tilbakeførte.</span><span class="sxs-lookup"><span data-stu-id="0d38b-156">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="0d38b-157">Følgende informasjon vises for hvert arkiv i rutenettet:</span><span class="sxs-lookup"><span data-stu-id="0d38b-157">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="0d38b-158">**Aktive** – En hake angir at arkivet er aktivt.</span><span class="sxs-lookup"><span data-stu-id="0d38b-158">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="0d38b-159">**Fra-dato** – Datoen for den eldste transaksjonen som kan tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-159">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="0d38b-160">**Til-dato** – Datoen for den yngste transaksjonen som kan tas med i arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-160">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="0d38b-161">**Planlagt av** – Brukerkontoen som opprettet arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-161">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="0d38b-162">**Utført** – Datoen da arkivet ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-162">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="0d38b-163">**Tilbakeført** – En hake angir at arkivet er tilbakeført.</span><span class="sxs-lookup"><span data-stu-id="0d38b-163">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="0d38b-164">**Stopp gjeldende oppdatering** – En hake angir at arkivering pågår, men at den er stoppet midlertidig.</span><span class="sxs-lookup"><span data-stu-id="0d38b-164">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="0d38b-165">**Tilstand** – Behandlingsstatusen til arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-165">**State** – The processing status of the archive.</span></span> <span data-ttu-id="0d38b-166">De mulige verdiene er *Venter*, *Pågår* og *Avsluttet*.</span><span class="sxs-lookup"><span data-stu-id="0d38b-166">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="0d38b-167">Verktøylinjen over rutenettet inneholder følgende knapper som du kan bruke til å arbeide med et valgt arkiv:</span><span class="sxs-lookup"><span data-stu-id="0d38b-167">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="0d38b-168">**Arkiverte transaksjoner** – Vis alle detaljene i det valgte arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-168">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="0d38b-169">Siden **Arkiverte transaksjoner** vises med alle transaksjonene i arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-169">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="0d38b-170">![Siden Arkiverte transaksjoner](media/archive-inventory-transactions.png "Siden Arkiverte transaksjoner")</span><span class="sxs-lookup"><span data-stu-id="0d38b-170">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="0d38b-171">Hvis du vil vise mer informasjon om en bestemt transaksjon på siden **Arkiverte transaksjoner**, kan du velge den i rutenettet og deretter velge **Arkiverte transaksjonsdetaljer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="0d38b-171">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="0d38b-172">Detaljsiden **Arkiverte transaksjoner** som vises, viser informasjon som finanspostering, relaterte underregnskapsreferanser og finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="0d38b-172">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="0d38b-173">**Stanse arkivering midlertidig** – Stans et valgt arkiv midlertidig som behandles.</span><span class="sxs-lookup"><span data-stu-id="0d38b-173">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="0d38b-174">Den midlertidige stansen aktiveres bare etter at arkiveringsoppgaven er generert.</span><span class="sxs-lookup"><span data-stu-id="0d38b-174">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="0d38b-175">Det kan derfor ta litt tid før den midlertidige stansen trer i kraft.</span><span class="sxs-lookup"><span data-stu-id="0d38b-175">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="0d38b-176">Hvis et arkiv er stoppet midlertidig, vises det en hake i feltet **Stopp gjeldende oppdatering**.</span><span class="sxs-lookup"><span data-stu-id="0d38b-176">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="0d38b-177">**Fortsett arkivering** – Fortsett behandling for et valgt arkiv som midlertidig er stanset.</span><span class="sxs-lookup"><span data-stu-id="0d38b-177">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="0d38b-178">**Tilbakefør** – Tilbakefør det valgte arkivet.</span><span class="sxs-lookup"><span data-stu-id="0d38b-178">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="0d38b-179">Du kan bare tilbakeføre et arkiv hvis feltet **Tilstand** er satt til *Avsluttet*.</span><span class="sxs-lookup"><span data-stu-id="0d38b-179">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="0d38b-180">Hvis et arkiv er tilbakeført, vises det en hake i feltet **Tilbakefør**.</span><span class="sxs-lookup"><span data-stu-id="0d38b-180">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
