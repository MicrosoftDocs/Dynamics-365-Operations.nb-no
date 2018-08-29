---
title: Konfigurere manuelle beslutninger i en arbeidsflyt
description: Dette emnet forklarer hvordan du konfigurerer egenskapene i en manuell beslutning.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: e942942aac5e9973ebd0a4e3f3a134b0c667ff5b
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="b3a40-103">Konfigurere manuelle beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="b3a40-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3a40-104">Dette emnet forklarer hvordan du konfigurerer egenskapene i en manuell beslutning.</span><span class="sxs-lookup"><span data-stu-id="b3a40-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="b3a40-105">Når du skal konfigurere en manuell beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den manuelle beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="b3a40-106">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for den manuelle beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="b3a40-107">Navn på beslutningen</span><span class="sxs-lookup"><span data-stu-id="b3a40-107">Name the decision</span></span>
<span data-ttu-id="b3a40-108">Følg denne fremgangsmåten for å sette et navn på den manuelle beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-108">Follow these steps to enter a name for the manual decision.</span></span>

1.  <span data-ttu-id="b3a40-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3a40-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="b3a40-110">I feltet **Navn** angir du et unikt navn på den manuelle beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="b3a40-111">Legg inn en emnelinje og instruksjoner</span><span class="sxs-lookup"><span data-stu-id="b3a40-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="b3a40-112">Du må skrive inn en emnelinje og instruksjoner til brukeren som er knyttet til den manuelle beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="b3a40-113">Hvis du for eksempel konfigurerer en beslutning for innkjøpsrekvisisjoner, ser brukeren som er tilordnet til beslutningen, emnelinjen og instruksjonene på **Innkjøpsrekvisisjoner**-siden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="b3a40-114">Emnelinjen vises i en meldingslinje øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="b3a40-115">Brukeren kan deretter klikke ikonet i meldingslinjen for å vise instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="b3a40-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="b3a40-116">Følg trinnene nedenfor for å legge inn en emnelinje og instruksjoner.</span><span class="sxs-lookup"><span data-stu-id="b3a40-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="b3a40-117">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3a40-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="b3a40-118">I **Emne for arbeidselement**-feltet i kategorien **Instruksjoner** angir du emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="b3a40-119">Hvis du vil tilpasse emnelinjen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="b3a40-120">Plassholdere erstattes med de riktige dataene når emnelinjen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="b3a40-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="b3a40-121">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="b3a40-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="b3a40-122">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="b3a40-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="b3a40-123">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="b3a40-124">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="b3a40-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="b3a40-125">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="b3a40-126">Hvis du vil legge til oversettelser av emnelinjen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="b3a40-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="b3a40-127">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="b3a40-128">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="b3a40-129">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="b3a40-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="b3a40-130">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="b3a40-131">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 3.</span><span class="sxs-lookup"><span data-stu-id="b3a40-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="b3a40-132">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-132">Click **Close**.</span></span>

5.  <span data-ttu-id="b3a40-133">I **Instruksjoner for arbeidselement**-feltet angir du instruksjonene.</span><span class="sxs-lookup"><span data-stu-id="b3a40-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="b3a40-134">Hvis du vil tilpasse instruksjonene, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="b3a40-135">Plassholdere erstattes med de riktige dataene når instruksjonene vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="b3a40-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="b3a40-136">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="b3a40-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="b3a40-137">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="b3a40-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="b3a40-138">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="b3a40-139">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="b3a40-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="b3a40-140">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="b3a40-141">Hvis du vil legge til oversettelser av instruksjonene, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="b3a40-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="b3a40-142">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="b3a40-143">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="b3a40-144">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="b3a40-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="b3a40-145">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="b3a40-146">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 6.</span><span class="sxs-lookup"><span data-stu-id="b3a40-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="b3a40-147">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="b3a40-148">Angi de mulige resultatene av en beslutning</span><span class="sxs-lookup"><span data-stu-id="b3a40-148">Specify the possible outcomes of a decision</span></span>
<span data-ttu-id="b3a40-149">Vanligvis når et dokument tilordnes til en beslutningstaker, får beslutningstakeren et spørsmål.</span><span class="sxs-lookup"><span data-stu-id="b3a40-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="b3a40-150">Svaret på dette spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="b3a40-151">Følg denne fremgangsmåten for å angi de mulige resultatene av den manuelle beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1.  <span data-ttu-id="b3a40-152">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3a40-152">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="b3a40-153">I kategorien **Resultater** i **Resultat 1**-feltet angir du navnet på resultatet eller alternativet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3.  <span data-ttu-id="b3a40-154">Hvis du vil legge til oversettelser av resultatet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="b3a40-154">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="b3a40-155">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-155">Click **Translations**.</span></span>
    2.  <span data-ttu-id="b3a40-156">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-156">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="b3a40-157">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="b3a40-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="b3a40-158">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-158">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="b3a40-159">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-159">Click **Close**.</span></span>

4.  <span data-ttu-id="b3a40-160">I **Resultat 2**-feltet angir du navnet på resultatet eller alternativet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5.  <span data-ttu-id="b3a40-161">Hvis du vil legge til oversettelser av resultatet, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="b3a40-161">To add translations of the outcome, follow these steps:</span></span>
    1.  <span data-ttu-id="b3a40-162">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-162">Click **Translations**.</span></span>
    2.  <span data-ttu-id="b3a40-163">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-163">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="b3a40-164">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="b3a40-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="b3a40-165">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-165">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="b3a40-166">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="b3a40-167">Angi når varslinger skal sendes</span><span class="sxs-lookup"><span data-stu-id="b3a40-167">Specify when notifications are sent</span></span>
<span data-ttu-id="b3a40-168">Du kan sende varslinger til personer når en beslutning er tatt, delegert eller videresendt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="b3a40-169">Følg fremgangsmåten nedenfor for å angi når meldinger skal sendes, og hvem de skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="b3a40-170">I den venstre ruten klikker du **Varslinger**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-170">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="b3a40-171">Merk av i avmerkingsboksen ved siden av hendelsene du vil sende meldinger for:</span><span class="sxs-lookup"><span data-stu-id="b3a40-171">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="b3a40-172">**\[Valg 1\]** – Den tilordnede brukeren har valgt **\[Valg 1\]**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    -   <span data-ttu-id="b3a40-173">**\[Valg 2\]** – Den tilordnede brukeren har valgt **\[Valg 2\]**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    -   <span data-ttu-id="b3a40-174">**Deleger** – Den tilordnede brukeren har tilordnet beslutningen til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="b3a40-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    -   <span data-ttu-id="b3a40-175">**Eskaler** – Den tilordnede brukeren har ikke tatt beslutningen innen fristen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3.  <span data-ttu-id="b3a40-176">Velg raden for en hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="b3a40-176">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="b3a40-177">I tekstfeltet i kategorien **Varslingstekst** skriver du inn teksten i meldingen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="b3a40-178">Hvis du vil tilpasse varslingen, kan du sette inn plassholdere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="b3a40-179">Plassholdere erstattes med de riktige dataene når varslingen vises til brukerne.</span><span class="sxs-lookup"><span data-stu-id="b3a40-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="b3a40-180">Følg denne fremgangsmåten for å sette inn en plassholder:</span><span class="sxs-lookup"><span data-stu-id="b3a40-180">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="b3a40-181">I tekstboksen klikker du der plassholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="b3a40-181">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="b3a40-182">Klikk **Sett inn plassholder**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-182">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="b3a40-183">I listen som vises, velger du plassholderen du vil sette inn.</span><span class="sxs-lookup"><span data-stu-id="b3a40-183">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="b3a40-184">Klikk **Sett inn**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-184">Click **Insert**.</span></span>

6.  <span data-ttu-id="b3a40-185">Hvis du vil legge til oversettelser av varslingen, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="b3a40-185">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="b3a40-186">Klikk **Oversettelser**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-186">Click **Translations**.</span></span>
    2.  <span data-ttu-id="b3a40-187">På siden som vises, klikker du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-187">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="b3a40-188">I listen som vises, velger du språket teksten angis på.</span><span class="sxs-lookup"><span data-stu-id="b3a40-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="b3a40-189">I **Oversatt tekst**-feltet legger du inn teksten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-189">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="b3a40-190">Hvis du vil tilpasse teksten, kan du sette inn plassholdere som beskrevet i trinn 5.</span><span class="sxs-lookup"><span data-stu-id="b3a40-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="b3a40-191">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-191">Click **Close**.</span></span>

7.  <span data-ttu-id="b3a40-192">I **Mottaker**-kategorien angir du hvem meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="b3a40-193">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 8.</span><span class="sxs-lookup"><span data-stu-id="b3a40-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="b3a40-194">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b3a40-194">Option</span></span></th>
    <th><span data-ttu-id="b3a40-195">Varslingsmottakere</span><span class="sxs-lookup"><span data-stu-id="b3a40-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="b3a40-196">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="b3a40-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="b3a40-197">Deltaker</span><span class="sxs-lookup"><span data-stu-id="b3a40-197">Participant</span></span></td>
    <td><span data-ttu-id="b3a40-198">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="b3a40-198">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-199">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som meldingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="b3a40-200">I <strong>Deltaker</strong>-listen velger du gruppen eller som varslingene skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="b3a40-201">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-201">Workflow user</span></span></td>
    <td><span data-ttu-id="b3a40-202">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="b3a40-202">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="b3a40-203">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="b3a40-204">Bruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-204">User</span></span></td>
    <td><span data-ttu-id="b3a40-205">Bestemte Microsoft Dynamics 365 for Finance and Operations-brukere</span><span class="sxs-lookup"><span data-stu-id="b3a40-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-206">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3a40-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="b3a40-207"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Finance and Operations-brukere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="b3a40-208">Velg brukerne du vil sende varslinger til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="b3a40-209">Gjenta trinn 3 til 7 for hver hendelse du valgte i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="b3a40-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="b3a40-210">Tilordne en beslutning</span><span class="sxs-lookup"><span data-stu-id="b3a40-210">Assign a decision</span></span>
<span data-ttu-id="b3a40-211">Følg denne fremgangsmåten for å angi hvem en manuell beslutning skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1.  <span data-ttu-id="b3a40-212">I den venstre ruten klikker du **Tilordning**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-212">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="b3a40-213">I **Tilordningstype**-kategorien velger du ett av alternativene i tabellen nedenfor og følger deretter de resterende trinnene for dette alternativet før du går til trinn 3.</span><span class="sxs-lookup"><span data-stu-id="b3a40-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="b3a40-214">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b3a40-214">Option</span></span></th>
    <th><span data-ttu-id="b3a40-215">Brukere som beslutningen er tilordnet til</span><span class="sxs-lookup"><span data-stu-id="b3a40-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="b3a40-216">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="b3a40-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="b3a40-217">Deltaker</span><span class="sxs-lookup"><span data-stu-id="b3a40-217">Participant</span></span></td>
    <td><span data-ttu-id="b3a40-218">Brukere som er tilordnet til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="b3a40-218">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-219">Når du har valgt <strong>Deltaker</strong>i <strong>Rollebasert</strong>-kategorien i <strong>Type deltaker</strong>-listen, velger du typen gruppe eller rolle som beslutningen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="b3a40-220">I <strong>Deltaker</strong>-listen velger du gruppen eller rollen som beslutningen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="b3a40-221">Hierarki</span><span class="sxs-lookup"><span data-stu-id="b3a40-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="b3a40-222">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="b3a40-222">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-223">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som beslutningen skal tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="b3a40-224">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="b3a40-225">Disse navnene representerer brukere som beslutningen kan tilordnes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="b3a40-226">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="b3a40-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="b3a40-227">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="b3a40-228">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3a40-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="b3a40-229">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="b3a40-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="b3a40-230">I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som beslutningen skal tilordnes til:</span><span class="sxs-lookup"><span data-stu-id="b3a40-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="b3a40-231"><strong>Tilordne til alle hentede brukere</strong> – Beslutningen tilordnes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="b3a40-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="b3a40-232"><strong>Bare tilordne til den siste hentede brukeren</strong> – Beslutningen tilordnes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="b3a40-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="b3a40-233"><strong>Utelat brukere med følgende vilkår</strong> – Beslutningen tilordnes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="b3a40-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="b3a40-234">Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="b3a40-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="b3a40-235">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-235">Workflow user</span></span></td>
    <td><span data-ttu-id="b3a40-236">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="b3a40-236">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="b3a40-237">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="b3a40-238">Bruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-238">User</span></span></td>
    <td><span data-ttu-id="b3a40-239">Bestemte Finance and Operations-brukere</span><span class="sxs-lookup"><span data-stu-id="b3a40-239">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-240">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3a40-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="b3a40-241"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Finance and Operations-brukere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="b3a40-242">Velg brukerne du vil tilordne beslutningen til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="b3a40-243">Kø</span><span class="sxs-lookup"><span data-stu-id="b3a40-243">Queue</span></span></td>
    <td><span data-ttu-id="b3a40-244">En arbeidselementkø</span><span class="sxs-lookup"><span data-stu-id="b3a40-244">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="b3a40-245">Når du har valgt <strong>Kø</strong>, klikker du <strong>Købasert</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3a40-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="b3a40-246">Gjør følgende for å tilordne beslutningen til en bestemt kø:</span><span class="sxs-lookup"><span data-stu-id="b3a40-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="b3a40-247">I <strong>Køtype</strong>-listen velger du <strong>Arbeidselementkøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3a40-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="b3a40-248">Velg køen i <strong>Kønavn</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="b3a40-249">Hvis en bestemt betingelse skal bestemme hvilken kø beslutningen skal tilordnes til, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="b3a40-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="b3a40-250">I <strong>Køtype</strong>-listen velger du <strong>Betingede arbeidselementkøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3a40-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="b3a40-251">I <strong>Kønavn</strong>-listen velger du <strong>Betinget kø</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3a40-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="b3a40-252">
    <strong>Merk:</strong> Dette alternativet brukes bare i noen få arbeidsflyter, for eksempel saksbehandling.</span><span class="sxs-lookup"><span data-stu-id="b3a40-252">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="b3a40-253">I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="b3a40-254">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="b3a40-254">Select one of the following options:</span></span>
    -   <span data-ttu-id="b3a40-255">**Timer** – Angi antallet timer som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="b3a40-256">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="b3a40-257">**Dager** – Angi antallet dager som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="b3a40-258">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="b3a40-259">**Uker** – Angi antallet uker som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    -   <span data-ttu-id="b3a40-260">**Måneder** – Velg dagen og uken som brukeren senest må ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="b3a40-261">Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="b3a40-262">**År** – Velg dagen, uken og måneden som brukeren senest må ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="b3a40-263">Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="b3a40-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="b3a40-264">Hvis brukeren ikke tar beslutningen innen fristen, er beslutningen forfalt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="b3a40-265">Et beslutning som er forfalt, videresendes, basert på alternativene du velger i **Eskalering**-området på siden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="b3a40-266">Angi hva som skal skje når en beslutning er forfalt</span><span class="sxs-lookup"><span data-stu-id="b3a40-266">Specify what happens when a decision is overdue</span></span>
<span data-ttu-id="b3a40-267">Hvis en bruker ikke tar beslutningen innen fristen, er beslutningen forfalt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="b3a40-268">En beslutning som er forfalt, kan videresendes eller tilordnes automatisk til en annen bruker.</span><span class="sxs-lookup"><span data-stu-id="b3a40-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="b3a40-269">Følg denne fremgangsmåten for å videresende beslutningen hvis den er forfalt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="b3a40-270">I den venstre ruten klikker du **Eskalering**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="b3a40-271">Merk av for **Bruk videresendingsbane** hvis du vil opprette en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="b3a40-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="b3a40-272">Systemet tilordner automatisk beslutningen til brukerne som er oppført i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="b3a40-273">Tabellen nedenfor er et eksempel på en videresendingsbane.</span><span class="sxs-lookup"><span data-stu-id="b3a40-273">For example, the following table represents an escalation path.</span></span>

   | <span data-ttu-id="b3a40-274">Sekvens</span><span class="sxs-lookup"><span data-stu-id="b3a40-274">Sequence</span></span> | <span data-ttu-id="b3a40-275">Videresendingsbane</span><span class="sxs-lookup"><span data-stu-id="b3a40-275">Escalation path</span></span>            |
   |----------|----------------------------|
   | <span data-ttu-id="b3a40-276">1</span><span class="sxs-lookup"><span data-stu-id="b3a40-276">1</span></span>        | <span data-ttu-id="b3a40-277">Tilordne til: Doris</span><span class="sxs-lookup"><span data-stu-id="b3a40-277">Assign to: Donna</span></span>           |
   | <span data-ttu-id="b3a40-278">2</span><span class="sxs-lookup"><span data-stu-id="b3a40-278">2</span></span>        | <span data-ttu-id="b3a40-279">Tilordne til: Elin</span><span class="sxs-lookup"><span data-stu-id="b3a40-279">Assign to: Erin</span></span>            |
   | <span data-ttu-id="b3a40-280">3</span><span class="sxs-lookup"><span data-stu-id="b3a40-280">3</span></span>        | <span data-ttu-id="b3a40-281">Endelig handling: \[Valg 1\]</span><span class="sxs-lookup"><span data-stu-id="b3a40-281">Final action: \[Choice 1\]</span></span> |

   <span data-ttu-id="b3a40-282">I dette eksempelet tilordnes den forfalte beslutningen til Doris.</span><span class="sxs-lookup"><span data-stu-id="b3a40-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="b3a40-283">Hvis Doris ikke tar beslutningen innen tidsfristen, tilordnes beslutningen til Elin.</span><span class="sxs-lookup"><span data-stu-id="b3a40-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="b3a40-284">Hvis Elin ikke tar beslutningen innen tidsfristen, velges **\[Valg 1\]** som beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>
3. <span data-ttu-id="b3a40-285">Klikk **Legg til videresending** for å legge til en bruker i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="b3a40-286">Velg ett av alternativene i tabellen nedenfor og følg deretter de resterende trinnene for dette alternativet før du går til trinn 4.</span><span class="sxs-lookup"><span data-stu-id="b3a40-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th><span data-ttu-id="b3a40-287">Alternativ</span><span class="sxs-lookup"><span data-stu-id="b3a40-287">Option</span></span></th>
   <th><span data-ttu-id="b3a40-288">Brukere som beslutningen videresendes til</span><span class="sxs-lookup"><span data-stu-id="b3a40-288">Users that the decision is escalated to</span></span></th>
   <th><span data-ttu-id="b3a40-289">Tilleggstrinn</span><span class="sxs-lookup"><span data-stu-id="b3a40-289">Additional steps</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td><span data-ttu-id="b3a40-290">Hierarki</span><span class="sxs-lookup"><span data-stu-id="b3a40-290">Hierarchy</span></span></td>
   <td><span data-ttu-id="b3a40-291">Brukere i et bestemt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="b3a40-291">Users in a specific organizational hierarchy</span></span></td>
   <td><ol>
   <li><span data-ttu-id="b3a40-292">Når du har valgt <strong>Hierarki</strong>i <strong>Hierarkivalg</strong>-kategorien i <strong>Hierarkitype</strong>-listen, velger du typen hierarki som beslutningen videresendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
   <li><span data-ttu-id="b3a40-293">Systemet må hente et område med brukernavn fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="b3a40-294">Disse navnene representerer brukere som beslutningen kan videresendes til.</span><span class="sxs-lookup"><span data-stu-id="b3a40-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="b3a40-295">Følg fremgangsmåten nedenfor for å angi start- og sluttpunktet for området med brukernavn som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="b3a40-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
   <li><span data-ttu-id="b3a40-296">Velg en person fra <strong>Start fra</strong>-listen for å angi startpunktet.</span><span class="sxs-lookup"><span data-stu-id="b3a40-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
   <li><span data-ttu-id="b3a40-297">Hvis du vil angi sluttpunktet, klikker du <strong>Legg til betingelse</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3a40-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="b3a40-298">Angi deretter en betingelse som bestemmer hvor i hierarkiet systemet slutter å hente navn.</span><span class="sxs-lookup"><span data-stu-id="b3a40-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
   </ol></li>
   <li><span data-ttu-id="b3a40-299">I kategorien <strong>Hierarkialternativer</strong> angir du hvilke brukere i området som beslutningen skal videresendes til:</span><span class="sxs-lookup"><span data-stu-id="b3a40-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
   <li><span data-ttu-id="b3a40-300"><strong>Tilordne til alle hentede brukere</strong> – Beslutningen videresendes til alle brukere i området.</span><span class="sxs-lookup"><span data-stu-id="b3a40-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
   <li><span data-ttu-id="b3a40-301"><strong>Bare tilordne til den siste hentede brukeren</strong> – Beslutningen videresendes bare til den siste brukeren i området.</span><span class="sxs-lookup"><span data-stu-id="b3a40-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
   <li><span data-ttu-id="b3a40-302"><strong>Utelat brukere med følgende vilkår</strong> – Beslutningen videresendes ikke til noen brukere i området som oppfyller et bestemt vilkår.</span><span class="sxs-lookup"><span data-stu-id="b3a40-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="b3a40-303">Klikk <strong>Legg til betingelse</strong> for å angi vilkåret.</span><span class="sxs-lookup"><span data-stu-id="b3a40-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
   </ul></li>
   </ol></td>
   </tr>
   <tr class="even">
   <td><span data-ttu-id="b3a40-304">Arbeidsflytbruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-304">Workflow user</span></span></td>
   <td><span data-ttu-id="b3a40-305">Brukere i den gjeldende arbeidsflyten</span><span class="sxs-lookup"><span data-stu-id="b3a40-305">Users in the current workflow</span></span></td>
   <td><ul>
   <li><span data-ttu-id="b3a40-306">Når du har valgt <strong>Arbeidsflytbruker</strong>i <strong>Arbeidsflytbruker</strong>-kategorien i <strong>Arbeidsflytbruker</strong>-listen, velger du en bruker som deltar i arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="b3a40-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td><span data-ttu-id="b3a40-307">Bruker</span><span class="sxs-lookup"><span data-stu-id="b3a40-307">User</span></span></td>
   <td><span data-ttu-id="b3a40-308">Bestemte Finance and Operations-brukere</span><span class="sxs-lookup"><span data-stu-id="b3a40-308">Specific Finance and Operations users</span></span></td>
   <td><ol>
   <li><span data-ttu-id="b3a40-309">Når du har valgt <strong>Bruker</strong>, klikker du <strong>Bruker</strong>-kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3a40-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
   <li><span data-ttu-id="b3a40-310"><strong>Tilgjengelige brukere</strong>-listen inkluderer alle Finance and Operations-brukere.</span><span class="sxs-lookup"><span data-stu-id="b3a40-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="b3a40-311">Velg brukerne du vil videresende beslutningen til, og flytt deretter disse brukerne til <strong>Valgte brukere</strong>-listen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
   </ol></td>
   </tr>
   </tbody>
   </table>

4. <span data-ttu-id="b3a40-312">I **Tidsbegrensning**-kategorien i **Varighet**-feltet angir du hvor lang tid brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="b3a40-313">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="b3a40-313">Select one of the following options:</span></span>
   -   <span data-ttu-id="b3a40-314">**Timer** – Angi antallet timer som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="b3a40-315">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="b3a40-316">**Dager** – Angi antallet dager som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="b3a40-317">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
   -   <span data-ttu-id="b3a40-318">**Uker** – Angi antallet uker som brukeren har til å ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
   -   <span data-ttu-id="b3a40-319">**Måneder** – Velg dagen og uken som brukeren senest må ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="b3a40-320">Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
   -   <span data-ttu-id="b3a40-321">**År** – Velg dagen, uken og måneden som brukeren senest må ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="b3a40-322">Du vil for eksempel at brukeren skal ta beslutningen innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="b3a40-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="b3a40-323">Gjenta trinn 3 og 4 for hver bruker som skal legges til i videresendingsbanen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="b3a40-324">Du kan endre rekkefølgen på brukerne.</span><span class="sxs-lookup"><span data-stu-id="b3a40-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="b3a40-325">Hvis brukerne i videresendingsbanen ikke tar beslutningen innen tidsfristen, vil systemet ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="b3a40-326">Hvis du vil angi alternativet systemet skal velge, merker du **Handling**-raden, og velger deretter et alternativ i kategorien **Avslutt handling**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="b3a40-327">Angi en tidsfrist</span><span class="sxs-lookup"><span data-stu-id="b3a40-327">Set a time limit</span></span>
<span data-ttu-id="b3a40-328">Følg denne fremgangsmåten hvis beslutningen må tas innen et bestemt tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-328">Follow these steps if the decision must be made in a specific time.</span></span> <span data-ttu-id="b3a40-329">**Obs!** Alternativene du velger i prosedyren, overstyrer alternativene du velger i **Tilordning**- og **Eskalering**-området på siden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="b3a40-330">Klikk **Avanserte innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="b3a40-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="b3a40-331">Merk av for **Angi en tidsgrense for arbeidsflytelementet**.</span><span class="sxs-lookup"><span data-stu-id="b3a40-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="b3a40-332">I **Varighet**-feltet angir du når beslutningen må tas.</span><span class="sxs-lookup"><span data-stu-id="b3a40-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="b3a40-333">Velg ett av følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="b3a40-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="b3a40-334">**Timer** – Angi antallet timer.</span><span class="sxs-lookup"><span data-stu-id="b3a40-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="b3a40-335">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="b3a40-336">**Dager** – Angi antallet dager.</span><span class="sxs-lookup"><span data-stu-id="b3a40-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="b3a40-337">Deretter velger du kalenderen som organisasjonen din bruker, og angir informasjon om organisasjonens arbeidsuke.</span><span class="sxs-lookup"><span data-stu-id="b3a40-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="b3a40-338">**Uker** – Angi antallet uker.</span><span class="sxs-lookup"><span data-stu-id="b3a40-338">**Weeks** – Enter the number of weeks.</span></span>
    -   <span data-ttu-id="b3a40-339">**Måneder** – Velg dagen og uken da beslutningen må være tatt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="b3a40-340">Du vil for eksempel at beslutningen skal tas innen fredag i den tredje uken i måneden.</span><span class="sxs-lookup"><span data-stu-id="b3a40-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="b3a40-341">**År** – Velg dagen, uken og måneden da beslutningen må være tatt.</span><span class="sxs-lookup"><span data-stu-id="b3a40-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="b3a40-342">Du vil for eksempel at beslutningen skal tas innen fredag i den tredje uken i desember.</span><span class="sxs-lookup"><span data-stu-id="b3a40-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="b3a40-343">Hvis tidsgrensen overskrides, vil systemet ta beslutningen.</span><span class="sxs-lookup"><span data-stu-id="b3a40-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="b3a40-344">I listen **Handling** velger du alternativet som systemet skal velge.</span><span class="sxs-lookup"><span data-stu-id="b3a40-344">In the **Action** list, select the option that the system should select.</span></span>





