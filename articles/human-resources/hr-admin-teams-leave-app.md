---
title: Human Resources-app i Teams
description: Dette emnet gir en innføring i Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889746"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="59bf1-103">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="59bf1-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="59bf1-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="59bf1-105">Ansatte kan samhandle med en robot for å be om informasjon.</span><span class="sxs-lookup"><span data-stu-id="59bf1-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="59bf1-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="59bf1-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="59bf1-107">I tillegg kan de sende personinformasjon om kommende fritid i grupper og samtaler utenfor Human Resources-appen.</span><span class="sxs-lookup"><span data-stu-id="59bf1-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Robot for permisjonsapp i Human Resources Teams](./media/hr-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-permisjonsforespørselskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="59bf1-111">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="59bf1-111">Install and setup</span></span>

<span data-ttu-id="59bf1-112">Du finner Dynamics 365 Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="59bf1-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="59bf1-113">Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="59bf1-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="59bf1-114">Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="59bf1-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="59bf1-115">Hvis du vil at brukerne skal vise permisjons- og fraværskalenderen i appen, må du aktivere **Permisjons- og fraværskalender i Teams** i Funksjonsstyring.</span><span class="sxs-lookup"><span data-stu-id="59bf1-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="59bf1-116">Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="59bf1-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="59bf1-117">Aktiver varslinger for Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="59bf1-118">Hvis du vil at brukere skal motta permisjonsforespørselsvarsler i Teams-appen, må du aktivere varslinger i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="59bf1-119">Det er bare brukere som er logget på Teams og som bruker Teams-appen i Dynamics 365 Human Resources, som mottar varslinger.</span><span class="sxs-lookup"><span data-stu-id="59bf1-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="59bf1-120">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="59bf1-121">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-121">Select **Links**.</span></span>

3. <span data-ttu-id="59bf1-122">Under **Oppsett** velger du **Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="59bf1-123">I kategorien **Generelt** setter du **Aktiver varslinger for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere varslinger for Teams-appen i Systemparametere](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="59bf1-125">Hvis du vil aktivere Teams-varslinger for alle brukere, velger du **Ja** i ledeteksten.</span><span class="sxs-lookup"><span data-stu-id="59bf1-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-varslinger for alle brukere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="59bf1-127">Aktivere eller deaktivere Teams-varslinger for individuelle brukere</span><span class="sxs-lookup"><span data-stu-id="59bf1-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="59bf1-128">Når du har aktivert varsler for Teams-appen i Dynamics 365 Human Resources, kan du aktivere eller deaktivere varslinger for individuelle brukere.</span><span class="sxs-lookup"><span data-stu-id="59bf1-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="59bf1-129">Velg **Systemadministrasjon** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="59bf1-130">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-130">Select **Links**.</span></span>

3. <span data-ttu-id="59bf1-131">Under **Brukere** velger du **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="59bf1-132">Velg kategorien **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="59bf1-133">Sett **Aktiver varslinger for Teams-app** til **Ja** for å aktivere varslinger for brukeren, eller **Nei** for å deaktivere varslinger for brukeren.</span><span class="sxs-lookup"><span data-stu-id="59bf1-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivere varslinger for Teams-appen i kategorien Arbeidsflyt i Brukeralternativer](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="59bf1-135">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="59bf1-136">Språk som støttes</span><span class="sxs-lookup"><span data-stu-id="59bf1-136">Supported languages</span></span>

<span data-ttu-id="59bf1-137">Appen Dynamics 365 Human Resources i Teams støtter følgende språk:</span><span class="sxs-lookup"><span data-stu-id="59bf1-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="59bf1-138">ID for nasjonal innstilling</span><span class="sxs-lookup"><span data-stu-id="59bf1-138">Locale ID</span></span> | <span data-ttu-id="59bf1-139">Språk</span><span class="sxs-lookup"><span data-stu-id="59bf1-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="59bf1-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="59bf1-140">de-DE</span></span> | <span data-ttu-id="59bf1-141">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="59bf1-141">German (Germany)</span></span> |
| <span data-ttu-id="59bf1-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="59bf1-142">es-ES</span></span> | <span data-ttu-id="59bf1-143">Spansk (Spania)</span><span class="sxs-lookup"><span data-stu-id="59bf1-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="59bf1-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="59bf1-144">es-MX</span></span> | <span data-ttu-id="59bf1-145">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="59bf1-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="59bf1-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="59bf1-146">fr-CA</span></span> | <span data-ttu-id="59bf1-147">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="59bf1-147">French (Canada)</span></span> |
| <span data-ttu-id="59bf1-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="59bf1-148">fr-FR</span></span> | <span data-ttu-id="59bf1-149">Fransk (Frankrike)</span><span class="sxs-lookup"><span data-stu-id="59bf1-149">French (France)</span></span> |
| <span data-ttu-id="59bf1-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="59bf1-150">it-IT</span></span> | <span data-ttu-id="59bf1-151">Italiensk (Italia)</span><span class="sxs-lookup"><span data-stu-id="59bf1-151">Italian (Italy)</span></span> |
| <span data-ttu-id="59bf1-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="59bf1-152">nl-NL</span></span> | <span data-ttu-id="59bf1-153">Nederlandsk (Nederland)</span><span class="sxs-lookup"><span data-stu-id="59bf1-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="59bf1-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="59bf1-154">pt-BR</span></span> | <span data-ttu-id="59bf1-155">Portugisisk (Brasil)</span><span class="sxs-lookup"><span data-stu-id="59bf1-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="59bf1-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="59bf1-156">tr-TR</span></span> | <span data-ttu-id="59bf1-157">Tyrkisk (Tyrkia)</span><span class="sxs-lookup"><span data-stu-id="59bf1-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="59bf1-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="59bf1-158">zh-CN</span></span> | <span data-ttu-id="59bf1-159">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="59bf1-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="59bf1-160">Notater</span><span class="sxs-lookup"><span data-stu-id="59bf1-160">Notes</span></span>

<span data-ttu-id="59bf1-161">Følgende arbeidselementer er planlagt for fremtidige versjoner:</span><span class="sxs-lookup"><span data-stu-id="59bf1-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="59bf1-162">Arbeidselement</span><span class="sxs-lookup"><span data-stu-id="59bf1-162">Work item</span></span> | <span data-ttu-id="59bf1-163">Status</span><span class="sxs-lookup"><span data-stu-id="59bf1-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="59bf1-164">Balansen er feil når du sender inn fridager for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="59bf1-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="59bf1-165">Prognoser er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="59bf1-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="59bf1-166">Saldoen vises for den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="59bf1-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="59bf1-167">Kan ikke avbryte en forespørsel med statusen **Til vurdering**.</span><span class="sxs-lookup"><span data-stu-id="59bf1-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="59bf1-168">Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon.</span><span class="sxs-lookup"><span data-stu-id="59bf1-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="59bf1-169">Saldoinformasjon beregnes per i dag.</span><span class="sxs-lookup"><span data-stu-id="59bf1-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="59bf1-170">Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="59bf1-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="59bf1-171">Feilsøking</span><span class="sxs-lookup"><span data-stu-id="59bf1-171">Troubleshooting</span></span>

<span data-ttu-id="59bf1-172">Hvis en bruker har problemer med å logge på eller bruke Human Resources Teams-appen, kan du prøve å følge disse instruksjonene for feilsøking.</span><span class="sxs-lookup"><span data-stu-id="59bf1-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="59bf1-173">Hvis du fortsatt har problemer etter feilsøking, kontakter du kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="59bf1-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="59bf1-174">For mer informasjon, se [Få kundestøtte](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="59bf1-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="59bf1-175">Kan ikke logge på Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="59bf1-176">Hvis en bruker kontakter deg fordi vedkommende ikke kan logge på appen, må du kontrollere at brukeren har en tilknyttet ansattpost i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="59bf1-177">Feil under godkjenning av permisjonsforespørsler i Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="59bf1-178">Hvis en bruker får en feilmelding under forsøk på å godkjenne permisjonsforespørsler i Teams-appen, kan du prøve følgende feilsøkingstrinn:</span><span class="sxs-lookup"><span data-stu-id="59bf1-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="59bf1-179">Kontroller at Teams-kontoen er den samme som de bruker for å få tilgang til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="59bf1-180">Kontroller at de er en gyldig godkjenner for forespørselen ved å kontrollere arbeidsflytinnstillingene for permisjonsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="59bf1-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="59bf1-181">Hvis du vil ha mer informasjon om arbeidsflyter for permisjonsforespørsel, kan du se [Opprette en permisjonsforespørsel](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="59bf1-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="59bf1-182">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="59bf1-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="59bf1-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="59bf1-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="59bf1-184">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="59bf1-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="59bf1-185">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="59bf1-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="59bf1-186">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="59bf1-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="59bf1-187">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="59bf1-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="59bf1-188">Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="59bf1-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="59bf1-189">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="59bf1-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="59bf1-190">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59bf1-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="59bf1-191">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="59bf1-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="59bf1-192">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="59bf1-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="59bf1-193">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="59bf1-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="59bf1-194">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="59bf1-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="59bf1-195">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="59bf1-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="59bf1-196">Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Microsoft Teams, kan bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.</span><span class="sxs-lookup"><span data-stu-id="59bf1-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="59bf1-197">Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="59bf1-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="59bf1-198">Disse dataene kan være lagret i Microsoft Azure Event Grid i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer.</span><span class="sxs-lookup"><span data-stu-id="59bf1-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="59bf1-199">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="59bf1-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="59bf1-200">Mens du samtaler med chatroboten i Human Resources-appen, kan samtaleinnholdet lagres i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="59bf1-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="59bf1-201">Disse dataene kan være lagret i Azure Cosmos DB i opptil 24 timer, og kan behandles utenfor det geografiske området der leierens Human Resources-tjeneste distribueres, krypteres i transitt og når inaktiv og brukes ikke brukes av Microsoft eller dets underprosesser for opplærings- eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="59bf1-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="59bf1-202">Hvis du vil forstå hvor dataene er lagret i Teams, kan du se: [Plassering av data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="59bf1-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="59bf1-203">Hvis du vil begrense tilgangen til Human Resources-appen i Microsoft Teams for organisasjonen eller brukere i organisasjonen, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="59bf1-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="59bf1-204">Se også</span><span class="sxs-lookup"><span data-stu-id="59bf1-204">See also</span></span> 

[<span data-ttu-id="59bf1-205">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="59bf1-206">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="59bf1-207">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="59bf1-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]