---
title: Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk
description: Dette emnet beskriver noen av implementeringsavgjørelsene du bør ta hensyn til når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 36e0af4f1b4fa0013490a2acc2bfcac0de05f5dd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185342"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="f5e5a-103">Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk</span><span class="sxs-lookup"><span data-stu-id="f5e5a-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5e5a-104">Dette emnet beskriver noen av implementeringsavgjørelsene du bør ta hensyn til når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="f5e5a-105">Finansdimensjoner og hovedkontoer er nøkkelkomponentene i planleggingsfasen for en implementering.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="f5e5a-106">Når finansdimensjoner og hovedkontoer er opprettet i systemet, blir de brukt på sidene **Konfigurer kontostrukturer**, **Avanserte regelstrukturer** og **Konfigurasjon av finansdimensjoner for programintegrering**.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="f5e5a-107">Rekkefølgen som er definert på disse sidene, brukes til dataregistrering og forbruk i systemet.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="f5e5a-108">Noen steder i systemet vises finansdimensjonen og hovedkontoene i separate felt.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="f5e5a-109">Andre steder, for eksempel i journaler, vises imidlertid finansdimensjoner og hovedkontoer som en enkelt streng.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="f5e5a-110">Anbefalte fremgangsmåter for definering av finansdimensjoner og hovedkontoer i et høyre-mot-venstre-system</span><span class="sxs-lookup"><span data-stu-id="f5e5a-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="f5e5a-111">Når du velger skilletegn for kontoplaner, velger du ett av alternativene for dobbel skilletegn: doble bindestrek (-), dobbel strek (|) eller doble punktum (..) eller dobbel understreking (\_\_).</span><span class="sxs-lookup"><span data-stu-id="f5e5a-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="f5e5a-112">Når du oppretter finansdimensjons- og hovedkontoverdier, kan du bare bruke tall og tegn for høyre-mot-venstre-språk.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="f5e5a-113">Unngå å bruke det valgte skilletegnet for kontoplanen i finansdimensjons- og hovedkontoverdier.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="f5e5a-114">Ved å følge disse anbefalte fremgangsmåtene, kan du hjelpe å garantere konsekvent presentasjon av den brukerdefinerte ordren i hele systemet.</span><span class="sxs-lookup"><span data-stu-id="f5e5a-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>



