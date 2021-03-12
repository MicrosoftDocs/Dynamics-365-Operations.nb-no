---
title: Definere en betalingsmåte for ISO20022-avtalegiro
description: Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2cd5c174b0f3e3e15678513cecade020705beda
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982135"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="4a8c8-103">Definere en betalingsmåte for ISO20022-avtalegiro</span><span class="sxs-lookup"><span data-stu-id="4a8c8-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a8c8-104">Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="4a8c8-105">Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og betalingskontoer.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="4a8c8-106">Denne fremgangsmåten ble opprettet med demonstrasjonsdatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="4a8c8-107">Dette er den tredje av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="4a8c8-108">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="4a8c8-109">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4a8c8-110">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="4a8c8-111">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="4a8c8-111">Click Edit.</span></span>
4. <span data-ttu-id="4a8c8-112">Angi verdiene DEMF OPER i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="4a8c8-113">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="4a8c8-114">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="4a8c8-115">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="4a8c8-116">I listen velger du ISO20022-avtalegiro (DE).</span><span class="sxs-lookup"><span data-stu-id="4a8c8-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="4a8c8-117">Hvis listen er tom, er ikke konfigurasjonen for eksportformater for kundebetaling importert og aktiv.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="4a8c8-118">I feltet Krever mandat velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="4a8c8-119">Velg parameteren Krever mandat for kundebetalingsformater, som krever at mandatinformasjon tas med i betalingsmeldingen, som SEPA-avtalegiro.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="4a8c8-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4a8c8-120">Click Save.</span></span>

