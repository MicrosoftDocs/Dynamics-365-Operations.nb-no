---
title: Feilsøke utgående lageroperasjoner
description: Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med utgående lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 1344a1c16bf72b31f7aaf18aaeb6e08c7bc9d87e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223272"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="70155-103">Feilsøke utgående lageroperasjoner</span><span class="sxs-lookup"><span data-stu-id="70155-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70155-104">Dette emnet beskriver hvordan du løser vanlige problemer som kan oppstå mens du arbeider med utgående lageroperasjoner i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="70155-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="70155-105">Jeg får følgende feilmelding: Salgsordre kan ikke frigis.</span><span class="sxs-lookup"><span data-stu-id="70155-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="70155-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="70155-106">Issue description</span></span>

<span data-ttu-id="70155-107">Dette problemet kan oppstå av flere årsaker.</span><span class="sxs-lookup"><span data-stu-id="70155-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="70155-108">Ordren er for eksempel på vent for kredittbehandling, og ingen forsendelser kan opprettes før en gyldig postadresse angis for alle salgslinjer som er tilknyttet en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="70155-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="70155-109">Det finnes også en ordresperre som må løses før ordren kan frigis til lageret.</span><span class="sxs-lookup"><span data-stu-id="70155-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="70155-110">Denne sperringen kan være ordrespesifikk, eller den kan være på kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="70155-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="70155-111">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="70155-111">Issue resolution</span></span>

<span data-ttu-id="70155-112">Legg til eller oppdater adressen på salgsordren og ordrelinjene, og frigi deretter ordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="70155-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="70155-113">Ordrer kan bare frigis til lageret hvis de har en gyldig leveringsadresse (per adresseformatoppsettet i modulen **Organisasjonsstyring**).</span><span class="sxs-lookup"><span data-stu-id="70155-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="70155-114">Undersøk ordresperringen og løs problemene.</span><span class="sxs-lookup"><span data-stu-id="70155-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="70155-115">Fjern deretter sperringen fra ordren eller kunden, og frigi ordren til lageret.</span><span class="sxs-lookup"><span data-stu-id="70155-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="70155-116">Jeg får følgendemelding: Forsendelsen for lasten 1% er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="70155-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="70155-117">Ingen linjer er imidlertid postert.</span><span class="sxs-lookup"><span data-stu-id="70155-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="70155-118">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="70155-118">Issue description</span></span>

<span data-ttu-id="70155-119">En forsendelse på en last ble bekreftet, men det har ikke vært flere posteringer.</span><span class="sxs-lookup"><span data-stu-id="70155-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="70155-120">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="70155-120">Issue resolution</span></span>

<span data-ttu-id="70155-121">Forsendelsesbekreftelsen påvirker ikke postering.</span><span class="sxs-lookup"><span data-stu-id="70155-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="70155-122">Den oppdaterer bare forsendelses- og laststatusen.</span><span class="sxs-lookup"><span data-stu-id="70155-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="70155-123">Posteringen må forekomme i en egen prosess.</span><span class="sxs-lookup"><span data-stu-id="70155-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="70155-124">Jeg får følgende feilmelding: Direkte levering kan ikke behandle for lager 1% fordi lagerstyring er aktivert.</span><span class="sxs-lookup"><span data-stu-id="70155-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="70155-125">Angi et annet lager som ikke er aktivert for lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="70155-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="70155-126">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="70155-126">Issue description</span></span>

<span data-ttu-id="70155-127">En vare legges til en salgslinje for direkte levering fra et lager som er aktivert for lagerstyring (WMS).</span><span class="sxs-lookup"><span data-stu-id="70155-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="70155-128">Du får denne feilmeldingen når salgslinjen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="70155-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="70155-129">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="70155-129">Issue resolution</span></span>

<span data-ttu-id="70155-130">Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.</span><span class="sxs-lookup"><span data-stu-id="70155-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="70155-131">For øyeblikket støtter ikke WMS direkte levering.</span><span class="sxs-lookup"><span data-stu-id="70155-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="70155-132">Hvis du vil bruke direkte levering, må du derfor velge en vare og et lager som ikke er WMS.</span><span class="sxs-lookup"><span data-stu-id="70155-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]