---
title: Oppsett av sjøreisestatus
description: Dette emnet beskriver hvordan du fastsetter statusverdiene som brukere kan tilordne til sjøreiser.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500892"
---
# <a name="voyage-status-setup"></a>Oppsett av sjøreisestatus

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

På siden **Sjøreisestatuser** fastsetter du settet med statusverdier som brukere kan tilordne til sjøreiser. Brukere kan tilordne statusverdier for sjøreiser til alle nivåer for en sjøreise: sjøreise, forsendelsescontainer, folio, bestillinger og vare (innkjøpslinjer og overføringsordrelinjer). De brukes til to formål:

- Informer brukeren om statusen til sjøreisen, forsendelsescontaineren, folioen, bestillingen eller varen (innkjøpslinjer og overføringsordrelinjer).
- Begrens bruken av kostnadsområdet ved å hindre endring eller sletting.

Hvis du vil konfigurere sjøreisestatusene, går du til **Netto innkjøpspris \> Oppsett \> Sjøreisestatuser**. Der kan du legge til, fjerne og redigere statuser ved hjelp av knappene i handlingsruten.

Hvert kostnadsområde har sitt eget sett og hierarki av sjøreisestatuser. Derfor må du først velge kostnadsområdet du vil vise eller opprette sjøreisestatuser for, i feltet **Kostnadsområde** på siden **Sjøreisestatuser**. Angi deretter verdier i feltene som er beskrevet i tabellen nedenfor, for hver sjøreisestatus, etter behov. Vær oppmerksom på at statusen for en sjøreise også kan endres automatisk av systemhendelser, for eksempel regler som er fastsatt ved hjelp av sporingskontrollsenteret.

| Felt | beskrivelse |
|---|---|
| Sjøreisestatus | Angi navnet på sjøreisestatusen. |
| beskrivelse | Angi en beskrivelse av sjøreisestatusen. |
| Endre | Merk av i denne avmerkingsboksen hvis brukere har tillatelse til å endre sjøreiser som har denne statusen. |
| Delete | Merk av i denne avmerkingsboksen hvis brukere har tillatelse til å slette sjøreiser som har denne statusen. |
| Obligatorisk | Merk av i denne avmerkingsboksen for å gjøre sjøreisestatusen obligatorisk, slik at den ikke kan hoppes over. |
| Overordnet | Bruk dette feltet til å opprette et hierarki blant statusverdiene. Sjøreisestatuser kan endres (manuelt eller automatisk) bare nedover i hierarkiet, fra overordnet status til en av dens underordnede statuser.

> [!NOTE]
> Du trenger bare konfigurere de spesifikke sjøreisestatusene som organisasjonen bruker. Typiske sjøreisestatuser inkluderer *Bekreftet*, *Varer i transitt*, *Mottatt*, *Klar til etterkalkulering* og *Kostnadsført*. Andre statuser kan imidlertid være til stede.
