---
title: Opprette en leverandørbankkonto
description: Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør.
author: mkirknel
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8dd3664d86ffdb8bf731a6ff1e0ed60b50eed61
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916835"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="f3bf6-103">Opprette en leverandørbankkonto</span><span class="sxs-lookup"><span data-stu-id="f3bf6-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3bf6-104">Denne fremgangsmåten viser hvordan du oppretter en bankkonto for en leverandør.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="f3bf6-105">Du kan bruke prosedyren i demonstrasjonsdataselskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="f3bf6-106">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-106">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="f3bf6-107">Velg leverandøren du vil opprette en bankkonto for, og klikk deretter koblingen i feltet **Leverandørens konto-ID**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-107">Select the vendor that you want to create a bank account for, and then click the link on the **Vendor account ID** field.</span></span>
3. <span data-ttu-id="f3bf6-108">Klikk **Leverandør** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-108">On the **Action pane**, click **Vendor**.</span></span>
4. <span data-ttu-id="f3bf6-109">Klikk **Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-109">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="f3bf6-110">Klikk **Ny** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-110">On the **Action pane**, click **New**.</span></span>
6. <span data-ttu-id="f3bf6-111">Skriv inn en verdi i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-111">In the **Bank account** field, type a value.</span></span> <span data-ttu-id="f3bf6-112">Denne ID-en brukes for å identifisere bankkontoen på leverandørposten.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="f3bf6-113">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="f3bf6-114">Angi eller velg en verdi i **Bankgrupper**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-114">In the **Bank groups** field, enter or select a value.</span></span>
9. <span data-ttu-id="f3bf6-115">Velg et alternativ i feltet **Registreringsnummertype**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-115">In the **Routing number type** field, select an option.</span></span> <span data-ttu-id="f3bf6-116">Dette er registreringsnummertypen som brukes for internasjonale betalinger.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="f3bf6-117">Skriv inn en verdi i feltet **Bankkontonummer**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-117">In the **Bank account number** field, type a value.</span></span>
11. <span data-ttu-id="f3bf6-118">Skriv inn en verdi i **SWIFT-kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-118">In the **SWIFT code** field, type a value.</span></span>
12. <span data-ttu-id="f3bf6-119">Skriv inn en verdi i **IBAN**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-119">In the **IBAN** field, type a value.</span></span>
    - <span data-ttu-id="f3bf6-120">IBAN-nummeret må være i riktig format.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="f3bf6-121">Du kan for eksempel bruke DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-121">For example, you could use DE89370400440532013000.</span></span>  
    - <span data-ttu-id="f3bf6-122">Statusen for bankkontoen er Aktiv hvis aktiveringsdatoen er nådd og utløpsdatoen ikke er overskredet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="f3bf6-123">Den er også aktivt hvis både aktiveringsdato og utløpsdato er tomme.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="f3bf6-124">Hvis datoene i både Aktiveringsdato- og Utløpsdato-feltene i er fremtiden, er ikke elektroniske betalinger tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="f3bf6-125">Andre betalingstyper er tilgjengelige, og bankkontoen er aktiv.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="f3bf6-126">Utvid **Oppsett**-delen.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-126">Expand the **Setup** section.</span></span>
14. <span data-ttu-id="f3bf6-127">Skriv inn en verdi i **Tekstkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-127">In the **Text code** field, type a value.</span></span> <span data-ttu-id="f3bf6-128">Dette feltet angir en kode som vises på bankkontoutdraget til mottakeren.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="f3bf6-129">Skriv inn en verdi i **Melding til bank**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-129">In the **Message to bank** field, type a value.</span></span>
16. <span data-ttu-id="f3bf6-130">Skriv inn en verdi i **Kursreferanse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-130">In the **Exchange reference** field, type a value.</span></span> <span data-ttu-id="f3bf6-131">Dette er referansenummeret for en eventuell fremtids- eller avtalekurs.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>
17. <span data-ttu-id="f3bf6-132">Angi eller velg en verdi i **Valuta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-132">In the **Currency** field, enter or select a value.</span></span> <span data-ttu-id="f3bf6-133">Når forhåndsmerknader utstedes, vil denne delen gir en oversikt over statusen (venter eller godkjent).</span><span class="sxs-lookup"><span data-stu-id="f3bf6-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="f3bf6-134">Vis delen **Adresse**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-134">Expand the **Address** section.</span></span>
19. <span data-ttu-id="f3bf6-135">Vis **Forhåndsmerknader**-delen.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-135">Expand the **Prenotes** section.</span></span>
20. <span data-ttu-id="f3bf6-136">Vis delen **Kontaktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-136">Expand the **Contact information** section.</span></span>
21. <span data-ttu-id="f3bf6-137">Skriv inn en verdi i feltet **Telefon**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-137">In the **Telephone** field, type a value.</span></span>
22. <span data-ttu-id="f3bf6-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-138">Close the page.</span></span>
23. <span data-ttu-id="f3bf6-139">Klikk **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-139">Click **Edit**.</span></span>
24. <span data-ttu-id="f3bf6-140">Vis delen **Betaling**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-140">Expand the **Payment** section.</span></span>
25. <span data-ttu-id="f3bf6-141">Velg kontoen du nettopp har opprettet i **Bankkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-141">In the **Bank account** field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="f3bf6-142">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-142">Click **Save**.</span></span> <span data-ttu-id="f3bf6-143">Adressen kan arves fra bankgruppen, hvis det er angitt, eller du kan legge den til her.</span><span class="sxs-lookup"><span data-stu-id="f3bf6-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

