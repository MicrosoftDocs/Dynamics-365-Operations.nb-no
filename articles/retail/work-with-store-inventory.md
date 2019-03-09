---
title: Butikklagerstyring
description: Dette emnet beskriver hvilke typer dokumenter du kan bruke til å styre lager.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "339240"
---
# <a name="store-inventory-management"></a>Butikklagerstyring

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvilke typer dokumenter du kan bruke til å styre lager.

Du kan bruke følgende typer dokumenter til å styre organisasjonens lager.

Når du arbeider med lager i Dynamics 365 for Retail og bruker salgsstedsprogrammet, er det viktig å merke seg at salgsstedet gir begrenset støtte for lagerdimensjoner og bestemt lagervaretyper.  

Salgsstedsløsningen støtter ikke følgende varekonfigurasjoner:
- Stykklistevarer (unntatt pakkeprodukter, som bruker noen av komponentene i stykklisterammeverket)
- Faktisk vekt-varer
- Partikontrollerte varer

Salgsstedsprogrammet støtter for øyeblikket ikke følgende sporingsdimensjoner på salgsstedet:
- Partisporingsdimensjon
- Eierdimensjon

Salgsstedsløsningen gir begrenset støtte for følgende dimensjoner. Begrenset støtte angir at salgsstedet kan plassere noen av disse dimensjonene i lagertransaksjoner automatisk som standard basert på lager-/butikkoppsettkonfigurasjonen. Salgsstedet støtter ikke dimensjonene fullstendig på samme måte som hvis en salgstransaksjon angis manuelt i ERP. 

- Plassering
- Nummerskilt (gjelder bare når **Bruk lagerstyringsprosesser** er aktivert på varen og i butikklageret)
- Serienummer
- Beholdningsstatus

> [!NOTE]
> Alle organisasjoner må teste varekonfigurasjoner gjennom POS i utviklings- eller testmiljøer før de distribueres til produksjon. Test varene ved å utføre vanlige hentesalgstransaksjoner og opprette kundeordrer (om nødvendig) via salgsstedet med varene dine. Testing må inneholde kjøring av fullstendige utdragsposteringsprosesser i testmiljøet og kontroll av at det ikke er noen problemer.
> Konfigurering av varer på en måte som ikke støttes av salgsstedsprogrammet, uten riktig testing, kan føre til at utdragsposteringsprosessen mislykkes i produksjonen uten en enkel måte å rette opp problemene. Partner- eller kundetilpassing til programmet kan eventuelt vurderes slik at disse posteringsprosessene kan fullføres. Hvis det ikke trengs tilpasninger, må organisasjonen sørge for at produktkonfigurasjonen av produktene er utført på en måte som støttes av standard salgsstedsprogram/ordreoppretting/utdragsposteringsprosess.

## <a name="purchase-orders"></a>Bestillinger

Bestillinger opprettes ved hovedkontoret. Hvis et lager for detaljhandel er inkludert i bestillingshodet, kan ordren mottas i butikken ved hjelp av Modern POS (MPOS) eller Cloud POS i Microsoft Dynamics 365 for Retail. Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret vises antallene som ble mottatt i butikken, i Dynamics 365 for Retail i **Motta nå**-feltet i bestillingen.

## <a name="transfer-orders"></a>Overføringsordrer

En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes fra. I dette tilfellet vises overføringsordren i butikken som en plukkforespørsel i Moderne salgssted eller Skysalgssted. Når de ønskede antallene er plukket, er lagres de og sendes til hovedkontoret. På hovedkontoret vises antallene som ble plukket i butikken, i Dynamics 365 for Retail i **Send nå**-feltet i overføringsordren. En overføringsordre kan angi at en bestemt butikk er en lokasjon som varer kan sendes til. I dette tilfellet vises overføringsordren i butikken som en mottaksforespørsel i Moderne salgssted eller Skysalgssted. Når antallene som er mottatt i butikken, er registrert, kan de lagres lokalt for ytterligere endring. Antallene kan eventuelt lagres og sendes til hovedkontoret. På hovedkontoret vises antallene som ble mottatt i butikken, i Dynamics 365 for Retail i **Motta nå**-feltet i overføringsordren.

## <a name="stock-counts"></a>Lagerantall

Lagertellinger kan være planlagt eller ikke planlagt. Planlagte lagertellinger startes ved hovedkontoret, som angir hvilke varer som skal telles. Hovedkontoret oppretter et opptellingsdokument som kan mottas i butikken, der faktisk beholdningsantall registreres i Moderne salgssted eller Skysalgssted. Ikke planlagte lagertellinger startes i en butikk, og faktisk beholdningsantall oppdateres i Moderne salgssted eller Skysalgssted. I motsetning til planlagte lagertellinger har ikke ikke-planlagte lagertellinger en forhåndsdefinert liste over varer. Når en lagertelling av en av disse typene er fullført, lagres og sendes den til hovedkontoret. Ved hovedkontoret valideres og posteres antallet.

## <a name="inventory-lookup"></a>Beholdningsoppslag

Det gjeldende produktantallet på lager for flere butikker og lagre kan vises på Beholdningsoppslag-siden. I tillegg til gjeldende antall på lager kan fremtidige antall tilgjengelig for ordre (ATP) vises for hver enkelt butikk. Dette gjør du ved å velge butikken du vil vise ATP-Antallet for, og deretter klikker du **Vis butikktilgjengelighet**.
