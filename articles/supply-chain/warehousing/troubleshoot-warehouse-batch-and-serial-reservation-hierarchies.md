---
title: Feilsøke lagerparti- og seriereserveringshierarkier
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med reservasjonshierarkier som bruker parti- eller seriedimensjoner.
author: perlynne
ms.date: 3/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 3/12/2021
ms.openlocfilehash: 1cd4883cdd95a97f821e0103da910e2c0346a08d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022552"
---
# <a name="troubleshoot-warehouse-batch-and-serial-reservation-hierarchies"></a><span data-ttu-id="f1cc2-103">Feilsøke lagerparti- og seriereserveringshierarkier</span><span class="sxs-lookup"><span data-stu-id="f1cc2-103">Troubleshoot warehouse batch and serial reservation hierarchies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1cc2-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med reservasjonshierarkier som bruker parti- eller seriedimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-104">This topic describes how to fix common issues that you might encounter while you work with reservation hierarchies that use batch or serial dimensions.</span></span>

<span data-ttu-id="f1cc2-105">Hvis du vil ha mer informasjon, kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="f1cc2-105">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>

<span data-ttu-id="f1cc2-106">Reservasjonshierarkiet til en vare angir behovet for lagringsdimensjoner som må oppfylles, for å tilordne en lokasjon til en behovsordre.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-106">The reservation hierarchy of an item dictates the requirement of storage dimensions that must be fulfilled to assign a location to a demand order.</span></span> <span data-ttu-id="f1cc2-107">Disse dimensjonene kan beskrives som *dimensjoner over lokasjonen* for alle dimensjonene som må oppfylles før en lokasjon tilordnes, og *dimensjoner under lokasjonen* for dimensjoner som kan tilordnes etter at en lokasjon er tilordnet behovsordren.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-107">These dimensions can be described as *dimensions above location*, for all the dimensions that must be fulfilled before a location is assigned, and *dimensions below location*, for dimensions that can be allocated after a location has been assigned to the demand order.</span></span> <span data-ttu-id="f1cc2-108">Disse reservasjonshierarkiene kalles også *parti-over* og *parti-under* eller *serie-over* og *serie-under*.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-108">These reservation hierarchies are also known as *batch-above* and *batch-below* reservation hierarchies, or *serial-above* and *serial-below* reservation hierarchies.</span></span>

<span data-ttu-id="f1cc2-109">Beholdningen kan bare tilordnes hvis det ikke er noen huller i dimensjonene over lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-109">Inventory can be successfully allocated only if there are no gaps in the dimensions above location.</span></span> <span data-ttu-id="f1cc2-110">I et reservasjonshierarki av typen *parti-over* forventer du for eksempel at dimensjonene **Sted**, **Lager** og **Partinummer** er angitt i behovsordren.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-110">For example, in a *batch-above* reservation hierarchy, you expect **Site,** **Warehouse,** and **Batch number** dimensions to be specified on the demand order.</span></span> <span data-ttu-id="f1cc2-111">Hvis noen av disse dimensjonene mangler, mislykkes tildelingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-111">If any of these dimensions are missing, the allocation process will fail.</span></span> <span data-ttu-id="f1cc2-112">I kontrast til dette kan reservasjonshierarki av typen *parti-under* eller *serie-under* ha et parti- eller serienummer angitt i behovsordren, men tildelingsprosessen krever ikke dette.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-112">By contrast, in a *batch-below* or *serial-below* reservation hierarchy, a batch or serial number might be specified on the demand order, but the allocation process doesn't require it.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="f1cc2-113">Jeg får følgende feilmelding: For å tilordne bølge må lastlinjer angi dimensjonene over lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-113">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="f1cc2-114">Hvis du vil tilordne disse dimensjonene, må du reservere og opprette lastlinjen på nytt.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-114">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1cc2-115">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f1cc2-115">Issue description</span></span>

<span data-ttu-id="f1cc2-116">Når du bruker en vare som har et *parti-over*-reservasjonshierarki, fungerer ikke kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging** hvis du prøver å frigi en last for en delvis mengde.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-116">When you use an item that has a *batch-above* reservation hierarchy, the **Release to warehouse** command on the **Load planning workbench** page doesn't work if you try to release a load for a partial quantity.</span></span> <span data-ttu-id="f1cc2-117">Du får denne feilmeldingen, og det opprettes ikke noe arbeid for det delvise antallet.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-117">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="f1cc2-118">Når du imidlertid bruker en vare som har et *parti-under*-reservasjonshierarki, kan du frigi en last for en delvis mengde fra siden **Arbeidsområde for lastplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-118">However, when you use an item that has a *batch-below* reservation hierarchy, you can release a load for a partial quantity from the **Load planning workbench** page.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="f1cc2-119">Feilårsak</span><span class="sxs-lookup"><span data-stu-id="f1cc2-119">Issue cause</span></span>

<span data-ttu-id="f1cc2-120">Når en dimensjon er over **Lokasjon**-dimensjonen i reservasjonshierarkiet, må den angis før frigivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-120">When a dimension is above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="f1cc2-121">Delvise antall kan ikke frigis hvis én eller flere dimensjoner over **Lokasjon** ikke er angitt.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-121">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

## <a name="the-auto-reservation-prompt-for-a-batch-number-is-triggered-even-though-there-is-available-inventory"></a><span data-ttu-id="f1cc2-122">Ledeteksten for automatisk reservering av et partinummer utløses selv om det er tilgjengelig lager.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-122">The auto-reservation prompt for a batch number is triggered even though there is available inventory.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1cc2-123">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f1cc2-123">Issue description</span></span>

<span data-ttu-id="f1cc2-124">Når du bruker en vare som har et *parti-over*-reservasjonshierarki i et lager som ikke har aktivert lagerprosesser, og automatisk reservering er aktivert, vises ledeteksten for automatisk reservering for et partinummer, selv om bare ett parti er tilgjengelig for plukking.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-124">When you use an item that has a *batch-above* reservation hierarchy in a warehouse that hasn't enabled warehouse processes, and automatic reservation is enabled, the auto-reservation prompt for a batch number is shown even if only one batch is available for picking.</span></span>

<span data-ttu-id="f1cc2-125">Når du imidlertid bruker den samme varen i et lager der lagerprosessene er aktivert, vises ikke ledeteksten for automatisk reservering.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-125">However, when you use the same item in a warehouse where warehouse processes are enabled, the auto-reservation prompt isn't shown.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="f1cc2-126">Feilårsak</span><span class="sxs-lookup"><span data-stu-id="f1cc2-126">Issue cause</span></span>

<span data-ttu-id="f1cc2-127">Hvis et reserveringshierarki er definert som *parti-over* eller *serie-over*, må den refererte dimensjonen (**Partinummer** eller **Serienummer**) alltid være angitt i behovsordrer.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-127">If a reservation hierarchy is defined as *batch-above* or *serial-above*, the referenced dimension (**Batch number** or **Serial number**) must always be specified on demand orders.</span></span> <span data-ttu-id="f1cc2-128">Lagerprosesser kan kanskje fylle ut informasjonen hvis ett enkelt parti- eller serienummer er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-128">Warehouse processes might be able to complete the information if a single batch or serial number is available.</span></span> <span data-ttu-id="f1cc2-129">Siden lageret ikke er aktivert for lagerprosesser, må imidlertid brukeren alltid angi alle dimensjonene over **Lokasjon**.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-129">However, because the warehouse isn't enabled for warehouse processes, the user must always specify all the dimensions above **Location**.</span></span>

## <a name="slotting-templates-that-have-the-consider-on-hand-slot-criterion-dont-consider-current-on-hand-inventory-for-batch-enabled-items"></a><span data-ttu-id="f1cc2-130">Sporingsmaler som har kriteriet Vurder sporbeholdning, tar ikke hensyn til gjeldende lagerbeholdning for partiaktiverte varer.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-130">Slotting templates that have the Consider on-hand slot criterion don't consider current on-hand inventory for batch-enabled items.</span></span>

<span data-ttu-id="f1cc2-131">Hvis du vil ha mer informasjon, kan du se [Lagersporing](warehouse-slotting.md).</span><span class="sxs-lookup"><span data-stu-id="f1cc2-131">For more information, see [Warehouse slotting](warehouse-slotting.md).</span></span>

### <a name="issue-description"></a><span data-ttu-id="f1cc2-132">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="f1cc2-132">Issue description</span></span>

<span data-ttu-id="f1cc2-133">Sporingsmaler som har kriteriet *Vurder sporbeholdning*, tar ikke hensyn til gjeldende lagerbeholdning for *parti-over*-varer.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-133">Slotting templates that have the *Consider on-hand* slot criterion don't consider current on-hand inventory for *batch-above* items.</span></span> <span data-ttu-id="f1cc2-134">De vurderer det bare hvis partinummeret er angitt på salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-134">They consider it only if the batch number is specified on the sales order line.</span></span>

<span data-ttu-id="f1cc2-135">Når du bruker *parti-under*-varer, vurderes imidlertid den gjeldende lagerbeholdningen som forventet.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-135">However, when you use *batch-below* items, the current on-hand inventory is considered as expected.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="f1cc2-136">Feilårsak</span><span class="sxs-lookup"><span data-stu-id="f1cc2-136">Issue cause</span></span>

<span data-ttu-id="f1cc2-137">Sporingsmalhodet kan defineres for behovsstrategien *Bestilt*, *Reservert* eller *Frigitt*.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-137">The slotting template header can be defined for the *Ordered,* *Reserved*, or *Released* demand strategy.</span></span> <span data-ttu-id="f1cc2-138">Når det gjelder strategien for *bestilt* etterspørsel, gjelder de samme reservasjonshierarkikravene som gjelder for reservering eller frigivelse for lagerprosesser.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-138">For the *Ordered* demand strategy, the same reservation hierarchy requirements apply that apply to reservation or release to warehouse processes.</span></span> <span data-ttu-id="f1cc2-139">For varer som har *parti-over*- og *serie-under*-reservasjonshierarkier, må derfor parti- eller serienummeret angis på behovsordren (salg eller overføring).</span><span class="sxs-lookup"><span data-stu-id="f1cc2-139">Therefore, for items that have *batch-above* and *serial-below* reservation hierarchies, the batch or serial number must be specified on the demand order (sales or transfer).</span></span> <span data-ttu-id="f1cc2-140">Du kan også bruke strategien for *reservert* etterspørsel til å velge parti- eller serienummeret før lagerets sporbehov genereres.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-140">Alternatively, the *Reserved* demand strategy can be used to select the batch or serial number before the warehouse slotting demand is generated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
