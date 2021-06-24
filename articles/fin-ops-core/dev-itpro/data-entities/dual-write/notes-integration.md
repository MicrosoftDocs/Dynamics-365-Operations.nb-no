---
title: Merknadsintegrering
description: Dette emnet beskriver integreringen av merknadsdata i dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186792"
---
# <a name="note-integration"></a><span data-ttu-id="b13fc-103">Merknadsintegrering</span><span class="sxs-lookup"><span data-stu-id="b13fc-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b13fc-104">I forretningsprosesser samler Microsoft Dynamics 365-brukere ofte inn informasjon om kundene sine.</span><span class="sxs-lookup"><span data-stu-id="b13fc-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="b13fc-105">Denne informasjonen registreres som aktiviteter og merknader.</span><span class="sxs-lookup"><span data-stu-id="b13fc-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="b13fc-106">Dette emnet beskriver integreringen av merknadsdata i dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="b13fc-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="b13fc-107">Kundeopplysninger kan klassifiseres på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="b13fc-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="b13fc-108">**Handlingsbar informasjon som en Dynamics 365-bruker håndterer på vegne av en kunde** –  Contoso (en Dynamics 365-bruker) arrangerer for eksempel en spørrekonkurranse.</span><span class="sxs-lookup"><span data-stu-id="b13fc-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="b13fc-109">En av Contoso-kundene (en kunde) ønsker å delta i spørrekonkkurransen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="b13fc-110">Kunden ber en Contoso-ansatt om å reservere en plass i spørrekonkkurranse for dem.</span><span class="sxs-lookup"><span data-stu-id="b13fc-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="b13fc-111">Reservasjonen skjer i Contoso sin hendelseskalender for deltakeren.</span><span class="sxs-lookup"><span data-stu-id="b13fc-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="b13fc-112">**Informasjon som kan behandles for en Dynamics 365-bruker** – En kunde som kjøper en Surface-enhet, legger for eksempel inn spesielle instruksjoner som indikerer at enheten skal pakkes inn i gave før levering.</span><span class="sxs-lookup"><span data-stu-id="b13fc-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="b13fc-113">Disse instruksjonene er informasjon som kan behandles, og som bør behandles av Contoso-ansatte som er ansvarlig for emballasje.</span><span class="sxs-lookup"><span data-stu-id="b13fc-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="b13fc-114">**Informasjon som ikke kan behandles** – En kunde besøker for eksempel Contoso-butikken, og uttrykker interesse for *Halo*-spill og spilltilbehør i samtalen med butikkmedarbeideren.</span><span class="sxs-lookup"><span data-stu-id="b13fc-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="b13fc-115">Butikkmedarbeideren noterer seg denne informasjonen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="b13fc-116">Produktanbefalingsmotoren bruker deretter informasjonen til å foreta anbefalinger til kunden.</span><span class="sxs-lookup"><span data-stu-id="b13fc-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="b13fc-117">Som regel registreres informasjon som kan behandles, som *aktiviteter* i Finance and Operations-apper og Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="b13fc-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="b13fc-118">Informasjon som ikke kan behandles, blir lagret som *merknader* i Finance and Operations-apper, og som *kommentarer* i Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="b13fc-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="b13fc-119">Selv om notater er beregnet på informasjon som ikke kan behandles, vil ikke appene hindre deg i å bruke dem til å lagre og håndtere informasjon som kan behandles, hvis du vil bruke dem på denne måten.</span><span class="sxs-lookup"><span data-stu-id="b13fc-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="b13fc-120">Microsoft frigir funksjonalitet for merknadsintegrering.</span><span class="sxs-lookup"><span data-stu-id="b13fc-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="b13fc-121">(Funksjonalitet for aktivitetsintegrering blir frigitt senere.) Merknadsintegrasjon er tilgjengelig for kunder, leverandører, salgsordrer og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="b13fc-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="b13fc-122">Opprette en merknad i en Customer Engagement-app</span><span class="sxs-lookup"><span data-stu-id="b13fc-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="b13fc-123">Følg denne fremgangsmåten for å opprette et notat i en Customer Engagement-app og deretter synkronisere den med en Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="b13fc-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b13fc-124">Åpne kontoposten for en kunde i Customer Engagement-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="b13fc-125">I ruten **Tidslinje** velger du plusstegnet (**+**), og deretter velger du **Merknad** for å opprette en merknad.</span><span class="sxs-lookup"><span data-stu-id="b13fc-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Oppretting av en merknad i Customer Engagement-appen](media/notes-ce-1.png)

3. <span data-ttu-id="b13fc-127">Skriv inn en tittel og en beskrivelse, og velg deretter **Legg til merknad**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Angivelse av en tittel og en beskrivelse](media/notes-ce-2.png)

    <span data-ttu-id="b13fc-129">Den nye merknaden legges til på kundetidslinjen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-129">The new note is added to the customer timeline.</span></span>

    ![Ny merknad på kundetidslinjen](media/notes-ce-3.png)

4. <span data-ttu-id="b13fc-131">Logg på Finance and Operations-appen og åpne den samme kundeposten.</span><span class="sxs-lookup"><span data-stu-id="b13fc-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="b13fc-132">Legg merke til knappen **Vedlegg** (binderssymbol) i øvre høyre hjørne viser at posten har en tilknytning.</span><span class="sxs-lookup"><span data-stu-id="b13fc-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Varsling om en tilknytning](media/notes-ce-4.png)

5. <span data-ttu-id="b13fc-134">Velg knappen **Vedlegg** for å åpne siden **Vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="b13fc-135">Du bør finne merknaden du opprettet i Customer Engagement-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Merknad fra Customer Engagement-appen](media/notes-ce-5.png)

<span data-ttu-id="b13fc-137">Alle oppdateringer av merknaden synkroniseres frem og tilbake mellom Finance and Operations-appen og Customer Engagement-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="b13fc-138">Opprette en merknad i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="b13fc-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="b13fc-139">Du kan også opprette en merknad i en Finance and Operations-app, og den blir synkronisert til en Customer Engagement-app.</span><span class="sxs-lookup"><span data-stu-id="b13fc-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="b13fc-140">Følg denne fremgangsmåten for å opprette et notat i en Finance and Operations-app og deretter synkronisere den med en Customer Engagement-app.</span><span class="sxs-lookup"><span data-stu-id="b13fc-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b13fc-141">Velg **Ny** \> **merknad** på siden **Vedlegg** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Oppretting av en merknad i Finance and Operations-appen](media/notes-fo-1.png)

2. <span data-ttu-id="b13fc-143">Skriv inn en tittel og et kort sett med instruksjoner, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Angivelse av en tittel og instruksjoner](media/notes-fo-2.png)

3. <span data-ttu-id="b13fc-145">Oppdater posten i Customer Engagement-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="b13fc-146">Du bør finne det nye notatet på tidslinjen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-146">You should find the new note on the timeline.</span></span>

    ![Ny merknad på tidslinjen i Customer Engagement-appen](media/notes-fo-3.png)

<span data-ttu-id="b13fc-148">Du kan klassifisere en merknad som enten intern eller ekstern.</span><span class="sxs-lookup"><span data-stu-id="b13fc-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="b13fc-149">Åpne merknaden på siden **Vedlegg** i Finance and Operations-appen, og velg deretter **Intern** eller **Ekstern** i feltet **Begrensning**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Restriksjonsfelt](media/notes-fo-4.png)

<span data-ttu-id="b13fc-151">Du kan også opprette en URL.</span><span class="sxs-lookup"><span data-stu-id="b13fc-151">You can also create a URL.</span></span>

1. <span data-ttu-id="b13fc-152">Velg **Ny** \> **URL** på siden **Vedlegg** i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="b13fc-153">Angi en tittel og URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="b13fc-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="b13fc-154">Velg **Intern** eller **Ekstern** i feltet **Begrensning**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Oppretting av en URL-adresse i Finance and Operations-appen](media/notes-fo-5.png)

4. <span data-ttu-id="b13fc-156">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b13fc-156">Select **Save**.</span></span>

    <span data-ttu-id="b13fc-157">Ettersom Customer Engagement-apper ikke har en URL-type, er URL-adressen integrert med skrivetilgang som et notat.</span><span class="sxs-lookup"><span data-stu-id="b13fc-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL-adresse som vises som et notat i Customer Engagement-appen](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="b13fc-159">Filvedlegg støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="b13fc-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="b13fc-160">Maler</span><span class="sxs-lookup"><span data-stu-id="b13fc-160">Templates</span></span>

<span data-ttu-id="b13fc-161">Merknadsintegrering inkluderer en samling tabelltilordninger som fungerer sammen under datasamhandling, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="b13fc-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="b13fc-162">Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="b13fc-162">Finance and Operations app</span></span> | <span data-ttu-id="b13fc-163">Kundeengasjementsapp</span><span class="sxs-lookup"><span data-stu-id="b13fc-163">Customer engagement app</span></span> | <span data-ttu-id="b13fc-164">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b13fc-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="b13fc-165">Kundevedlegg</span><span class="sxs-lookup"><span data-stu-id="b13fc-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="b13fc-166">Merknader</span><span class="sxs-lookup"><span data-stu-id="b13fc-166">Annotations</span></span> | <span data-ttu-id="b13fc-167">Virksomheter som bruker ren tekst og URL-adresser, til å registrere kundespesifikk informasjon (for både organisasjoner og personer).</span><span class="sxs-lookup"><span data-stu-id="b13fc-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="b13fc-168">Vedlegg for leverandørdokument</span><span class="sxs-lookup"><span data-stu-id="b13fc-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="b13fc-169">Merknader</span><span class="sxs-lookup"><span data-stu-id="b13fc-169">Annotations</span></span> | <span data-ttu-id="b13fc-170">Virksomheter som bruker ren tekst og URL-adresser, til å registrere leverandørspesifikk informasjon (for både organisasjoner og personer).</span><span class="sxs-lookup"><span data-stu-id="b13fc-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="b13fc-171">Dokumentvedlegg for topptekst i salgsordre</span><span class="sxs-lookup"><span data-stu-id="b13fc-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="b13fc-172">Merknader</span><span class="sxs-lookup"><span data-stu-id="b13fc-172">Annotations</span></span> | <span data-ttu-id="b13fc-173">Virksomheter som bruker ren tekst og URL-adresser, til å registrere salgsordrespesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="b13fc-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="b13fc-174">Dokumentvedlegg for topptekst i bestilling</span><span class="sxs-lookup"><span data-stu-id="b13fc-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="b13fc-175">Merknader</span><span class="sxs-lookup"><span data-stu-id="b13fc-175">Annotations</span></span> | <span data-ttu-id="b13fc-176">Virksomheter som bruker ren tekst og URL-adresser, til å registrere bestillingspesifikk informasjon.</span><span class="sxs-lookup"><span data-stu-id="b13fc-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="b13fc-177">Begrensninger</span><span class="sxs-lookup"><span data-stu-id="b13fc-177">Limitations</span></span>

<span data-ttu-id="b13fc-178">Når du har installert merknadsløsningen, kan du ikke avinstallere den.</span><span class="sxs-lookup"><span data-stu-id="b13fc-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="b13fc-179">Hvis du vil ha mer informasjon, kan du se [Referanse for lesetilgang til skrivetilgang](mapping-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b13fc-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
