---
title: Human Resources-app i Teams
description: Dette emnet gir en innføring i Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
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
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388122"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="5db58-103">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="5db58-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5db58-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan ansatte raskt be om fridager og vise saldoinformasjon for fridager i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5db58-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="5db58-105">Ansatte kan samhandle med en robot for å be om informasjon.</span><span class="sxs-lookup"><span data-stu-id="5db58-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="5db58-106">Kateogrien **Fridager** gir mer detaljert informasjon.</span><span class="sxs-lookup"><span data-stu-id="5db58-106">The **Time off** tab provides more detailed information.</span></span>

![Robot for permisjonsapp i Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Kategorien Fridager i permisjonsapp for Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="5db58-109">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="5db58-109">Install and setup</span></span>

<span data-ttu-id="5db58-110">Du kan finne Human Resources-appen i Teams-butikken.</span><span class="sxs-lookup"><span data-stu-id="5db58-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="5db58-111">Hvis du vil ha informasjon om hvordan du installerer Teams-appen, kan du se [Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="5db58-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="5db58-112">Hvis du vil ha informasjon om hvordan du administrerer apptillatelser i Teams, kan du se [Behandle policyer for apptillatelse i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="5db58-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="5db58-113">Kjente problemer</span><span class="sxs-lookup"><span data-stu-id="5db58-113">Known issues</span></span>

| <span data-ttu-id="5db58-114">Avgang</span><span class="sxs-lookup"><span data-stu-id="5db58-114">Issue</span></span> | <span data-ttu-id="5db58-115">Status</span><span class="sxs-lookup"><span data-stu-id="5db58-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="5db58-116">Balansen er feil når du sender inn fridager for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="5db58-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="5db58-117">Prognoser er ennå ikke tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="5db58-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="5db58-118">Saldoen vises for den gjeldende datoen.</span><span class="sxs-lookup"><span data-stu-id="5db58-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="5db58-119">Når antall timer i en eksisterende forespørsel reduseres, vil den **gjenværende saldoen** gå ned i stedet for opp.</span><span class="sxs-lookup"><span data-stu-id="5db58-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="5db58-120">Vi vil håndtere dette kjente problemet i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="5db58-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="5db58-121">Visningen er feil, men de riktige beløpene justeres ved innsending.</span><span class="sxs-lookup"><span data-stu-id="5db58-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="5db58-122">To kort for **Kommende fridager** vises for samme dato.</span><span class="sxs-lookup"><span data-stu-id="5db58-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="5db58-123">Kortene representerer atskilte innsendinger.</span><span class="sxs-lookup"><span data-stu-id="5db58-123">The cards represent individual submissions.</span></span> <span data-ttu-id="5db58-124">Vi vil fortsette å registrere tilbakemeldinger og gjøre justeringer.</span><span class="sxs-lookup"><span data-stu-id="5db58-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="5db58-125">Kan ikke avbryte en forespørsel med statusen **Til vurdering**.</span><span class="sxs-lookup"><span data-stu-id="5db58-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="5db58-126">Denne funksjonaliteten støttes ikke for øyeblikket og blir lagt til i en fremtidig versjon.</span><span class="sxs-lookup"><span data-stu-id="5db58-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="5db58-127">Saldoinformasjon beregnes per i dag.</span><span class="sxs-lookup"><span data-stu-id="5db58-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="5db58-128">Systemet viser ikke saldoer i løpet av avsetningsperioden, selv om det er konfigurert i permisjons- og fraværsparametere.</span><span class="sxs-lookup"><span data-stu-id="5db58-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="5db58-129">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="5db58-129">Privacy notice</span></span>

<span data-ttu-id="5db58-130">Ved hjelp av Dynamics 365 Human Resources-roboten i Microsoft Teams blir brukerens tekstinndata analysert for å forstå den underliggende spørringen/hensikten.</span><span class="sxs-lookup"><span data-stu-id="5db58-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="5db58-131">Brukerens inndata, for eksempel "Søk i konto i Contoso", rutes til en av Microsofts kognitive tjenester, kalt Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="5db58-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="5db58-132">Les mer om LUIS  [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="5db58-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="5db58-133">LUIS-tjenesten skiller eller forstår gjengivelsen av brukerens inndata (i dette tilfellet er hensikten å finne informasjon) og målenheten (i dette tilfellet er den tiltenkte enheten en konto kalt Contoso).</span><span class="sxs-lookup"><span data-stu-id="5db58-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="5db58-134">Denne informasjonen sendes deretter videre til Microsofts [Azure-robotrammeverk](https://azure.microsoft.com/services/bot-service/) som kommuniserer med data fra Dynamics 365 Human Resources, og henter den ønskede informasjonen for brukerspørringen.</span><span class="sxs-lookup"><span data-stu-id="5db58-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="5db58-135">Ved å installere og tillate tilgang til bruk av robot, godtar du at LUIS-tjenesten og Azure-robotrammeverket behandler hensikten bak inndataene, noe som resulterer i en forbedret samtalebasert brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="5db58-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="5db58-136">LUIS-tjenesten og Azure-robotrammeverket kan ha forskjellige samsvarsnivåer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5db58-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5db58-137">Selv om LUIS-tjenesten har tilgang bare til brukerspørringene og ikke er utformet for å være koblet til brukerens Dynamics 365 Human Resources-data eller konto, kan en bruker av Dynamics 365 Human Resources-roboten frivillig angi en spørring som inneholder kundedata, personlige data eller andre data, og denne typen spørringsinnhold kan sendes til LUIS-tjenesten og det profesjonelle Azure-robotrammeverket.</span><span class="sxs-lookup"><span data-stu-id="5db58-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="5db58-138">Innholdet i brukerens spørringer og meldinger beholdes i LUIS-systemet i maksimalt 30 dager, blir kryptert når inaktive, og brukes ikke til opplæring eller forbedring av tjenesten.</span><span class="sxs-lookup"><span data-stu-id="5db58-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="5db58-139">Les mer om kognitive tjenester [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="5db58-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="5db58-140">Hvis du vil behandle administrasjonsinnstillinger for apper i Microsoft Teams, går du til [administrasjonssenteret for Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="5db58-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="5db58-141">Se også</span><span class="sxs-lookup"><span data-stu-id="5db58-141">See also</span></span> 

[<span data-ttu-id="5db58-142">Laste ned og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5db58-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="5db58-143">Hjelpesenter for Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5db58-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="5db58-144">Behandle permisjonsforespørsler i Teams</span><span class="sxs-lookup"><span data-stu-id="5db58-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

