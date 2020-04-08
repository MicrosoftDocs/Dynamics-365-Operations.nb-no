---
title: Deaktivere en produksjonsflytversjon
description: Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 860873a1fd61d52f642774e69d48c5ef6c7465a9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146842"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="79a58-103">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="79a58-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="79a58-104">Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="79a58-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="79a58-105">Du bør bare bruke dette alternativet hvis alle Kanban-regler og aktiviteter er avsluttet og ikke skal aktiveres igjen.</span><span class="sxs-lookup"><span data-stu-id="79a58-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="79a58-106">Vær oppmerksom på at utløpsdatoen for alle Kanban-regler som er knyttet til denne produksjonsflytversjonen, vil bli oppdatert med gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="79a58-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="79a58-107">Hvis du vil endre en aktiv produksjonsflytversjon, bør du vurdere å angi en utløpsdato for den aktive versjonen og opprette en ny versjon.</span><span class="sxs-lookup"><span data-stu-id="79a58-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="79a58-108">Dette gjør at du kan fortsette produksjonsoperasjonene mens den nye versjonen og relaterte Kanban-regler klargjøres.</span><span class="sxs-lookup"><span data-stu-id="79a58-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="79a58-109">Du må angi en utløpsdato for å utløpe en aktiv produksjonsflytversjon.</span><span class="sxs-lookup"><span data-stu-id="79a58-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="79a58-110">I den forstand er deaktivering mer et unntak enn en regel.</span><span class="sxs-lookup"><span data-stu-id="79a58-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="79a58-111">Til denne prosedyren trenger du en produksjonsflyt med en versjon som kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="79a58-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="79a58-112">Ikke prøv dette i et produksjonsmiljø med mindre du er 100% sikker på at versjonen er fullstendig utdatert.</span><span class="sxs-lookup"><span data-stu-id="79a58-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="79a58-113">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="79a58-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="79a58-114">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="79a58-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="79a58-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="79a58-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="79a58-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="79a58-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="79a58-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="79a58-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="79a58-118">Klikk Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="79a58-118">Click Deactivate.</span></span>
    * <span data-ttu-id="79a58-119">Ikke fortsett hvis du ikke er 100 % sikker på at denne produksjonsflytversjonen er foreldet.</span><span class="sxs-lookup"><span data-stu-id="79a58-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="79a58-120">Når du klikker OK, utløper alle aktive Kanban-regler og alle produksjons- og etterfyllingsaktiviteter for denne produksjonsflytversjonen opphører umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="79a58-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="79a58-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="79a58-121">Click OK.</span></span>

