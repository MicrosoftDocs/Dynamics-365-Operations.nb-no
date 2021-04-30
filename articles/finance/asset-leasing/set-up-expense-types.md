---
title: Definere utgiftstyper
description: Dette emnet forklarer hvordan du definerer utgiftstyper i aktivaleie.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880990"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="2c5c7-103">Definere utgiftstyper</span><span class="sxs-lookup"><span data-stu-id="2c5c7-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c5c7-104">Dette emnet forklarer hvordan du definerer utgiftstyper i aktivaleie.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="2c5c7-105">Kostnader som ikke representeres av betalingsplanen, kalles *utgiftskostnader*.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="2c5c7-106">Eksempler på disse kostnadene inkluderer eiendomsavgifter, vedlikeholdskostnader for vanlige områder og forsikringsutgifter.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="2c5c7-107">Legge til en administrativ utgiftstype</span><span class="sxs-lookup"><span data-stu-id="2c5c7-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="2c5c7-108">Gå til **Aktivaleie \> Oppsett \> Utgiftstyper**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="2c5c7-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-109">Select **New**.</span></span>
3. <span data-ttu-id="2c5c7-110">I de aktuelle feltene angir du den nye utgiftstypen og en beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="2c5c7-111">Tilordne kontoer til administrative kostnader</span><span class="sxs-lookup"><span data-stu-id="2c5c7-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="2c5c7-112">Deretter bør du knytte kontoer til utgiftstypene.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="2c5c7-113">Disse kontoene blir debitert når utgiftsplanoppføringer posteres.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="2c5c7-114">Motkontoen angis på linjene for **betalingsplan for fullbyrdelseskostnad** på hver leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="2c5c7-115">Gå til **Aktivaleie \> Oppsett \> Parametere for aktivaleie**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="2c5c7-116">I kategorien **Kontoer** på hurtigfanen for **fullbyrdelseskostnad** i feltet **Utgiftstype** velger du utgiftstype.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="2c5c7-117">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-117">Select **Add**.</span></span>
4. <span data-ttu-id="2c5c7-118">I feltet for **tablåtype** velger du tablåtypen for å koble til de administrative kostnadene.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2c5c7-119">Flere tablåtyper kan knyttes til den samme utgiftskontoen.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="2c5c7-120">I **Kontokode**-feltet angir du hvilke leieavtaler tablået skal brukes på:</span><span class="sxs-lookup"><span data-stu-id="2c5c7-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="2c5c7-121">**Alle** – Bruk tablået på alle leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="2c5c7-122">**Gruppe** – Bruk tablået på en bestemt gruppe leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="2c5c7-123">**Tabell** – Bruk tablået på spesifikke leieavtaler.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="2c5c7-124">Hvis du har valgt **Gruppe** eller **Tabell** i **Kontokode**, velger du et kontonummer eller gruppenummer i feltet **Konto-/gruppenummer**.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="2c5c7-125">I de aktuelle feltene velger du hovedkonto for finansiell leie og hovedkonto for gjeldende leie.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="2c5c7-126">Når du har fullført disse trinnene, kan du legge til utgifter ved hjelp av linjene i **betalingsplan for fullbyrdelseskostnad** på siden **Leiedetaljer** for en valgt leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="2c5c7-127">Du kan også legge til utgifter når du oppretter en ny leieavtale.</span><span class="sxs-lookup"><span data-stu-id="2c5c7-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
