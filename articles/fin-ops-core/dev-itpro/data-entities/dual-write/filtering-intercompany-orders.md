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
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer

[!include [banner](../../includes/banner.md)]

Du kan filtrere konserninterne ordrer for å unngå synkronisering av **Ordrer**- og **Ordrelinjer**-enhetene. I noen scenarioer er ikke de konserninterne ordredetaljene nødvendige i kundeengasjementappen.

Hver av de standard Common Data Service-enhetene utvides med referanser til **IntercompanyOrder**-feltet, og dobbeltskrivningstilordningene endres for å referere til tilleggsfeltene i filtrene. Resultatet er at de konserninterne ordrene ikke lenger er synkronisert. Denne prosessen unngår unødvendige data i kundeengasjementappen.

1. Legg til en referanse til **IntercompanyOrder** i **CDS-salgsordrehoder**. Den fylles bare ut på konserninterne ordrer. Feltet **IntercompanyOrder** er tilgjengelig i **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Tilordne oppsamling til mål, SalesOrderHeader":::
    
2. Når **CDS-salgsordrehoder** er utvidet, er feltet **IntercompanyOrder** tilgjengelig i tilordningen. Bruk et filter med `INTERCOMPANYORDER == ""` som spørrestreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Salgsordrehoder, rediger spørring":::

3. Legg til en referanse til **IntercompanyInventTransId** i **CDS-salgsordrelinjer**.  Den fylles bare ut på konserninterne ordrer. Feltet **InterCompanyInventTransID** er tilgjengelig i **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Tilordne oppsamling til mål, SalesOrderLine":::

4. Når **CDS-salgsordrelinjer** er utvidet, er feltet **IntercompanyInventTransId** tilgjengelig i tilordningen. Bruk et filter med `INTERCOMPANYINVENTTRANSID == ""` som spørrestreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Salgsordrelinjer, rediger spørring":::

5. Utvid **Salgsfakturahoder V2** og **Salgsfakturalinjer V2** på samme måte som du utvidet Common Data Service-enhetene i trinn 1 og 2. Legg deretter til filterspørringene. Filterstrengen for **Salgsfakturahoder V2** er `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Filterstrengen for **Salgsfakturalinjer V2** er `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Tilordne oppsamling til mål, Salgsfakturahoder":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Salgsfakturahoder, rediger spørring":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Salgsfakturalinjer, rediger spørring":::

6. **Tilbud**-enheten har ikke en konsernintern relasjon. Hvis noen oppretter et tilbud for en av de konserninterne kundene, kan du legge alle disse kundene i én kundegruppe ved hjelp av **CustGroup**-feltet.  Topptekst og linjer kan utvides for å legge til **CustGroup**-feltet og deretter filtreres, slik at denne gruppen ikke inkluderes.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Tilordne oppsamling til mål, Salgstilbudshoder":::

7. Når du har utvidet enheten **Tilbud**, bruker du et filter med `CUSTGROUP !=  "<company>"` som spørrestreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Salgstilbudshode, rediger spørring":::
