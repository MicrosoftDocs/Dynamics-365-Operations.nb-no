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
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776314"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="a3a45-103">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a3a45-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3a45-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="a3a45-105">Ansatte kan samhandle med en robot for å be om informasjon.</span><span class="sxs-lookup"><span data-stu-id="a3a45-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="a3a45-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="a3a45-106">The **Time off** tab provides more detailed information.</span></span>

![Robot for permisjonsapp i Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="a3a45-109">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="a3a45-109">Install and setup</span></span>

<span data-ttu-id="a3a45-110">Du kan finne Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="a3a45-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="a3a45-111">Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="a3a45-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="a3a45-112">Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a3a45-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="a3a45-113">Aktiver varslinger for Human Resources-appen i Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="a3a45-114">Hvis du vil at brukere skal motta permisjonsforespørselsvarsler i Teams-appen, må du aktivere varslinger i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3a45-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="a3a45-115">Det er bare brukere som er logget på Teams og som bruker Teams-appen i Human Resources, som mottar varslinger.</span><span class="sxs-lookup"><span data-stu-id="a3a45-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="a3a45-116">Velg **Systemadministrasjon**i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3a45-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a3a45-117">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-117">Select **Links**.</span></span>

3. <span data-ttu-id="a3a45-118">Under **Oppsett** velger du **Systemparametere**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="a3a45-119">I kategorien **Generelt** setter du **Aktiver varslinger for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere varslinger for Teams-appen i Systemparametere](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="a3a45-121">Hvis du vil aktivere Teams-varslinger for alle brukere, velger du **Ja** i ledeteksten.</span><span class="sxs-lookup"><span data-stu-id="a3a45-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-varslinger for alle brukere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="a3a45-123">Aktivere eller deaktivere Teams-varslinger for individuelle brukere</span><span class="sxs-lookup"><span data-stu-id="a3a45-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="a3a45-124">Når du har aktivert varsler for Teams-appen i Human Resources, kan du aktivere eller deaktivere varslinger for individuelle brukere.</span><span class="sxs-lookup"><span data-stu-id="a3a45-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="a3a45-125">Velg **Systemadministrasjon**i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3a45-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a3a45-126">Velg **Koblinger**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-126">Select **Links**.</span></span>

3. <span data-ttu-id="a3a45-127">Under **Brukere** velger du **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="a3a45-128">Velg kategorien **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="a3a45-129">Sett **Aktiver varslinger for Teams-app** til **Ja** for å aktivere varslinger for brukeren, eller **Nei** for å deaktivere varslinger for brukeren.</span><span class="sxs-lookup"><span data-stu-id="a3a45-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivere varslinger for Teams-appen i kategorien Arbeidsflyt i Brukeralternativer](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="a3a45-131">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="a3a45-132">Kjente problemer</span><span class="sxs-lookup"><span data-stu-id="a3a45-132">Known issues</span></span>

| <span data-ttu-id="a3a45-133">Problem</span><span class="sxs-lookup"><span data-stu-id="a3a45-133">Issue</span></span> | <span data-ttu-id="a3a45-134">Status</span><span class="sxs-lookup"><span data-stu-id="a3a45-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="a3a45-135">Horisontal rulling fungerer ikke på Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="a3a45-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="a3a45-136">Horisontal rulling er ikke et problem på iOS-enheter eller skrivebordsenheter.</span><span class="sxs-lookup"><span data-stu-id="a3a45-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="a3a45-137">Vi arbeider med en løsning for Android.</span><span class="sxs-lookup"><span data-stu-id="a3a45-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="a3a45-138">Feil: Det oppstod et problem under søk etter et miljø å koble til.</span><span class="sxs-lookup"><span data-stu-id="a3a45-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="a3a45-139">Du kan få denne feilmeldingen selv om du har bekreftet at brukeren har tilgang til ett eller flere HR-miljøer.</span><span class="sxs-lookup"><span data-stu-id="a3a45-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="a3a45-140">I tillegg vil du kanskje ikke se alle de forventede miljøene.</span><span class="sxs-lookup"><span data-stu-id="a3a45-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="a3a45-141">Til vi har løst problemet, sletter du brukeren og importerer vedkommende på nytt for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="a3a45-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="a3a45-142">Balansen er feil når du sender inn fridager for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="a3a45-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="a3a45-143">Prognoser er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="a3a45-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="a3a45-144">Saldoen vises for den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="a3a45-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="a3a45-145">Kan ikke avbryte en forespørsel med statusen **Til vurdering**.</span><span class="sxs-lookup"><span data-stu-id="a3a45-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="a3a45-146">Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon.</span><span class="sxs-lookup"><span data-stu-id="a3a45-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="a3a45-147">Saldoinformasjon beregnes per i dag.</span><span class="sxs-lookup"><span data-stu-id="a3a45-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="a3a45-148">Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="a3a45-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="a3a45-149">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="a3a45-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a3a45-150">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a3a45-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a3a45-151">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="a3a45-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a3a45-152">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a3a45-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a3a45-153">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a3a45-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a3a45-154">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="a3a45-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a3a45-155">Denne informasjonen sendes deretter videre til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som kommuniserer med data fra Dynamics 365 Human Resources og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="a3a45-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a3a45-156">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="a3a45-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a3a45-157">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a3a45-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a3a45-158">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="a3a45-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a3a45-159">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="a3a45-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a3a45-160">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a3a45-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a3a45-161">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a3a45-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="a3a45-162">Microsoft Azure Event Grid og Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="a3a45-163">Når du bruker varslingsfunksjonen for Dynamics 365 Human Resources-appen i Teams, vil bestemte kundedata flyte utenfor det geografiske området der firmaets Human Resources-service blir distribuert.</span><span class="sxs-lookup"><span data-stu-id="a3a45-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="a3a45-164">Dynamics 365 Human Resources sender informasjon om den ansattes permisjonsforespørsel og arbeidsflytoppgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="a3a45-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a3a45-165">Disse dataene kan være lagret i opptil 24 timer og behandles i USA, krypteres i transitt og ved inaktivitet, og brukes ikke av Microsoft eller dets underprosesser til opplærings- eller serviceforbedringer.</span><span class="sxs-lookup"><span data-stu-id="a3a45-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3a45-166">Se også</span><span class="sxs-lookup"><span data-stu-id="a3a45-166">See also</span></span> 

[<span data-ttu-id="a3a45-167">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a3a45-168">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a3a45-169">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="a3a45-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

