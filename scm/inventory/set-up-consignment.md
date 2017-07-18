---
title: Definere forsendelse
description: Dette emnet forklarer hvordan du konfigurerer operasjoner for innkommende forsendelseslager.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b8692a3033cd665402721ea18ba8c28557c049de
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017

---

# <a name="set-up-consignment"></a>Definere forsendelse

[!include[banner](../includes/banner.md)]


Dette emnet forklarer hvordan du konfigurerer operasjoner for innkommende forsendelseslager. 

Forsendeleslager er lager som eies av en leverandør, men lagres på ditt område. Når du er klar til å forbruke eller bruke lageret, kan du ta over eierskapet for lageret. Dette emnet beskriver oppsettet for å aktivere forsendelsesprosessene. Hvis du vil ha mer informasjon om forsendelsesprosesser, kan du se [Forsendelse](consignment.md).

## <a name="inventory-owners"></a>Beholdningseiere
Hvis du vil registrere fysisk forsendelse for innkommende lager, må du definere en leverandøreier. Dette gjøres på siden **Lagereier**. Når du velger en **leverandørkonto**, genereres det standardverdier for feltene **Navn** og **Eier**. Verdien i **Eier**-feltet vil være synlig for leverandøren, slik at du kanskje vil endre dette hvis dine navn på leverandørkontoer ikke er enkle for eksterne brukere å gjenkjenne. Det er mulig å redigere **Eier**-feltet, men bare frem til når du lagrer posten **Lagereier**. **Navn**-feltet fylles ut med navnet på parten som leverandørkontoen som er knyttet til, og dette kan ikke endres. 

[![Beholdningseiere](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sporingsdimensjonsgruppe
Varer som skal brukes i forsendelsesprosesser må være knyttet til en **sporingsdimensjonsgruppe** der **Eier**-dimensjonen er satt til **Aktiv**. Alternativene **Fysisk beholdning** og **Økonomisk lager** er alltid valgt for eierdimensjonen. **Dekningsplanlegg etter dimensjon** er aldri er valgt. 

[![Sporingsdimensjonsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Endringsjournal for lagereierskap
Journalen **Endring av lagereierskap** brukes til å registrere overføring av eierskap av forsendelseslageret fra leverandøren til den juridiske enheten som forbruker det. Det må identifiseres med et lagerjournalnavn, på samme måte som en hvilken som helst annen lagerjournal. Disse navnene opprettes på siden **Navn på lagerjournal**, og **Journaltype** må være satt til **Endring av eierskap**. 

[![Endringsjournal for lagereierskap](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbeid i forsendelsesprosesser
Hvis leverandørene bruker grensesnittet for leverandørsamarbeid, kan de bruke dette til å overvåke forbruket av beholdningen på området. Hvis du vil ha mer informasjon om hvordan du definerer leverandører med leverandørsamarbeid, kan du se [Konfigurere sikkerhet for brukere av leverandørsamarbeid](../procurement/configure-security-vendor-portal-users.md).




