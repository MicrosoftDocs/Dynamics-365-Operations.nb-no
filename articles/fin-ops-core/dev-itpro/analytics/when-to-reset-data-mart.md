---
title: Når skal et data mart tilbakestilles
description: Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988998"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="a9db0-103">Når skal et data mart tilbakestilles</span><span class="sxs-lookup"><span data-stu-id="a9db0-103">When to reset a data mart</span></span>

<span data-ttu-id="a9db0-104">Det kan være tidkrevende å tilbakestille et data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="a9db0-105">Denne handlingen er kanskje ikke løsningen som trengs, avhengig av forholdene.</span><span class="sxs-lookup"><span data-stu-id="a9db0-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="a9db0-106">Dette emnet viser en oversikt over forhold som kan forbedres ved å tilbakestille et data mart, og forhold der det er usannsynlig at tilbakestilling av data mart hjelper.</span><span class="sxs-lookup"><span data-stu-id="a9db0-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="a9db0-107">Når må jeg tilbakestille et data mart?</span><span class="sxs-lookup"><span data-stu-id="a9db0-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="a9db0-108">Vurder følgende spørsmål før du tilbakestiller et data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="a9db0-109">Hvis du svarer ja på ett eller flere spørsmål, kan det bety at organisasjonen kan dra nytte av å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="a9db0-110">Ble applikasjonsdatabasen gjenopprettet?</span><span class="sxs-lookup"><span data-stu-id="a9db0-110">Was the application database restored?</span></span>
- <span data-ttu-id="a9db0-111">Hvis du har åpnet en støttehendelse og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn?</span><span class="sxs-lookup"><span data-stu-id="a9db0-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="a9db0-112">Når passer det ikke å tilbakestille et data mart?</span><span class="sxs-lookup"><span data-stu-id="a9db0-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="a9db0-113">Det finnes visse omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="a9db0-114">Disse omfatter følgende.</span><span class="sxs-lookup"><span data-stu-id="a9db0-114">These include the following.</span></span> 

- <span data-ttu-id="a9db0-115">Du har ytelsesproblemer som er knyttet til en datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="a9db0-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="a9db0-116">Hvis du har et gjentakende tilbakestillingsmønster av en av følgende årsaker:</span><span class="sxs-lookup"><span data-stu-id="a9db0-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="a9db0-117">**Manglende data**</span><span class="sxs-lookup"><span data-stu-id="a9db0-117">**Missing data**</span></span> 
  - <span data-ttu-id="a9db0-118">**Fastlåst integreringstilstand**</span><span class="sxs-lookup"><span data-stu-id="a9db0-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="a9db0-119">**Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="a9db0-120">Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.</span><span class="sxs-lookup"><span data-stu-id="a9db0-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="a9db0-121">Hva er en tilbakestilling av data mart?</span><span class="sxs-lookup"><span data-stu-id="a9db0-121">What is a data mart reset?</span></span>
- <span data-ttu-id="a9db0-122">En tilbakestilling starter bare når eksisterende oppgaver er fullført.</span><span class="sxs-lookup"><span data-stu-id="a9db0-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="a9db0-123">Dette sikrer at gamle data ikke settes inn.</span><span class="sxs-lookup"><span data-stu-id="a9db0-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="a9db0-124">På dette tidspunktet kan du for eksempel få meldingen «Tilbakestillingen av data mart kan ikke behandles på grunn av en aktiv oppgave.</span><span class="sxs-lookup"><span data-stu-id="a9db0-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="a9db0-125">Prøv på nytt senere.»</span><span class="sxs-lookup"><span data-stu-id="a9db0-125">Please try again later.”</span></span>
- <span data-ttu-id="a9db0-126">Tilbakestillingen deaktiverer integreringsoppgavene og sletter alle data mart-data.</span><span class="sxs-lookup"><span data-stu-id="a9db0-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="a9db0-127">Integreringen aktiveres på nytt.</span><span class="sxs-lookup"><span data-stu-id="a9db0-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="a9db0-128">Hvis jeg tilbakestiller data mart, vil jeg miste rapporter som jeg allerede har utformet?</span><span class="sxs-lookup"><span data-stu-id="a9db0-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="a9db0-129">Nei, rapportene lagres i SQL-tabeller som ikke påvirkes av en tilbakestilling av data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="a9db0-130">Hvis du er opptatt av å miste rapporter du har utformet, kan du sikkerhetskopiere utformingene du ikke vil miste.</span><span class="sxs-lookup"><span data-stu-id="a9db0-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="a9db0-131">Hvis du vil sikkerhetskopiere dem, åpner du Rapportutforming og går til **Firma > Firmaer > Byggesteiner > Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="a9db0-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="a9db0-132">Er det nødvendig for alle brukere å avslutte systemet for å tilbakestille data mart?</span><span class="sxs-lookup"><span data-stu-id="a9db0-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="a9db0-133">Nei, brukere kan fortsette å arbeide i systemet under tilbakestillingen av data mart.</span><span class="sxs-lookup"><span data-stu-id="a9db0-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="a9db0-134">De vil imidlertid ikke få tilgang til rapporter som ble opprettet med finansrapportering før tilbakestillingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="a9db0-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
