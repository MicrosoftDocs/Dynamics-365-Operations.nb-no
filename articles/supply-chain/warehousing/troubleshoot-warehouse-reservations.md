---
title: Feilsøke reserveringer i lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248721"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="03935-103">Feilsøke reserveringer i lagerstyring</span><span class="sxs-lookup"><span data-stu-id="03935-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03935-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="03935-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="03935-105">Jeg får følgende feilmelding: Reservasjoner kan ikke fjernes fordi det er opprettet arbeid som er avhengig av reservasjonen.</span><span class="sxs-lookup"><span data-stu-id="03935-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03935-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="03935-106">Issue description</span></span>

<span data-ttu-id="03935-107">Du kan ikke reservere lager på en salgslinje, fordi det er åpent arbeid mot linjen.</span><span class="sxs-lookup"><span data-stu-id="03935-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03935-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="03935-108">Issue resolution</span></span>

<span data-ttu-id="03935-109">Undersøk om det finnes åpent emballasjegruppearbeid for å hente varen fra en pakkestasjon til en annen lokasjon (f.eks. *Rampedør*).</span><span class="sxs-lookup"><span data-stu-id="03935-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="03935-110">Se gjennom postene på sidene **Logg over oppretting av arbeid** og **Arbeidsdetaljer** for å fastslå hva som fysisk reserverer lageret, og fullfør eller slett arbeidet for å frigjøre reservasjonen.</span><span class="sxs-lookup"><span data-stu-id="03935-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="03935-111">Jeg får følgende feilmelding: Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for vare %2 ....</span><span class="sxs-lookup"><span data-stu-id="03935-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03935-112">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="03935-112">Issue description</span></span>

<span data-ttu-id="03935-113">Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="03935-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="03935-114">Her er hele teksten til hele feilmeldingen:</span><span class="sxs-lookup"><span data-stu-id="03935-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="03935-115">Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for varen %2 med dimensjonsstørrelse = %3, farge = %4, tillegg = %5, område = %6, lager = %7, lokasjon = %8, lagerstatus = tilgjengelig, nummerskilt = %9, partinummer = %10 for referanse-ID %11 på parti-ID %12.</span><span class="sxs-lookup"><span data-stu-id="03935-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03935-116">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="03935-116">Issue resolution</span></span>

<span data-ttu-id="03935-117">Kontroller at ingen lagertransaksjoner fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="03935-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="03935-118">Disse transaksjonene kan for eksempel åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="03935-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="03935-119">Jeg får følgende feilmelding: Fysisk lagerbeholdning ... kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.</span><span class="sxs-lookup"><span data-stu-id="03935-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03935-120">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="03935-120">Issue description</span></span>

<span data-ttu-id="03935-121">Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="03935-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="03935-122">Her er hele teksten til hele feilmeldingen:</span><span class="sxs-lookup"><span data-stu-id="03935-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="03935-123">Fysisk lagerbeholdning område = %1, lager = %2, lagerstatus = tilgjengelig, partinummer = %3, eier = %4: %5 kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.</span><span class="sxs-lookup"><span data-stu-id="03935-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03935-124">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="03935-124">Issue resolution</span></span>

<span data-ttu-id="03935-125">Dette problemet skyldes sannsynligvis åpent arbeid.</span><span class="sxs-lookup"><span data-stu-id="03935-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="03935-126">Du må enten fullføre arbeidet eller motta uten arbeidsoppretting.</span><span class="sxs-lookup"><span data-stu-id="03935-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="03935-127">Kontroller at ingen lagertransaksjoner fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="03935-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="03935-128">Disse transaksjonene kan for eksempel være åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="03935-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="03935-129">Jeg får følgende feilmelding: For å tilordne bølge må lastlinjer angi dimensjonene over lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="03935-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="03935-130">Hvis du vil tilordne disse dimensjonene, må du reservere og opprette lastlinjen på nytt.</span><span class="sxs-lookup"><span data-stu-id="03935-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="03935-131">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="03935-131">Issue description</span></span>

<span data-ttu-id="03935-132">Når du bruker en vare som har et parti over-reservasjonshierarki (med **Partinummer**-dimensjonen som er plassert *over* **Lokasjon**-dimensjonen), fungerer ikke kommandoen **Frigi til lager** på siden **Arbeidsområde for lastplanlegging** for et delvis antall.</span><span class="sxs-lookup"><span data-stu-id="03935-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="03935-133">Du får denne feilmeldingen, og det opprettes ikke noe arbeid for det delvise antallet.</span><span class="sxs-lookup"><span data-stu-id="03935-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="03935-134">Hvis du imidlertid bruker en vare som har et parti under-reservasjonshierarki (med **Partinummer**-dimensjonen som er plassert *under* **Lokasjon**-dimensjonen), kan du frigi en last fra siden **Arbeidsområde for lastplanlegging** for et delvis antall.</span><span class="sxs-lookup"><span data-stu-id="03935-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="03935-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="03935-135">Issue resolution</span></span>

<span data-ttu-id="03935-136">Denne virkemåten er standard.</span><span class="sxs-lookup"><span data-stu-id="03935-136">This behavior is by design.</span></span> <span data-ttu-id="03935-137">Hvis du legger en dimensjon til over **Lokasjon**-dimensjonen i reservasjonshierarkiet, må den angis før frigivelse til lageret.</span><span class="sxs-lookup"><span data-stu-id="03935-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="03935-138">Microsoft har evaluert dette problemet, og har funnet ut at det er en funksjonsbegrensning under frigivelser til lageret fra arbeidsområdet for lastplanlegging.</span><span class="sxs-lookup"><span data-stu-id="03935-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="03935-139">Delvise antall kan ikke frigis hvis én eller flere dimensjoner over **Lokasjon** ikke er angitt.</span><span class="sxs-lookup"><span data-stu-id="03935-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="03935-140">Hvis du vil ha mer informasjon, kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="03935-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]