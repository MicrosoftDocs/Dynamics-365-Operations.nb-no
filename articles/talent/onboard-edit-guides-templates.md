---
title: Redigere veiledninger og maler for jobbintroduksjon i Dynamics 365 Talent – Onboard
description: Dette emnet forklarer hvordan du legger til aktiviteter og annen informasjon i veiledninger og maler for jobbintroduksjon i Microsoft Dynamics 365 Talent – Onboard.
author: andreabichsel
manager: ''
ms.date: 06/19/2019
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
ms.search.validFrom: 2019-06-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0f4c68acfe021e736c259e91a40ce7d43d401246
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552008"
---
# <a name="edit-onboarding-guides-and-templates-in-dynamics-365-talent---onboard"></a><span data-ttu-id="3e4a5-103">Redigere veiledninger og maler for jobbintroduksjon i Dynamics 365 Talent – Onboard</span><span class="sxs-lookup"><span data-stu-id="3e4a5-103">Edit onboarding guides and templates in Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e4a5-104">Når du har opprettet en veiledning eller mal for jobbintroduksjon i Microsoft Dynamics 365 Talent: Onboard, må du legge til en innledning, aktiviteter, kontakter og ressurser.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-104">After you create an onboarding guide or template in Microsoft Dynamics 365 Talent: Onboard, you must add an introduction, activities, contacts, and resources.</span></span> <span data-ttu-id="3e4a5-105">I Onboard kan du ta med rikt innhold i jobbintroduksjonsveiledningene, inkludert:</span><span class="sxs-lookup"><span data-stu-id="3e4a5-105">Onboard lets you include rich content in your onboarding guides, including:</span></span>

- <span data-ttu-id="3e4a5-106">YouTube-videoer</span><span class="sxs-lookup"><span data-stu-id="3e4a5-106">YouTube videos</span></span>
- <span data-ttu-id="3e4a5-107">Microsoft Sway-presentasjoner</span><span class="sxs-lookup"><span data-stu-id="3e4a5-107">Microsoft Sway presentations</span></span>
- <span data-ttu-id="3e4a5-108">Microsoft PowerApps-apper</span><span class="sxs-lookup"><span data-stu-id="3e4a5-108">Microsoft PowerApps apps</span></span>
- <span data-ttu-id="3e4a5-109">Microsoft Stream-videoer</span><span class="sxs-lookup"><span data-stu-id="3e4a5-109">Microsoft Stream videos</span></span>
- <span data-ttu-id="3e4a5-110">Microsoft Forms-skjemaer</span><span class="sxs-lookup"><span data-stu-id="3e4a5-110">Microsoft Forms forms</span></span>
- <span data-ttu-id="3e4a5-111">Iframe som inneholder webinnhold</span><span class="sxs-lookup"><span data-stu-id="3e4a5-111">Iframes that contains web content</span></span>

## <a name="edit-introductions-or-activities-imported-from-a-template"></a><span data-ttu-id="3e4a5-112">Redigere introduksjoner eller aktiviteter som er importert fra en mal</span><span class="sxs-lookup"><span data-stu-id="3e4a5-112">Edit introductions or activities imported from a template</span></span>

<span data-ttu-id="3e4a5-113">Hvis du oppretter en jobbintroduksjonsveiledning fra en mal, eller hvis du importerer aktiviteter fra én mal til en annen, vil du se en **låseknapp** på de importerte aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-113">If you create an onboarding guide from a template, or if you import activities from one template into another, you'll notice a **Lock** button on the imported activities.</span></span> <span data-ttu-id="3e4a5-114">Disse kalles *administrerte aktiviteter*.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-114">These are called *managed activities*.</span></span>

<span data-ttu-id="3e4a5-115">[![Administrerte aktiviteter](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-115">[![Managed activities](./media/onboard-edit-guide-managed-activities.png)](./media/onboard-edit-guide-managed-activities.png)</span></span>

<span data-ttu-id="3e4a5-116">Når du velger en administrert aktivitet, kan du se kildemalen øverst i aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-116">When you select a managed activity, you can see the source template at the top of the activity.</span></span>

<span data-ttu-id="3e4a5-117">[![Kilde for administrert aktivitet](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-117">[![Managed activity source](./media/onboard-edit-guide-managed-activity-source.png)](./media/onboard-edit-guide-managed-activity-source.png)</span></span>

<span data-ttu-id="3e4a5-118">Hvis du redigerer en aktivitet i en mal, vil Onboard overføre endringene til alle maler og usendte veiledninger som er basert på denne malen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-118">If you edit an activity in a template, Onboard will push the changes to all templates and unsent guides that are based on that template.</span></span> <span data-ttu-id="3e4a5-119">Hvis du velger en usendt veiledning basert på en mal du har redigert, og velger deretter **Aktiviteter**-kategorien i veiledningen, vil du se en melding om at veiledningen er endret.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-119">If you select an unsent guide based on a template you edited and then select the **Activities** tab in the guide, you will see a notice that your guide has changed.</span></span> <span data-ttu-id="3e4a5-120">Velg **OK** for å forkaste varselet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-120">To dismiss the notification, select **OK**.</span></span> 

<span data-ttu-id="3e4a5-121">[![Endringsvarsel](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-121">[![Change notification](./media/onboard-edit-guide-change-notification.png)](./media/onboard-edit-guide-change-notification.png)</span></span>

<span data-ttu-id="3e4a5-122">Du ser en svart prikk ved siden av de oppdaterte aktivitetene.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-122">You'll see a black dot next to the updated activities.</span></span>

<span data-ttu-id="3e4a5-123">[![Endret aktivitet](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-123">[![Changed activity](./media/onboard-edit-guide-changed-activity.png)](./media/onboard-edit-guide-changed-activity.png)</span></span>

<span data-ttu-id="3e4a5-124">Du kan ikke redigere administrerte aktiviteter utenfor den opprinnelige malen, bortsett fra å legge til en tilordnet person, forfallsdato eller annen informasjon i den høyre delen av aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-124">You can't edit managed activities outside of the original template, except to add an assignee, due date, or other information in the right-hand section of the activity.</span></span>

<span data-ttu-id="3e4a5-125">Hvis du vil redigere en administrert aktivitet, eller hvis du ikke vil at en aktivitet skal motta oppdateringer fra malen den kom fra, velger du **Lås**-knappen for denne aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-125">If you want to edit a managed activity, or if you don't want an activity to receive updates from the template it came from, select the **Lock** button for that activity.</span></span> <span data-ttu-id="3e4a5-126">**Lås**-knappen vil forsvinne.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-126">The **Lock** button will disappear.</span></span> <span data-ttu-id="3e4a5-127">Aktiviteten blir ikke lenger administrert av den opprinnelige malen, og den vil ikke lenger motta oppdateringer fra denne malen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-127">The activity will no longer be managed by the original template, and it will no longer receive updates from that template.</span></span> <span data-ttu-id="3e4a5-128">Oppdateringer du gjør i en aktivitet, påvirker ikke den opprinnelige malen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-128">Updates you make to an activity do not affect the original template.</span></span>

<span data-ttu-id="3e4a5-129">Hvis du sletter en aktivitet fra en veiledning og overfører endringer fra malen for denne veiledningen, vil aktiviteten forbli slettet i veiledningen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-129">If you delete an activity from a guide and push changes from that guide's template, the activity will remain deleted in the guide.</span></span>

> [!NOTE]
> <span data-ttu-id="3e4a5-130">Kontakter og ressurser administreres ikke av maler.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-130">Contacts and resources aren't managed by templates.</span></span> <span data-ttu-id="3e4a5-131">I tillegg administreres ikke inndelinger, så hvis du legger til eller redigerer en inndeling i en mal, blir ikke endringene overført til noen veiledninger eller maler som bruker denne malen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-131">In addition, sections aren't managed, so if you add or edit a section in a template, the changes won't be pushed to any guides or templates that use that template.</span></span>
> 
> <span data-ttu-id="3e4a5-132">Hvis du legger til nye aktiviteter i en mal, overføres de nye aktivitetene til veiledninger og maler basert på denne malen, og de nye aktivitetene vises øverst.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-132">If you add new activities to a template, the new activities are pushed to guides and templates based on that template, and the new activities display at the top.</span></span>

## <a name="import-activities-from-another-template"></a><span data-ttu-id="3e4a5-133">Importere aktiviteter fra en annen mal</span><span class="sxs-lookup"><span data-stu-id="3e4a5-133">Import activities from another template</span></span>

<span data-ttu-id="3e4a5-134">Du kan importere aktiviteter fra én eller flere maler til en veiledning eller mal.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-134">You can import activities from one or more templates into a guide or template.</span></span>

1. <span data-ttu-id="3e4a5-135">Velg veiledningen eller malen du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-135">Select the guide or template you want to edit.</span></span>

2. <span data-ttu-id="3e4a5-136">Velg fanen **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-136">Select the **Activities** tab.</span></span>

3. <span data-ttu-id="3e4a5-137">Velg kategorien **Importer** i delen til høyre.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-137">Select the **Import** tab in the section on the right.</span></span>

   <span data-ttu-id="3e4a5-138">[![Importere aktiviteter](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-138">[![Import activities](./media/onboard-edit-guide-import-activities.png)](./media/onboard-edit-guide-import-activities.png)</span></span>

4. <span data-ttu-id="3e4a5-139">Hvis du vil forhåndsvise oppgavene i en ny fane i nettleseren, velger du knappen **Åpne i en ny kategori** i en mal.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-139">To preview the tasks in a new tab in your browser, select the **Open in new tab** button on any template.</span></span>

   <span data-ttu-id="3e4a5-140">[![Importere aktiviteter](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-140">[![Import activities](./media/onboard-edit-guide-preview-activities.png)](./media/onboard-edit-guide-preview-activities.png)</span></span>

5. <span data-ttu-id="3e4a5-141">Dra og slipp den ønskede malen på stedet i veiledningsmalen der du vil at aktivitetene skal vises.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-141">Drag and drop the desired template to the place in your guide template where you want the activities to appear.</span></span> <span data-ttu-id="3e4a5-142">Fortsett å redigere veiledningen eller malen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-142">Continue editing your guide or template.</span></span>

<span data-ttu-id="3e4a5-143">De importerte aktivitetene vil inneholde en **låseknapp**, som angir at disse aktivitetene administreres av malen du importerte fra.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-143">The imported activities will contain a **Lock** button, which indicates those activities are managed by the template you imported from.</span></span> <span data-ttu-id="3e4a5-144">Når du gjør endringer i malen du importerte, oppdateres disse aktivitetene i malen du importerte dem til.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-144">When you make changes to the template you imported, those activities will update in the template you imported them to.</span></span> <span data-ttu-id="3e4a5-145">Endringene vil imidlertid ikke bli overført automatisk til veiledninger som er opprettet fra malen du importerte til.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-145">However, the changes will not be pushed automatically to any guides created from the template you imported to.</span></span>

## <a name="push-changes-from-a-template-to-other-templates-or-guides"></a><span data-ttu-id="3e4a5-146">Overføre endringer fra en mal til andre maler eller veiledninger</span><span class="sxs-lookup"><span data-stu-id="3e4a5-146">Push changes from a template to other templates or guides</span></span>

<span data-ttu-id="3e4a5-147">Hvis du redigerer en mal som inneholder aktiviteter som brukes i andre maler eller veiledninger, må du overføre endringene hvis du vil at de skal vises i de andre malene eller veiledningene.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-147">If you edit a template that contains activities that are used in other templates or guides, you must push the changes if you want them to appear in the other templates or guides.</span></span>

<span data-ttu-id="3e4a5-148">Hvis du ikke er sikker på om malens aktiviteter brukes i andre maler eller veiledninger, velger du **Brukt i**-kategorien for å vise hvor disse aktivitetene vises.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-148">If you're not sure whether your template's activities are used in other templates or guides, select the **Used in** tab to view where those activities appear.</span></span>

   <span data-ttu-id="3e4a5-149">[![Vise hvor aktiviteter for veiledninger og maler brukes](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-149">[![View guides and templates activities are used in](./media/onboard-edit-guide-view-used-in.png)](./media/onboard-edit-guide-view-used-in.png)</span></span>

<span data-ttu-id="3e4a5-150">Slik overfører du endringene:</span><span class="sxs-lookup"><span data-stu-id="3e4a5-150">To push your changes:</span></span>

1. <span data-ttu-id="3e4a5-151">Lagre endringene ved å velge **Lagre**-knappen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-151">Save your changes by selecting the **Save** button.</span></span> <span data-ttu-id="3e4a5-152">Hvis du ikke gjør dette, blir du bedt om å lagre endringene i neste trinn.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-152">If you don't do this, you'll be prompted to save your changes in the next step.</span></span>

2. <span data-ttu-id="3e4a5-153">Velg **Overfør disse endringene**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-153">Select **Push these changes**.</span></span>

   
## <a name="add-or-edit-an-introduction"></a><span data-ttu-id="3e4a5-154">Legge til eller redigere en innledning</span><span class="sxs-lookup"><span data-stu-id="3e4a5-154">Add or edit an introduction</span></span>

1. <span data-ttu-id="3e4a5-155">I kategorien **Innledning** skriver du inn en tittel for veiledningen og en innledningsmelding.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-155">On the **Introduction** tab, enter a title for your guide and an opening message.</span></span> <span data-ttu-id="3e4a5-156">Hvis du vil bruke eksempelteksten, velger du **Bruk denne meldingen**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-156">To use the sample text, select **Use this message**.</span></span>

    <span data-ttu-id="3e4a5-157">[![Innledning-fanen i en Onboard-mal](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-157">[![Introduction tab in an Onboard template](./media/onboard-template-introduction.png)](./media/onboard-template-introduction.png)</span></span>

2. <span data-ttu-id="3e4a5-158">Bruk formateringsknappene til å fremheve tekst etter behov, eller for å legge til bilder eller koblinger.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-158">Use the formatting buttons to call out text as you require, or to add images or links.</span></span>
3. <span data-ttu-id="3e4a5-159">Velg **Lagre** for å lagre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-159">Select **Save** to save your work.</span></span>

## <a name="add-or-edit-activities"></a><span data-ttu-id="3e4a5-160">Legge til eller redigere aktiviteter</span><span class="sxs-lookup"><span data-stu-id="3e4a5-160">Add or edit activities</span></span>

1. <span data-ttu-id="3e4a5-161">Dra elementer fra høyre til redigeringsområdet i kategorien **Aktiviteter**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-161">On the **Activities** tab, drag items from the right to the editing area.</span></span>
2. <span data-ttu-id="3e4a5-162">Hvis du vil organisere veiledningen i inndelinger, drar du **Ny seksjon**-elementet til redigeringsområdet og skriver inn et navn og en valgfri beskrivelse for inndelingen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-162">To organize your guide into sections, drag the **New section** item to the editing area, and enter a name and an optional description for the section.</span></span>

    ![[<span data-ttu-id="3e4a5-163">Legge til en ny inndeling i en veiledning eller mal for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="3e4a5-163">Adding a new section to an onboarding guide or template</span></span>](./media/onboard-edit-add-section.png)](./media/onboard-edit-add-section.png)

3. <span data-ttu-id="3e4a5-164">Hvis du vil legge til aktiviteter som den nyansatte skal fullføre, drar du elementet **Ny aktivitet** til redigeringsområdet og skriver inn et navn og en beskrivelse for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-164">To add activities for your new hire to complete, drag the **New activity** item to the editing area, and enter a name and description for the activity.</span></span>

    ![[<span data-ttu-id="3e4a5-165">Legge til en ny aktivitet i en veiledning eller mal for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="3e4a5-165">Adding a new activity to an onboarding guide or template</span></span>](./media/onboard-edit-add-activity.png)](./media/onboard-edit-add-activity.png)

4. <span data-ttu-id="3e4a5-166">Legge til rikt innhold i veiledningen for jobbintroduksjon:</span><span class="sxs-lookup"><span data-stu-id="3e4a5-166">Add rich content to your onboarding guide:</span></span>

    - <span data-ttu-id="3e4a5-167">Hvis du vil legge til en YouTube-video, drar du **YouTube**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, og skriver inn URL-adressen for YouTube-videoen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-167">To add a YouTube video, drag the **YouTube** item to the editing area, enter a name and description for the activity, and enter the URL for the YouTube video.</span></span>
    - <span data-ttu-id="3e4a5-168">Hvis du vil legge til en Sway-presentasjon eller et nyhetsbrev, drar du **Sway**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten og skriver inn den innebygde URL-adressen for Sway-presentasjonen eller -nyhetsbrevet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-168">To add a Sway presentation or newsletter, drag the **Sway** item to the editing area, enter a name and description for the activity, and enter the embedded URL for the Sway presentation or newsletter.</span></span>
    - <span data-ttu-id="3e4a5-169">Hvis du vil legge til en PowerApps-app, drar du **PowerApps**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten og velger PowerApps-appen eller angir ID-en for PowerApps-appen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-169">To add a PowerApps app, drag the **PowerApps** item to the editing area, enter a name and description for the activity, and either select the PowerApps app or enter the PowerApps app ID.</span></span>
    - <span data-ttu-id="3e4a5-170">Hvis du vil legge til en Microsoft Stream-video, drar du **Microsoft Stream**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, og skriver inn URL-adressen for Microsoft Stream-videoen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-170">To add a Microsoft Stream video, drag the **Microsoft Stream** item to the editing area, enter a name and description for the activity, and enter the URL for the Microsoft Stream video.</span></span>
    - <span data-ttu-id="3e4a5-171">Hvis du vil legge til et Microsoft Forms-skjema, drar du **Microsoft Forms**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, skriver inn URL-adressen for Microsoft Forms-skjemaet og angir størrelsen på skjermområdet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-171">To add a Microsoft Forms form, drag the **Microsoft Forms** item to the editing area, enter a name and description for the activity, enter the URL for the Microsoft Forms form, and specify the size of the screen area.</span></span>
    - <span data-ttu-id="3e4a5-172">Hvis du vil legge til en iframe som inneholder webinnhold, drar du **Webinnhold (iframe)**-elementet til redigeringsområdet, skriver inn et navn og en beskrivelse for aktiviteten, skriver inn URL-adressen for webinnholdet og angir størrelsen på skjermområdet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-172">To add an iframe that contains web content, drag the **Web Content (iframe)** item to the editing area, enter a name and description for the activity, enter the URL for the web content, and specify the size of the screen area.</span></span>

    ![[<span data-ttu-id="3e4a5-173">Legge til rikt innhold i en veiledning eller mal for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="3e4a5-173">Adding rich content to an onboarding guide or template</span></span>](./media/onboard-edit-add-rich-content.png)](./media/onboard-edit-add-rich-content.png)

2. <span data-ttu-id="3e4a5-174">Valgfritt: I området til høyre for hver aktivitet tilordner du aktiviteten til en bestemt person eller rolle, legger til en forfallsdato og kontaktperson og tilordner en kategorifarge.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-174">Optional: In the area on the right of each activity, assign the activity to a specific person or role, add a due date and contact person, and assign a category color.</span></span> <span data-ttu-id="3e4a5-175">Når du tilordner en aktivitet til en person eller rolle, opprettes en oppgave for hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-175">When you assign an activity to a person or role, a task is created for each individual.</span></span> <span data-ttu-id="3e4a5-176">Denne oppgaven vises på **Oppgaver**-menyen i Onboard.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-176">This task appears on the **Tasks** menu in Onboard.</span></span>

    <span data-ttu-id="3e4a5-177">[![Tilordne en aktivitet i en veiledning eller mal for jobbintroduksjon](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span><span class="sxs-lookup"><span data-stu-id="3e4a5-177">[![Assigning an activity in an onboarding guide or template](./media/onboard-assign-activity.png)](./media/onboard-assign-activity.png)</span></span>

3. <span data-ttu-id="3e4a5-178">Velg **Lagre** for å lagre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-178">Select **Save** to save your work.</span></span>

<span data-ttu-id="3e4a5-179">Hvis du vil slette en aktivitet eller en inndeling, velger du **Slett**-knappen (papirkurvsymbolet) øverst i høyre hjørne av aktiviteten eller inndelingen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-179">To delete an activity or section, select the **Delete** button (the trash can symbol) in the upper-right corner of the activity or section.</span></span>

<span data-ttu-id="3e4a5-180">Hvis du vil omorganisere aktiviteter og inndelinger, drar du dem til en ny plassering.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-180">To rearrange activities and sections, drag them to a new location.</span></span>

## <a name="add-or-edit-contacts"></a><span data-ttu-id="3e4a5-181">Legge til eller redigere kontakter</span><span class="sxs-lookup"><span data-stu-id="3e4a5-181">Add or edit contacts</span></span>

<span data-ttu-id="3e4a5-182">Du kan legge til kontaktpersoner som kan hjelpe den nyansatte med å lykkes fra dag én.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-182">You can add contact people who can help your new hire succeed from day one.</span></span> <span data-ttu-id="3e4a5-183">Disse kontaktene kan være rekrutterere, teammedlemmer, jobbintroduksjonskontakter, mentorer, administratorer og IT-støttepersonale.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-183">These contacts can be recruiters, teammates, onboarding buddies, mentors, admins, and IT support staff.</span></span>

1. <span data-ttu-id="3e4a5-184">Velg **Ny kontakt** i fanen **Kontakter**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-184">On the **Contacts** tab, select **New contact**.</span></span>
2. <span data-ttu-id="3e4a5-185">Skriv inn kontaktpersonens navn eller e-postadresse i dialogboksen **Legg til teammedlem,** skriv inn en kort beskrivelse som forklarer hvordan kontaktpersonen kan hjelpe den nyansatte, og velg deretter **Legg til** .</span><span class="sxs-lookup"><span data-stu-id="3e4a5-185">In the **Add team member** dialog box, enter the contact person's name or email address, enter a short description that explains how the contact person can help the new hire, and then select **Add**.</span></span> 

    ![[<span data-ttu-id="3e4a5-186">Legge til kontakter i en veiledning eller mal for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="3e4a5-186">Adding contacts to an onboarding guide or template</span></span>](./media/onboard-edit-add-contact.png)](./media/onboard-edit-add-contact.png)

    <span data-ttu-id="3e4a5-187">Du kan eventuelt velge én eller flere kontakter under **Forslag**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-187">Alternately, you can select one or more contacts under **Suggestions**.</span></span>

3. <span data-ttu-id="3e4a5-188">Velg **Lagre** for å lagre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-188">Select **Save** to save your work.</span></span>

<span data-ttu-id="3e4a5-189">Hvis du vil slette en kontakt, velger du **Slett**-knappen (papirkurvsymbolet) til høyre for kontakten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-189">To delete a contact, select the **Delete** button (the trash can symbol) to the right of the contact.</span></span>

<span data-ttu-id="3e4a5-190">Hvis du vil redigere en kontakt, velger du **Rediger**-knappen (blyantsymbolet) til høyre for kontakten.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-190">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the contact.</span></span>

## <a name="add-or-edit-resources"></a><span data-ttu-id="3e4a5-191">Legge til eller redigere ressurser</span><span class="sxs-lookup"><span data-stu-id="3e4a5-191">Add or edit resources</span></span>

<span data-ttu-id="3e4a5-192">Du kan legge til nyttige filer, kart og koblinger i **Ressurser**-delen i jobbintroduksjonsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-192">You can add useful files, maps, and links to the **Resources** section of your onboarding guide.</span></span>

1. <span data-ttu-id="3e4a5-193">Velg **Ny ressurs** i fanen **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-193">On the **Resources** tab, select **New resource**.</span></span>
2. <span data-ttu-id="3e4a5-194">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="3e4a5-194">Follow one of these steps:</span></span>

    - <span data-ttu-id="3e4a5-195">Hvis du vil legge til en fil, velger du kategorien **Fil** og drar filen til det angitte området.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-195">To add a file, select the **File** tab, and drag the file into the designated area.</span></span> <span data-ttu-id="3e4a5-196">(Du kan også klikke hvor som helst i området for å søke etter filen på datamaskinen, eller velge **Bla gjennom OneDrive**.) Skriv inn et navn på filen, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-196">(Alternatively, click anywhere in that area to browse for the file on your computer, or select **Browse OneDrive**.) Enter a name for the file, and then select **Add**.</span></span>
    - <span data-ttu-id="3e4a5-197">Hvis du vil legge til en kobling , velger du kategorien **Kobling**, skriver inn et navn og en adresse for koblingen og velger deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-197">To add a link, select the **Link** tab, enter a name and address for the link, and then select **Add**.</span></span>
    - <span data-ttu-id="3e4a5-198">Hvis du vil legge til et kart , velger du kategorien **Kart**, skriver inn et navn og en adresse for kartet og velger deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-198">To add a map, select the **Map** tab, enter a name and address for the map, and then select **Add**.</span></span> <span data-ttu-id="3e4a5-199">Onboard vil ta med et kart over adressen du angir.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-199">Onboard will include a map of the address that you specify.</span></span>

    ![[<span data-ttu-id="3e4a5-200">Legge til en ressurs i en veiledning eller mal for jobbintroduksjon</span><span class="sxs-lookup"><span data-stu-id="3e4a5-200">Adding a resource to an onboarding guide or template</span></span>](./media/onboard-edit-add-resource.png)](./media/onboard-edit-add-resource.png)

3. <span data-ttu-id="3e4a5-201">Velg **Lagre** for å lagre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-201">Select **Save** to save your work.</span></span>

<span data-ttu-id="3e4a5-202">Hvis du vil slette en ressurs, velger du **Slett**-knappen (papirkurvsymbolet) til høyre for ressursen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-202">To delete a resource, select the **Delete** button (the trash can symbol) to the right of the resource.</span></span>

<span data-ttu-id="3e4a5-203">Hvis du vil redigere en kontakt, velger du **Rediger**-knappen (blyantsymbolet) til høyre for ressursen.</span><span class="sxs-lookup"><span data-stu-id="3e4a5-203">To edit a contact, select the **Edit** button (the pencil symbol) to the right of the resource.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3e4a5-204">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="3e4a5-204">Next steps</span></span>

- [<span data-ttu-id="3e4a5-205">Dele innhold med andre bidragsytere</span><span class="sxs-lookup"><span data-stu-id="3e4a5-205">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="3e4a5-206">Vise statusen for oppgaver og jobbintroduksjonsmedarbeidere</span><span class="sxs-lookup"><span data-stu-id="3e4a5-206">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="3e4a5-207">Opprette ansettelsesteam i Onboard</span><span class="sxs-lookup"><span data-stu-id="3e4a5-207">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="3e4a5-208">Se også</span><span class="sxs-lookup"><span data-stu-id="3e4a5-208">See also</span></span>

- [<span data-ttu-id="3e4a5-209">Prøve eller kjøpe Onboard-appen</span><span class="sxs-lookup"><span data-stu-id="3e4a5-209">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="3e4a5-210">Hva er nytt</span><span class="sxs-lookup"><span data-stu-id="3e4a5-210">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="3e4a5-211">Produktmerknader</span><span class="sxs-lookup"><span data-stu-id="3e4a5-211">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="3e4a5-212">Få kundestøtte</span><span class="sxs-lookup"><span data-stu-id="3e4a5-212">Get support</span></span>](./talent-support.md)
