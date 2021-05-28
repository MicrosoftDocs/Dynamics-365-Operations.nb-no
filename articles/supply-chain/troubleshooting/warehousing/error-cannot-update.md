---
title: Det oppstår en feil når lokasjonen velges under plukklisteregistrering
description: Det oppstår en feil når lokasjonen velges under plukklisteregistrering.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026763"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="f2b7b-103">Det oppstår en feil når lokasjonen velges under plukklisteregistrering</span><span class="sxs-lookup"><span data-stu-id="f2b7b-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="f2b7b-104">KB-nummer: 4613106</span><span class="sxs-lookup"><span data-stu-id="f2b7b-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="f2b7b-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f2b7b-105">Symptoms</span></span>

<span data-ttu-id="f2b7b-106">Dette problemet oppstår når systemet er konfigurert til å reservere salgsordrer automatisk.</span><span class="sxs-lookup"><span data-stu-id="f2b7b-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="f2b7b-107">Hvis du prøver å velge lokasjonen for en plukklisteregistreringslinje, får du følgende feilmelding når du bruker lagerstyringsreservasjonsprosesser (WMS):</span><span class="sxs-lookup"><span data-stu-id="f2b7b-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="f2b7b-108">Kan ikke oppdatere antall med nye dimensjoner</span><span class="sxs-lookup"><span data-stu-id="f2b7b-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="f2b7b-109">Dette problemet kan oppstå fordi du ikke har nok lagerbeholdning på en angitt lokasjon.</span><span class="sxs-lookup"><span data-stu-id="f2b7b-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="f2b7b-110">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="f2b7b-110">Resolution</span></span>

<span data-ttu-id="f2b7b-111">Systemet fungerer som tiltenkt.</span><span class="sxs-lookup"><span data-stu-id="f2b7b-111">The system is behaving as designed.</span></span>

<span data-ttu-id="f2b7b-112">I scenarier der du bruker reserveringsprosessen på lagernivå, anbefaler vi at du bruker den manuelle reserveringsprosessen fra plukklinjen hvis du ikke bruker lagerbeholdningen på alle lagerdimensjonsnivåer.</span><span class="sxs-lookup"><span data-stu-id="f2b7b-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="f2b7b-113">Du kan deretter bruke funksjonen *Reserver parti* til å fordele de nedre reserveringene, for eksempel lokasjon, for alle tilgjengelige lagerantall.</span><span class="sxs-lookup"><span data-stu-id="f2b7b-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
