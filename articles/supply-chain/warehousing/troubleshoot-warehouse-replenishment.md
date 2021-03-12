---
title: Feilsøke lageretterfylling
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993897"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="af952-103">Feilsøke lageretterfylling</span><span class="sxs-lookup"><span data-stu-id="af952-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af952-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lageretterfylling i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="af952-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="af952-105">Jeg får følgende feilmelding: Blokkeringen av arbeid %1 kan ikke oppheves, fordi den har ikke-fullført etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="af952-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="af952-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="af952-106">Issue description</span></span>

<span data-ttu-id="af952-107">Plukkarbeid er blokkert på grunn av avhengig etterfyllingsarbeid.</span><span class="sxs-lookup"><span data-stu-id="af952-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af952-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="af952-108">Issue resolution</span></span>

<span data-ttu-id="af952-109">Når du bruker etterfylling av bølgebehov, hvis en plukklokasjon må etterfylles for å opofylle kildeordrebehovet, vil systemet opprette både etter fyllingsarbeidet og plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="af952-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="af952-110">Det blokkerer imidlertid plukkarbeidet til etterfyllingsarbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="af952-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="af952-111">Denne virkemåten er med hensikt, fordi plukklokasjonen ikke har nok lager hvis ikke etterfyllingsarbeidet er fullført.</span><span class="sxs-lookup"><span data-stu-id="af952-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="af952-112">Fullfør etterfyllingsarbeidet, og behandle deretter plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="af952-112">Complete the replenishment work, and then process the picking work.</span></span>
