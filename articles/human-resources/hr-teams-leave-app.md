---
title: Behandle permisjonsforespørsler i Teams
description: Dette emnet viser hvordan du ber om fridager Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828950"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="90288-103">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="90288-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="90288-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="90288-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="90288-105">Du kan samhandle med en robot for å be om informasjon og starte en permisjonsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="90288-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="90288-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="90288-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="90288-107">I tillegg kan du sende personinformasjon om kommende fritid i grupper og samtaler utenfor Human Resources-appen.</span><span class="sxs-lookup"><span data-stu-id="90288-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="90288-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="90288-108">Install the app</span></span>

<span data-ttu-id="90288-109">Du kan finne Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="90288-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="90288-110">I Microsoft Teams klikker du på ellipsene.</span><span class="sxs-lookup"><span data-stu-id="90288-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="90288-112">Søk etter Dynamics 365 Human Resources, og velg deretter flisen **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="90288-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-flis for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="90288-114">Velg **Legg til** for å installere appen.</span><span class="sxs-lookup"><span data-stu-id="90288-114">Select the **Add** button to install the app.</span></span>

   ![Installasjon av permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="90288-116">Hvis appen ikke logger deg på automatisk, velger du kategorien **Innstillinger** for å logge på.</span><span class="sxs-lookup"><span data-stu-id="90288-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Kategorien Innstillinger i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="90288-118">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="90288-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="90288-119">Hvis du har tilgang til mer enn én forekomst av Human Resources, kan du velge hvilket miljø du vil koble til, i kategorien **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="90288-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="90288-120">Appen støtter nå sikkerhetsrollen systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="90288-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="90288-121">Bruke roboten</span><span class="sxs-lookup"><span data-stu-id="90288-121">Use the bot</span></span>

<span data-ttu-id="90288-122">Når appen er installert, vises det en velkomstmelding med informasjon om hvilke handlingstyper roboten kan utføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="90288-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Velkomstmelding for robot i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="90288-124">Når du først samhandler med roboten, må du kanskje logge på.</span><span class="sxs-lookup"><span data-stu-id="90288-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="90288-125">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="90288-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="90288-126">Du kan be roboten om å:</span><span class="sxs-lookup"><span data-stu-id="90288-126">You can ask the bot to:</span></span>

- <span data-ttu-id="90288-127">Vise saldoinformasjon om fridager for hver permisjonstype du er registrert i.</span><span class="sxs-lookup"><span data-stu-id="90288-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Vise saldoer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="90288-129">Vise flere detaljer om en bestemt permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="90288-129">Show additional details about a specific leave type.</span></span>

   ![Vise detaljer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="90288-131">Starte en permisjonsforespørsel for deg.</span><span class="sxs-lookup"><span data-stu-id="90288-131">Start a leave request for you.</span></span>

   ![Be om permisjon i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="90288-133">Når du har startet en permisjonsforespørsel, kan du justere dagene mot høyre i kortet.</span><span class="sxs-lookup"><span data-stu-id="90288-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Redigering av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="90288-135">Når du er ferdig med å angi informasjon, velger du **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="90288-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="90288-136">Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="90288-136">You can also select **Save as draft** to come back to it later.</span></span>

![Innsending av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="90288-138">Behandle permisjonen i Teams</span><span class="sxs-lookup"><span data-stu-id="90288-138">Manage your leave in Teams</span></span>

<span data-ttu-id="90288-139">I kategorien **Fridager** kan du vise:</span><span class="sxs-lookup"><span data-stu-id="90288-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="90288-140">Saldoinformasjon om fridager for hver permisjonstype du er registrert i</span><span class="sxs-lookup"><span data-stu-id="90288-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="90288-141">Forespørsler om kommende permisjoner</span><span class="sxs-lookup"><span data-stu-id="90288-141">Upcoming leave requests</span></span>

- <span data-ttu-id="90288-142">Forespørsler om fridager</span><span class="sxs-lookup"><span data-stu-id="90288-142">Time-off requests</span></span>

- <span data-ttu-id="90288-143">Utkast til permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="90288-143">Draft leave requests</span></span>

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="90288-145">Opprette en ny forespørsel</span><span class="sxs-lookup"><span data-stu-id="90288-145">Create a new request</span></span>

1. <span data-ttu-id="90288-146">Hvis du vil opprette en ny permisjonsforespørsel, velger du **Ny forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="90288-146">To create a new leave request, select **New request**.</span></span>

   ![Ny forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="90288-148">Angi dagen eller dagene du vil ha fri, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="90288-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tillegg av fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="90288-150">Angi en årsakskode hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="90288-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="90288-151">Skriv også inn kommentarer og legg til eventuelle vedlegg.</span><span class="sxs-lookup"><span data-stu-id="90288-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="90288-152">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="90288-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="90288-153">Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="90288-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="90288-154">Behandle utkast til forespørsler</span><span class="sxs-lookup"><span data-stu-id="90288-154">Manage draft requests</span></span>

1. <span data-ttu-id="90288-155">Velg kategorien **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="90288-155">Select the **Drafts** tab.</span></span>

   ![Kategorien Utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="90288-157">Velg blyanten for å redigere forespørselen, eller velg papirkurven for å slette forespørselen.</span><span class="sxs-lookup"><span data-stu-id="90288-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="90288-158">Gjør nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="90288-158">Make any necessary changes.</span></span> <span data-ttu-id="90288-159">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="90288-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="90288-160">Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="90288-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering av utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="90288-162">Svare på Teams-varslinger</span><span class="sxs-lookup"><span data-stu-id="90288-162">Respond to Teams notifications</span></span>

<span data-ttu-id="90288-163">Når du eller en arbeider du er godkjenner for, sender en permisjonsforespørsel, vil du motta en melding i Human Resources-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="90288-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="90288-164">Du kan merke varslingen for å vise den.</span><span class="sxs-lookup"><span data-stu-id="90288-164">You can select the notification to view it.</span></span> <span data-ttu-id="90288-165">Varslinger vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="90288-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="90288-166">Hvis du er godkjenner, kan du velge **Godkjenn** eller **Avvis** i varslingen.</span><span class="sxs-lookup"><span data-stu-id="90288-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="90288-167">Du kan også angi en valgfri melding.</span><span class="sxs-lookup"><span data-stu-id="90288-167">You can also provide an optional message.</span></span>

![Varsling om permisjonsforespørsel i Human Resources-appen i Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="90288-169">Sende kommende informasjon om fritid til kollegene</span><span class="sxs-lookup"><span data-stu-id="90288-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="90288-170">Når du har installert Human Resources-appen for Teams, kan du enkelt sende informasjon om kommende fritid til kollegene i grupper eller samtaler.</span><span class="sxs-lookup"><span data-stu-id="90288-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="90288-171">Velg Human Resources-knappen under chattevinduet i et team eller en chat i Teams.</span><span class="sxs-lookup"><span data-stu-id="90288-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources-knapp under chattevinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="90288-173">Velg permisjonsforespørselen du vil dele.</span><span class="sxs-lookup"><span data-stu-id="90288-173">Select the leave request you want to share.</span></span> <span data-ttu-id="90288-174">Hvis du vil dele et utkast av en permisjonsforespørsel, velger du **Utkast** først.</span><span class="sxs-lookup"><span data-stu-id="90288-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Velge en forestående permisjonsforespørsel som skal deles](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="90288-176">Permisjonsforespørselen vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="90288-176">Your leave request will display in the chat.</span></span>

![Human Resources-permisjonsforespørselskort](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="90288-178">Hvis du delte en utkastforespørsel, vil den vises som et utkast:</span><span class="sxs-lookup"><span data-stu-id="90288-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resources-utkast til permisjonsforespørselskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="90288-180">Vise teamets persmisjonskalender</span><span class="sxs-lookup"><span data-stu-id="90288-180">View your team's leave calendar</span></span>

<span data-ttu-id="90288-181">Hvis du er leder med direkterapporter, kan du vise gruppens godkjente og uavsluttede fritid.</span><span class="sxs-lookup"><span data-stu-id="90288-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="90288-182">I Human Resources-appen i Teams velger du **Fritid**.</span><span class="sxs-lookup"><span data-stu-id="90288-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="90288-183">Velg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="90288-183">Select **Team calendar**.</span></span>

   ![Vise kalender i Human Resources-app i Teams](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="90288-185">Kalenderen viser de godkjente og uavsluttede fritidene for direkterapporter.</span><span class="sxs-lookup"><span data-stu-id="90288-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Fritidskalender i Human Resources-app i Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="90288-187">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="90288-187">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="90288-188">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="90288-188">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="90288-189">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="90288-189">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="90288-190">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="90288-190">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="90288-191">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="90288-191">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="90288-192">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="90288-192">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="90288-193">Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="90288-193">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="90288-194">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="90288-194">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="90288-195">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="90288-195">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="90288-196">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="90288-196">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="90288-197">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="90288-197">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="90288-198">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="90288-198">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="90288-199">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="90288-199">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="90288-200">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="90288-200">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="90288-201">Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.</span><span class="sxs-lookup"><span data-stu-id="90288-201">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="90288-202">Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="90288-202">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="90288-203">Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer.</span><span class="sxs-lookup"><span data-stu-id="90288-203">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="90288-204">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="90288-204">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="90288-205">Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="90288-205">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="90288-206">Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="90288-206">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="90288-207">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="90288-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="90288-208">Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="90288-208">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="90288-209">Se også</span><span class="sxs-lookup"><span data-stu-id="90288-209">See also</span></span>

[<span data-ttu-id="90288-210">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="90288-210">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="90288-211">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="90288-211">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="90288-212">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="90288-212">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
