---
title: Prosessautomatisering
description: Dette emnet inneholder detaljer om hvordan prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
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
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690052"
---
# <a name="process-automation"></a>Prosessautomatisering

[!include[banner](../includes/banner.md)]

Prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren. Den oppdaterte kalendervisningen for det planlagte arbeidet gir sluttbrukerne mulighet til å vise og utføre handlinger på planlagt og fullført arbeid.

## <a name="administration"></a>Administrasjon

Du finner siden for sentraladministrasjon for alle prosessautomatiseringer i Systemadministrasjon-modulen på **Oppsett**-menyen. Denne siden viser en liste over alle automatiserte prosesser (serier) som er konfigurert i systemet. Du kan også legge til nye prosessautomatiseringer direkte fra denne siden. Når en serie er definert, kan du administrere hver serie fra denne listen. Du kan velge å redigere hele serien, slette den, vise alle forekomster i en liste visning eller deaktivere serien hvis du vil stanse det planlagte arbeidet i en tidsperiode. 

Prosesser som deaktiveres i funksjonsbehandling, vises ikke når funksjonen er deaktivert. I tillegg vil ikke planleggingsmotoren for prosessautomatisering planlegge noen forekomster eller bakgrunnsprosesser for en deaktivert funksjon. Når du aktiverer funksjonen på nytt, blir planlagte forekomster eller bakgrunnsprosesser i fortiden kjørt umiddelbart.

## <a name="calendar-view"></a>Kalendervisning 
En av de viktigste fordelene med prosessautomatisering er muligheten til å se det planlagte arbeidet i en enkel kalendervisning.  I denne visningen kan du se arbeid for en uke om gangen. Du vil se denne visningen på høyre side av **Prosessautomatisering**-siden. Det vil bli fylt ut med det planlagte arbeidet for den valgte serien. 

[![Prosessautomatiseringskalender](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Forekomstendringer
Hver forekomst kan endres uten å påvirke andre forekomster som er definert av serien de kom fra. Forekomster av planlagt arbeid kan redigeres fra kalendervisningen ved å velge **Vis/rediger**-knappen og velge **Forekomst**. Dette gir deg tilgang til alle innstillingene som opprinnelig vises i veiviseren for serieoppsett, og gir deg muligheten til å utføre en engangsendring for den valgte forekomsten. En forekomst av planlagt arbeid kan også deaktiveres ved å velge **Deaktiver**-knappen fra kalendervisningen. 

## <a name="developer-documentation"></a>Utviklerdokumentasjon 
Utviklerdokumentasjon skrives for å tillate at utviklerne utvider rammeverket for prosessautomatisering. Denne dokumentasjonen gir informasjon om hvordan du kan opprette egendefinerte prosesser som må kjøres av den satsvise serveren som er planlagt med veiviseren for prosessautomatisering, og som vises automatisk i kalendervisningen.
