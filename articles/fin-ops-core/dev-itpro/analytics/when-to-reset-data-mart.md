---
title: Vanlige spørsmål om tilbakestilling av data mart
description: Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av data mart.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266615"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="c2a56-103">Vanlige spørsmål om tilbakestilling av data mart</span><span class="sxs-lookup"><span data-stu-id="c2a56-103">Data mart resets FAQ</span></span>

<span data-ttu-id="c2a56-104">Dette emnet gir svar på noen vanlige spørsmål om tilbakestilling av data mart.</span><span class="sxs-lookup"><span data-stu-id="c2a56-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="c2a56-105">En tilbakestilling av data mart kan være en tidkrevende prosess og, avhengig av omstendighetene, kan det hende at det ikke er den løsningen som kreves.</span><span class="sxs-lookup"><span data-stu-id="c2a56-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="c2a56-106">Derfor inneholder dette emnet informasjon om forhold der en tilbakestilling av data mart kan hjelpe, og også forhold der det sannsynligvis ikke vil hjelpe.</span><span class="sxs-lookup"><span data-stu-id="c2a56-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="c2a56-107">Hva er en tilbakestilling av data mart?</span><span class="sxs-lookup"><span data-stu-id="c2a56-107">What is a data mart reset?</span></span>

<span data-ttu-id="c2a56-108">En datatilbakestilling av data mart vil deaktivere integreringsoppgavene, slette alle data mart-data og deretter aktivere integreringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="c2a56-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="c2a56-109">For å sikre at de gamle dataene ikke settes inn, kan en datatilbakestilling startes bare etter at eksisterende oppgaver er fullført.</span><span class="sxs-lookup"><span data-stu-id="c2a56-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="c2a56-110">Hvis du prøver å tilbakestille data mart før alle oppgavene er fullført, kan du for eksempel få meldingen: "Tilbakestilling av data mart vil ikke kunne behandles på grunn av en aktiv oppgave.</span><span class="sxs-lookup"><span data-stu-id="c2a56-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="c2a56-111">Prøv på nytt senere."</span><span class="sxs-lookup"><span data-stu-id="c2a56-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="c2a56-112">Når må jeg tilbakestille et data mart?</span><span class="sxs-lookup"><span data-stu-id="c2a56-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="c2a56-113">Hvis én eller flere av de følgende erklæringene gjelder for din situasjon, kan organisasjonen dra nytte av en tilbakestilling av data mart:</span><span class="sxs-lookup"><span data-stu-id="c2a56-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="c2a56-114">Applikasjonsdatabasen ble gjenopprettet.</span><span class="sxs-lookup"><span data-stu-id="c2a56-114">The application database was restored.</span></span>
- <span data-ttu-id="c2a56-115">Du har åpnet en støtteforespørsel, og en kundestøttetekniker har bedt deg om å tilbakestille data mart som en del av et feilsøkingstrinn.</span><span class="sxs-lookup"><span data-stu-id="c2a56-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="c2a56-116">Når blir et data mart tilbakestilt på feil måte?</span><span class="sxs-lookup"><span data-stu-id="c2a56-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="c2a56-117">Her er noen omstendigheter der vi anbefaler at du ikke tilbakestiller et data mart:</span><span class="sxs-lookup"><span data-stu-id="c2a56-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="c2a56-118">Du har ytelsesproblemer som er knyttet til datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c2a56-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="c2a56-119">Du har et gjentakende tilbakestillingsmønster av en av følgende årsaker:</span><span class="sxs-lookup"><span data-stu-id="c2a56-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="c2a56-120">**Manglende data** – Hvis du ser at det mangler data, åpner du en støtteforespørsel hos Microsoft for å gå gjennom rapportformatet og mulige problemer med datasynkronisering.</span><span class="sxs-lookup"><span data-stu-id="c2a56-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="c2a56-121">**Fastlåst integreringstilstand**</span><span class="sxs-lookup"><span data-stu-id="c2a56-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="c2a56-122">**Foreldede poster** – Foreldede poster alene gir ikke nødvendigvis en god grunn til å tilbakestille data mart.</span><span class="sxs-lookup"><span data-stu-id="c2a56-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="c2a56-123">Hvis du har et stort datasett, tar det litt tid å kjøre tilbakestillingsprosessen, men den fører sannsynligvis ikke til forbedringer.</span><span class="sxs-lookup"><span data-stu-id="c2a56-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="c2a56-124">Hvis jeg tilbakestiller data mart, vil jeg miste rapporter som jeg allerede har utformet?</span><span class="sxs-lookup"><span data-stu-id="c2a56-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="c2a56-125">Nei.</span><span class="sxs-lookup"><span data-stu-id="c2a56-125">No.</span></span> <span data-ttu-id="c2a56-126">Rapportene dine lagres i SQL-tabeller som ikke påvirkes av en tilbakestilling av data mart.</span><span class="sxs-lookup"><span data-stu-id="c2a56-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="c2a56-127">Hvis du er opptatt av å miste rapporter du har utformet, kan du sikkerhetskopiere utformingene du ikke vil miste.</span><span class="sxs-lookup"><span data-stu-id="c2a56-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="c2a56-128">Hvis du vil sikkerhetskopiere utforminger, åpner du Rapportutforming og går til **Firma \> Firmaer \> Byggesteiner \> Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="c2a56-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="c2a56-129">Må alle brukerne avslutte systemet før jeg kan tilbakestille data mart?</span><span class="sxs-lookup"><span data-stu-id="c2a56-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="c2a56-130">Nei.</span><span class="sxs-lookup"><span data-stu-id="c2a56-130">No.</span></span> <span data-ttu-id="c2a56-131">Brukere kan fortsette å arbeide i systemet under tilbakestillingen av data mart.</span><span class="sxs-lookup"><span data-stu-id="c2a56-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="c2a56-132">De vil imidlertid ikke få tilgang til rapporter som ble opprettet med Financial Reporter før tilbakestillingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="c2a56-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
