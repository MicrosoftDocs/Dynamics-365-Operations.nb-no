---
title: Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner
description: Dette emnet beskriver den fordelte, feedbaserte ordreopprettingen for detaljhandelstransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004280"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="5b07e-103">Fordele feedbasert ordreoppretting for detaljhandelstransaksjoner (offentlig forhåndsvisning)</span><span class="sxs-lookup"><span data-stu-id="5b07e-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="5b07e-104">I Dynamics 365 Retail versjon 10.0.4 og tidligere er postering av utdrag en operasjon på slutten av dagen, og alle transaksjoner posteres i bøkene på slutten av dagen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="5b07e-105">Store transaksjoner må deretter behandles i et begrenset tidsvindu, noe som noen ganger kan føre til belastning og låsing og feil i utdragsposteringen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="5b07e-106">Forhandlere kan heller ikke føre inntekter og betalinger i sine bøker gjennom hele dagen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="5b07e-107">Med offentlig forhåndsvisning av fordeling av feedbasert ordreoppretting, som ble innført i Retail versjon 10.0.5, behandles transaksjoner gjennom hele dagen, og bare finansavstemmingen for betalingsmidler og andre kassastyringstransaksjoner behandles på slutten av dagen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="5b07e-108">Denne funksjonen deler belastningen med å opprette salgsordrer, fakturaer og betalinger gjennom hele dagen, noe som gir bedre ytelse og muligheten til å føre inntekter og betalinger i de andre bøkene i nærheten av sanntid.</span><span class="sxs-lookup"><span data-stu-id="5b07e-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="5b07e-109">Bruke fordeling av feedbasert postering</span><span class="sxs-lookup"><span data-stu-id="5b07e-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="5b07e-110">Hvis du vil aktivere fordeling av feedbasert postering for transaksjoner, går du til **Systemadministrasjon > Oppsett > Lisenskonfigurasjon** og deaktiverer nøkkelen **Utdrag**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="5b07e-111">På samme side aktiverer du lisensnøkkelen **Utdrag (fordelingsfeed) – forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="5b07e-112">Når du aktiverer denne nøkkelen, må du kontrollere at det ikke finnes ventende utdrag som venter på å bli postert.</span><span class="sxs-lookup"><span data-stu-id="5b07e-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="5b07e-113">Før du aktiverer lisensnøkkelen **Utdrag (fordelingsfeed) – forhåndsvisning**, må du kontrollere at ingen ventende utdrag venter på å bli postert.</span><span class="sxs-lookup"><span data-stu-id="5b07e-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="5b07e-114">Gjeldende utdragsdokument blir delt inn i to forskjellige typer: transaksjonsutdrag og regnskapsoppgjør.</span><span class="sxs-lookup"><span data-stu-id="5b07e-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="5b07e-115">Transaksjonsoppgaven vil plukke opp alle uposterte og godkjente transaksjoner, og opprette salgsordrer, salgsfakturaer, betalings- og rabattjournaler og transaksjoner for inntekter/utgifter med det intervallet du konfigurerer.</span><span class="sxs-lookup"><span data-stu-id="5b07e-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="5b07e-116">Du bør konfigurere denne prosessen til å kjøre med høy frekvens, slik at dokumenter opprettes når transaksjonene lastes opp til Headquarters via P-jobben.</span><span class="sxs-lookup"><span data-stu-id="5b07e-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="5b07e-117">Med transaksjonsutdraget som allerede oppretter salgsordrer og salgsfakturaer, er det ikke noe reelt behov for å konfigurere den satsvise jobben **Poster lager**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="5b07e-118">Du kan imidlertid fortsatt bruke den til å oppfylle bestemte forretningskrav som du kanskje har.</span><span class="sxs-lookup"><span data-stu-id="5b07e-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="5b07e-119">Regnskapsoppgjøret er utformet til å opprettes på slutten av dagen, og støtter bare avsluttingsmetoden **Skift**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="5b07e-120">Dette utdraget vil være begrenset til økonomisk avstemming, og vil bare opprette journaler for de ulike beholdningsbeløpene mellom telt beløp og transaksjonsbeløp for de forskjellige anleggsmidlene, sammen med journaler for andre kontantstyringstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5b07e-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="5b07e-121">Hvis du vil beregne transaksjonsutdraget, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn transaksjonsutdrag satsvis**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="5b07e-122">Hvis du vil postere transaksjonsutdrag satsvis, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster transaksjonsutdrag satsvis**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="5b07e-123">Hvis du vil beregne regnskapsoppgjøret, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn regnskapsoppgjør satsvis**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="5b07e-124">Hvis du vil postere regnskapsoppgjøret satsvis, klikker du **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster regnskapsoppgjør satsvis**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="5b07e-125">Menyelementene **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Beregn utdrag satsvis** og **Detaljhandel og handel > IT for Detaljhandel og handel > Salgsstedspostering > Poster utdrag satsvis** blir fjernet med denne nye funksjonen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="5b07e-126">Du kan også opprette typer transaksjons- og regnskapsoppgjør manuelt.</span><span class="sxs-lookup"><span data-stu-id="5b07e-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="5b07e-127">Gå til **Detaljhandel og handel > Kanaler > Butikker** og klikk **Utdrag**.</span><span class="sxs-lookup"><span data-stu-id="5b07e-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="5b07e-128">Klikk **Ny**, og velg deretter typen utdrag du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="5b07e-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="5b07e-129">Felt på siden **Utdrag** og handlinger under **Utdragsgruppe** på siden viser relevante data og handlinger basert på den valgte utdragstypen.</span><span class="sxs-lookup"><span data-stu-id="5b07e-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
