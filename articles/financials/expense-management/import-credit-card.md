---
title: Importere og opprettholde kredittkorttransaksjoner
description: Dette emnet forklarer hvordan importere og vedlikeholde kostnadsrelaterte kredittkorttransaksjoner. Disse transaksjonene kan konfigureres slik at de importeres automatisk i en gjentatt tidsplan, eller de kan importeres manuelt etter behov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840943"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="1dbe2-104">Importere og opprettholde kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="1dbe2-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dbe2-105">Utgiftsrelaterte kredittkorttransaksjoner kan konfigureres slik at de automatisk importeres på en gjentatt tidsplan.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="1dbe2-106">Alternativt kan transaksjonene importeres manuelt etter behov.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="1dbe2-107">Kredittkorttransaksjonene blir importert via dataenheten Kredittkorttransaksjon.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="1dbe2-108">Hvis du vil ha mer informasjon om datatyper, kan du se [Dataenheter](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="1dbe2-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="1dbe2-109">Importer kredittkorttransaksjoner</span><span class="sxs-lookup"><span data-stu-id="1dbe2-109">Import credit card transactions</span></span>

1. <span data-ttu-id="1dbe2-110">På siden **kredittkorttransaksjoner**, velg **Importer transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="1dbe2-111">Hvis du åpner databehandling for første gang, må systemet oppdatere listen over dataenheter før du kan fortsette.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="1dbe2-112">Skriv inn en unik beskrivelse av importjobben i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="1dbe2-113">I feltet **Kildedataformat**, velg formatet for filen som inneholder kredittkorttransaksjonene som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="1dbe2-114">Velg **Last opp** og finn og velg filen som skal importeres.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="1dbe2-115">Etter at filen er lastet opp, valider tilordning av filen med kredittkorttransaksjonene og kolonnene for dataenhet for Kredittkorttransaksjoner ved å velge **Se kartlegging**-koblingen på flisen.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="1dbe2-116">Hvis det er tilordningsfeil, eller du må endre tilordningen, gjør tilordningsendringene fra enten kategorien **Mappevisualisering** eller kategorien **Mappedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="1dbe2-117">For å automatisere kredittkorttransaksjoner, velg **Opprett gjentakende datajobb**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="1dbe2-118">Du kan deretter angi gjentakelsen som definerer hvor ofte kredittkorttransaksjoner skal importeres.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="1dbe2-119">Når du er ferdig, velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="1dbe2-120">For å importere den valgte filen nå, velg **Importer**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="1dbe2-121">Hvis det oppstår feil under importen, kan du se utførelsesloggen eller lagringsdata for å se feilene du må fikse for å garantere en vellykket import.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="1dbe2-122">Hvis du må importere flere enn ett filformat, må du opprette separate importjobber for hver formattype.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="1dbe2-123">Tilordne kredittkorttransaksjonene for ansatte som har sluttet</span><span class="sxs-lookup"><span data-stu-id="1dbe2-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="1dbe2-124">Etter at en ansatts oppføringer er terminert, vil den ansattes Active Directory Domain Services (AD DS)-konto deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="1dbe2-125">Det kan imidlertid være aktive kredittkorttransaksjoner som fortsatt må kostnadsføres og refunderes.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="1dbe2-126">Fra siden **Kredittkorttransaksjoner** kan du tilordne medarbeiderne for eventuelle kredittkorttransaksjoner for ansatte som har sluttet.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="1dbe2-127">Velg én eller flere kredittkorttransaksjoner, og velg deretter **Tilordne transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="1dbe2-128">Du kan velge en annen ansatt å tildele kredittkorttransaksjoner til.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="1dbe2-129">Etter at kredittkorttransaksjonene er tildelt kan de velges for en utgiftsrapport og betales gjennom de vanlige prosesser for refusjon av utgifter.</span><span class="sxs-lookup"><span data-stu-id="1dbe2-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
