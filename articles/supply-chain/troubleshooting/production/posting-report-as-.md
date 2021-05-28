---
title: Feil når Ferdigmeldingsjournalen er postert
description: Når du posterer ferdigmeldingsjournalen, får du en feilmelding som angir at det bestilte antallet ikke kan reduseres.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026768"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="403fc-103">Feil når Ferdigmeldingsjournalen er postert</span><span class="sxs-lookup"><span data-stu-id="403fc-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="403fc-104">KB-nummer: 4612891</span><span class="sxs-lookup"><span data-stu-id="403fc-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="403fc-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="403fc-105">Symptoms</span></span>

<span data-ttu-id="403fc-106">Når du posterer **Ferdigmeld**-journalen, oppstår det en feil, og du får følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="403fc-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="403fc-107">Det bestilte antallet kan ikke settes ned siden det ikke finnes nok åpne lagertransaksjoner med status Bestilt.</span><span class="sxs-lookup"><span data-stu-id="403fc-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="403fc-108">Varene er kjøpt, mottatt eller registrert.</span><span class="sxs-lookup"><span data-stu-id="403fc-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="403fc-109">Denne feilen oppstår bare når feltet **Antall feil** er angitt på den første linjen i **Ferdigmeld**-journalen og feltet **Antall korrekte** er angitt på den siste linjen.</span><span class="sxs-lookup"><span data-stu-id="403fc-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="403fc-110">Hvis feltet **Antall feil** er angitt på den siste linjen, oppstår det ingen feil.</span><span class="sxs-lookup"><span data-stu-id="403fc-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="403fc-111">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="403fc-111">Resolution</span></span>

<span data-ttu-id="403fc-112">Hvis du vil hindre denne feilen, åpner du siden **Parametere for produksjonskontroll**, og i kategorien **Generelt** angir du alternativet for **Øk gjenværende antall med feilantall** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="403fc-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
