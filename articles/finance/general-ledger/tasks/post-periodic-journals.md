---
title: Postere periodiske journaler
description: Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dacf7f21d147b780d57b0e7a61b11d78d30fa52
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834425"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="0fd46-103">Postere periodiske journaler</span><span class="sxs-lookup"><span data-stu-id="0fd46-103">Post periodic journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fd46-104">Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes.</span><span class="sxs-lookup"><span data-stu-id="0fd46-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="0fd46-105">Når du oppretter den periodiske journalen, angir du tidsintervallet for gjentakelse, for eksempel dager eller måneder.</span><span class="sxs-lookup"><span data-stu-id="0fd46-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="0fd46-106">Denne oppgaveveiledningen oppretter en periodisk journal med månedlig gjentakelse.</span><span class="sxs-lookup"><span data-stu-id="0fd46-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="0fd46-107">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Periodiske oppgaver > Periodiske journaler**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="0fd46-108">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-108">Click **New**.</span></span>
3. <span data-ttu-id="0fd46-109">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="0fd46-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0fd46-111">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="0fd46-112">Beskrivelsen vil være navnet på den periodiske journalen når du senere henter den, så pass på å gi den et relevant navn.</span><span class="sxs-lookup"><span data-stu-id="0fd46-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="0fd46-113">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="0fd46-114">En periodisk journal inneholder vanligvis flere journallinjer.</span><span class="sxs-lookup"><span data-stu-id="0fd46-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="0fd46-115">Denne oppgaveveiledningen legger imidlertid bare til én linje.</span><span class="sxs-lookup"><span data-stu-id="0fd46-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="0fd46-116">Angi en dato i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="0fd46-117">**Dato**-feltet inneholder posteringsdatoen for neste overføring til den daglige journalen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="0fd46-118">For journaler som hentes hver måned, anbefales det å bruke datoen i måneden når det skal posteres, vanligvis første eller siste datoen i perioden.</span><span class="sxs-lookup"><span data-stu-id="0fd46-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="0fd46-119">Det er mulig å la Dato-feltet stå tomt og gi en dato når journalen hentes, ved hjelp av det tomme Dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="0fd46-120">Feltet oppdateres automatisk til neste gjentakende dato når transaksjoner hentes.</span><span class="sxs-lookup"><span data-stu-id="0fd46-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="0fd46-121">Angi de ønskede verdiene i **Konto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="0fd46-122">Velg en verdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="0fd46-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0fd46-123">Close the page.</span></span>
11. <span data-ttu-id="0fd46-124">Angi et tall i **Debet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="0fd46-125">Angi ønskede verdier i **Motkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="0fd46-126">Velg Måneder i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="0fd46-127">Angi 1 i feltet **Antall enheter**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="0fd46-128">Angi en dato i **Siste dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="0fd46-129">Hvis du angir den siste datoen i den forrige perioden, hindrer du at den gjentakende journalen ved en feil blir opprettet i feil startperiode.</span><span class="sxs-lookup"><span data-stu-id="0fd46-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="0fd46-130">Siste dato oppdateres senere hver gang den periodiske journalen hentes.</span><span class="sxs-lookup"><span data-stu-id="0fd46-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="0fd46-131">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-131">Click **Save**.</span></span>
17. <span data-ttu-id="0fd46-132">Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="0fd46-133">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-133">Click **New**.</span></span>
19. <span data-ttu-id="0fd46-134">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="0fd46-135">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="0fd46-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="0fd46-137">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="0fd46-138">Klikk på **Linjer** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="0fd46-139">Klikk på **Periodisk journal** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="0fd46-140">Klikk på **Hent journal**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="0fd46-141">Angi en dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0fd46-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="0fd46-142">**Til dato** fungerer som fristen for de periodiske bilagslinjene.</span><span class="sxs-lookup"><span data-stu-id="0fd46-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="0fd46-143">Basert på innstillingen for regelmessighet kan den siste datoen og til-datoen på den samme linjen inkluderes mer enn én gang i den resulterende journalen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="0fd46-144">Til-datoen oppdateres automatisk basert på øktdatoen for siste gang den periodiske linjen ble overført til en journal.</span><span class="sxs-lookup"><span data-stu-id="0fd46-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="0fd46-145">Angi eller velg en verdi i feltet **Nummer på periodisk journal**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="0fd46-146">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0fd46-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="0fd46-147">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fd46-147">Click **OK**.</span></span> <span data-ttu-id="0fd46-148">Den periodiske journalen kan nå gjennomgås, godkjennes eller posteres avhengig av behov og oppsett.</span><span class="sxs-lookup"><span data-stu-id="0fd46-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]