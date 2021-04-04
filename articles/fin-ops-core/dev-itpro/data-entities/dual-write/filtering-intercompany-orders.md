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
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Filtrere konserninterne ordrer for å unngå synkronisering av ordrer og ordrelinjer

[!include [banner](../../includes/banner.md)]

Du kan filtrere konserninterne ordrer slik at tabellene **Ordrer** og **Ordrelinjer** ikke synkroniseres. I enkelte scenarioer er ikke de konserninterne ordredetaljene nødvendige i en kundeengasjementsapp.

Hver standard Dataverse-tabell utvides via referanser til kolonnen **IntercompanyOrder**, og tilordningene for dobbel skriving endres slik at de refererer til tilleggskolonnene i filtrene. Derfor synkroniseres ikke konserninterne ordrer lenger. Denne prosessen bidrar til å unngå unødvendige data i kundeengasjementsappen.

1. Utvid tabellen **CDS-salgsordrehoder** ved å legge til en referanse i kolonnen **IntercompanyOrder**. Denne kolonnen fylles bare ut i konserninterne ordrer. Kolonnen **IntercompanyOrder** er tilgjengelig i **SalesTable**-tabellen.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgsordrehoder":::

2. Når **CDS-salgsordrehoder** er utvidet, er kolonnen **IntercompanyOrder** tilgjengelig i tilordningen. Bruk et filter som har `INTERCOMPANYORDER == ""` som spørrestreng.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Dialogboksen Rediger spørring for CDS-salgsordrehoder":::

3. Utvid tabellen **CDS-salgsordrelinjer** ved å legge til en referanse i kolonnen **IntercompanyInventTransId**. Denne kolonnen fylles bare ut i konserninterne ordrer. Kolonnen **InterCompanyInventTransId** er tilgjengelig i **SalesLine**-tabellen.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgsordrelinjer":::

4. Når **CDS-salgsordrelinjer** er utvidet, er kolonnen **IntercompanyInventTransId** tilgjengelig i tilordningen. Bruk et filter som har `INTERCOMPANYINVENTTRANSID == ""` som spørrestreng.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Dialogboksen Rediger spørring for CDS-salgsordrelinjer":::

5. Gjenta trinn 1 og 2 for å utvide tabellen **Salgsfakturahoder V2** og legge til en filterspørring. I dette tilfellet bruker du `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`som spørrestrengen for filteret.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Siden Tilordne oppsamling til mål for Salgsfakturahoder V2":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Dialogboksen Rediger spørring for Salgsfakturahoder V2":::

6. Gjenta trinn 3 og 4 for å utvide tabellen **Salgsfakturalinjer V2** og legge til en filterspørring. I dette tilfellet bruker du `INTERCOMPANYINVENTTRANSID == ""`som spørrestrengen for filteret.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Dialogboksen Rediger spørring for Salgsfakturalinjer V2":::

7. **Tilbud**-tabellen har ikke en konsernintern relasjon. Hvis noen oppretter et tilbud for en av de konserninterne kundene, kan du bruke **CustGroup**-kolonnen til å legge alle disse kundene i én kundegruppe. Du kan utvide hodet og linjene ved å legge til **CustGroup**-kolonnen og deretter filtrere slik at gruppen ikke tas med.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Siden Tilordne oppsamling til mål for CDS-salgstilbudshode":::

8. Etter at **Tilbud** er utvidet, bruker du et filter som har `CUSTGROUP != "<company>"` som spørrestreng.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Dialogboksen Rediger spørring for CDS-salgstilbudshode":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]