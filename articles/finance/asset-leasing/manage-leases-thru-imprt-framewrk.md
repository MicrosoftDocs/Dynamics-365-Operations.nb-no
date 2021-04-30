---
title: Administrere leie via rammeverket for leieimport
description: Dette emnet forklarer hvordan du bruker rammeverket for leieimport til å justere flere leieavtaler samtidig.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseImportHeader
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 083adf0a4bb74ac65e6f8b5077f65c74eb3fa337
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880916"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="17f6e-103">Administrere leie via rammeverket for leieimport</span><span class="sxs-lookup"><span data-stu-id="17f6e-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17f6e-104">Dette emnet forklarer hvordan du bruker rammeverket for leieimport til å justere flere leieavtaler i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="17f6e-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="17f6e-105">Ved å bruke denne funksjonen kan du spare tid, og du kan også sikre mer nøyaktige justeringer ved å redusere faren for menneskelige feil.</span><span class="sxs-lookup"><span data-stu-id="17f6e-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="17f6e-106">I tillegg kan denne funksjonen koble Microsoft Dynamics 365 Finance sammen med eksterne dataenheter for å kunne laste opp data effektivt.</span><span class="sxs-lookup"><span data-stu-id="17f6e-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="17f6e-107">Følgende dataenheter kan brukes til å integrere aktivaleie med eksterne systemer:</span><span class="sxs-lookup"><span data-stu-id="17f6e-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="17f6e-108">Leieklargjøring</span><span class="sxs-lookup"><span data-stu-id="17f6e-108">Lease staging</span></span>
- <span data-ttu-id="17f6e-109">Klargjøring av betalingskontrakt</span><span class="sxs-lookup"><span data-stu-id="17f6e-109">Payment contract staging</span></span>
- <span data-ttu-id="17f6e-110">Klargjøring av fullbyrdelseskontrakt</span><span class="sxs-lookup"><span data-stu-id="17f6e-110">Executory contract staging</span></span>

<span data-ttu-id="17f6e-111">Du kan bruke importprosessen til å justere en leieavtale, oppdatere ikke-økonomisk informasjon eller legge til nye leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="17f6e-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="17f6e-112">Du kan vise og redigere leiedataene før du importerer dem.</span><span class="sxs-lookup"><span data-stu-id="17f6e-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="17f6e-113">Systemet kan kjøre følgende tre prosesser via leieimportserien.</span><span class="sxs-lookup"><span data-stu-id="17f6e-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="17f6e-114">Prosesstype</span><span class="sxs-lookup"><span data-stu-id="17f6e-114">Process type</span></span>  | <span data-ttu-id="17f6e-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="17f6e-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="17f6e-116">Legge til post</span><span class="sxs-lookup"><span data-stu-id="17f6e-116">Add record</span></span>    | <span data-ttu-id="17f6e-117">Overførte leieavtaler som har denne prosesstypen, oppretter en leieavtale i systemet.</span><span class="sxs-lookup"><span data-stu-id="17f6e-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="17f6e-118">Betalingsplanen må bekreftes manuelt, og journaloppføringen for opprinnelig føring må posteres manuelt etter overføringen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="17f6e-119">Oppdater post</span><span class="sxs-lookup"><span data-stu-id="17f6e-119">Update record</span></span> | <span data-ttu-id="17f6e-120">Overførte leieavtaler som har denne prosesstypen, oppdaterer feltverdier for en leieavtale som allerede finnes i systemet.</span><span class="sxs-lookup"><span data-stu-id="17f6e-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="17f6e-121">Bare feltene som er valgt på siden for **Oppdater feltvalg**, oppdateres.</span><span class="sxs-lookup"><span data-stu-id="17f6e-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="17f6e-122">Vi anbefaler at du velger ikke-finansielle felt på siden for **Oppdater feltvalg**, fordi denne prosesstypen ikke justerer leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="17f6e-123">Juster post</span><span class="sxs-lookup"><span data-stu-id="17f6e-123">Adjust record</span></span> | <span data-ttu-id="17f6e-124">Overførte leieavtaler som har denne prosesstypen, justerer leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="17f6e-125">Denne justeringen fører til en finansiell endring av leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="17f6e-126">Når leieavtalen er behandlet, oppretter systemet en ny betalingsplan ved å bruke de nye dataene fra leieimportserien.</span><span class="sxs-lookup"><span data-stu-id="17f6e-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="17f6e-127">Systemet bekrefter ikke betalingsplanen eller posterer justeringsjournaloppføringen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="17f6e-128">Når informasjonen er lastet opp via **Databehandling**-arbeidsområdet, åpner du siden **Importhode** (**Aktivaleie \> Rammeverk for import av leieavtale \> Importhode**).</span><span class="sxs-lookup"><span data-stu-id="17f6e-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="17f6e-129">Denne siden viser alle importer av de tre dataenhetene som ble vist tidligere.</span><span class="sxs-lookup"><span data-stu-id="17f6e-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="17f6e-130">Hvis du vil vise leieroppsamlingsdata før behandling kjøres, velger du **Oppsamlingsdata**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="17f6e-131">Med sammenligningsfunksjonen kan du sammenligne en post du skal importere, med den tilsvarende posten som allerede finnes i systemet.</span><span class="sxs-lookup"><span data-stu-id="17f6e-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="17f6e-132">Hvis du vil sammenligne en enkelt leieoppføring, velger du en leieavtale og deretter **Sammenlign**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="17f6e-133">Du bør fullføre dette trinnet for å generere en **Forskjeller**-rapport før du overfører leiepostene.</span><span class="sxs-lookup"><span data-stu-id="17f6e-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="17f6e-134">Sammenligningsfunksjonaliteten sammenligner verdiene i oppsamlingsdataene med verdiene for leieavtaler som for øyeblikket finnes i systemet.</span><span class="sxs-lookup"><span data-stu-id="17f6e-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="17f6e-135">Sammenligningsfunksjonaliteten fungerer ikke for leieavtaler som har prosesstypen **Legg til post**, fordi det ikke er noe å sammenligne mot denne leieavtalen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-135">The Compare functionality won't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="17f6e-136">Hvis du vil sammenligne flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Sammenlign**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Compare**.</span></span>

<span data-ttu-id="17f6e-137">For hver enhet kan du vise forskjellene mellom det som finnes i systemet, og det som finnes i oppsamlingstabellene.</span><span class="sxs-lookup"><span data-stu-id="17f6e-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="17f6e-138">Velg **Vis forskjeller** for hver enhet i oppsamlingstabellene.</span><span class="sxs-lookup"><span data-stu-id="17f6e-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="17f6e-139">Dialogboksen som vises, viser den gjeldende verdien og den foreslåtte oppsamlingsverdien.</span><span class="sxs-lookup"><span data-stu-id="17f6e-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="17f6e-140">Du kan også oppdatere oppsamlingsverdien ved å endre den i kolonnen **Ny verdi** og deretter velge valget for **Oppdater oppsamling**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="17f6e-141">Du kan validere leieavtaler for å sikre at postene kan hentes inn i systemet uten å introdusere feil.</span><span class="sxs-lookup"><span data-stu-id="17f6e-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="17f6e-142">Før en leieavtale overføres, kjører systemet flere valideringer for å sikre at posten blir importert.</span><span class="sxs-lookup"><span data-stu-id="17f6e-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="17f6e-143">Velg **Valider** for å validere en enkelt leieavtale.</span><span class="sxs-lookup"><span data-stu-id="17f6e-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="17f6e-144">Hvis du vil validere flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Valider**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Validate**.</span></span>

<span data-ttu-id="17f6e-145">Hvis du vil behandle en enkelt leieavtale, velger du å **overføre leieposter** på siden **Importhode**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="17f6e-146">Når en leieavtale overføres, utfører systemet handlingen som er angitt i **Prosesstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="17f6e-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="17f6e-147">Hvis du vil overføre flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Overfør**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-147">To migrate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic**, and select **Migrate**.</span></span>

<span data-ttu-id="17f6e-148">Når leieavtalene er sammenlignet, kan du kjøre en rapport for å vise forskjellene for hver leieavtale som er inkludert i import-IDen.</span><span class="sxs-lookup"><span data-stu-id="17f6e-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="17f6e-149">Hvis du vil kjøre rapporten for én leieavtale, velger du leieavtalen i oppsamlingsdataene, og deretter velger du **sammenlign og vis rapport \> rapport om forskjeller**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="17f6e-150">Hvis du vil sammenligne flere leieavtaler samtidig, går du til **Aktivaleie \> rammeverket for import av leieavtale \> Periodisk**, og deretter velger du **Sammenlign**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-150">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic** and select **Compare**.</span></span> 

## <a name="set-up-update-fields"></a><span data-ttu-id="17f6e-151">Definere oppdateringsfelt</span><span class="sxs-lookup"><span data-stu-id="17f6e-151">Set up update fields</span></span>

<span data-ttu-id="17f6e-152">Hvis du bruker rammeverket for import av leieavtale til å oppdatere leieavtaler, og prosesstypen er **Oppdater post**, kan du velge bestemte felt som skal oppdateres.</span><span class="sxs-lookup"><span data-stu-id="17f6e-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="17f6e-153">Gå til **Aktivaleie \> rammeverket for leieimport \> Oppsett \> Oppdater feltvalg**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="17f6e-154">På siden som vises, velger du feltene som skal oppdateres, og deretter velger du den grønne pilen for å flytte dem til listen for **Valgte felt**.</span><span class="sxs-lookup"><span data-stu-id="17f6e-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="17f6e-155">Bare felt i listen for **Valgte felt** kan oppdateres ved å bruke leieimportserien.</span><span class="sxs-lookup"><span data-stu-id="17f6e-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
