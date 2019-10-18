---
title: Rapporter for utsalgspris
description: Dette emnet gir en oversikt over prisrapportfunksjonen, som kan brukes til å vise kommende prisendringer for assorterte produkter.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 4fb02bdeca2d71d84ebdddfd16d471a532823e42
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025201"
---
# <a name="retail-price-reports"></a><span data-ttu-id="d7975-103">Rapporter for utsalgspris</span><span class="sxs-lookup"><span data-stu-id="d7975-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="d7975-104">Hvis du vil gi konkurransedyktige priser til kundene, endrer forhandlerne ofte priser på varer.</span><span class="sxs-lookup"><span data-stu-id="d7975-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="d7975-105">Butikksjefer ønsker muligheten til å få enkel tilgang til nylige eller kommende priser, slik at de kan planlegge de nødvendige ressursene for å oppdatere prisetikettene som vises på butikkhyllene.</span><span class="sxs-lookup"><span data-stu-id="d7975-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="d7975-106">Med frigivelse 10.0 av Retail kan en butikksjef åpne **Pris**-rapporten ved å gå til **Alle detaljhandelbutikker \> Butikk \> Prisrapport** og vise de oppdaterte prisene for produktene som er knyttet til butikken.</span><span class="sxs-lookup"><span data-stu-id="d7975-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All retail stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="d7975-107">For å aktivere rapporten må parameteren **Aktiver prisrapport for detaljhandelbutikk** være aktivert.</span><span class="sxs-lookup"><span data-stu-id="d7975-107">To enable the price report, the **Enable price report for Retail store** parameter must be turned on.</span></span> <span data-ttu-id="d7975-108">Denne parameteren ligger i fanen **Detaljhandelsparametere \> Rabatter \> Diverse**. Ved å åpne siden **Prisrapport** vises en dialogboks med forskjellige konfigurasjoner.</span><span class="sxs-lookup"><span data-stu-id="d7975-108">This parameter is located on the **Retail parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="d7975-109">De tilgjengelige konfigurasjonene vises nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d7975-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="d7975-110">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="d7975-110">Configuration</span></span> | <span data-ttu-id="d7975-111">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d7975-111">Description</span></span> |
|---|---|
| <span data-ttu-id="d7975-112">Fra dato / Til dato</span><span class="sxs-lookup"><span data-stu-id="d7975-112">From date / To date</span></span>| <span data-ttu-id="d7975-113">Datointervallet som prisrapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="d7975-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="d7975-114">Varigheten er for øyeblikket begrenset til 7 dager.</span><span class="sxs-lookup"><span data-stu-id="d7975-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="d7975-115">Kanal</span><span class="sxs-lookup"><span data-stu-id="d7975-115">Channel</span></span>| <span data-ttu-id="d7975-116">Detaljhandelsbutikken som prisrapporten skal genereres for.</span><span class="sxs-lookup"><span data-stu-id="d7975-116">The retail store for which the price report should be generated.</span></span> |
| <span data-ttu-id="d7975-117">Vis produkter med tilgjengelig beholdning</span><span class="sxs-lookup"><span data-stu-id="d7975-117">Display products with available inventory</span></span>| <span data-ttu-id="d7975-118">Hvis du setter dette til **Ja**, vises priser for bare produktene som for øyeblikket har fysisk beholdning tilgjengelig i lageret.</span><span class="sxs-lookup"><span data-stu-id="d7975-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="d7975-119">Vis priser for varianter</span><span class="sxs-lookup"><span data-stu-id="d7975-119">Display prices for variants</span></span> | <span data-ttu-id="d7975-120">Hvis du setter dette til **Ja**, vises priser for variantene sammen med produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="d7975-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="d7975-121">Dette bør bare settes til **På** hvis du har variantspesifikke priser, ettersom antall rader blir svært stor.</span><span class="sxs-lookup"><span data-stu-id="d7975-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="d7975-122">I fremtidige versjoner vil vi aktivere de dimensjonsbaserte prisene, slik at butikksjefen kan velge dimensjonene som prisene skal vises for.</span><span class="sxs-lookup"><span data-stu-id="d7975-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="d7975-123">Vis produkter med prisendringer</span><span class="sxs-lookup"><span data-stu-id="d7975-123">Display products with price changes</span></span> | <span data-ttu-id="d7975-124">Hvis du setter dette til **Ja**, vises prisene bare for datoene da prisen ble endret.</span><span class="sxs-lookup"><span data-stu-id="d7975-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="d7975-125">Prisen for *én dag før* den valgte **Fra dato** vises alltid, slik at butikksjefen enkelt kan identifisere produktene som ikke har endret pris for den valgte varigheten, og også kan vise den gjeldende prisen.</span><span class="sxs-lookup"><span data-stu-id="d7975-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="d7975-126">Når rapporten er generert, kan Excel-filen lastes ned for eventuelle ekstra filtreringsbehov.</span><span class="sxs-lookup"><span data-stu-id="d7975-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="d7975-127">Prisrapporten kan også brukes til å kontrollere de historiske prisene for produkter for tidligere datoer.</span><span class="sxs-lookup"><span data-stu-id="d7975-127">The price report can also be used to check the historical prices of products for past dates.</span></span>
