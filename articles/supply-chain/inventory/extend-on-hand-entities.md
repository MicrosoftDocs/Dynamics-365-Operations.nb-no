---
title: Utvide dataenheter for lagerbeholdning
description: Dette emnet inneholder et eksempel som viser hvordan du legger til utvidede felt i INVENTORSITEONHANDENTITY- og INVENTWAREHOUSEONHANDENTITY-visningene, slik at egenskapene til lagerbeholdningsdataenhetene kan fungere med tilleggene.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8161d951c3296b63476c4e7b527efca163a4f4b3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577702"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Utvide dataenheter for lagerbeholdning

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management tilbyr [utvidelsesfunksjoner](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) som lar deg [legge til felt i tabeller ved hjelp av utvidelser](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Dette emnet inneholder et eksempel som viser hvordan du legger til utvidede felt i `INVENTORSITEONHANDENTITY`- og `INVENTWAREHOUSEONHANDENTITY`-visningene, slik at egenskapene til lagerbeholdningsdataenhetene kan fungere med tilleggene. Hvis du vil ha mer informasjon om dataenheter, kan du se [Oversikt over databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Her er en liste over noen av lagerbeholdningsdataenhetene:
>
> - Lagerbeholdning etter område
> - Lagerbeholdning etter område V2
> - Lagerbeholdning etter lager
> - Lagerbeholdning etter lager v2

Når du har lagt til felt i tabeller som brukes av `inventSiteOnHandView`-visningen, må du synkronisere motoren, slik at utvidelsene blir gjenkjent på riktig måte.

1. Utvid `InventSiteOnHandView`-visningen ved å legge til utvidelsesfeltet.
1. Utvid `InventSiteOnHandAggregatedView`-visningen med utvidelsesfeltene.
1. Utvid `InventSiteOnHandAggregatedViewBuilder` viewBuilder-klassen ved å endre `getExtensionFields()`-metoden. På denne måten tilordner du gamle visningsfelt til nye visningsfelt når viewBuilder-synkronisering kjøres.

Du har for eksempel lagt til følgende fire felt i `InventTable`-tabellen via utvidelse:

- Egendefinert felt 1
- Egendefinert felt 2
- Egendefinert felt 3
- Egendefinert felt 4

I dette tilfellet må du endre `getExtensionFields()`-metoden på følgende måte.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Når du har fullført disse trinnene, kan du utvide lagerbeholdningen etter område og lagerbeholdningen etter lagerdataenheter ved å legge til de nye feltene. På denne måten sikrer du at de utvidede feltene gjenkjennes og tas med under dataoverføring som bruker disse dataenhetene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]