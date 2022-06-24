---
title: Beholdningstilgjengelighet i dobbel skriving
description: Denne artikkelen inneholder informasjon om hvordan beholdningstilgjengelighet i dobbel skriving sjekkes.
author: RamaKrishnamoorthy
ms.date: 05/26/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: efd175dfbe49549561bdb7d697c8bc47016f1d5d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908269"
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

Finance and Operations-apper | Kundeengasjementsapper     | beskrivelse
---|---|---
[Lagerbeholdningsoppføringer for CDS](mapping-reference.md#145) | msdyn_inventoryonhandentries |
[Forespørsler om lagerbeholdning for CDS](mapping-reference.md#147) | msdyn_inventoryonhandrequests |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
