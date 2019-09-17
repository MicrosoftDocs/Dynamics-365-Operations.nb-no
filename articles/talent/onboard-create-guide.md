---
title: Opprette og sende en veiledning for jobbintroduksjon med Dynamics 365 for Talent - Onboard
description: Dette emnet forklarer hvordan du bruker Microsoft Dynamics 365 for Talent - Onboard-appen til å opprette en jobbintroduksjonsveiledning for nyansatte. Denne oppgaven er et viktig første skritt i en ansettelse-til-pensjonering-strategi for administrasjon av menneskelig kapital (HCM).
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: de5d584e3b7edba2751aa0c83b0465df2c3e4f7d
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731592"
---
# <a name="create-and-send-an-onboarding-guide-by-using-dynamics-365-for-talent-onboard"></a><span data-ttu-id="fba18-104">Opprette og sende en veiledning for jobbintroduksjon med Dynamics 365 for Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="fba18-104">Create and send an onboarding guide by using Dynamics 365 for Talent: Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fba18-105">Med Microsoft Dynamics 365 for Talent: Onboard kan du opprette jobbintroduksjonsveiledninger fra maler som du har opprettet selv, fra maler som er tilgjengelige i et galleri, eller fra bunnen av.</span><span class="sxs-lookup"><span data-stu-id="fba18-105">Microsoft Dynamics 365 for Talent: Onboard lets you create onboarding guides from templates that you created yourself, from templates that are available in a gallery, or from scratch.</span></span>

<span data-ttu-id="fba18-106">Når du har opprettet en jobbintroduksjonsveiledning, kan du sende den til en nyansatt.</span><span class="sxs-lookup"><span data-stu-id="fba18-106">After you've created an onboarding guide, you can send it to a new hire.</span></span> <span data-ttu-id="fba18-107">Alternativt kan du sende den til flere nyansatte som du angir i en Microsoft Excel-fil som du laster ned fra Onboard-appen.</span><span class="sxs-lookup"><span data-stu-id="fba18-107">Alternatively, you can send it to multiple new hires that you specify in a Microsoft Excel file that you download from the Onboard app.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-a-single-new-hire"></a><span data-ttu-id="fba18-108">Opprette en jobbintroduksjonsveiledning fra en mal og sende den til én nyansatt</span><span class="sxs-lookup"><span data-stu-id="fba18-108">Create an onboarding guide from a template and send it to a single new hire</span></span>

1. <span data-ttu-id="fba18-109">Velg **Maler** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="fba18-109">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="fba18-110">Under **Mine maler** velger du malen du vil konfigurere som jobbintroduksjonsveiledning for den nyansatte.</span><span class="sxs-lookup"><span data-stu-id="fba18-110">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hire.</span></span>
3. <span data-ttu-id="fba18-111">Rediger malen som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="fba18-111">Edit the template as you desire.</span></span> <span data-ttu-id="fba18-112">Husk å lagre arbeidet underveis.</span><span class="sxs-lookup"><span data-stu-id="fba18-112">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="fba18-113">Når du er ferdig med å redigere malen, **velger du**Opprett veiledning.</span><span class="sxs-lookup"><span data-stu-id="fba18-113">When you've finished editing the template, select **Create guide**.</span></span>

    <span data-ttu-id="fba18-114">[![Opprette en veiledning for jobbintroduksjon fra en mal](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span><span class="sxs-lookup"><span data-stu-id="fba18-114">[![Creating an onboarding guide from a template](./media/onboard-create-guide.png)](./media/onboard-create-guide.png)</span></span>

5. <span data-ttu-id="fba18-115">I vinduet **Opprett en veiledning** under **Hvem introduserer du** skriver du inn navnet eller e-postadressen til den nyansatte.</span><span class="sxs-lookup"><span data-stu-id="fba18-115">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="fba18-116">Hvis den nyansatte ikke finnes i systemet ennå, velger du **Legg til nå** og angir den ansattes informasjon.</span><span class="sxs-lookup"><span data-stu-id="fba18-116">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="fba18-117">Angi informasjon for veiledningen for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="fba18-117">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

6. <span data-ttu-id="fba18-118">Under **Når starter de** velger du en startdato.</span><span class="sxs-lookup"><span data-stu-id="fba18-118">Under **When do they start**, select a start date.</span></span>
7. <span data-ttu-id="fba18-119">Hvis veiledningen for jobbintroduksjon skal sendes automatisk til den nyansatte på en bestemt dato, må du kontrollere at alternativet **Planlegg en dato for automatisk sending** er slått på, og deretter velge den automatiske sendedatoen.</span><span class="sxs-lookup"><span data-stu-id="fba18-119">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="fba18-120">Hvis du vil sende veiledningen med en gang, deaktiverer du alternativet **Planlegg en dato for automatisk sending**.</span><span class="sxs-lookup"><span data-stu-id="fba18-120">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
8. <span data-ttu-id="fba18-121">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="fba18-121">Select **Done**.</span></span>
9. <span data-ttu-id="fba18-122">Når du er ferdig med å redigere veiledningen for jobbintroduksjon, velger du **Send** i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="fba18-122">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="fba18-123">Følg deretter ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fba18-123">Then follow one of these steps:</span></span>

    - <span data-ttu-id="fba18-124">Hvis du vil sende den nyansatte en kobling til veiledningen for jobbintroduksjon, velger du **kopier en kobling** og velger deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="fba18-124">To send the new hire a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="fba18-125">Hvis du vil tilpasse e-posten for jobbintroduksjonsveiledningen før du sender den, velger du **Tilpass e-posten før sending**, velger **Neste**, tilpasser e-posten som du ønsker, og velger deretter **Send**.</span><span class="sxs-lookup"><span data-stu-id="fba18-125">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="fba18-126">Hvis du vil sende e-posten uten å tilpasse den, velger du **Neste**og velger deretter **Send**.</span><span class="sxs-lookup"><span data-stu-id="fba18-126">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-an-onboarding-guide-from-a-template-and-send-it-to-multiple-new-hires"></a><span data-ttu-id="fba18-127">Opprette en jobbintroduksjonsveiledning fra en mal og sende den til flere nyansatte</span><span class="sxs-lookup"><span data-stu-id="fba18-127">Create an onboarding guide from a template and send it to multiple new hires</span></span>

<span data-ttu-id="fba18-128">Med Onboard kan du sende en jobbintroduksjonsveiledning til flere nyansatte samtidig.</span><span class="sxs-lookup"><span data-stu-id="fba18-128">Onboard lets you send an onboarding guide to multiple new hires at the same time.</span></span>

1. <span data-ttu-id="fba18-129">Velg **Maler** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="fba18-129">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="fba18-130">Under **Mine maler** velger du malen du vil konfigurere som jobbintroduksjonsveiledning for de nyansatte.</span><span class="sxs-lookup"><span data-stu-id="fba18-130">Under **My templates**, select the template that you want to set up as an onboarding guide for the new hires.</span></span>
3. <span data-ttu-id="fba18-131">Rediger malen som du ønsker.</span><span class="sxs-lookup"><span data-stu-id="fba18-131">Edit the template as you desire.</span></span> <span data-ttu-id="fba18-132">Husk å lagre arbeidet underveis.</span><span class="sxs-lookup"><span data-stu-id="fba18-132">Be sure to save your work as you go.</span></span>
4. <span data-ttu-id="fba18-133">Når du er ferdig med å redigere malen, **velger du**Opprett veiledning.</span><span class="sxs-lookup"><span data-stu-id="fba18-133">When you've finished editing the template, select **Create guide**.</span></span>
5. <span data-ttu-id="fba18-134">I vinduet **Opprett en veiledning** velger du **Trenger du å introdusere flere personer samtidig**.</span><span class="sxs-lookup"><span data-stu-id="fba18-134">In the **Create a guide** window, select **Need to onboard multiple people at once**.</span></span>

    <span data-ttu-id="fba18-135">[![Opprette en veiledning for jobbintroduksjon for flere nyansatte](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span><span class="sxs-lookup"><span data-stu-id="fba18-135">[![Creating an onboarding guide for multiple new hires](./media/onboard-send-guide-multiple-people.png)](./media/onboard-send-guide-multiple-people.png)</span></span>

6. <span data-ttu-id="fba18-136">Velg **mal for nyansettelse**.</span><span class="sxs-lookup"><span data-stu-id="fba18-136">Select **new hire template**.</span></span>
7. <span data-ttu-id="fba18-137">Etter at XLSX-filen er lastet ned, velger du **Åpne**, angir ansattes informasjon i Excel-arbeidsboken og lagrer arbeidsboken.</span><span class="sxs-lookup"><span data-stu-id="fba18-137">After the .xlsx file is downloaded, select **Open**, enter the employees' information in the Excel workbook, and save the workbook.</span></span>

    <span data-ttu-id="fba18-138">[![Laste ned Excel-malen for å sende veiledningen for jobbintroduksjon til flere nyansatte](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="fba18-138">[![Downloading the Excel template for sending the onboarding guide to multiple new hires](./media/onboard-send-guide-download-spreadsheet.png)](./media/onboard-send-guide-download-spreadsheet.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="fba18-139">Før du kan redigere arbeidsboken, må du velge **Aktiver redigering** i Excel.</span><span class="sxs-lookup"><span data-stu-id="fba18-139">Before you can edit the workbook, you must select **Enable editing** in Excel.</span></span>
    > 
    > <span data-ttu-id="fba18-140">[![Aktivere redigering](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span><span class="sxs-lookup"><span data-stu-id="fba18-140">[![Enabling editing](./media/onboard-send-guide-enable-editing.png)](./media/onboard-send-guide-enable-editing.png)</span></span>

8. <span data-ttu-id="fba18-141">Dra Excel-arbeidsboken til det angitte området i vinduet **Opprett flere veiledninger**, eller klikk hvor som helst i området for å søke etter filen på datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="fba18-141">Drag the Excel workbook to the designated area in the **Create multiple guides** window, or click anywhere in that area to browse for the file on your computer.</span></span>

    <span data-ttu-id="fba18-142">[![Dra den redigerte arbeidsboken](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span><span class="sxs-lookup"><span data-stu-id="fba18-142">[![Dragging the edited workbook](./media/onboard-send-guide-drag-spreadsheet.png)](./media/onboard-send-guide-drag-spreadsheet.png)</span></span>

9. <span data-ttu-id="fba18-143">Når du er ferdig med å redigere veiledningen for jobbintroduksjon, velger du **Send** i øvre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="fba18-143">When you've finished editing the onboarding guide, select **Send** in the upper-right corner.</span></span> <span data-ttu-id="fba18-144">Følg deretter ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="fba18-144">Then follow one of these steps:</span></span>

    - <span data-ttu-id="fba18-145">Hvis du vil sende de nyansatte en kobling til veiledningen for jobbintroduksjon, velger du **kopier en kobling** og velger deretter **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="fba18-145">To send the new hires a link to the onboarding guide, select **copy a link**, and then select **Copy**.</span></span>
    - <span data-ttu-id="fba18-146">Hvis du vil tilpasse e-posten for jobbintroduksjonsveiledningen før du sender den, velger du **Tilpass e-posten før sending**, velger **Neste**, tilpasser e-posten som du ønsker, og velger deretter **Send**.</span><span class="sxs-lookup"><span data-stu-id="fba18-146">To customize the email for the onboarding guide before you send it, select **Customize the email before sending**, select **Next**, customize the email as you desire, and then select **Send**.</span></span>
    - <span data-ttu-id="fba18-147">Hvis du vil sende e-posten uten å tilpasse den, velger du **Neste**og velger deretter **Send**.</span><span class="sxs-lookup"><span data-stu-id="fba18-147">To send the email without customizing it, select **Next**, and then select **Send**.</span></span>

## <a name="create-a-guide-without-using-a-template"></a><span data-ttu-id="fba18-148">Opprette en veiledning uten å bruke mal</span><span class="sxs-lookup"><span data-stu-id="fba18-148">Create a guide without using a template</span></span>

<span data-ttu-id="fba18-149">Du trenger ikke alltid å opprette en veiledning fra en mal.</span><span class="sxs-lookup"><span data-stu-id="fba18-149">You don't always have to create a guide from a template.</span></span> <span data-ttu-id="fba18-150">Hvis du foretrekker det, kan du opprette en veiledning fra bunnene av i stedet.</span><span class="sxs-lookup"><span data-stu-id="fba18-150">If you prefer, you can create a guide from scratch instead.</span></span>

1. <span data-ttu-id="fba18-151">På menyen til venstre velger du **Veiledninger**, og deretter velger du **Legg til**-knappen (plusstegnet \[**+**\]).</span><span class="sxs-lookup"><span data-stu-id="fba18-151">On the left menu, select **Guides**, and then select the **Add** button (the plus sign \[**+**\]).</span></span>
2. <span data-ttu-id="fba18-152">I vinduet **Opprett en veiledning** under **Hvem introduserer du** skriver du inn navnet eller e-postadressen til den nyansatte.</span><span class="sxs-lookup"><span data-stu-id="fba18-152">In the **Create a guide** window, under **Who are you onboarding**, enter the new hire's name or email address.</span></span> <span data-ttu-id="fba18-153">Hvis den nyansatte ikke finnes i systemet ennå, velger du **Legg til nå** og angir den ansattes informasjon.</span><span class="sxs-lookup"><span data-stu-id="fba18-153">If the new hire isn't in the system yet, select **Add now**, and enter the employee's information.</span></span>

    ![[<span data-ttu-id="fba18-154">Angi informasjon for veiledningen for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="fba18-154">Entering information for the onboarding guide</span></span>](./media/onboard-create-a-guide-window.png)](./media/onboard-create-a-guide-window.png)

3. <span data-ttu-id="fba18-155">Under **Når starter de** velger du en startdato.</span><span class="sxs-lookup"><span data-stu-id="fba18-155">Under **When do they start**, select a start date.</span></span>
4. <span data-ttu-id="fba18-156">Hvis veiledningen for jobbintroduksjon skal sendes automatisk til den nyansatte på en bestemt dato, må du kontrollere at alternativet **Planlegg en dato for automatisk sending** er slått på, og deretter velge den automatiske sendedatoen.</span><span class="sxs-lookup"><span data-stu-id="fba18-156">If the onboarding guide should be sent automatically to the new hire on a specific date, make sure that the **Schedule an automatic send date** option is turned on, and then select the automatic send date.</span></span> <span data-ttu-id="fba18-157">Hvis du vil sende veiledningen med en gang, deaktiverer du alternativet **Planlegg en dato for automatisk sending**.</span><span class="sxs-lookup"><span data-stu-id="fba18-157">To send the guide immediately, turn off the **Schedule an automatic send date** option.</span></span>
5. <span data-ttu-id="fba18-158">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="fba18-158">Select **Done**.</span></span>

## <a name="save-a-guide-as-a-template"></a><span data-ttu-id="fba18-159">Lagre en veiledning som mal</span><span class="sxs-lookup"><span data-stu-id="fba18-159">Save a guide as a template</span></span>

<span data-ttu-id="fba18-160">Du kan lagre en jobbintroduksjonsveiledning som mal.</span><span class="sxs-lookup"><span data-stu-id="fba18-160">You can save an onboarding guide as a template.</span></span> <span data-ttu-id="fba18-161">På denne måten kan du spare tid når du skal opprette flere jobbintroduksjonsveiledninger senere.</span><span class="sxs-lookup"><span data-stu-id="fba18-161">In this way, you can save time when you must create more onboarding guides later.</span></span>

1. <span data-ttu-id="fba18-162">Velg **Veiledninger** på menyen til venstre.</span><span class="sxs-lookup"><span data-stu-id="fba18-162">On the left menu, select **Guides**.</span></span>
2. <span data-ttu-id="fba18-163">Velg **Mer**-knappen (ellipsen \[**...**\]) for veiledningen du vil opprette en mal fra, og velg deretter **Lagre som mal**.</span><span class="sxs-lookup"><span data-stu-id="fba18-163">Select the **More** button (the ellipsis \[**...**\]) for the guide that you want to create a template from, and then select **Save as template**.</span></span>

    ![[Lagre en jobbintroduksjonsveiledning som mal] (./media/onboard-save-guide-as-template.png)](./media/onboard-save-guide-as-template.png)

3. <span data-ttu-id="fba18-165">Skriv inn et navn på den nye malen i vinduet **Lagre som en ny mal**, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="fba18-165">In the **Save as a new template** window, enter a name for your new template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fba18-166">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="fba18-166">Next steps</span></span>

- [<span data-ttu-id="fba18-167">Redigere veiledninger og maler for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="fba18-167">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="fba18-168">Dele innhold med andre bidragsytere</span><span class="sxs-lookup"><span data-stu-id="fba18-168">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="fba18-169">Vise statusen for oppgaver og jobbintroduksjonsmedarbeidere</span><span class="sxs-lookup"><span data-stu-id="fba18-169">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="fba18-170">Opprette ansettelsesteam i Onboard</span><span class="sxs-lookup"><span data-stu-id="fba18-170">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="fba18-171">Se også</span><span class="sxs-lookup"><span data-stu-id="fba18-171">See also</span></span>

- [<span data-ttu-id="fba18-172">Prøve eller kjøpe Onboard-appen</span><span class="sxs-lookup"><span data-stu-id="fba18-172">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="fba18-173">Hva er nytt</span><span class="sxs-lookup"><span data-stu-id="fba18-173">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="fba18-174">Produktmerknader</span><span class="sxs-lookup"><span data-stu-id="fba18-174">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="fba18-175">Få kundestøtte</span><span class="sxs-lookup"><span data-stu-id="fba18-175">Get support</span></span>](./talent-support.md)
