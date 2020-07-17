---
title: Prosessautomatisering
description: Dette emnet inneholder detaljer om hvordan prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508191"
---
# <a name="process-automation"></a>Prosessautomatisering

[!include[banner](../includes/banner.md)]

Prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren. Den oppdaterte kalendervisningen for det planlagte arbeidet gir sluttbrukerne mulighet til å vise og utføre handlinger på planlagt og fullført arbeid.

## <a name="administration"></a>Administrasjon

Du finner siden for sentraladministrasjon for alle prosessautomatiseringer i Systemadministrasjon-modulen på **Oppsett**-menyen. Denne siden viser en liste over alle automatiserte prosesser (serier) som er konfigurert i systemet. Du kan også legge til nye prosessautomatiseringer direkte fra denne siden. Når en serie er definert, kan du administrere hver serie fra denne listen. Du kan velge å redigere hele serien, slette den, vise alle forekomster i en liste visning eller deaktivere serien hvis du vil stanse det planlagte arbeidet i en tidsperiode. 

## <a name="calendar-view"></a>Kalendervisning 
En av de viktigste fordelene med prosessautomatisering er muligheten til å se det planlagte arbeidet i en enkel kalendervisning.  I denne visningen kan du se arbeid for en uke om gangen. Du vil se denne visningen på høyre side av **Prosessautomatisering**-siden. Det vil bli fylt ut med det planlagte arbeidet for den valgte serien. 

[![Prosessautomatiseringskalender](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Forekomstendringer
Hver forekomst kan endres uten å påvirke andre forekomster som er definert av serien de kom fra. Forekomster av planlagt arbeid kan redigeres fra kalendervisningen ved å velge **Vis/rediger**-knappen og velge **Forekomst**. Dette gir deg tilgang til alle innstillingene som opprinnelig vises i veiviseren for serieoppsett, og gir deg muligheten til å utføre en engangsendring for den valgte forekomsten. En forekomst av planlagt arbeid kan også deaktiveres ved å velge **Deaktiver**-knappen fra kalendervisningen. 

## <a name="developer-documentation"></a>Utviklerdokumentasjon 
Utviklerdokumentasjon skrives for å tillate at utviklerne utvider rammeverket for prosessautomatisering. Denne dokumentasjonen gir informasjon om hvordan du kan opprette egendefinerte prosesser som må kjøres av den satsvise serveren som er planlagt med veiviseren for prosessautomatisering, og som vises automatisk i kalendervisningen.
