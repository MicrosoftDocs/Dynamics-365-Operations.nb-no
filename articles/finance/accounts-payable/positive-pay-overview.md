---
title: Oversikt over positiv betaling
description: Denne artikkelen inneholder informasjon om positiv betaling, som brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49fe8369fce599d16134541b1c968727f38ebff9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189643"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="ac8f4-103">Oversikt over positiv betaling</span><span class="sxs-lookup"><span data-stu-id="ac8f4-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac8f4-104">Denne artikkelen inneholder informasjon om positiv betaling, som brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="ac8f4-105">Positiv betaling brukes til å generere en elektronisk liste over kontroller som kan leveres til en bank.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="ac8f4-106">Positive betalingsfiler kan hjelpe banker med å forhindre sjekksvindel.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="ac8f4-107">Du definerer positiv betaling for å generere en elektronisk liste over sjekker hver gang det skrives ut sjekker.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="ac8f4-108">Når en sjekk mottas av banken, sammenligner banken sjekken med listen over sjekker som du sendte tidligere.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="ac8f4-109">Hvis sjekken samsvarer med en sjekk i listen, betales sjekken av banken.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="ac8f4-110">Hvis sjekken ikke samsvarer med en sjekk i listen, beholder banken sjekken til gjennomgang.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="ac8f4-111">Positiv betaling er også kjent som SafePay.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="ac8f4-112">Positive betalingsfiler kan inneholde sensitiv informasjon om betalingsmottakere og sjekkbeløp.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="ac8f4-113">Derfor må du sørge for at du bruker riktige sikkerhetstiltak fra tidspunktet som filene er generert, til de er mottatt av banken.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="ac8f4-114">Positive betalingsfiler blir lastet ned i henhold til nedlastingsinstruksjonene for nettleseren.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="ac8f4-115">Positive betalingsfiler opprettes ved hjelp av dataenheter.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="ac8f4-116">Før du genererer en positiv betalingsfil, må du definere transformasjonsformatene for XML som oversetter dataene til et format som banken kan bruke.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="ac8f4-117">For hver bankkonto du vil generere informasjon om positiv betaling for, må du tilordne det positive betalingsformatetl.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="ac8f4-118">Når du har generert betalinger, kan du generere en positiv betalingsfil for én juridisk enhet og én bankkonto.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="ac8f4-119">Du kan også generere positive betalingsfiler for flere juridiske enheter og bankkontoer samtidig.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="ac8f4-120">Når kontrollene som er oppført i en positiv lønnsfilen er betalt, får du et bekreftelsesnummer fra banken.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="ac8f4-121">Du kan deretter bekrefte den positive lønnsfilen i systemet.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="ac8f4-122">Hvis du må endre en positiv betalingsfil, kan du tilbakekalle den.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="ac8f4-123">For hver kontroll i den positive betalingsfilen tilbakestilles deretter feltet som angir om kontrollen er inkludert i en positiv betalingsfil.</span><span class="sxs-lookup"><span data-stu-id="ac8f4-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="ac8f4-124">Hvis du vil ha mer informasjon, kan du se [Definere og generere positive betalingsfiler](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="ac8f4-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



