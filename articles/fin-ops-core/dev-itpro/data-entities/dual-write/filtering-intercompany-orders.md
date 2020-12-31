---
title: Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer
description: Dette emnet beskriver hvordan konserninterne ordrer filtreres for å unngå synkronisering av ordrer og ordrelinjer.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701039"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a><span data-ttu-id="73107-103">Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer</span><span class="sxs-lookup"><span data-stu-id="73107-103">Filter intercompany orders to avoid synchronizing Orders and OrderLines</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73107-104">Du kan filtrere konserninterne ordrer for å unngå synkronisering av **Ordrer**- og **Ordrelinjer**-enhetene.</span><span class="sxs-lookup"><span data-stu-id="73107-104">You can filter intercompany orders to avoid synchronizing the **Orders** and **OrderLines** entities.</span></span> <span data-ttu-id="73107-105">I noen scenarioer er ikke de konserninterne ordredetaljene nødvendige i kundeengasjementappen.</span><span class="sxs-lookup"><span data-stu-id="73107-105">In some scenarios, the intercompany order details are not necessary in customer engagement app.</span></span>

<span data-ttu-id="73107-106">Hver av de standard Common Data Service-enhetene utvides med referanser til **IntercompanyOrder**-feltet, og dobbeltskrivningstilordningene endres for å referere til tilleggsfeltene i filtrene.</span><span class="sxs-lookup"><span data-stu-id="73107-106">Each of the standard Common Data Service entities is extended with references to the **IntercompanyOrder** field, and the dual-write maps are modified to refer to the additional fields in the filters.</span></span> <span data-ttu-id="73107-107">Resultatet er at de konserninterne ordrene ikke lenger er synkronisert.</span><span class="sxs-lookup"><span data-stu-id="73107-107">The result is that the intercompany orders are no longer synchronized.</span></span> <span data-ttu-id="73107-108">Denne prosessen unngår unødvendige data i kundeengasjementappen.</span><span class="sxs-lookup"><span data-stu-id="73107-108">This process avoids unnecessary data in the customer engagement app.</span></span>

1. <span data-ttu-id="73107-109">Legg til en referanse til **IntercompanyOrder** i **CDS-salgsordrehoder**.</span><span class="sxs-lookup"><span data-stu-id="73107-109">Add a reference to **IntercompanyOrder** to **CDS Sales Order Headers**.</span></span> <span data-ttu-id="73107-110">Den fylles bare ut på konserninterne ordrer.</span><span class="sxs-lookup"><span data-stu-id="73107-110">It is populated on only intercompany orders.</span></span> <span data-ttu-id="73107-111">Feltet **IntercompanyOrder** er tilgjengelig i **SalesTable**.</span><span class="sxs-lookup"><span data-stu-id="73107-111">The field **IntercompanyOrder** is available in **SalesTable**.</span></span>

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Tilordne oppsamling til mål, SalesOrderHeader":::
    
2. <span data-ttu-id="73107-113">Når **CDS-salgsordrehoder** er utvidet, er feltet **IntercompanyOrder** tilgjengelig i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="73107-113">After **CDS Sales Order Headers** is extended, the **IntercompanyOrder** field is available in the mapping.</span></span> <span data-ttu-id="73107-114">Bruk et filter med `INTERCOMPANYORDER == ""` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="73107-114">Apply a filter with `INTERCOMPANYORDER == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Salgsordrehoder, rediger spørring":::

3. <span data-ttu-id="73107-116">Legg til en referanse til **IntercompanyInventTransId** i **CDS-salgsordrelinjer**.</span><span class="sxs-lookup"><span data-stu-id="73107-116">Add a reference to **IntercompanyInventTransId** to **CDS Sales Order Lines**.</span></span>  <span data-ttu-id="73107-117">Den fylles bare ut på konserninterne ordrer.</span><span class="sxs-lookup"><span data-stu-id="73107-117">It is populated on only intercompany orders.</span></span> <span data-ttu-id="73107-118">Feltet **InterCompanyInventTransID** er tilgjengelig i **SalesLine**.</span><span class="sxs-lookup"><span data-stu-id="73107-118">The field **InterCompanyInventTransID** is available in **SalesLine**.</span></span>

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Tilordne oppsamling til mål, SalesOrderLine":::

4. <span data-ttu-id="73107-120">Når **CDS-salgsordrelinjer** er utvidet, er feltet **IntercompanyInventTransId** tilgjengelig i tilordningen.</span><span class="sxs-lookup"><span data-stu-id="73107-120">After **CDS Sales Order Lines** is extended, the **IntercompanyInventTransId** field is available in the mapping.</span></span> <span data-ttu-id="73107-121">Bruk et filter med `INTERCOMPANYINVENTTRANSID == ""` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="73107-121">Apply a filter with `INTERCOMPANYINVENTTRANSID == ""` as the query string.</span></span>

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Salgsordrelinjer, rediger spørring":::

5. <span data-ttu-id="73107-123">Utvid **Salgsfakturahoder V2** og **Salgsfakturalinjer V2** på samme måte som du utvidet Common Data Service-enhetene i trinn 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="73107-123">Extend **Sales Invoice Header V2** and **Sales Invoice Lines V2** in the same way you extended the Common Data Service entities in steps 1 and 2.</span></span> <span data-ttu-id="73107-124">Legg deretter til filterspørringene.</span><span class="sxs-lookup"><span data-stu-id="73107-124">Then add the filter queries.</span></span> <span data-ttu-id="73107-125">Filterstrengen for **Salgsfakturahoder V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span><span class="sxs-lookup"><span data-stu-id="73107-125">The filter string for **Sales Invoice Header V2** is `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.</span></span> <span data-ttu-id="73107-126">Filterstrengen for **Salgsfakturalinjer V2** er `INTERCOMPANYINVENTTRANSID == ""`.</span><span class="sxs-lookup"><span data-stu-id="73107-126">The filter string for **Sales Invoice Lines V2** is `INTERCOMPANYINVENTTRANSID == ""`.</span></span>

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Tilordne oppsamling til mål, Salgsfakturahoder":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Salgsfakturahoder, rediger spørring":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Salgsfakturalinjer, rediger spørring":::

6. <span data-ttu-id="73107-130">**Tilbud**-enheten har ikke en konsernintern relasjon.</span><span class="sxs-lookup"><span data-stu-id="73107-130">The **Quotations** entity doesn't have an intercompany relationship.</span></span> <span data-ttu-id="73107-131">Hvis noen oppretter et tilbud for en av de konserninterne kundene, kan du legge alle disse kundene i én kundegruppe ved hjelp av **CustGroup**-feltet.</span><span class="sxs-lookup"><span data-stu-id="73107-131">If someone creates a quote for one of your intercompany customers, you can put all of these customers in one customer group by using the **CustGroup** field.</span></span>  <span data-ttu-id="73107-132">Topptekst og linjer kan utvides for å legge til **CustGroup**-feltet og deretter filtreres, slik at denne gruppen ikke inkluderes.</span><span class="sxs-lookup"><span data-stu-id="73107-132">Header and lines can be extended to add the **CustGroup** field and then filter to not include this group.</span></span>

    :::image type="content" source="media/filter-cust-group.png" alt-text="Tilordne oppsamling til mål, Salgstilbudshoder":::

7. <span data-ttu-id="73107-134">Når du har utvidet enheten **Tilbud**, bruker du et filter med `CUSTGROUP !=  "<company>"` som spørrestreng.</span><span class="sxs-lookup"><span data-stu-id="73107-134">After you extent the **Quotations** entity, apply a filter with `CUSTGROUP !=  "<company>"` as the query string.</span></span>

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Salgstilbudshode, rediger spørring":::
