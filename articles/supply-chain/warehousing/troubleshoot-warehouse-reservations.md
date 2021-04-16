---
title: Feilsøke reserveringer i lagerstyring
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
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
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828112"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="69199-103">Feilsøke reserveringer i lagerstyring</span><span class="sxs-lookup"><span data-stu-id="69199-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69199-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med lagerreservasjoner i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="69199-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="69199-105">For emner som er relatert til parti- og serienummerregistreringer, kan du se [Feilsøke lagerparti- og seriereserveringshierarkier](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="69199-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="69199-106">Jeg får følgende feilmelding: Reservasjoner kan ikke fjernes fordi det er opprettet arbeid som er avhengig av reservasjonen.</span><span class="sxs-lookup"><span data-stu-id="69199-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="69199-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="69199-107">Issue description</span></span>

<span data-ttu-id="69199-108">Du kan ikke reservere lager på en salgslinje, fordi det er åpent arbeid mot linjen.</span><span class="sxs-lookup"><span data-stu-id="69199-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="69199-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="69199-109">Issue resolution</span></span>

<span data-ttu-id="69199-110">Undersøk om det finnes åpent emballasjegruppearbeid for å hente varen fra en pakkestasjon til en annen lokasjon (f.eks. *Rampedør*).</span><span class="sxs-lookup"><span data-stu-id="69199-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="69199-111">Se gjennom postene på sidene **Logg over oppretting av arbeid** og **Arbeidsdetaljer** for å fastslå hva som fysisk reserverer lageret, og fullfør eller slett arbeidet for å frigjøre reservasjonen.</span><span class="sxs-lookup"><span data-stu-id="69199-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="69199-112">Jeg får følgende feilmelding: Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for vare %2 ....</span><span class="sxs-lookup"><span data-stu-id="69199-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="69199-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="69199-113">Issue description</span></span>

<span data-ttu-id="69199-114">Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="69199-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="69199-115">Her er hele teksten til hele feilmeldingen:</span><span class="sxs-lookup"><span data-stu-id="69199-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="69199-116">Lagerantall -%1 kan ikke oppdateres på grunn av utilstrekkelige lagertransaksjoner for varen %2 med dimensjonsstørrelse = %3, farge = %4, tillegg = %5, område = %6, lager = %7, lokasjon = %8, lagerstatus = tilgjengelig, nummerskilt = %9, partinummer = %10 for referanse-ID %11 på parti-ID %12.</span><span class="sxs-lookup"><span data-stu-id="69199-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="69199-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="69199-117">Issue resolution</span></span>

<span data-ttu-id="69199-118">Kontroller at ingen lagertransaksjoner fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="69199-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="69199-119">Disse transaksjonene kan for eksempel åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="69199-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="69199-120">Jeg får følgende feilmelding: Fysisk lagerbeholdning ... kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.</span><span class="sxs-lookup"><span data-stu-id="69199-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="69199-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="69199-121">Issue description</span></span>

<span data-ttu-id="69199-122">Dette problemet kan oppstå hvis systemet ikke kan oppdatere et lagerantall, fordi det ikke finnes nok lagertransaksjoner som har de angitte dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="69199-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="69199-123">Her er hele teksten til hele feilmeldingen:</span><span class="sxs-lookup"><span data-stu-id="69199-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="69199-124">Fysisk lagerbeholdning område = %1, lager = %2, lagerstatus = tilgjengelig, partinummer = %3, eier = %4: %5 kan ikke reserveres fordi bare 0,00 er tilgjengelig på lageret.</span><span class="sxs-lookup"><span data-stu-id="69199-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="69199-125">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="69199-125">Issue resolution</span></span>

<span data-ttu-id="69199-126">Dette problemet skyldes sannsynligvis åpent arbeid.</span><span class="sxs-lookup"><span data-stu-id="69199-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="69199-127">Du må enten fullføre arbeidet eller motta uten arbeidsoppretting.</span><span class="sxs-lookup"><span data-stu-id="69199-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="69199-128">Kontroller at ingen lagertransaksjoner fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="69199-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="69199-129">Disse transaksjonene kan for eksempel være åpne kvalitetsordrer, lagerblokkeringsposter eller ordrer.</span><span class="sxs-lookup"><span data-stu-id="69199-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
