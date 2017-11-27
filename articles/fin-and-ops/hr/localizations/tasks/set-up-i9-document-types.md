--- 
title: Definere dokumenttyper for I-9
description: "Denne prosedyren viser hvordan du viser og definerer dokumenttyper som skal brukes for å bekrefte I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 950237499441e7f1d5b9e3355c4bd9513ad3783e
ms.openlocfilehash: b47998eccd7509154ee8863e2e19594cc59ac945
ms.contentlocale: nb-no
ms.lasthandoff: 11/01/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="b033f-103">Definere dokumenttyper for I-9</span><span class="sxs-lookup"><span data-stu-id="b033f-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="b033f-104">Denne prosedyren viser hvordan du viser og definerer dokumenttyper som skal brukes for å bekrefte I-9.</span><span class="sxs-lookup"><span data-stu-id="b033f-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="b033f-105">Før du setter opp I-9 dokumenttyper, må du også angi utstederinstanser og identifikasjonstyper.</span><span class="sxs-lookup"><span data-stu-id="b033f-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="b033f-106">Demonstrasjonsdatafirmaet som brukes til å opprette denne prosedyren, er USMF, som inneholder eksempler på utstederinstanser og identifikasjonstyper som kreves for å fullføre prosedyren.</span><span class="sxs-lookup"><span data-stu-id="b033f-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="b033f-107">Gå til Personale > Arbeidere > I-9 > I-9 dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="b033f-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="b033f-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b033f-108">Click New.</span></span>
3. <span data-ttu-id="b033f-109">Skriv inn en verdi i feltet I-9 dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="b033f-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="b033f-110">Eksempel: Skole-ID.</span><span class="sxs-lookup"><span data-stu-id="b033f-110">Example: School ID.</span></span>  
4. <span data-ttu-id="b033f-111">Velg identifikasjonstypen.</span><span class="sxs-lookup"><span data-stu-id="b033f-111">Select the identification type.</span></span>  <span data-ttu-id="b033f-112">Eksempel: Skole-ID</span><span class="sxs-lookup"><span data-stu-id="b033f-112">Example:  School ID</span></span>
    * <span data-ttu-id="b033f-113">Eksempler på identifikasjonstyper er et personnummer (SSN), visa-nummer, pass-ID eller førerkort.</span><span class="sxs-lookup"><span data-stu-id="b033f-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's license.</span></span>  
5. <span data-ttu-id="b033f-114">Velg I-9 dokumentlisten som skal brukes for dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b033f-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="b033f-115">Som del av I-9-prosessen må ansatte presentere dokumentasjon som viser arbeidsgiveren identitet og ansettelsesautorisasjon.</span><span class="sxs-lookup"><span data-stu-id="b033f-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="b033f-116">Webområdet for US Citizenship and Immigration Services inneholder informasjon om hvilke dokumenter som kan brukes, og hvilken liste de tilhører.</span><span class="sxs-lookup"><span data-stu-id="b033f-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="b033f-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="b033f-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="b033f-118">I feltet Skjema angir du det offisielle skjemanummeret for dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b033f-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="b033f-119">Eksempel: Skole-ID.</span><span class="sxs-lookup"><span data-stu-id="b033f-119">Example: School ID.</span></span>
    * <span data-ttu-id="b033f-120">De offisielle skjemanumrene finnes på webområdet for US Citizenship and Immigration Services.</span><span class="sxs-lookup"><span data-stu-id="b033f-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="b033f-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="b033f-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="b033f-122">Merk av eller fjern merket i boksen Aktiv.</span><span class="sxs-lookup"><span data-stu-id="b033f-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="b033f-123">Angi datoen i feltet Utløp til 2019-10-27.</span><span class="sxs-lookup"><span data-stu-id="b033f-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="b033f-124">Utløpsdatoen valgfri.</span><span class="sxs-lookup"><span data-stu-id="b033f-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="b033f-125">Velg organisasjonen som utstedte dokumenttypen.</span><span class="sxs-lookup"><span data-stu-id="b033f-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="b033f-126">Eksempel: Område/distrikt</span><span class="sxs-lookup"><span data-stu-id="b033f-126">Example: Province/territory</span></span>
10. <span data-ttu-id="b033f-127">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b033f-127">Click Save.</span></span>


