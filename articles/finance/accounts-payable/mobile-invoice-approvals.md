---
title: Mobile fakturagodkjenninger
description: Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta godkjenning av leverandørfaktura for mobil som et brukstilfelle.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 956c866a6b39e2a81f085910e00d2bfe8683829c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179292"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="12d1d-103">Mobile fakturagodkjenninger</span><span class="sxs-lookup"><span data-stu-id="12d1d-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12d1d-104">Mobilfunksjoner lar forretningsbrukere utforme mobilopplevelser.</span><span class="sxs-lookup"><span data-stu-id="12d1d-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="12d1d-105">For avanserte scenarier lar plattformen også utviklere utvide egenskapene som de ønsker.</span><span class="sxs-lookup"><span data-stu-id="12d1d-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="12d1d-106">Den mest effektive måten å lære noen av de nye konseptene på mobil er å gå gjennom prosessen med å utforme et par scenarier.</span><span class="sxs-lookup"><span data-stu-id="12d1d-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="12d1d-107">Dette emnet er ment å gi en praktisk tilnærming til utforming av mobile scenarier ved å ta godkjenning av leverandørfaktura for mobil som et brukstilfelle.</span><span class="sxs-lookup"><span data-stu-id="12d1d-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="12d1d-108">Dette emnet hjelper deg med å utforme andre variasjoner av scenarier, og kan også brukes til andre scenarier som ikke er relatert til leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12d1d-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="12d1d-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="12d1d-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="12d1d-110">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="12d1d-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="12d1d-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="12d1d-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12d1d-112">Før du leser håndboken for mobil</span><span class="sxs-lookup"><span data-stu-id="12d1d-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="12d1d-113">Mobil plattform</span><span class="sxs-lookup"><span data-stu-id="12d1d-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="12d1d-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="12d1d-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="12d1d-115">Et miljø som har versjon 1611 og Platform update 3 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="12d1d-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="12d1d-116">Installer hurtigreparasjon KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="12d1d-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="12d1d-117">Oppgaveregistrering kan feilaktig registrere to Lukk-kommandoer for rullegardindialoger. Dette er inkludert i Platform update 3 (november-oppdatering 2016).</span><span class="sxs-lookup"><span data-stu-id="12d1d-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="12d1d-118">Installer hurtigreparasjon KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="12d1d-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="12d1d-119">Denne hurtigreparasjonen gjør at vedlegg skal vises på den mobile klienten. Dette er inkludert i Platform update 3 (november-oppdatering 2016).</span><span class="sxs-lookup"><span data-stu-id="12d1d-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="12d1d-120">Installer hurtigreparasjon KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="12d1d-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="12d1d-121">Programkode for godkjenning av leverandørfaktura på mobil. Dette er inkludert i versjon 7.0.1 (mai 2016).</span><span class="sxs-lookup"><span data-stu-id="12d1d-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="12d1d-122">En Android- eller iOS- eller Windows-enhet som har mobilappen installert.</span><span class="sxs-lookup"><span data-stu-id="12d1d-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="12d1d-123">Søk etter appen i riktig applager.</span><span class="sxs-lookup"><span data-stu-id="12d1d-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="12d1d-124">Innledning</span><span class="sxs-lookup"><span data-stu-id="12d1d-124">Introduction</span></span>
<span data-ttu-id="12d1d-125">Mobile godkjenninger for leverandørfakturaer krever de tre hurtigreparasjonene som er nevnt i delen "Forutsetninger".</span><span class="sxs-lookup"><span data-stu-id="12d1d-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="12d1d-126">Disse hurtigreparasjonene gir ikke et arbeidsområde for fakturagodkjenninger.</span><span class="sxs-lookup"><span data-stu-id="12d1d-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="12d1d-127">Hvis du vil vite hva et arbeidsområde er i forbindelse med mobil, kan du lese håndboken for mobil som er nevnt i delen "Forutsetninger".</span><span class="sxs-lookup"><span data-stu-id="12d1d-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="12d1d-128">Arbeidsområdet for fakturagodkjenninger må være utformet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="12d1d-129">Alle organisasjoner lager og definerer sin forretningsprosess for leverandørfakturaer annerledes.</span><span class="sxs-lookup"><span data-stu-id="12d1d-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="12d1d-130">Før du utformer en mobil opplevelse for godkjenning av leverandørfakturaer, bør du vurdere følgende aspekter av forretningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="12d1d-131">Tanken er å bruke disse datapunkter som er så mye som mulig å optimalisere brukerens opplevelse på enheten.</span><span class="sxs-lookup"><span data-stu-id="12d1d-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="12d1d-132">Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="12d1d-133">Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="12d1d-134">Hvor mange fakturalinjene er det i en faktura?</span><span class="sxs-lookup"><span data-stu-id="12d1d-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="12d1d-135">Bruke 80-20 regelen her, og optimalisere 80 prosent.</span><span class="sxs-lookup"><span data-stu-id="12d1d-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="12d1d-136">Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser?</span><span class="sxs-lookup"><span data-stu-id="12d1d-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="12d1d-137">Hvis svaret på dette spørsmålet er Ja, kan du vurdere følgende spørsmål:</span><span class="sxs-lookup"><span data-stu-id="12d1d-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="12d1d-138">Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg, delinger og så videre) er det for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="12d1d-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="12d1d-139">Igjen, bruke 80-20 regelen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="12d1d-140">Fakturaene også har regnskapsdistribusjoner i fakturahodet?</span><span class="sxs-lookup"><span data-stu-id="12d1d-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="12d1d-141">I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="12d1d-142">Dette emnet forklarer ikke hvordan du redigerer regnskapsdistribusjoner, fordi denne funksjonaliteten ikke støttes for øyeblikket for mobile scenarier.</span><span class="sxs-lookup"><span data-stu-id="12d1d-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="12d1d-143">Brukere vil se vedlegg for fakturaen på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="12d1d-144">Utformingen av mobil opplevelse for fakturagodkjenninger varierer avhengig av svarene på disse spørsmålene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="12d1d-145">Målet er å optimalisere brukerens opplevelse for forretningsprosessen på mobil i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="12d1d-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="12d1d-146">I resten av dette emnet vil vi se på to scenariovariasjoner som er basert på forskjellige svar på spørsmålene ovenfor.</span><span class="sxs-lookup"><span data-stu-id="12d1d-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="12d1d-147">Som en generell veiledning, når du arbeider med mobile designer, må du "publisere" endringene for ikke å miste oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="12d1d-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="12d1d-148">Utforme et scenario for godkjenning av enkel faktura for Contoso</span><span class="sxs-lookup"><span data-stu-id="12d1d-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12d1d-149">Scenarieattributt</span><span class="sxs-lookup"><span data-stu-id="12d1d-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="12d1d-150">Svar</span><span class="sxs-lookup"><span data-stu-id="12d1d-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12d1d-151">Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="12d1d-152">Navn på leverandør</span><span class="sxs-lookup"><span data-stu-id="12d1d-152">Vendor name</span></span></li>
<li><span data-ttu-id="12d1d-153">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="12d1d-153">Invoice total</span></span></li>
<li><span data-ttu-id="12d1d-154">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="12d1d-154">Invoice account</span></span></li>
<li><span data-ttu-id="12d1d-155">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="12d1d-155">Invoice number</span></span></li>
<li><span data-ttu-id="12d1d-156">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="12d1d-156">Invoice date</span></span></li>
<li><span data-ttu-id="12d1d-157">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="12d1d-157">Invoice description</span></span></li>
<li><span data-ttu-id="12d1d-158">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="12d1d-158">Due date</span></span></li>
<li><span data-ttu-id="12d1d-159">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="12d1d-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-160">Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="12d1d-161">Innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="12d1d-161">Procurement category</span></span></li>
<li><span data-ttu-id="12d1d-162">Antall</span><span class="sxs-lookup"><span data-stu-id="12d1d-162">Quantity</span></span></li>
<li><span data-ttu-id="12d1d-163">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="12d1d-163">Unit price</span></span></li>
<li><span data-ttu-id="12d1d-164">Nettobeløp for linje</span><span class="sxs-lookup"><span data-stu-id="12d1d-164">Line net amount</span></span></li>
<li><span data-ttu-id="12d1d-165">1099-beløp</span><span class="sxs-lookup"><span data-stu-id="12d1d-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-166">Hvor mange fakturalinjene er det i en faktura?</span><span class="sxs-lookup"><span data-stu-id="12d1d-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="12d1d-167">Bruke 80-20 regelen her, og optimalisere 80 prosent.</span><span class="sxs-lookup"><span data-stu-id="12d1d-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="12d1d-168">1</span><span class="sxs-lookup"><span data-stu-id="12d1d-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-169">Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser?</span><span class="sxs-lookup"><span data-stu-id="12d1d-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="12d1d-170">Ja</span><span class="sxs-lookup"><span data-stu-id="12d1d-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-171">Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg og så videre) er det for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="12d1d-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="12d1d-172">Igjen, bruke 80-20 regelen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="12d1d-173">Utvidet pris: 2 mva: 0 gebyrer: 0</span><span class="sxs-lookup"><span data-stu-id="12d1d-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-174">Fakturaene også har regnskapsdistribusjoner i fakturahodet?</span><span class="sxs-lookup"><span data-stu-id="12d1d-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="12d1d-175">I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="12d1d-176">Brukes ikke</span><span class="sxs-lookup"><span data-stu-id="12d1d-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-177">Brukere vil se vedlegg for fakturaen på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="12d1d-178">Ja</span><span class="sxs-lookup"><span data-stu-id="12d1d-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="12d1d-179">Opprett arbeidsområdet</span><span class="sxs-lookup"><span data-stu-id="12d1d-179">Create the workspace</span></span>

1.  <span data-ttu-id="12d1d-180">Åpne en nettleser, og logg på programmet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="12d1d-181">Etter at du har logget på, kan du legge til **&mode=mobile** i URL-adressen som vist i følgende eksempel, og oppdater siden: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="12d1d-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="12d1d-182">Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="12d1d-183">Mobile app-designer må vises akkurat slik oppgaveopptaker vises.</span><span class="sxs-lookup"><span data-stu-id="12d1d-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="12d1d-184">Klikk på **Legg til** for å opprette det nye arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="12d1d-185">For dette eksemplet gir du arbeidsområdet navnet **Mine godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="12d1d-186">Angi en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12d1d-186">Enter a description.</span></span>
6.  <span data-ttu-id="12d1d-187">Velg en farge for arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-187">Select a workspace color.</span></span> <span data-ttu-id="12d1d-188">Arbeidsområdefargen vil bli brukt for den generelle stilen for mobil opplevelse for arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="12d1d-189">Velg et ikon for arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="12d1d-190">Klikk **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-190">Click **Done**</span></span>
9.  <span data-ttu-id="12d1d-191">Klikk **Publiser arbeidsområde** for å lagre endringene</span><span class="sxs-lookup"><span data-stu-id="12d1d-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="12d1d-192">Leverandørfakturaer som er tilordnet til meg</span><span class="sxs-lookup"><span data-stu-id="12d1d-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="12d1d-193">Den første mobile siden som du bør utforme er listen over fakturaer som er tilordnet til brukeren for gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="12d1d-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="12d1d-194">Hvis du vil utforme Mobil-siden, kan du bruke **VendMobileInvoiceAssignedToMeListPage**-siden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="12d1d-195">Før du fullfører denne prosedyren, må du kontrollere at minst en leverandørfaktura er tilordnet til deg for gjennomgang, og at fakturalinjen har to distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="12d1d-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="12d1d-196">Dette oppsettet oppfyller kravene for dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="12d1d-197">I URL-adressen erstatter du navnet på menyelementet med **VendMobileInvoiceAssignedToMeListPage** for å åpne den mobile versjonen av listesiden **Ventende leverandørfakturaer som er tilordnet til meg** i **Leverandører**-modulen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="12d1d-198">Avhengig av hvor mange fakturaer som du har i systemet tilordnet deg viser denne siden de fakturaene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="12d1d-199">Du kan bruke filteret til venstre for å finne en spesifikk faktura.</span><span class="sxs-lookup"><span data-stu-id="12d1d-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="12d1d-200">Men krever vi ikke en bestemt faktura for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="12d1d-201">Vi krever bare noen fakturaen som er tilordnet til deg som kommer til å la deg utforme Mobil-siden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="12d1d-202">De nye sidene som er tilgjengelige er utformet spesielt for utvikling av mobile scenarier for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="12d1d-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="12d1d-203">Derfor må du bruke disse sidene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="12d1d-204">URL-adressen skal ligne på følgende URL-adresse, og når du har angitt det, må siden som vises i illustrasjonen, vises: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Ventende leverandørfakturaer som er tilordnet til meg-siden](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="12d1d-205">Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**</span><span class="sxs-lookup"><span data-stu-id="12d1d-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="12d1d-206">Velg arbeidsområdet og klikk **Rediger**</span><span class="sxs-lookup"><span data-stu-id="12d1d-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="12d1d-207">Klikk **Legg til side** for å opprette den første mobilsiden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="12d1d-208">Skriv inn et navn som **Mine leverandørfakturaer** og en beskrivelse som **Leverandørfakturaer som er tilordnet til meg for gjennomgang**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="12d1d-209">Klikk **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-209">Click **Done**.</span></span>
7.  <span data-ttu-id="12d1d-210">I mobile designer på **Felt**-kategorien, klikk **Velg felt**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="12d1d-211">Kolonnene på listesiden over må ligne på følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="12d1d-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="12d1d-212">[![Kolonner på siden Ventende leverandørfakturaer som er tilordnet til meg](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="12d1d-213">Legg til de påkrevde kolonnene fra listesiden som vises til brukerne på mobilsiden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="12d1d-214">Rekkefølgen som du legger til, er rekkefølgen som feltene vises til sluttbrukeren.</span><span class="sxs-lookup"><span data-stu-id="12d1d-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="12d1d-215">Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt.</span><span class="sxs-lookup"><span data-stu-id="12d1d-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="12d1d-216">Basert på kravene for dette scenariet, er følgende åtte felt obligatoriske.</span><span class="sxs-lookup"><span data-stu-id="12d1d-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="12d1d-217">Men noen brukere kan vurdere at åtte felt er for mye informasjon å ha på en mobil enhet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="12d1d-218">Derfor vil vi vise bare de viktigste feltene i den mobile listevisningen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="12d1d-219">De gjenværende feltene vises i detaljvisningen, som vi vil utforme senere.</span><span class="sxs-lookup"><span data-stu-id="12d1d-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="12d1d-220">Nå skal vi legge til følgende felt.</span><span class="sxs-lookup"><span data-stu-id="12d1d-220">For now, we will add the following fields.</span></span> <span data-ttu-id="12d1d-221">Klikk plusstegnet (**+**) i disse kolonnene for å legge dem til på den mobile siden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="12d1d-222">Navn på leverandør</span><span class="sxs-lookup"><span data-stu-id="12d1d-222">Vendor name</span></span>
    - <span data-ttu-id="12d1d-223">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="12d1d-223">Invoice total</span></span>
    - <span data-ttu-id="12d1d-224">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="12d1d-224">Invoice account</span></span>
    - <span data-ttu-id="12d1d-225">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="12d1d-225">Invoice number</span></span>
    - <span data-ttu-id="12d1d-226">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="12d1d-226">Invoice date</span></span>

    <span data-ttu-id="12d1d-227">Når feltene er lagt til, må mobilsiden ligne på følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="12d1d-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="12d1d-228">[![Side når felt er lagt til](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="12d1d-229">Du må også legge til følgende kolonner nå, slik at vi kan aktivere arbeidsflythandlinger senere.</span><span class="sxs-lookup"><span data-stu-id="12d1d-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="12d1d-230">Vis fullført oppgave</span><span class="sxs-lookup"><span data-stu-id="12d1d-230">Show complete task</span></span>
    - <span data-ttu-id="12d1d-231">Vis delegert oppgave</span><span class="sxs-lookup"><span data-stu-id="12d1d-231">Show delegate task</span></span>
    - <span data-ttu-id="12d1d-232">Vis tilbakekallt oppgave</span><span class="sxs-lookup"><span data-stu-id="12d1d-232">Show recall task</span></span>
    - <span data-ttu-id="12d1d-233">Vis avvist oppgave</span><span class="sxs-lookup"><span data-stu-id="12d1d-233">Show reject task</span></span>
    - <span data-ttu-id="12d1d-234">Vis oppgave for å be om fullføring</span><span class="sxs-lookup"><span data-stu-id="12d1d-234">Show request completion task</span></span>
    - <span data-ttu-id="12d1d-235">Vis send på nytt-oppgave</span><span class="sxs-lookup"><span data-stu-id="12d1d-235">Show resubmit task</span></span>

10. <span data-ttu-id="12d1d-236">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="12d1d-237">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="12d1d-238">Klikk **Publiser arbeidsområde** for å lagre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="12d1d-239">Aktiver **Vis fakturatotal på listen over leverandørfakturaer på vent** i skjemaet med leverandørparametere under **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="12d1d-240">Vær oppmerksom på at bare ved å aktivere denne parameteren, fakturatotaler beregnes som skal vises på den ventende listesiden leverandørfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12d1d-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="12d1d-241">Dette er en ny funksjon som en del av den nødvendige hurtigreparasjonen 3208224.</span><span class="sxs-lookup"><span data-stu-id="12d1d-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="12d1d-242">Leverandørfakturadetaljer</span><span class="sxs-lookup"><span data-stu-id="12d1d-242">Vendor invoice details</span></span>

<span data-ttu-id="12d1d-243">Hvis du vil utforme siden med fakturadetaljer for mobil, kan du bruke siden **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="12d1d-244">Legg merke til at, avhengig av antall fakturaer som du har på maskinen, denne siden viser den eldste fakturaen (faktura som var opprettet først).</span><span class="sxs-lookup"><span data-stu-id="12d1d-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="12d1d-245">Du kan bruke filteret til venstre for å finne en spesifikk faktura.</span><span class="sxs-lookup"><span data-stu-id="12d1d-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="12d1d-246">Men krever vi ikke en bestemt faktura for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="12d1d-247">Vi krever bare noen fakturadata slik at vi kan utforme mobilsiden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="12d1d-248">[![Arbeidsflytside](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="12d1d-249">I URL-adressen erstatter du navnet på menyelementet med **VendMobileInvoiceHeaderDetails** for å åpne skjemaet</span><span class="sxs-lookup"><span data-stu-id="12d1d-249">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2. <span data-ttu-id="12d1d-250">Åpne utformingen for mobil fra **Innstillinger** (tannhjul)-knappen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3. <span data-ttu-id="12d1d-251">Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4. <span data-ttu-id="12d1d-252">Velg siden **Mine leverandørfakturaer** som du opprettet tidligere, og klikk deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-252">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>
5. <span data-ttu-id="12d1d-253">På kategorien **Felt** klikker du **Rutenett**-kolonneoverskriften.</span><span class="sxs-lookup"><span data-stu-id="12d1d-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6. <span data-ttu-id="12d1d-254">Klikk **Egenskaper &gt; Legg til side**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-254">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="12d1d-255">**Obs!** Når du klikker på **Rutenett**-overskriften og legger til en side, i forhold til detaljene siden opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="12d1d-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7. <span data-ttu-id="12d1d-256">Angi en tittel, som **Fakturaopplysninger**, og en beskrivelse, som **Vis fakturahode og linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8. <span data-ttu-id="12d1d-257">Klikk **Velg felt**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-257">Click **Select fields**.</span></span> <span data-ttu-id="12d1d-258">Legg merke til at rekkefølgen som du legger til, er rekkefølgen som feltene vises til sluttbrukeren.</span><span class="sxs-lookup"><span data-stu-id="12d1d-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="12d1d-259">Vil være den eneste måten å endre rekkefølgen på feltene ved å velge alle feltene på nytt.</span><span class="sxs-lookup"><span data-stu-id="12d1d-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9. <span data-ttu-id="12d1d-260">Legg til følgende felt fra hodet, basert på kravene for dette scenariet:</span><span class="sxs-lookup"><span data-stu-id="12d1d-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="12d1d-261">Navn på leverandør</span><span class="sxs-lookup"><span data-stu-id="12d1d-261">Vendor name</span></span>
   - <span data-ttu-id="12d1d-262">Fakturatotal</span><span class="sxs-lookup"><span data-stu-id="12d1d-262">Invoice total</span></span>
   - <span data-ttu-id="12d1d-263">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="12d1d-263">Invoice account</span></span>
   - <span data-ttu-id="12d1d-264">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="12d1d-264">Invoice number</span></span>
   - <span data-ttu-id="12d1d-265">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="12d1d-265">Invoice date</span></span>
   - <span data-ttu-id="12d1d-266">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="12d1d-266">Invoice description</span></span>
   - <span data-ttu-id="12d1d-267">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="12d1d-267">Due date</span></span>
   - <span data-ttu-id="12d1d-268">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="12d1d-268">Invoice currency</span></span>

10. <span data-ttu-id="12d1d-269">Legg til følgende felt fra rutenettlinjene på siden:</span><span class="sxs-lookup"><span data-stu-id="12d1d-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="12d1d-270">Innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="12d1d-270">Procurement category</span></span>
    - <span data-ttu-id="12d1d-271">Antall</span><span class="sxs-lookup"><span data-stu-id="12d1d-271">Quantity</span></span>
    - <span data-ttu-id="12d1d-272">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="12d1d-272">Unit price</span></span>
    - <span data-ttu-id="12d1d-273">Nettobeløp for linje</span><span class="sxs-lookup"><span data-stu-id="12d1d-273">Line net amount</span></span>
    - <span data-ttu-id="12d1d-274">1099-beløp</span><span class="sxs-lookup"><span data-stu-id="12d1d-274">1099 amount</span></span>

11. <span data-ttu-id="12d1d-275">Når du har lagt til alle feltene fra de forrige to trinnene, klikker du **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="12d1d-276">Siden må ligne på følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="12d1d-276">The page must resemble the following illustration.</span></span>
    <span data-ttu-id="12d1d-277">[![Side når felt er lagt til](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="12d1d-278">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="12d1d-279">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="12d1d-280">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="12d1d-281">Arbeidsflythandlinger</span><span class="sxs-lookup"><span data-stu-id="12d1d-281">Workflow actions</span></span>

<span data-ttu-id="12d1d-282">Hvis du vil legge til arbeidsflythandlinger, kan du bruke siden **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="12d1d-283">Hvis du vil åpne denne siden, erstatter du navnet på menyelementet i URL-adressen, slik du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="12d1d-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="12d1d-284">Åpne deretter utformingen for mobil fra **Innstillinger** (tannhjul)-knappen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="12d1d-285">Følg disse trinnene for å legge til handlinger i arbeidsflyten på detaljer-siden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="12d1d-286">Du må ha fakturaer tilordnet til deg som er i den tilstanden som gjør arbeidsflythandlingene du skal utforme for, tilgjengelige for deg.</span><span class="sxs-lookup"><span data-stu-id="12d1d-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="12d1d-287">Registrere arbeidsflythandlinger</span><span class="sxs-lookup"><span data-stu-id="12d1d-287">Record workflow actions</span></span>
1.  <span data-ttu-id="12d1d-288">Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="12d1d-289">Velg siden **Mine leverandørfakturaer** som du opprettet tidligere, og klikk deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="12d1d-290">På kategorien **Handlinger** klikker du **Legg til handling**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="12d1d-291">Angi en tittel for handling, som **Godkjenn**, og en beskrivelse, som **Godkjenn faktura**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="12d1d-292">Legg merke til at handlingstittelen du angir her, blir navnet på handlingen som vises for brukeren i den mobile app.</span><span class="sxs-lookup"><span data-stu-id="12d1d-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="12d1d-293">Klikk **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-293">Click **Done**.</span></span>
6.  <span data-ttu-id="12d1d-294">Klikk **Velg felt**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="12d1d-295">Gå gjennom arbeidsflytprosessen på siden **VendMobileInvoiceHeaderDetails**, og fullfør handlingen som du vil registrere.</span><span class="sxs-lookup"><span data-stu-id="12d1d-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="12d1d-296">Kontroller at du skriver inn kommentarer for arbeidsflyten under denne prosessen, slik at et kommentarfelt også er inkludert i mobilopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="12d1d-297">Når arbeidsflythandlingen er utført, klikker du **Ferdig** å fullføre Velg felt-oppgaven.</span><span class="sxs-lookup"><span data-stu-id="12d1d-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="12d1d-298">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="12d1d-299">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="12d1d-300">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="12d1d-301">Gjenta de forrige trinnene for å registrere alle nødvendige arbeidsflythandlinger.</span><span class="sxs-lookup"><span data-stu-id="12d1d-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="12d1d-302">Opprette en .js-fil</span><span class="sxs-lookup"><span data-stu-id="12d1d-302">Create a .js file</span></span>
1. <span data-ttu-id="12d1d-303">Åpne Notisblokk eller Microsoft Visual Studio, og lim inn følgende kode.</span><span class="sxs-lookup"><span data-stu-id="12d1d-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="12d1d-304">Lagre filen som en .js-fil.</span><span class="sxs-lookup"><span data-stu-id="12d1d-304">Save the file as a .js file.</span></span> <span data-ttu-id="12d1d-305">Denne koden gjør følgende:</span><span class="sxs-lookup"><span data-stu-id="12d1d-305">This code does the following:</span></span>
    - <span data-ttu-id="12d1d-306">De ekstra arbeidsflytrelaterte kolonnene som vi tidligere lagt til på den mobile listesiden, skjules.</span><span class="sxs-lookup"><span data-stu-id="12d1d-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="12d1d-307">Vi har lagt til disse kolonnene slik at appen får denne informasjonen i kontekst og kan utføre det neste trinnet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="12d1d-308">Basert på arbeidsflyttrinnet som er aktivt, brukes logikk til å vise bare disse handlingene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="12d1d-309">Navnet på sidene og andre kontroller i JS-koden må være de samme som navnene i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="12d1d-310">Last opp kodefilen til arbeidsområdet ved å velge **Logic**-kategorien</span><span class="sxs-lookup"><span data-stu-id="12d1d-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="12d1d-311">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="12d1d-312">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="12d1d-313">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="12d1d-314">Leverandørfakturavedlegg</span><span class="sxs-lookup"><span data-stu-id="12d1d-314">Vendor invoice attachments</span></span>

1. <span data-ttu-id="12d1d-315">Klikk på **Innstillinger** (tannhjul)-knappen øverst til høyre på siden, og klikk deretter **Mobile app**</span><span class="sxs-lookup"><span data-stu-id="12d1d-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2. <span data-ttu-id="12d1d-316">Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3. <span data-ttu-id="12d1d-317">Velg siden <strong>Fakturadetaljer \*\*som du opprettet tidligere, og klikk deretter \*\*Rediger</strong> .</span><span class="sxs-lookup"><span data-stu-id="12d1d-317">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>
4. <span data-ttu-id="12d1d-318">Angi **Dokumentbehandling** til **Ja** som vist nedenfor.</span><span class="sxs-lookup"><span data-stu-id="12d1d-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="12d1d-319">**Obs!** Hvis det er ingen krav til å vise vedlegg på den mobile enheten, kan du la dette alternativet være angitt til **Nei**, som er standardinnstillingen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   <span data-ttu-id="12d1d-320">![Dokumentstyring](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-320">![Document management](./media/docmanagement-216x300.png)</span></span>
5. <span data-ttu-id="12d1d-321">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-321">Click **Done** to exit edit mode.</span></span>
6. <span data-ttu-id="12d1d-322">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-322">Click **Back** and then **Done** to exit the workspace</span></span>
7. <span data-ttu-id="12d1d-323">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="12d1d-324">Leverandørfakturalinjedistribusjoner</span><span class="sxs-lookup"><span data-stu-id="12d1d-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="12d1d-325">Kravene for dette scenariet bekrefter at det vil bli bare distribusjoner på linjenivå, og at en faktura har alltid bare én linje.</span><span class="sxs-lookup"><span data-stu-id="12d1d-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="12d1d-326">Fordi dette scenariet er enkelt, må også brukeropplevelsen på den mobile enheten være enkel nok til at brukeren ikke trenger å bore ned flere nivåer for å vise distribusjonen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="12d1d-327">Leverandørfakturaer omfatter muligheten til å vise alle distribusjoner fra fakturahodet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-327">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="12d1d-328">Denne opplevelsen er det vi trenger for det mobile scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="12d1d-329">Derfor vil vi bruke siden **VendMobileInvoiceAllDistributionTree** til å utforme denne delen av det mobile scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="12d1d-330">Å kjenne kravene hjelper oss med å bestemme hvilke bestemte siden for å bruke og hvordan nøyaktig å optimalisere mobil opplevelse for brukeren når vi utformer scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="12d1d-331">Vi vil bruke en annen side til å vise distribusjoner, fordi har ulike krav for scenariet, i det andre scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="12d1d-332">Erstatt navnet på menyelementet i URL-adressen, slik du gjorde tidligere.</span><span class="sxs-lookup"><span data-stu-id="12d1d-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="12d1d-333">Siden som vises bør ligne på følgende illustrasjon.</span><span class="sxs-lookup"><span data-stu-id="12d1d-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="12d1d-334">[![Alle distribusjoner-siden](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="12d1d-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="12d1d-335">Åpne utformingen for mobil fra **Innstillinger** (tannhjul)-knappen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="12d1d-336">Klikk på **Rediger**-knappen for å starte redigeringsmodus i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="12d1d-337">**Obs!** Du skal se at to nye sider ble opprettet automatisk.</span><span class="sxs-lookup"><span data-stu-id="12d1d-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="12d1d-338">Fordi du har aktivert dokumentbehandling i den forrige delen, oppretter systemet disse sidene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="12d1d-339">Du kan ignorere disse nye sider.</span><span class="sxs-lookup"><span data-stu-id="12d1d-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="12d1d-340">Klikk **Legg til side**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="12d1d-341">Angi en sidetittel, som **Vis regnskap**, og en beskrivelse, som **Vis regnskap for fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="12d1d-342">Klikk **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-342">Click **Done**.</span></span>
7.  <span data-ttu-id="12d1d-343">På kategorien **Felt**, klikk **Velg felt**, velg du følgende felt fra siden med distribusjoner, og klikk deretter **Ferdig**:</span><span class="sxs-lookup"><span data-stu-id="12d1d-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="12d1d-344">Beløp</span><span class="sxs-lookup"><span data-stu-id="12d1d-344">Amount</span></span>
    2.  <span data-ttu-id="12d1d-345">Valuta</span><span class="sxs-lookup"><span data-stu-id="12d1d-345">Currency</span></span>
    3.  <span data-ttu-id="12d1d-346">Finanskonto</span><span class="sxs-lookup"><span data-stu-id="12d1d-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="12d1d-347">Vi valgte ikke **Beskrivelse**-kolonnen fra rutenettet over distribusjoner, fordi kravene for dette scenariet bekreftet at den utvidede prisen er bare beløpet som det skal være distribusjoner for.</span><span class="sxs-lookup"><span data-stu-id="12d1d-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="12d1d-348">Brukeren vil derfor ikke trenge et annet felt til å bestemme beløpet som er fordelingen for.</span><span class="sxs-lookup"><span data-stu-id="12d1d-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="12d1d-349">Men i neste scenario **vil** vi bruke denne informasjonen, fordi kravene for scenariet angir at andre beløpstyper har distribusjoner (for eksempel merverdiavgift).</span><span class="sxs-lookup"><span data-stu-id="12d1d-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="12d1d-350">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="12d1d-351">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="12d1d-352">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="12d1d-353">Mobilsiden **Vis regnskap** er ikke koblet til noen av mobilsidene som vi har utviklet så langt.</span><span class="sxs-lookup"><span data-stu-id="12d1d-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="12d1d-354">Fordi brukeren bør være i stand til å navigere til siden **Vis regnskap** fra siden **Fakturaopplysninger** på den mobile enheten, må vi gi navigasjon fra siden **Fakturaopplysninger** til siden **Vis regnskap**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="12d1d-355">Vi etablerer denne navigasjonen ved hjelp av ekstra logikk via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="12d1d-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="12d1d-356">Åpne .js-filen som du opprettet tidligere, og legg til linjene som er uthevet i følgende kode.</span><span class="sxs-lookup"><span data-stu-id="12d1d-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="12d1d-357">Denne koden gjør to ting:</span><span class="sxs-lookup"><span data-stu-id="12d1d-357">This code does two things:</span></span>
    1.  <span data-ttu-id="12d1d-358">Den hjelper å garantere at brukerne ikke kan gå direkte fra arbeidsområdet til siden **Vis regnskap**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="12d1d-359">Den oppretter en navigasjonskontroll fra siden **Fakturaopplysninger** til siden **Vis regnskap**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="12d1d-360">Navnet på sidene og andre kontroller i JS-koden må være de samme som navnene i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="12d1d-361">Last opp kodefilen til arbeidsområdet ved å velge **Logic**-kategorien for å overskrive den forrige koden</span><span class="sxs-lookup"><span data-stu-id="12d1d-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="12d1d-362">Klikk **Ferdig** for å avslutte redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="12d1d-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="12d1d-363">Klikk **Tilbake** og deretter **Ferdig** for å gå ut av arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="12d1d-364">Klikk **Publiser arbeidsområde** for å lagre arbeidet</span><span class="sxs-lookup"><span data-stu-id="12d1d-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="12d1d-365">Validering</span><span class="sxs-lookup"><span data-stu-id="12d1d-365">Validation</span></span>

<span data-ttu-id="12d1d-366">Åpne programmet fra mobilenheten, og koble til din forekomst.</span><span class="sxs-lookup"><span data-stu-id="12d1d-366">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="12d1d-367">Kontroller at du logger deg på firmaet der leverandørfakturaer er tilordnet til deg for gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="12d1d-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="12d1d-368">Du skal kunne utføre følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="12d1d-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="12d1d-369">Se arbeidsområdet **Mine godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="12d1d-370">Gå nedover i arbeidsområdet **Mine godkjenninger** og se siden **Mine leverandørfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="12d1d-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="12d1d-371">Gå nedover på siden **Mine leverandørfakturaer** og se en oversikt over fakturaer som er tilordnet til deg.</span><span class="sxs-lookup"><span data-stu-id="12d1d-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="12d1d-372">Gå nedover i en av fakturaene, og se fakturahodedetaljer og linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="12d1d-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="12d1d-373">På detaljer-siden ser du en kobling til vedlegg. Bruk denne koblingen til å navigere til vedleggslisten og vise vedleggene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="12d1d-374">På detaljer-siden ser du en kobling til siden **Vis regnskap**. Bruk denne koblingen til å navigere til distribusjonssiden og vise distribusjonene.</span><span class="sxs-lookup"><span data-stu-id="12d1d-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="12d1d-375">På detaljer-siden, klikker du **Handlinger**-menyen nederst, og utfør handlinger i arbeidsflyten som gjelder for arbeidsflyttrinnet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="12d1d-376">Utforme et scenario for godkjenning av komplisert faktura for Fabrikam</span><span class="sxs-lookup"><span data-stu-id="12d1d-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12d1d-377">Scenarieattributt</span><span class="sxs-lookup"><span data-stu-id="12d1d-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="12d1d-378">Svar</span><span class="sxs-lookup"><span data-stu-id="12d1d-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12d1d-379">Hvilke felt fra fakturahodet brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="12d1d-380">Navn på leverandør</span><span class="sxs-lookup"><span data-stu-id="12d1d-380">Vendor name</span></span></li>
<li><span data-ttu-id="12d1d-381">Fakturabeløp</span><span class="sxs-lookup"><span data-stu-id="12d1d-381">Invoice amount</span></span></li>
<li><span data-ttu-id="12d1d-382">Fakturakonto</span><span class="sxs-lookup"><span data-stu-id="12d1d-382">Invoice account</span></span></li>
<li><span data-ttu-id="12d1d-383">Fakturanummer</span><span class="sxs-lookup"><span data-stu-id="12d1d-383">Invoice number</span></span></li>
<li><span data-ttu-id="12d1d-384">Fakturadato</span><span class="sxs-lookup"><span data-stu-id="12d1d-384">Invoice date</span></span></li>
<li><span data-ttu-id="12d1d-385">Fakturabeskrivelse</span><span class="sxs-lookup"><span data-stu-id="12d1d-385">Invoice description</span></span></li>
<li><span data-ttu-id="12d1d-386">Forfallsdato</span><span class="sxs-lookup"><span data-stu-id="12d1d-386">Due date</span></span></li>
<li><span data-ttu-id="12d1d-387">Fakturavaluta</span><span class="sxs-lookup"><span data-stu-id="12d1d-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-388">Hvilke felt fra fakturalinjer brukeren vil se i mobil opplevelse, og i hvilken rekkefølge?</span><span class="sxs-lookup"><span data-stu-id="12d1d-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="12d1d-389">Innkjøpskategori</span><span class="sxs-lookup"><span data-stu-id="12d1d-389">Procurement category</span></span></li>
<li><span data-ttu-id="12d1d-390">Antall</span><span class="sxs-lookup"><span data-stu-id="12d1d-390">Quantity</span></span></li>
<li><span data-ttu-id="12d1d-391">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="12d1d-391">Unit price</span></span></li>
<li><span data-ttu-id="12d1d-392">Nettobeløp for linje</span><span class="sxs-lookup"><span data-stu-id="12d1d-392">Line net amount</span></span></li>
<li><span data-ttu-id="12d1d-393">1099-beløp</span><span class="sxs-lookup"><span data-stu-id="12d1d-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-394">Hvor mange fakturalinjene er det i en faktura?</span><span class="sxs-lookup"><span data-stu-id="12d1d-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="12d1d-395">Bruke 80-20 regelen her, og optimalisere 80 prosent.</span><span class="sxs-lookup"><span data-stu-id="12d1d-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="12d1d-396">5</span><span class="sxs-lookup"><span data-stu-id="12d1d-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-397">Brukere vil se regnskapsdistribusjoner (fakturakoding) på den mobile enheten under anmeldelser?</span><span class="sxs-lookup"><span data-stu-id="12d1d-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="12d1d-398">Ja</span><span class="sxs-lookup"><span data-stu-id="12d1d-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-399">Hvor mange regnskapsdistribusjoner (utvidet pris, merverdiavgift, tillegg og så videre) er det for en fakturalinje?</span><span class="sxs-lookup"><span data-stu-id="12d1d-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="12d1d-400">Igjen, bruke 80-20 regelen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="12d1d-401">Utvidet pris: 2 mva: 2 gebyrer: 2</span><span class="sxs-lookup"><span data-stu-id="12d1d-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12d1d-402">Fakturaene også har regnskapsdistribusjoner i fakturahodet?</span><span class="sxs-lookup"><span data-stu-id="12d1d-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="12d1d-403">I så fall bør disse regnskapsdistribusjoner være tilgjengelig på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="12d1d-404">Brukes ikke</span><span class="sxs-lookup"><span data-stu-id="12d1d-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12d1d-405">Brukere vil se vedlegg for fakturaen på enheten?</span><span class="sxs-lookup"><span data-stu-id="12d1d-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="12d1d-406">Ja</span><span class="sxs-lookup"><span data-stu-id="12d1d-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="12d1d-407">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="12d1d-407">Next steps</span></span>

<span data-ttu-id="12d1d-408">Følgende variasjoner kan gjøres for scenario 1, basert på kravene for scenario 2.</span><span class="sxs-lookup"><span data-stu-id="12d1d-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="12d1d-409">Du kan bruke denne delen til å forbedre opplevelsen av mobilappen.</span><span class="sxs-lookup"><span data-stu-id="12d1d-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="12d1d-410">Fordi flere fakturalinjer er forventet i scenario 2, hjelper følgende endringer i utformingen optimalisere brukerens opplevelse på den mobile enheten:</span><span class="sxs-lookup"><span data-stu-id="12d1d-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="12d1d-411">I stedet for å vise fakturalinjer på detaljer-siden (som i scenario 1), kan brukere velge å vise linjer på en egen side for mobil.</span><span class="sxs-lookup"><span data-stu-id="12d1d-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="12d1d-412">Fordi mer enn én fakturalinjen forventes i dette tilfellet hvis siden **VendMobileInvoiceAllDistributionTree** brukes til å utforme distribusjonssiden mobil (som i scenario 1), kan det være forvirrende for brukeren å koordinere linjer til distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="12d1d-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="12d1d-413">Bruk derfor siden **VendMobileInvoiceLineDistributionTree** til å utforme distribusjonssiden.</span><span class="sxs-lookup"><span data-stu-id="12d1d-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="12d1d-414">Ideelt sett bør distribusjonene vises i konteksten for en fakturalinje i dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="12d1d-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="12d1d-415">Sørg derfor for at brukeren kan gå til en linje for å se siden distribusjoner.</span><span class="sxs-lookup"><span data-stu-id="12d1d-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="12d1d-416">Bruk sidekoblingsmuligheten til å opprette gjennomgangen, akkurat som du gjorde for hode- og detaljer-sidene i scenario 1.</span><span class="sxs-lookup"><span data-stu-id="12d1d-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="12d1d-417">Fordi mer enn én beløpstype forventes på distribusjoner i scenario 2 (merverdiavgift, gebyrer og så videre), vil det være nyttig å vise beskrivelsen av beløpstype.</span><span class="sxs-lookup"><span data-stu-id="12d1d-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="12d1d-418">(Vi har utelatt informasjonen i scenario 1.)</span><span class="sxs-lookup"><span data-stu-id="12d1d-418">(We omitted this information in scenario 1.)</span></span>




