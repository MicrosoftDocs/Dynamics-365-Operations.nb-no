---
title: Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for butikktransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991362"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="1f91f-103">Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="1f91f-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f91f-104">I Dynamics 365 Retail versjon 10.0.4 og tidligere er postering av utdrag en operasjon på slutten av dagen, og alle transaksjoner posteres i bøkene på slutten av dagen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="1f91f-105">Store transaksjoner må deretter behandles i et begrenset tidsvindu, noe som noen ganger kan føre til belastning og låsing og feil i utdragsposteringen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="1f91f-106">Forhandlere kan heller ikke føre inntekter og betalinger i sine bøker gjennom hele dagen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="1f91f-107">Med fordeling av feedbasert ordreoppretting, som ble innført i Retail versjon 10.0.5, behandles transaksjoner gjennom hele dagen, og bare finansavstemmingen for betalingsmidler og andre kassastyringstransaksjoner behandles på slutten av dagen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="1f91f-108">Denne funksjonen deler belastningen med å opprette salgsordrer, fakturaer og betalinger gjennom hele dagen, noe som gir bedre ytelse og muligheten til å føre inntekter og betalinger i de andre bøkene i nærheten av sanntid.</span><span class="sxs-lookup"><span data-stu-id="1f91f-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="1f91f-109">Bruke fordeling av feedbasert postering</span><span class="sxs-lookup"><span data-stu-id="1f91f-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="1f91f-110">Hvis du vil aktivere fordelingsfeedbasert postering av detaljhandelstransaksjoner, aktiverer du funksjonen **Detaljhandelsoppgaver – fordelingsfeed** ved hjelp av Funksjonsbehandling.</span><span class="sxs-lookup"><span data-stu-id="1f91f-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="1f91f-111">Før du aktiverer funksjonen må du sørge for at ingen utdrag venter på å bli postert.</span><span class="sxs-lookup"><span data-stu-id="1f91f-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="1f91f-112">Gjeldende utdragsdokument blir delt inn i to typer: transaksjonsutdrag og regnskapsoppgjør.</span><span class="sxs-lookup"><span data-stu-id="1f91f-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="1f91f-113">Transaksjonsoppgaven vil plukke opp alle uposterte og godkjente transaksjoner, og opprette salgsordrer, salgsfakturaer, betalings- og rabattjournaler og transaksjoner for inntekter/utgifter med det intervallet du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="1f91f-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="1f91f-114">Du bør konfigurere denne prosessen til å kjøre med høy frekvens, slik at dokumenter opprettes når transaksjonene lastes opp til Headquarters via P-jobben.</span><span class="sxs-lookup"><span data-stu-id="1f91f-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="1f91f-115">Med transaksjonsutdraget som allerede oppretter salgsordrer og salgsfakturaer, er det ikke noe reelt behov for å konfigurere den satsvise jobben **Poster lager**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="1f91f-116">Du kan imidlertid fortsatt bruke den til å oppfylle bestemte forretningskrav som du kanskje har.</span><span class="sxs-lookup"><span data-stu-id="1f91f-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="1f91f-117">Regnskapsoppgjøret er utformet til å opprettes på slutten av dagen, og støtter bare avsluttingsmetoden **Skift**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="1f91f-118">Dette utdraget vil være begrenset til økonomisk avstemming, og vil bare opprette journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for de forskjellige anleggsmidlene, sammen med journaler for andre kontantstyringstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="1f91f-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="1f91f-119">Hvis du vil beregne transaksjonsutdraget, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn transaksjonsutdrag satsvis**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="1f91f-120">Hvis du vil postere transaksjonsutdragene satsvis, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster transaksjonsutdrag satsvis**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="1f91f-121">Hvis du vil beregne regnskapsoppgjøret, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn regnskapsoppgjør satsvis**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="1f91f-122">Hvis du vil postere regnskapsoppgjøret satsvis, går du til **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster regnskapsoppgjør satsvis**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="1f91f-123">Menyelementene **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Beregn utdrag satsvis** og **Retail og Commerce > IT for Retail og Commerce > Salgsstedspostering > Poster utdrag satsvis** blir fjernet med denne nye funksjonen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="1f91f-124">Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt.</span><span class="sxs-lookup"><span data-stu-id="1f91f-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="1f91f-125">Gå til **Retail og Commerce > Kanaler > Butikker** og klikk **Utdrag**.</span><span class="sxs-lookup"><span data-stu-id="1f91f-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="1f91f-126">Klikk **Ny**, og velg deretter typen utdrag du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="1f91f-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="1f91f-127">Felt på siden **Utdrag** og handlinger under **Utdragsgruppe** på siden viser relevante data og handlinger basert på den valgte utdragstypen.</span><span class="sxs-lookup"><span data-stu-id="1f91f-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
