---
title: Prosessautomatisering
description: Denne artikkelen inneholder detaljer om hvordan prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: f13392fd6610735f8c539d42b62cf71cece71fba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898616"
---
# <a name="process-automation"></a>Prosessautomatisering

[!include[banner](../includes/banner.md)]

Prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren. Den oppdaterte kalendervisningen for det planlagte arbeidet gir sluttbrukerne mulighet til å vise og utføre handlinger på planlagt og fullført arbeid.

## <a name="administration"></a>Administrasjon

Du finner siden for sentraladministrasjon for alle prosessautomatiseringer i Systemadministrasjon-modulen på **Oppsett**-menyen. Denne siden viser en liste over alle automatiserte prosesser (serier) som er konfigurert i systemet. Du kan også legge til nye prosessautomatiseringer direkte fra denne siden. Når en serie er definert, kan du administrere hver serie fra denne listen. Du kan velge å redigere hele serien, slette den, vise alle forekomster i en liste visning eller deaktivere serien hvis du vil stanse det planlagte arbeidet i en tidsperiode. 

Prosesser som deaktiveres i funksjonsbehandling, vises ikke når funksjonen er deaktivert. I tillegg vil ikke planleggingsmotoren for prosessautomatisering planlegge noen forekomster eller bakgrunnsprosesser for en deaktivert funksjon. Når du aktiverer funksjonen på nytt, blir planlagte forekomster eller bakgrunnsprosesser i fortiden kjørt umiddelbart. Planleggingsmotoren for prosessautomatisering er avhengig av systemets satsvise jobb, **Avspørringssystem for prosessautomatisering** for å kjøres. Jobben bør ikke endres på noe tidspunkt. 

## <a name="calendar-view"></a>Kalendervisning

En av de viktigste fordelene med prosessautomatisering er muligheten til å se det planlagte arbeidet i en enkel kalendervisning.  I denne visningen kan du se arbeid for en uke om gangen. Du vil se denne visningen på høyre side av **Prosessautomatisering**-siden. Det vil bli fylt ut med det planlagte arbeidet for den valgte serien. 

[![Prosessautomatiseringskalender.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Forekomstendringer

Hver forekomst kan endres uten å påvirke andre forekomster som er definert av serien de kom fra. Forekomster av planlagt arbeid kan redigeres fra kalendervisningen ved å velge **Vis/rediger**-knappen og velge **Forekomst**. Denne siden gir deg tilgang til alle innstillingene som opprinnelig vises i veiviseren for serieoppsett, og gir deg muligheten til å utføre en engangsendring for den valgte forekomsten. En forekomst av planlagt arbeid kan også deaktiveres ved å velge **Deaktiver**-knappen fra kalendervisningen.

## <a name="developer-documentation"></a>Utviklerdokumentasjon

Rammeverk for prosessautomatisering gjør det mulig for utviklere å utvide rammeverket for prosessautomatisering. Dokumentasjonen for [Rammeverk for prosessautomatisering](../process-automation/process-automation-framework.md) gir informasjon om hvordan du kan opprette egendefinerte prosesser som må kjøres av den satsvise serveren som er planlagt med veiviseren for prosessautomatisering, og som vises automatisk i kalendervisningen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
