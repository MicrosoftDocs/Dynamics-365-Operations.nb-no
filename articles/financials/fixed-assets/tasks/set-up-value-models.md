--- 
title: "Definere tablåer"
description: "Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: b18f52254b9073cd95bf50539a4414598a8c19cc
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-books"></a><span data-ttu-id="c8f06-103">Definere tablåer</span><span class="sxs-lookup"><span data-stu-id="c8f06-103">Set up books</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c8f06-104">Denne fremgangsmåten viser hvordan du oppretter et nytt anleggsmiddeltablå og knytter det til en anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="c8f06-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="c8f06-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="c8f06-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="c8f06-106">Opprette et tablå</span><span class="sxs-lookup"><span data-stu-id="c8f06-106">Create a book</span></span>
1. <span data-ttu-id="c8f06-107">Gå til Anleggsmidler > Oppsett > Tablåer.</span><span class="sxs-lookup"><span data-stu-id="c8f06-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="c8f06-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="c8f06-108">Click New.</span></span>
3. <span data-ttu-id="c8f06-109">Skriv inn en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="c8f06-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="c8f06-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c8f06-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c8f06-111">Hvis Beregn avskrivning er valgt, inkluderes det tilknyttede anleggsmiddeltablået i avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="c8f06-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="c8f06-112">Hvis det ikke er valgt, vil anleggsmiddeltablået ikke automatisk avskrives.</span><span class="sxs-lookup"><span data-stu-id="c8f06-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="c8f06-113">Velg Ja i feltet Beregn avskrivning.</span><span class="sxs-lookup"><span data-stu-id="c8f06-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="c8f06-114">Angi eller velg en verdi i feltet Avskrivningsprofil.</span><span class="sxs-lookup"><span data-stu-id="c8f06-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f06-115">En alternativ avskrivningsprofil er også kjent som en avskrivningsmetode for avskrivning.</span><span class="sxs-lookup"><span data-stu-id="c8f06-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="c8f06-116">Avskrivningsforslaget vil bytte til denne profilen når den alternative profilen beregner et avskrivningsbeløp som er lik eller større enn standard avskrivningsprofil.</span><span class="sxs-lookup"><span data-stu-id="c8f06-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="c8f06-117">Den ekstraordinære avskrivningsprofilen brukes til ytterligere avskrivning av et aktiva i uvanlige omstendigheter.</span><span class="sxs-lookup"><span data-stu-id="c8f06-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="c8f06-118">Du kan for eksempel bruke denne til å registrere avskrivning som skyldes en naturkatastrofe.</span><span class="sxs-lookup"><span data-stu-id="c8f06-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="c8f06-119">Hvis Opprett avskrivningsjusteringer med basisjusteringer er valgt, opprettes avskrivningsjusteringer automatisk når verdien til anleggsmidlet blir oppdatert.</span><span class="sxs-lookup"><span data-stu-id="c8f06-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="c8f06-120">Hvis det ikke er valgt, påvirker den oppdaterte anleggsmiddelverdien bare avskrivningsberegninger fremover.</span><span class="sxs-lookup"><span data-stu-id="c8f06-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="c8f06-121">Velg Ja i feltet Opprett avskrivningsjusteringer med basisjusteringer.</span><span class="sxs-lookup"><span data-stu-id="c8f06-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="c8f06-122">Som standard posteres anleggsmiddeltablåtransaksjoner til økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c8f06-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="c8f06-123">Du kan deaktivere postering i Finans for tablået ved å sette Poster i økonomimodul til Nei.</span><span class="sxs-lookup"><span data-stu-id="c8f06-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="c8f06-124">Tablåer som ikke posteres i Finans brukes vanligvis for mva-rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="c8f06-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="c8f06-125">Dette gir deg mer fleksibilitet til å slette historiske transaksjoner for anleggsmiddeltablået fordi de ikke er lagret i Finans.</span><span class="sxs-lookup"><span data-stu-id="c8f06-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="c8f06-126">Posteringslaget er som standard det gjeldende laget hvis tablået posterer til Finans, og Ingen hvis det ikke bokføres i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="c8f06-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="c8f06-127">Oppdater posteringslaget hvis du må postere transaksjoner for dette tablået til et annet lag.</span><span class="sxs-lookup"><span data-stu-id="c8f06-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="c8f06-128">Angi eller velg en verdi i Kalender-feltet.</span><span class="sxs-lookup"><span data-stu-id="c8f06-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="c8f06-129">Avledede tablåer vil postere transaksjoner til forskjellige tablåer samtidig.</span><span class="sxs-lookup"><span data-stu-id="c8f06-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="c8f06-130">Du oppretter transaksjonene med det primære tablået og under posteringen posteres en nøyaktig kopi av transaksjonen til det avledede tablået.</span><span class="sxs-lookup"><span data-stu-id="c8f06-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="c8f06-131">Det er ingen omberegning med avledede tablåtransaksjoner, og må derfor ikke brukes for avskrivningstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c8f06-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="c8f06-132">Knytte tablået til en anleggsmiddelgruppe</span><span class="sxs-lookup"><span data-stu-id="c8f06-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="c8f06-133">Klikk Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="c8f06-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="c8f06-134">Angi eller velg en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="c8f06-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="c8f06-135">Angi et tall i Levetid-feltet.</span><span class="sxs-lookup"><span data-stu-id="c8f06-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="c8f06-136">Merk at Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="c8f06-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="c8f06-137">Du kan angi avskrivningskonvensjonen etter behov for skatte-og avgiftsformål.</span><span class="sxs-lookup"><span data-stu-id="c8f06-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


