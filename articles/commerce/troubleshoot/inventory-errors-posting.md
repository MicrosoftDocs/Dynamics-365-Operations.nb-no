---
title: Posteringsfeil på kontoutdrag på grunn av utilgjengelig lager eller oppdateringskonflikter
description: Denne artikkelen inneholder mulige omgåelser for lagerrelaterte problemer under utdragspostering i Microsoft Dynamics 365 Commerce.
author: Shajain
ms.date: 12/19/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: cebb890b42def6e9b002b01be63266b88bfc35a4
ms.sourcegitcommit: 4ad87483ba0bfea3e04fdb7e578d8abc34e607a4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2022
ms.locfileid: "9887632"
---
# <a name="statement-posting-errors-due-to-unavailable-inventory-or-update-conflicts"></a>Posteringsfeil på kontoutdrag på grunn av utilgjengelig lager eller oppdateringskonflikter

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder mulige omgåelser for lagerrelaterte problemer under utdragspostering i Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Beskrivelse

Under posteringen av Commerce-transaksjoner kan du motta feilmeldinger som er knyttet til lagerproblemer eller oppdateringskonflikter.

### <a name="inventory-issues-error-message"></a>Feilmelding om lagerproblemer

Hvis du oppdager lagerproblemer, ligner feilmeldingen du mottar, på dette eksemplet:

> xx kan ikke plukkes, siden det bare er yy tilgjengelig i beholdningen

### <a name="update-conflict-error-messages"></a>Feilmeldinger for oppdateringskonflikt

En oppdateringskonflikt kan oppstå når lagervurderingsmetoden er enten *Standardkostnad* eller *Glidende gjennomsnitt*. Fordi begge disse metodene er permanente kostnadsberegningsmetoder, bestemmes den endelige kostnaden ved postering.

Hvis du bruker metoden *Glidende gjennomsnitt*, ligner feilmeldingen for oppdateringskonflikten som du mottar, på dette eksemplet:

> Lagerverdien xx,xx forventes ikke etter den proporsjonale utgiftsberegningen

Hvis du bruker metoden *Standardkostnad*, ligner feilmeldingen for oppdateringskonflikten som du mottar, på dette eksemplet:

> Standardkostnaden samsvarer ikke med den økonomiske lagerverdien etter oppdateringen. Verdi = xx,xx, Ant. = yy,yy, Standardkostnad = zz,zz

## <a name="resolutions"></a>Løsninger

### <a name="workaround-for-the-inventory-error"></a>Løsning for lagerfeilen

Du kan redusere lagerfeilen enten ved å oppdatere lageret for varen manuelt eller ved å aktivere fysisk negativt lager for varemodellgruppen som er knyttet til varen i Commerce headquarters.

For en konsekvent posteringsopplevelse anbefaler Microsoft at du aktiverer fysisk negativt lager for varemodellgruppen. I enkelte tilfeller kan kanskje ikke utdrag posteres med mindre fysisk negativt lager er aktivert.

Lager er for eksempel ikke tilgjengelig for en vare, men en kasserer returnerer varen og legger den deretter til den samme transaksjonen til en redusert pris for å etterligne et prissamsvar. I dette tilfellet blir både returtransaksjonen og salgstransaksjonen trukket inn i det samme utdraget for den enkelte kundeordren. Fordi det ikke er noen garanti for at returlinjen (som øker lageret) blir postert før salgslinjen (som reduserer lageret) blir postert, kan det imidlertid forekomme lagerfeil. Hvis fysisk negativ beholdning er aktivert i denne situasjonen, påvirkes ikke transaksjonsposteringen negativt og systemet gjenspeiler riktig beholdning.

#### <a name="enable-negative-physical-inventory-for-an-item-model-group"></a>Aktiver negativt fysisk lager for en varemodellgruppe

Følg denne fremgangsmåten for å aktivere negativt fysisk lager for en varemodellgruppe i Commerce headquarters.

1. Gå til **Lagerstyring \> Oppsett \> Lager**.
1. Velg varemodellgruppen i den venstre kjøpeboksmodulen.
1. Merk av for **Fysisk negativt lager** under **Negativt lager** i **Lagerpolicyer**-delen.

![Fysisk negativt lager er aktivert.](./media/Physical_Negative_Inventory.png)

### <a name="workaround-for-the-update-conflict-error"></a>Løsning for oppdateringskonfliktfeilen

Hvis du vil ha mulige løsninger for å rette oppdateringskonfliktfeilen, kan du se [En oppdateringskonflikt oppstår når lagervurderingsmetoden enten er standardkost eller glidende gjennomsnitt](/troubleshoot/dynamics-365/supply-chain/costing/update-conflict-standard-cost-moving-average-inventory-valuation).

> [!NOTE]
> For oppdateringskonfliktfeilen behøver du ikke å slette kundeordrene som ble generert ved hjelp av samlingstrinnet for postering. Når du har implementert de foreslåtte løsningene, bør utdraget posteres hvis du vurderer utdragspostering på nytt.
