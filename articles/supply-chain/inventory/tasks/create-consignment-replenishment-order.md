---
title: Opprette en ny etterfyllingsordre for forsendelse
description: Dette emnet forklarer hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret.
author: sherry-zheng
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0d2030277e0810bebef9356136b0e11effc6d5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834031"
---
# <a name="create-a-consignment-replenishment-order"></a>Opprette en ny etterfyllingsordre for forsendelse

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret. Den viser også hvordan du registrerer et mottak av produkter slik at forsendelseslageret registreres som tilgjengelig lagerbeholdning eid av leverandøren. Dette gjøres vanligvis av en innkjøpansvarlig. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.

## <a name="create-a-consignment-replenishment-order"></a>Opprette en ny etterfyllingsordre for forsendelse
1. I navigasjonsruten går du til **Moduler > Innkjøp og leverandører > Forsendelse > Etterfyllingsordrer for forsendelse**.
2. Velg **Ny**.
3. I **Leverandørkonto**-feltet velger du leverandør **US-104** (du må velge en leverandør som er registrert som en eier på **lagereiere**-siden). 
4. Velg **OK**.
5. Velg **Legg til linje**.
6. I **Varenummer**-feltet skriver du inn `M9211CI` (du må velge en vare som er definert for forsendelseslager).
7. Angi et tall i **Antall**-feltet.
8. Angi en dato i feltet **Ønsket leveringsdato**. Ønskede og bekreftede datoer brukes av MRP-motoren for den forventede ankomsten av varene.  
9. Angi en dato i feltet **Bekreftet leveringsdato**.
10. Vis delen **Linjedetaljer**.
11. Velg fanen **Lagerdimensjoner**.
12. Hvis du vil vise eieren i feltet **Lagerdimensjonseier**, må du oppdatere siden. Leverandør US-104 er nå oppført som eier.  

## <a name="check-the-inventory-transaction-status"></a>Kontrollere lagertransaksjonsstatusen
1. Velg **Lager**.
2. Velg **Transaksjoner**.
3. Legg merke til at **Mottak**-feltet er satt til **Bestilt** i den ønskede raden.  
4. Lukk siden.

## <a name="receive-items"></a>Motta varer
1. Velg **Produktkvittering**.
2. Skriv inn en verdi i feltet **Ekstern mottaksseddel**.
3. I **Antall**-feltet skriver du inn et tall som er lavere enn antallet som vises. 
4. Velg **OK**.

## <a name="check-the-on-hand-inventory"></a>Kontrollere lagerbeholdningen
1. Velg **Lager**.
2. Velg **Beholdning**.
3. Velg **Oversikt**. Varene som er mottatt som forsendelseslager og som eies av leverandøren, er tilgjengelig lagerbeholdning. Restantall på etterfyllingsordren for forsendelsen vises i feltet **Bestilt i alt**.  
4. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]