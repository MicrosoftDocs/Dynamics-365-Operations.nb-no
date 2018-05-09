---
title: Ordresperrer
description: "Dette emnet beskriver sperringer på ordrer ved hjelp av Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 106ce40f93704e67e53db2e62ae481d271aed755
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="order-holds"></a><span data-ttu-id="3aec2-103">Ordresperrer</span><span class="sxs-lookup"><span data-stu-id="3aec2-103">Order holds</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3aec2-104">Dette emnet beskriver sperringer på ordrer ved hjelp av Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3aec2-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="3aec2-105">En ordre kan sperres av ulike årsaker.</span><span class="sxs-lookup"><span data-stu-id="3aec2-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="3aec2-106">Du kan for eksempel sette en ordre på vent til kundens adresse eller betalingsmetode kan bekreftes, eller til en leder kan gå gjennom kundens kredittgrense.</span><span class="sxs-lookup"><span data-stu-id="3aec2-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="3aec2-107">I løpet av salgsprosessen hender det at salgsordrer må settes på vent.</span><span class="sxs-lookup"><span data-stu-id="3aec2-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="3aec2-108">En salgsordre kan for eksempel settes på vent på grunn av problemer med en kundebetaling, mistanke om svindel, eller for å vente på gjennomgang ved en leder.</span><span class="sxs-lookup"><span data-stu-id="3aec2-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="3aec2-109">Når en salgsordre settes på vent, tilordnes en ordresperrekode til salgsordren for å angi årsaken til sperringen.</span><span class="sxs-lookup"><span data-stu-id="3aec2-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="3aec2-110">Sperrekoder for salgsordre konfigureres på **Salg og markedsføring** &gt; **Oppsett** &gt; **Salgsordrer** &gt; **Koder for ordresperringer**.</span><span class="sxs-lookup"><span data-stu-id="3aec2-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="3aec2-111">En salgsordre kan sperres manuelt på tidspunktet for oppretting eller senere.</span><span class="sxs-lookup"><span data-stu-id="3aec2-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="3aec2-112">I tillegg kan kan en ordre sperres automatisk, basert på regler for svindel.</span><span class="sxs-lookup"><span data-stu-id="3aec2-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="3aec2-113">Når en ordre er på vent, må du kanskje oppdatere den med mer informasjon.</span><span class="sxs-lookup"><span data-stu-id="3aec2-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="3aec2-114">Det kan også hende at du vil sjekke ut den salgsordren når du fortsetter å arbeide med den.</span><span class="sxs-lookup"><span data-stu-id="3aec2-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="3aec2-115">Du kan sjekke ut en salgsordre, sjekke den inn igjen, og også overstyre utsjekkingen av en annen bruker ved å bruke arbeidsområde for ordresperre (**Detaljhandel** &gt; **Kunder** &gt; **Ordresperrer**).</span><span class="sxs-lookup"><span data-stu-id="3aec2-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="3aec2-116">Når en ordre er klar til å fullføres, må du fjerne sperringen før du kan fullføre ordreprosessen.</span><span class="sxs-lookup"><span data-stu-id="3aec2-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




