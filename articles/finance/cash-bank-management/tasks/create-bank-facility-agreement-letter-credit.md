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
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bffb5c802e8fa261e52197d1293ffb15c35981f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989170"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="e395b-103">Opprette en fasilitetsavtale for en remburs</span><span class="sxs-lookup"><span data-stu-id="e395b-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e395b-104">Denne oppgaven hjelper deg med å opprette en bankfasilitetsavtale for å behandle en remburs.</span><span class="sxs-lookup"><span data-stu-id="e395b-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="e395b-105">Du skal sette opp bankfasiliteter og posteringsprofiler før denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="e395b-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="e395b-106">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="e395b-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="e395b-107">Opprette en bankfasilitetsavtale</span><span class="sxs-lookup"><span data-stu-id="e395b-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="e395b-108">Gå til Kontant- og bankbehandling > Purringer > Bankfasilitetsavtaler.</span><span class="sxs-lookup"><span data-stu-id="e395b-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="e395b-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e395b-109">Click New.</span></span>
3. <span data-ttu-id="e395b-110">I Avtalenummer-feltet angir du avtalenummeret i henhold til avtalen med banken.</span><span class="sxs-lookup"><span data-stu-id="e395b-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="e395b-111">I Bankkonto-feltet angir du kontonummeret for utstedende bank.</span><span class="sxs-lookup"><span data-stu-id="e395b-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="e395b-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e395b-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e395b-113">Angi dato og klokkeslett i Startdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="e395b-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="e395b-114">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="e395b-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="e395b-115">Vis eller skjul delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="e395b-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="e395b-116">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="e395b-116">Click Add line.</span></span>
10. <span data-ttu-id="e395b-117">Klikk rullegardinknappen i feltet Fasilitetstype for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="e395b-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e395b-118">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e395b-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e395b-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e395b-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e395b-120">Angi fasilitetsbeløpet som er fremforhandlet med banken, i Grense-feltet.</span><span class="sxs-lookup"><span data-stu-id="e395b-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="e395b-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="e395b-121">Click Save.</span></span>
15. <span data-ttu-id="e395b-122">Klikk Utvid for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="e395b-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="e395b-123">Angi en verdi i feltet Nytt avtalenummer.</span><span class="sxs-lookup"><span data-stu-id="e395b-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="e395b-124">Angi dato og klokkeslett i Sluttdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="e395b-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="e395b-125">Klikk Utvid.</span><span class="sxs-lookup"><span data-stu-id="e395b-125">Click Extend.</span></span>
19. <span data-ttu-id="e395b-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e395b-126">Close the page.</span></span>

