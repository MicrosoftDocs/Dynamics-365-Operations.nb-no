---
title: Endre eller tilordne en finanskalender på nytt
description: Dette emnet beskriver hvordan du endrer kalenderen som for øyeblikket er tilordnet finans, og hvordan du tilordner en ny kalender til finans.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039956"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="fc591-103">Endre eller tilordne en finanskalender på nytt</span><span class="sxs-lookup"><span data-stu-id="fc591-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc591-104">Dette emnet beskriver hvordan du endrer kalenderen som for øyeblikket er tilordnet finans, og hvordan du tilordner en ny kalender til finans.</span><span class="sxs-lookup"><span data-stu-id="fc591-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="fc591-105">Problem</span><span class="sxs-lookup"><span data-stu-id="fc591-105">Issue</span></span>

<span data-ttu-id="fc591-106">Noen ganger må firmaer enten endre den eksisterende kalenderen som er tilordnet finans, eller tilordne en ny kalender.</span><span class="sxs-lookup"><span data-stu-id="fc591-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="fc591-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="fc591-107">Resolution</span></span>

<span data-ttu-id="fc591-108">Det finnes to scenarioer for endring eller ny tilordning av en finanskalender.</span><span class="sxs-lookup"><span data-stu-id="fc591-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="fc591-109">Det første scenarioet omfatter endring av en eksisterende kalender som allerede er tilordnet finans.</span><span class="sxs-lookup"><span data-stu-id="fc591-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="fc591-110">Det andre scenarioet omfatter oppretting av en ny kalender og tilordning av den til finans.</span><span class="sxs-lookup"><span data-stu-id="fc591-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="fc591-111">Begge endringene kan utføres når som helst, også etter at transaksjoner er postert til finans.</span><span class="sxs-lookup"><span data-stu-id="fc591-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="fc591-112">Endre en eksisterende regnskapskalender</span><span class="sxs-lookup"><span data-stu-id="fc591-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="fc591-113">Hvis du vil endre en eksisterende kalender som er tilordnet finans, kan du gå til **Økonomimodul \> Finansoppsett \> Finans** og velge koblingen for regnskapskalenderen for å åpne siden **Finanskalendere**.</span><span class="sxs-lookup"><span data-stu-id="fc591-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="fc591-114">Det er begrensninger på hvilke endringer som kan gjøres i en kalender.</span><span class="sxs-lookup"><span data-stu-id="fc591-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="fc591-115">Du kan for eksempel endre start- og sluttdatoene for *periodene* i et år, men du kan ikke endre start- og sluttdatoene for et *år* i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="fc591-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="fc591-116">Hvis du vil endre periodene i et år, velger du riktig kalender og år.</span><span class="sxs-lookup"><span data-stu-id="fc591-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="fc591-117">Først bruker du knappen **Slett periode** til å slette noen av eller alle de eksisterende driftsperiodene.</span><span class="sxs-lookup"><span data-stu-id="fc591-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="fc591-118">Alle driftsperioder, bortsett fra den første, kan slettes.</span><span class="sxs-lookup"><span data-stu-id="fc591-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="fc591-119">Deretter kan du bruke knappen **Del opp periode** til å dele opp gjenstående periode eller perioder i nye perioder ved å angi en passende startdato for den neste perioden.</span><span class="sxs-lookup"><span data-stu-id="fc591-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="fc591-120">Når du har endret periodene i en kalender, må du kjøre prosessen **Beregn finansperioder på nytt** i hver juridiske enhet (firma) som kalenderen er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="fc591-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="fc591-121">Selv om ingen advarsel påminner deg om å fullføre dette trinnet, er omberegningsprosessen nødvendig for å oppdatere perioden som er tilordnet hver posterte transaksjon i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="fc591-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="fc591-122">Hvis du vil kjøre omberegningsprosessen, velger du **Beregn finansperioder på nytt** på siden **Finansoppsett** i hvert firma.</span><span class="sxs-lookup"><span data-stu-id="fc591-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="fc591-123">Hvis omberegningsprosessen ikke kjøres, kan det hende at transaksjonssaldoer på en råbalanse eller i regnskapsoppgjør er feilaktig tatt med i perioder.</span><span class="sxs-lookup"><span data-stu-id="fc591-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="fc591-124">I dette tilfellet kan du når som helst rette opp saldoene ved å kjøre omberegningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fc591-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="fc591-125">Tilordne en ny regnskapskalender</span><span class="sxs-lookup"><span data-stu-id="fc591-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="fc591-126">Hvis du vil tilordne en ny regnskapskalender, kan du gå til **Økonomimodul \> Finansoppsett \> Finans** og velge **Rediger** for å sette siden **Finans** i redigeringsmodus.</span><span class="sxs-lookup"><span data-stu-id="fc591-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="fc591-127">Velg deretter en ny regnskapskalender i feltet **Regnskapskalender**.</span><span class="sxs-lookup"><span data-stu-id="fc591-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="fc591-128">Når du har endret regnskapskalenderen for finans, må du kjøre **Beregn finansperioder på nytt**.</span><span class="sxs-lookup"><span data-stu-id="fc591-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="fc591-129">Når du tilordner en ny regnskapskalender til finans, får du en melding som minner deg på å fullføre dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="fc591-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="fc591-130">Selv om meldingen kan indikere at omberegningsprosessen er valgfri, så er den ikke det.</span><span class="sxs-lookup"><span data-stu-id="fc591-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="fc591-131">Det er nødvendig å oppdatere perioden som er tilordnet hver posterte transaksjon i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="fc591-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="fc591-132">Hvis du vil kjøre omberegningsprosessen, velger du **Beregn finansperioder på nytt** på siden **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="fc591-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="fc591-133">Hvis omberegningsprosessen ikke kjøres, kan det hende at transaksjonssaldoer på en råbalanse eller i regnskapsoppgjør er feilaktig tatt med i perioder.</span><span class="sxs-lookup"><span data-stu-id="fc591-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="fc591-134">I dette tilfellet kan du når som helst rette opp saldoene ved å kjøre omberegningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="fc591-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
