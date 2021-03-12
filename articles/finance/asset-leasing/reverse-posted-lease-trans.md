---
title: Tilbakeføre posterte leietransaksjoner
description: Dette emnet beskriver hvordan du tilbakefører en postert leietransaksjon. Alle transaksjoner som opprettes gjennom aktivaleie, kan tilbakeføres.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e4908ddab2650e5ff7e4a28bf916604d165d08c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969534"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="f5511-104">Tilbakeføre posterte leietransaksjoner</span><span class="sxs-lookup"><span data-stu-id="f5511-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5511-105">Alle transaksjoner som opprettes gjennom aktivaleie, kan tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="f5511-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="f5511-106">Transaksjoner som tilbakeføres gjennom aktivaleie, oppdaterer leiedataene.</span><span class="sxs-lookup"><span data-stu-id="f5511-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="f5511-107">Derfor oppdaterer du også de bærende verdiene for leieforpliktelse og bruksrettseiendel.</span><span class="sxs-lookup"><span data-stu-id="f5511-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="f5511-108">Hvis du vil opprette en tilbakeføringstransaksjon for en leieavtale, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f5511-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="f5511-109">På siden **Aktivatransaksjoner** eller **Gjeldstransaksjoner** velger du transaksjonen, og deretter velger du **Tilbakefør transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="f5511-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="f5511-110">I dialogboksen som vises, kan du redigere datoen for postering av tilbakeføringsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="f5511-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="f5511-111">Som standard er **Dato**-feltet satt til transaksjonsposteringsdatoen for transaksjonen som er valgt.</span><span class="sxs-lookup"><span data-stu-id="f5511-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="f5511-112">Tilbakeføringsoppføringen kan ikke posteres tidligere enn den opprinnelige posteringsdatoen for den valgte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="f5511-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="f5511-113">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5511-113">Select **OK**.</span></span> <span data-ttu-id="f5511-114">En journaloppføring posteres, som reverserer posten du har valgt.</span><span class="sxs-lookup"><span data-stu-id="f5511-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="f5511-115">Tilbakeføringen vises på siden **Aktivatransaksjoner** eller **Gjeldstransaksjoner**, og nettosummen for gjeldende saldo som vises på siden, oppdateres.</span><span class="sxs-lookup"><span data-stu-id="f5511-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="f5511-116">Når du velger **Tilbakeført sporing**, blir det vist en dialogboks der det vises både de opprinnelige transaksjonene og de tilbakeførte transaksjonene sammen med et koblet nummer som kalles et *sporingsnummer*.</span><span class="sxs-lookup"><span data-stu-id="f5511-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="f5511-117">Hvis du vil gjøre tilbakeføringene enklere å forstå og forbedre synligheten, kan du også spore tilbakeføringer ved hjelp av leieplaner.</span><span class="sxs-lookup"><span data-stu-id="f5511-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="f5511-118">Feltet **Siste journalnummer** på siden **Tidsplan** viser journalnumrene til transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="f5511-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="f5511-119">Når en transaksjon tilbakeføres, oppdateres dette feltet med journalnummeret til en tilbakeføringstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5511-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="f5511-120">I tillegg er avmerkingsboksen **Tilbakeført** for å angi at transaksjonen er tilbakeført, og at feltet **Postert** er valgt.</span><span class="sxs-lookup"><span data-stu-id="f5511-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="f5511-121">Oppheve en tilbakeført transaksjon</span><span class="sxs-lookup"><span data-stu-id="f5511-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="f5511-122">Følg denne fremgangsmåten for å oppheve en tilbakeført transaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5511-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="f5511-123">På siden **Tidsplan** eller **Transaksjoner** velger du en opprinnelig transaksjon.</span><span class="sxs-lookup"><span data-stu-id="f5511-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="f5511-124">Følg ett av disse trinnene:</span><span class="sxs-lookup"><span data-stu-id="f5511-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="f5511-125">Hvis du valgte transaksjonen på siden **Tidsplan**, følger du fremgangsmåten for å opprette en journal i [Opprette månedlige journaloppføringer i en bunke](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="f5511-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="f5511-126">Du må postere journalen manuelt.</span><span class="sxs-lookup"><span data-stu-id="f5511-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="f5511-127">Hvis du valgte transaksjonen på **Transaksjoner**-siden, velger du **Tilbakefør transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="f5511-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="f5511-128">Du får en melding som sier at denne opphevelsen er en opphevelse av en tidligere tilbakeføring, og at du kan redigere posteringsdatoen for denne opphevelsen.</span><span class="sxs-lookup"><span data-stu-id="f5511-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="f5511-129">Generelle forretningsvalideringer påvirker imidlertid datoene som kan registreres i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f5511-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="f5511-130">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5511-130">Select **OK**.</span></span> <span data-ttu-id="f5511-131">En journaloppføring posteres, som reverserer posten du har valgt.</span><span class="sxs-lookup"><span data-stu-id="f5511-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="f5511-132">Tilbakeføringen vises på **Transaksjoner**-siden, og nettosummen for gjeldende saldo gjenopprettes til hva den var før den første tilbakeføringen.</span><span class="sxs-lookup"><span data-stu-id="f5511-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="f5511-133">Derfor vil innvirkningen som tilbakeføringen hadde på saldoene, negeres.</span><span class="sxs-lookup"><span data-stu-id="f5511-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="f5511-134">Når du velger **Tilbakeført sporing**, blir det vist en dialogboks der det vises både de opprinnelige transaksjonene og de tilbakeførte transaksjonene sammen med et koblet sporingsnummer.</span><span class="sxs-lookup"><span data-stu-id="f5511-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="f5511-135">Du kan også spore opphevelser ved å bruke den riktige **Tidsplaner**-siden.</span><span class="sxs-lookup"><span data-stu-id="f5511-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="f5511-136">Merket fjernes i **Tilbakefør**-feltet, mens **Journal postert** velges.</span><span class="sxs-lookup"><span data-stu-id="f5511-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="f5511-137">I tillegg oppdateres feltet **Siste journalnummer** med journalnummeret til den opphevede transaksjonen, og feltet **Journalnummer** oppdateres med tilbakeføringsjournalnummeret.</span><span class="sxs-lookup"><span data-stu-id="f5511-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>
