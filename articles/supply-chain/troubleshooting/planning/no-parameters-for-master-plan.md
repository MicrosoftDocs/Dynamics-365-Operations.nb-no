---
title: Parametere for hovedplanen finnes ikke
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at det ikke finnes parametere for hovedplanen.
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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294148"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="de9f0-103">Parametere for hovedplanen finnes ikke</span><span class="sxs-lookup"><span data-stu-id="de9f0-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="de9f0-104">Feilkode: SYS25368</span><span class="sxs-lookup"><span data-stu-id="de9f0-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="de9f0-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="de9f0-105">Symptoms</span></span>

<span data-ttu-id="de9f0-106">Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="de9f0-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="de9f0-107">Parametere for hovedplanen %1 finnes ikke.</span><span class="sxs-lookup"><span data-stu-id="de9f0-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="de9f0-108">Årsak</span><span class="sxs-lookup"><span data-stu-id="de9f0-108">Cause</span></span>

<span data-ttu-id="de9f0-109">På grunn av konfigurasjonsproblemer finner ikke systemet innstillingene for den angitte planen.</span><span class="sxs-lookup"><span data-stu-id="de9f0-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="de9f0-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="de9f0-110">Resolution</span></span>

- <span data-ttu-id="de9f0-111">Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**, og kontroller at det finnes en plan som har det angitte navnet.</span><span class="sxs-lookup"><span data-stu-id="de9f0-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
