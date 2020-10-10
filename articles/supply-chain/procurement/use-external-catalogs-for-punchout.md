---
title: Bruke eksterne kataloger for PunchOut-e-Procurement
description: Dette emnet forklarer hvordan du kan bruke eksterne kataloger til å opprette og sende rekvisisjoner.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adeffa101aa5a17543ca531aacde2130a07086e9
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826810"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a><span data-ttu-id="6e663-103">Bruke eksterne kataloger for PunchOut-e-Procurement</span><span class="sxs-lookup"><span data-stu-id="6e663-103">Use external catalogs for PunchOut e-procurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e663-104">Når du bruker eksterne kataloger for PunchOut eProcurement, trenger du ikke å vedlikeholde informasjon om leverandørens produkter i dine egne hoveddata.</span><span class="sxs-lookup"><span data-stu-id="6e663-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="6e663-105">I stedet er handlekurven på webområdet til en leverandør konvertert til rekvisisjonslinjer som har den riktige produktinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="6e663-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="6e663-106">Du bør ikke vedlikeholde beskrivelser og priser for leverandørenes produkter i dine egne hoveddata for produktet.</span><span class="sxs-lookup"><span data-stu-id="6e663-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="6e663-107">Bruk i stedet eksterne kataloger for PunchOut eProcurement.</span><span class="sxs-lookup"><span data-stu-id="6e663-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="6e663-108">Deretter, når ansatte oppretter rekvisisjoner, de kan stemple ut til en leverandørs eksterne katalogområde (de forlater med andre ord systemet ditt og går til leverandørens område).</span><span class="sxs-lookup"><span data-stu-id="6e663-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="6e663-109">Produktene som legges til i handlekurven på leverandørens webområde, kan deretter konverteres til rekvisisjonslinjer.</span><span class="sxs-lookup"><span data-stu-id="6e663-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="6e663-110">Derfor får du den riktige produktinformasjonen: produkt-ID, navn, pris og så videre.</span><span class="sxs-lookup"><span data-stu-id="6e663-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="6e663-111">Hvis du vil bruke eksterne kataloger, må en ansatt opprette en rekvisisjon på siden **Mine innkjøpsrekvisisjoner**.</span><span class="sxs-lookup"><span data-stu-id="6e663-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="6e663-112">Den ansatte som oppretter rekvisisjonen, kalles klargjøreren av rekvisjonen.</span><span class="sxs-lookup"><span data-stu-id="6e663-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="6e663-113">Som klargjører kan du utføre følgende oppgaver.</span><span class="sxs-lookup"><span data-stu-id="6e663-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="6e663-114">Bruk linjehandlingen **Eksterne kataloger** for å åpne en side som inneholder alle eksterne kataloger som er tilgjengelige for den angitte bestilleren, den juridiske enheten for innkjøp og mottaksdriftsenheten.</span><span class="sxs-lookup"><span data-stu-id="6e663-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="6e663-115">Avhengig av tillatelsene dine, kan du endre bestiller, juridisk enhet for innkjøp og mottaksdriftsenhet.</span><span class="sxs-lookup"><span data-stu-id="6e663-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="6e663-116">En endring i disse verdiene kan endre listen over eksterne kataloger som er tilgjengelige for en bestiller.</span><span class="sxs-lookup"><span data-stu-id="6e663-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="6e663-117">De eksterne katalogene som er tilgjengelige, avhenger av de gjeldende aktive innkjøpspolicyene for den juridiske enheten for innkjøp eller mottaksdriftsenheten.</span><span class="sxs-lookup"><span data-stu-id="6e663-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="6e663-118">Disse policyene kan tillate eller hindre tilgang til bestemte innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="6e663-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="6e663-119">Listen over eksterne kataloger som er tilordnet disse innkjøpskategoriene, kan derfor bli påvirket.</span><span class="sxs-lookup"><span data-stu-id="6e663-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="6e663-120">Hvis du vil ha mer informasjon om policyer, kan du se [Oversikt over innkjøpspolicyer](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6e663-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="6e663-121">For å finne eksterne kataloger for bestemte innkjøpskategorier skriver du inn tekst i katalogsøkefeltet.</span><span class="sxs-lookup"><span data-stu-id="6e663-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="6e663-122">Hvis du vil legge til produkter fra ekstern katalog for en leverandør på leverandørens webområde, klikker du den eksterne katalogen.</span><span class="sxs-lookup"><span data-stu-id="6e663-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="6e663-123">Legg deretter til produkter i handlekurven, og sjekk ut. Handlekurvene overføres til Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6e663-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="6e663-124">Hvis det finnes flere alternativer for innkjøpskategoriene, velger du den riktige innkjøpskategorien før du legger til linjene i rekvisisjonen.</span><span class="sxs-lookup"><span data-stu-id="6e663-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="6e663-125">Når linjer er lagt til en rekvisisjon, kan du legge til flere linjer uten å bruke eksterne kataloger.</span><span class="sxs-lookup"><span data-stu-id="6e663-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="6e663-126">Du kan også fortsette å bruke eksterne kataloger til å legge til linjer.</span><span class="sxs-lookup"><span data-stu-id="6e663-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="6e663-127">Når rekvisisjonen er klar, kan du bruke handlingen **Arbeidsflyt** > **Send** for å sende den til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6e663-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="6e663-128">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6e663-128">Additional resources</span></span>

- [<span data-ttu-id="6e663-129">Definere en ekstern katalog for PunchOut-e-Procurement</span><span class="sxs-lookup"><span data-stu-id="6e663-129">Set up an external catalog for PunchOut e-procurement</span></span>](set-up-external-catalog-for-punchout.md)
- [<span data-ttu-id="6e663-130">Kjøp av cXML-forbedringer</span><span class="sxs-lookup"><span data-stu-id="6e663-130">Purchasing cXML enhancements</span></span>](purchasing-cxml-enhancements.md)