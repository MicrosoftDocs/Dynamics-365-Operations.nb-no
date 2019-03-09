---
title: Korrigere en fritekstfaktura
description: Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "364609"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="885b3-103">Korrigere en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="885b3-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="885b3-104">Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura.</span><span class="sxs-lookup"><span data-stu-id="885b3-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="885b3-105">Hvis du vil rette en fritekstfaktura som allerede er postert, kan du åpne den posterte fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="885b3-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="885b3-106">På **Faktura**-siden velger du **Avbryt**, og velger deretter **Rett faktura**.</span><span class="sxs-lookup"><span data-stu-id="885b3-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="885b3-107">Velg en årsakskode, legg til kommentarer, og velg datoen for ny, korrigert faktura.</span><span class="sxs-lookup"><span data-stu-id="885b3-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="885b3-108">Du kan endre den rettede fakturaen og postere den.</span><span class="sxs-lookup"><span data-stu-id="885b3-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="885b3-109">Når du posterer den rettede fakturaen, opprettes en annulleringsfaktura for et kreditbeløp som er lik det opprinnelige fakturabeløpet.</span><span class="sxs-lookup"><span data-stu-id="885b3-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="885b3-110">Den kombinerte saldoen mellom den opprinnelige fakturaen og annulleringsfakturaen er derfor 0 (null).</span><span class="sxs-lookup"><span data-stu-id="885b3-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="885b3-111">Annulleringsfakturaen utlignes mot den opprinnelige fakturaen.</span><span class="sxs-lookup"><span data-stu-id="885b3-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="885b3-112">Når du posterer den rettede fakturaen, får du tre fakturaer:</span><span class="sxs-lookup"><span data-stu-id="885b3-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="885b3-113">**Opprinnelig faktura** – Fakturaen som inneholder informasjonen du retter.</span><span class="sxs-lookup"><span data-stu-id="885b3-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="885b3-114">**Annulleringsfaktura** – Den systemgenererte kreditfakturaen som ble opprettet for å annullere fakturaen som sist ble rettet.</span><span class="sxs-lookup"><span data-stu-id="885b3-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="885b3-115">**Rettet faktura** – Fakturaen som inneholder den rettede fakturainformasjonen.</span><span class="sxs-lookup"><span data-stu-id="885b3-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="885b3-116">Du kan identifisere annullerings- og korrigeringsfakturaer på to måter:</span><span class="sxs-lookup"><span data-stu-id="885b3-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="885b3-117">Siden **Alle fritekstfakturaer** inneholder en **Korrigering**-kolonne der du kan se hvilke fakturaer som er annulleringsfakturaer, og hvilke som er korrigeringsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="885b3-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="885b3-118">Toppteksten i fritekstfakturaen viser statusen **Annulleringsfaktura \[fakturanummeret\]** eller **Rettet faktura\[ fakturanummer\]**.</span><span class="sxs-lookup"><span data-stu-id="885b3-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="885b3-119">Denne funksjonen er bare tilgjengelig hvis konfigurasjonsnøkkelen **Korreksjon av fritekstfaktura** er valgt.</span><span class="sxs-lookup"><span data-stu-id="885b3-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>



