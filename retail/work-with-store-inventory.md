---
title: Behandle butikkbeholdning
description: "Denne artikkelen beskriver hvilke typer dokumenter som du kan bruke til å styre lager."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Behandle butikkbeholdning

Denne artikkelen beskriver hvilke typer dokumenter som du kan bruke til å styre lager.

Du kan bruke følgende typer dokumenter til å styre organisasjonens lager.

## <a name="purchase-orders"></a>Bestillinger
Bestillinger opprettes ved hovedkontoret. Hvis et lager for detaljhandel er inkludert i bestillingshodet, kan bestillingen mottas i butikken ved hjelp av moderne POS (MPOS) eller sky POS i Microsoft Dynamics 365 for operasjoner - detaljhandel. Når du har antallet som er mottatt på lageret, kan de lagres lokalt for ytterligere endringer. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret, antallene som ble mottatt på lageret, vises i Dynamics 365 for operasjoner, i den **får nå** på bestillingen.

## <a name="transfer-orders"></a>Overføringsordrer
En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes fra. I dette tilfellet vises overføringsordren i butikken som en plukking forespørsel i MPOS eller sky POS. Når antall er plukket, er de utført og sendt til hovedkontoret. På hovedkontoret, vises antallet som ble plukket i butikken i Dynamics 365 for operasjoner, i den **leverer nå** i overføringsordren. En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes til. I dette tilfellet vises overføringsordren i butikken som en mottakende forespørsel i MPOS eller sky POS. Når du har antallet som er mottatt på lageret, kan de lagres lokalt for ytterligere endringer. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret, antallene som ble mottatt på lageret, vises i Dynamics 365 for operasjoner, i den **får nå** i overføringsordren.

## <a name="stock-counts"></a>Lagerantall
Lagertellinger kan være planlagt eller ikke planlagt. Planlagte lagertellinger startes ved hovedkontoret, som angir hvilke varer som skal telles. Hovedkontoret oppretter et opptellingsdokument som kan mottas i butikken, der antall faktiske beholdningen lager angis i MPOS eller sky POS. Ikke planlagt lagerantall startes ved en butikk, og antall faktisk beholdning-aksjer er oppdatert i enten MPOS eller sky POS. I motsetning til planlagt lagerantall har ikke planlagt lagerantall ikke en forhåndsdefinert liste over elementer. Når en lagertelling av en av disse typene er fullført, lagres og sendes den til hovedkontoret. Ved hovedkontoret valideres og posteres antallet.




