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
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18395f300965df7e024f0eec2b53fa4e8ad2cc3e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566208"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="eef91-103">Opprette en fasilitetsavtale for en remburs</span><span class="sxs-lookup"><span data-stu-id="eef91-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eef91-104">Denne oppgaven hjelper deg med å opprette en bankfasilitetsavtale for å behandle en remburs.</span><span class="sxs-lookup"><span data-stu-id="eef91-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="eef91-105">Du skal sette opp bankfasiliteter og posteringsprofiler før denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eef91-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="eef91-106">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="eef91-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="eef91-107">Opprette en bankfasilitetsavtale</span><span class="sxs-lookup"><span data-stu-id="eef91-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="eef91-108">Gå til Kontant- og bankbehandling > Purringer > Bankfasilitetsavtaler.</span><span class="sxs-lookup"><span data-stu-id="eef91-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="eef91-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="eef91-109">Click New.</span></span>
3. <span data-ttu-id="eef91-110">I Avtalenummer-feltet angir du avtalenummeret i henhold til avtalen med banken.</span><span class="sxs-lookup"><span data-stu-id="eef91-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="eef91-111">I Bankkonto-feltet angir du kontonummeret for utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="eef91-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="eef91-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eef91-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="eef91-113">Angi dato og klokkeslett i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="eef91-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="eef91-114">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="eef91-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="eef91-115">Vis eller skjul delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="eef91-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="eef91-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="eef91-116">Click Add line.</span></span>
10. <span data-ttu-id="eef91-117">Klikk rullegardinknappen i feltet Fasilitetstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="eef91-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="eef91-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="eef91-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="eef91-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="eef91-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="eef91-120">Angi fasilitetsbeløpet som er fremforhandlet med banken, i Grense-feltet.</span><span class="sxs-lookup"><span data-stu-id="eef91-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="eef91-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="eef91-121">Click Save.</span></span>
15. <span data-ttu-id="eef91-122">Klikk Utvid for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="eef91-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="eef91-123">Angi en verdi i feltet Nytt avtalenummer.</span><span class="sxs-lookup"><span data-stu-id="eef91-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="eef91-124">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="eef91-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="eef91-125">Klikk Utvid.</span><span class="sxs-lookup"><span data-stu-id="eef91-125">Click Extend.</span></span>
19. <span data-ttu-id="eef91-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="eef91-126">Close the page.</span></span>

