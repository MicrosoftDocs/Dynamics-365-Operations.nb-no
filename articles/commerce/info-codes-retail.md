---
title: Informasjonskoder og informasjonskodegrupper
description: Denne artikkelen gir en oversikt om informasjonskoder, informasjonskodegrupper og hvordan de brukes.
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 046204d36e2fc7a69129aaf7fe027b2abc7e8dd9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023615"
---
# <a name="info-codes-and-info-code-groups"></a><span data-ttu-id="65d4f-103">Informasjonskoder og informasjonskodegrupper</span><span class="sxs-lookup"><span data-stu-id="65d4f-103">Info codes and info code groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65d4f-104">Denne artikkelen gir en oversikt om informasjonskoder, informasjonskodegrupper og hvordan de brukes.</span><span class="sxs-lookup"><span data-stu-id="65d4f-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="65d4f-105">Informasjonskoder gjør det mulig å hente data på i en salgsstedskasse (POS).</span><span class="sxs-lookup"><span data-stu-id="65d4f-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="65d4f-106">Du kan bruke infokoder til å spørre kassereren om å angi informasjon i forskjellige handlinger på salgsstedet, for eksempel varesalg, retur av varer eller valg av kunder.</span><span class="sxs-lookup"><span data-stu-id="65d4f-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="65d4f-107">Kasserere kan velge inndata fra en liste eller angi dem som en kode, et nummer, en dato eller tekst.</span><span class="sxs-lookup"><span data-stu-id="65d4f-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="65d4f-108">Du kan tilordne informasjonskoder til forhåndsdefinerte butikkhandlinger, detaljvarer, betalingsmåter, kunder eller bestemte salgsstedsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="65d4f-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="65d4f-109">Du kan bruke informasjonskoder til å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="65d4f-109">You can use info codes to do the following:</span></span>

- <span data-ttu-id="65d4f-110">Hente tilleggsinformasjon på transaksjonstidspunktet, for eksempel et flightnummer eller årsaken til en retur.</span><span class="sxs-lookup"><span data-stu-id="65d4f-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
- <span data-ttu-id="65d4f-111">Be kassereren om å velge fra en prisliste for bestemte produkter.</span><span class="sxs-lookup"><span data-stu-id="65d4f-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
- <span data-ttu-id="65d4f-112">Koble en delkode til en informasjonskode som gjør at kassereren blir bedt om å angi inndata mens vedkommende utfører en bestemt aktivitet.</span><span class="sxs-lookup"><span data-stu-id="65d4f-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="65d4f-113">Når en kunde returnerer et produkt, kan du for eksempel be kassereren om å spørre hvorfor produktet returneres.</span><span class="sxs-lookup"><span data-stu-id="65d4f-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="65d4f-114">Du kan deretter bruke delkoder til å vise en liste over årsaker som kassereren kan velge blant.</span><span class="sxs-lookup"><span data-stu-id="65d4f-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
- <span data-ttu-id="65d4f-115">Selg et produkt som en vanlig salg, rabattert salg eller gratisprodukt.</span><span class="sxs-lookup"><span data-stu-id="65d4f-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
- <span data-ttu-id="65d4f-116">Be kasserere om å angi en verdi eller velge fra en liste over delkoder når de åpner kasseskuffen uten å utføre en salgsoperasjon.</span><span class="sxs-lookup"><span data-stu-id="65d4f-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="65d4f-117">Informasjonskodegruppe</span><span class="sxs-lookup"><span data-stu-id="65d4f-117">Info codes group</span></span>

<span data-ttu-id="65d4f-118">I Commerce kan du opprette grupper med informasjonskoder.</span><span class="sxs-lookup"><span data-stu-id="65d4f-118">In Commerce, you can create groups of info codes.</span></span> <span data-ttu-id="65d4f-119">Informasjonskodegrupper legger til fleksibilitet ved å la deg definere færre informasjonskoder og deretter bruke dem på mer fleksible måter.</span><span class="sxs-lookup"><span data-stu-id="65d4f-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="65d4f-120">Du kan bruke informasjonskodegrupper på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="65d4f-120">You can use info code groups in the following ways:</span></span>

- <span data-ttu-id="65d4f-121">Definere færre infokoder, og enkelt bruke dem på nytt.</span><span class="sxs-lookup"><span data-stu-id="65d4f-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="65d4f-122">Informasjonskoder som er inkludert i informasjonskodegrupper, har ingen forhåndsdefinerte avhengigheter om andre informasjonskoder.</span><span class="sxs-lookup"><span data-stu-id="65d4f-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="65d4f-123">Du kan ta med den samme informasjonskoden i flere informasjonskodegrupper og deretter bruke prioritering til å vise de samme informasjonskodene i rekkefølgen som er mest aktuell i en gitt situasjon.</span><span class="sxs-lookup"><span data-stu-id="65d4f-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
- <span data-ttu-id="65d4f-124">Koble informasjonskoder til andre koder eller informasjonskodegrupper for å samle inn informasjon om et produkt eller en transaksjon, uten å definere en egen informasjonskode eller koblede informasjonskoden for hvert scenario.</span><span class="sxs-lookup"><span data-stu-id="65d4f-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="65d4f-125">Informasjonskodeeksempler</span><span class="sxs-lookup"><span data-stu-id="65d4f-125">Info code examples</span></span>

<span data-ttu-id="65d4f-126">**Eksempel 1: Bruke infokoder på nytt**</span><span class="sxs-lookup"><span data-stu-id="65d4f-126">**Example 1: Reuse info codes**</span></span>

<span data-ttu-id="65d4f-127">Du kan koble informasjonskoder slik at når én informasjonskode blir utløst, utløses en annen informasjonskode like etter.</span><span class="sxs-lookup"><span data-stu-id="65d4f-127">You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="65d4f-128">Når du selger enkelte produkter, kan du eksempel be kassereren om å spørre kunden om de vil kjøpe batterier og en produktgaranti.</span><span class="sxs-lookup"><span data-stu-id="65d4f-128">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="65d4f-129">Når det gjelder andre produkter, kan du be kassereren om å spørre kunden om de vil kjøpe batterier, og også be om postnummeret deres.</span><span class="sxs-lookup"><span data-stu-id="65d4f-129">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="65d4f-130">Hvis du oppretter koblede informasjonskoder for disse scenariene, må du definere alle variantene av informasjonskoden, slik at kassereren blir bedt om å be om riktig informasjon.</span><span class="sxs-lookup"><span data-stu-id="65d4f-130">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="65d4f-131">Hvis du bruker informasjonskodegrupper, kan du definere vanlige informasjonskoder, for eksempel forespørsel om batterier, én gang og deretter bruke dem på nytt i flere informasjonskodegrupper.</span><span class="sxs-lookup"><span data-stu-id="65d4f-131">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="65d4f-132">Du kan også bruke prioritering i informasjonskodegruppene til å identifisere rekkefølgen spørsmålene vises i.</span><span class="sxs-lookup"><span data-stu-id="65d4f-132">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>

<span data-ttu-id="65d4f-133">**Eksempel 2: Koble infokoder til infokodegrupper**</span><span class="sxs-lookup"><span data-stu-id="65d4f-133">**Example 2: Link info codes to info code groups**</span></span>

<span data-ttu-id="65d4f-134">Når du selger visse produkter, for eksempel mobilenheter, er det alltid aktuelt å samle inn et spesifikt sett med informasjon, for eksempel telefonnummer, MEID-nummer (Mobile Equipment Identifier) og serienummer.</span><span class="sxs-lookup"><span data-stu-id="65d4f-134">When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="65d4f-135">Du vil imidlertid også samle inn annen informasjon for et nettbrett enn for en mobiltelefon.</span><span class="sxs-lookup"><span data-stu-id="65d4f-135">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="65d4f-136">Du kan definere en informasjonskodegruppe som inkluderer spørsmål om telefonnummeret, MEID-nummeret og serienummeret, og deretter koble informasjonskodegruppen til en individuell informasjonskode.</span><span class="sxs-lookup"><span data-stu-id="65d4f-136">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="65d4f-137">Når den produktspesifikke informasjonskoden utløses, kan informasjonskodegruppen utløses i neste omgang, slik at du kan samle inn fellesdataene uten å måtte definere flere sett med koblede informasjonskoder for hver enhet.</span><span class="sxs-lookup"><span data-stu-id="65d4f-137">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>