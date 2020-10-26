---
title: Identifisere en hypotese og fastslå måledataene for et eksperiment
description: Dette emnet beskriver hvordan du identifiserer hypotesen og suksessmåledataene for et eksperiment som du kan kjøre på et nettsted for e-handel i Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930258"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="558c5-103">Identifisere en hypotese og fastslå suksessmåledataene for et eksperiment</span><span class="sxs-lookup"><span data-stu-id="558c5-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="558c5-104">Den første fasen i livssyklusen for eksperimentering omfatter å identifisere hypotesen for eksperimentet og fastslå måledataene du vil spore for å vurdere suksess.</span><span class="sxs-lookup"><span data-stu-id="558c5-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="558c5-105">Diagrammet nedenfor viser alle trinnene for å [konfigurere og kjøre et eksperiment](experimentation-overview.md) på et nettsted for e-handel i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="558c5-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="558c5-106">Flere trinn er beskrevet i separate emner.</span><span class="sxs-lookup"><span data-stu-id="558c5-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="558c5-107">[ ![Brukerreise for eksperimentering – identifisere](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="558c5-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="558c5-108">En hypotese er en erklæring der du forutser resultatet av eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="558c5-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="558c5-109">Mange faktorer inngår definisjonen av en hypotese, for eksempel undersøke brukerens atferd og nettstedsdata som du har samlet inn.</span><span class="sxs-lookup"><span data-stu-id="558c5-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="558c5-110">Med hypotesen definerer du antakelsen eller teorien du vil validere med eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="558c5-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="558c5-111">Et eksempel på en hypotese for eksperimentet kan være *et bilde av en hvit t-skjorte på startsiden vil gi en høyere grad av gjennomklikking enn en blå genser i sommermånedene fordi brukerne vil gjerne ha på seg noe lett og lyst om sommeren* .</span><span class="sxs-lookup"><span data-stu-id="558c5-111">An example of a hypothesis for your experiment may be " *a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.* "</span></span> <span data-ttu-id="558c5-112">I så fall kan du opprette variasjoner som inneholder en hvit t-skjorte og en blå genser og publisere begge samtidig.</span><span class="sxs-lookup"><span data-stu-id="558c5-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="558c5-113">For å validere en hypotese må et eksperiment som er en suksess eller er mislykket, være direkte knyttet til brukerhandlinger, for eksempel hvis nettstedsbrukeren klikker på en kobling eller knapp.</span><span class="sxs-lookup"><span data-stu-id="558c5-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="558c5-114">Disse handlingene må samsvare med hendelser som vil bli rapportert til tredjepartstjenesten som sporer eksperimentet.</span><span class="sxs-lookup"><span data-stu-id="558c5-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="558c5-115">Over tid blir prosentandelen av brukere som utfører handlingen, registrert som en måleverdi du kan bruke til å generere rapporter og utføre analyser.</span><span class="sxs-lookup"><span data-stu-id="558c5-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="558c5-116">Se emnet [Hendelser for Commerce-komponent for diagnose og feilsøking](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) for å se gjennom alle tilgjengelige hendelser og attributter.</span><span class="sxs-lookup"><span data-stu-id="558c5-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="558c5-117">Forrige trinn</span><span class="sxs-lookup"><span data-stu-id="558c5-117">Previous step</span></span>
[<span data-ttu-id="558c5-118">Eksperimentering i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="558c5-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="558c5-119">Neste trinn</span><span class="sxs-lookup"><span data-stu-id="558c5-119">Next step</span></span>
[<span data-ttu-id="558c5-120">Definer et eksperiment</span><span class="sxs-lookup"><span data-stu-id="558c5-120">Set up an experiment</span></span>](experimentation-setup.md)
