---
title: Tilbakeføring av ferdigmeldinger oppretter en uventet åpen transaksjon
description: Tilbakeføring av ferdigmeldte varer som har merking, oppretter en åpen transaksjon der det tilbakeførte antallet har de samme lagerdimensjonene som den tilbakeførte transaksjonen.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026791"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="a6202-103">Tilbakeføring av ferdigmeldinger oppretter en uventet åpen transaksjon</span><span class="sxs-lookup"><span data-stu-id="a6202-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="a6202-104">KB-nummer: 4612469</span><span class="sxs-lookup"><span data-stu-id="a6202-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="a6202-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="a6202-105">Symptoms</span></span>

<span data-ttu-id="a6202-106">Hvis du tilbakefører ferdigmeldte varer som har merking, oppretter systemet en åpen transaksjon der det tilbakeførte antallet har de samme lagerdimensjonene som den tilbakeførte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a6202-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="a6202-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="a6202-107">Resolution</span></span>

<span data-ttu-id="a6202-108">Når du tilbakefører en ferdigmeldingsoperasjon, initialiseres lagerdimensjonen fra produksjonsjournalen.</span><span class="sxs-lookup"><span data-stu-id="a6202-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="a6202-109">Derfor hentes partinummeret.</span><span class="sxs-lookup"><span data-stu-id="a6202-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="a6202-110">På grunn av merking vil salgsordretransaksjonene arve partinummeret.</span><span class="sxs-lookup"><span data-stu-id="a6202-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="a6202-111">Dimensjonen kan tilbakestilles når ferdigmeldingen posteres.</span><span class="sxs-lookup"><span data-stu-id="a6202-111">The dimension can be reset when the reporting as finished is posted.</span></span>
