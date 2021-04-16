---
title: Utligne transaksjoner mellom finanskontoer
description: Denne fremgangsmåten viser hvordan du utligner transaksjoner mellom finanskontoer og avbryter en finansutligning.
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2594b90ed58a1e7f12c8a94d3c48266faef557f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817059"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="ec212-103">Utligne transaksjoner mellom finanskontoer</span><span class="sxs-lookup"><span data-stu-id="ec212-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec212-104">Denne fremgangsmåten viser hvordan du utligner transaksjoner mellom finanskontoer og avbryter en finansutligning.</span><span class="sxs-lookup"><span data-stu-id="ec212-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="ec212-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ec212-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="ec212-106">Utligne transaksjon mellom finanskontoer</span><span class="sxs-lookup"><span data-stu-id="ec212-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="ec212-107">Gå til Økonomimodul > Periodiske oppgaver > Utligninger.</span><span class="sxs-lookup"><span data-stu-id="ec212-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="ec212-108">Finn transaksjonen som du vil utligne, i listen.</span><span class="sxs-lookup"><span data-stu-id="ec212-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="ec212-109">Saldobeløpet må være null.</span><span class="sxs-lookup"><span data-stu-id="ec212-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="ec212-110">Klikk Inkluder.</span><span class="sxs-lookup"><span data-stu-id="ec212-110">Click Include.</span></span>
4. <span data-ttu-id="ec212-111">Klikk Godta.</span><span class="sxs-lookup"><span data-stu-id="ec212-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="ec212-112">Avbryte en utligning</span><span class="sxs-lookup"><span data-stu-id="ec212-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="ec212-113">Gå til Økonomimodul > Forespørsler og rapporter > Råbalanse.</span><span class="sxs-lookup"><span data-stu-id="ec212-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="ec212-114">Klikk Parametre for å åpne nedtrekksdialogskjemaet.</span><span class="sxs-lookup"><span data-stu-id="ec212-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="ec212-115">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="ec212-115">Click Update.</span></span>
4. <span data-ttu-id="ec212-116">Finn kontoen som har den utlignede transaksjonen, i listen.</span><span class="sxs-lookup"><span data-stu-id="ec212-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="ec212-117">Klikk Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ec212-117">Click All transactions.</span></span>
6. <span data-ttu-id="ec212-118">Bruk et filter til enkelt å finne transaksjonen i listen.</span><span class="sxs-lookup"><span data-stu-id="ec212-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="ec212-119">Klikk Utligninger.</span><span class="sxs-lookup"><span data-stu-id="ec212-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="ec212-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ec212-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]