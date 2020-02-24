---
title: Klientfrakoblinger
description: Denne artikkelen forklarer hva du gjør hvis kunden kobles fra hans eller hennes miljø og ikke vet hvorfor.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.article: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 73f0c31d5153a82651ed77aa37bc10966ce7c9b1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010042"
---
# <a name="client-disconnects"></a><span data-ttu-id="96511-103">Klientfrakoblinger</span><span class="sxs-lookup"><span data-stu-id="96511-103">Client disconnects</span></span>

<span data-ttu-id="96511-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="96511-104">**Environment details**</span></span> 

<span data-ttu-id="96511-105">Dette problemet kan oppstå i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="96511-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="96511-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="96511-106">**Symptom**</span></span> 

<span data-ttu-id="96511-107">Kunden kobles fra hans eller hennes miljø og vet ikke hvorfor.</span><span class="sxs-lookup"><span data-stu-id="96511-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="96511-108">Kunden mottar én av følgende feilmeldinger:</span><span class="sxs-lookup"><span data-stu-id="96511-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="96511-109">Forbindelsen er brutt.</span><span class="sxs-lookup"><span data-stu-id="96511-109">We've lost your connection.</span></span> <span data-ttu-id="96511-110">Klikk Lukk for å fortsette å arbeide.</span><span class="sxs-lookup"><span data-stu-id="96511-110">Click Close to continue working.</span></span>
- <span data-ttu-id="96511-111">Det virker som du har mistet nettverkstilkoblingen. Klikk Prøv på nytt for å prøve på nytt.</span><span class="sxs-lookup"><span data-stu-id="96511-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="96511-112">**Rødt flagg**</span><span class="sxs-lookup"><span data-stu-id="96511-112">**Red flag**</span></span>

<span data-ttu-id="96511-113">Dette skjer ofte når brukere er i fasen for implementeringen, sammenligner informasjon på tvers av produksjon og testmiljøer og glemmer at de flytter mellom økter.</span><span class="sxs-lookup"><span data-stu-id="96511-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="96511-114">Hvis brukere er på dette tidspunktet, vil de mest sannsynlig oppleve dette problemet.</span><span class="sxs-lookup"><span data-stu-id="96511-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="96511-115">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="96511-115">**Issue**</span></span> 

<span data-ttu-id="96511-116">**Weblesertyper:** Google Chrome, Internet Explorer og Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="96511-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="96511-117">Microsoft Dynamics 365 Human Resources kobler fra brukere når to forskjellige økter er åpne samtidig for samme bruker og samme weblesertype.</span><span class="sxs-lookup"><span data-stu-id="96511-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="96511-118">(For eksempel viser bruker A både miljø 1 og miljø 2 i Chrome.) Det spiller ingen rolle om brukerne åpner ulike leservinduer eller forskjellige faner.</span><span class="sxs-lookup"><span data-stu-id="96511-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="96511-119">Hvis den samme brukerlegitimasjonen brukes til å logge på både miljø 1 og miljø 2 samtidig og i den samme weblesertypen, kobler Human Resources fra én av øktene.</span><span class="sxs-lookup"><span data-stu-id="96511-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="96511-120">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="96511-120">**Solution**</span></span>

<span data-ttu-id="96511-121">Kontroller at bare ett miljø er åpent om gangen for en bestemt webleser.</span><span class="sxs-lookup"><span data-stu-id="96511-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="96511-122">Brukere kan åpne flere økter i samme miljø (det vil si flere faner i samme webleser).</span><span class="sxs-lookup"><span data-stu-id="96511-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="96511-123">Brukere som vil hoppe mellom to miljøer samtidig, bør åpne hvert miljø i en annen webleser.</span><span class="sxs-lookup"><span data-stu-id="96511-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="96511-124">(For eksempel kan bruker A vise miljø 1 i Chrome og miljø 2 i Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="96511-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
