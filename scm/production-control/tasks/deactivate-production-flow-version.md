--- 
title: Deaktivere en produksjonsflytversjon
description: "Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres."
author: cvocph
manager: AnnBe
ms.date: 10/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db4b2857e9a7c99ee6fa4ef397f7ed99335faba
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="d7649-103">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="d7649-103">Deactivate a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7649-104">Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="d7649-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="d7649-105">Du bør bare bruke dette alternativet hvis alle Kanban-regler og aktiviteter er avsluttet og ikke skal aktiveres igjen.</span><span class="sxs-lookup"><span data-stu-id="d7649-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="d7649-106">Vær oppmerksom på at utløpsdatoen for alle Kanban-regler som er knyttet til denne produksjonsflytversjonen, vil bli oppdatert med gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="d7649-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="d7649-107">Hvis du vil endre en aktiv produksjonsflytversjon, bør du vurdere å angi en utløpsdato for den aktive versjonen og opprette en ny versjon.</span><span class="sxs-lookup"><span data-stu-id="d7649-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="d7649-108">Dette gjør at du kan fortsette produksjonsoperasjonene mens den nye versjonen og relaterte Kanban-regler klargjøres.</span><span class="sxs-lookup"><span data-stu-id="d7649-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="d7649-109">Du må angi en utløpsdato for å utløpe en aktiv produksjonsflytversjon.</span><span class="sxs-lookup"><span data-stu-id="d7649-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="d7649-110">I den forstand er deaktivering mer et unntak enn en regel.</span><span class="sxs-lookup"><span data-stu-id="d7649-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="d7649-111">Til denne prosedyren trenger du en produksjonsflyt med en versjon som kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="d7649-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="d7649-112">Ikke prøv dette i et produksjonsmiljø med mindre du er 100% sikker på at versjonen er fullstendig utdatert.</span><span class="sxs-lookup"><span data-stu-id="d7649-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="d7649-113">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="d7649-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="d7649-114">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="d7649-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d7649-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d7649-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d7649-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d7649-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d7649-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d7649-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d7649-118">Klikk Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="d7649-118">Click Deactivate.</span></span>
    * <span data-ttu-id="d7649-119">Ikke fortsett hvis du ikke er 100 % sikker på at denne produksjonsflytversjonen er foreldet.</span><span class="sxs-lookup"><span data-stu-id="d7649-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="d7649-120">Når du klikker OK, utløper alle aktive Kanban-regler og alle produksjons- og etterfyllingsaktiviteter for denne produksjonsflytversjonen opphører umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="d7649-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="d7649-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d7649-121">Click OK.</span></span>


