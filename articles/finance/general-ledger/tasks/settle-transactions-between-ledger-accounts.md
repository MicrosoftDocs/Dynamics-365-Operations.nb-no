---
title: Utligne transaksjoner mellom finanskontoer
description: Denne fremgangsmåten viser hvordan du utligner transaksjoner mellom finanskontoer og avbryter en finansutligning.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446418"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="e8220-103">Utligne transaksjoner mellom finanskontoer</span><span class="sxs-lookup"><span data-stu-id="e8220-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8220-104">Denne fremgangsmåten viser hvordan du utligner transaksjoner mellom finanskontoer og avbryter en finansutligning.</span><span class="sxs-lookup"><span data-stu-id="e8220-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="e8220-105">Denne prosedyren bruker demonstrasjonsdatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e8220-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="e8220-106">Utligne transaksjon mellom finanskontoer</span><span class="sxs-lookup"><span data-stu-id="e8220-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="e8220-107">Gå til Økonomimodul > Periodiske oppgaver > Utligninger.</span><span class="sxs-lookup"><span data-stu-id="e8220-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="e8220-108">Finn transaksjonen som du vil utligne, i listen.</span><span class="sxs-lookup"><span data-stu-id="e8220-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="e8220-109">Saldobeløpet må være null.</span><span class="sxs-lookup"><span data-stu-id="e8220-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="e8220-110">Klikk Inkluder.</span><span class="sxs-lookup"><span data-stu-id="e8220-110">Click Include.</span></span>
4. <span data-ttu-id="e8220-111">Klikk Godta.</span><span class="sxs-lookup"><span data-stu-id="e8220-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="e8220-112">Avbryte en utligning</span><span class="sxs-lookup"><span data-stu-id="e8220-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="e8220-113">Gå til Økonomimodul > Forespørsler og rapporter > Råbalanse.</span><span class="sxs-lookup"><span data-stu-id="e8220-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="e8220-114">Klikk Parametre for å åpne nedtrekksdialogskjemaet.</span><span class="sxs-lookup"><span data-stu-id="e8220-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="e8220-115">Klikk Oppdater.</span><span class="sxs-lookup"><span data-stu-id="e8220-115">Click Update.</span></span>
4. <span data-ttu-id="e8220-116">Finn kontoen som har den utlignede transaksjonen, i listen.</span><span class="sxs-lookup"><span data-stu-id="e8220-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="e8220-117">Klikk Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e8220-117">Click All transactions.</span></span>
6. <span data-ttu-id="e8220-118">Bruk et filter til enkelt å finne transaksjonen i listen.</span><span class="sxs-lookup"><span data-stu-id="e8220-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="e8220-119">Klikk Utligninger.</span><span class="sxs-lookup"><span data-stu-id="e8220-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="e8220-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e8220-120">In the list, mark the selected row.</span></span>

