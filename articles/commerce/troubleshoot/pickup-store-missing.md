---
title: Detaljhandelsbutikk vises ikke i listen over butikker å hente fra
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en detaljhandel ikke vises i listen over butikker der varer kan hentes.
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
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020833"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="07041-103">Detaljhandelsbutikk vises ikke i listen over butikker å hente fra</span><span class="sxs-lookup"><span data-stu-id="07041-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07041-104">Dette emnet inneholder feilsøkingsveiledning som kan hjelpe når en detaljhandel ikke vises i listen over butikker der varer kan hentes.</span><span class="sxs-lookup"><span data-stu-id="07041-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="07041-105">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="07041-105">Description</span></span>

<span data-ttu-id="07041-106">En butikk vises ikke i listen over butikker der varer kan hentes.</span><span class="sxs-lookup"><span data-stu-id="07041-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="07041-107">Oppløsning</span><span class="sxs-lookup"><span data-stu-id="07041-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="07041-108">Konfigurere lengde- og breddegrad for butikkadressen i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="07041-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="07041-109">Hvis du vil konfigurere lengde- og breddegrad for butikkadressen i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="07041-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="07041-110">Gå til **Detaljhandel og handel \> Kanaler \> Butikker \> Alle butikker**.</span><span class="sxs-lookup"><span data-stu-id="07041-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="07041-111">Finn butikken du vil skal vises blant hentealternativene på e-handelsområdet.</span><span class="sxs-lookup"><span data-stu-id="07041-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="07041-112">Noter deg verdien for **Driftsenhetsnummer**.</span><span class="sxs-lookup"><span data-stu-id="07041-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="07041-113">Gå til **Organisasjonsstyring \> Organisasjoner \> Driftsenheter**.</span><span class="sxs-lookup"><span data-stu-id="07041-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="07041-114">Søk etter operasjonsnummeret du noterte deg tidligere, og velg deretter driftsenheten i søkeresultatene.</span><span class="sxs-lookup"><span data-stu-id="07041-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="07041-115">Velg **Flere alternativer** i hurtigfanen **Adresser**, og velg deretter **Avansert**.</span><span class="sxs-lookup"><span data-stu-id="07041-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="07041-116">Kontroller at faltene **Lengdegrad** og **Breddegrad** er riktig angitt i hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="07041-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="07041-117">Som et ledd i dette trinnet må du kontrollere at verdiene er riktig angitt som positive eller negative tall.</span><span class="sxs-lookup"><span data-stu-id="07041-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="07041-118">Konfigurere oppfyllelsesgrupper i Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="07041-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="07041-119">Hvis du vil konfigurere oppfyllelsesgrupper i Commerce Headquarters, gjør du følgende.</span><span class="sxs-lookup"><span data-stu-id="07041-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="07041-120">Gå til **Detaljhandel og handel \> Kanaler \> Nettbutikker**.</span><span class="sxs-lookup"><span data-stu-id="07041-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="07041-121">Velg nettbutikken du vil konfigurere.</span><span class="sxs-lookup"><span data-stu-id="07041-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="07041-122">Velg **Konfigurer** i handlingsruten, og velg deretter **Tilordning for oppfyllelsesgruppe**.</span><span class="sxs-lookup"><span data-stu-id="07041-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="07041-123">På siden **Tilordning for oppfyllelsesgruppe** velger du oppfyllelsesgruppen for nettbutikken.</span><span class="sxs-lookup"><span data-stu-id="07041-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="07041-124">Under **Oppsett** kontrollerer du at detaljhandelen er riktig konfigurert for oppfyllelsesgruppen.</span><span class="sxs-lookup"><span data-stu-id="07041-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07041-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="07041-125">Additional resources</span></span> 

[<span data-ttu-id="07041-126">Opprette en driftsenhet</span><span class="sxs-lookup"><span data-stu-id="07041-126">Create an operating unit</span></span>](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[<span data-ttu-id="07041-127">Konfigurere en nettkanal</span><span class="sxs-lookup"><span data-stu-id="07041-127">Set up an online channel</span></span>](../channel-setup-online.md)