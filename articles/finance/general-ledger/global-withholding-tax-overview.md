---
title: Global kildeskatt
description: Dette emnet gir informasjon om global funksjonalitet for kildeskatt og hvordan du definerer det. Global kildeskattfunksjonalitet er utvidet for leverandør- og kundetransaksjoner, slik at kildeskatt beregnes på varenivå.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075744"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="00784-104">Global kildeskatt</span><span class="sxs-lookup"><span data-stu-id="00784-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00784-105">Dette emnet gir informasjon om global funksjonalitet for kildeskatt og forklarer hvordan du definerer det.</span><span class="sxs-lookup"><span data-stu-id="00784-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="00784-106">Den nye funksjonen er tilgjengelig i versjon 10.0.17 og senere.</span><span class="sxs-lookup"><span data-stu-id="00784-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="00784-107">Global kildeskattfunksjonalitet er utvidet for leverandør- og kundetransaksjoner, slik at kildeskatt beregnes på varenivå.</span><span class="sxs-lookup"><span data-stu-id="00784-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="00784-108">Saldoen på kildeskattkontoen fra kjøpstransaksjoner kan utlignes ved å kjøre betalingsjobben for kildeskatt mot utligningskontoen for kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="00784-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="00784-109">Global kildeskatt støtter ikke funksjonen **Vedlikehold tillegg** på bestillings-, leverandørfaktura- og salgsordresidene.</span><span class="sxs-lookup"><span data-stu-id="00784-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="00784-110">Slå på global kildeskatt</span><span class="sxs-lookup"><span data-stu-id="00784-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="00784-111">I **Funksjonsbehandling**-arbeidsområdet velger du **Global kildeskatt**, og deretter velger du **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="00784-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="00784-112">Gå til **Avgift \> Oppsett \> Parametere \> Parametere for økonomimodul** og deretter, i kategorien **Kildeskatt**, setter du alternativet **Aktiver global kildeskatt** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="00784-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="00784-113">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="00784-113">Select **Save**.</span></span>
4. <span data-ttu-id="00784-114">Oppdatere siden i webleseren.</span><span class="sxs-lookup"><span data-stu-id="00784-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="00784-115">Global kildeskattfunksjonalitet kan ikke aktiveres for land/områder der det allerede finnes lokale kildeskattløsninger.</span><span class="sxs-lookup"><span data-stu-id="00784-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="00784-116">Disse områdene omfatter, men er ikke begrenset til India, Brasil, Thailand, Saudi-Arabia, Irland, Storbritannia og USA.</span><span class="sxs-lookup"><span data-stu-id="00784-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
