---
title: Feilsøke bestillinger
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med bestillinger.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e55974f65577170880e60095f1ba74ea7366e592
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834404"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="b1a33-103">Feilsøke bestillinger</span><span class="sxs-lookup"><span data-stu-id="b1a33-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="b1a33-104">Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med bestillinger.</span><span class="sxs-lookup"><span data-stu-id="b1a33-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="b1a33-105">En handling kan bare fullføres etter at linjenummeret er ferdig distribuert.</span><span class="sxs-lookup"><span data-stu-id="b1a33-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="b1a33-106">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="b1a33-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="b1a33-107">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="b1a33-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="b1a33-108">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="b1a33-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="b1a33-109">Når bestillinger importeres via databehandling, følger ikke bestillingslinjenumrene den økningen som er definert i systemparametere.</span><span class="sxs-lookup"><span data-stu-id="b1a33-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-110">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-110">Issue description</span></span>

<span data-ttu-id="b1a33-111">Som standard vil automatisk genererte linjenumre for bestillingslinjer som importeres via *Bestillingslinjer v2*-dataenheten, ikke bruke systemets linjenummerøkning som er angitt i systemparametere.</span><span class="sxs-lookup"><span data-stu-id="b1a33-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="b1a33-112">Hvis du oppretter en bestilling manuelt og legger til linjer via bruker grensesnittet, økes linjenumrene på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="b1a33-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="b1a33-113">Hvis du imidlertid bruker Data Management Framework (DMF), økes de ikke riktig.</span><span class="sxs-lookup"><span data-stu-id="b1a33-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="b1a33-114">Dette problemet oppstår fordi når du importerer linjer via DMF, hvis linjenumre ikke allerede er tilordnet i den importerte enheten, bruker systemet DMFs metode for å tilordne dem.</span><span class="sxs-lookup"><span data-stu-id="b1a33-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="b1a33-115">Denne metoden øker alltid linjenumrene med én.</span><span class="sxs-lookup"><span data-stu-id="b1a33-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="b1a33-116">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-116">Issue workaround</span></span>

<span data-ttu-id="b1a33-117">Kontroller at de ønskede linjenumrene allerede er angitt i linjenummerfeltene for dataenhet når du importerer bestillingslinjer.</span><span class="sxs-lookup"><span data-stu-id="b1a33-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="b1a33-118">I dette tilfellet vil ikke DMF overskrive linjenumrene.</span><span class="sxs-lookup"><span data-stu-id="b1a33-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="b1a33-119">En standard mva-gruppe og en standard kontantrabatt blir ikke fylt ut fra fakturakontoen.</span><span class="sxs-lookup"><span data-stu-id="b1a33-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="b1a33-120">Hvis du bruker en fakturakonto som er forskjellig fra kundekontoen, blir det ikke fylt ut en standard mva-gruppe og en standard kontantrabatt fra fakturakontoen når en bestilling opprettes.</span><span class="sxs-lookup"><span data-stu-id="b1a33-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="b1a33-121">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="b1a33-121">This behavior is by design.</span></span> <span data-ttu-id="b1a33-122">Standardverdiene for mva-gruppen, kontantrabattene og annen prisinformasjon er basert på kundekontoen, ikke fakturakontoen.</span><span class="sxs-lookup"><span data-stu-id="b1a33-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="b1a33-123">Jeg får feilmeldingen "Objektreferanse er ikke angitt" under bestillingsbekreftelsen, eller unntaket "Målet forårsaket et unntak under aktivering" oppstår ved postering av leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="b1a33-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="b1a33-124">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="b1a33-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="b1a33-125">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="b1a33-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="b1a33-126">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="b1a33-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="b1a33-127">Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert.</span><span class="sxs-lookup"><span data-stu-id="b1a33-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-128">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-128">Issue description</span></span>

<span data-ttu-id="b1a33-129">Du får følgende feilmelding: "Én eller flere regnskapsdistribusjoner er enten over- eller underdistribuert".</span><span class="sxs-lookup"><span data-stu-id="b1a33-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1a33-130">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-130">Issue resolution</span></span>

<span data-ttu-id="b1a33-131">Dette problemet kan oppstå på grunn av inkonsekvens i bestillingsdistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="b1a33-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="b1a33-132">Du fjerner blokkeringen av dette problemet og tilbakestiller bestillingen til en *Utkast*-tilstand ved å gå til **Innkjøp og leverandører \> Periodiske oppgaver \> Opprydding \> Tilbakestill bestillingsdistribusjon**.</span><span class="sxs-lookup"><span data-stu-id="b1a33-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="b1a33-133">Hvis du vil ha mer informasjon, kan du se følgende blogginnlegg: [Løse bestillingsdistribusjonsfeil i Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="b1a33-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="b1a33-134">Kan jeg bare vise bestillinger som jeg har opprettet?</span><span class="sxs-lookup"><span data-stu-id="b1a33-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="b1a33-135">Denne funksjonen er ikke tilgjengelig nå.</span><span class="sxs-lookup"><span data-stu-id="b1a33-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="b1a33-136">Kan jeg reservere lager og opprette transaksjoner mot registrert lager i en bestilling?</span><span class="sxs-lookup"><span data-stu-id="b1a33-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-137">Issue description</span></span>

<span data-ttu-id="b1a33-138">Selv når varene er i en *Registrert*-tilstand på en bestilling, kan du likevel reservere lageret.</span><span class="sxs-lookup"><span data-stu-id="b1a33-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="b1a33-139">Du kan med andre ord opprette transaksjoner mot det registrerte lageret.</span><span class="sxs-lookup"><span data-stu-id="b1a33-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="b1a33-140">Reprodusere problemet</span><span class="sxs-lookup"><span data-stu-id="b1a33-140">Reproduce the issue</span></span>

<span data-ttu-id="b1a33-141">Følgende prosedyre viser én måte å reprodusere problemet på.</span><span class="sxs-lookup"><span data-stu-id="b1a33-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="b1a33-142">Opprett en bestilling.</span><span class="sxs-lookup"><span data-stu-id="b1a33-142">Create a purchase order.</span></span>
2. <span data-ttu-id="b1a33-143">Registrere bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="b1a33-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="b1a33-144">Legg merke til at du kan generere reservasjoner eller transaksjoner mot det registrerte lageret.</span><span class="sxs-lookup"><span data-stu-id="b1a33-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1a33-145">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-145">Issue resolution</span></span>

<span data-ttu-id="b1a33-146">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="b1a33-146">This behavior is by design.</span></span> <span data-ttu-id="b1a33-147">Forventningen er at de registrerte varene fysisk har ankommet på lageret, og at de derfor er tilgjengelige for reservasjon.</span><span class="sxs-lookup"><span data-stu-id="b1a33-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="b1a33-148">Bestillinger reflekterer ikke språkinnstillingene til den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="b1a33-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-149">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-149">Issue description</span></span>

<span data-ttu-id="b1a33-150">Produktnavnet på en bestilling vises på systemspråket i stedet for språket som er angitt for den juridiske enheten der bestillingen ble opprettet.</span><span class="sxs-lookup"><span data-stu-id="b1a33-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="b1a33-151">Reprodusere problemet</span><span class="sxs-lookup"><span data-stu-id="b1a33-151">Reproduce the issue</span></span>

<span data-ttu-id="b1a33-152">Følgende prosedyre viser én måte å reprodusere problemet på.</span><span class="sxs-lookup"><span data-stu-id="b1a33-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="b1a33-153">Sett systemspråket til *EN-US* (amerikansk engelsk).</span><span class="sxs-lookup"><span data-stu-id="b1a33-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="b1a33-154">Kontroller at det finnes et produkt der språkene *EN-US* og *DE* (tysk) blir vedlikeholdt for oversettelser av produktnavnet.</span><span class="sxs-lookup"><span data-stu-id="b1a33-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="b1a33-155">Endre språket for en juridisk enhet til *DE*.</span><span class="sxs-lookup"><span data-stu-id="b1a33-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="b1a33-156">I den juridiske enheten der *DE* er angitt som språk, oppretter du en bestilling som inkluderer produktet.</span><span class="sxs-lookup"><span data-stu-id="b1a33-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="b1a33-157">Legg merke til at produktnavnet fremdeles vises på amerikansk engelsk (systemspråket).</span><span class="sxs-lookup"><span data-stu-id="b1a33-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1a33-158">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-158">Issue resolution</span></span>

<span data-ttu-id="b1a33-159">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="b1a33-159">This behavior is by design.</span></span> <span data-ttu-id="b1a33-160">I bestillinger vises produktet alltid på systemspråket.</span><span class="sxs-lookup"><span data-stu-id="b1a33-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="b1a33-161">Bestillingsspråket brukes når det opprettes en bekreftelsesjournal.</span><span class="sxs-lookup"><span data-stu-id="b1a33-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="b1a33-162">Listen over godkjente leverandører per produktenhet tillater ikke at ikrafttredelsesdatoen endres.</span><span class="sxs-lookup"><span data-stu-id="b1a33-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-163">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-163">Issue description</span></span>

<span data-ttu-id="b1a33-164">Et produkt har en godkjent leverandør som for eksempel har gyldighetsdato 11. januar 2018 (*01/11/2018*) og utløpsdatoen *Aldri*.</span><span class="sxs-lookup"><span data-stu-id="b1a33-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="b1a33-165">Hvis du prøver å endre ikrafttredelsesdatoen til 10. januar 2018 (*01/10/2018*) eller 12. januar 2018 (*01/12/2018*), får du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="b1a33-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="b1a33-166">Kan ikke opprette en post i liste over godkjente leverandører (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="b1a33-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="b1a33-167">Verdien for utløpsdato må være større enn eller lik verdien for gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="b1a33-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1a33-168">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-168">Issue resolution</span></span>

<span data-ttu-id="b1a33-169">Du kan bare forlenge perioden leverandøren er godkjent for.</span><span class="sxs-lookup"><span data-stu-id="b1a33-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="b1a33-170">Følgende regler gjelder:</span><span class="sxs-lookup"><span data-stu-id="b1a33-170">The following rules apply:</span></span>

- <span data-ttu-id="b1a33-171">Hvis du vil endre ikrafttredelsesdatoen slik at den er tidligere enn noen av de eksisterende postene (perioder) for vareleverandøren, må utløpsdatoen for den nye perioden være før alle utløpsdatoene i de eksisterende postene.</span><span class="sxs-lookup"><span data-stu-id="b1a33-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="b1a33-172">Hvis du vil endre utløpsdatoen slik at den er senere enn noen av de eksisterende periodene, må ikrafttredelsesdatoen være etter den seneste utløpsdatoen i alle eksisterende poster.</span><span class="sxs-lookup"><span data-stu-id="b1a33-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="b1a33-173">Hvis du vil redusere den overordnede perioden som leverandøren er godkjent for, må du slette eller endre eksisterende poster.</span><span class="sxs-lookup"><span data-stu-id="b1a33-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="b1a33-174">Du kan også bruke bryteren for **avkorting** under import.</span><span class="sxs-lookup"><span data-stu-id="b1a33-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="b1a33-175">Denne bryteren sletter alle eksisterende poster i tabellen for godkjente leverandører etter vare.</span><span class="sxs-lookup"><span data-stu-id="b1a33-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="b1a33-176">For eksempel scenarioet som er beskrevet i problembeskrivelsen, der en post har en gyldighetsdato på *01/11/2018* og utløpsdatoen *Aldri*, kan du importere en ny post som har en gyldighetsdato på *01/10/2018* og utløpsdatoen *Aldri*.</span><span class="sxs-lookup"><span data-stu-id="b1a33-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="b1a33-177">Du kan imidlertid ikke redusere perioden slik at ikrafttredelsesdatoen oppdateres til *01/12/2018* via databehandling.</span><span class="sxs-lookup"><span data-stu-id="b1a33-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="b1a33-178">Du må gjøre denne endringen i brukergrensesnittet.</span><span class="sxs-lookup"><span data-stu-id="b1a33-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="b1a33-179">Etter at jeg endret leveringsadressen i et bestillingshode, blir ikke leveringsnavnet synkronisert.</span><span class="sxs-lookup"><span data-stu-id="b1a33-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1a33-180">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="b1a33-180">Issue description</span></span>

<span data-ttu-id="b1a33-181">Adressen på hodet til en bestilling oppdateres til en adresse som ikke er en leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="b1a33-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="b1a33-182">Selv om adressen oppdateres på bestillingen, oppdateres ikke leveringsnavnet basert på den oppdaterte adressen.</span><span class="sxs-lookup"><span data-stu-id="b1a33-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1a33-183">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="b1a33-183">Issue resolution</span></span>

<span data-ttu-id="b1a33-184">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="b1a33-184">This behavior is by design.</span></span> <span data-ttu-id="b1a33-185">Den valgte adressen må klassifiseres som leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="b1a33-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="b1a33-186">Hvis ikke oppdateres ikke leveringsnavnet basert på den valgte adressen.</span><span class="sxs-lookup"><span data-stu-id="b1a33-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="b1a33-187">Kan jeg finne brukeren som annullerte en bestilling?</span><span class="sxs-lookup"><span data-stu-id="b1a33-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="b1a33-188">Denne informasjonen spores bare hvis bestillingen er underlagt endringsstyring.</span><span class="sxs-lookup"><span data-stu-id="b1a33-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="b1a33-189">Hvis du bruker endringsstyring, kan du se hvem som sendte inn endringen (annulleringen), og hvem som godkjente den.</span><span class="sxs-lookup"><span data-stu-id="b1a33-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
