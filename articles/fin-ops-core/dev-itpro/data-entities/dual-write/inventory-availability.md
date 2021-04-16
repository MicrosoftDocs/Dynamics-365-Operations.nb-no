---
title: Beholdningstilgjengelighet i dobbel skriving
description: Dette emnet inneholder informasjon om hvordan beholdningstilgjengelighet i dobbel skriving sjekkes.
author: yijialuan
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 9d9b7970720218fbcf2f512345ade672810440b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748571"
---
# <a name="inventory-availability-in-dual-write"></a>Beholdningstilgjengelighet i dobbel skriving

[!include [banner](../../includes/banner.md)]

Ve å bruke beholdningstilgjengelighet kan du kontrollere beholdningen før du legger til et produkt på sidene **Tilbud**, **Ordre** eller **Fakturaer** i Microsoft Dynamics 365 Sales. Du kan for eksempel kontrollere beholdning og fastslå en fullføringsdato som én hovedoppgave i [kundeemne-til-kontanter](dual-write-prospect-to-cash.md)-prosessen.

Hvis du ikke har nok beholdning, kan du beregne en leveringsdato basert på prosjekterte beholdningsmottak og -problemer. Du kan også kontrollere produktets tilgjengelig for ordre (ATP)-informasjon, der du kan finne ATP-antallet i den forhåndsdefinerte tidshorisonten.

## <a name="on-hand-inventory"></a>Lagerbeholdning

I Dynamics 365 Sales er en ny **Lagerbeholdning**-knapp lagt til i hodet på sidene **Tilbud**, **Ordrer** og **Fakturaer**. Når du velger denne knappen, vises det en dialogboks hvor du kan angi firmaet og produktet du vil kontrollere tilgjengelig beholdning for. Denne dialogboksen viser den samme informasjonen som [Lagerbeholdning](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogboksen returnerer lagerinformasjonen fra Dynamics 365 Supply Chain Management. Denne informasjonen inneholder følgende antall:

- Antall på lager
- Antall reservert på lager
- Antall tilgjengelig på lager
- Bestilt antall
- Antall i bestilling
- Reservert bestilt antall
- Totalt tilgjengelig antall

## <a name="atp-information"></a>ATP-informasjon

I Sales er det lagt til en ny **ATP-informasjon**-knapp for linjeelementer på sidene **Tilbud**, **Ordrer** og **Fakturaer**. Når du velger denne knappen, vises det en dialogboks hvor du kan angi firma, produkt, beholdningsnettsted, beholdningslager og ordreantall. Denne dialogboksen har de samme innstillingene som er beskrevet i [Ordrebekreftelse](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogboksen returnerer ATP-informasjonen fra Supply Chain Management. Denne informasjonen inneholder følgende antall:

- ATP-antall
- Tilgangsantall
- Avgangsantall
- Antall på lager

## <a name="how-it-works"></a>Hvordan det fungerer

Når du velger knappen **Lagerbeholdning** på siden **Tilbud**, **Ordrer** eller **Fakturaer**, foretas et live oppkall med dobbel skriving til API-en for **Lagerbeholdning**. API-en beregner lagerbeholdningen for det angitte produktet. Resultatet blir lagret i tabellene **InventCDSInventoryOnHandRequestEntity** og **InventCDSInventoryOnHandEntryEntity** og skrives deretter til Dataverse av dobbel skriving. Hvis du vil bruke denne funksjonaliteten, må du kjøre følgende dobbel skriving-tilordninger. Hopp over innledende synkronisering når du kjører tilordningene.

- Oppføringer for CDS-lagerbeholdning (msdyn_inventoryonhandentries)
- Forespørsler om CDS-lagerbeholdning (msdyn_inventoryonhandrequests)

## <a name="templates"></a>Maler
Følgende maler er tilgjengelige for visning av lagerbeholdningsdata.

Finance and Operations-apper | Kundeengasjementsapp | beskrivelse 
---|---|---
[Lagerbeholdningsoppføringer for CDS](#145) | msdyn_inventoryonhandentries |
[Forespørsler om lagerbeholdning for CDS](#147) | msdyn_inventoryonhandrequests |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a>Oppføringer for CDS-lagerbeholdning (msdyn_inventoryonhandentries)

Denne malen synkroniserer data mellom Finance and Operations-apper og Dataverse.

Finance and Operations-felt | Tilordningstype | Kundeengasjement-felt | Standardverdi
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a>Forespørsler om CDS-lagerbeholdning (msdyn_inventoryonhandrequests)

Denne malen synkroniserer data mellom Finance and Operations-apper og Dataverse.

Finance and Operations-felt | Tilordningstype | Kundeengasjement-felt | Standardverdi
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |






[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]