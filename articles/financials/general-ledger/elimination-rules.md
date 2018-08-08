---
title: Elimineringsregler
description: Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c0736d63c9a582948d197dc267f9941cbbd3e3c6
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---

# <a name="elimination-rules"></a><span data-ttu-id="ec6c8-103">Elimineringsregler</span><span class="sxs-lookup"><span data-stu-id="ec6c8-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec6c8-104">Dette emnet inneholder informasjon om elimineringsregler og de ulike alternativene for rapportering om elimineringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="ec6c8-105">Elimineringstransaksjoner er nødvendige når en overordnet juridisk enhet handler med én eller flere underordnede juridiske enheter og bruker konsolidert finansrapportering.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="ec6c8-106">Konsoliderte regnskapsoppgjør kan bare omfatte transaksjoner som forekommer mellom den konsoliderte organisasjonen og andre enheter utenfor denne organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="ec6c8-107">Derfor må transaksjoner mellom juridiske enheter som er en del av samme organisasjon, fjernes, eller elimineres, fra økonomimodulen, slik at de ikke vises i finansrapporter.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="ec6c8-108">Det finnes flere måter å rapportere om elimineringer på:</span><span class="sxs-lookup"><span data-stu-id="ec6c8-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="ec6c8-109">En elimineringsregel kan opprettes og behandles i et konsoliderings- eller elimineringsfirma.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="ec6c8-110">Finansrapportering kan brukes til å vise elimineringskontoene og -dimensjonene i en bestemt rad eller kolonne.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="ec6c8-111">En separat juridisk enhet kan brukes til å postere manuelle transaksjonsoppføringer for å spore elimineringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="ec6c8-112">Dette emnet fokuserer på elimineringsregler som behandles i et konsoliderings- eller elimineringsfirma.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="ec6c8-113">Du kan definere elimineringsregler for å opprette elimineringstransaksjoner i en juridisk enhet som er angitt som juridisk målenhet for elimineringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="ec6c8-114">Denne juridiske mottakerenheten kalles den den juridiske elimineringsenheten.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="ec6c8-115">Elimineringsjournaler kan enten genereres under konsolideringsprosessen eller ved hjelp av et elimineringsjournalforslag.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="ec6c8-116">Før du definerer elimineringsregler, bør du gjøre deg kjent med følgende begreper:</span><span class="sxs-lookup"><span data-stu-id="ec6c8-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="ec6c8-117">**Kilde for juridisk enhet** – Den juridiske enheten der beløpene som elimineres, var postert.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="ec6c8-118">**Juridisk målenhet** – Den juridiske enheten der elimineringsreglene posteres.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="ec6c8-119">**Juridisk enhet for eliminering** – Den juridiske enheten som er angitt som juridisk målenhet for elimineringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="ec6c8-120">**Konsolidert juridisk enhet** – Den juridiske enheten som opprettes for å rapportere økonomiske resultater for en gruppe med juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="ec6c8-121">De økonomiske dataene fra de juridiske enhetene konsolideres til denne juridiske enheten, og deretter opprettes en finansrapport ved hjelp av de kombinerte dataene.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="ec6c8-122">Følgende tabell viser hvilke typer transaksjoner du kan være nødt til å eliminere.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec6c8-123">transaksjonstype</span><span class="sxs-lookup"><span data-stu-id="ec6c8-123">Transaction type</span></span></th>
<th><span data-ttu-id="ec6c8-124">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ec6c8-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec6c8-125">Salgsordreoppføringer og -fakturering (sentralisert behandling)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="ec6c8-126">Du selger et produkt til en kunde på vegne av en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-127">Salgsordreoppføring (mellom firmaer / internt i ett firma) og -fakturering</span><span class="sxs-lookup"><span data-stu-id="ec6c8-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="ec6c8-128">Du selger varer mellom juridiske enheter i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6c8-129">Bestillinger (sentralisert behandling)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="ec6c8-130">Du kjøper lagerbeholdning, utstyr, tjenester, anleggsmidler og andre produkter fra en leverandør på vegne av en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-131">Lagerstyring (mellom firmaer / internt i ett firma)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="ec6c8-132">Du overfører beholdningen til én juridisk enhet til anleggsmidler for en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="ec6c8-133">Du overfører beholdningen til én juridisk enhet til beholdningen for en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6c8-134">Lagersporing i transitt</span><span class="sxs-lookup"><span data-stu-id="ec6c8-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="ec6c8-135">Du overfører varer mellom lagre i den samme juridiske enheten, men i forskjellige geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-136">Sentralisert fakturabehandling for leverandører</span><span class="sxs-lookup"><span data-stu-id="ec6c8-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="ec6c8-137">Du registrerer en faktura på vegne av en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6c8-138">Sentralisert betaling av leverandører</span><span class="sxs-lookup"><span data-stu-id="ec6c8-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="ec6c8-139">Du betaler en faktura på vegne av en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-140">Kontantstyring og pengebeholdning (sentralisert behandling)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="ec6c8-141">Du behandler skatteinnbetalinger, skatterefusjoner, rentebelastninger, lån, forskudd, utbetalt aksjeutbytte og forhåndsbetalt royalty eller provisjon.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="ec6c8-142">Du betaler en utgift på vegne av en annen juridisk enhet i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="ec6c8-143">Fakturaen legges inn i den juridiske målenhetens bøker, og du må utligne mellom juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="ec6c8-144">En juridisk enhet betaler for eksempel reiseregningsrapporten for en ansatt i en annen juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="ec6c8-145">I dette tilfellet har den ansattes reiseregningsrapport utgifter som er knyttet til en annen juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="ec6c8-146">Du overfører kontanter fra én juridisk enhet til en annen i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6c8-147">Kunder (sentralisert behandling)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="ec6c8-148">Du mottar kontanter for kundefakturaen for en annen juridiske enhet, og du betaler sjekken inn på bankkontoen til denne juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-149">Lønn (sentralisert behandling, mellom firmaer / innenfor ett firma)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="ec6c8-150">Du betaler lønnen til en annen juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="ec6c8-151">En juridisk enhet betaler for eksempel sin egen lønn til sine ansatte, men viderefakturerer arbeid som en ansatt har utført for en annen juridisk enhet i den lønnsperioden.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="ec6c8-152">Eller en ansatt har arbeidet deltid for juridisk enhet A og deltid for juridisk enhet B, og fordelene beregnes ut fra samlet lønn.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="ec6c8-153">I disse tilfellene inneholder lønnen til den ansatte lønn fra begge juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="ec6c8-154">Ikke bare posteres lønn, men også avgifter, fordeler, fradrag og avsetninger for lønn.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="ec6c8-155">Du overfører arbeidskraft fra en avdeling eller divisjon til en annen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec6c8-156">Anleggsmidler (mellom firmaer / innenfor ett firma)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="ec6c8-157">Du overfører anleggsmidler til en annen juridisk enhets anleggsmidler eller lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec6c8-158">Tildelinger (mellom firmaer / innenfor ett firma)</span><span class="sxs-lookup"><span data-stu-id="ec6c8-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="ec6c8-159">Du behandler firmatilordninger.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-159">You process corporate allocations.</span></span> <span data-ttu-id="ec6c8-160">Tildelinger er aktiviteter til en hvilken som helst tildelt konto, uansett opprinnelsesmodul.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="ec6c8-161">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ec6c8-161">Example</span></span>
<span data-ttu-id="ec6c8-162">Den juridiske enheten, juridisk enhet A, selge noe til en annen juridisk enhet i organisasjonen, juridisk enhet B. Følgende eksempel viser hvordan transaksjoner som forekommer mellom de to juridiske enhetene kan måtte elimineres:</span><span class="sxs-lookup"><span data-stu-id="ec6c8-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="ec6c8-163">Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 10,00.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="ec6c8-164">Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 10,00 pluss 2,00 i faktiske leveringskostnader.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="ec6c8-165">Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 15,00 og anerkjenner en margin på dette salget.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="ec6c8-166">Juridisk enhet A selger en gjenstand som koster 10,00 til juridisk enhet B for 15,00 og anerkjenner halvparten av marginen på dette salget.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="ec6c8-167">Juridisk enhet B anerkjenner den andre halvparten av marginen på salget.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="ec6c8-168">Derfor deles omsetningen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="ec6c8-169">Delt omsetning gir et insentiv til å bestille fra en annen juridisk enhet i organisasjonen i stedet for en ekstern organisasjon.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="ec6c8-170">Alle disse transaksjonene genererer transaksjoner mellom firmaene som posteres til forfall-til- og forfall-fra-kontoer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="ec6c8-171">I tillegg kan disse transaksjonene omfatte påslags- og avslagsbeløp når beløpet for konserninternt salg ikke er likt kostnadene for varene som ble solgt.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="ec6c8-172">Definere elimineringsregler</span><span class="sxs-lookup"><span data-stu-id="ec6c8-172">Set up elimination rules</span></span>
<span data-ttu-id="ec6c8-173">Når du definerer elimineringsregler i Microsoft Dynamics 365 for Finance and Operations, anbefaler vi at du oppretter en finansdimensjon spesielt for elimineringsformål.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="ec6c8-174">De fleste kunder gir den navnet Handelspartner eller noe lignende.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="ec6c8-175">Hvis du bestemmer deg for ikke å bruke en finansdimensjon, må du sørge for å ha hovedkontoer som er spesifikke for bare konserninterne transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="ec6c8-176">Oppsettet for elimineringer finnes i Oppsett-området i modulen Konsolideringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="ec6c8-177">Når du har skrevet inn en beskrivelse av regelen, må du velge firmaet som elimineringsjournalen skal postere til.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="ec6c8-178">Dette bør være et firma som har valgt **Brukes til finanseliminering** under oppsettet av den juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="ec6c8-179">Du kan angi en dato da elimineringsregelen trer i kraft, og når den utløpes, om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="ec6c8-180">Du må angi **Aktiv** til **Ja** hvis du vil at den skal være tilgjengelig i elimineringsforslagsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="ec6c8-181">Velg et journalnavn som har en type **Eliminering**.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="ec6c8-182">Når du har definert det grunnleggende, kan du definere de faktiske behandlingsreglene ved å klikke **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="ec6c8-183">Det finnes to alternativer for elimineringer: eliminere netto endringsbeløp eller definere et fast beløp.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="ec6c8-184">Velg kildekontoen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-184">Select your source account.</span></span> <span data-ttu-id="ec6c8-185">Du kan bruke stjerne (\*) som et jokertegn.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="ec6c8-186">1\* velger for eksempel alle kontoer som starter med 1, som en kilde for datatildelingen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="ec6c8-187">Når du har valgt kildekontoene, bestemmer **kontospesifikasjonen** kontoen fra målfirmaet som brukes.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="ec6c8-188">Velg **Kilde** hvis du vil bruke den samme hovedkontoen som er definert i **Kilde**-kontoen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="ec6c8-189">Hvis du velger **Brukerdefinert**, må du angi en målkonto.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="ec6c8-190">Dimensjonsspesifikasjonen fungerer på samme måte.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="ec6c8-191">Hvis du velger **Kilde**, vil den bruke de samme dimensjonene i målfirmaet som kildefirmaet.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="ec6c8-192">Hvis du velger **Brukerdefinert**, må du angi dimensjoner i målfirmaet ved å klikke **Måldimensjoner**-menyelementet.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="ec6c8-193">Velg kildedimensjoner og finansdimensjoner og verdiene som brukes som en kilde for eliminering.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="ec6c8-194">Behandle elimineringstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="ec6c8-194">Process elimination transactions</span></span>
<span data-ttu-id="ec6c8-195">Det er to måter å behandle elimineringstransaksjoner på, under den elektroniske konsolideringsprosessen eller ved å opprette en elimineringsjournal og kjøre elimineringsforslagsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="ec6c8-196">Denne delen fokuserer på å opprette journalen og kjøre elimineringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="ec6c8-197">I et firma som er definert som et elimineringsfirma, velger du **Elimineringsjournal** i modulen Konsolideringer.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="ec6c8-198">Når du har valgt journalnavnet, klikker du **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="ec6c8-199">Du kan kjøre forslaget ved å velge **Forslag**-menyen og deretter velge **Elimineringsforslag**.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="ec6c8-200">Velg firmaet som er kilden til de konsoliderte dataene, og velg deretter regelen du vil behandle.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="ec6c8-201">Angi en startdato for å starte søket for elimineringsbeløp, og en sluttdato for å avslutte søkedatoen for elimineringsbeløp.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="ec6c8-202">Feltet **FIN-posteringsdato** brukes til å postere journalen til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="ec6c8-203">Når du klikker **OK**, kan du se gjennom beløpene og postere journalen.</span><span class="sxs-lookup"><span data-stu-id="ec6c8-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




