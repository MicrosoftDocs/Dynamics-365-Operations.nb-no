---
title: Etterdaterte sjekker
description: Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker i Microsoft Dynamics 365 for Finance and Operations. Etterdaterte sjekker er sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato. Derfor kan ikke veksles sjekken før den angitte datoen.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb879103c86cd251efcb1d3efa1faf847cb5ca74
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842311"
---
# <a name="postdated-checks"></a><span data-ttu-id="9f136-105">Etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="9f136-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f136-106">Denne artikkelen inneholder informasjon om støtte for etterdaterte sjekker i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9f136-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="9f136-107">Etterdaterte sjekker er sjekker som er utstedt for å foreta og motta betalinger på en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="9f136-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="9f136-108">Derfor kan ikke veksles sjekken før den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="9f136-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="9f136-109">Microsoft Dynamics 365 for Finance and Operations støtter hele forvaltningssyklusen for etterdaterte sjekker i både Kunder og Leverandører, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="9f136-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f136-110">Scenario</span><span class="sxs-lookup"><span data-stu-id="9f136-110">Scenario</span></span></th>
<th><span data-ttu-id="9f136-111">Detaljer</span><span class="sxs-lookup"><span data-stu-id="9f136-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f136-112">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="9f136-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="9f136-113">Du må definere en ny betalingsmåte og angi betalingsrutiner for å slette kontoer for utstedte sjekker, mottatte sjekker og kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="9f136-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f136-114">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="9f136-115">Registrere detaljer om en etterdaterte sjekk du utsteder til en leverandør.</span><span class="sxs-lookup"><span data-stu-id="9f136-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="9f136-116">Når betalingen er postert, er leverandøren gjenkjent, men bankkontoen ennå ikke kredit.</span><span class="sxs-lookup"><span data-stu-id="9f136-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="9f136-117">I stedet brukes en avregningskonto for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="9f136-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f136-118">Registrere og postere en etterdatert sjekk for en kunde</span><span class="sxs-lookup"><span data-stu-id="9f136-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="9f136-119">Registrer informasjonen i en etterdatert sjekk som du mottar fra en kunde.</span><span class="sxs-lookup"><span data-stu-id="9f136-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="9f136-120">Når betalingen er postert, er kunden kredit, men bankkontoen ikke ennå debet.</span><span class="sxs-lookup"><span data-stu-id="9f136-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="9f136-121">I stedet brukes en avregningskonto for dette formålet.</span><span class="sxs-lookup"><span data-stu-id="9f136-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f136-122">Registrere og postere en erstatning for etterdatert sjekk for en kunde eller leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="9f136-123">Hvis den opprinnelige sjekken til en leverandør eller kunde blir mistet eller skadet, kan du utstede en erstatning for den etterdaterte sjekken.</span><span class="sxs-lookup"><span data-stu-id="9f136-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="9f136-124">Når du registrerer sjekkdetaljene, må du oppgi en referanse til den opprinnelige sjekken og angi at den nye sjekken er en erstatning for den opprinnelige.</span><span class="sxs-lookup"><span data-stu-id="9f136-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="9f136-125">Du kan også postere erstatningssjekken.</span><span class="sxs-lookup"><span data-stu-id="9f136-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f136-126">Overføre en etterdatert kundesjekk til en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="9f136-127">Når du får en etterdatert sjekk fra en kunde, kan du overføre denne sjekken til en leverandør som betaling.</span><span class="sxs-lookup"><span data-stu-id="9f136-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f136-128">Utligne en etterdatert sjekk for en kunde eller en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="9f136-129">Utligne en etterdatert sjekk som er postert til en mellomkonto for en kunde eller leverandør når sjekken forfaller.</span><span class="sxs-lookup"><span data-stu-id="9f136-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="9f136-130">Når sjekken er utlignet, er banken til slutt debet eller kredit mot avregningskontoen som ble brukt tidligere.</span><span class="sxs-lookup"><span data-stu-id="9f136-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f136-131">Avbryte en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="9f136-132">Du kan avbryte en postert etterdatert sjekk i disse situasjonene: - Sjekken returneres av banken.</span><span class="sxs-lookup"><span data-stu-id="9f136-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="9f136-133">- Sjekken brukes på feil faktura.</span><span class="sxs-lookup"><span data-stu-id="9f136-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="9f136-134">- Det er gjort en kontantbetaling mot sjekken.</span><span class="sxs-lookup"><span data-stu-id="9f136-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="9f136-135">Stoppe betaling av en etterdatert sjekk</span><span class="sxs-lookup"><span data-stu-id="9f136-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="9f136-136">Du kan stoppe betaling av en etterdatert sjekk som ble utstedt til en leverandør, på grunn av for eksempel utilstrekkelige midler, endring av vilkårene i avtalen med leverandøren, mottak av defekte varer fra leverandøren, eller retur av varer til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="9f136-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="9f136-137">Du kan bare stoppe betaling av sjekker som ikke er avregnet.</span><span class="sxs-lookup"><span data-stu-id="9f136-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="9f136-138">Hvis du vil ha mer informasjon, se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="9f136-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="9f136-139">Definere etterdaterte sjekker</span><span class="sxs-lookup"><span data-stu-id="9f136-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="9f136-140">Registrere og postere en etterdatert sjekk for en kunde</span><span class="sxs-lookup"><span data-stu-id="9f136-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="9f136-141">Utligne en etterdatert sjekk fra en kunde</span><span class="sxs-lookup"><span data-stu-id="9f136-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="9f136-142">Registrere og postere en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="9f136-143">Utligne en etterdatert sjekk for en leverandør</span><span class="sxs-lookup"><span data-stu-id="9f136-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)



