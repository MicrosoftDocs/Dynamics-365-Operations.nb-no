---
title: Human Resources-app i Teams
description: Dette emnet gir en innføring i Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828920"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="b0c3d-103">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="b0c3d-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="b0c3d-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="b0c3d-105">Ansatte kan samhandle med en robot for å be om informasjon.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="b0c3d-106">Kategorien **Fritid** gir mer detaljert information. In tillegg kan de sende personer informasjon om kommende fritid i grupper og chatter utenfor Human Resources-appen.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Robot for permisjonsapp i Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-permisjonsforespørselskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="b0c3d-110">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="b0c3d-110">Install and setup</span></span>

<span data-ttu-id="b0c3d-111">Du kan finne Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="b0c3d-112">Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="b0c3d-113">Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="b0c3d-114">Aktiver varslinger for Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="b0c3d-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="b0c3d-115">Hvis du vil at brukere skal motta permisjonsforespørselsvarsler i Teams-appen, må du aktivere varslinger i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="b0c3d-116">Det er bare brukere som er logget på Teams og som bruker Teams-appen i Human Resources, som mottar varslinger.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="b0c3d-117">Velg **Systemadministrasjon**i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b0c3d-118">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-118">Select **Links**.</span></span>

3. <span data-ttu-id="b0c3d-119">Under **Oppsett** velger du **Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="b0c3d-120">I kategorien **Generelt** setter du **Aktiver varslinger for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere varslinger for Teams-appen i Systemparametere](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="b0c3d-122">Hvis du vil aktivere Teams-varslinger for alle brukere, velger du **Ja** i ledeteksten.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-varslinger for alle brukere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="b0c3d-124">Aktivere eller deaktivere Teams-varslinger for individuelle brukere</span><span class="sxs-lookup"><span data-stu-id="b0c3d-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="b0c3d-125">Når du har aktivert varsler for Teams-appen i Human Resources, kan du aktivere eller deaktivere varslinger for individuelle brukere.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="b0c3d-126">Velg **Systemadministrasjon**i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="b0c3d-127">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-127">Select **Links**.</span></span>

3. <span data-ttu-id="b0c3d-128">Under **Brukere** velger du **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="b0c3d-129">Velg kategorien **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="b0c3d-130">Sett **Aktiver varslinger for Teams-app** til **Ja** for å aktivere varslinger for brukeren, eller **Nei** for å deaktivere varslinger for brukeren.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivere varslinger for Teams-appen i kategorien Arbeidsflyt i Brukeralternativer](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="b0c3d-132">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="b0c3d-133">Kjente problemer</span><span class="sxs-lookup"><span data-stu-id="b0c3d-133">Known issues</span></span>

| <span data-ttu-id="b0c3d-134">Problem</span><span class="sxs-lookup"><span data-stu-id="b0c3d-134">Issue</span></span> | <span data-ttu-id="b0c3d-135">Status</span><span class="sxs-lookup"><span data-stu-id="b0c3d-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="b0c3d-136">Horisontal rulling fungerer ikke på Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="b0c3d-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="b0c3d-137">Horisontal rulling er ikke et problem på iOS-enheter eller skrivebordsenheter.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="b0c3d-138">Vi arbeider med en løsning for Android.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="b0c3d-139">Balansen er feil når du sender inn fridager for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="b0c3d-140">Prognoser er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="b0c3d-141">Saldoen vises for den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="b0c3d-142">Kan ikke avbryte en forespørsel med statusen **Til vurdering**.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="b0c3d-143">Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="b0c3d-144">Saldoinformasjon beregnes per i dag.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="b0c3d-145">Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="b0c3d-146">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="b0c3d-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="b0c3d-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="b0c3d-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="b0c3d-148">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="b0c3d-149">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="b0c3d-150">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="b0c3d-151">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="b0c3d-152">Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="b0c3d-153">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="b0c3d-154">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b0c3d-155">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="b0c3d-156">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="b0c3d-157">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="b0c3d-158">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="b0c3d-159">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="b0c3d-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="b0c3d-160">Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="b0c3d-161">Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="b0c3d-162">Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b0c3d-163">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="b0c3d-164">Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="b0c3d-165">Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="b0c3d-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="b0c3d-166">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="b0c3d-167">Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="b0c3d-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="b0c3d-168">Se også</span><span class="sxs-lookup"><span data-stu-id="b0c3d-168">See also</span></span> 

[<span data-ttu-id="b0c3d-169">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0c3d-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="b0c3d-170">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b0c3d-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="b0c3d-171">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="b0c3d-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

