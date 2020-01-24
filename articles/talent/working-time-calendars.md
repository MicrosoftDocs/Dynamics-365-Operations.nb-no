---
title: Arbeidstidskalendere
description: Dette emnet beskriver driftskalendere i Dynamics 365 Talent – Core HR og hvordan du definerer kalendere.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-07-01
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: f69bfec663cb8473c112f108813f042368439570
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897241"
---
# <a name="working-time-calendars"></a><span data-ttu-id="5b581-103">Arbeidstidskalendere</span><span class="sxs-lookup"><span data-stu-id="5b581-103">Working time calendars</span></span>

<span data-ttu-id="5b581-104">Driftskalenderen lar deg opprette en kalender med timer og dager som de ansatte arbeider i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="5b581-104">The working time calendar enables you to create a calendar with the hours and days that employees work in your organization.</span></span> <span data-ttu-id="5b581-105">Kalendere brukes til å strømlinjeforme forespørsler om fridager som standard i timer eller dager.</span><span class="sxs-lookup"><span data-stu-id="5b581-105">Calendars streamline the time off request process by default in the hours or days.</span></span> <span data-ttu-id="5b581-106">Når en ansatt sender en forespørsel om fridager, trenger de ikke trenger å tenke på helligdager og stengetider, som er behandlet for dem gjennom driftskalenderen.</span><span class="sxs-lookup"><span data-stu-id="5b581-106">When an employee submits a time off request, they don't have to worry about holidays and closures, which is handled for them through the working time calendar.</span></span>

## <a name="setting-up-a-working-time-calendar"></a><span data-ttu-id="5b581-107">Definere en driftskalender</span><span class="sxs-lookup"><span data-stu-id="5b581-107">Setting up a working time calendar</span></span>

<span data-ttu-id="5b581-108">Kalendere inkluderer detaljer for generering, dagene og timene du vil inkludere, dagene i kalenderen, arbeidstider for disse dagene, i tillegg til registrerte ansatte.</span><span class="sxs-lookup"><span data-stu-id="5b581-108">Calendars include generation details, the days and hours you want to included, the days of the calendar, working times for those days as well as enrolled employees.</span></span> 

<span data-ttu-id="5b581-109">Følg denne fremgangsmåten for å definere en kalender:</span><span class="sxs-lookup"><span data-stu-id="5b581-109">To set up a calendar, follow these steps:</span></span>

1. <span data-ttu-id="5b581-110">På siden **Organisasjonsstyring** klikker du **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="5b581-110">On the **Organization Administration** page, click **Calendars**.</span></span>

2. <span data-ttu-id="5b581-111">I handlingsruten velger du **Ny** og angir et navn og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5b581-111">On the Action Pane, select **New** and enter a name and description.</span></span>

3. <span data-ttu-id="5b581-112">Velg arbeidsdager for organisasjonen og angi arbeidstiden.</span><span class="sxs-lookup"><span data-stu-id="5b581-112">Choose the work days for your organization and enter work time.</span></span>

4. <span data-ttu-id="5b581-113">Legg til helligdager og stengetider ved hjelp av **Legg til**-knappen.</span><span class="sxs-lookup"><span data-stu-id="5b581-113">Add Holidays and closures by using the **Add** button.</span></span>

5. <span data-ttu-id="5b581-114">Angi navnet og beskrivelsen for helligdager og stengetider, for eksempel offentlige høytidsdager eller helligdager.</span><span class="sxs-lookup"><span data-stu-id="5b581-114">Enter the name and description for the holidays and closures, such as US holidays or Bank holidays.</span></span> <span data-ttu-id="5b581-115">Angi datoene for helligdager og lukninger.</span><span class="sxs-lookup"><span data-stu-id="5b581-115">Enter the dates for the holidays and closures.</span></span> <span data-ttu-id="5b581-116">Lagre listen over helligdager og lukninger, og lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b581-116">Save the Holidays and closures list and close the page.</span></span>

6. <span data-ttu-id="5b581-117">Velg listen over helligdager og lukninger fra rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="5b581-117">Select the holidays and closures list from the drop-down menu.</span></span>

7. <span data-ttu-id="5b581-118">Hvis de ansatte har tid de ikke arbeider, for eksempel lunsj eller pauser, legger du til disse også.</span><span class="sxs-lookup"><span data-stu-id="5b581-118">If your employees have non-work time, such as lunches or breaks, add those as well.</span></span> <span data-ttu-id="5b581-119">Velg **Fritid**, og skrive inn et navn og tidsomfanget.</span><span class="sxs-lookup"><span data-stu-id="5b581-119">Select **Non-work time** and enter the name and time range.</span></span> <span data-ttu-id="5b581-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b581-120">Close the page.</span></span> 

8. <span data-ttu-id="5b581-121">Klikk **Legg til** for å legge til fritid i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="5b581-121">Click **Add** to add the non-work time to your calendar.</span></span>

9. <span data-ttu-id="5b581-122">I kategorien **Dager** velger du **Generer** for å generere dagene i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="5b581-122">On the **Days** tab, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="5b581-123">Angi datoområdet for kalenderen.</span><span class="sxs-lookup"><span data-stu-id="5b581-123">Enter the date range for the calendar.</span></span> <span data-ttu-id="5b581-124">Dagene og arbeidstidene genereres basert på arbeidsdagene og klokkeslettene som er definert under genereringsalternativene, sammen med datoene du valgte.</span><span class="sxs-lookup"><span data-stu-id="5b581-124">The days and working times are generated based on the work days and times defined under the generation options in conjunction with the dates selected.</span></span>

10. <span data-ttu-id="5b581-125">Hvis du vil tilordne en kalender til ansatte, velger du **Tilordne til ansatte** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b581-125">To assign a calendar to employees, select **Assign to employees** in the Action Pane.</span></span> <span data-ttu-id="5b581-126">Velg de ansatte du vil tilordne denne kalenderen til, og klikk deretter **Tilordne**.</span><span class="sxs-lookup"><span data-stu-id="5b581-126">Select the that employees you would like to assign this calendar to, and then click **Assign**.</span></span>

<span data-ttu-id="5b581-127">Ansatte trenger ikke å ha kalendere som er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="5b581-127">Employees aren't required to have calendars assigned.</span></span> <span data-ttu-id="5b581-128">Hvis det er definert en arbeidstidskalender, utelates fridager automatisk fra forespørselen.</span><span class="sxs-lookup"><span data-stu-id="5b581-128">If there is a working time calendar defined, off days are automatically excluded from the request.</span></span> <span data-ttu-id="5b581-129">Mengden, i timer eller dager, er som standard arbeidstiden som er definert i kalenderen.</span><span class="sxs-lookup"><span data-stu-id="5b581-129">The amount, in hours or days, defaults to the working times defined in the calendar.</span></span> <span data-ttu-id="5b581-130">Hvis en ansatt ikke har en kalender som er tilordnet, er alle dager tilgjengelige for fritid og fritidsmengden er ikke standard for forespørselen.</span><span class="sxs-lookup"><span data-stu-id="5b581-130">If an employee doesn't have a calendar assigned, all days are available for time off and the amount of time off is not the default for the request.</span></span> 
