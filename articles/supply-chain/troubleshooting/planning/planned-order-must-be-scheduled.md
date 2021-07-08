---
title: Planlagt produksjonsordre må planlegges før det kan autoriseres
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at ordren må planlegges før den kan autoriseres.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294150"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="c00ee-103">Planlagt produksjonsordre må planlegges før det kan autoriseres</span><span class="sxs-lookup"><span data-stu-id="c00ee-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="c00ee-104">Feilkode: SYS309802</span><span class="sxs-lookup"><span data-stu-id="c00ee-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="c00ee-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="c00ee-105">Symptoms</span></span>

<span data-ttu-id="c00ee-106">Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="c00ee-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="c00ee-107">Den planlagte produksjonsordren må planlegges før den kan autoriseres.</span><span class="sxs-lookup"><span data-stu-id="c00ee-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="c00ee-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="c00ee-108">Cause</span></span>

<span data-ttu-id="c00ee-109">De planlagte start- og sluttdatoene kan ikke være tomme.</span><span class="sxs-lookup"><span data-stu-id="c00ee-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="c00ee-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="c00ee-110">Resolution</span></span>

<span data-ttu-id="c00ee-111">Følg denne fremgangsmåten for å angi start- og sluttdato for den planlagte bestillingen.</span><span class="sxs-lookup"><span data-stu-id="c00ee-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="c00ee-112">Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="c00ee-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="c00ee-113">Åpne den planlagte ordren.</span><span class="sxs-lookup"><span data-stu-id="c00ee-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="c00ee-114">Angi datoer i feltene **Startdato** og **Sluttdato** i hurtigfanen **Generelt** i delen **Planlagt**.</span><span class="sxs-lookup"><span data-stu-id="c00ee-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
