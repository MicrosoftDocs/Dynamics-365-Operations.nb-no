---
title: Purringer og importinkassoer
description: Denne artikkelen inneholder generell informasjon om purringer og importsamlinger. Begge typer bankdokument brukes ofte til kjøp og salg av varer på tvers av internasjonale grenser.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: roschlom
ms.custom: 18321
ms.assetid: 5c97ab81-632b-4043-a940-674bcb496c80
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45eed711ace1534df462a21d0f37bdfaa09e6392
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253945"
---
# <a name="letters-of-credit-and-import-collections"></a><span data-ttu-id="520c5-104">Purringer og importinkassoer</span><span class="sxs-lookup"><span data-stu-id="520c5-104">Letters of credit and import collections</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="520c5-105">Denne artikkelen inneholder generell informasjon om purringer og importsamlinger.</span><span class="sxs-lookup"><span data-stu-id="520c5-105">This article provides general information about letters of credit and import collections.</span></span> <span data-ttu-id="520c5-106">Begge typer bankdokument brukes ofte til kjøp og salg av varer på tvers av internasjonale grenser.</span><span class="sxs-lookup"><span data-stu-id="520c5-106">Both types of bank document are often used for the purchase and sale of goods across international borders.</span></span>

<a name="letters-of-credit"></a><span data-ttu-id="520c5-107">Purringer</span><span class="sxs-lookup"><span data-stu-id="520c5-107">Letters of credit</span></span>
-----------------

<span data-ttu-id="520c5-108">Remburser brukes i internasjonale transaksjoner og bidrar til å garantere at betalinger blir foretatt.</span><span class="sxs-lookup"><span data-stu-id="520c5-108">Letters of credit are used for international transactions and help guarantee that payments will be made.</span></span> <span data-ttu-id="520c5-109">En remburs er en avtale som utstedes av en bank, der banken godtar å garantere betaling på vegne av en kjøper, så lenge vilkårene i avtalen mellom kjøper og selger er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="520c5-109">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to guarantee payment on behalf of a buyer, provided that the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="520c5-110">En remburs også omtales som en vareremburs eller bankremburs.</span><span class="sxs-lookup"><span data-stu-id="520c5-110">A letter of credit is also referred to as a documentary credit (DC).</span></span>

<span data-ttu-id="520c5-111">Når det gjelder en importremburs, er den juridiske enheten kjøperen eller søkeren for rembursen.</span><span class="sxs-lookup"><span data-stu-id="520c5-111">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="520c5-112">Når det gjelder en eksportremburs, er den juridiske enheten selgeren eller mottakeren av rembursen.</span><span class="sxs-lookup"><span data-stu-id="520c5-112">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="520c5-113">Følgende parter er involvert i en remburs:</span><span class="sxs-lookup"><span data-stu-id="520c5-113">The following parties are involved in a letter of credit:</span></span>

-   <span data-ttu-id="520c5-114">Søkeren (kjøperen) som har til hensikt å betale for varene</span><span class="sxs-lookup"><span data-stu-id="520c5-114">The applicant (buyer) who intends to pay for the goods</span></span>
-   <span data-ttu-id="520c5-115">Mottakeren (selgeren) som skal motta betalingen</span><span class="sxs-lookup"><span data-stu-id="520c5-115">The beneficiary (seller) who will receive the payment</span></span>
-   <span data-ttu-id="520c5-116">Den utstedende banken som utsteder rembursen</span><span class="sxs-lookup"><span data-stu-id="520c5-116">The issuing bank that issues the letter of credit</span></span>
-   <span data-ttu-id="520c5-117">Advisbanken som utfører transaksjonen på vegne av søkeren</span><span class="sxs-lookup"><span data-stu-id="520c5-117">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="520c5-118">Rembursen inneholder en beskrivelse av varene, eventuelle påkrevde dokumenter, forsendelsesdatoen og utløpsdatoen som betaling ikke foretas etter.</span><span class="sxs-lookup"><span data-stu-id="520c5-118">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment won't be made.</span></span> <span data-ttu-id="520c5-119">Den utstedende banken får en margin for rembursen.</span><span class="sxs-lookup"><span data-stu-id="520c5-119">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="520c5-120">En remburs kan enten være **gjenkallelig** eller **ugjenkallelig**.</span><span class="sxs-lookup"><span data-stu-id="520c5-120">A letter of credit can be **revocable** or **irrevocable**.</span></span> <span data-ttu-id="520c5-121">En remburs kan være **overførbar**, **ikke overførbar** eller **rullerende**.</span><span class="sxs-lookup"><span data-stu-id="520c5-121">The nature of a letter of credit can be **transferable**, **non-transferable**, or **revolving**.</span></span> <span data-ttu-id="520c5-122">En remburs er vanligvis en ugjenkallelig og bekreftet avtale om at betaling blir foretatt til en bestemt mottaker når komplett og nøyaktig forsendelsesdokumentasjon er sendt.</span><span class="sxs-lookup"><span data-stu-id="520c5-122">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

## <a name="import-collections"></a><span data-ttu-id="520c5-123">Importinkassoer</span><span class="sxs-lookup"><span data-stu-id="520c5-123">Import collections</span></span>
<span data-ttu-id="520c5-124">En importinkasso er en avtale mellom banken og eksportøren (selgeren) der banken avtaler å levere forsendelsesdokumentasjonen til den internasjonale importøren (kjøperen).</span><span class="sxs-lookup"><span data-stu-id="520c5-124">An import collection is an agreement between the bank and the exporter (seller), in which the bank agrees to deliver the shipping documentation to the international importer (buyer).</span></span> <span data-ttu-id="520c5-125">Banken forventes å levere forsendelsesdokumentasjonen ved mottak av kontant betaling for de sendte varene, eller ved mottak av en signert anvisning mot betalingen.</span><span class="sxs-lookup"><span data-stu-id="520c5-125">The bank is expected to deliver the shipping documentation upon receipt of payment for the shipped goods in cash, or upon receipt of a signed draft toward the payment.</span></span> 

<span data-ttu-id="520c5-126">En importinkasso er med på å garantere at selgeren betales når kjøperen henter forsendelsesdokumentene for å motta de importerte varene.</span><span class="sxs-lookup"><span data-stu-id="520c5-126">An import collection helps guarantee that the seller is paid when the buyer collects the shipping documents to take delivery of the imported goods.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]