---
title: Behandle butikkbeholdning
description: "Denne artikkelen beskriver hvilke typer dokumenter du kan bruke til å styre lager."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Behandle butikkbeholdning

[!include[banner](includes/banner.md)]


Denne artikkelen beskriver hvilke typer dokumenter du kan bruke til å styre lager.

Du kan bruke følgende typer dokumenter til å styre organisasjonens lager.

## <a name="purchase-orders"></a>Bestillinger
Bestillinger opprettes ved hovedkontoret. Hvis et lager for detaljhandel er inkludert i bestillingshodet, kan ordren mottas i butikken ved hjelp av Detaljhandel og handel i moderne salgssted eller skysalgssted for Microsoft Dynamics 365 for Operations - Retail. Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret vises antallene som ble mottatt i butikken, i **Motta nå**-feltet i bestillingen i Microsoft Dynamics 365 for Operations.

## <a name="transfer-orders"></a>Overføringsordrer
En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes fra. I dette tilfellet vises overføringsordren i butikken som en plukkforespørsel i Moderne salgssted eller Skysalgssted. Når de ønskede antallene er plukket, er lagres de og sendes til hovedkontoret. På hovedkontoret vises antallene som ble plukket i butikken, i **Send nå**-feltet i overføringsordren i Microsoft Dynamics 365 for Operations. En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes til. I dette tilfellet vises overføringsordren i butikken som en mottaksforespørsel i Moderne salgssted eller Skysalgssted. Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret vises antallene som ble mottatt i butikken, i **Motta nå**-feltet i overføringsordren i Microsoft Dynamics 365 for Operations.

## <a name="stock-counts"></a>Lagerantall
Lagertellinger kan være planlagt eller ikke planlagt. Planlagte lagertellinger startes ved hovedkontoret, som angir hvilke varer som skal telles. Hovedkontoret oppretter et opptellingsdokument som kan mottas i butikken, der faktisk beholdningsantall registreres i Moderne salgssted eller Skysalgssted. Ikke planlagte lagertellinger startes i en butikk, og faktisk beholdningsantall oppdateres i Moderne salgssted eller Skysalgssted. I motsetning til planlagte lagertellinger har ikke ikke-planlagte lagertellinger en forhåndsdefinert liste over varer. Når en lagertelling av en av disse typene er fullført, lagres og sendes den til hovedkontoret. Ved hovedkontoret valideres og posteres antallet.






