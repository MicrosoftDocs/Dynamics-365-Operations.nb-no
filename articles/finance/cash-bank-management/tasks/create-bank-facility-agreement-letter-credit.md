---
title: Opprette en fasilitetsavtale for en remburs
description: Denne oppgaven hjelper deg med å opprette en bankfasilitetsavtale for å behandle en remburs.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb624700e0b052de977fabecf9670b3515d32ab7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446382"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="43933-103">Opprette en fasilitetsavtale for en remburs</span><span class="sxs-lookup"><span data-stu-id="43933-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43933-104">Denne oppgaven hjelper deg med å opprette en bankfasilitetsavtale for å behandle en remburs.</span><span class="sxs-lookup"><span data-stu-id="43933-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="43933-105">Du skal sette opp bankfasiliteter og posteringsprofiler før denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="43933-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="43933-106">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="43933-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="43933-107">Opprette en bankfasilitetsavtale</span><span class="sxs-lookup"><span data-stu-id="43933-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="43933-108">Gå til Kontant- og bankbehandling > Purringer > Bankfasilitetsavtaler.</span><span class="sxs-lookup"><span data-stu-id="43933-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="43933-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="43933-109">Click New.</span></span>
3. <span data-ttu-id="43933-110">I Avtalenummer-feltet angir du avtalenummeret i henhold til avtalen med banken.</span><span class="sxs-lookup"><span data-stu-id="43933-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="43933-111">I Bankkonto-feltet angir du kontonummeret for utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="43933-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="43933-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="43933-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="43933-113">Angi dato og klokkeslett i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="43933-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="43933-114">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="43933-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="43933-115">Vis eller skjul delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="43933-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="43933-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="43933-116">Click Add line.</span></span>
10. <span data-ttu-id="43933-117">Klikk rullegardinknappen i feltet Fasilitetstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="43933-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="43933-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="43933-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="43933-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="43933-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="43933-120">Angi fasilitetsbeløpet som er fremforhandlet med banken, i Grense-feltet.</span><span class="sxs-lookup"><span data-stu-id="43933-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="43933-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="43933-121">Click Save.</span></span>
15. <span data-ttu-id="43933-122">Klikk Utvid for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="43933-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="43933-123">Angi en verdi i feltet Nytt avtalenummer.</span><span class="sxs-lookup"><span data-stu-id="43933-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="43933-124">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="43933-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="43933-125">Klikk Utvid.</span><span class="sxs-lookup"><span data-stu-id="43933-125">Click Extend.</span></span>
19. <span data-ttu-id="43933-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="43933-126">Close the page.</span></span>

