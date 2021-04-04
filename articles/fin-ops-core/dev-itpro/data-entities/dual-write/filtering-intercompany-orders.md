---
title: Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer
description: Dette emnet forklarer hvordan du filtrerer konserninterne ordrer slik at enhetene Ordrer og Ordrelinjer ikke synkroniseres.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 9a736c8e93dfa7dbcd0739b52e2da987dcefdc0e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568108"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a><span data-ttu-id="19ce6-103">Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer</span><span class="sxs-lookup"><span data-stu-id="19ce6-103">Filter intercompany orders to avoid syncing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19ce6-104">Du kan filtrere konserninterne ordrer slik at tabellene **Ordrer** og **Ordrelinjer** ikke synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="19ce6-104">You can filter intercompany orders so that the **Orders** and **OrderLines** tables aren't synced.</span></span> <span data-ttu-id="19ce6-105">I enkelte scenarioer er ikke de konserninterne ordredetaljene nødvendige i en kundeengasjementsapp.</span><span class="sxs-lookup"><span data-stu-id="19ce6-105">In some scenarios, the intercompany order details aren't required in a customer engagement app.</span></span>

<span data-ttu-id="19ce6-106">Hver standard Dataverse-tabell utvides via referanser til kolonnen **IntercompanyOrder**, og tilordningene for dobbel skriving endres slik at de refererer til tilleggskolonnene i filtrene.</span><span class="sxs-lookup"><span data-stu-id="19ce6-106">Each standard Dataverse table is extended through references to the **IntercompanyOrder** column, and the dual-write maps are modified so that they refer to the additional columns in the filters.</span></span> <span data-ttu-id="19ce6-107">Derfor synkroniseres ikke konserninterne ordrer lenger.</span><span class="sxs-lookup"><span data-stu-id="19ce6-107">Therefore, the intercompany orders are no longer synced.</span></span> <span data-ttu-id="19ce6-108">Denne prosessen bidrar til å unngå unødvendige data i kundeengasjementsappen.</span><span class="sxs-lookup"><span data-stu-id="19ce6-108">This process helps prevent unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="19ce6-109">Utvid tabellen **CDS-salgsordrehoder** ved å legge til en referanse i kolonnen **IntercompanyOrder**.</span><span class="sxs-lookup"><span data-stu-id="19ce6-109">Extend the **CDS Sales Order Headers** table by adding a reference to the **IntercompanyOrder** column.</span></span> <span data-ttu-id="19ce6-110">Denne kolonnen fylles bare ut i konserninterne ordrer.</span><span class="sxs-lookup"><span data-stu-id="19ce6-110">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="19ce6-111">Kolonnen **IntercompanyOrder** er tilgjengelig i **SalesTable**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="19ce6-111">The **IntercompanyOrder** column is available in the **SalesTable** table.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgsordrehoder":::

2. <span data-ttu-id="19ce6-113">Når **CDS-salgsordrehoder** er utvidet, er kolonnen **IntercompanyOrder** tilgjengelig i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="19ce6-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** column is available in the mapping.</span></span> <span data-ttu-id="19ce6-114">Bruk et filter som har `INTERCOMPANYORDER == ""` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="19ce6-114">Apply a filter that has `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogboksen Rediger spørring for CDS-salgsordrehoder":::

3. <span data-ttu-id="19ce6-116">Utvid tabellen **CDS-salgsordrelinjer** ved å legge til en referanse i kolonnen **IntercompanyInventTransId**.</span><span class="sxs-lookup"><span data-stu-id="19ce6-116">Extend the **CDS Sales Order Lines** table by adding a reference to the **IntercompanyInventTransId** column.</span></span> <span data-ttu-id="19ce6-117">Denne kolonnen fylles bare ut i konserninterne ordrer.</span><span class="sxs-lookup"><span data-stu-id="19ce6-117">This column is filled in only on intercompany orders.</span></span> <span data-ttu-id="19ce6-118">Kolonnen **InterCompanyInventTransId** er tilgjengelig i **SalesLine**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="19ce6-118">The **InterCompanyInventTransId** column is available in the **SalesLine** table.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgsordrelinjer":::

4. <span data-ttu-id="19ce6-120">Når **CDS-salgsordrelinjer** er utvidet, er kolonnen **IntercompanyInventTransId** tilgjengelig i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="19ce6-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** column is available in the mapping.</span></span> <span data-ttu-id="19ce6-121">Bruk et filter som har `INTERCOMPANYINVENTTRANSID == ""` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="19ce6-121">Apply a filter that has `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogboksen Rediger spørring for CDS-salgsordrelinjer":::

5. <span data-ttu-id="19ce6-123">Gjenta trinn 1 og 2 for å utvide tabellen **Salgsfakturahoder V2** og legge til en filterspørring.</span><span class="sxs-lookup"><span data-stu-id="19ce6-123">Repeat steps 1 and 2 to extend the **Sales Invoice Header V2** table and add a filter query.</span></span> <span data-ttu-id="19ce6-124">I dette tilfellet bruker du `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`som spørrestrengen for filteret.</span><span class="sxs-lookup"><span data-stu-id="19ce6-124">In this case, use `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Siden Tilordne oppsamling til mål for Salgsfakturahoder V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogboksen Rediger spørring for Salgsfakturahoder V2":::

6. <span data-ttu-id="19ce6-127">Gjenta trinn 3 og 4 for å utvide tabellen **Salgsfakturalinjer V2** og legge til en filterspørring.</span><span class="sxs-lookup"><span data-stu-id="19ce6-127">Repeat steps 3 and 4 to extend the **Sales Invoice Lines V2** table and add a filter query.</span></span> <span data-ttu-id="19ce6-128">I dette tilfellet bruker du `INTERCOMPANYINVENTTRANSID == ""`som spørrestrengen for filteret.</span><span class="sxs-lookup"><span data-stu-id="19ce6-128">In this case, use `INTERCOMPANYINVENTTRANSID == ""` as the query string for the filter.</span></span>

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogboksen Rediger spørring for Salgsfakturalinjer V2":::

7. <span data-ttu-id="19ce6-130">**Tilbud**-tabellen har ikke en konsernintern relasjon.</span><span class="sxs-lookup"><span data-stu-id="19ce6-130">The **Quotations** table doesn't have an intercompany relationship.</span></span> <span data-ttu-id="19ce6-131">Hvis noen oppretter et tilbud for en av de konserninterne kundene, kan du bruke **CustGroup**-kolonnen til å legge alle disse kundene i én kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="19ce6-131">If someone creates a quotation for one of your intercompany customers, you can use the **CustGroup** column to put all those customers into one customer group.</span></span> <span data-ttu-id="19ce6-132">Du kan utvide hodet og linjene ved å legge til **CustGroup**-kolonnen og deretter filtrere slik at gruppen ikke tas med.</span><span class="sxs-lookup"><span data-stu-id="19ce6-132">You can extend the header and lines by adding the **CustGroup** column, and then filter so that the group isn't included.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgstilbudshode":::

8. <span data-ttu-id="19ce6-134">Etter at **Tilbud** er utvidet, bruker du et filter som har `CUSTGROUP != "<company>"` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="19ce6-134">After **Quotations** is extended, apply a filter that has `CUSTGROUP != "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogboksen Rediger spørring for CDS-salgstilbudshode":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]