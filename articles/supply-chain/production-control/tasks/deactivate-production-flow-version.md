---
title: Deaktivere en produksjonsflytversjon
description: Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e47cb950ce488d8b6170f829e1fedc664b921a1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811564"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="242d9-103">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="242d9-103">Deactivate a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="242d9-104">Når en aktiv produksjonsflytversjon ikke lenger er nødvendig, kan den deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="242d9-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="242d9-105">Du bør bare bruke dette alternativet hvis alle Kanban-regler og aktiviteter er avsluttet og ikke skal aktiveres igjen.</span><span class="sxs-lookup"><span data-stu-id="242d9-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="242d9-106">Vær oppmerksom på at utløpsdatoen for alle Kanban-regler som er knyttet til denne produksjonsflytversjonen, vil bli oppdatert med gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="242d9-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="242d9-107">Hvis du vil endre en aktiv produksjonsflytversjon, bør du vurdere å angi en utløpsdato for den aktive versjonen og opprette en ny versjon.</span><span class="sxs-lookup"><span data-stu-id="242d9-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="242d9-108">Dette gjør at du kan fortsette produksjonsoperasjonene mens den nye versjonen og relaterte Kanban-regler klargjøres.</span><span class="sxs-lookup"><span data-stu-id="242d9-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="242d9-109">Du må angi en utløpsdato for å utløpe en aktiv produksjonsflytversjon.</span><span class="sxs-lookup"><span data-stu-id="242d9-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="242d9-110">I den forstand er deaktivering mer et unntak enn en regel.</span><span class="sxs-lookup"><span data-stu-id="242d9-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="242d9-111">Til denne prosedyren trenger du en produksjonsflyt med en versjon som kan deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="242d9-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="242d9-112">Ikke prøv dette i et produksjonsmiljø med mindre du er 100% sikker på at versjonen er fullstendig utdatert.</span><span class="sxs-lookup"><span data-stu-id="242d9-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="242d9-113">Deaktivere en produksjonsflytversjon</span><span class="sxs-lookup"><span data-stu-id="242d9-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="242d9-114">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="242d9-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="242d9-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="242d9-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="242d9-116">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="242d9-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="242d9-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="242d9-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="242d9-118">Klikk på Deaktiver.</span><span class="sxs-lookup"><span data-stu-id="242d9-118">Click Deactivate.</span></span>
    * <span data-ttu-id="242d9-119">Ikke fortsett hvis du ikke er 100 % sikker på at denne produksjonsflytversjonen er foreldet.</span><span class="sxs-lookup"><span data-stu-id="242d9-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="242d9-120">Når du klikker OK, utløper alle aktive Kanban-regler og alle produksjons- og etterfyllingsaktiviteter for denne produksjonsflytversjonen opphører umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="242d9-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="242d9-121">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="242d9-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]