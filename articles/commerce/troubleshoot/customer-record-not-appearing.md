---
title: Kundeposter vises ikke i Commerce Headquarters
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når kundeposter ikke vises i Commerce Headquarters umiddelbart.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018488"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a><span data-ttu-id="25852-103">Kundeposter vises ikke i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="25852-103">Customer records don't appear in Commerce headquarters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25852-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når kundeposter ikke vises i Commerce Headquarters umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="25852-104">This topic provides troubleshooting guidance that can help when customer records don't immediately appear in Commerce headquarters.</span></span>

## <a name="description"></a><span data-ttu-id="25852-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="25852-105">Description</span></span>

<span data-ttu-id="25852-106">Når du oppretter en ny kundepost ved hjelp av registreringsflyten i e-handelbutikken, vises ikke den tilsvarende kundeposten umiddelbart i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="25852-106">When you create a new customer record by using the sign-up flow in the e-commerce storefront, the corresponding customer record doesn't immediately appear in Commerce headquarters.</span></span>

## <a name="resolution"></a><span data-ttu-id="25852-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="25852-107">Resolution</span></span>

### <a name="disable-customer-creation-in-async-mode"></a><span data-ttu-id="25852-108">Deaktivere kundeoppretting i Async-modus</span><span class="sxs-lookup"><span data-stu-id="25852-108">Disable customer creation in async mode</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25852-109">Hvis du deaktiverer oppretting av asynkron kunde, kan systemytelsen påvirkes, fordi oppretting av hver post vil føre til en forespørsel i sanntid til Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="25852-109">If you disable asynchronous customer creation, system performance could be affected, because creation of each record will produce a real-time request to Commerce headquarters.</span></span> <span data-ttu-id="25852-110">Hvis også Commerce Headquarters er nede (for eksempel under serviceflyt), vil det føre til feil hvis det opprettes nye flyter for kunde.</span><span class="sxs-lookup"><span data-stu-id="25852-110">In addition, if Commerce headquarters is down (for example, during servicing flows), any new customer creation flows will produce errors.</span></span>

<span data-ttu-id="25852-111">Følg denne fremgangsmåten for å deaktivere kundeoppretting i asynkron modus i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="25852-111">To disable customer creation in async mode in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="25852-112">Gå til **Detaljhandel og handel \> Kanaloppsett \> Oppsett av nettbutikk \> Funksjonsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="25852-112">Go to **Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="25852-113">Hvis du ikke allerede bruker en funksjonsprofil for den nettbaserte kanalen, kan du opprette en.</span><span class="sxs-lookup"><span data-stu-id="25852-113">If you aren't already using a functionality profile for your online channel, create one.</span></span>
1. <span data-ttu-id="25852-114">Kontroller at alternativet **Opprett kunde i async-modus** er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="25852-114">Make sure that the **Create customer in async mode** option is set to **No**.</span></span>
1. <span data-ttu-id="25852-115">Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.</span><span class="sxs-lookup"><span data-stu-id="25852-115">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="25852-116">Velg den elektroniske butikken du vil deaktivere oppretting av asynkron kunde for.</span><span class="sxs-lookup"><span data-stu-id="25852-116">Select the online store to disable asynchronous customer creation for.</span></span>
1. <span data-ttu-id="25852-117">I fanen **Generelt** kontrollerer du at feltet **Funksjonsprofil** er satt til funksjonsprofilen du bruker for den elektroniske kanalen.</span><span class="sxs-lookup"><span data-stu-id="25852-117">On the **General** tab, make sure that the **Functionality profile** field is set to the functionality profile that you're using for your online channel.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25852-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="25852-118">Additional resources</span></span>

[<span data-ttu-id="25852-119">Konfigurere en B2C-leier i Commerce</span><span class="sxs-lookup"><span data-stu-id="25852-119">Setup a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
