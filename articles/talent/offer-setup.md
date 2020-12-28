---
title: Konfigurere tilbudsbehandling i Attract
description: Dette emnet beskriver hvordan du setter opp tilbud i Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462104"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="a8c41-103">Konfigurere tilbudsbehandling i Attract</span><span class="sxs-lookup"><span data-stu-id="a8c41-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8c41-104">Når en kandidat flyttes til tilbudstrinnet i Dynamics 365 Talent: Attract, må du forsikre deg om at tilbudene kan opprettes raskt for kandidaten, godkjent etter behov, og sendes ut til kandidaten.</span><span class="sxs-lookup"><span data-stu-id="a8c41-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="a8c41-105">Siden de fleste tilbud er standard, kan de opprettes fra maler som kan brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8c41-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="a8c41-106">I Attract er alle tilbud samlet i en pakke for tilbudet, som er en samling av ett eller flere tilbudsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a8c41-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="a8c41-107">Dette emnet viser alle trinnene som Attract-administrator vil bruke for å definere ulike tilbudspakkemaler som en del av funksjonen for tilbudsadministrasjon i Attract.</span><span class="sxs-lookup"><span data-stu-id="a8c41-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="a8c41-108">Brukere med roller som ikke er administrator, får ikke tilgang til disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="a8c41-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="a8c41-109">Tilbudsadministrasjonsfunksjonene er tilgjengelige som en del av tillegget for omfattende ansettelse.</span><span class="sxs-lookup"><span data-stu-id="a8c41-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="a8c41-110">Tilbudsdata</span><span class="sxs-lookup"><span data-stu-id="a8c41-110">Offer data</span></span> 

<span data-ttu-id="a8c41-111">Tilbudsdata er den minste enheten i tilbudspakkemalen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="a8c41-112">Et vanlig tilbud består av standardtekst og et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="a8c41-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="a8c41-113">Settene med verdier er de eneste delene som kan endres mellom tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="a8c41-114">Under opprettingen av tilbud er det viktigste aspektet som personen som oppretter tilbudet kan fokusere på, en liste over tilbudsdataplassholdere som finnes i en tilbudspakkemal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="a8c41-115">Hvis du vil angi data for tilbudet, kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a8c41-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="a8c41-116">Gå til **Tilbudsadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="a8c41-117">Utvid **Biblioteket**-delen i den venstre navigasjonsruten, og gå deretter til **Tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="a8c41-118">På **Tilbudsdata**-siden finnes delene **Kandidatdetaljer** og **Jobbdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="a8c41-119">Attract innehoder noen datatilbudsplassholdere som standard.</span><span class="sxs-lookup"><span data-stu-id="a8c41-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="a8c41-120">Det er inndelinger på siden for å organisere ulike tilbudsdataplassholdere sammen i logiske grupper.</span><span class="sxs-lookup"><span data-stu-id="a8c41-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="a8c41-121">Disse delene kan hjelpe med vedlikehold av tilbudsdata og populasjon av data under oppretting av tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="a8c41-122">Hvis du vil opprette en liste over verdier for en plassholder, laster du opp et Excel-regneark som har én kolonne med plassholderen som kolonnetittel og listen over valg i radene under.</span><span class="sxs-lookup"><span data-stu-id="a8c41-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="a8c41-123">Hvis det refereres til samme plassholder i et annet dataregelsett, må du kontrollere at de har et felles sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="a8c41-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="a8c41-124">For å opprette en ny tilbudsdatadel klikke på **Legg til en seksjon**, og angi et unikt navn for seksjonen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="a8c41-125">For å legge til tilbudsdataplassholdere i en seksjon klikk på **Legg til tilbudsdata**, og angi et unikt navn for plassholderen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="a8c41-126">Hvis du vil redigere navnet på en seksjon, holder du pekeren over navnet på seksjonen og oppdaterer navnet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="a8c41-127">Hvis du vil redigere navnet på eksisterende tilbudsdataplassholdere, må du først kontrollere at plassholderen ikke allerede er en del av en mal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="a8c41-128">Deretter holder du pekeren over navnet på plassholderen for tilbudsdata og oppdatere navnet etter behov.</span><span class="sxs-lookup"><span data-stu-id="a8c41-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="a8c41-129">Hvis du vil slette en eksisterende tilbudsdataplassholder, må du først kontrollere at plassholderen ikke er en del av en annen mal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="a8c41-130">Deretter holder du pekeren over plassholderen, og når papirkurvikonet vises, klikker du på papirkurven for å slette tilbudsdataplassholderen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="a8c41-131">Du kan se hvor mange maler som en plassholder for tilbudsdata er en del av, ved å se på tallindikatoren ved siden av hvert enkelt tilbudsdata.</span><span class="sxs-lookup"><span data-stu-id="a8c41-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="a8c41-132">Hvis du vil slette en seksjon, holder du pekeren over navnet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="a8c41-133">Hvis ingen av tilbudsdataplassholderne i seksjonen vises i en mal, kan du klikke på papirkurvikonet for å slette den.</span><span class="sxs-lookup"><span data-stu-id="a8c41-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="a8c41-134">Ved å slette seksjonen slettes også alle tilbudsdataplassholdere i seksjonen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="a8c41-135">Når tilbudsdataplassholderne er opprettet, kan du bruke dem på tvers av alle dokumentmaler.</span><span class="sxs-lookup"><span data-stu-id="a8c41-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="a8c41-136">Tilbudsdataplassholdere er ikke begrenset til en bestemt mal – samme sett kan brukes på tvers av alle maler.</span><span class="sxs-lookup"><span data-stu-id="a8c41-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="a8c41-137">Regler for tilbudsdata</span><span class="sxs-lookup"><span data-stu-id="a8c41-137">Offer data rules</span></span>

<span data-ttu-id="a8c41-138">De fleste organisasjoner har regler for hvordan tilbud må opprettes.</span><span class="sxs-lookup"><span data-stu-id="a8c41-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="a8c41-139">En organisasjon vil kanskje kreve at det maksimale årslønntilbudet for et bestemt sted og ansiennitetsnivå sammen må være innenfor et bestemt område, eller at det er bare noen få bestemte verdier som er mulige for tilbudsnivået for nyansettelsen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="a8c41-140">Attract støtter alle slike dataregler ved hjelp av en CSV-fil.</span><span class="sxs-lookup"><span data-stu-id="a8c41-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="a8c41-141">Når du skal klargjøre dataregel-CSV-filen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="a8c41-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="a8c41-142">Bestem tilbudsdataplassholderen for regelsettet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="a8c41-143">For eksempel **Årslønn**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="a8c41-144">Identifiser de avhengige tilbudsdataplassholderverdiene.</span><span class="sxs-lookup"><span data-stu-id="a8c41-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="a8c41-145">Eksempel **Jobbsted** og **Nivå**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="a8c41-146">Angi kolonne 1 og 2 som **Jobbsted** og **Nivå**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="a8c41-147">Hvis du vil laste opp en områdeverdi, kan du gjøre kolonnene 3 og 4 til **Årslønn**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="a8c41-148">Hvis du vil laste opp en bestemt verdi i stedet for et område, gjør du bare kolonne 3 til **Årslønn**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="a8c41-149">Fyll ut Microsoft Excel-filen basert på nødvendige rollene.</span><span class="sxs-lookup"><span data-stu-id="a8c41-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="a8c41-150">Kontroller at hver rad er en unik kombinasjon av alle verdier som er satt sammen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="a8c41-151">Lagre filen i CSV-format.</span><span class="sxs-lookup"><span data-stu-id="a8c41-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="a8c41-152">Gjør følgende for å laste opp regelfilen for tilbudsdata:</span><span class="sxs-lookup"><span data-stu-id="a8c41-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="a8c41-153">Gå til **Tilbudsadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="a8c41-154">Utvid **Bibliotek**-delen i det venstre navigasjonspanelet, og gå deretter til **Regler for tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="a8c41-155">Klikk **Nytt datasett** for å vise **Last opp**-dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="a8c41-156">Angi et unikt navn for regelsettet, og deretter last opp den lagrede CSV-filen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="a8c41-157">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-157">Click **Add**.</span></span>
    <span data-ttu-id="a8c41-158">Regelsettet behandles i bakgrunnen, og du blir varslet i programmet og via e-post når det er fullført.</span><span class="sxs-lookup"><span data-stu-id="a8c41-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="a8c41-159">Du vil varsles hvis det er feil under behandling av opplastingen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="a8c41-160">Deretter kan du laste ned feilloggen, rette filen og laste opp på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8c41-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="a8c41-161">Bruk ellipseknappen (**...**) hvis du vil laste ned regelsettet og oppdatere settet med verdier.</span><span class="sxs-lookup"><span data-stu-id="a8c41-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="a8c41-162">Når du har oppdatert, kan du laste opp filen på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8c41-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="a8c41-163">Du kan slette en eksisterende regelsettopplasting hvis plassholderen som defineres, ikke brukes i en annen dokumentmal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="a8c41-164">Hver plassholder kan bare ha ett unikt sett med kolonner som den er avhengig av.</span><span class="sxs-lookup"><span data-stu-id="a8c41-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="a8c41-165">Hvis for eksempel **Årslønn** er avhengig av **Jobbsted** og **Nivå**, kan du ikke laste opp et annet regelsett der **Årslønn** er avhengig av et annet sett med kolonner.</span><span class="sxs-lookup"><span data-stu-id="a8c41-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="a8c41-166">Du kan laste ned eksempelsett med tilbudsdata i kategorien **Eksempler** på siden **Regler for tilbudsdata**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="a8c41-167">Når en tilbudsoppretter overstyrer verdiene som er anbefalt av tilbudsdatareglene, flagges tilbudet som ikke-standard, og tilbudsgodkjenningsarbeidsflyten blir obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a8c41-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="a8c41-168">Dokumentmaler</span><span class="sxs-lookup"><span data-stu-id="a8c41-168">Document templates</span></span>

<span data-ttu-id="a8c41-169">En tilbudsdokumentmal kan hjelpe administratorer med å opprette tilbudsbrev.</span><span class="sxs-lookup"><span data-stu-id="a8c41-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="a8c41-170">Tilbudsdokumentmalen er en kombinasjon av teksten som skal inngå i tilbudet, i tillegg til de definerte tilbudsdataplassholderne.</span><span class="sxs-lookup"><span data-stu-id="a8c41-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="a8c41-171">Hvis du vil opprette en tilbudsdokumentmal, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a8c41-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="a8c41-172">Gå til **Tilbudsadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="a8c41-173">Utvid **Biblioteket**-delen i den venstre navigasjonsruten, og gå til **Maler**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="a8c41-174">**Maler**-siden viser en liste over dokumentmaler som allerede er definert.</span><span class="sxs-lookup"><span data-stu-id="a8c41-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="a8c41-175">Klikk **Ny mal** for å opprette en ny dokumentmal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="a8c41-176">Angi et unikt navn for malen, og klikk på **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="a8c41-177">Bruk redigeringsprogrammet for rik tekst til å sette inn eller redigere tilbudsdokumentinnholdet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="a8c41-178">Du kan sette inn tabeller, bilder og hyperkoblinger ved hjelp av alternativene som er tilgjengelige på toppen av tekstredigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="a8c41-179">Du kan sette inn tilbudsdataplassholdere i tilbudsmaldokumentet ved å:</span><span class="sxs-lookup"><span data-stu-id="a8c41-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="a8c41-180">Dra og slippe fra den høyre ruten.</span><span class="sxs-lookup"><span data-stu-id="a8c41-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="a8c41-181">Sett hashtag på tilbudsdataplassholderen direkte på posisjonen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="a8c41-182">Skriv inn **\#**, og skriv deretter inn navnet på tilbudsdataplassholderen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="a8c41-183">Alternativer vises i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="a8c41-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="a8c41-184">Klikk eller trykk på **Enter** for å sette inn tilbudsdataplassholderen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="a8c41-185">Hvis du vil tilknytte en plassholder til tilbudsdokumentmalen uten å vise verdien til kandidaten, holder du pekeren over tilbudsdataplassholderen og klikker på **Fest**-ikonet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="a8c41-186">Dette vil flytte plassholderen til **Festede tilbudsdata**-delen i tilbudsdokumentmalen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="a8c41-187">For å fjerne festingen følg de samme trinnene, men klikk på **Løsne** i listen over tilbudsdataplassholdere.</span><span class="sxs-lookup"><span data-stu-id="a8c41-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="a8c41-188">Hvis du vil vise listen over aktive tilbudsdataplassholdere, må du bytte til **Aktiv**-kategorien i høyre rute.</span><span class="sxs-lookup"><span data-stu-id="a8c41-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="a8c41-189">Hvis du setter inn en plassholder som styres av et tilbudsregeldatasett, kan du se avhengigheten for denne dataplassholderen på andre verdier.</span><span class="sxs-lookup"><span data-stu-id="a8c41-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="a8c41-190">Du kan også velge **Importer** for innholdet fra en DOCX-fil på den lokale maskinen og redigere etter behov.</span><span class="sxs-lookup"><span data-stu-id="a8c41-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="a8c41-191">På den måten behøver du ikke å skrive inn alt innholdet i redigeringsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="a8c41-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="a8c41-192">Hvis du vil forhåndsvise tilbudsdokumentet, kan du bruke **Forhåndsvisning**-alternativet øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="a8c41-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="a8c41-193">For å kontrollere om en tilbudsoppretter kan redigere dokumentinnholdet, bruk alternativet **Administrer tillatelse** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="a8c41-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="a8c41-194">Hvis du vil tilby oppretteren å bare sette inn plassholderverdier og ikke redigere tekst, angir du tillatelsesverdien til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="a8c41-195">Klikk på **Lagre** for å lagre progresjonen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="a8c41-196">Malen lagres i en kladdetilstand.</span><span class="sxs-lookup"><span data-stu-id="a8c41-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="a8c41-197">For å fullføre og merke dokumentet som publisert, klikker du på **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="a8c41-198">Du kan se hvilke dokumentmaler som er aktive, i utkastmodus, og som er arkiverte og er ikke lenger i bruk på startsiden for dokumentmalbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="a8c41-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="a8c41-199">Du kan slette alle tilbudsdokumentmaler som ikke er en del av en eksisterende tilbudspakkemal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="a8c41-200">Tilbudspakkemaler</span><span class="sxs-lookup"><span data-stu-id="a8c41-200">Offer package templates</span></span>

<span data-ttu-id="a8c41-201">Tilbudspakker er tilbudsartefaktene som deles med kandidaten og består av en kombinasjon av én eller flere tilbudsdokumentmaler.</span><span class="sxs-lookup"><span data-stu-id="a8c41-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="a8c41-202">Hvis du vil opprette en pakke, må du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="a8c41-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="a8c41-203">Gå til **Tilbudsadministrasjon**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="a8c41-204">Gå til **Pakker** i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="a8c41-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="a8c41-205">Det vises en liste over aktive pakkemaler som er tilgjengelige for tilbudsopprettere.</span><span class="sxs-lookup"><span data-stu-id="a8c41-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="a8c41-206">Trykk på **Ny pakke** for å opprette en ny tilbudspakke.</span><span class="sxs-lookup"><span data-stu-id="a8c41-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="a8c41-207">Angi et unikt navn, og klikk på **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="a8c41-208">Klikk på **Legg til mal**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="a8c41-209">Du kan velge å opprette en ny mal eller velge fra en eksisterende mal.</span><span class="sxs-lookup"><span data-stu-id="a8c41-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="a8c41-210">Hvis du vil legge til en eksisterende mal, må du kontrollere at tilbudsdokumentmalen ble lagret, fullført og merket som aktiv.</span><span class="sxs-lookup"><span data-stu-id="a8c41-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="a8c41-211">Du kan velge så mange dokumentmaler som du vil.</span><span class="sxs-lookup"><span data-stu-id="a8c41-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="a8c41-212">Klikk på **Ferdig** å gå tilbake til **Pakkestyring**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="a8c41-213">Du kan konfigurere rekkefølgen på dokumentene og også angi om det bestemte tilbudsdokumentet er nødvendig under oppretting av tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="a8c41-214">Personen som opprettet tilbudet, får muligheten til å slette dokumentene som er merket som **Ikke nødvendig**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="a8c41-215">For å lagre tilbudspakkemalen slik at den kan brukes av alle opprettere av tilbud, klikk på **Lagre og publiser**.</span><span class="sxs-lookup"><span data-stu-id="a8c41-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="a8c41-216">Hvis du vil vise utkast av tilbudspakkemaler, gå til **Kladder**-kategorien. Hvis det gjøres en endring i tilbudspakkemalen, må den lagres og publiseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="a8c41-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="a8c41-217">Konfigurere en tilbudsprosess</span><span class="sxs-lookup"><span data-stu-id="a8c41-217">Configure an offer process</span></span>

<span data-ttu-id="a8c41-218">Det er flere deler av tilbudsopprettingsprosessen som kan konfigureres av en Attract-administrator.</span><span class="sxs-lookup"><span data-stu-id="a8c41-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="a8c41-219">**Tilby godkjenninger** – Velg om tilbudsgodkjenninger kreves før tilbudet kan sendes til kandidaten.</span><span class="sxs-lookup"><span data-stu-id="a8c41-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="a8c41-220">Som administrator kan du også bestemme om alle tilbudsgodkjenninger skal skje i rekkefølge eller i en parallell godkjenningsarbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="a8c41-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="a8c41-221">Du kan også gjøre det obligatorisk om tilbudsgodskjennere må legge til en kommentar sammen med tilbudsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="a8c41-222">Tilbudsgodkjennere er obligatoriske for alle ikke-standard tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="a8c41-223">**Kandidatens tilbudserfaring** – Som administrator kan du velge å angi om alle tilbud skal ha en utløpsdato, og i så fall hva som skal være standard forskyvning for utløpsdatoen.</span><span class="sxs-lookup"><span data-stu-id="a8c41-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="a8c41-224">Du kan også konfigurere om kandidater kan avvise et tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="a8c41-225">**e-signaturer** - Som administrator kan du også velge metoden som kandidater kan bruke til å signere tilbud.</span><span class="sxs-lookup"><span data-stu-id="a8c41-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="a8c41-226">Adobe Sign - Alle tilbudspakker blir sendt og signert via Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="a8c41-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="a8c41-227">Hver tilbudsoppretter som publiserer tilbudet, må ha sin Adobe Sign-konto knyttet til Attract.</span><span class="sxs-lookup"><span data-stu-id="a8c41-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="a8c41-228">For Adobe Sign-lisenser og en kostnadsfri prøveversjon kan du velge denne [koblingen](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="a8c41-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="a8c41-229">DocuSign - Alle tilbudspakker blir sendt og signert via DocuSign.</span><span class="sxs-lookup"><span data-stu-id="a8c41-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="a8c41-230">Hver tilbudsoppretter som publiserer tilbudet, må ha sin DocuSign-konto knyttet til Attract.</span><span class="sxs-lookup"><span data-stu-id="a8c41-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="a8c41-231">ESign - Dette er standardvalget, som følger med som standard, der brukeren kan signere et tilbud ved å skrive inn navn og initialer.</span><span class="sxs-lookup"><span data-stu-id="a8c41-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="a8c41-232">Hvis du vil vite mer om tilbudsopprettingsprosessen, kan du se [Opprette, godkjenne og signere tilbud](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="a8c41-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
