---
title: Behandle permisjonsforespørsler i Teams
description: Dette emnet viser hvordan du ber om fridager Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393014"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="d2490-103">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="d2490-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d2490-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d2490-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="d2490-105">Du kan samhandle med en robot for å be om informasjon.</span><span class="sxs-lookup"><span data-stu-id="d2490-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="d2490-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="d2490-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="d2490-107">Installere appen</span><span class="sxs-lookup"><span data-stu-id="d2490-107">Install the app</span></span>

<span data-ttu-id="d2490-108">Du kan finne Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="d2490-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="d2490-109">I Microsoft Teams klikker du på ellipsene.</span><span class="sxs-lookup"><span data-stu-id="d2490-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="d2490-111">Søk etter Dynamics 365 Human Resources, og velg deretter flisen **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="d2490-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-flis for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="d2490-113">Velg **Legg til** for å installere appen.</span><span class="sxs-lookup"><span data-stu-id="d2490-113">Select the **Add** button to install the app.</span></span>

   ![Installasjon av permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="d2490-115">Hvis appen ikke logger deg på automatisk, velger du kategorien **Innstillinger** for å logge på.</span><span class="sxs-lookup"><span data-stu-id="d2490-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Kategorien Innstillinger i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="d2490-117">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="d2490-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="d2490-118">Hvis du har tilgang til mer enn én forekomst av Human Resources, kan du velge hvilket miljø du vil koble til, i kategorien **Innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="d2490-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="d2490-119">Appen støtter for øyeblikket ikke sikkerhetsrollen Systeadministrator, og vil vise en feilmelding hvis du logger på med en systemadministratorkonto.</span><span class="sxs-lookup"><span data-stu-id="d2490-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="d2490-120">Hvis du vil logge på med en annen konto, velger du **Bytt kontoer** i kategorien **Innstillinger**, og deretter logger du på med en brukerkonto som ikke har rettigheter som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="d2490-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="d2490-121">Bruke roboten</span><span class="sxs-lookup"><span data-stu-id="d2490-121">Use the bot</span></span>

<span data-ttu-id="d2490-122">Når appen er installert, vises det en velkomstmelding med informasjon om hvilke handlingstyper roboten kan utføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="d2490-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Velkomstmelding for robot i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="d2490-124">Når du først samhandler med roboten, må du kanskje logge på.</span><span class="sxs-lookup"><span data-stu-id="d2490-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="d2490-125">Hvis du ikke ser en påloggingsdialogboks, må du kontrollere innstillingene for nettleseren for å tillate popup-vinduer.</span><span class="sxs-lookup"><span data-stu-id="d2490-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="d2490-126">Du kan be roboten om å:</span><span class="sxs-lookup"><span data-stu-id="d2490-126">You can ask the bot to:</span></span>

- <span data-ttu-id="d2490-127">Vise saldoinformasjon om fridager for hver permisjonstype du er registrert i.</span><span class="sxs-lookup"><span data-stu-id="d2490-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Vise saldoer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="d2490-129">Vise flere detaljer om en bestemt permisjonstype.</span><span class="sxs-lookup"><span data-stu-id="d2490-129">Show additional details about a specific leave type.</span></span>

   ![Vise detaljer i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="d2490-131">Starte en permisjonsforespørsel for deg.</span><span class="sxs-lookup"><span data-stu-id="d2490-131">Start a leave request for you.</span></span>

   ![Be om permisjon i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="d2490-133">Etter at du har startet en permisjonsforespørsel, kan du justere dagene på kortet, eller du kan velge **Rediger detaljer** for å legge til mer informasjon i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="d2490-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Redigering av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="d2490-135">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d2490-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d2490-136">Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="d2490-136">You can also type **Save as draft** to come back to it later.</span></span>

![Innsending av forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="d2490-138">Behandle permisjonen i Teams</span><span class="sxs-lookup"><span data-stu-id="d2490-138">Manage your leave in Teams</span></span>

<span data-ttu-id="d2490-139">I kategorien **Fridager** kan du vise:</span><span class="sxs-lookup"><span data-stu-id="d2490-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="d2490-140">Saldoinformasjon om fridager for hver permisjonstype du er registrert i</span><span class="sxs-lookup"><span data-stu-id="d2490-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="d2490-141">Forespørsler om kommende permisjoner</span><span class="sxs-lookup"><span data-stu-id="d2490-141">Upcoming leave requests</span></span>

- <span data-ttu-id="d2490-142">Forespørsler om fridager</span><span class="sxs-lookup"><span data-stu-id="d2490-142">Time-off requests</span></span>

- <span data-ttu-id="d2490-143">Utkast til permisjonsforespørsler</span><span class="sxs-lookup"><span data-stu-id="d2490-143">Draft leave requests</span></span>

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="d2490-145">Opprette en ny forespørsel</span><span class="sxs-lookup"><span data-stu-id="d2490-145">Create a new request</span></span>

1. <span data-ttu-id="d2490-146">Hvis du vil opprette en ny permisjonsforespørsel, velger du **Ny forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="d2490-146">To create a new leave request, select **New request**.</span></span>

   ![Ny forespørsel i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="d2490-148">Angi dagen eller dagene du vil ha fri, og velg deretter **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d2490-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tillegg av fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="d2490-150">Angi en årsakskode hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="d2490-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="d2490-151">Skriv også inn kommentarer og legg til eventuelle vedlegg.</span><span class="sxs-lookup"><span data-stu-id="d2490-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="d2490-152">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d2490-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d2490-153">Du kan også skrive inn **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="d2490-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="d2490-154">Behandle utkast til forespørsler</span><span class="sxs-lookup"><span data-stu-id="d2490-154">Manage draft requests</span></span>

1. <span data-ttu-id="d2490-155">Velg kategorien **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="d2490-155">Select the **Drafts** tab.</span></span>

   ![Kategorien Utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="d2490-157">Velg blyanten for å redigere forespørselen, eller velg papirkurven for å slette forespørselen.</span><span class="sxs-lookup"><span data-stu-id="d2490-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="d2490-158">Gjør nødvendige endringer.</span><span class="sxs-lookup"><span data-stu-id="d2490-158">Make any necessary changes.</span></span> <span data-ttu-id="d2490-159">Når du er ferdig med å angi informasjon, skriver du inn **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="d2490-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="d2490-160">Du kan også velge **Lagre som utkast** for å komme tilbake til den senere.</span><span class="sxs-lookup"><span data-stu-id="d2490-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering av utkast i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="d2490-162">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="d2490-162">Privacy notice</span></span>

<span data-ttu-id="d2490-163">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="d2490-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="d2490-164">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="d2490-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="d2490-165">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="d2490-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="d2490-166">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="d2490-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="d2490-167">Denne informasjonen sendes deretter videre til Microsofts [Azure-robotrammeverk](https://azure.microsoft.com/services/bot-service/) som kommuniserer med data fra Dynamics 365 Human Resources, og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="d2490-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="d2490-168">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="d2490-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="d2490-169">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d2490-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2490-170">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="d2490-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="d2490-171">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="d2490-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="d2490-172">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="d2490-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="d2490-173">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="d2490-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="d2490-174">Se også</span><span class="sxs-lookup"><span data-stu-id="d2490-174">See also</span></span>

[<span data-ttu-id="d2490-175">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d2490-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="d2490-176">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d2490-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="d2490-177">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="d2490-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
