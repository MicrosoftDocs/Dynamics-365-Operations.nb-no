---
title: Frakoblinger for Talent-klient
description: Dette emnet forklarer hva du gjør hvis kunden kobles fra hans eller hennes miljø og ikke vet hvorfor.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305603"
---
# <a name="talent-client-disconnects"></a><span data-ttu-id="21843-103">Frakoblinger for Talent-klient</span><span class="sxs-lookup"><span data-stu-id="21843-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="21843-104">**Miljødetaljer**</span><span class="sxs-lookup"><span data-stu-id="21843-104">**Environment details**</span></span> 

<span data-ttu-id="21843-105">Dette problemet kan oppstå i alle miljøer.</span><span class="sxs-lookup"><span data-stu-id="21843-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="21843-106">**Symptom**</span><span class="sxs-lookup"><span data-stu-id="21843-106">**Symptom**</span></span> 

<span data-ttu-id="21843-107">Kunden kobles fra hans eller hennes miljø og vet ikke hvorfor.</span><span class="sxs-lookup"><span data-stu-id="21843-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="21843-108">Kunden mottar én av følgende feilmeldinger:</span><span class="sxs-lookup"><span data-stu-id="21843-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="21843-109">Forbindelsen er brutt.</span><span class="sxs-lookup"><span data-stu-id="21843-109">We've lost your connection.</span></span> <span data-ttu-id="21843-110">Klikk Lukk for å fortsette å arbeide.</span><span class="sxs-lookup"><span data-stu-id="21843-110">Click Close to continue working.</span></span>
- <span data-ttu-id="21843-111">Det virker som du har mistet nettverkstilkoblingen. Klikk Prøv på nytt for å prøve på nytt.</span><span class="sxs-lookup"><span data-stu-id="21843-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="21843-112">**Rødt flagg**</span><span class="sxs-lookup"><span data-stu-id="21843-112">**Red flag**</span></span>

<span data-ttu-id="21843-113">Dette skjer ofte når brukere er i fasen for implementeringen, sammenligner informasjon på tvers av produksjon og testmiljøer og glemmer at de flytter mellom økter.</span><span class="sxs-lookup"><span data-stu-id="21843-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="21843-114">Hvis brukere er på dette tidspunktet, vil de mest sannsynlig oppleve dette problemet.</span><span class="sxs-lookup"><span data-stu-id="21843-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="21843-115">**Avgang**</span><span class="sxs-lookup"><span data-stu-id="21843-115">**Issue**</span></span> 

<span data-ttu-id="21843-116">**Weblesertyper:** Google Chrome, Internet Explorer og Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="21843-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="21843-117">Microsoft Dynamics 365 for Talent-plattformen kobler fra brukere når to forskjellige økter er åpne samtidig for samme bruker og samme weblesertype.</span><span class="sxs-lookup"><span data-stu-id="21843-117">The Microsoft Dynamics 365 for Talent platform disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="21843-118">(For eksempel viser bruker A både miljø 1 og miljø 2 i Chrome.) Det spiller ingen rolle om brukerne åpner ulike leservinduer eller forskjellige faner.</span><span class="sxs-lookup"><span data-stu-id="21843-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="21843-119">Hvis den samme brukerlegitimasjonen brukes til å logge på både miljø 1 og miljø 2 samtidig og i den samme weblesertypen, kobler Talent fra én av øktene.</span><span class="sxs-lookup"><span data-stu-id="21843-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="21843-120">**Løsning**</span><span class="sxs-lookup"><span data-stu-id="21843-120">**Solution**</span></span>

<span data-ttu-id="21843-121">Kontroller at bare ett miljø er åpent om gangen for en bestemt webleser.</span><span class="sxs-lookup"><span data-stu-id="21843-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="21843-122">Brukere kan åpne flere økter i samme miljø (det vil si flere faner i samme webleser).</span><span class="sxs-lookup"><span data-stu-id="21843-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="21843-123">Brukere som vil hoppe mellom to miljøer samtidig, bør åpne hvert miljø i en annen webleser.</span><span class="sxs-lookup"><span data-stu-id="21843-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="21843-124">(For eksempel kan bruker A vise miljø 1 i Chrome og miljø 2 i Microsoft Edge.)</span><span class="sxs-lookup"><span data-stu-id="21843-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>
