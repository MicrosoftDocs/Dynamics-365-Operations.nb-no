---
title: Behandle permisjonsforespørsler i Teams
description: Dette emnet viser hvordan du ber om fridager Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953418"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a4f02-103">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a4f02-104">Med Dynamics 365 Human Resources-appen i Microsoft Teams kan du raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a4f02-105">Du kan samhandle med en robot for å be om informasjon og starte en permisjonsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="a4f02-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="a4f02-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="a4f02-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="a4f02-107">Du kan også sende personinformasjon om kommende fritid i Teams og samtaler utenfor Human Resources-appen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a4f02-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="a4f02-108">Install the app</span></span>

<span data-ttu-id="a4f02-109">Du finner Dynamics 365 Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="a4f02-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a4f02-110">I Microsoft Teams klikker du på ellipsene.</span><span class="sxs-lookup"><span data-stu-id="a4f02-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a4f02-112">Søk etter Dynamics 365 Human Resources, og velg deretter flisen **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-flis for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a4f02-114">Velg **Legg til** for å installere appen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-114">Select the **Add** button to install the app.</span></span>

   ![Installasjon av permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a4f02-116">Hvis appen ikke logger deg på automatisk, velger du kategorien **Innstillinger** for å logge på.</span><span class="sxs-lookup"><span data-stu-id="a4f02-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Kategorien Innstillinger i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a4f02-118">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a4f02-119">Hvis du har tilgang til mer enn én forekomst av Human Resources, kan du velge hvilket miljø du vil koble til, i kategorien **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="a4f02-120">Appen støtter nå sikkerhetsrollen systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="a4f02-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a4f02-121">Bruke roboten</span><span class="sxs-lookup"><span data-stu-id="a4f02-121">Use the bot</span></span>

<span data-ttu-id="a4f02-122">Når appen er installert, vises det en velkomstmelding med informasjon om hvilke handlingstyper roboten kan utføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="a4f02-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Velkomstmelding for robot i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a4f02-124">Når du først samhandler med roboten, må du kanskje logge på.</span><span class="sxs-lookup"><span data-stu-id="a4f02-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a4f02-125">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a4f02-126">Du kan be roboten om å:</span><span class="sxs-lookup"><span data-stu-id="a4f02-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a4f02-127">Starte en permisjonsforespørsel for deg.</span><span class="sxs-lookup"><span data-stu-id="a4f02-127">Start a leave request for you.</span></span>

  ![Starte en permisjonsforespørsel i Teams-samtaler](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="a4f02-129">Samtalen fylles ut en permisjonsforespørsel for deg.</span><span class="sxs-lookup"><span data-stu-id="a4f02-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="a4f02-130">Velg **Be om fravær** og rediger detaljene for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Redigere detaljer for permisjonsforespørsel](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="a4f02-132">Når du er ferdig med å redigere detaljene for permisjonsforespørselen, velger du **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a4f02-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Sende permisjonsforespørsel](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a4f02-134">Behandle permisjonen i Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-134">Manage your leave in Teams</span></span>

<span data-ttu-id="a4f02-135">I kategorien **Fridager** kan du vise:</span><span class="sxs-lookup"><span data-stu-id="a4f02-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="a4f02-136">Saldoinformasjon om fridager for hver permisjonstype du er registrert i</span><span class="sxs-lookup"><span data-stu-id="a4f02-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a4f02-137">Forespørsler om kommende permisjoner</span><span class="sxs-lookup"><span data-stu-id="a4f02-137">Upcoming leave requests</span></span>

- <span data-ttu-id="a4f02-138">Forespørsler om fridager</span><span class="sxs-lookup"><span data-stu-id="a4f02-138">Time-off requests</span></span>

- <span data-ttu-id="a4f02-139">Utkast til permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="a4f02-139">Draft leave requests</span></span>

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a4f02-141">Opprette en ny forespørsel</span><span class="sxs-lookup"><span data-stu-id="a4f02-141">Create a new request</span></span>

1. <span data-ttu-id="a4f02-142">Hvis du vil opprette en ny permisjonsforespørsel, velger du **Ny forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-142">To create a new leave request, select **New request**.</span></span>

   ![Ny forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a4f02-144">Angi dagen eller dagene du vil ha fri, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tillegg av fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a4f02-146">Angi en årsakskode hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="a4f02-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="a4f02-147">Skriv også inn kommentarer og legg til eventuelle vedlegg.</span><span class="sxs-lookup"><span data-stu-id="a4f02-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a4f02-148">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a4f02-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a4f02-149">Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="a4f02-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a4f02-150">Behandle utkast til forespørsler</span><span class="sxs-lookup"><span data-stu-id="a4f02-150">Manage draft requests</span></span>

1. <span data-ttu-id="a4f02-151">Velg kategorien **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-151">Select the **Drafts** tab.</span></span>

   ![Kategorien Utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a4f02-153">Velg blyanten for å redigere forespørselen, eller velg papirkurven for å slette forespørselen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a4f02-154">Gjør nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-154">Make any necessary changes.</span></span> <span data-ttu-id="a4f02-155">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a4f02-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a4f02-156">Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="a4f02-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering av utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="a4f02-158">Svare på Teams-varslinger</span><span class="sxs-lookup"><span data-stu-id="a4f02-158">Respond to Teams notifications</span></span>

<span data-ttu-id="a4f02-159">Når du eller en arbeider du er godkjenner for, sender en permisjonsforespørsel, vil du motta en melding i Human Resources-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="a4f02-160">Du kan merke varslingen for å vise den.</span><span class="sxs-lookup"><span data-stu-id="a4f02-160">You can select the notification to view it.</span></span> <span data-ttu-id="a4f02-161">Varslinger vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="a4f02-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="a4f02-162">Hvis du er godkjenner, kan du velge **Godkjenn** eller **Avvis** i varslingen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="a4f02-163">Du kan også angi en valgfri melding.</span><span class="sxs-lookup"><span data-stu-id="a4f02-163">You can also provide an optional message.</span></span>

![Varsling om permisjonsforespørsel i Human Resources-appen i Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="a4f02-165">Sende kommende informasjon om fritid til kollegene</span><span class="sxs-lookup"><span data-stu-id="a4f02-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="a4f02-166">Når du har installert Human Resources-appen for Teams, kan du enkelt sende informasjon om kommende fritid til kollegene i grupper eller samtaler.</span><span class="sxs-lookup"><span data-stu-id="a4f02-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="a4f02-167">Velg Human Resources-knappen under chattevinduet i et team eller en chat i Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources-knapp under chattevinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="a4f02-169">Velg permisjonsforespørselen du vil dele.</span><span class="sxs-lookup"><span data-stu-id="a4f02-169">Select the leave request you want to share.</span></span> <span data-ttu-id="a4f02-170">Hvis du vil dele et utkast av en permisjonsforespørsel, velger du **Utkast** først.</span><span class="sxs-lookup"><span data-stu-id="a4f02-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Velge en forestående permisjonsforespørsel som skal deles](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="a4f02-172">Permisjonsforespørselen vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="a4f02-172">Your leave request will display in the chat.</span></span>

![Human Resources-permisjonsforespørselskort](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="a4f02-174">Hvis du delte en utkastforespørsel, vil den vises som et utkast:</span><span class="sxs-lookup"><span data-stu-id="a4f02-174">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources-utkast til permisjonsforespørselskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="a4f02-176">Vise teamets persmisjonskalender</span><span class="sxs-lookup"><span data-stu-id="a4f02-176">View your team's leave calendar</span></span>

<span data-ttu-id="a4f02-177">Hvis du er leder med direkterapporter, kan du vise gruppens godkjente og uavsluttede fritid.</span><span class="sxs-lookup"><span data-stu-id="a4f02-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="a4f02-178">I Human Resources-appen i Teams velger du **Fritid**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="a4f02-179">Velg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-179">Select **Team calendar**.</span></span> <span data-ttu-id="a4f02-180">Kalenderen viser de godkjente og uavsluttede fritidene for direkterapporter.</span><span class="sxs-lookup"><span data-stu-id="a4f02-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Vise kalender i Human Resources-app i Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="a4f02-182">Hvis du ikke kan se gruppekalenderen, ber du administratoren om å aktivere den.</span><span class="sxs-lookup"><span data-stu-id="a4f02-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="a4f02-183">Hvis du vil ha mer informasjon, kan du se [Installere og konfigurere](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="a4f02-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="a4f02-184">Språk som støttes</span><span class="sxs-lookup"><span data-stu-id="a4f02-184">Supported languages</span></span>

<span data-ttu-id="a4f02-185">Appen Dynamics 365 Human Resources i Teams støtter følgende språk:</span><span class="sxs-lookup"><span data-stu-id="a4f02-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="a4f02-186">ID for nasjonal innstilling</span><span class="sxs-lookup"><span data-stu-id="a4f02-186">Locale ID</span></span> | <span data-ttu-id="a4f02-187">Språk</span><span class="sxs-lookup"><span data-stu-id="a4f02-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="a4f02-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="a4f02-188">de-DE</span></span> | <span data-ttu-id="a4f02-189">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="a4f02-189">German (Germany)</span></span> |
| <span data-ttu-id="a4f02-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="a4f02-190">es-ES</span></span> | <span data-ttu-id="a4f02-191">Spansk (Spania)</span><span class="sxs-lookup"><span data-stu-id="a4f02-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="a4f02-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="a4f02-192">es-MX</span></span> | <span data-ttu-id="a4f02-193">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="a4f02-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="a4f02-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="a4f02-194">fr-CA</span></span> | <span data-ttu-id="a4f02-195">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="a4f02-195">French (Canada)</span></span> |
| <span data-ttu-id="a4f02-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="a4f02-196">fr-FR</span></span> | <span data-ttu-id="a4f02-197">Fransk (Frankrike)</span><span class="sxs-lookup"><span data-stu-id="a4f02-197">French (France)</span></span> |
| <span data-ttu-id="a4f02-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="a4f02-198">it-IT</span></span> | <span data-ttu-id="a4f02-199">Italiensk (Italia)</span><span class="sxs-lookup"><span data-stu-id="a4f02-199">Italian (Italy)</span></span> |
| <span data-ttu-id="a4f02-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="a4f02-200">nl-NL</span></span> | <span data-ttu-id="a4f02-201">Nederlandsk (Nederland)</span><span class="sxs-lookup"><span data-stu-id="a4f02-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="a4f02-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="a4f02-202">pt-BR</span></span> | <span data-ttu-id="a4f02-203">Portugisisk (Brasil)</span><span class="sxs-lookup"><span data-stu-id="a4f02-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="a4f02-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="a4f02-204">tr-TR</span></span> | <span data-ttu-id="a4f02-205">Tyrkisk (Tyrkia)</span><span class="sxs-lookup"><span data-stu-id="a4f02-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="a4f02-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="a4f02-206">zh-CN</span></span> | <span data-ttu-id="a4f02-207">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="a4f02-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="a4f02-208">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="a4f02-208">Troubleshooting</span></span>

<span data-ttu-id="a4f02-209">Hvis du har problemer med å logge på eller bruke Dynamics 365 Human Resources Teams-appen, kan du prøve å følge disse instruksjonene for feilsøking.</span><span class="sxs-lookup"><span data-stu-id="a4f02-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="a4f02-210">Hvis du fortsatt har problemer etter feilsøking, kontakter du kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="a4f02-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="a4f02-211">For mer informasjon, se [Få kundestøtte](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="a4f02-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="a4f02-212">Kan ikke logge på Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="a4f02-213">Hvis du ikke kan logge på appen, kan det hende at kontoen du bruker til å logge på Microsoft Teams, ikke er tilknyttet en ansattpost i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a4f02-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a4f02-214">Kontakt systemadministrator for å kontrollere at ansattposten er riktig tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="a4f02-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="a4f02-215">Oversettelser vises ikke riktig</span><span class="sxs-lookup"><span data-stu-id="a4f02-215">Translations don't display correctly</span></span>

<span data-ttu-id="a4f02-216">Hvis oversettelsene ikke vises som forventet, må du kontrollere at språket du velger i Teams, samsvarer med språket som er valgt i **Brukeralternativer** for Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a4f02-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="a4f02-217">I Teams kan du se på **Appspråk** i **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a4f02-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-innstillinger](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="a4f02-219">Velg **Innstillinger** og deretter **Brukeralternativer** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a4f02-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="a4f02-220">Kontroller at feltet **Språk** samsvarer med feltet **Appspråk** i Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Brukeralternativer for Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="a4f02-222">Gi oss beskjed hvis du fremdeles opplever oversettelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="a4f02-223">Hvis du vil ha informasjon, kan du se [Få støtte for Finance and Operations-apper eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="a4f02-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="a4f02-224">Feil under godkjenning av permisjonsforespørsler i Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="a4f02-225">Hvis du får en feilmelding under forsøk på å godkjenne permisjonsforespørsler i Teams-appen, kan du prøve følgende feilsøkingstrinn:</span><span class="sxs-lookup"><span data-stu-id="a4f02-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="a4f02-226">Kontroller at kontoen du bruker til å logge på Microsoft Teams, er den samme som du bruker til å få tilgang til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a4f02-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="a4f02-227">Kontroller at du er en gyldig godkjenner for forespørselen ved å kontrollere arbeidsflytinnstillingene for permisjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="a4f02-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="a4f02-228">Hvis du vil ha mer informasjon om arbeidsflyter for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="a4f02-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="a4f02-229">Permisjonsgodkjennere mottar ikke Teams-chatmeldinger for å godkjenne permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="a4f02-229">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="a4f02-230">Sikre at varslinger er aktivert for miljøet og brukeren.</span><span class="sxs-lookup"><span data-stu-id="a4f02-230">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="a4f02-231">Hvis du vil ha mer informasjon, kan du se [Aktiver varslinger for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Aktivere eller deaktivere Teams-varslinger for individuelle brukere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="a4f02-231">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="a4f02-232">Kontroller at brukere blir logget på **Chatter**-kategorien med samme legitimasjon som de bruker for godkjenning av permisjonsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="a4f02-232">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="a4f02-233">Bruk meldingene "logg av" og deretter "logg på" for å logge deg på med riktig legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="a4f02-233">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="a4f02-234">Hvis problemet vedvarer, må du kontrollere statusen til den satsvise jobben for forretningshendelser som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="a4f02-234">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="a4f02-235">Hvis den er i et ventende stadium eller utførelsesstadium, må du sjekke tilbake om et par minutter.</span><span class="sxs-lookup"><span data-stu-id="a4f02-235">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="a4f02-236">Hvis statusen forblir uendret, kan du logge en støtteforespørsel, slik at teamet kan bidra til å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="a4f02-236">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="a4f02-237">Kjente tilgjengelighetsproblemer</span><span class="sxs-lookup"><span data-stu-id="a4f02-237">Known accessibility issues</span></span>

<span data-ttu-id="a4f02-238">Human Resources-appen i Teams har følgende tilgjengelighetsproblemer som vi jobber med å rette opp i fremtidige versjoner.</span><span class="sxs-lookup"><span data-stu-id="a4f02-238">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="a4f02-239">Problem</span><span class="sxs-lookup"><span data-stu-id="a4f02-239">Issue</span></span> | <span data-ttu-id="a4f02-240">Midlertidig løsning eller forklaring</span><span class="sxs-lookup"><span data-stu-id="a4f02-240">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="a4f02-241">Hvis du zoomer til 400 % på skrivebordet, skjules noen av handlingsknappene fra visningen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-241">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="a4f02-242">Det anbefales bruk av et forstørrelsesprogram i stedet til vi kan støtte dette zoomenivået.</span><span class="sxs-lookup"><span data-stu-id="a4f02-242">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="a4f02-243">I fanen **Fridager** annonserer VoiceOver en knappehandling ved å lese toppteksen for fridagerrutenettet.</span><span class="sxs-lookup"><span data-stu-id="a4f02-243">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="a4f02-244">Toppteksten og elementene i rutenettet er gruppert etter år, og de kan skjules.</span><span class="sxs-lookup"><span data-stu-id="a4f02-244">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="a4f02-245">VoiceOver tolker dette som et handlingselement, men det er ikke det.</span><span class="sxs-lookup"><span data-stu-id="a4f02-245">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="a4f02-246">I fanen **Fridager** er det en ekstra sveipebevegelse når du navigerer til **Årsakskode** i en ny forespørsel.</span><span class="sxs-lookup"><span data-stu-id="a4f02-246">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="a4f02-247">Det finnes ingen skjult kontroll som sveipenavigeringen prøver å komme til.</span><span class="sxs-lookup"><span data-stu-id="a4f02-247">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="a4f02-248">På fanen **Fridager** hvis du sveiper mens kalenderen er åpen, kan du havne utenfor kontrollen i stedet for øverst i en ny forespørsel eller mens du redigerer en forespørsel.</span><span class="sxs-lookup"><span data-stu-id="a4f02-248">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="a4f02-249">Når du kommer **Gå til i dag**, bør du anse det som slutten på kontrollen, og sveipe i motsatt retning for å komme tilbake toppen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-249">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="a4f02-250">I fanen **Chat** hopper fokuset tilbake til toppen når du angir en dato ved bruk av hjelpeverktøyet eller tastaturnavigasjonen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-250">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="a4f02-251">Bruk tabulator til du kommer til inndataområdet igjen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-251">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="a4f02-252">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="a4f02-252">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a4f02-253">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a4f02-253">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a4f02-254">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="a4f02-254">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a4f02-255">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a4f02-255">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a4f02-256">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a4f02-256">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a4f02-257">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="a4f02-257">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a4f02-258">Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="a4f02-258">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a4f02-259">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="a4f02-259">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a4f02-260">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a4f02-260">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a4f02-261">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="a4f02-261">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a4f02-262">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a4f02-262">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a4f02-263">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a4f02-263">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a4f02-264">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a4f02-264">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="a4f02-265">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a4f02-265">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="a4f02-266">Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.</span><span class="sxs-lookup"><span data-stu-id="a4f02-266">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="a4f02-267">Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-267">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a4f02-268">Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-268">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a4f02-269">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="a4f02-269">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="a4f02-270">Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a4f02-270">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="a4f02-271">Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="a4f02-271">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="a4f02-272">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="a4f02-272">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="a4f02-273">Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a4f02-273">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="a4f02-274">Se også</span><span class="sxs-lookup"><span data-stu-id="a4f02-274">See also</span></span>

[<span data-ttu-id="a4f02-275">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-275">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a4f02-276">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-276">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a4f02-277">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="a4f02-277">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]