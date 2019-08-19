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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848653"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="ffed2-103">Definere en betalingsmåte for ISO20022-avtalegiro</span><span class="sxs-lookup"><span data-stu-id="ffed2-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ffed2-104">Denne fremgangsmåten viser hvordan du setter opp kundebetalingsmåten for ISO20022-avtalegiro eller andre betalingsmåter ved hjelp av elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ffed2-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="ffed2-105">Før du fullfører denne oppgaven, må du definere eksportformatkonfigurasjoner og betalingskontoer.</span><span class="sxs-lookup"><span data-stu-id="ffed2-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="ffed2-106">Denne fremgangsmåten ble opprettet med demonstrasjonsdatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="ffed2-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="ffed2-107">Dette er den tredje av fem prosedyrer, som viser kundebetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ffed2-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="ffed2-108">Gå til Kunder > Betalingsoppsett > Betalingsmåter.</span><span class="sxs-lookup"><span data-stu-id="ffed2-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="ffed2-109">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="ffed2-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ffed2-110">Du kan for eksempel filtrere på Betalingsmåte-feltet med verdien ELEKTRONISK.</span><span class="sxs-lookup"><span data-stu-id="ffed2-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="ffed2-111">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="ffed2-111">Click Edit.</span></span>
4. <span data-ttu-id="ffed2-112">Angi verdiene DEMF OPER i feltet Betalingskonto.</span><span class="sxs-lookup"><span data-stu-id="ffed2-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="ffed2-113">Vis delen Filformater.</span><span class="sxs-lookup"><span data-stu-id="ffed2-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="ffed2-114">Velg Ja i feltet Generell elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ffed2-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="ffed2-115">Angi eller velg en verdi i feltet Eksportformatkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="ffed2-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="ffed2-116">I listen velger du ISO20022-avtalegiro (DE).</span><span class="sxs-lookup"><span data-stu-id="ffed2-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="ffed2-117">Hvis listen er tom, er ikke konfigurasjonen for eksportformater for kundebetaling importert og aktiv.</span><span class="sxs-lookup"><span data-stu-id="ffed2-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="ffed2-118">I feltet Krever mandat velger du Ja.</span><span class="sxs-lookup"><span data-stu-id="ffed2-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="ffed2-119">Velg parameteren Krever mandat for kundebetalingsformater, som krever at mandatinformasjon tas med i betalingsmeldingen, som SEPA-avtalegiro.</span><span class="sxs-lookup"><span data-stu-id="ffed2-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="ffed2-120">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ffed2-120">Click Save.</span></span>

