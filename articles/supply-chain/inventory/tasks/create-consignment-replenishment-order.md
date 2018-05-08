---
title: Opprette en ny etterfyllingsordre for forsendelse
description: "Denne fremgangsmåten viser hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Opprette en ny etterfyllingsordre for forsendelse

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter en etterfyllingsordre for forsendelse der du kan spore forventet levering fra en leverandør til forsendelseslageret. Den viser også hvordan du registrerer et mottak av produkter slik at forsendelseslageret registreres som tilgjengelig lagerbeholdning eid av leverandøren. Dette gjøres vanligvis av en innkjøpansvarlig. Du kan bruke denne veiledningen i USMF-demodatafirmaet. Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.




## <a name="create-a-consignment-replenishment-order"></a>Opprette en ny etterfyllingsordre for forsendelse
1. Gå til Innkjøp og leverandører > Forsendelse > Etterfyllingsordrer for forsendelse.
2. Klikk Ny.
3. Angi leverandøren US-104 i Leverandørkonto-feltet.
    * Du må velge en leverandør som er registrert som eier på siden Beholdningseiere.  
4. Klikk OK.
5. Klikk Legg til linje.
6. Skriv inn M9211CI i Varenummer-feltet.
    * Du må velge en vare som er definert for forsendelseslager.  
7. Angi et tall i feltet Antall.
8. Angi en dato i feltet Ønsket leveringsdato.
    * Ønskede og bekreftede datoer brukes av MRP-motoren for den forventede ankomsten av varene.  
9. Angi en dato i Bekreftet leveringsdato-feltet.
10. Vis seksjonen Linjedetaljer.
11. Klikk kategorien Lagerdimensjoner.
12. Hvis du vil vise eieren i feltet Lagerdimensjonseier, må du oppdatere siden.
    * Leverandør US-104 er nå oppført som eier.  

## <a name="check-the-inventory-transaction-status"></a>Kontrollere lagertransaksjonsstatusen
1. Klikk Lager.
2. Klikk Transaksjoner.
3. Merk den valgte raden i listen.
    * Legg merke til at Mottak-feltet er satt til Bestilt.  
4. Lukk siden.

## <a name="receive-items"></a>Motta varer
1. Klikk Produktkvittering.
2. Skriv inn en verdi i feltet Ekstern mottaksseddel.
3. I Antall-feltet skriver du inn et tall som er lavere enn antallet som vises.
4. Klikk OK.

## <a name="check-the-on-hand-inventory"></a>Kontrollere lagerbeholdningen
1. Klikk Lager.
2. Klikk På lager.
3. Klikk Oversikt.
    * Varene som er mottatt som forsendelseslager og som eies av leverandøren, er tilgjengelig lagerbeholdning. Restantall på etterfyllingsordren for forsendelsen vises i Bestilt i alt-feltet.  
4. Lukk siden.
5. Klikk Lukk.

