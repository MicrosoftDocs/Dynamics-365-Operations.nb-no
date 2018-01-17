---
title: "Plukke eldste parti på en mobil enhet"
description: "Dette emnet beskriver hvordan du definerer og bruker alternativene for å velge det eldste partiet fra en mobilenhet."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 97bf72769f58d19d84f73f9de5ca9d1b354843ac
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="86136-103">Plukke eldste parti på en mobil enhet</span><span class="sxs-lookup"><span data-stu-id="86136-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="86136-104">Du kan få tilgang til konfigurasjonen **Plukk eldste parti** via en mobilenhetsmeny, og det gjør det mulig å tvinge eller instruere lagermedarbeidere til å plukke det eldste partiet på gjeldende sted.</span><span class="sxs-lookup"><span data-stu-id="86136-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="86136-105">Der det er aktuelt</span><span class="sxs-lookup"><span data-stu-id="86136-105">Where it applies</span></span>
<span data-ttu-id="86136-106">Plukk eldste parti er konfigurert på menyelementer for mobilenhet, og påvirker plukkingen for partivarer under.</span><span class="sxs-lookup"><span data-stu-id="86136-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="86136-107">Hvordan du definerer konfigurasjonen for plukk eldste parti</span><span class="sxs-lookup"><span data-stu-id="86136-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="86136-108">For varer som er angitt til å bruke eksisterende arbeid, kan **Plukk eldste parti** settes til **Ingen**, **Varsle**, eller **Fremtving** fra en mobilenhetsmeny.</span><span class="sxs-lookup"><span data-stu-id="86136-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="86136-109">**Ingen**: Arbeidere vil ikke motta meldinger og de kan plukke alle partier på plasseringen.</span><span class="sxs-lookup"><span data-stu-id="86136-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="86136-110">**Varsle** og **Fremtving**: En liste over partiene med den eldste utløpsdatoen vises over partikontrollen når arbeideren velger et parti.</span><span class="sxs-lookup"><span data-stu-id="86136-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="86136-111">Hvis lokasjonen er nummerskiltkontrollert, vises en liste over lisensplater med den eldste batchen over nummerskiltkontrollen.</span><span class="sxs-lookup"><span data-stu-id="86136-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="86136-112">**Varsle**: Hvis en arbeider velger et nummerskilt eller parti som ikke er i listen som vises, er kontrollen nedtonet, og det vises en advarsel om at det finnes et eldre parti å velge.</span><span class="sxs-lookup"><span data-stu-id="86136-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="86136-113">For at arbeideren skal kunne fortsette arbeidet må han/hun velge samme nummerskilt eller parti på nytt.</span><span class="sxs-lookup"><span data-stu-id="86136-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="86136-114">**Fremtving**: Arbeidere vil fortsette å motta meldingen om at det er et eldre parti som skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="86136-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>

