---
title: Klientfrakoblinger
description: Denne artikkelen forklarer hva du gjør hvis kunden kobles fra miljøet og ikke vet hvorfor.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fcb7e5e3230aee9f6c04e4854c8eea836ae14c7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053425"
---
# <a name="client-disconnects"></a><span data-ttu-id="5a1b9-103">Klientfrakoblinger</span><span class="sxs-lookup"><span data-stu-id="5a1b9-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5a1b9-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="5a1b9-104">**Environment details**</span></span> 

<span data-ttu-id="5a1b9-105">Dette problemet kan oppstå i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="5a1b9-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="5a1b9-106">**Symptom**</span></span> 

<span data-ttu-id="5a1b9-107">Kunden kobles fra miljøet og vet ikke hvorfor.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="5a1b9-108">Kunden mottar én av følgende feilmeldinger:</span><span class="sxs-lookup"><span data-stu-id="5a1b9-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="5a1b9-109">Forbindelsen er brutt.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-109">We've lost your connection.</span></span> <span data-ttu-id="5a1b9-110">Klikk Lukk for å fortsette å arbeide.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-110">Click Close to continue working.</span></span>
- <span data-ttu-id="5a1b9-111">Det virker som du har mistet nettverkstilkoblingen. Klikk Prøv på nytt for å prøve på nytt.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="5a1b9-112">**Rødt flagg**</span><span class="sxs-lookup"><span data-stu-id="5a1b9-112">**Red flag**</span></span>

<span data-ttu-id="5a1b9-113">Dette skjer ofte når brukere er i fasen for implementeringen, sammenligner informasjon på tvers av produksjon og testmiljøer og glemmer at de flytter mellom økter.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="5a1b9-114">Hvis brukere er på dette tidspunktet, vil de mest sannsynlig oppleve dette problemet.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="5a1b9-115">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="5a1b9-115">**Issue**</span></span> 

<span data-ttu-id="5a1b9-116">**Weblesertyper:** Google Chrome, Internet Explorer og Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5a1b9-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="5a1b9-117">Microsoft Dynamics 365 Human Resources kobler fra brukere når to forskjellige økter er åpne samtidig for samme bruker og samme weblesertype.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="5a1b9-118">(For eksempel viser bruker A både miljø 1 og miljø 2 i Chrome.) Det spiller ingen rolle om brukerne åpner ulike leservinduer eller forskjellige faner.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="5a1b9-119">Hvis den samme brukerlegitimasjonen brukes til å logge på både miljø 1 og miljø 2 samtidig og i den samme weblesertypen, kobler Human Resources fra én av øktene.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="5a1b9-120">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="5a1b9-120">**Solution**</span></span>

<span data-ttu-id="5a1b9-121">Kontroller at bare ett miljø er åpent om gangen for en bestemt webleser.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="5a1b9-122">Brukere kan åpne flere økter i samme miljø (det vil si flere faner i samme webleser).</span><span class="sxs-lookup"><span data-stu-id="5a1b9-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="5a1b9-123">Brukere som vil hoppe mellom to miljøer samtidig, bør åpne hvert miljø i en annen webleser.</span><span class="sxs-lookup"><span data-stu-id="5a1b9-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="5a1b9-124">(For eksempel kan bruker A vise miljø 1 i Chrome og miljø 2 i Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="5a1b9-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]