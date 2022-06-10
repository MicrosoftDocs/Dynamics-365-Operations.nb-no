---
title: Enheten for containeraktiviteter
description: Dette emnet gir informasjon om containeraktiviteter, som brukes til å spore fremdriften til forsendelsescontainere.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813100"
---
# <a name="container-activities-entity"></a>Enheten for containeraktiviteter

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Containeraktiviteter brukes til å spore fremdriften til forsendelsescontainere. Det opprettes en post for hver etappe som er tilordnet til reisemalen som velges når containeroppretting opprettes. Det opprettes også poster når forsendelsescontaineren via en dataenhet.

Informasjon om fremdriften til en forsendelsescontainer for transitt mottas ofte fra en ekstern kilde. Enheten for containeraktiviteter gjør det mulig for en ekstern kilde, for eksempel en fraktforsender, å oppdatere posten direkte. Det kreves derfor ingen manuell oppdatering av data.

## <a name="container-activities-itmcontaineractivityentity"></a>Containeraktiviteter (ITMContainerActivityEntity)

Du kan bruke enheten for containeraktiviteter (`ITMContainerActivityEntity`) til å opprette flere aktivitetsposter. Et fraktoversender kan eventuelt sende oppdateringer for en bekreftet **Faktisk sluttdato**-verdi.

| Navn | Tilordning | Datatype | Nøkkel | Obligatorisk |
|---|---|---|---|---|
| Faktisk sluttdato | ITMContainerActivityTable.ActualEndDate | Dato/klokkeslett | Nei | Nei |
| Leveringsmåte | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | Nei | Nei |
| Estimert sluttdato | ITMContainerActivityTable.EsimatedDate | Dato/klokkeslett | Nei | Nei |
| Linjenummer | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Ja** | Nei |
| Notater | ITMContainerActivityTable.Notes | nvarchar(MAX) | Nei | Nei |
| Aktivitet | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | Nei | **Ja** |
| Fraktcontainer | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Ja** | **Ja** |
| Sjøreise | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Ja** | **Ja** |
| Strekning | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | Nei | **Ja** |
| Tjenesteleverandør | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | Nei | Nei |
| Temperatur | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | Nei | Nei |
| Fartøy | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | Nei | Nei |
| Startdato | ITMContainerActivityTable.StartDate | Dato/klokkeslett | Nei | Nei |

## <a name="tracking-control"></a>Sporingskontroll

Sporingskontrollsenteret gjør det mulig å utløse en oppdatering av et bestemt kildefelt av en oppdatering av et bestemt målfelt. Hvis både verdien i kildefeltet og verdien i målfeltet oppdateres ved hjelp av enheten for containeraktiviteter, vil målfeltet vise enhetsverdien. Denne virkemåten er knyttet til sporing av kontrollposter som har en **Opprett type**-verdien *Leveringstid*.

For kostnadsområder som har verdien **Opprett type** for *Statusoppdatering* eller *Tom* (som er en brukerdefinert verdi), oppdaterer systemet status eller målfeltet i henhold til sporingskontrollkonfigurasjonen.

## <a name="calculated-fields"></a>Beregnede felt

Verdiene til følgende felt i en containeraktivitetspost beregnes på grunnlag av verdiene til andre felt. Selv om disse beregnede feltene ikke er inkludert i dataenheten, angis de hvis feltene beregningene er basert på, oppgis.

- **Estimerte dager** = **Estimert sluttdato** – **Startdato**
- **Faktiske dager** = **Faktisk sluttdato** – **Startdato**
